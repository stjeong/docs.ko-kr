---
title: '방법: 설치된 .NET Framework 버전 확인'
ms.date: 04/10/2018
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
ms.openlocfilehash: 6b77775fdc7f552e6433e6364f153c5bde32d9e0
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53151046"
---
# <a name="how-to-determine-which-net-framework-versions-are-installed"></a><span data-ttu-id="ea846-102">방법: 설치된 .NET Framework 버전 확인</span><span class="sxs-lookup"><span data-stu-id="ea846-102">How to: Determine which .NET Framework versions are installed</span></span>

<span data-ttu-id="ea846-103">사용자는 자신의 컴퓨터에 여러 버전의 .NET Framework를 설치하여 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-103">Users can install and run multiple versions of the .NET Framework on their computers.</span></span> <span data-ttu-id="ea846-104">따라서 앱을 개발하거나 배포할 때는 사용자의 컴퓨터에 어떤 .NET Framework 버전이 설치되었는지 알아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-104">When you develop or deploy your app, you might need to know which .NET Framework versions are installed on the user’s computer.</span></span> <span data-ttu-id="ea846-105">.NET Framework는 각 버전으로 식별되는 다음과 같은 2개의 주요 구성 요소로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-105">Note that the .NET Framework consists of two main components, which are versioned separately:</span></span>  
  
-   <span data-ttu-id="ea846-106">앱의 기능을 제공하는 형식 및 리소스 컬렉션에 해당하는 어셈블리 집합.</span><span class="sxs-lookup"><span data-stu-id="ea846-106">A set of assemblies, which are collections of types and resources that provide the functionality for your apps.</span></span> <span data-ttu-id="ea846-107">.NET Framework와 어셈블리는 동일한 버전 번호를 공유합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-107">The .NET Framework and assemblies share the same version number.</span></span>  
  
-   <span data-ttu-id="ea846-108">앱 코드를 관리하고 실행하는 CLR(공용 언어 런타임).</span><span class="sxs-lookup"><span data-stu-id="ea846-108">The common language runtime (CLR), which manages and executes your app's code.</span></span> <span data-ttu-id="ea846-109">CLR은 고유한 버전 번호로 식별됩니다([버전 및 종속성](~/docs/framework/migration-guide/versions-and-dependencies.md) 참조).</span><span class="sxs-lookup"><span data-stu-id="ea846-109">The CLR is identified by its own version number (see [Versions and Dependencies](~/docs/framework/migration-guide/versions-and-dependencies.md)).</span></span>  
  
 <span data-ttu-id="ea846-110">컴퓨터에 설치된 정확한 .NET Framework 버전 목록을 보려면 다음을 참조하여 레지스트리를 확인하거나 코드로 레지스트리를 쿼리합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-110">To get an accurate list of the .NET Framework versions installed on a computer, you can view the registry or query the registry in code:</span></span>  
  
 [<span data-ttu-id="ea846-111">레지스트리 보기(버전 1-4)</span><span class="sxs-lookup"><span data-stu-id="ea846-111">Viewing the registry (versions 1-4)</span></span>](#net_a)  
 [<span data-ttu-id="ea846-112">레지스트리 보기(버전 4.5 이상)</span><span class="sxs-lookup"><span data-stu-id="ea846-112">Viewing the registry (version 4.5 and later)</span></span>](#net_b)  
 [<span data-ttu-id="ea846-113">코드를 사용하여 레지스트리 쿼리(버전 1-4)</span><span class="sxs-lookup"><span data-stu-id="ea846-113">Using code to query the registry (versions 1-4)</span></span>](#net_c)  
 [<span data-ttu-id="ea846-114">코드를 사용하여 레지스트리 쿼리(버전 4.5 이상)</span><span class="sxs-lookup"><span data-stu-id="ea846-114">Using code to query the registry (version 4.5 and later)</span></span>](#net_d)  
 [<span data-ttu-id="ea846-115">PowerShell을 사용하여 레지스트리 쿼리(버전 4.5 이상)</span><span class="sxs-lookup"><span data-stu-id="ea846-115">Using PowerShell to query the registry (version 4.5 and later)</span></span>](#ps_a)  
  
 <span data-ttu-id="ea846-116">CLR 버전을 찾으려면 다음을 참조하여 도구나 코드를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-116">To find the CLR version, you can use a tool or code:</span></span>  
  
 [<span data-ttu-id="ea846-117">Clrver 도구 사용</span><span class="sxs-lookup"><span data-stu-id="ea846-117">Using the Clrver tool</span></span>](#clr_a)  
 [<span data-ttu-id="ea846-118">코드를 사용하여 System.Environment 클래스 쿼리</span><span class="sxs-lookup"><span data-stu-id="ea846-118">Using code to query the System.Environment class</span></span>](#clr_b)  
  
 <span data-ttu-id="ea846-119">.NET Framework 버전별로 설치된 업데이트를 검색하는 방법에 대한 자세한 내용은 [방법: 설치된 .NET Framework 업데이트 확인](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ea846-119">For information about detecting the installed updates for each version of the .NET Framework, see [How to: Determine Which .NET Framework Updates Are Installed](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md).</span></span> <span data-ttu-id="ea846-120">.NET Framework 설치에 대한 자세한 내용은 [개발자용 .NET Framework 설치](../../../docs/framework/install/guide-for-developers.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ea846-120">For information about installing the .NET Framework, see [Install the .NET Framework for developers](../../../docs/framework/install/guide-for-developers.md).</span></span>  
  
<a name="net_a"></a>   
## <a name="to-find-net-framework-versions-by-viewing-the-registry-net-framework-1-4"></a><span data-ttu-id="ea846-121">레지스트리를 확인하여 .NET Framework 버전을 찾으려면(.NET Framework 1-4)</span><span class="sxs-lookup"><span data-stu-id="ea846-121">To find .NET Framework versions by viewing the registry (.NET Framework 1-4)</span></span>  
  
1.  <span data-ttu-id="ea846-122">**시작** 메뉴에서 **실행**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-122">On the **Start** menu, choose **Run**.</span></span>  
  
2.  <span data-ttu-id="ea846-123">**열기** 상자에 **regedit.exe**를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-123">In the **Open** box, enter **regedit.exe**.</span></span>  
  
     <span data-ttu-id="ea846-124">regedit.exe를 실행하려면 관리자 자격 증명이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-124">You must have administrative credentials to run regedit.exe.</span></span>  
  
3.  <span data-ttu-id="ea846-125">레지스트리 편집기에서 다음 하위 키를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-125">In the Registry Editor, open the following subkey:</span></span>  
  
     `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP`  
  
     <span data-ttu-id="ea846-126">설치된 버전은 NDP 하위 키 아래에 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-126">The installed versions are listed under the NDP subkey.</span></span> <span data-ttu-id="ea846-127">버전 번호는 **Version** 항목에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-127">The version number is stored in the **Version** entry.</span></span> <span data-ttu-id="ea846-128">[!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)]의 **Version** 항목은 NDP 아래 Client 또는 Full 하위 키 아래에 있거나 두 하위 키 아래 모두에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-128">For the [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)] the **Version** entry is under the Client or Full subkey (under NDP), or under both subkeys.</span></span>  
  

    > [!NOTE]
    > <span data-ttu-id="ea846-129">레지스트리의 "NET Framework Setup" 폴더는 마침표로 시작하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-129">The "NET Framework Setup" folder in the registry does not begin with a period.</span></span>

<a name="net_b"></a> 
## <a name="to-find-net-framework-versions-by-viewing-the-registry-net-framework-45-and-later"></a><span data-ttu-id="ea846-130">레지스트리를 확인하여 .NET Framework 버전을 찾으려면(.NET Framework 4.5 이상)</span><span class="sxs-lookup"><span data-stu-id="ea846-130">To find .NET Framework versions by viewing the registry (.NET Framework 4.5 and later)</span></span>

1. <span data-ttu-id="ea846-131">**시작** 메뉴에서 **실행**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-131">On the **Start** menu, choose **Run**.</span></span>

2. <span data-ttu-id="ea846-132">**열기** 상자에 **regedit.exe**를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-132">In the **Open** box, enter **regedit.exe**.</span></span>

     <span data-ttu-id="ea846-133">regedit.exe를 실행하려면 관리자 자격 증명이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-133">You must have administrative credentials to run regedit.exe.</span></span>

3. <span data-ttu-id="ea846-134">레지스트리 편집기에서 다음 하위 키를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-134">In the Registry Editor, open the following subkey:</span></span>

     `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full`

     <span data-ttu-id="ea846-135">`Full` 하위 키에 대한 경로에는 `.NET Framework` 대신 `Net Framework` 하위 키가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-135">Note that the path to the `Full` subkey includes the subkey `Net Framework` rather than `.NET Framework`.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ea846-136">`Full` 하위 키가 없으면 .NET Framework 4.5 이상이 설치되어 있지 않은 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-136">If the `Full` subkey is not present, then you do not have the .NET Framework 4.5 or later installed.</span></span>

     <span data-ttu-id="ea846-137">`Release`라는 DWORD 값을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-137">Check for a DWORD value named `Release`.</span></span> <span data-ttu-id="ea846-138">`Release` DWORD가 있으면 [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] 또는 그 이상 버전이 해당 컴퓨터에 설치되어 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-138">The existence of the `Release` DWORD indicates that the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] or newer has been installed on that computer.</span></span>

     <span data-ttu-id="ea846-139">![.NET Framework 4.5.](../../../docs/framework/migration-guide/media/clr-installdir.png "CLR_InstallDir")에 대한 레지스트리 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-139">![The registry entry for the .NET Framework 4.5.](../../../docs/framework/migration-guide/media/clr-installdir.png "CLR_InstallDir")</span></span>

     <span data-ttu-id="ea846-140">`Release` DWORD의 값은 설치된 .NET Framework 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-140">The value of the `Release` DWORD indicates which version of the .NET Framework is installed.</span></span>

    [!INCLUDE[Release key values note](~/includes/version-keys-note.md)]

    |<span data-ttu-id="ea846-141">릴리스 DWORD의 값</span><span class="sxs-lookup"><span data-stu-id="ea846-141">Value of the Release DWORD</span></span>|<span data-ttu-id="ea846-142">버전</span><span class="sxs-lookup"><span data-stu-id="ea846-142">Version</span></span>|
    |--------------------------------|-------------|
    |<span data-ttu-id="ea846-143">378389</span><span class="sxs-lookup"><span data-stu-id="ea846-143">378389</span></span>|<span data-ttu-id="ea846-144">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="ea846-144">.NET Framework 4.5</span></span>|
    |<span data-ttu-id="ea846-145">378675</span><span class="sxs-lookup"><span data-stu-id="ea846-145">378675</span></span>|<span data-ttu-id="ea846-146">.NET Framework 4.5.1이 Windows 8.1 또는 Windows Server 2012 R2와 함께 설치됨</span><span class="sxs-lookup"><span data-stu-id="ea846-146">.NET Framework 4.5.1 installed with Windows 8.1 or Windows Server 2012 R2</span></span>|
    |<span data-ttu-id="ea846-147">378758</span><span class="sxs-lookup"><span data-stu-id="ea846-147">378758</span></span>|<span data-ttu-id="ea846-148">.NET Framework 4.5.1이 Windows 8, Windows 7 SP1 또는 Windows Vista SP2에 설치됨</span><span class="sxs-lookup"><span data-stu-id="ea846-148">.NET Framework 4.5.1 installed on Windows 8, Windows 7 SP1, or Windows Vista SP2</span></span>|
    |<span data-ttu-id="ea846-149">379893</span><span class="sxs-lookup"><span data-stu-id="ea846-149">379893</span></span>|<span data-ttu-id="ea846-150">.NET Framework 4.5.2</span><span class="sxs-lookup"><span data-stu-id="ea846-150">.NET Framework 4.5.2</span></span>|
    |<span data-ttu-id="ea846-151">Windows 10 시스템에서만: 393295</span><span class="sxs-lookup"><span data-stu-id="ea846-151">On Windows 10 systems only: 393295</span></span><br /><br /> <span data-ttu-id="ea846-152">다른 모든 OS 버전에서: 393297</span><span class="sxs-lookup"><span data-stu-id="ea846-152">On all other OS versions: 393297</span></span>|[!INCLUDE[net_v46](../../../includes/net-v46-md.md)]|
    |<span data-ttu-id="ea846-153">Windows 10 11월 업데이트 시스템에서만: 394254</span><span class="sxs-lookup"><span data-stu-id="ea846-153">On Windows 10 November Update systems only: 394254</span></span><br /><br /> <span data-ttu-id="ea846-154">모든 다른 OS 버전: 394271</span><span class="sxs-lookup"><span data-stu-id="ea846-154">On all other OS versions: 394271</span></span>|[!INCLUDE[net_v461](../../../includes/net-v461-md.md)]|
    |<span data-ttu-id="ea846-155">Windows 10 1주년 업데이트 및 Windows Server 2016: 394802</span><span class="sxs-lookup"><span data-stu-id="ea846-155">On Windows 10 Anniversary Update and Windows Server 2016: 394802</span></span><br /><br /> <span data-ttu-id="ea846-156">모든 다른 OS 버전: 394806</span><span class="sxs-lookup"><span data-stu-id="ea846-156">On all other OS versions: 394806</span></span>|[!INCLUDE[net_v462](../../../includes/net-v462-md.md)]| 
    |<span data-ttu-id="ea846-157">Windows 10 작성자 업데이트에서만: 460798</span><span class="sxs-lookup"><span data-stu-id="ea846-157">On Windows 10 Creators Update only: 460798</span></span><br/><br/> <span data-ttu-id="ea846-158">다른 모든 OS 버전: 460805</span><span class="sxs-lookup"><span data-stu-id="ea846-158">On all other OS versions: 460805</span></span> | <span data-ttu-id="ea846-159">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="ea846-159">.NET Framework 4.7</span></span> |
    |<span data-ttu-id="ea846-160">Windows 10 가을 작성자 업데이트에서만: 461308</span><span class="sxs-lookup"><span data-stu-id="ea846-160">On Windows 10 Fall Creators Update only: 461308</span></span><br/><br/> <span data-ttu-id="ea846-161">다른 모든 OS 버전: 461310</span><span class="sxs-lookup"><span data-stu-id="ea846-161">On all other OS versions: 461310</span></span> | <span data-ttu-id="ea846-162">.NET Framework 4.7.1</span><span class="sxs-lookup"><span data-stu-id="ea846-162">.NET Framework 4.7.1</span></span> |
    |<span data-ttu-id="ea846-163">Windows 10 2018년 10월 업데이트에서만: 461814</span><span class="sxs-lookup"><span data-stu-id="ea846-163">On Windows 10 October 2018 Update only: 461814</span></span><br/><br/> <span data-ttu-id="ea846-164">Windows 10 2018년 4월 업데이트에서만: 461808</span><span class="sxs-lookup"><span data-stu-id="ea846-164">On Windows 10 April 2018 Update only: 461808</span></span><br/><br/> <span data-ttu-id="ea846-165">다른 모든 OS 버전: 461814</span><span class="sxs-lookup"><span data-stu-id="ea846-165">On all other OS versions: 461814</span></span>| <span data-ttu-id="ea846-166">.NET Framework 4.7.2</span><span class="sxs-lookup"><span data-stu-id="ea846-166">.NET Framework 4.7.2</span></span> |
    
<a name="net_c"></a> 
## <a name="to-find-net-framework-versions-by-querying-the-registry-in-code-net-framework-1-4"></a><span data-ttu-id="ea846-167">코드로 레지스트리를 쿼리하여 .NET Framework 버전을 찾으려면(.NET Framework 1-4)</span><span class="sxs-lookup"><span data-stu-id="ea846-167">To find .NET Framework versions by querying the registry in code (.NET Framework 1-4)</span></span>

- <span data-ttu-id="ea846-168"><xref:Microsoft.Win32.RegistryKey?displayProperty=nameWithType> 클래스를 사용하여 Windows 레지스트리의 HKEY_LOCAL_MACHINE 아래에 있는 Software\Microsoft\NET Framework Setup\NDP\ 하위 키에 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-168">Use the <xref:Microsoft.Win32.RegistryKey?displayProperty=nameWithType> class to access the Software\Microsoft\NET Framework Setup\NDP\ subkey under HKEY_LOCAL_MACHINE in the Windows registry.</span></span>

     <span data-ttu-id="ea846-169">다음 코드에서는 이 쿼리의 예제를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-169">The following code shows an example of this query.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ea846-170">이 코드는 [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] 이상 버전을 검색하는 방법은 보여 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-170">This code does not show how to detect the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] or later.</span></span> <span data-ttu-id="ea846-171">이전 섹션에 설명된 대로 `Release` DWORD를 확인하여 해당 버전을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-171">Check the `Release` DWORD to detect those versions, as described in the previous section.</span></span> <span data-ttu-id="ea846-172">[!INCLUDE[net_v45](../../../includes/net-v45-md.md)] 또는 이후 버전을 검색하는 코드에 대해서는 이 문서의 다음 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ea846-172">For code that does detect the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] or later versions, see the next section in this article.</span></span>

     [!code-csharp[ListVersions](../../../samples/snippets/csharp/framework/migration-guide/versions-installed1.cs)]
     [!code-vb[ListVersions](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed1.vb)]

     <span data-ttu-id="ea846-173">이 예제는 다음과 유사한 출력 결과를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-173">The example produces output that's similar to the following:</span></span>

    ```
    v2.0.50727  2.0.50727.4016  SP2
    v3.0  3.0.30729.4037  SP2
    v3.5  3.5.30729.01  SP1
    v4
      Client  4.0.30319
      Full  4.0.30319
    ```

<a name="net_d"></a> 
## <a name="to-find-net-framework-versions-by-querying-the-registry-in-code-net-framework-45-and-later"></a><span data-ttu-id="ea846-174">코드로 레지스트리를 쿼리하여 .NET Framework 버전을 찾으려면(.NET Framework 4.5 이상)</span><span class="sxs-lookup"><span data-stu-id="ea846-174">To find .NET Framework versions by querying the registry in code (.NET Framework 4.5 and later)</span></span>

1. <span data-ttu-id="ea846-175">`Release` DWORD가 있으면 .NET Framework 4.5 이상이 컴퓨터에 설치되어 있는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-175">The existence of the `Release` DWORD indicates that the .NET Framework 4.5 or later has been installed on a computer.</span></span> <span data-ttu-id="ea846-176">이 키워드 값이 설치된 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-176">The value of the keyword indicates the installed version.</span></span> <span data-ttu-id="ea846-177">이 키워드를 확인하려면 <xref:Microsoft.Win32.RegistryKey?displayProperty=nameWithType> 클래스의 <xref:Microsoft.Win32.RegistryKey.OpenBaseKey%2A> 및 <xref:Microsoft.Win32.RegistryKey.OpenSubKey%2A> 메서드를 사용하여 Windows 레지스트리의 HKEY_LOCAL_MACHINE 아래에 있는 Software\Microsoft\NET Framework Setup\NDP\v4\Full 하위 키에 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-177">To check this keyword, use the <xref:Microsoft.Win32.RegistryKey.OpenBaseKey%2A> and <xref:Microsoft.Win32.RegistryKey.OpenSubKey%2A> methods of the <xref:Microsoft.Win32.RegistryKey?displayProperty=nameWithType> class to access the Software\Microsoft\NET Framework Setup\NDP\v4\Full subkey under HKEY_LOCAL_MACHINE in the Windows registry.</span></span>

2. <span data-ttu-id="ea846-178">`Release` 키워드 값을 확인하여 설치된 버전을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-178">Check the value of the `Release` keyword to determine the installed version.</span></span> <span data-ttu-id="ea846-179">이후 버전과의 호환성을 유지하려는 경우 버전의 값이 표에 나와 있는 값 이상인지를 확인하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-179">To be forward-compatible, you can check for a value greater than or equal to the values listed in the table.</span></span> <span data-ttu-id="ea846-180">다음 표에는 .NET Framework 버전 및 이에 해당되는 `Release` 키워드가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-180">Here are the .NET Framework versions and associated `Release` keywords.</span></span>

    [!INCLUDE[Release key values note](~/includes/version-keys-note.md)]

    |<span data-ttu-id="ea846-181">버전</span><span class="sxs-lookup"><span data-stu-id="ea846-181">Version</span></span>|<span data-ttu-id="ea846-182">릴리스 DWORD의 값</span><span class="sxs-lookup"><span data-stu-id="ea846-182">Value of the Release DWORD</span></span>|
    |-------------|--------------------------------|
    |<span data-ttu-id="ea846-183">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="ea846-183">.NET Framework 4.5</span></span>|<span data-ttu-id="ea846-184">378389</span><span class="sxs-lookup"><span data-stu-id="ea846-184">378389</span></span>|
    |<span data-ttu-id="ea846-185">.NET Framework 4.5.1이 Windows 8.1과 함께 설치됨</span><span class="sxs-lookup"><span data-stu-id="ea846-185">.NET Framework 4.5.1 installed with Windows 8.1</span></span>|<span data-ttu-id="ea846-186">378675</span><span class="sxs-lookup"><span data-stu-id="ea846-186">378675</span></span>|
    |<span data-ttu-id="ea846-187">.NET Framework 4.5.1이 Windows 8, Windows 7 SP1 또는 Windows Vista SP2에 설치됨</span><span class="sxs-lookup"><span data-stu-id="ea846-187">.NET Framework 4.5.1 installed on Windows 8, Windows 7 SP1, or Windows Vista SP2</span></span>|<span data-ttu-id="ea846-188">378758</span><span class="sxs-lookup"><span data-stu-id="ea846-188">378758</span></span>|
    |<span data-ttu-id="ea846-189">.NET Framework 4.5.2</span><span class="sxs-lookup"><span data-stu-id="ea846-189">.NET Framework 4.5.2</span></span>|<span data-ttu-id="ea846-190">379893</span><span class="sxs-lookup"><span data-stu-id="ea846-190">379893</span></span>|
    |<span data-ttu-id="ea846-191">.NET Framework 4.6이 Windows 10과 함께 설치됨</span><span class="sxs-lookup"><span data-stu-id="ea846-191">.NET Framework 4.6 installed with Windows 10</span></span>|<span data-ttu-id="ea846-192">393295</span><span class="sxs-lookup"><span data-stu-id="ea846-192">393295</span></span>|
    |<span data-ttu-id="ea846-193">.NET Framework 4.6이 다른 모든 Windows OS 버전에 설치됨</span><span class="sxs-lookup"><span data-stu-id="ea846-193">.NET Framework 4.6 installed on all other Windows OS versions</span></span>|<span data-ttu-id="ea846-194">393297</span><span class="sxs-lookup"><span data-stu-id="ea846-194">393297</span></span>|
    |<span data-ttu-id="ea846-195">.NET Framework 4.6.1이 Windows 10에 설치됨</span><span class="sxs-lookup"><span data-stu-id="ea846-195">.NET Framework 4.6.1 installed on Windows 10</span></span>|<span data-ttu-id="ea846-196">394254</span><span class="sxs-lookup"><span data-stu-id="ea846-196">394254</span></span>|
    |<span data-ttu-id="ea846-197">.NET Framework 4.6.1이 다른 모든 Windows OS 버전에 설치됨</span><span class="sxs-lookup"><span data-stu-id="ea846-197">.NET Framework 4.6.1 installed on all other Windows OS versions</span></span>|<span data-ttu-id="ea846-198">394271</span><span class="sxs-lookup"><span data-stu-id="ea846-198">394271</span></span>|
    |<span data-ttu-id="ea846-199">.NET Framework 4.6.2가 Windows 10 1주년 업데이트 및 Windows Server 2016에 설치됨</span><span class="sxs-lookup"><span data-stu-id="ea846-199">.NET Framework 4.6.2 installed on Windows 10 Anniversary Update and Windows Server 2016</span></span>|<span data-ttu-id="ea846-200">394802</span><span class="sxs-lookup"><span data-stu-id="ea846-200">394802</span></span>|
    |<span data-ttu-id="ea846-201">.NET Framework 4.6.2가 다른 모든 Windows OS 버전에 설치됨</span><span class="sxs-lookup"><span data-stu-id="ea846-201">.NET Framework 4.6.2 installed on all other Windows OS versions</span></span>|<span data-ttu-id="ea846-202">394806</span><span class="sxs-lookup"><span data-stu-id="ea846-202">394806</span></span>|
    |<span data-ttu-id="ea846-203">.NET Framework 4.7이 Windows 10 크리에이터 업데이트에 설치됨</span><span class="sxs-lookup"><span data-stu-id="ea846-203">.NET Framework 4.7 installed on Windows 10 Creators Update</span></span>|<span data-ttu-id="ea846-204">460798</span><span class="sxs-lookup"><span data-stu-id="ea846-204">460798</span></span>|
    |<span data-ttu-id="ea846-205">.NET Framework 4.7이 다른 모든 Windows OS 버전에 설치됨</span><span class="sxs-lookup"><span data-stu-id="ea846-205">.NET Framework 4.7 installed on all other Windows OS versions</span></span>|<span data-ttu-id="ea846-206">460805</span><span class="sxs-lookup"><span data-stu-id="ea846-206">460805</span></span>|
    |<span data-ttu-id="ea846-207">Windows 10 Fall Creators Update에 설치된 .NET Framework 4.7.1</span><span class="sxs-lookup"><span data-stu-id="ea846-207">.NET Framework 4.7.1 installed on Windows 10 Fall Creators Update</span></span>|<span data-ttu-id="ea846-208">461308</span><span class="sxs-lookup"><span data-stu-id="ea846-208">461308</span></span>|
    |<span data-ttu-id="ea846-209">.NET Framework 4.7.1이 다른 모든 Windows OS 버전에 설치됨</span><span class="sxs-lookup"><span data-stu-id="ea846-209">.NET Framework 4.7.1 installed on all other Windows OS versions</span></span>|<span data-ttu-id="ea846-210">461310</span><span class="sxs-lookup"><span data-stu-id="ea846-210">461310</span></span>|
    |<span data-ttu-id="ea846-211">.NET Framework 4.7.2가 Windows 10 2018년 10월 업데이트에 설치됨</span><span class="sxs-lookup"><span data-stu-id="ea846-211">.NET Framework 4.7.2 installed on Windows 10 October 2018 Update</span></span>|<span data-ttu-id="ea846-212">461814</span><span class="sxs-lookup"><span data-stu-id="ea846-212">461814</span></span>|
    |<span data-ttu-id="ea846-213">.NET Framework 4.7.2가 Windows 10 2018년 4월 업데이트에 설치됨</span><span class="sxs-lookup"><span data-stu-id="ea846-213">.NET Framework 4.7.2 installed on Windows 10 April 2018 Update</span></span>|<span data-ttu-id="ea846-214">461808</span><span class="sxs-lookup"><span data-stu-id="ea846-214">461808</span></span>|
    |<span data-ttu-id="ea846-215">.NET Framework 4.7.2가 Windows 10 Fall Creators Update 이하 OS 버전에 설치됨</span><span class="sxs-lookup"><span data-stu-id="ea846-215">.NET Framework 4.7.2 installed on Windows 10 Fall Creators Update and earlier OS versions</span></span>|<span data-ttu-id="ea846-216">461814</span><span class="sxs-lookup"><span data-stu-id="ea846-216">461814</span></span>|
    
     <span data-ttu-id="ea846-217">다음 예제에서는 레지스트리에서 `Release` 값을 확인하여 [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] 또는 이후 버전의 .NET Framework가 설치되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-217">The following example checks the `Release` value in the registry to determine whether the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] or a later version of the .NET Framework is installed.</span></span>

     [!code-csharp[ListVersions#5](../../../samples/snippets/csharp/framework/migration-guide/versions-installed3.cs)]
     [!code-vb[ListVersions#5](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed3.vb)]

     <span data-ttu-id="ea846-218">이 예제에서는 버전을 확인하기 위한 권장된 방법을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-218">This example follows the recommended practice for version checking:</span></span>

    - <span data-ttu-id="ea846-219">`Release` 항목의 값이 알려진 릴리즈 키의 값보다 *크거나 같은지* 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-219">It checks whether the value of the `Release` entry is *greater than or equal to* the value of the known release keys.</span></span>

    - <span data-ttu-id="ea846-220">최신 버전에서 가장 오래된 버전 순서대로 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-220">It checks in order from most recent version to earliest version.</span></span>

<a name="ps_a"></a> 
## <a name="to-check-for-a-minimum-required-net-framework-version-by-querying-the-registry-in-powershell-net-framework-45-and-later"></a><span data-ttu-id="ea846-221">PowerShell로 레지스트리를 쿼리하여 최소한 필요한 .NET Framework 버전을 확인하려면(.NET Framework 4.5 이상)</span><span class="sxs-lookup"><span data-stu-id="ea846-221">To check for a minimum-required .NET Framework version by querying the registry in PowerShell (.NET Framework 4.5 and later)</span></span>

- <span data-ttu-id="ea846-222">다음 예제에서는 `Release` 키워드 값을 확인하여 Windows OS 버전에 관계없이 .NET Framework 4.6.2 이상이 설치되어 있는지 확인합니다(해당하는 경우 `True` 반환, 이외의 경우 `False` 반환).</span><span class="sxs-lookup"><span data-stu-id="ea846-222">The following example checks the value of the `Release` keyword to determine whether .NET Framework 4.6.2 or higher is installed, regardless of Windows OS version (returning `True` if it is and `False` otherwise).</span></span>

    ```PowerShell
    # PowerShell 5
    Get-ChildItem 'HKLM:\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full\' | Get-ItemPropertyValue -Name Release | Foreach-Object { $_ -ge 394802 } 
    ```

    ```PowerShell
    # PowerShell 4
    (Get-ItemProperty "HKLM:SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full").Release -gt 394802
    ```

    <span data-ttu-id="ea846-223">다른 최소한 필요한 .NET Framework 버전을 확인하기 위해 이전 예제의 `394802`를 다음 표의 다른 값으로 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-223">You can replace `394802` in the previous example with another value from the following table to check for a different minimum-required .NET Framework version.</span></span>
  
    |<span data-ttu-id="ea846-224">버전</span><span class="sxs-lookup"><span data-stu-id="ea846-224">Version</span></span>|<span data-ttu-id="ea846-225">릴리스 DWORD의 최소 값</span><span class="sxs-lookup"><span data-stu-id="ea846-225">Minimum value of the Release DWORD</span></span>|
    |-------------|--------------------------------|
    |<span data-ttu-id="ea846-226">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="ea846-226">.NET Framework 4.5</span></span>|<span data-ttu-id="ea846-227">378389</span><span class="sxs-lookup"><span data-stu-id="ea846-227">378389</span></span>|
    |<span data-ttu-id="ea846-228">.NET Framework 4.5.1</span><span class="sxs-lookup"><span data-stu-id="ea846-228">.NET Framework 4.5.1</span></span>|<span data-ttu-id="ea846-229">378675</span><span class="sxs-lookup"><span data-stu-id="ea846-229">378675</span></span>|
    |<span data-ttu-id="ea846-230">.NET Framework 4.5.2</span><span class="sxs-lookup"><span data-stu-id="ea846-230">.NET Framework 4.5.2</span></span>|<span data-ttu-id="ea846-231">379893</span><span class="sxs-lookup"><span data-stu-id="ea846-231">379893</span></span>|
    |[!INCLUDE[net_v46](../../../includes/net-v46-md.md)]|<span data-ttu-id="ea846-232">393295</span><span class="sxs-lookup"><span data-stu-id="ea846-232">393295</span></span>|
    |[!INCLUDE[net_v461](../../../includes/net-v461-md.md)]|<span data-ttu-id="ea846-233">394254</span><span class="sxs-lookup"><span data-stu-id="ea846-233">394254</span></span>|
    |[!INCLUDE[net_v462](../../../includes/net-v462-md.md)]|<span data-ttu-id="ea846-234">394802</span><span class="sxs-lookup"><span data-stu-id="ea846-234">394802</span></span>|
    |<span data-ttu-id="ea846-235">.NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="ea846-235">.NET Framework 4.7</span></span>|<span data-ttu-id="ea846-236">460798</span><span class="sxs-lookup"><span data-stu-id="ea846-236">460798</span></span>|
    |<span data-ttu-id="ea846-237">.NET Framework 4.7.1</span><span class="sxs-lookup"><span data-stu-id="ea846-237">.NET Framework 4.7.1</span></span>|<span data-ttu-id="ea846-238">461308</span><span class="sxs-lookup"><span data-stu-id="ea846-238">461308</span></span>|
    |<span data-ttu-id="ea846-239">.NET Framework 4.7.2</span><span class="sxs-lookup"><span data-stu-id="ea846-239">.NET Framework 4.7.2</span></span>|<span data-ttu-id="ea846-240">461808</span><span class="sxs-lookup"><span data-stu-id="ea846-240">461808</span></span>|

<a name="clr_a"></a> 
## <a name="to-find-the-current-runtime-version-by-using-the-clrver-tool"></a><span data-ttu-id="ea846-241">Clrver 도구를 사용하여 현재 런타임 버전을 찾으려면</span><span class="sxs-lookup"><span data-stu-id="ea846-241">To find the current runtime version by using the Clrver tool</span></span>

- <span data-ttu-id="ea846-242">CLR 버전 도구(Clrver.exe)를 사용하여 컴퓨터에 설치된 공용 언어 런타임의 버전을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-242">Use the CLR Version Tool (Clrver.exe) to determine which versions of the common language runtime are installed on a computer.</span></span>

     <span data-ttu-id="ea846-243">Visual Studio 명령 프롬프트에서 `clrver`을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-243">From a Visual Studio Command Prompt, enter `clrver`.</span></span> <span data-ttu-id="ea846-244">이 명령은 다음과 유사한 출력 결과를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-244">This command produces output similar to the following:</span></span>

    ```
    Versions installed on the machine:
    v2.0.50727
    v4.0.30319
    ```

     <span data-ttu-id="ea846-245">이 도구의 사용 방법에 대한 자세한 내용은 [Clrver.exe(CLR 버전 도구)](~/docs/framework/tools/clrver-exe-clr-version-tool.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ea846-245">For more information about using this tool, see [Clrver.exe (CLR Version Tool)](~/docs/framework/tools/clrver-exe-clr-version-tool.md).</span></span>

<a name="clr_b"></a> 
## <a name="to-find-the-current-runtime-version-by-querying-the-environment-class-in-code"></a><span data-ttu-id="ea846-246">Environment 클래스를 코드로 쿼리하여 현재 런타임 버전을 확인하려면</span><span class="sxs-lookup"><span data-stu-id="ea846-246">To find the current runtime version by querying the Environment class in code</span></span>

- <span data-ttu-id="ea846-247">현재 코드를 실행하는 런타임 버전을 식별하는 <xref:System.Version> 개체를 검색하기 위해 <xref:System.Environment.Version%2A?displayProperty=nameWithType> 속성을 쿼리합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-247">Query the <xref:System.Environment.Version%2A?displayProperty=nameWithType> property to retrieve a <xref:System.Version> object that identifies the version of the runtime that is currently executing the code.</span></span> <span data-ttu-id="ea846-248"><xref:System.Version.Major%2A?displayProperty=nameWithType> 속성을 사용하여 주 릴리스 식별자(예: 버전 4.0의 "4")를 얻거나 <xref:System.Version.Minor%2A?displayProperty=nameWithType> 속성을 사용하여 부 릴리스 식별자(예: 버전 4.0의 "0")를 얻거나 <xref:System.Object.ToString%2A?displayProperty=nameWithType> 메서드를 사용하여 전체 버전 문자열(예: 다음 코드에 표시된 "4.0.30319.18010")을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-248">You can use the <xref:System.Version.Major%2A?displayProperty=nameWithType> property to get the major release identifier (for example, "4" for version 4.0), the <xref:System.Version.Minor%2A?displayProperty=nameWithType> property to get the minor release identifier (for example, "0" for version 4.0), or the <xref:System.Object.ToString%2A?displayProperty=nameWithType> method to get the entire version string (for example, "4.0.30319.18010", as shown in the following code).</span></span> <span data-ttu-id="ea846-249">이 속성은 현재 코드를 실행 중인 런타임 버전을 반영하는 단일 값을 반환합니다. 컴퓨터에 설치되어 있을 수 있는 다른 버전의 런타임이나 어셈블리 버전은 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-249">This property returns a single value that reflects the version of the runtime that is currently executing the code; it does not return assembly versions or other versions of the runtime that may have been installed on the computer.</span></span>

     <span data-ttu-id="ea846-250">.NET Framework 버전 4, 4.5, 4.5.1 및 4.5.2의 경우 <xref:System.Environment.Version%2A?displayProperty=nameWithType> 속성은 문자열 표시가 `4.0.30319.xxxxx` 형식인 <xref:System.Version> 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-250">For the .NET Framework Versions 4, 4.5, 4.5.1, and 4.5.2, the <xref:System.Environment.Version%2A?displayProperty=nameWithType> property returns a <xref:System.Version> object whose string representation has the form `4.0.30319.xxxxx`.</span></span> <span data-ttu-id="ea846-251">.NET Framework 4.6 이상에서는 `4.0.30319.42000` 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-251">For the .NET Framework 4.6 and later, it has the form `4.0.30319.42000`.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="ea846-252">[!INCLUDE[net_v45](../../../includes/net-v45-md.md)] 이상의 경우 <xref:System.Environment.Version%2A?displayProperty=nameWithType> 속성을 사용하여 런타임 버전을 확인하는 것을 권장하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-252">For the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] and later, we do not recommend using the  <xref:System.Environment.Version%2A?displayProperty=nameWithType> property to detect the version of the runtime.</span></span> <span data-ttu-id="ea846-253">대신 이 문서의 앞부분에 나오는 [코드로 레지스트리를 쿼리하여 .NET Framework 버전을 찾으려면(.NET Framework 4.5 이상)](#net_d) 섹션에서 설명된 것처럼 레지스트리를 쿼리하는 것을 권장합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-253">Instead, we recommend that you query the registry, as described in the [To find .NET Framework versions by querying the registry in code (.NET Framework 4.5 and later)](#net_d) section earlier in this article.</span></span>

     <span data-ttu-id="ea846-254">런타임 버전 정보의 <xref:System.Environment.Version%2A?displayProperty=nameWithType> 속성을 쿼리하는 예제는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-254">Here's an example of querying the <xref:System.Environment.Version%2A?displayProperty=nameWithType> property for runtime version information:</span></span>

     [!code-csharp[ListVersions](../../../samples/snippets/csharp/framework/migration-guide/versions-installed2.cs)]
     [!code-vb[ListVersions](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed2.vb)]

     <span data-ttu-id="ea846-255">이 예제는 다음과 유사한 출력 결과를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="ea846-255">The example produces output that's similar to the following:</span></span>

    ```
    Version: 4.0.30319.18010
    ```

## <a name="see-also"></a><span data-ttu-id="ea846-256">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ea846-256">See also</span></span>

[<span data-ttu-id="ea846-257">방법: 설치된 .NET Framework 업데이트 확인</span><span class="sxs-lookup"><span data-stu-id="ea846-257">How to: Determine Which .NET Framework Updates Are Installed</span></span>](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md)  
[<span data-ttu-id="ea846-258">개발자용 .NET Framework 설치</span><span class="sxs-lookup"><span data-stu-id="ea846-258">Install the .NET Framework for developers</span></span>](../../../docs/framework/install/guide-for-developers.md)  
[<span data-ttu-id="ea846-259">버전 및 종속성</span><span class="sxs-lookup"><span data-stu-id="ea846-259">Versions and Dependencies</span></span>](~/docs/framework/migration-guide/versions-and-dependencies.md)  
