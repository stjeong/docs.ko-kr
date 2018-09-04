---
title: '방법: WPF 응용 프로그램에 시작 화면 추가'
ms.date: 08/18/2018
helpviewer_keywords:
- WPF [WPF], splash screen
- startup window [WPF]
- SplashScreen class [WPF]
- splash screen [WPF]
ms.assetid: d70a25c4-5fb9-4c27-b01d-b1b8ef39b3fd
ms.openlocfilehash: 46efa041736870c5c0f08baa321ef0dc53cacc0d
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43502756"
---
# <a name="how-to-add-a-splash-screen-to-a-wpf-application"></a>방법: WPF 응용 프로그램에 시작 화면 추가

이 항목에서는 시작 창에 추가 하는 방법 또는 *시작 화면*, Windows Presentation Foundation (WPF) 응용 프로그램입니다.

## <a name="to-add-an-existing-image-as-a-splash-screen"></a>시작 화면으로 기존 이미지를 추가 하려면

1.  시작 화면에 사용 하려는 이미지를 찾거나 만듭니다. Windows Imaging 구성 요소 (WIC)에서 지원 되는 모든 이미지 형식을 사용할 수 있습니다. 예를 들어, BMP, GIF, JPEG, PNG 또는 TIFF 형식으로 사용할 수 있습니다.

2.  WPF 응용 프로그램 프로젝트에 이미지 파일을 추가 합니다.

3.  **솔루션 탐색기**, 이미지를 선택 합니다.

4.  속성 창에서 드롭다운 화살표를 클릭 합니다 **빌드 작업** 속성입니다.

5.  선택 **SplashScreen** 드롭 다운 목록에서.

6.  **F5** 키를 눌러 응용 프로그램을 빌드하고 실행합니다.

     시작 화면 이미지 화면 중앙에 나타나고 주 응용 프로그램 창이 나타나면 사라집니다.

## <a name="to-exclude-the-splash-screen-from-build"></a>시작 화면 빌드에서 제외할

1.  **솔루션 탐색기**, 시작 화면 이미지를 선택 합니다.

2.  에 **속성** 창에서 **빌드 작업** 에 **None**합니다.

## <a name="to-remove-the-splash-screen-from-an-application"></a>응용 프로그램에서 시작 화면을 제거 하려면

**솔루션 탐색기**, 시작 화면 이미지를 삭제 합니다.

## <a name="see-also"></a>참고 항목

- <xref:System.Windows.SplashScreen>
- [방법: 프로젝트에 기존 항목 추가](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/9f4t9t92(v=vs.100))
