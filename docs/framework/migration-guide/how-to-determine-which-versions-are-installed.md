---
title: '방법: 설치된 .NET Framework 버전 확인'
ms.date: 02/20/2019
dev_langs:
- csharp
- vb
ms.custom: updateeachrelease
helpviewer_keywords:
- versions, determining for .NET Framework
- .NET Framework, determining version
ms.assetid: 40a67826-e4df-4f59-a651-d9eb0fdc755d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d7661b3ebaa8f29d6d3b2adbc56c405c8f0945f3
ms.sourcegitcommit: 07c4368273b446555cb2c85397ea266b39d5fe50
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56584176"
---
# <a name="how-to-determine-which-net-framework-versions-are-installed"></a><span data-ttu-id="3e84e-102">방법: 설치된 .NET Framework 버전 확인</span><span class="sxs-lookup"><span data-stu-id="3e84e-102">How to: Determine which .NET Framework versions are installed</span></span>

<span data-ttu-id="3e84e-103">사용자는 자신의 컴퓨터에 여러 버전의 .NET Framework를 설치하여 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-103">Users can install and run multiple versions of the .NET Framework on their computers.</span></span> <span data-ttu-id="3e84e-104">따라서 앱을 개발하거나 배포할 때는 사용자의 컴퓨터에 어떤 .NET Framework 버전이 설치되었는지 알아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-104">When you develop or deploy your app, you might need to know which .NET Framework versions are installed on the user’s computer.</span></span> <span data-ttu-id="3e84e-105">.NET Framework는 각 버전으로 식별되는 다음과 같은 2개의 주요 구성 요소로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-105">Note that the .NET Framework consists of two main components, which are versioned separately:</span></span>  
  
- <span data-ttu-id="3e84e-106">앱의 기능을 제공하는 형식 및 리소스 컬렉션에 해당하는 어셈블리 집합.</span><span class="sxs-lookup"><span data-stu-id="3e84e-106">A set of assemblies, which are collections of types and resources that provide the functionality for your apps.</span></span> <span data-ttu-id="3e84e-107">.NET Framework와 어셈블리는 동일한 버전 번호를 공유합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-107">The .NET Framework and assemblies share the same version number.</span></span>  
  
- <span data-ttu-id="3e84e-108">앱 코드를 관리하고 실행하는 CLR(공용 언어 런타임).</span><span class="sxs-lookup"><span data-stu-id="3e84e-108">The common language runtime (CLR), which manages and executes your app's code.</span></span> <span data-ttu-id="3e84e-109">CLR은 고유한 버전 번호로 식별됩니다([버전 및 종속성](~/docs/framework/migration-guide/versions-and-dependencies.md) 참조).</span><span class="sxs-lookup"><span data-stu-id="3e84e-109">The CLR is identified by its own version number (see [Versions and Dependencies](~/docs/framework/migration-guide/versions-and-dependencies.md)).</span></span>  
  
<span data-ttu-id="3e84e-110">컴퓨터에 설치된 정확한 .NET Framework 버전 목록을 보려면 다음을 참조하여 레지스트리를 확인하거나 코드로 레지스트리를 쿼리합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-110">To get an accurate list of the .NET Framework versions installed on a computer, you can view the registry or query the registry in code:</span></span>  
  
 [<span data-ttu-id="3e84e-111">레지스트리에서 .NET Framework 버전 1-4 찾기</span><span class="sxs-lookup"><span data-stu-id="3e84e-111">Find .NET Framework versions 1-4 in the registry</span></span>](#net_a)  
 [<span data-ttu-id="3e84e-112">레지스트리에서 .NET Framework 버전 4.5 이상 찾기</span><span class="sxs-lookup"><span data-stu-id="3e84e-112">Find .NET Framework versions 4.5 and later in the registry)</span></span>](#net_b)  
 [<span data-ttu-id="3e84e-113">코드를 사용하여 레지스트리 쿼리(버전 1-4)</span><span class="sxs-lookup"><span data-stu-id="3e84e-113">Using code to query the registry (versions 1-4)</span></span>](#net_c)  
 [<span data-ttu-id="3e84e-114">코드를 사용하여 레지스트리 쿼리(버전 4.5 이상)</span><span class="sxs-lookup"><span data-stu-id="3e84e-114">Using code to query the registry (version 4.5 and later)</span></span>](#net_d)  
 [<span data-ttu-id="3e84e-115">PowerShell을 사용하여 레지스트리 쿼리(버전 4.5 이상)</span><span class="sxs-lookup"><span data-stu-id="3e84e-115">Using PowerShell to query the registry (version 4.5 and later)</span></span>](#ps_a)  

 <span data-ttu-id="3e84e-116">CLR 버전을 찾으려면 다음을 참조하여 도구나 코드를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-116">To find the CLR version, you can use a tool or code:</span></span>  
  
 [<span data-ttu-id="3e84e-117">Clrver 도구 사용</span><span class="sxs-lookup"><span data-stu-id="3e84e-117">Using the Clrver tool</span></span>](#clr_a)  
 [<span data-ttu-id="3e84e-118">코드를 사용하여 System.Environment 클래스 쿼리</span><span class="sxs-lookup"><span data-stu-id="3e84e-118">Using code to query the System.Environment class</span></span>](#clr_b)  

> [!NOTE]
> <span data-ttu-id="3e84e-119">.NET Framework 버전과 CLR(공용 언어 런타임) 버전은 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-119">There is a difference between the .NET Framework version and the common language runtime (CLR) version.</span></span> <span data-ttu-id="3e84e-120">.NET Framework의 버전은 .NET Framework 클래스 라이브러리를 구성하는 어셈블리 세트를 기반으로 정해집니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-120">The .NET Framework is versioned based on the set of assemblies that form the .NET Framework Class Library.</span></span> <span data-ttu-id="3e84e-121">예를 들어, .NET Framework 버전에는 4.5, 4.6.1, 4.7.2가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-121">For example, .NET Framework versions include 4.5, 4.6.1, and 4.7.2.</span></span> <span data-ttu-id="3e84e-122">CLR의 버전은 .NET Framework 애플리케이션이 실행되는 런타임을 기반으로 정해지며, 일반적으로 하나의 CLR 버전이 여러 개의 .NET Framework 버전을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-122">The CLR is versioned based on the runtime on which .NET Framework applications execute, and a single CLR version typically supports multiple .NET Framework versions.</span></span> <span data-ttu-id="3e84e-123">CLR 버전 4.30319.*xxxxx*는 .NET Framework 버전 4~4.5.2를 지원하고, CLR 버전 4.30319.42000은 .NET Framework 4.6에서 시작하는 .NET Framework 버전을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-123">CLR version 4.30319.*xxxxx* supports .NET Framework versions 4 through 4.5.2; CLR version 4.30319.42000 supports .NET Framework versions starting with .NET Framework 4.6.</span></span> <span data-ttu-id="3e84e-124">자세한 내용은 <xref:System.Environment.Version?displayProperty=nameWithType> 속성을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3e84e-124">For more information, see the <xref:System.Environment.Version?displayProperty=nameWithType> property.</span></span>

 <span data-ttu-id="3e84e-125">.NET Framework의 버전별로 설치된 업데이트를 검색하는 방법에 대한 자세한 내용은 [방법: 설치된 .NET Framework 업데이트 확인](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3e84e-125">For information about detecting the installed updates for each version of the .NET Framework, see [How to: Determine Which .NET Framework Updates Are Installed](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md).</span></span> <span data-ttu-id="3e84e-126">.NET Framework 설치에 대한 자세한 내용은 [개발자용 .NET Framework 설치](../../../docs/framework/install/guide-for-developers.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3e84e-126">For information about installing the .NET Framework, see [Install the .NET Framework for developers](../../../docs/framework/install/guide-for-developers.md).</span></span>  
  
<a name="net_a"></a>   
## <a name="find-net-framework-versions-1-4-in-the-registry"></a><span data-ttu-id="3e84e-127">레지스트리에서 .NET Framework 버전 1-4 찾기</span><span class="sxs-lookup"><span data-stu-id="3e84e-127">Find .NET Framework versions 1-4 in the registry</span></span> 
  
1.  <span data-ttu-id="3e84e-128">**시작** 메뉴에서 **실행**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-128">On the **Start** menu, choose **Run**.</span></span>  
  
2.  <span data-ttu-id="3e84e-129">**열기** 상자에 **regedit.exe**를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-129">In the **Open** box, enter **regedit.exe**.</span></span>  
  
     <span data-ttu-id="3e84e-130">regedit.exe를 실행하려면 관리자 자격 증명이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-130">You must have administrative credentials to run regedit.exe.</span></span>  
  
3.  <span data-ttu-id="3e84e-131">레지스트리 편집기에서 다음 하위 키를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-131">In the Registry Editor, open the following subkey:</span></span>  
  
     `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP`  
  
     <span data-ttu-id="3e84e-132">.NET Framework 버전 1.1~3.5의 경우, 설치된 버전이 `NDP` 하위 키 아래에 하위 키로 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-132">For .NET Framework versions 1.1 through 3.5, the installed versions are listed as subkeys under the `NDP` subkey.</span></span> <span data-ttu-id="3e84e-133">버전 번호는 버전 하위 키의 **Version** 항목에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-133">The version number is stored in the version subkey's **Version** entry.</span></span> 
     
     <span data-ttu-id="3e84e-134">.NET Framework 4의 경우, **Version** 항목은 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4.0\Client` 하위 키 또는 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4.0\Full` 하위 키 아래에, 또는 두 하위 키 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-134">For .NET Framework 4, the **Version** entry is under the `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4.0\Client` subkey, the `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4.0\Full` subkey, or under both subkeys.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3e84e-135">레지스트리의 "NET Framework Setup" 폴더는 마침표로 시작하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-135">The "NET Framework Setup" folder in the registry does not begin with a period.</span></span>

    <span data-ttu-id="3e84e-136">다음 그림은 .NET Framework 3.5의 하위 키와 **Version** 항목을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-136">The following figure shows that the subkey for the .NET Framework 3.5 along with its **Version** entry.</span></span>

     <span data-ttu-id="3e84e-137">![.NET Framework 3.5의 레지스트리 항목.](../../../docs/framework/migration-guide/media/net-4-and-earlier.png ".NET Framework 4 및 이전 버전")</span><span class="sxs-lookup"><span data-stu-id="3e84e-137">![The registry entry for the .NET Framework 3.5.](../../../docs/framework/migration-guide/media/net-4-and-earlier.png ".NET Framework 4 and earlier versions")</span></span>

<a name="net_b"></a> 
## <a name="find-net-framework-versions-45-and-later-in-the-registry"></a><span data-ttu-id="3e84e-138">레지스트리에서 .NET Framework 버전 4.5 이상 찾기</span><span class="sxs-lookup"><span data-stu-id="3e84e-138">Find .NET Framework versions 4.5 and later in the registry</span></span>

1. <span data-ttu-id="3e84e-139">**시작** 메뉴에서 **실행**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-139">On the **Start** menu, choose **Run**.</span></span>

2. <span data-ttu-id="3e84e-140">**열기** 상자에 **regedit.exe**를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-140">In the **Open** box, enter **regedit.exe**.</span></span>

     <span data-ttu-id="3e84e-141">regedit.exe를 실행하려면 관리자 자격 증명이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-141">You must have administrative credentials to run regedit.exe.</span></span>

3. <span data-ttu-id="3e84e-142">레지스트리 편집기에서 다음 하위 키를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-142">In the Registry Editor, open the following subkey:</span></span>

     `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full`

     <span data-ttu-id="3e84e-143">`Full` 하위 키에 대한 경로에는 `.NET Framework` 대신 `Net Framework` 하위 키가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-143">Note that the path to the `Full` subkey includes the subkey `Net Framework` rather than `.NET Framework`.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3e84e-144">`Full` 하위 키가 없으면 .NET Framework 4.5 이상이 설치되어 있지 않은 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-144">If the `Full` subkey is not present, then you do not have the .NET Framework 4.5 or later installed.</span></span>

     <span data-ttu-id="3e84e-145">`Release`라는 DWORD 값을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-145">Check for a DWORD value named `Release`.</span></span> <span data-ttu-id="3e84e-146">`Release` DWORD가 있으면 컴퓨터에 .NET Framework 4.5 이상이 설치된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-146">The existence of the `Release` DWORD indicates that .NET Framework 4.5 or later has been installed on that computer.</span></span> <span data-ttu-id="3e84e-147">그 값은 특정 버전의 .NET Framework에 대응되는 릴리스 키입니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-147">Its value is a release key that corresponds to a particular version of .NET Framework.</span></span> <span data-ttu-id="3e84e-148">예를 들어, 다음 그림에서 `Release` DWORD의 값은 378389로, 이것은 .NET Framework 4.5의 릴리스 키입니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-148">In the following figure, for example, the value of the `Release` DWORD is 378389, which is the release key for .NET Framework 4.5.</span></span> 

     <span data-ttu-id="3e84e-149">![.NET Framework 4.5.](../../../docs/framework/migration-guide/media/clr-installdir.png "CLR_InstallDir")에 대한 레지스트리 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-149">![The registry entry for the .NET Framework 4.5.](../../../docs/framework/migration-guide/media/clr-installdir.png "CLR_InstallDir")</span></span>

<span data-ttu-id="3e84e-150">다음 표에서는 각 .NET Framework 버전의 `Release` DWORD의 최솟값을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-150">The following table lists the minimum value of the `Release` DWORD for each .NET Framework version.</span></span> <span data-ttu-id="3e84e-151">이 값은 다음과 같이 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-151">You can use these values as follows:</span></span>

- <span data-ttu-id="3e84e-152">최소 .NET Framework 버전이 설치되었는지 확인하려면, 레지스트리에서 확인한 `Release` DWORD 값이 표에 있는 값보다 ‘크거나 같은지’ 살펴봅니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-152">To determine whether a minimum .NET Framework version is present, test whether the `Release` DWORD value found in the registry is *greater than or equal to* the value listed in the table.</span></span> <span data-ttu-id="3e84e-153">예를 들어, 애플리케이션에 .NET Framework 4.7 이상이 필요한 경우, 릴리스 키 값이 최소 460798이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-153">For example, if your application requires .NET Framework 4.7 or later, you would test for a minimum release key value of 460798.</span></span>

- <span data-ttu-id="3e84e-154">여러 버전을 테스트하려면 최신 .NET Framework 버전부터 시작하고 역으로 버전을 줄여가며 하나씩 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-154">To test for multiple versions, begin with the latest .NET Framework version, and then test for each successive earlier version.</span></span>

[!INCLUDE[Release key values note](~/includes/version-keys-note.md)]

|<span data-ttu-id="3e84e-155">.NET Framework 버전</span><span class="sxs-lookup"><span data-stu-id="3e84e-155">.NET Framework Version</span></span>|<span data-ttu-id="3e84e-156">릴리스 DWORD의 값</span><span class="sxs-lookup"><span data-stu-id="3e84e-156">Value of the Release DWORD</span></span>|
|--------------------------------|-------------|
|<span data-ttu-id="3e84e-157">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="3e84e-157">.NET Framework 4.5</span></span>|<span data-ttu-id="3e84e-158">378389</span><span class="sxs-lookup"><span data-stu-id="3e84e-158">378389</span></span>|
|<span data-ttu-id="3e84e-159">.NET Framework 4.5.1</span><span class="sxs-lookup"><span data-stu-id="3e84e-159">.NET Framework 4.5.1</span></span>|<span data-ttu-id="3e84e-160">378675</span><span class="sxs-lookup"><span data-stu-id="3e84e-160">378675</span></span>|
|<span data-ttu-id="3e84e-161">.NET Framework 4.5.2</span><span class="sxs-lookup"><span data-stu-id="3e84e-161">.NET Framework 4.5.2</span></span>|<span data-ttu-id="3e84e-162">379893</span><span class="sxs-lookup"><span data-stu-id="3e84e-162">379893</span></span>|
|<span data-ttu-id="3e84e-163">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="3e84e-163">.NET Framework 4.6</span></span>|<span data-ttu-id="3e84e-164">393295</span><span class="sxs-lookup"><span data-stu-id="3e84e-164">393295</span></span>|
|<span data-ttu-id="3e84e-165">.NET Framework 4.6.1</span><span class="sxs-lookup"><span data-stu-id="3e84e-165">.NET Framework 4.6.1</span></span>|<span data-ttu-id="3e84e-166">394254</span><span class="sxs-lookup"><span data-stu-id="3e84e-166">394254</span></span>|
|<span data-ttu-id="3e84e-167">.NET Framework 4.6.2</span><span class="sxs-lookup"><span data-stu-id="3e84e-167">.NET Framework 4.6.2</span></span>|<span data-ttu-id="3e84e-168">394802</span><span class="sxs-lookup"><span data-stu-id="3e84e-168">394802</span></span>|
|<span data-ttu-id="3e84e-169">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="3e84e-169">.NET Framework 4.7</span></span>|<span data-ttu-id="3e84e-170">460798</span><span class="sxs-lookup"><span data-stu-id="3e84e-170">460798</span></span>|
|<span data-ttu-id="3e84e-171">.NET Framework 4.7.1</span><span class="sxs-lookup"><span data-stu-id="3e84e-171">.NET Framework 4.7.1</span></span>|<span data-ttu-id="3e84e-172">461308</span><span class="sxs-lookup"><span data-stu-id="3e84e-172">461308</span></span>|
|<span data-ttu-id="3e84e-173">.NET Framework 4.7.2</span><span class="sxs-lookup"><span data-stu-id="3e84e-173">.NET Framework 4.7.2</span></span>|<span data-ttu-id="3e84e-174">461808</span><span class="sxs-lookup"><span data-stu-id="3e84e-174">461808</span></span>|

<span data-ttu-id="3e84e-175">특정 Windows 운영 체제 버전용 .NET Framework의 릴리스 키를 모두 확인하려면 [.NET Framework 릴리스 키 및 Windows 운영 체제 버전](release-keys-and-os-versions.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3e84e-175">For a complete table of release keys for the .NET Framework for specific Windows operating system versions, see [.NET Framework release keys and Windows operating system versions](release-keys-and-os-versions.md).</span></span>

<a name="net_c"></a> 
## <a name="find-net-framework-versions-1-4-with-code"></a><span data-ttu-id="3e84e-176">코드를 사용하여 .NET Framework 버전 1-4 찾기</span><span class="sxs-lookup"><span data-stu-id="3e84e-176">Find .NET Framework versions 1-4 with code</span></span>

- <span data-ttu-id="3e84e-177"><xref:Microsoft.Win32.RegistryKey?displayProperty=nameWithType> 클래스를 사용하여 Windows 레지스트리에서 `HKEY_LOCAL_MACHINE` 분기 아래에 있는 `Software\Microsoft\NET Framework Setup\NDP\` 하위 키에 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-177">Use the <xref:Microsoft.Win32.RegistryKey?displayProperty=nameWithType> class to access the `Software\Microsoft\NET Framework Setup\NDP\` subkey under `HKEY_LOCAL_MACHINE` branch in the Windows registry.</span></span>

     <span data-ttu-id="3e84e-178">다음 코드에서는 이 쿼리의 예제를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-178">The following code shows an example of this query.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3e84e-179">이 코드는 .NET Framework 4.5 이상을 확인하는 방법을 보여주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-179">This code does not show how to detect .NET Framework 4.5 or later.</span></span> <span data-ttu-id="3e84e-180">이전 섹션에 설명된 대로 `Release` DWORD를 확인하여 해당 버전을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-180">Check the `Release` DWORD to detect those versions, as described in the previous section.</span></span> <span data-ttu-id="3e84e-181">.NET Framework 4.5 이상 버전을 확인하는 코드가 필요하면 이 문서의 다음 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3e84e-181">For code that detects .NET Framework 4.5 or later versions, see the next section in this article.</span></span>

     [!code-csharp[ListVersions](../../../samples/snippets/csharp/framework/migration-guide/versions-installed1.cs)]
     [!code-vb[ListVersions](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed1.vb)]

<a name="net_d"></a> 
## <a name="find-net-framework-versions-45-and-later-with-code"></a><span data-ttu-id="3e84e-182">코드를 사용하여 .NET Framework 버전 4.5 이상 찾기</span><span class="sxs-lookup"><span data-stu-id="3e84e-182">Find .NET Framework versions 4.5 and later with code</span></span>

1. <span data-ttu-id="3e84e-183">`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full` 키에 `Release` DWORD가 있으면 .NET Framework 4.5 이상이 컴퓨터에 설치된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-183">The existence of the `Release` DWORD in the `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full` key indicates that the .NET Framework 4.5 or later is installed on a computer.</span></span> <span data-ttu-id="3e84e-184">이 키워드 값이 설치된 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-184">The value of the keyword indicates the installed version.</span></span> <span data-ttu-id="3e84e-185">이 키워드를 확인하려면 <xref:Microsoft.Win32.RegistryKey.OpenBaseKey%2A?displayProperty=nameWithType> 및 <xref:Microsoft.Win32.RegistryKey.OpenSubKey%2A?displayProperty=nameWithType> 메서드를 사용하여 Windows 레지스트리의 하위 키에 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-185">To check this keyword, use the <xref:Microsoft.Win32.RegistryKey.OpenBaseKey%2A?displayProperty=nameWithType> and <xref:Microsoft.Win32.RegistryKey.OpenSubKey%2A?displayProperty=nameWithType> methods to access the subkey in the Windows registry.</span></span>

2. <span data-ttu-id="3e84e-186">`Release` 키워드 값을 확인하여 설치된 버전을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-186">Check the value of the `Release` keyword to determine the installed version.</span></span> <span data-ttu-id="3e84e-187">이후 버전과의 호환성을 유지하려면 값이 [레지스트리에서 .NET Framework 버전 4.5 이상 찾기](#net_b) 섹션의 표에 있는 값보다 크거나 같은지 확인하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-187">To be forward-compatible, you can check for a value greater than or equal to the value listed in the table in the [Find .NET Framework versions 4.5 and later in the registry](#net_b) section.</span></span>

<span data-ttu-id="3e84e-188">다음 예제에서는 레지스트리에서 `Release` 값을 확인하여 .NET Framework 4.5 이상 버전이 설치되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-188">The following example checks the `Release` value in the registry to determine whether .NET Framework 4.5 or a later version is installed.</span></span>

[!code-csharp[ListVersions#5](../../../samples/snippets/csharp/framework/migration-guide/versions-installed3.cs)]
[!code-vb[ListVersions#5](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed3.vb)]

<span data-ttu-id="3e84e-189">이 예제에서는 버전을 확인하기 위한 권장된 방법을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-189">This example follows the recommended practice for version checking:</span></span>

- <span data-ttu-id="3e84e-190">`Release` 항목의 값이 알려진 릴리즈 키의 값보다 *크거나 같은지* 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-190">It checks whether the value of the `Release` entry is *greater than or equal to* the value of the known release keys.</span></span>

- <span data-ttu-id="3e84e-191">최신 버전에서 가장 오래된 버전 순서대로 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-191">It checks in order from most recent version to earliest version.</span></span>

<a name="ps_a"></a> 
## <a name="check-for-a-minimum-required-net-framework-version-45-and-later-with-powershell"></a><span data-ttu-id="3e84e-192">PowerShell을 사용하여 필요한 최소 .NET Framework 버전(4.5 이상) 확인</span><span class="sxs-lookup"><span data-stu-id="3e84e-192">Check for a minimum required .NET Framework version (4.5 and later) with PowerShell</span></span>

<span data-ttu-id="3e84e-193">다음 예제에서는 `Release` 키워드 값을 확인하여 .NET Framework 4.6.2 이상이 설치되어 있는지 확인합니다(설치된 경우 `True` 반환, 설치되지 않은 경우 `False` 반환).</span><span class="sxs-lookup"><span data-stu-id="3e84e-193">The following example checks the value of the `Release` keyword to determine whether .NET Framework 4.6.2 or higher is installed (returning `True` if it is and `False` otherwise).</span></span>

    ```PowerShell
    # PowerShell 5
    Get-ChildItem 'HKLM:\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full\' | Get-ItemPropertyValue -Name Release | Foreach-Object { $_ -ge 394802 } 
    ```

    ```PowerShell
    # PowerShell 4
    (Get-ItemProperty "HKLM:SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full").Release -gt 394802
    ```

    You can replace `394802` in the previous example with another value from the following table in the [Find .NET Framework versions 4.5 and later in the registry](#net_b) section to check for a different minimum required .NET Framework version.
  
<a name="clr_a"></a> 
## <a name="find-the-current-clr-version-with-clrverexe"></a><span data-ttu-id="3e84e-194">Clrver.exe를 사용하여 현재 CLR 버전 찾기</span><span class="sxs-lookup"><span data-stu-id="3e84e-194">Find the current CLR version with Clrver.exe</span></span>

<span data-ttu-id="3e84e-195">CLR 버전 도구(Clrver.exe)를 사용하여 컴퓨터에 설치된 공용 언어 런타임의 버전을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-195">Use the CLR Version Tool (Clrver.exe) to determine which versions of the common language runtime are installed on a computer.</span></span>

<span data-ttu-id="3e84e-196">Visual Studio용 개발자 명령 프롬프트에서 `clrver`을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-196">From a Developer Command Prompt for Visual Studio, enter `clrver`.</span></span> <span data-ttu-id="3e84e-197">이 명령은 다음과 유사한 출력 결과를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-197">This command produces output similar to the following:</span></span>

```console
Versions installed on the machine:
v2.0.50727
v4.0.30319
```

<span data-ttu-id="3e84e-198">이 도구의 사용 방법에 대한 자세한 내용은 [Clrver.exe(CLR 버전 도구)](~/docs/framework/tools/clrver-exe-clr-version-tool.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3e84e-198">For more information about using this tool, see [Clrver.exe (CLR Version Tool)](~/docs/framework/tools/clrver-exe-clr-version-tool.md).</span></span>

<a name="clr_b"></a> 
## <a name="find-the-current-clr-version-with-the-environment-class"></a><span data-ttu-id="3e84e-199">Environment 클래스를 사용하여 현재 CLR 버전 찾기</span><span class="sxs-lookup"><span data-stu-id="3e84e-199">Find the current CLR version with the Environment class</span></span>

<span data-ttu-id="3e84e-200"><xref:System.Environment.Version?displayProperty=nameWithType> 속성의 값을 가져와서 현재 코드를 실행하고 있는 런타임의 버전을 식별하는 <xref:System.Version> 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-200">You can retrieve the value of the <xref:System.Environment.Version?displayProperty=nameWithType> property to retrieve a <xref:System.Version> object that identifies the version of the runtime that is currently executing the code.</span></span> <span data-ttu-id="3e84e-201">이 속성은 현재 코드를 실행하고 있는 런타임의 버전을 반영하는 하나의 값을 반환하며, 컴퓨터에 설치된 어셈블리 버전이나 다른 런타임 버전은 반환하지 않습니다. <xref:System.Version.Major%2A?displayProperty=nameWithType> 속성을 사용하여 주 릴리스 식별자(예: 버전 4.0의 경우 “4”)를 가져오고, <xref:System.Version.Minor%2A?displayProperty=nameWithType> 속성을 사용하여 부 릴리스 식별자(예: 버전 4.0의 경우 “0”)를 가져오고, <xref:System.Version.ToString%2A?displayProperty=nameWithType> 메서드를 사용하여 전체 버전 문자열(예: 다음 코드에 표시된 것 같이 “4.0.30319.18010”)을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-201">This property returns a single value that reflects the version of the runtime that is currently executing the code; it does not return assembly versions or other versions of the runtime that may have been installed on the computer.You can use the <xref:System.Version.Major%2A?displayProperty=nameWithType> property to get the major release identifier (for example, "4" for version 4.0), the <xref:System.Version.Minor%2A?displayProperty=nameWithType> property to get the minor release identifier (for example, "0" for version 4.0), or the <xref:System.Version.ToString%2A?displayProperty=nameWithType> method to get the entire version string (for example, "4.0.30319.18010", as shown in the following code).</span></span> 

<span data-ttu-id="3e84e-202">.NET Framework 버전 4, 4.5, 4.5.1 및 4.5.2의 경우 <xref:System.Environment.Version%2A?displayProperty=nameWithType> 속성은 문자열 표시가 `4.0.30319.xxxxx` 형식인 <xref:System.Version> 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-202">For the .NET Framework Versions 4, 4.5, 4.5.1, and 4.5.2, the <xref:System.Environment.Version%2A?displayProperty=nameWithType> property returns a <xref:System.Version> object whose string representation has the form `4.0.30319.xxxxx`.</span></span> <span data-ttu-id="3e84e-203">.NET Framework 4.6 이상에서는 `4.0.30319.42000` 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-203">For the .NET Framework 4.6 and later, it has the form `4.0.30319.42000`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e84e-204">.NET Framework 4.5 이상의 경우 <xref:System.Environment.Version%2A?displayProperty=nameWithType> 속성을 사용하여 런타임의 버전을 확인하는 것을 권장하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-204">For the .NET Framework 4.5 and later, we do not recommend using the  <xref:System.Environment.Version%2A?displayProperty=nameWithType> property to detect the version of the runtime.</span></span> <span data-ttu-id="3e84e-205">대신 이 문서의 앞부분에 나오는 [코드로 레지스트리를 쿼리하여 .NET Framework 버전을 찾으려면(.NET Framework 4.5 이상)](#net_d) 섹션에서 설명된 것처럼 레지스트리를 쿼리하는 것을 권장합니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-205">Instead, we recommend that you query the registry, as described in the [To find .NET Framework versions by querying the registry in code (.NET Framework 4.5 and later)](#net_d) section earlier in this article.</span></span>

<span data-ttu-id="3e84e-206">다음 예제에서는 <xref:System.Environment.Version%2A?displayProperty=nameWithType> 속성을 사용하여 런타임 버전 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3e84e-206">The following example used the <xref:System.Environment.Version%2A?displayProperty=nameWithType> property to retrieve runtime version information:</span></span>

[!code-csharp[ListVersions](../../../samples/snippets/csharp/framework/migration-guide/versions-installed2.cs)]
[!code-vb[ListVersions](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed2.vb)]

## <a name="see-also"></a><span data-ttu-id="3e84e-207">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3e84e-207">See also</span></span>

- [<span data-ttu-id="3e84e-208">방법: 설치된 .NET Framework 업데이트 확인</span><span class="sxs-lookup"><span data-stu-id="3e84e-208">How to: Determine Which .NET Framework Updates Are Installed</span></span>](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md)
- [<span data-ttu-id="3e84e-209">개발자용 .NET Framework 설치</span><span class="sxs-lookup"><span data-stu-id="3e84e-209">Install the .NET Framework for developers</span></span>](../../../docs/framework/install/guide-for-developers.md)
- [<span data-ttu-id="3e84e-210">버전 및 종속성</span><span class="sxs-lookup"><span data-stu-id="3e84e-210">Versions and Dependencies</span></span>](~/docs/framework/migration-guide/versions-and-dependencies.md)
