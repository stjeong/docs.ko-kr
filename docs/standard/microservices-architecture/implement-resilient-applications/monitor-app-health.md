---
title: 상태 모니터링
description: 상태 모니터링을 구현하는 한 가지 방법을 살펴봅니다.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/16/2018
ms.openlocfilehash: 666b55608ca4e5d18448e1a0b4a1735f3e856474
ms.sourcegitcommit: 542aa405b295955eb055765f33723cb8b588d0d0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/17/2019
ms.locfileid: "54362485"
---
# <a name="health-monitoring"></a><span data-ttu-id="340ae-103">상태 모니터링</span><span class="sxs-lookup"><span data-stu-id="340ae-103">Health monitoring</span></span>

<span data-ttu-id="340ae-104">상태 모니터링은 컨테이너 및 마이크로 서비스의 상태에 대해 거의 실시간으로 정보를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-104">Health monitoring can allow near-real-time information about the state of your containers and microservices.</span></span> <span data-ttu-id="340ae-105">상태 모니터링은 마이크로 서비스를 작동하는 데 있어 여러 가지 측면에서 매우 중요하며, 나중에 설명하는 대로 오케스트레이터에서 애플리케이션을 부분적으로 업그레이드할 때 특히 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-105">Health monitoring is critical to multiple aspects of operating microservices and is especially important when orchestrators perform partial application upgrades in phases, as explained later.</span></span>

<span data-ttu-id="340ae-106">마이크로 서비스 기반 애플리케이션은 종종 하트비트 또는 상태 검사를 사용하여 성능 모니터, 스케줄러 및 오케스트레이터에서 다양한 서비스를 추적할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-106">Microservices-based applications often use heartbeats or health checks to enable their performance monitors, schedulers, and orchestrators to keep track of the multitude of services.</span></span> <span data-ttu-id="340ae-107">서비스에서 요청 시 또는 일정에 따라 “활성(I’m alive)” 신호를 보낼 수 없는 경우, 업데이트를 배포할 때 애플리케이션이 위험에 직면할 수 있고, 단순히 오류를 너무 늦게 검색해서 연속 오류를 방지하지 못해 심각한 중단 상태에 놓일 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-107">If services cannot send some sort of “I’m alive” signal, either on demand or on a schedule, your application might face risks when you deploy updates, or it might just detect failures too late and not be able to stop cascading failures that can end up in major outages.</span></span>

<span data-ttu-id="340ae-108">일반적인 모델에서 서비스는 상태에 대한 보고서를 보내고, 해당 정보를 집계하여 애플리케이션 상태 전체에 대한 보기를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-108">In the typical model, services send reports about their status, and that information is aggregated to provide an overall view of the state of health of your application.</span></span> <span data-ttu-id="340ae-109">오케스트레이터를 사용하는 경우 클러스터가 적절하게 작동할 수 있도록 오케스트레이터의 클러스터에 상태 정보를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-109">If you're using an orchestrator, you can provide health information to your orchestrator’s cluster, so that the cluster can act accordingly.</span></span> <span data-ttu-id="340ae-110">애플리케이션에 맞게 사용자 지정된 고품질 상태 보고에 투자하는 경우 실행 중인 애플리케이션에 대한 문제를 훨씬 쉽게 검색하고 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-110">If you invest in high-quality health reporting that's customized for your application, you can detect and fix issues for your running application much more easily.</span></span>

## <a name="implement-health-checks-in-aspnet-core-services"></a><span data-ttu-id="340ae-111">ASP.NET Core 서비스에서 상태 검사 구현</span><span class="sxs-lookup"><span data-stu-id="340ae-111">Implement health checks in ASP.NET Core services</span></span>

<span data-ttu-id="340ae-112">ASP.NET Core 마이크로 서비스 또는 웹 애플리케이션을 개발할 때 ASP.NET 팀에서 ‘상태 검사’라는 대역 외 라이브러리(ASP.NET Core의 공식적인 구성 요소는 아니며 더 이상 사용되지 않음)를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-112">When developing an ASP.NET Core microservice or web application, you can use an experimental out-of-band library (not official as part of ASP.NETCore and now deprecated) named *Health Checks* from the ASP.NET team.</span></span> <span data-ttu-id="340ae-113">이 [dotnet-architecture GitHub 리포지토리](https://github.com/dotnet-architecture/HealthChecks)에서 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-113">It's available at this [dotnet-architecture GitHub repository](https://github.com/dotnet-architecture/HealthChecks).</span></span> <span data-ttu-id="340ae-114">그러나 ‘상태 검사’의 공식 버전은 [ASP.NET Core 2.2에 릴리스](https://github.com/aspnet/Announcements/issues/307)됩니다(2018년 말까지 공식적으로 릴리스됨).</span><span class="sxs-lookup"><span data-stu-id="340ae-114">However, the official version of *Health Checks* [will be released in ASP.NET Core 2.2](https://github.com/aspnet/Announcements/issues/307) (Should be officially released by the end of 2018).</span></span>

<span data-ttu-id="340ae-115">이 라이브러리는 사용하기 쉽고 애플리케이션에 필요한 특정 외부 리소스(예: SQL Server 데이터베이스 또는 원격 API)가 사용할 수 있습니다. 작동하는지 확인할 수 있는 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-115">This library is easy to use and provides features that let you validate that any specific external resource needed for your application (like a SQL Server database or remote API) is working properly.</span></span> <span data-ttu-id="340ae-116">이 라이브러리를 사용하면 나중에 설명하는 대로 정상 리소스에 대한 의미를 결정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-116">When you use this library, you can also decide what it means that the resource is healthy, as we explain later.</span></span>

<span data-ttu-id="340ae-117">이 라이브러리를 사용하려면 먼저 마이크로 서비스에서 라이브러리를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-117">In order to use this library, you need to first use the library in your microservices.</span></span> <span data-ttu-id="340ae-118">다음으로, 상태 보고서를 쿼리하는 프런트 엔드 애플리케이션이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-118">Second, you need a front-end application that queries for the health reports.</span></span> <span data-ttu-id="340ae-119">프런트 엔드 애플리케이션은 사용자 지정 보고 애플리케이션이거나 성능 상태에 따라 대응할 수 있는 오케스트레이터 자체일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-119">That front-end application could be a custom reporting application, or it could be an orchestrator itself that can react accordingly to the health states.</span></span>

### <a name="use-the-healthchecks-library-in-your-back-end-aspnet-microservices"></a><span data-ttu-id="340ae-120">백 엔드 ASP.NET 마이크로 서비스에서 HealthChecks 라이브러리 사용</span><span class="sxs-lookup"><span data-stu-id="340ae-120">Use the HealthChecks library in your back-end ASP.NET microservices</span></span>

<span data-ttu-id="340ae-121">eShopOnContainers 샘플 애플리케이션에서 HealthChecks 라이브러리가 사용되는 방식을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-121">You can see how the HealthChecks library is used in the eShopOnContainers sample application.</span></span> <span data-ttu-id="340ae-122">시작하려면 각 마이크로 서비스에 대한 성능 상태를 구성하는 항목을 정의해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-122">To begin, you need to define what constitutes a healthy status for each microservice.</span></span> <span data-ttu-id="340ae-123">샘플 애플리케이션에서 마이크로 서비스 API가 HTTP를 통해 액세스할 수 있고 관련 SQL Server 데이터베이스도 사용할 수 있으면 마이크로 서비스가 정상입니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-123">In the sample application, the microservices are healthy if the microservice API is accessible via HTTP and if its related SQL Server database is also available.</span></span>

<span data-ttu-id="340ae-124">나중에 HealthChecks 라이브러리를 NuGet 패키지로 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-124">In the future, you'll be able to install the HealthChecks library as a NuGet package.</span></span> <span data-ttu-id="340ae-125">그러나 이 문서를 작성한 시점 이후로는 코드를 솔루션의 일부로 다운로드하고 컴파일해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-125">But as of this writing, you need to download and compile the code as part of your solution.</span></span> <span data-ttu-id="340ae-126">[https://github.com/dotnet-architecture/HealthChecks](<https://github.com/dotnet-architecture/HealthChecks>)에서 사용할 수 있는 코드를 복제하고 솔루션에 다음 폴더를 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-126">Clone the code available at <https://github.com/dotnet-architecture/HealthChecks> and copy the following folders to your solution:</span></span>

- <span data-ttu-id="340ae-127">src/common</span><span class="sxs-lookup"><span data-stu-id="340ae-127">src/common</span></span>
- <span data-ttu-id="340ae-128">src/Microsoft.AspNetCore.HealthChecks</span><span class="sxs-lookup"><span data-stu-id="340ae-128">src/Microsoft.AspNetCore.HealthChecks</span></span>
- <span data-ttu-id="340ae-129">src/Microsoft.Extensions.HealthChecks</span><span class="sxs-lookup"><span data-stu-id="340ae-129">src/Microsoft.Extensions.HealthChecks</span></span>
- <span data-ttu-id="340ae-130">src/Microsoft.Extensions.HealthChecks.SqlServer</span><span class="sxs-lookup"><span data-stu-id="340ae-130">src/Microsoft.Extensions.HealthChecks.SqlServer</span></span>

<span data-ttu-id="340ae-131">Azure(Microsoft.Extensions.HealthChecks.AzureStorage)에 대한 것과 같은 추가 검사를 사용할 수도 있지만, 이 버전의 eShopOnContainers에는 Azure에 대한 종속성이 없으므로 이러한 검사는 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-131">You could also use additional checks like the ones for Azure (Microsoft.Extensions.HealthChecks.AzureStorage), but since this version of eShopOnContainers does not have any dependency on Azure, you do not need it.</span></span> <span data-ttu-id="340ae-132">eShopOnContainers는 ASP.NET Core를 기반으로 하므로 ASP.NET 상태 검사가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-132">You do not need the ASP.NET health checks, because eShopOnContainers is based on ASP.NET Core.</span></span>

<span data-ttu-id="340ae-133">그림 8-7에서는 모든 마이크로 서비스에서 구성 요소로 사용할 준비가 된 Visual Studio의 HealthChecks 라이브러리를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-133">Figure 8-7 shows the HealthChecks library in Visual Studio, ready to be used as a building block by any microservices.</span></span>

![3개의 프로젝트를 표시하는 HealthChecks 폴더의 솔루션 탐색기 보기입니다.](./media/image6.png)

<span data-ttu-id="340ae-135">**그림 8-7**.</span><span class="sxs-lookup"><span data-stu-id="340ae-135">**Figure 8-7**.</span></span> <span data-ttu-id="340ae-136">Visual Studio 솔루션의 ASP.NET Core HealthChecks 라이브러리 소스 코드</span><span class="sxs-lookup"><span data-stu-id="340ae-136">ASP.NET Core HealthChecks library source code in a Visual Studio solution</span></span>

<span data-ttu-id="340ae-137">앞에서 소개한 대로 각 마이크로 서비스 프로젝트에서 가장 먼저 수행할 작업은 세 가지 HealthChecks 라이브러리에 대한 참조를 추가하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-137">As introduced earlier, the first thing to do in each microservice project is to add a reference to the three HealthChecks libraries.</span></span> <span data-ttu-id="340ae-138">그런 다음, 해당 마이크로 서비스에서 수행하려는 상태 검사 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-138">After that, you add the health check actions that you want to perform in that microservice.</span></span> <span data-ttu-id="340ae-139">이러한 작업은 기본적으로 다른 마이크로 서비스(HttpUrlCheck) 또는 데이터베이스(현재의 SQL Server 데이터베이스에 대한 SqlCheck\*)에 종속됩니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-139">These actions are basically dependencies on other microservices (HttpUrlCheck) or databases (currently SqlCheck\* for SQL Server databases).</span></span> <span data-ttu-id="340ae-140">작업은 각 ASP.NET 마이크로 서비스 또는 ASP.NET 웹 애플리케이션의 Startup 클래스 내에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-140">You add the action within the Startup class of each ASP.NET microservice or ASP.NET web application.</span></span>

<span data-ttu-id="340ae-141">각 서비스 또는 웹 애플리케이션은 HTTP 또는 데이터베이스 종속성을 모두 하나의 AddHealthCheck 메서드로 추가하여 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-141">Each service or web application should be configured by adding all its HTTP or database dependencies as one AddHealthCheck method.</span></span> <span data-ttu-id="340ae-142">예를 들어 eShopOnContainers의 MVC 웹 애플리케이션은 여러 서비스에 종속되므로 상태 검사에 몇 가지 AddCheck 메서드가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-142">For example, the MVC web application from eShopOnContainers depends on many services, therefore has several AddCheck methods added to the health checks.</span></span>

<span data-ttu-id="340ae-143">예를 들어 다음 (간소화된) 코드에서 카탈로그 마이크로 서비스가 SQL Server 데이터베이스에 대한 종속성을 추가하는 방법을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-143">For instance, in the following (simplified) code you can see how the catalog microservice adds a dependency on its SQL Server database.</span></span>

```csharp
// Startup.cs from Catalog.api microservice
//
public class Startup
{
    public void ConfigureServices(IServiceCollection services)
    {
        // Add framework services
        services.AddHealthChecks(checks =>
        {
            checks.AddSqlCheck("CatalogDb", Configuration["ConnectionString"]);
        });
        // Other services
    }
}
```

<span data-ttu-id="340ae-144">그러나 eShopOnContainers의 MVC 웹 애플리케이션에는 나머지 마이크로 서비스에 대한 여러 종속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-144">However, the MVC web application of eShopOnContainers has multiple dependencies on the rest of the microservices.</span></span> <span data-ttu-id="340ae-145">따라서 다음 (간소화된) 예제와 같이 각 마이크로 서비스에 대해 하나의 AddUrlCheck 메서드를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-145">Therefore, it calls one AddUrlCheck method for each microservice, as shown in the following (simplified) example:</span></span>

```csharp
// Startup.cs from the MVC web app
public class Startup
{
    public void ConfigureServices(IServiceCollection services)
    {
        services.AddMvc();
        services.Configure<AppSettings>(Configuration);
        services.AddHealthChecks(checks =>
        {
            checks.AddUrlCheck(Configuration["CatalogUrl"]);
            checks.AddUrlCheck(Configuration["OrderingUrl"]);
            checks.AddUrlCheck(Configuration["BasketUrl"]);
            checks.AddUrlCheck(Configuration["IdentityUrl"]);
        });
    }
}
```

<span data-ttu-id="340ae-146">따라서 마이크로 서비스는 모든 검사가 정상일 때까지 "정상" 상태를 제공하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-146">Thus, a microservice will not provide a “healthy” status until all its checks are healthy as well.</span></span>

<span data-ttu-id="340ae-147">마이크로 서비스가 서비스 또는 SQL Server에 종속되지 않으면 정상("OK") 검사를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-147">If the microservice does not have a dependency on a service or on SQL Server, you should just add a Healthy("Ok") check.</span></span> <span data-ttu-id="340ae-148">다음 코드는 eShopOnContainers `basket.api` 마이크로 서비스에서 가져온 것입니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-148">The following code is from the eShopOnContainers `basket.api` microservice.</span></span> <span data-ttu-id="340ae-149">(장바구니 마이크로 서비스에서 Redis 캐시를 사용하지만, 라이브러리에는 아직 Redis 상태 검사 공급자가 포함되어 있지 않습니다.)</span><span class="sxs-lookup"><span data-stu-id="340ae-149">(The basket microservice uses the Redis cache, but the library does not yet include a Redis health check provider.)</span></span>

```csharp
services.AddHealthChecks(checks =>
{
    checks.AddValueTaskCheck("HTTP Endpoint", () => new
        ValueTask<IHealthCheckResult>(HealthCheckResult.Healthy("Ok")));
});
```

<span data-ttu-id="340ae-150">서비스 또는 웹 애플리케이션에서 상태 검사 엔드포인트를 노출하려면 `UseHealthChecks([*url_for_health_checks*])` 확장 메서드를 사용하도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-150">For a service or web application to expose the health check endpoint, it has to enable the `UseHealthChecks([*url_for_health_checks*])` extension method.</span></span> <span data-ttu-id="340ae-151">이 메서드는 다음 간소화된 코드와 같이 <xref:Microsoft.AspNetCore.WebHost.CreateDefaultBuilder> 바로 뒤에서 ASP.NET Core 서비스 또는 웹 애플리케이션의 `Program` 클래스 main 메서드에 있는 `WebHostBuilder` 수준으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-151">This method goes at the `WebHostBuilder` level in the main method of the `Program` class of your ASP.NET Core service or web application, right after <xref:Microsoft.AspNetCore.WebHost.CreateDefaultBuilder> as shown in the following simplified code:</span></span>

```csharp
namespace Microsoft.eShopOnContainers.WebMVC
{
    public class Program
    {
        public static void Main(string[] args)
        {
            var host = WebHost.CreateDefaultBuilder(args)
                .UseHealthChecks("/hc")
                .UseContentRoot(Directory.GetCurrentDirectory())
                .UseStartup<Startup>()
                .Build();

            host.Run();
        }
    }
}
```

<span data-ttu-id="340ae-152">프로세스는 각 마이크로 서비스에서 /hc 엔드포인트를 노출하는 방식으로 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-152">The process works this way: each microservice exposes the endpoint /hc.</span></span> <span data-ttu-id="340ae-153">이 엔드포인트는 HealthChecks 라이브러리 ASP.NET Core 미들웨어에서 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-153">That endpoint is created by the HealthChecks library ASP.NET Core middleware.</span></span> <span data-ttu-id="340ae-154">해당 엔드포인트가 호출되면 Startup 클래스의 AddHealthChecks 메서드에 구성된 상태 검사를 모두 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-154">When that endpoint is invoked, it runs all the health checks that are configured in the AddHealthChecks method in the Startup class.</span></span>

<span data-ttu-id="340ae-155">UseHealthChecks 메서드에는 포트 또는 경로가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-155">The UseHealthChecks method expects a port or a path.</span></span> <span data-ttu-id="340ae-156">해당 포트 또는 경로는 서비스의 성능 상태를 확인하는 데 사용할 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-156">That port or path is the endpoint to use to check the health state of the service.</span></span> <span data-ttu-id="340ae-157">예를 들어 카탈로그 마이크로 서비스는/hc 경로를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-157">For instance, the catalog microservice uses the path /hc.</span></span>

### <a name="cache-health-check-responses"></a><span data-ttu-id="340ae-158">상태 검사 응답 캐싱</span><span class="sxs-lookup"><span data-stu-id="340ae-158">Cache health check responses</span></span>

<span data-ttu-id="340ae-159">서비스에서 DoS(서비스 거부) 공격이 발생하지 않도록 하려거나 단순히 리소스를 너무 자주 검사하여 서비스 성능에 영향을 미치지 않으려고 하는 경우에는 각 상태 검사에 대해 반환을 캐시하고 캐시 기간을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-159">Since you do not want to cause a Denial of Service (DoS) in your services, or you simply do not want to impact service performance by checking resources too frequently, you can cache the returns and configure a cache duration for each health check.</span></span>

<span data-ttu-id="340ae-160">기본적으로 캐시 기간은 내부적으로 5분으로 설정되지만, 다음 코드와 같이 각 상태 검사에 대한 해당 캐시 기간을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-160">By default, the cache duration is internally set to 5 minutes, but you can change that cache duration on each health check, as in the following code:</span></span>

```csharp
checks.AddUrlCheck(Configuration["CatalogUrl"],1); // 1 min as cache duration
```

### <a name="query-your-microservices-to-report-about-their-health-status"></a><span data-ttu-id="340ae-161">마이크로 서비스를 쿼리하여 성능 상태에 대해 보고</span><span class="sxs-lookup"><span data-stu-id="340ae-161">Query your microservices to report about their health status</span></span>

<span data-ttu-id="340ae-162">이 문서에 설명된 대로 상태 검사를 구성했으며 Docker에서 마이크로 서비스가 실행 중인 경우 브라우저에서 정상인지 여부를 직접 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-162">When you've configured health checks as described in this article and you have the microservice running in Docker, you can directly check from a browser if it's healthy.</span></span>

<span data-ttu-id="340ae-163">그림 8-8과 같이 컨테이너 포트를 Docker 호스트에 게시해야 외부 Docker 호스트 IP 또는 `localhost`를 통해 컨테이너에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-163">You have to publish the container port in the Docker host, so you can access the container through the external Docker host IP or through `localhost`, as shown in figure 8-8.</span></span>

![상태 검사에서 반환된 JSON 응답의 브라우저 보기](./media/image7.png)

<span data-ttu-id="340ae-165">**그림 8-8**.</span><span class="sxs-lookup"><span data-stu-id="340ae-165">**Figure 8-8**.</span></span> <span data-ttu-id="340ae-166">브라우저에서 단일 서비스의 성능 상태 검사</span><span class="sxs-lookup"><span data-stu-id="340ae-166">Checking health status of a single service from a browser</span></span>

<span data-ttu-id="340ae-167">이 테스트에서는 catalog.api 마이크로 서비스(5101 포트에서 실행 중)가 정상이며, JSON에서 200 HTTP 상태 및 상태 정보를 반환한다는 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-167">In that test, you can see that the catalog.api microservice (running on port 5101) is healthy, returning HTTP status 200 and status information in JSON.</span></span> <span data-ttu-id="340ae-168">또한 이 서비스는 내부적으로 SQL Server 데이터베이스 종속성의 상태를 검사했고 상태 검사에서 직접 정상으로 보고되었음을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-168">It also means that internally the service also checked the health of its SQL Server database dependency and that health check was reported itself as healthy.</span></span>

## <a name="use-watchdogs"></a><span data-ttu-id="340ae-169">Watchdog 사용</span><span class="sxs-lookup"><span data-stu-id="340ae-169">Use watchdogs</span></span>

<span data-ttu-id="340ae-170">Watchdog는 앞에서 소개한 `HealthChecks` 라이브러리로 쿼리하여 서비스 전반의 상태와 로드를 감시하고 마이크로 서비스에 대한 상태를 보고할 수 있는 별도의 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-170">A watchdog is a separate service that can watch health and load across services, and report health about the microservices by querying with the `HealthChecks` library introduced earlier.</span></span> <span data-ttu-id="340ae-171">이렇게 하면 단일 서비스의 보기를 기반으로 하여 검색되지 않는 오류를 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-171">This can help prevent errors that would not be detected based on the view of a single service.</span></span> <span data-ttu-id="340ae-172">또한 Watchdog은 사용자 개입 없이 알려진 조건에 대한 수정 작업을 수행할 수 있는 코드를 호스팅하는 데 적합한 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-172">Watchdogs also are a good place to host code that can perform remediation actions for known conditions without user interaction.</span></span>

<span data-ttu-id="340ae-173">eShopOnContainers 샘플에는 그림 8-9와 같이 샘플 상태 검사 보고서를 표시하는 웹 페이지가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-173">The eShopOnContainers sample contains a web page that displays sample health check reports, as shown in Figure 8-9.</span></span> <span data-ttu-id="340ae-174">단지 eShopOnContainers의 마이크로 서비스 및 웹 애플리케이션 상태만 표시하므로 가장 간단한 Watchdog입니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-174">This is the simplest watchdog you could have since it only shows the state of the microservices and web applications in eShopOnContainers.</span></span> <span data-ttu-id="340ae-175">일반적으로 비정상 상태가 검색되면 Watchdog에서 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-175">Usually a watchdog also takes actions when it detects unhealthy states.</span></span>

![eShopOnContainers에서 마이크로 서비스 5개의 성능 상태를 표시하는 WebStatus 앱의 브라우저 보기](./media/image8.png)

<span data-ttu-id="340ae-177">**그림 8-9**.</span><span class="sxs-lookup"><span data-stu-id="340ae-177">**Figure 8-9**.</span></span> <span data-ttu-id="340ae-178">eShopOnContainers의 샘플 상태 검사 보고서</span><span class="sxs-lookup"><span data-stu-id="340ae-178">Sample health check report in eShopOnContainers</span></span>

<span data-ttu-id="340ae-179">요약하면, ASP.NET Core HealthChecks 라이브러리의 ASP.NET 미들웨어는 각 마이크로 서비스에 대해 단일 상태 검사 엔드포인트를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-179">In summary, the ASP.NET middleware of the ASP.NET Core HealthChecks library provides a single health check endpoint for each microservice.</span></span> <span data-ttu-id="340ae-180">이렇게 하면 내부에 정의된 모든 상태 검사가 실행되고, 모든 검사에 따라 전체 성능 상태가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-180">This will execute all the health checks defined within it and return an overall health state depending on all those checks.</span></span>

<span data-ttu-id="340ae-181">HealthChecks 라이브러리는 향후 외부 리소스에 대한 새로운 상태 검사를 통해 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-181">The HealthChecks library is extensible through new health checks of future external resources.</span></span> <span data-ttu-id="340ae-182">예를 들어 나중에 Redis 캐시 및 다른 데이터베이스에 대한 상태 검사가 라이브러리에 제공될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-182">For example, we expect that in the future the library will have health checks for Redis cache and for other databases.</span></span> <span data-ttu-id="340ae-183">라이브러리를 사용하면 여러 서비스 또는 애플리케이션 종속성을 통해 상태를 보고할 수 있고, 이러한 상태 검사에 따라 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-183">The library allows health reporting by multiple service or application dependencies, and you can then take actions based on those health checks.</span></span>

## <a name="health-checks-when-using-orchestrators"></a><span data-ttu-id="340ae-184">오케스트레이터 사용 시의 상태 검사</span><span class="sxs-lookup"><span data-stu-id="340ae-184">Health checks when using orchestrators</span></span>

<span data-ttu-id="340ae-185">Kubernetes 및 Service Fabric과 같은 오케스트레이션은 마이크로 서비스의 가용성을 모니터링하기 위해 정기적으로 마이크로 서비스 테스트 요청을 보내 상태 검사를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-185">To monitor the availability of your microservices, orchestrators like Kubernetes and Service Fabric periodically perform health checks by sending requests to test the microservices.</span></span> <span data-ttu-id="340ae-186">오케스트레이터에서 비정상 서비스/컨테이너로 인식하면 해당 인스턴스에 대한 요청 라우팅을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-186">When an orchestrator determines that a service/container is unhealthy, it stops routing requests to that instance.</span></span> <span data-ttu-id="340ae-187">또한 일반적으로 해당 컨테이너의 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-187">It also usually creates a new instance of that container.</span></span>

<span data-ttu-id="340ae-188">예를 들어 대부분의 오케스트레이터에서 상태 검사를 사용하여 가동 중지 시간이 없는 배포를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-188">For instance, most orchestrators can use health checks to manage zero-downtime deployments.</span></span> <span data-ttu-id="340ae-189">서비스/컨테이너의 상태가 정상으로 변경될 때만 오케스트레이터에서 트래픽을 서비스/컨테이너 인스턴스로 라우팅하기 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-189">Only when the status of a service/container changes to healthy will the orchestrator start routing traffic to service/container instances.</span></span>

<span data-ttu-id="340ae-190">상태 모니터링은 오케스트레이터에서 애플리케이션 업그레이드를 수행할 때 특히 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-190">Health monitoring is especially important when an orchestrator performs an application upgrade.</span></span> <span data-ttu-id="340ae-191">Azure Service Fabric과 같은 일부 오케스트레이터는 서비스를 단계별로 업데이트합니다. 예를 들어 애플리케이션 업그레이드마다 클러스터 표면의 1/5을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-191">Some orchestrators (like Azure Service Fabric) update services in phases—for example, they might update one-fifth of the cluster surface for each application upgrade.</span></span> <span data-ttu-id="340ae-192">동시에 업그레이드되는 노드 집합을 ‘업그레이드 도메인’이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-192">The set of nodes that's upgraded at the same time is referred to as an *upgrade domain*.</span></span> <span data-ttu-id="340ae-193">각 업그레이드 도메인을 업그레이드하고 사용자가 사용할 수 있게 되면, 먼저 해당 업그레이드 도메인이 상태 검사를 통과한 후에 배포가 다음 업그레이드 도메인으로 이동해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-193">After each upgrade domain has been upgraded and is available to users, that upgrade domain must pass health checks before the deployment moves to the next upgrade domain.</span></span>

<span data-ttu-id="340ae-194">서비스 상태의 또 다른 측면은 서비스의 메트릭을 보고하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-194">Another aspect of service health is reporting metrics from the service.</span></span> <span data-ttu-id="340ae-195">이는 Service Fabric과 같은 일부 오케스트레이터의 상태 모델에 대한 고급 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-195">This is an advanced capability of the health model of some orchestrators, like Service Fabric.</span></span> <span data-ttu-id="340ae-196">메트릭은 리소스 사용량의 균형을 조정하는 데 사용되므로 오케스트레이터를 사용할 때 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-196">Metrics are important when using an orchestrator because they are used to balance resource usage.</span></span> <span data-ttu-id="340ae-197">또한 메트릭은 시스템 상태를 나타내는 지표가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-197">Metrics also can be an indicator of system health.</span></span> <span data-ttu-id="340ae-198">예를 들어 많은 마이크로 서비스가 있는 애플리케이션이 있을 수 있으며, 각 인스턴스에서 RPS(초당 요청 수)를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-198">For example, you might have an application that has many microservices, and each instance reports a requests-per-second (RPS) metric.</span></span> <span data-ttu-id="340ae-199">한 서비스에서 다른 서비스보다 더 많은 리소스(메모리, 프로세서 등)를 사용하는 경우, 오케스트레이터는 클러스터에서 서비스 인스턴스를 이동하여 리소스 사용률을 유지하려고 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-199">If one service is using more resources (memory, processor, etc.) than another service, the orchestrator could move service instances around in the cluster to try to maintain even resource utilization.</span></span>

<span data-ttu-id="340ae-200">Azure Service Fabric은 단순한 상태 검사보다 더 향상된 고급 기능을 갖춘 자체의 [상태 모니터링 모델](/azure/service-fabric/service-fabric-health-introduction)을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-200">Note that Azure Service Fabric provides its own [Health Monitoring model](/azure/service-fabric/service-fabric-health-introduction), which is more advanced than simple health checks.</span></span>

## <a name="advanced-monitoring-visualization-analysis-and-alerts"></a><span data-ttu-id="340ae-201">고급 모니터링: 시각화, 분석 및 경고</span><span class="sxs-lookup"><span data-stu-id="340ae-201">Advanced monitoring: visualization, analysis, and alerts</span></span>

<span data-ttu-id="340ae-202">모니터링의 마지막 부분은 이벤트 스트림을 시각화하고, 서비스 성능에 대해 보고하고, 문제가 검색되면 경고하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-202">The final part of monitoring is visualizing the event stream, reporting on service performance, and alerting when an issue is detected.</span></span> <span data-ttu-id="340ae-203">이 모니터링 측면에 대해 서로 다른 솔루션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-203">You can use different solutions for this aspect of monitoring.</span></span>

<span data-ttu-id="340ae-204">[ASP.NET Core HealthChecks](https://github.com/dotnet-architecture/HealthChecks)에 대해 설명할 때 보여 준 사용자 지정 페이지와 같이 서비스 상태를 표시하는 간단한 사용자 지정 애플리케이션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-204">You can use simple custom applications showing the state of your services, like the custom page shown when explaining the [ASP.NET Core HealthChecks](https://github.com/dotnet-architecture/HealthChecks).</span></span> <span data-ttu-id="340ae-205">또는 Azure Application Insights와 같은 고급 도구를 사용하여 이벤트 스트림에 따라 경고를 발생시킬 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-205">Or you could use more advanced tools like Azure Application Insights to raise alerts based on the stream of events.</span></span>

<span data-ttu-id="340ae-206">마지막으로 모든 이벤트 스트림을 저장하는 경우 Microsoft Power BI 또는 기타 솔루션(예: Kibana 또는 Splunk)을 사용하여 데이터를 시각화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340ae-206">Finally, if you're storing all the event streams, you can use Microsoft Power BI or other solutions like Kibana or Splunk to visualize the data.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="340ae-207">추가 자료</span><span class="sxs-lookup"><span data-stu-id="340ae-207">Additional resources</span></span>

- <span data-ttu-id="340ae-208">**ASP.NET Core HealthChecks**(실험적 릴리스)\\</span><span class="sxs-lookup"><span data-stu-id="340ae-208">**ASP.NET Core HealthChecks** (experimental release)\\</span></span>
  [*https://github.com/dotnet-architecture/HealthChecks/*](https://github.com/dotnet-architecture/HealthChecks/)

- <span data-ttu-id="340ae-209">**Service Fabric 상태 모니터링 소개**\\</span><span class="sxs-lookup"><span data-stu-id="340ae-209">**Introduction to Service Fabric health monitoring**\\</span></span>
  [*https://docs.microsoft.com/azure/service-fabric/service-fabric-health-introduction*](/azure/service-fabric/service-fabric-health-introduction)

- <span data-ttu-id="340ae-210">**Azure Application Insights**\\</span><span class="sxs-lookup"><span data-stu-id="340ae-210">**Azure Application Insights**\\</span></span>
  [*https://azure.microsoft.com/services/application-insights/*](https://azure.microsoft.com/services/application-insights/)

- <span data-ttu-id="340ae-211">**Microsoft Operations Management Suite**\\</span><span class="sxs-lookup"><span data-stu-id="340ae-211">**Microsoft Operations Management Suite**\\</span></span>
  [*https://www.microsoft.com/cloud-platform/operations-management-suite*](https://www.microsoft.com/cloud-platform/operations-management-suite)

>[!div class="step-by-step"]
><span data-ttu-id="340ae-212">[이전](implement-circuit-breaker-pattern.md)
>[다음](../secure-net-microservices-web-applications/index.md)</span><span class="sxs-lookup"><span data-stu-id="340ae-212">[Previous](implement-circuit-breaker-pattern.md)
[Next](../secure-net-microservices-web-applications/index.md)</span></span>