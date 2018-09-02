---
title: PrintForm 구성 요소 (Visual Basic)를 참조 하는 응용 프로그램 배포
ms.date: 07/20/2015
helpviewer_keywords:
- PrintForm component [Visual Basic], deploying
ms.assetid: b595ea44-a712-4625-a761-190c64f59bbe
ms.openlocfilehash: 6384ad6e3bf0520362267eddc8f7bbb05b37f283
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43400428"
---
# <a name="deploying-applications-that-reference-the-printform-component-visual-basic"></a>PrintForm 구성 요소 (Visual Basic)를 참조 하는 응용 프로그램 배포
<xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> 구성 요소를 참조하는 응용 프로그램을 배포하려면 대상 컴퓨터에 구성 요소를 설치해야 합니다.  
  
 PowerPack 컨트롤은 더 이상 Visual Studio에 포함 되었지만 이러한에서 다운로드할 수 없습니다 합니다 [다운로드 센터](https://www.microsoft.com/en-us/download/details.aspx?id=25169)합니다.  
  
## <a name="installing-the-printform-as-a-prerequisite"></a>PrintForm을 필수 조건으로 설치  
 응용 프로그램을 성공적으로 배포하려면 응용 프로그램이 참조하는 모든 구성 요소도 배포해야 합니다. 필수 조건 구성 요소를 설치하는 프로세스를 *부트스트래핑*이라고 합니다.  
  
 경우는 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> 구성 요소가 개발 컴퓨터에 설치 되어, Microsoft Visual Basic Power Packs 부트스트래퍼 패키지가 Visual Studio 부트스트래퍼 디렉터리에 추가 됩니다. 이 패키지는 [!INCLUDE[ndptecclick](~/includes/ndptecclick-md.md)] 또는 Windows Installer 배포에 대한 필수 조건을 추가하는 절차를 수행할 때 사용할 수 있습니다.  
  
 기본적으로 부트스트랩된 구성 요소는 설치 패키지와 같은 위치에서 배포됩니다. 또는 사용자가 필요한 경우 다운로드할 수 있는 URL 또는 파일 공유 위치에서 구성 요소를 배포하도록 선택할 수 있습니다.  
  
> [!NOTE]
>  부트스트랩된 구성 요소를 설치하려면 사용자는 컴퓨터에서 관리 권한이나 비슷한 사용자 권한이 필요할 수 있습니다. [!INCLUDE[ndptecclick](~/includes/ndptecclick-md.md)] 응용 프로그램의 경우 이는 응용 프로그램에서 지정된 보안 수준과 관계없이 응용 프로그램을 설치할 관리 권한이 사용자에게 필요함을 의미합니다. 응용 프로그램이 설치되고 나면 사용자는 관리 권한 없이 응용 프로그램을 실행할 수 있습니다.  
  
 설치하는 동안 대상 컴퓨터에 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> 구성 요소가 없을 경우 해당 구성 요소를 설치할지 묻는 메시지가 사용자에게 표시됩니다.  
  
 부트스트래핑 대신 Microsoft Systems Management Server와 같은 전자 소프트웨어 배포 시스템을 사용하여 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> 구성 요소를 미리 배포할 수 있습니다.  
  
## <a name="see-also"></a>참고자료  
 [방법: ClickOnce 응용 프로그램을 사용하여 필수 조건 설치](/visualstudio/deployment/how-to-install-prerequisites-with-a-clickonce-application)  
 [PrintForm 구성 요소](../../../visual-basic/developing-apps/printing/printform-component.md)
