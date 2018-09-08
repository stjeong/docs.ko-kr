---
title: '방법: Windows Forms에 ActiveX 컨트롤 추가'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls, ActiveX controls
- forms [Windows Forms], adding ActiveX controls
- ActiveX controls [Windows Forms], adding
ms.assetid: 54a61e5b-555e-4887-b41e-6244fed271eb
ms.openlocfilehash: 7d6514c679187e9ec193f6dda8336c8bd56fac81
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44200225"
---
# <a name="how-to-add-activex-controls-to-windows-forms"></a>방법: Windows Forms에 ActiveX 컨트롤 추가
Windows Forms 디자이너는 호스트 Windows Forms 컨트롤을 최적화 하는 동안에 Windows Forms에서 ActiveX 컨트롤을 배치할 수 있습니다.  
  
> [!CAUTION]
>  ActiveX 컨트롤에 추가 되 면 Windows Forms에 대 한 성능 제한이 있습니다.  
  
 ActiveX 컨트롤을 폼에 추가한 해당 도구 상자에 추가 해야 합니다. 자세한 내용은 [사용자 지정 도구 상자 대화 상자, COM 구성 요소](https://msdn.microsoft.com/library/171333f3-f207-4e02-bbdc-17862556212c)합니다.  
  
> [!NOTE]
>  표시되는 대화 상자와 메뉴 명령은 활성 설정이나 버전에 따라 도움말에서 설명하는 것과 다를 수 있습니다. 설정을 변경하려면 **도구** 메뉴에서 **설정 가져오기 및 내보내기** 를 클릭합니다. 자세한 내용은 [Visual Studio IDE 개인 설정](/visualstudio/ide/personalizing-the-visual-studio-ide)을 참조하세요.  
  
### <a name="to-add-an-activex-control-to-your-windows-form"></a>Windows 폼에 ActiveX 컨트롤을 추가 하려면  
  
-   도구 상자 컨트롤을 두 번 클릭 합니다.  
  
     Visual Studio 프로젝트에서 컨트롤에 대 한 모든 참조를 추가합니다. Windows Forms에서 ActiveX 컨트롤을 사용 하 여 때 염두 할 사항에 대 한 자세한 내용은 참조 하세요. [Windows Form에서 ActiveX 컨트롤을 호스팅할 때의 고려 사항](../../../../docs/framework/winforms/controls/considerations-when-hosting-an-activex-control-on-a-windows-form.md)합니다.  
  
    > [!NOTE]
    >  Windows Forms ActiveX 컨트롤 가져오기 (AxImp.exe) ActiveX 동적 링크 라이브러리 가져오기 시 예상 보다 다른 형식의 이벤트 인수를 만듭니다. AxImp.exe에서 만든 인수는 다음과 유사한: `Invoke(object sender, DWebBrowserEvents2_ProgressChangeEvent e)`때 `Invoke(object sender, DWebBrowserEvents2_ProgressChangeEventArgs e)` 예상 됩니다. 주의이 불일치로 해도 코드는 정상적으로 작동 합니다. 자세한 내용은 참조 하세요 [Windows Forms ActiveX 컨트롤 가져오기 (Aximp.exe)](../../../../docs/framework/tools/aximp-exe-windows-forms-activex-control-importer.md)합니다.  
  
## <a name="see-also"></a>참고 항목  
 [Windows Forms 컨트롤](../../../../docs/framework/winforms/controls/index.md)  
 [여러 언어 및 라이브러리에서 사용되는 컨트롤 및 프로그래밍 가능한 개체 비교](https://msdn.microsoft.com/library/021f2a1b-8247-4348-a5ad-e1d9ab23004b)  
 [방법: Windows Forms에 컨트롤 추가](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md)  
 [Windows Forms에서 컨트롤 정렬](../../../../docs/framework/winforms/controls/arranging-controls-on-windows-forms.md)  
 [개별 Windows Forms 컨트롤 레이블 지정 및 바로 가기 제공](../../../../docs/framework/winforms/controls/labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)  
 [Windows Forms에 사용할 수 있는 컨트롤](../../../../docs/framework/winforms/controls/controls-to-use-on-windows-forms.md)  
 [기능별 Windows Forms 컨트롤](../../../../docs/framework/winforms/controls/windows-forms-controls-by-function.md)
