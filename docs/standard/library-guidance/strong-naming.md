---
title: 강력한 이름 지정 및.NET 라이브러리
description: 강력한 이름 지정.NET 라이브러리에 대 한 권장 사항을 사용 하는 것이 좋습니다.
author: jamesnk
ms.author: mairaw
ms.date: 10/16/2018
ms.openlocfilehash: e3f7d443eb9acc84c800ea2611b803733085391c
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49372812"
---
# <a name="strong-naming"></a><span data-ttu-id="66f83-103">강력한 이름 지정</span><span class="sxs-lookup"><span data-stu-id="66f83-103">Strong naming</span></span>

<span data-ttu-id="66f83-104">강력한 이름 키 생성을 사용 하 여 어셈블리를 서명 가리킵니다를 [강력한 이름의 어셈블리](../../framework/app-domains/strong-named-assemblies.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-104">Strong naming refers to signing an assembly with a key, producing a [strong-named assembly](../../framework/app-domains/strong-named-assemblies.md).</span></span> <span data-ttu-id="66f83-105">강력한 이름의 어셈블리인 경우 이름 및 어셈블리 버전 번호를 기준으로 고유 id를 생성 및 어셈블리 충돌 되지 않도록 도와 줍니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-105">When an assembly is strong-named, it creates a unique identity based on the name and assembly version number, and it can help prevent assembly conflicts.</span></span>

<span data-ttu-id="66f83-106">강력한 이름 단점은 Windows에서.NET Framework 어셈블리는 강력한 이름이 지정 되 면 어셈블리의 엄격 하 게 로드 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-106">The downside to strong naming is that the .NET Framework on Windows enables strict loading of assemblies once an assembly is strong named.</span></span> <span data-ttu-id="66f83-107">강력한 이름의 어셈블리 참조를 개발자가 강제 적용 하는 어셈블리에서 참조 된 버전을 정확히 일치 해야 합니다 [바인딩 리디렉션을 구성](../../framework/configure-apps/redirect-assembly-versions.md) 어셈블리를 사용 하는 경우:</span><span class="sxs-lookup"><span data-stu-id="66f83-107">A strong-named assembly reference must exactly match the version referenced by an assembly, forcing developers to [configure binding redirects](../../framework/configure-apps/redirect-assembly-versions.md) when using the assembly:</span></span>

```xml
<configuration>
   <runtime>
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
         <dependentAssembly>
            <assemblyIdentity name="myAssembly" publicKeyToken="32ab4ba45e0a69a1" culture="neutral" />
            <bindingRedirect oldVersion="1.0.0.0" newVersion="2.0.0.0"/>
         </dependentAssembly>
      </assemblyBinding>
   </runtime>
</configuration>
```

<span data-ttu-id="66f83-108">.NET 개발자는 강력한 이름에 대 한 불만 제기 내용 해당 하는 일반적으로 불만족 때 엄격한 어셈블리를 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-108">When .NET developers complain about strong naming, what they're usually complaining about is strict assembly loading.</span></span> <span data-ttu-id="66f83-109">다행 스럽게도이 문제는.NET Framework에 격리 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-109">Fortunately, this issue is isolated to the .NET Framework.</span></span> <span data-ttu-id="66f83-110">.NET core, Xamarin, UWP 및 다른.NET 구현과 대부분의 엄격한 어셈블리 로드 없는 하 고 강력한 이름 지정의 주요 단점은 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-110">.NET Core, Xamarin, UWP, and most other .NET implementations don't have strict assembly loading and removes the main downside of strong naming.</span></span>

<span data-ttu-id="66f83-111">중요 한 측면의 강력한 이름 바 이럴 있다는 것입니다: 강력한 이름의 어셈블리 수만 참조 다른 강력한 이름의 어셈블리입니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-111">One important aspect of strong naming is that it's viral: a strong named assembly can only reference other strong named assemblies.</span></span> <span data-ttu-id="66f83-112">라이브러리 라는 강력한 없는 경우 응용 프로그램이 나이 사용 하 여 강력한 이름 지정 해야 하는 라이브러리를 빌드하는 개발자를 제외가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-112">If your library isn't strong named, then you have excluded developers who are building an application or library that needs strong naming from using it.</span></span>

<span data-ttu-id="66f83-113">강력한 이름 이점은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-113">The benefits of strong naming are:</span></span>

1. <span data-ttu-id="66f83-114">어셈블리를 참조 하 고 다른 강력한 이름의 어셈블리에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-114">The assembly can be referenced and used by other strong-named assemblies.</span></span>
2. <span data-ttu-id="66f83-115">어셈블리를 전역 어셈블리 캐시 (GAC)에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-115">The assembly can be stored in the Global Assembly Cache (GAC).</span></span>
3. <span data-ttu-id="66f83-116">어셈블리를 다른 버전의 어셈블리와 함께 로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-116">The assembly can be loaded side by side with other versions of the assembly.</span></span> <span data-ttu-id="66f83-117">Side-by-side-어셈블리 로드 플러그 인 아키텍처를 사용 하 여 응용 프로그램에서 일반적으로 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-117">Side-by-side assembly loading is commonly required by applications with plug-in architectures.</span></span>

## <a name="create-strong-named-net-libraries"></a><span data-ttu-id="66f83-118">.NET 라이브러리를 명명 된 강력한 만들려면</span><span class="sxs-lookup"><span data-stu-id="66f83-118">Create strong named .NET libraries</span></span>

<span data-ttu-id="66f83-119">강력한 오픈 소스.NET 라이브러리 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-119">You should strong name your open-source .NET libraries.</span></span> <span data-ttu-id="66f83-120">강력한 이름의 어셈블리는 대부분의 사람들이 사용할 수 있습니다 하 고만 로드 하는 엄격한 어셈블리에.NET Framework에 영향을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-120">Strong naming an assembly ensures the most people can use it, and strict assembly loading only affects the .NET Framework.</span></span>

> [!NOTE]
> <span data-ttu-id="66f83-121">이 지침은 NuGet.org에 게시 된.NET 라이브러리와 같은 분산된 공개적으로.NET 라이브러리와 관련이 있습니다. 강력한 이름 지정 하는 대부분의.NET 응용 프로그램에 필요 하지 않은 및 기본적으로 실행 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-121">This guidance is specific to publicly distributed .NET libraries, such as .NET libraries published on NuGet.org. Strong naming is not required by most .NET applications and should not be done by default.</span></span>

<span data-ttu-id="66f83-122">**✔️ 하십시오** 강력한 라이브러리의 어셈블리 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-122">**✔️ CONSIDER** strong naming your library's assemblies.</span></span>

<span data-ttu-id="66f83-123">**✔️ 하십시오** 소스 제어 시스템에 강력한 이름으로 사용 된 키를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-123">**✔️ CONSIDER** checking in the key used to strong name into your source control system.</span></span>

> <span data-ttu-id="66f83-124">공개 키를 수정 하 고 동일한 키를 사용 하 여 라이브러리 소스 코드를 다시 컴파일해야 하는 개발자를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-124">A publicly available key lets developers modify and recompile your library source code with the same key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66f83-125">원하는 것이 id를 암호화 하는 경우 [Authenticode](/windows-hardware/drivers/install/authenticode) 하 고 [NuGet 패키지 서명](/nuget/create-packages/sign-a-package) 는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-125">When a cryptographic identity is desired, [Authenticode](/windows-hardware/drivers/install/authenticode) and [NuGet Package Signing](/nuget/create-packages/sign-a-package) are recommended.</span></span> <span data-ttu-id="66f83-126">강력한 이름 지정 해서는 안 보안 고려 사항에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-126">Strong naming should not be used for security considerations.</span></span>

<span data-ttu-id="66f83-127">**✔️ 하십시오** 바인딩 리디렉션 및 업데이트 하는 빈도 줄일 수 있도록만 주 버전 변경 내용에 대해 어셈블리 버전 증분 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-127">**✔️ CONSIDER** incrementing the assembly version on only major version changes to help users reduce binding redirects, and how often they're updated.</span></span>

> <span data-ttu-id="66f83-128">에 대해 자세히 알아보세요 [버전 관리 및 어셈블리 버전](./versioning.md#assembly-version)합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-128">Read more about [versioning and the assembly version](./versioning.md#assembly-version).</span></span>

<span data-ttu-id="66f83-129">**❌ 하지** 추가, 제거 또는 강력한 이름 키를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-129">**❌ DO NOT** add, remove, or change the strong naming key.</span></span>

> <span data-ttu-id="66f83-130">어셈블리의 강력한 이름 키를 수정 합니다. 어셈블리의 id를 변경 하 고 사용 하는 컴파일된 코드를 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-130">Modifying an assembly's strong naming key changes the assembly's identity and breaks compiled code that uses it.</span></span> <span data-ttu-id="66f83-131">자세한 내용은 [주요 변경 내용 이진](./breaking-changes.md#binary-breaking-change)합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-131">For more information, see [binary breaking changes](./breaking-changes.md#binary-breaking-change).</span></span>

<span data-ttu-id="66f83-132">**❌ 하지** 라이브러리의 강력한 이름을 지정 하 고 비-강력한 이름의 버전을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-132">**❌ DO NOT** publish strong-named and non-strong-named versions of your library.</span></span> <span data-ttu-id="66f83-133">예를 들어 `Contoso.Api` 및 `Contoso.Api.StrongNamed`를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-133">For example, `Contoso.Api` and `Contoso.Api.StrongNamed`.</span></span>

> <span data-ttu-id="66f83-134">두 개의 패키지 분기만 개발자 에코 시스템에 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-134">Publishing two packages forks your developer eco-system.</span></span> <span data-ttu-id="66f83-135">또한 응용 프로그램 패키지를 모두에 따라 최종적으로 개발자는 형식 이름 충돌을 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66f83-135">Also, if an application ends up depending on both packages the developer can encounter type name conflicts.</span></span> <span data-ttu-id="66f83-136">.NET은 관련해 서 이러한는 다른 어셈블리의 다른 형식</span><span class="sxs-lookup"><span data-stu-id="66f83-136">As far as .NET is concerned they are different types in different assemblies.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="66f83-137">[이전](./cross-platform-targeting.md)
[다음](./nuget.md)</span><span class="sxs-lookup"><span data-stu-id="66f83-137">[Previous](./cross-platform-targeting.md)
[Next](./nuget.md)</span></span>
