---
title: '방법: 글로벌 어셈블리 캐시에 어셈블리 설치'
ms.date: 02/05/2019
helpviewer_keywords:
- assemblies [.NET Framework], global assembly cache
- Gacutil.exe
- strong-named assemblies, global assembly cache
- global assembly cache, installing assemblies
- Global Assembly Cache tool
- windows installer, global assembly cache
ms.assetid: a7e6f091-d02c-49ba-b736-7295cb0eb743
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 233a7803cb59f9bfeac15d293dc3fb5a0db449c9
ms.sourcegitcommit: c6f69b0cf149f6b54483a6d5c2ece222913f43ce
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55903753"
---
# <a name="how-to-install-an-assembly-into-the-global-assembly-cache"></a><span data-ttu-id="72800-102">방법: 글로벌 어셈블리 캐시에 어셈블리 설치</span><span class="sxs-lookup"><span data-stu-id="72800-102">How to: Install an assembly into the global assembly cache</span></span>

<span data-ttu-id="72800-103">GAC(글로벌 어셈블리 캐시)는 여러 애플리케이션이 공유하는 어셈블리를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="72800-103">The global assembly cache (GAC) stores assemblies that several applications share.</span></span> <span data-ttu-id="72800-104">다음 구성 요소 중 하나를 사용하여 [글로벌 어셈블리 캐시](gac.md)에 어셈블리를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="72800-104">Install an assembly into the [global assembly cache](gac.md) with one of the following components:</span></span> 
- [<span data-ttu-id="72800-105">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="72800-105">Windows Installer</span></span>](#windows-installer)
- [<span data-ttu-id="72800-106">전역 어셈블리 캐시 도구</span><span class="sxs-lookup"><span data-stu-id="72800-106">Global assembly cache tool</span></span>](#global-assembly-cache-tool)

> [!IMPORTANT]
> <span data-ttu-id="72800-107">강력한 이름의 어셈블리만 GAC에 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72800-107">You can install only strong-named assemblies into the GAC.</span></span> <span data-ttu-id="72800-108">강력한 이름의 어셈블리를 만드는 방법에 대한 자세한 내용은 [방법: 강력한 이름으로 어셈블리 서명](how-to-sign-an-assembly-with-a-strong-name.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="72800-108">For information about how to create a strong-named assembly, see [How to: Sign an assembly with a strong name](how-to-sign-an-assembly-with-a-strong-name.md).</span></span>

## <a name="windows-installer"></a><span data-ttu-id="72800-109">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="72800-109">Windows Installer</span></span>

<span data-ttu-id="72800-110">Windows 설치 엔진인 [Windows Installer](/windows/desktop/Msi/installation-of-assemblies-to-the-global-assembly-cache)는 전역 어셈블리 캐시에 어셈블리를 추가하는 권장 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="72800-110">[Windows Installer](/windows/desktop/Msi/installation-of-assemblies-to-the-global-assembly-cache), the Windows installation engine, is the recommended way to add assemblies to the global assembly cache.</span></span> <span data-ttu-id="72800-111">Windows Installer는 전역 어셈블리 캐시의 어셈블리 참조 횟수 및 다른 여러 가지 혜택을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="72800-111">Windows Installer provides reference counting of assemblies in the global assembly cache and other benefits.</span></span> <span data-ttu-id="72800-112">Windows Installer용 설치 관리자 패키지를 만들려면 [Visual Studio 2017용 WiX Toolset 확장](https://marketplace.visualstudio.com/items?itemName=RobMensching.WixToolsetVisualStudio2017Extension)을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="72800-112">To create an installer package for Windows Installer, use the [WiX toolset extension for Visual Studio 2017](https://marketplace.visualstudio.com/items?itemName=RobMensching.WixToolsetVisualStudio2017Extension).</span></span>

## <a name="global-assembly-cache-tool"></a><span data-ttu-id="72800-113">전역 어셈블리 캐시 도구</span><span class="sxs-lookup"><span data-stu-id="72800-113">Global assembly cache tool</span></span>

<span data-ttu-id="72800-114">[글로벌 어셈블리 캐시 도구(gacutil.exe)](../tools/gacutil-exe-gac-tool.md)를 사용하여 어셈블리를 글로벌 어셈블리 캐시에 추가하고 글로벌 어셈블리 캐시의 콘텐츠를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72800-114">You can use the [global assembly cache tool (gacutil.exe)](../tools/gacutil-exe-gac-tool.md) to add assemblies to the global assembly cache and to view the contents of the global assembly cache.</span></span>

   > [!NOTE]
   > <span data-ttu-id="72800-115">*Gacutil.exe*는 개발 목적으로만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="72800-115">*Gacutil.exe* is for development purposes only.</span></span> <span data-ttu-id="72800-116">해당 파일을 사용하여 프로덕션 어셈블리를 글로벌 어셈블리 캐시에 설치하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="72800-116">Don't use it to install production assemblies into the global assembly cache.</span></span>

<span data-ttu-id="72800-117">GAC에 어셈블리를 설치하기 위해 *gacutil.exe*를 사용하는 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="72800-117">The syntax for using *gacutil.exe* to install an assembly in the GAC is as follows:</span></span>

```console
gacutil -i <assembly name>
```

<span data-ttu-id="72800-118">이 명령에서 *\<어셈블리 이름>* 은 글로벌 어셈블리 캐시에 설치할 어셈블리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72800-118">In this command, *\<assembly name>* is the name of the assembly to install in the global assembly cache.</span></span>

<span data-ttu-id="72800-119">*gacutil.exe*가 시스템 경로에 없는 경우 [eveloper Command Prompt for VS *\<version>*](../tools/developer-command-prompt-for-vs.md)을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="72800-119">If *gacutil.exe* isn't in your system path, use the [Developer Command Prompt for VS *\<version>*](../tools/developer-command-prompt-for-vs.md).</span></span>

<span data-ttu-id="72800-120">다음 예제는 파일 이름이 *hello.dll*인 어셈블리를 글로벌 어셈블리 캐시에 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="72800-120">The following example installs an assembly with the file name *hello.dll* into the global assembly cache.</span></span>

```console
gacutil -i hello.dll
```

> [!NOTE]
> <span data-ttu-id="72800-121">이전 버전의 .NET Framework에서는 *Shfusion.dll* Windows 셸 확장을 통해 파일 탐색기로 어셈블리를 끌어와서 설치할 수 있었습니다.</span><span class="sxs-lookup"><span data-stu-id="72800-121">In earlier versions of the .NET Framework, the *Shfusion.dll* Windows shell extension let you install assemblies by dragging them to File Explorer.</span></span> <span data-ttu-id="72800-122">.NET Framework 4부터는 *Shfusion.dll*이 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72800-122">Beginning with .NET Framework 4, *Shfusion.dll* is obsolete.</span></span>

## <a name="see-also"></a><span data-ttu-id="72800-123">참고 항목</span><span class="sxs-lookup"><span data-stu-id="72800-123">See also</span></span>

- [<span data-ttu-id="72800-124">어셈블리 및 글로벌 어셈블리 캐시 작업</span><span class="sxs-lookup"><span data-stu-id="72800-124">Working with assemblies and the global assembly cache</span></span>](working-with-assemblies-and-the-gac.md)
- [<span data-ttu-id="72800-125">방법: 글로벌 어셈블리 캐시에서 어셈블리 제거</span><span class="sxs-lookup"><span data-stu-id="72800-125">How to: Remove an assembly from the global assembly cache</span></span>](how-to-remove-an-assembly-from-the-gac.md)
- [<span data-ttu-id="72800-126">Gacutil.exe(글로벌 어셈블리 캐시 도구)</span><span class="sxs-lookup"><span data-stu-id="72800-126">Gacutil.exe (Global assembly cache tool)</span></span>](../tools/gacutil-exe-gac-tool.md)
- [<span data-ttu-id="72800-127">방법: 강력한 이름으로 어셈블리 서명</span><span class="sxs-lookup"><span data-stu-id="72800-127">How to: Sign an assembly with a strong name</span></span>](how-to-sign-an-assembly-with-a-strong-name.md)
