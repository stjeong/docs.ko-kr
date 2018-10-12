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
# <a name="how-to-install-an-assembly-into-the-global-assembly-cache"></a>방법: 전역 어셈블리 캐시에 어셈블리 설치

강력한 이름의 어셈블리를 GAC(전역 어셈블리 캐시)에 설치하는 방법에는 두 가지가 있습니다.

> [!IMPORTANT]
> 강력한 이름의 어셈블리만 GAC에 설치할 수 있습니다. 강력한 이름의 어셈블리를 만드는 방법에 대한 자세한 내용은 [방법: 강력한 이름으로 어셈블리 서명](how-to-sign-an-assembly-with-a-strong-name.md)을 참조하세요.

## <a name="windows-installer"></a>Windows Installer

Windows 설치 엔진인 [Windows Installer](/windows/desktop/Msi/installation-of-assemblies-to-the-global-assembly-cache)는 전역 어셈블리 캐시에 어셈블리를 추가하는 권장 방법입니다. Windows Installer는 전역 어셈블리 캐시의 어셈블리 참조 횟수 및 다른 여러 가지 혜택을 제공합니다. [Visual Studio 2017용 WiX Toolset 확장](https://marketplace.visualstudio.com/items?itemName=RobMensching.WixToolsetVisualStudio2017Extension)을 사용하여 Windows Installer용 설치 관리자 패키지를 만들 수 있습니다.

## <a name="global-assembly-cache-tool"></a>전역 어셈블리 캐시 도구

[전역 어셈블리 캐시 도구(Gacutil.exe)](../tools/gacutil-exe-gac-tool.md)를 사용하여 강력한 이름의 어셈블리를 전역 어셈블리 캐시에 추가하고 전역 어셈블리 캐시의 콘텐츠를 볼 수 있습니다.

   > [!NOTE]
   > Gacutil.exe는 개발 용도로만 사용되며, 전역 어셈블리 캐시에 프로덕션 어셈블리를 설치하는 데 사용할 수 없습니다.

gacutil의 구문은 다음과 같습니다.

```shell
gacutil -i <assembly name>
```

이 명령에서 *assembly name*은 전역 어셈블리 캐시에 설치할 어셈블리의 이름입니다.

다음 예제는 파일 이름이 `hello.dll`인 어셈블리를 전역 어셈블리 캐시에 설치합니다.

```shell
gacutil -i hello.dll
```

> [!NOTE]
> 이전 버전의 .NET Framework에서는 Shfusion.dll Windows 셸 확장을 통해 **파일 탐색기**에서 어셈블리를 끌어 설치할 수 있었습니다. .NET Framework 4부터는 Shfusion.dll이 사용되지 않습니다.

## <a name="see-also"></a>참고 항목

- [어셈블리 및 전역 어셈블리 캐시 사용](working-with-assemblies-and-the-gac.md)
- [방법: 전역 어셈블리 캐시에서 어셈블리 제거](how-to-remove-an-assembly-from-the-gac.md)
- [Gacutil.exe(전역 어셈블리 캐시 도구)](../tools/gacutil-exe-gac-tool.md)
- [방법: 강력한 이름으로 어셈블리 서명](how-to-sign-an-assembly-with-a-strong-name.md)