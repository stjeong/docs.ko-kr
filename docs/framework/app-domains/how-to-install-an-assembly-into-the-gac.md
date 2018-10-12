---
title: GAC에 어셈블리 설치
ms.date: 09/20/2018
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
ms.openlocfilehash: d365ac77fe6cd7fc4fca36705729ec12b06d6830
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/23/2018
ms.locfileid: "46584583"
---
# <a name="how-to-install-an-assembly-into-the-global-assembly-cache"></a><span data-ttu-id="dca06-102">방법: 전역 어셈블리 캐시에 어셈블리 설치</span><span class="sxs-lookup"><span data-stu-id="dca06-102">How to: Install an assembly into the global assembly cache</span></span>

<span data-ttu-id="dca06-103">강력한 이름의 어셈블리를 GAC(전역 어셈블리 캐시)에 설치하는 방법에는 두 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dca06-103">There are two ways to install a strong-named assembly into the global assembly cache (GAC).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dca06-104">강력한 이름의 어셈블리만 GAC에 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dca06-104">Only strong-named assemblies can be installed into the GAC.</span></span> <span data-ttu-id="dca06-105">강력한 이름의 어셈블리를 만드는 방법에 대한 자세한 내용은 [방법: 강력한 이름으로 어셈블리 서명](how-to-sign-an-assembly-with-a-strong-name.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dca06-105">For information about how to create a strong-named assembly, see [How to: Sign an Assembly with a Strong Name](how-to-sign-an-assembly-with-a-strong-name.md).</span></span>

## <a name="windows-installer"></a><span data-ttu-id="dca06-106">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="dca06-106">Windows Installer</span></span>

<span data-ttu-id="dca06-107">Windows 설치 엔진인 [Windows Installer](/windows/desktop/Msi/installation-of-assemblies-to-the-global-assembly-cache)는 전역 어셈블리 캐시에 어셈블리를 추가하는 권장 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="dca06-107">[Windows Installer](/windows/desktop/Msi/installation-of-assemblies-to-the-global-assembly-cache), the Windows installation engine, is the recommended way to add assemblies to the global assembly cache.</span></span> <span data-ttu-id="dca06-108">Windows Installer는 전역 어셈블리 캐시의 어셈블리 참조 횟수 및 다른 여러 가지 혜택을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="dca06-108">Windows Installer provides reference counting of assemblies in the global assembly cache and other benefits.</span></span> <span data-ttu-id="dca06-109">[Visual Studio 2017용 WiX Toolset 확장](https://marketplace.visualstudio.com/items?itemName=RobMensching.WixToolsetVisualStudio2017Extension)을 사용하여 Windows Installer용 설치 관리자 패키지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dca06-109">You can use the [WiX Toolset extension for Visual Studio 2017](https://marketplace.visualstudio.com/items?itemName=RobMensching.WixToolsetVisualStudio2017Extension) to create an installer package for Windows Installer.</span></span>

## <a name="global-assembly-cache-tool"></a><span data-ttu-id="dca06-110">전역 어셈블리 캐시 도구</span><span class="sxs-lookup"><span data-stu-id="dca06-110">Global assembly cache tool</span></span>

<span data-ttu-id="dca06-111">[전역 어셈블리 캐시 도구(Gacutil.exe)](../tools/gacutil-exe-gac-tool.md)를 사용하여 강력한 이름의 어셈블리를 전역 어셈블리 캐시에 추가하고 전역 어셈블리 캐시의 콘텐츠를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dca06-111">You can use the [Global assembly cache tool (gacutil.exe)](../tools/gacutil-exe-gac-tool.md) to add strong-named assemblies to the global assembly cache and to view the contents of the global assembly cache.</span></span>

   > [!NOTE]
   > <span data-ttu-id="dca06-112">Gacutil.exe는 개발 용도로만 사용되며, 전역 어셈블리 캐시에 프로덕션 어셈블리를 설치하는 데 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dca06-112">Gacutil.exe is only for development purposes and should not be used to install production assemblies into the global assembly cache.</span></span>

<span data-ttu-id="dca06-113">gacutil의 구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dca06-113">The syntax for gacutil is as follows:</span></span>

```shell
gacutil -i <assembly name>
```

<span data-ttu-id="dca06-114">이 명령에서 *assembly name*은 전역 어셈블리 캐시에 설치할 어셈블리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dca06-114">In this command, *assembly name* is the name of the assembly to install in the global assembly cache.</span></span>

<span data-ttu-id="dca06-115">다음 예제는 파일 이름이 `hello.dll`인 어셈블리를 전역 어셈블리 캐시에 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="dca06-115">The following example installs an assembly with the file name `hello.dll` into the global assembly cache.</span></span>

```shell
gacutil -i hello.dll
```

> [!NOTE]
> <span data-ttu-id="dca06-116">이전 버전의 .NET Framework에서는 Shfusion.dll Windows 셸 확장을 통해 **파일 탐색기**에서 어셈블리를 끌어 설치할 수 있었습니다.</span><span class="sxs-lookup"><span data-stu-id="dca06-116">In earlier versions of the .NET Framework, the Shfusion.dll Windows shell extension enabled you to install assemblies by dragging them in **File Explorer**.</span></span> <span data-ttu-id="dca06-117">.NET Framework 4부터는 Shfusion.dll이 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dca06-117">Beginning with the .NET Framework 4, Shfusion.dll is obsolete.</span></span>

## <a name="see-also"></a><span data-ttu-id="dca06-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="dca06-118">See also</span></span>

- [<span data-ttu-id="dca06-119">어셈블리 및 전역 어셈블리 캐시 사용</span><span class="sxs-lookup"><span data-stu-id="dca06-119">Working with Assemblies and the Global Assembly Cache</span></span>](working-with-assemblies-and-the-gac.md)
- [<span data-ttu-id="dca06-120">방법: 전역 어셈블리 캐시에서 어셈블리 제거</span><span class="sxs-lookup"><span data-stu-id="dca06-120">How to: Remove an Assembly from the Global Assembly Cache</span></span>](how-to-remove-an-assembly-from-the-gac.md)
- [<span data-ttu-id="dca06-121">Gacutil.exe(전역 어셈블리 캐시 도구)</span><span class="sxs-lookup"><span data-stu-id="dca06-121">Gacutil.exe (Global Assembly Cache Tool)</span></span>](../tools/gacutil-exe-gac-tool.md)
- [<span data-ttu-id="dca06-122">방법: 강력한 이름으로 어셈블리 서명</span><span class="sxs-lookup"><span data-stu-id="dca06-122">How to: Sign an Assembly with a Strong Name</span></span>](how-to-sign-an-assembly-with-a-strong-name.md)