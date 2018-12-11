---
title: 클라우드에 대 한 복원 력 있는 서비스를 빌드하십시오. 클라우드의 일시적 오류 포용
description: Azure 클라우드 및 Windows 컨테이너를 사용 하 여 기존.NET 응용 프로그램 현대화 | 클라우드에 대 한 복원 력 있는 서비스를 빌드하십시오. 클라우드의 일시적 오류 포용
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/30/2018
ms.openlocfilehash: 16228321cc788b381603513213130415eb73a95c
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53128858"
---
# <a name="build-resilient-services-ready-for-the-cloud-embrace-transient-failures-in-the-cloud"></a><span data-ttu-id="a6937-105">클라우드에 대 한 탄력적 서비스 구축: 클라우드의 일시적 오류 포용</span><span class="sxs-lookup"><span data-stu-id="a6937-105">Build resilient services ready for the cloud: Embrace transient failures in the cloud</span></span>

<span data-ttu-id="a6937-106">복원력은 오류를 복구하고 계속 작업을 진행하는 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-106">Resiliency is the ability to recover from failures and continue to function.</span></span> <span data-ttu-id="a6937-107">하지만 오류를 방지 하 고, 오류가 발생할 수 있는 팩트를 수락 하 고, 가동 중지 시간 또는 데이터 손실을 방지 하는 방식으로 응답 하는 방법에 대 한 복원 력이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-107">Resiliency is not about avoiding failures, but accepting the fact that failures will occur, and then responding to them in a way that avoids downtime or data loss.</span></span> <span data-ttu-id="a6937-108">복원력의 목표는 오류 발생 후 응용 프로그램을 완전히 작동 중인 상태로 되돌리는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-108">The goal of resiliency is to return the application to a fully functioning state after a failure.</span></span>

<span data-ttu-id="a6937-109">응용 프로그램은 최소한이 복원 력, 소프트웨어를 기반으로 모델 보다는 하드웨어 기반 모델을 구현 하는 경우 클라우드를 위한 준비.</span><span class="sxs-lookup"><span data-stu-id="a6937-109">Your application is ready for the cloud when, at a minimum, it implements a software-based model of resiliency, rather than a hardware-based model.</span></span> <span data-ttu-id="a6937-110">클라우드 응용 프로그램에 확실히 발생 하는 부분 오류를 받아들여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-110">Your cloud application must embrace the partial failures that will certainly occur.</span></span> <span data-ttu-id="a6937-111">디자인 또는 부분적으로 예상된 부분 실패 한 복원 력을 달성 하기 위해 응용 프로그램을 리팩터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-111">Design or partially refactor your application to achieve resiliency with expected partial failures.</span></span> <span data-ttu-id="a6937-112">이 일시적인 네트워크 중단 및 노드 또는 Vm 클라우드에서 충돌과 같은 부분 오류에 대처 하기 위해 설계 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-112">It should be designed to cope with partial failures, like transient network outages and nodes, or VMs crashing in the cloud.</span></span> <span data-ttu-id="a6937-113">에 컨테이너 오 케 스트레이 터 클러스터 내의 다른 노드로 이동 되는 응용 프로그램에서 일시적 단기 오류를 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-113">Even containers being moved to a different node within an orchestrator cluster can cause intermittent short failures within the application.</span></span>

## <a name="handling-partial-failure"></a><span data-ttu-id="a6937-114">부분 실패 처리</span><span class="sxs-lookup"><span data-stu-id="a6937-114">Handling partial failure</span></span>

<span data-ttu-id="a6937-115">클라우드 기반 응용 프로그램에서 부분 오류 위험이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-115">In a cloud-based application, there's an ever-present risk of partial failure.</span></span> <span data-ttu-id="a6937-116">예를 들어 단일 웹 사이트 인스턴스 또는 컨테이너 실패 하거나 사용할 수 없거나 짧은 시간 동안 응답 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-116">For instance, a single website instance or a container might fail, or it might be unavailable or unresponsive for a short time.</span></span> <span data-ttu-id="a6937-117">또는 단일 VM 또는 서버가 중단 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-117">Or, a single VM or server might crash.</span></span>

<span data-ttu-id="a6937-118">클라이언트 및 서비스에 별도 프로세스 이기 때문에 서비스 클라이언트의 요청에 시기 적절 하 게 응답 하지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-118">Because clients and services are separate processes, a service might not be able to respond in a timely manner to a client's request.</span></span> <span data-ttu-id="a6937-119">서비스가 오버 로드 될 수 있습니다 및 느린 요청에 응답 또는 아닐 단기간에 액세스할 수 있는 네트워크 문제 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-119">The service might be overloaded and respond slowly to requests, or it might not be accessible for a short time because of network issues.</span></span>

<span data-ttu-id="a6937-120">Azure SQL Database에서 데이터베이스에 액세스 하는 모놀리식.NET 응용 프로그램을 예로 들어 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-120">For example, consider a monolithic .NET application that accesses a database in Azure SQL Database.</span></span> <span data-ttu-id="a6937-121">Azure SQL database 또는 다른 타사 서비스에 대 한 간단한 응답 하지 않는 경우 (Azure SQL database 서버나 다른 노드로 이동할 수 있습니다 및 몇 초 동안 응답 하지 않을 수) 시간을 사용자가 모든 작업을 수행 하려고 응용 프로그램의 작동이 중지 될 수 있습니다 및 표시 w 동일한 순간 시 예외를 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-121">If the Azure SQL database or any other third-party service is unresponsive for a brief time (an Azure SQL database might be moved to a different node or server, and be unresponsive for a few seconds), when the user tries to do any action, the application might crash and show an exception at the same moment.</span></span>

<span data-ttu-id="a6937-122">비슷한 시나리오는 HTTP 서비스를 사용 하는 앱에서 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-122">A similar scenario might occur in an app that consumes HTTP services.</span></span> <span data-ttu-id="a6937-123">네트워크 또는 서비스 자체 못할 클라우드에서 짧은, 일시적인 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-123">The network or the service itself might not be available in the cloud during a short, transient failure.</span></span>

<span data-ttu-id="a6937-124">그림 4-9에 표시 된 것 처럼 응용 프로그램을 복원 력 있는 응용 프로그램 리소스의 일시적 오류를 처리할 수 있도록 "지 수 백오프를 사용 하 여 다시 시도"와 같은 기술을 구현 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-124">A resilient application like the one shown in Figure 4-9 should implement techniques like "retries with exponential backoff" to give the application an opportunity to handle transient failures in resources.</span></span> <span data-ttu-id="a6937-125">또한 응용 프로그램에서 "회로 차단기" 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-125">You also should use "circuit breakers" in your applications.</span></span> <span data-ttu-id="a6937-126">회로 차단기는 실제로 장기적으로 실패 하는 경우 리소스에 액세스 하려는 응용 프로그램을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-126">A circuit breaker stops an application from trying to access a resource when it's actually a long-term failure.</span></span> <span data-ttu-id="a6937-127">회로 차단기를 사용 하 여 응용 프로그램이 자신에 게 서비스 거부가 발생 시킨 피할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-127">By using a circuit breaker, the application avoids provoking a denial of service to itself.</span></span>

![지 수 백오프를 사용 하 여 다시 시도 하 여 처리 하는 부분 실패](./media/image9.png)

> <span data-ttu-id="a6937-129">**그림 4-9 합니다.**</span><span class="sxs-lookup"><span data-stu-id="a6937-129">**Figure 4-9.**</span></span> <span data-ttu-id="a6937-130">지 수 백오프를 사용 하 여 다시 시도 하 여 처리 하는 부분 실패</span><span class="sxs-lookup"><span data-stu-id="a6937-130">Partial failures handled by retries with exponential backoff</span></span>

<span data-ttu-id="a6937-131">HTTP 리소스와 데이터베이스 리소스에서 이러한 기술을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-131">You can use these techniques both in HTTP resources and in database resources.</span></span> <span data-ttu-id="a6937-132">그림 4-9에서 응용 프로그램 기반으로 3 계층 아키텍처를 데이터 계층 수준 (TCP) 및 서비스 수준 (HTTP)에서 이러한 기술을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-132">In Figure 4-9, the application is based on a 3-tier architecture, so you need these techniques at the services level (HTTP) and at the data tier level (TCP).</span></span> <span data-ttu-id="a6937-133">데이터베이스 (추가 서비스 또는 마이크로 서비스) 외에도 단일 앱 계층만을 사용 하는 모놀리식 응용 프로그램에서는 데이터베이스 연결 수준에서 임시 오류 처리 충분할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-133">In a monolithic application that uses only a single app tier in addition to the database (no additional services or microservices), handling transient failures at the database connection level might be enough.</span></span> <span data-ttu-id="a6937-134">이 시나리오에서는 데이터베이스 연결의 특정 구성만 필요한 경우</span><span class="sxs-lookup"><span data-stu-id="a6937-134">In that scenario, just a particular configuration of the database connection is required.</span></span>

<span data-ttu-id="a6937-135">를 사용 하는.NET 버전에 따라 데이터베이스에 액세스 하는 복원 력 있는 통신을 구현 하는 경우 간단 하 게 될 수 있습니다 (예를 들어 [Entity Framework 6 이상](https://msdn.microsoft.com/library/dn456835(v=vs.113).aspx)를 구성 하기만 하면 됩니다 것를 데이터베이스 연결)입니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-135">When implementing resilient communications that access the database, depending on the version of .NET you are using, it can be straightforward (for example, [with Entity Framework 6 or later](https://msdn.microsoft.com/library/dn456835(v=vs.113).aspx), it's just a matter of configuring the database connection).</span></span> <span data-ttu-id="a6937-136">또는 같은 추가 라이브러리를 사용 해야 할 수 있습니다는 [일시적인 오류 처리 응용 프로그램 블록](https://msdn.microsoft.com/library/hh680934(v=pandp.50).aspx) (이전 버전에 대 한.net)도 직접 라이브러리를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-136">Or, you might need to use additional libraries like the [Transient Fault Handling Application Block](https://msdn.microsoft.com/library/hh680934(v=pandp.50).aspx) (for earlier versions of .NET), or even implement your own library.</span></span>

<span data-ttu-id="a6937-137">.NET에 대 한 권장 사항을 사용 하는 것 HTTP 다시 시도 하 고 회로 차단기를 구현 하는 경우는 [Polly](https://github.com/App-vNext/Polly) .NET Framework 4.0,.NET Framework 4.5 및.NET Core 지원을 포함 하는.NET 표준 1.1을 대상으로 하는 라이브러리입니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-137">When implementing HTTP retries and circuit breakers, the recommendation for .NET is to use the [Polly](https://github.com/App-vNext/Polly) library, which targets .NET Framework 4.0, .NET Framework 4.5, and .NET Standard 1.1, which includes .NET Core support.</span></span>

<span data-ttu-id="a6937-138">클라우드에서 부분 실패 처리 전략을 구현 하는 방법에 알아보려면 다음을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6937-138">To learn how to implement strategies for handling partial failures in the cloud, see the following references.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="a6937-139">추가 자료</span><span class="sxs-lookup"><span data-stu-id="a6937-139">Additional resources</span></span>

-   <span data-ttu-id="a6937-140">**복원 력 있는 통신 부분 실패 처리 구현**</span><span class="sxs-lookup"><span data-stu-id="a6937-140">**Implementing resilient communication to handle partial failure**</span></span>

    [https://docs.microsoft.com/dotnet/standard/microservices-architecture/implement-resilient-applications/partial-failure-strategies](../../microservices-architecture/implement-resilient-applications/partial-failure-strategies.md)

-   <span data-ttu-id="a6937-141">**Entity Framework 연결 복원 력 및 재시도 논리 (버전 6 이상)**</span><span class="sxs-lookup"><span data-stu-id="a6937-141">**Entity Framework connection resiliency and retry logic (version 6 and later)**</span></span>

    [https://msdn.microsoft.com/library/dn456835(v=vs.113).aspx](https://msdn.microsoft.com/library/dn456835(v=vs.113).aspx)

-   <span data-ttu-id="a6937-142">**일시적인 오류 처리 응용 프로그램 블록**</span><span class="sxs-lookup"><span data-stu-id="a6937-142">**The Transient Fault Handling Application Block**</span></span>

-   [https://msdn.microsoft.com/library/hh680934(v=pandp.50).aspx](https://msdn.microsoft.com/library/hh680934(v=pandp.50).aspx)

-   <span data-ttu-id="a6937-143">**복원 력 있는 HTTP 통신에 Polly 라이브러리**</span><span class="sxs-lookup"><span data-stu-id="a6937-143">**Polly library for resilient HTTP communication**</span></span>

    https://github.com/App-vNext/Polly

>[!div class="step-by-step"]
><span data-ttu-id="a6937-144">[이전](when-to-deploy-windows-containers-to-azure-container-service-kubernetes.md)
>[다음](modernize-your-apps-with-monitoring-and-telemetry.md)</span><span class="sxs-lookup"><span data-stu-id="a6937-144">[Previous](when-to-deploy-windows-containers-to-azure-container-service-kubernetes.md)
[Next](modernize-your-apps-with-monitoring-and-telemetry.md)</span></span>