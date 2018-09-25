---
title: '방법: 자동 바인딩 리디렉션 사용 설정 및 해제'
ms.date: 09/12/2018
helpviewer_keywords:
- side-by-side execution, assembly binding redirection
- assemblies [.NET Framework], binding redirection
ms.assetid: 5fca42f3-bdce-4b81-a704-61e42c89d3ba
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 9b9c9cbdb89ccf67942dcccee37ea410c6fa39a5
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47079545"
---
# <a name="how-to-enable-and-disable-automatic-binding-redirection"></a><span data-ttu-id="34885-102">방법: 자동 바인딩 리디렉션 사용 설정 및 해제</span><span class="sxs-lookup"><span data-stu-id="34885-102">How to: Enable and Disable Automatic Binding Redirection</span></span>

<span data-ttu-id="34885-103">대상으로 하는 Visual Studio에서 앱을 컴파일할 때의 [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] 이상 버전에서는 바인딩 리디렉션이 어셈블리 통합을 재정의 하도록 앱 구성 파일을에 자동으로 추가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34885-103">When you compile apps in Visual Studio that target the [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] and later versions, binding redirects may be automatically added to the app configuration file to override assembly unification.</span></span> <span data-ttu-id="34885-104">수동으로 바인딩 리디렉션을 응용 프로그램의 구성 파일에 지정할 지라도 응용 프로그램 또는 해당 구성 요소가 동일 어셈블리의 두 개 이상의 버전을 참조할 경우 바인딩 리디렉션을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="34885-104">Binding redirects are added if your app or its components reference more than one version of the same assembly, even if you manually specify binding redirects in the configuration file for your app.</span></span> <span data-ttu-id="34885-105">자동 바인딩 리디렉션 기능에 영향을 기존 데스크톱 앱 및 web apps의 대상으로 하는 [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] 이상 버전, 웹 앱에 대 한 동작을 약간 다릅니다. 하지만 합니다.</span><span class="sxs-lookup"><span data-stu-id="34885-105">The automatic binding redirection feature affects traditional desktop apps and web apps that target the [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] or a later version, although the behavior is slightly different for a web app.</span></span> <span data-ttu-id="34885-106">이전 버전의 .NET Framework를 대상으로 하는 기존 응용 프로그램이 있는 경우 자동 바인딩 리디렉션을 사용할 수 있으며, 수동으로 작성되는 바인딩 리디렉션을 유지하려는 경우에는 이 기능을 비활성화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34885-106">You can enable automatic binding redirection if you have existing apps that target previous versions of the .NET Framework, or you can disable this feature if you want to keep manually authored binding redirects.</span></span>

## <a name="disable-automatic-binding-redirects-in-desktop-apps"></a><span data-ttu-id="34885-107">데스크톱 앱에서 자동 바인딩 리디렉션을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="34885-107">Disable automatic binding redirects in desktop apps</span></span>

<span data-ttu-id="34885-108">자동 바인딩 리디렉션은 [!INCLUDE[net_v451](../../../includes/net-v451-md.md)]을 대상으로 하는 기존 데스크톱 앱에 대해 기본적으로 사용하도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="34885-108">Automatic binding redirects are enabled by default for traditional desktop apps that target the [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] and later versions.</span></span> <span data-ttu-id="34885-109">응용 프로그램이 컴파일되고 그렇지 않으면 발생할 수 있는 어셈블리 통합을 재정의할 때 바인딩 리디렉션이 출력 구성(app.config) 파일에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="34885-109">The binding redirects are added to the output configuration (app.config) file when the app is compiled and overrides the assembly unification that might otherwise take place.</span></span> <span data-ttu-id="34885-110">소스 app.config 파일은 수정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34885-110">The source app.config file is not modified.</span></span> <span data-ttu-id="34885-111">응용 프로그램에 대한 프로젝트 파일을 수정하여 이 기능을 비활성화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34885-111">You can disable this feature by modifying the project file for the app.</span></span>

1. <span data-ttu-id="34885-112">다음 방법 중 하나를 사용 하 여 편집할 프로젝트 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="34885-112">Open the project file for editing using one of the following methods:</span></span>

   - <span data-ttu-id="34885-113">Visual Studio에서 프로젝트를 선택 **솔루션 탐색기**를 선택한 후 **파일 탐색기에서 폴더 열기** 바로 가기 메뉴에서.</span><span class="sxs-lookup"><span data-stu-id="34885-113">In Visual Studio, select the project in **Solution Explorer**, and then choose **Open Folder in File Explorer** from the shortcut menu.</span></span> <span data-ttu-id="34885-114">파일 탐색기에서 프로젝트 (.csproj 또는.vbproj) 파일을 찾아서 메모장에서 엽니다.</span><span class="sxs-lookup"><span data-stu-id="34885-114">In File Explorer, find the project (.csproj or .vbproj) file and open it in Notepad.</span></span>
   - <span data-ttu-id="34885-115">Visual Studio에서의 **솔루션 탐색기**프로젝트를 마우스 오른쪽 단추로 클릭 하 고 선택 **프로젝트 언로드**합니다.</span><span class="sxs-lookup"><span data-stu-id="34885-115">In Visual Studio, in **Solution Explorer**, right-click the project and choose **Unload Project**.</span></span> <span data-ttu-id="34885-116">언로드된 프로젝트를 다시 마우스 오른쪽 단추로 클릭 하 고 선택한 **[projectname.csproj] 편집**합니다.</span><span class="sxs-lookup"><span data-stu-id="34885-116">Right-click the unloaded project again, and then choose **Edit [projectname.csproj]**.</span></span>

2. <span data-ttu-id="34885-117">프로젝트 파일에서 다음 속성 항목을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="34885-117">In the project file, find the following property entry:</span></span>

   ```xml
   <AutoGenerateBindingRedirects>true</AutoGenerateBindingRedirects>
   ```

3. <span data-ttu-id="34885-118">`true`를 `false`로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="34885-118">Change `true` to `false`:</span></span>

   ```xml
   <AutoGenerateBindingRedirects>false</AutoGenerateBindingRedirects>
   ```

## <a name="enable-automatic-binding-redirects-manually"></a><span data-ttu-id="34885-119">수동으로 자동 바인딩 리디렉션을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="34885-119">Enable automatic binding redirects manually</span></span>

<span data-ttu-id="34885-120">해당 대상 이전 버전의.NET Framework 또는 자동으로 묻는 리디렉션을 추가 하는 경우 기존 앱에서 자동 바인딩 리디렉션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34885-120">You can enable automatic binding redirects in existing apps that target older versions of the .NET Framework, or in cases where you're not automatically prompted to add a redirect.</span></span> <span data-ttu-id="34885-121">최신 버전의 framework 대상으로 하지만 경우 수행 메시지가 자동으로 나타나지 리디렉션을 추가 하 가능성이 어셈블리를 다시 매핑하도록 제안 하는 빌드 출력을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34885-121">If you're targeting a newer version of the framework but do not get automatically prompted to add a redirect, you'll likely get build output that suggests you remap assemblies.</span></span>

1. <span data-ttu-id="34885-122">다음 방법 중 하나를 사용 하 여 편집할 프로젝트 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="34885-122">Open the project file for editing using one of the following methods:</span></span>

   - <span data-ttu-id="34885-123">Visual Studio에서 프로젝트를 선택 **솔루션 탐색기**를 선택한 후 **파일 탐색기에서 폴더 열기** 바로 가기 메뉴에서.</span><span class="sxs-lookup"><span data-stu-id="34885-123">In Visual Studio, select the project in **Solution Explorer**, and then choose **Open Folder in File Explorer** from the shortcut menu.</span></span> <span data-ttu-id="34885-124">파일 탐색기에서 프로젝트 (.csproj 또는.vbproj) 파일을 찾아서 메모장에서 엽니다.</span><span class="sxs-lookup"><span data-stu-id="34885-124">In File Explorer, find the project (.csproj or .vbproj) file and open it in Notepad.</span></span>
   - <span data-ttu-id="34885-125">Visual Studio에서의 **솔루션 탐색기**프로젝트를 마우스 오른쪽 단추로 클릭 하 고 선택 **프로젝트 언로드**합니다.</span><span class="sxs-lookup"><span data-stu-id="34885-125">In Visual Studio, in **Solution Explorer**, right-click the project and choose **Unload Project**.</span></span> <span data-ttu-id="34885-126">언로드된 프로젝트를 다시 마우스 오른쪽 단추로 클릭 하 고 선택한 **[projectname.csproj] 편집**합니다.</span><span class="sxs-lookup"><span data-stu-id="34885-126">Right-click the unloaded project again, and then choose **Edit [projectname.csproj]**.</span></span>

2. <span data-ttu-id="34885-127">첫 번째 구성 속성 그룹에 다음 요소를 추가 (아래는 \<PropertyGroup > 태그).</span><span class="sxs-lookup"><span data-stu-id="34885-127">Add the following element to the first configuration property group (under the \<PropertyGroup> tag):</span></span>

   ```xml
   <AutoGenerateBindingRedirects>true</AutoGenerateBindingRedirects>
   ```

   <span data-ttu-id="34885-128">다음은 삽입 된 요소를 사용 하 여 예제 프로젝트 파일.</span><span class="sxs-lookup"><span data-stu-id="34885-128">The following shows an example project file with the element inserted:</span></span>

   ```xml
   <?xml version="1.0" encoding="utf-8"?>
   <Project ToolsVersion="12.0" DefaultTargets="Build" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
     <Import Project="$(MSBuildExtensionsPath)\$(MSBuildToolsVersion)\Microsoft.Common.props" Condition="Exists('$(MSBuildExtensionsPath)\$(MSBuildToolsVersion)\Microsoft.Common.props')" />
       <PropertyGroup>
         <Configuration Condition=" '$(Configuration)' == ''     ">Debug</Configuration>
         <Platform Condition=" '$(Platform)' == '' ">AnyCPU</Platform>
         <ProjectGuid>{123334}</ProjectGuid>
         ...
         <AutoGenerateBindingRedirects>true</AutoGenerateBindingRedirects>
       </PropertyGroup>
     ...
   </Project>
   ```

3. <span data-ttu-id="34885-129">응용 프로그램을 컴파일합니다.</span><span class="sxs-lookup"><span data-stu-id="34885-129">Compile your app.</span></span>

## <a name="enable-automatic-binding-redirects-in-web-apps"></a><span data-ttu-id="34885-130">Web apps에서 자동 바인딩 리디렉션을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="34885-130">Enable automatic binding redirects in web apps</span></span>

<span data-ttu-id="34885-131">자동 바인딩 리디렉션은 웹 응용 프로그램마다 다르게 구현됩니다.</span><span class="sxs-lookup"><span data-stu-id="34885-131">Automatic binding redirects are implemented differently for web apps.</span></span> <span data-ttu-id="34885-132">웹 응용 프로그램에 대한 원본 구성(web.config) 파일을 수정해야 하기 때문에 구성 파일에 바인딩 리디렉션은 자동으로 추가되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34885-132">Because the source configuration (web.config) file must be modified for web apps, binding redirects are not automatically added to the configuration file.</span></span> <span data-ttu-id="34885-133">하지만 Visual Studio는 바인딩 충돌을 경고하고 충돌 해결을 위해 바인딩 리디렉션을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34885-133">However, Visual Studio notifies you of binding conflicts, and you can add binding redirects to resolve the conflicts.</span></span> <span data-ttu-id="34885-134">항상 바인딩 리디렉션을 추가 하는 메시지가 때문에 명시적으로 웹 앱에 대해이 기능을 사용 하지 않도록 설정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="34885-134">Because you're always prompted to add binding redirects, you don't need to explicitly disable this feature for a web app.</span></span>

<span data-ttu-id="34885-135">Web.config 파일에 바인딩 리디렉션을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="34885-135">To add binding redirects to a web.config file:</span></span>

1. <span data-ttu-id="34885-136">Visual Studio에서 응용 프로그램을 컴파일하고 빌드 경고를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="34885-136">In Visual Studio, compile the app, and check for build warnings.</span></span>

   <span data-ttu-id="34885-137">![어셈블리 참고 충돌에 대 한 경고를 빌드](../../../docs/framework/configure-apps/media/clr-assemblyrefwarning.png "CLR_AssemblyRefWarning")</span><span class="sxs-lookup"><span data-stu-id="34885-137">![Build warning for assembly reference conflicts](../../../docs/framework/configure-apps/media/clr-assemblyrefwarning.png "CLR_AssemblyRefWarning")</span></span>

2. <span data-ttu-id="34885-138">어셈블리 바인딩 충돌이 있을 경우 경고가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="34885-138">If there are assembly binding conflicts, a warning appears.</span></span> <span data-ttu-id="34885-139">경고를 두 번 클릭 하거나 선택 하 고 경고 press **Enter**합니다.</span><span class="sxs-lookup"><span data-stu-id="34885-139">Double-click the warning, or select the warning and press **Enter**.</span></span>

   <span data-ttu-id="34885-140">필요한 바인딩 리디렉션을 소스 web.config 파일에 자동으로 추가할 수 있는 대화 상자가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="34885-140">A dialog box that enables you to automatically add the necessary binding redirects to the source web.config file appears.</span></span>

   <span data-ttu-id="34885-141">![바인딩 리디렉션 권한 대화 상자](../../../docs/framework/configure-apps/media/clr-addbindingredirect.png "CLR_AddBindingRedirect")</span><span class="sxs-lookup"><span data-stu-id="34885-141">![Binding redirect permission dialog](../../../docs/framework/configure-apps/media/clr-addbindingredirect.png "CLR_AddBindingRedirect")</span></span>

## <a name="see-also"></a><span data-ttu-id="34885-142">참고자료</span><span class="sxs-lookup"><span data-stu-id="34885-142">See also</span></span>

- [<span data-ttu-id="34885-143">\<bindingRedirect > 요소</span><span class="sxs-lookup"><span data-stu-id="34885-143">\<bindingRedirect> Element</span></span>](../../../docs/framework/configure-apps/file-schema/runtime/bindingredirect-element.md)
- [<span data-ttu-id="34885-144">어셈블리 버전 리디렉션</span><span class="sxs-lookup"><span data-stu-id="34885-144">Redirecting Assembly Versions</span></span>](../../../docs/framework/configure-apps/redirect-assembly-versions.md)
