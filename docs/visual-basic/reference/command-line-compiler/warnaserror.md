---
title: -warnaserror (Visual Basic)
ms.date: 03/13/2018
helpviewer_keywords:
- warnaserror compiler option [Visual Basic]
- /warnaserror compiler option [Visual Basic]
- -warnaserror compiler option [Visual Basic]
ms.assetid: 49819f1d-a1bd-4201-affe-5afe6d9712e1
ms.openlocfilehash: 89f6566bd733ff92d464c026102429d3fc5cf0c1
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50047854"
---
# <a name="-warnaserror-visual-basic"></a>-warnaserror (Visual Basic)
컴파일러에서 맨 처음 발견 되는 경고를 오류로 처리 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
-warnaserror[+ | -][:numberList]  
```  
  
## <a name="arguments"></a>인수  
  
|용어|정의|  
|---|---|  
|+ &#124; -|선택 사항입니다. 기본적으로 `-warnaserror-` 은 적용 경고 해도 컴파일러에서 출력 파일을 생성 합니다. 합니다 `-warnaserror` 동일한 옵션으로 `-warnaserror+`, 경고가 오류로 처리 되도록 하면 합니다.|  
|`numberList`|선택 사항입니다. 경고 ID의 쉼표로 구분 된 목록에는 숫자는 `-warnaserror` 옵션은 적용 됩니다. 경고 ID가 없습니다. 지정 된 경우는 `-warnaserror` 옵션은 모든 경고에 적용 됩니다.|  
  
## <a name="remarks"></a>설명  
 `-warnaserror` 옵션 모든 경고를 오류로 처리 합니다. 일반적으로 보고 됩니다. 경고 대신 오류로 보고 되는 모든 메시지입니다. 컴파일러 경고로 동일한 경고를 계속 보고합니다.  
  
 기본적으로 `-warnaserror-` 만 정보를 경고 하면 적용 됩니다. 합니다 `-warnaserror` 동일한 옵션으로 `-warnaserror+`, 경고가 오류로 처리 되도록 하면 합니다.  
  
 특정 경고만 오류로 처리를 하려는 경우 오류로 처리할 경고 번호의 쉼표로 구분 된 목록을 지정할 수 있습니다.  
  
> [!NOTE]
>  `-warnaserror` 옵션에 경고가 표시 되는 방식을 제어 하지 않습니다. 사용 된 [-nowarn](../../../visual-basic/reference/command-line-compiler/nowarn.md) 경고를 사용 하지 않도록 설정 하는 옵션입니다.  
  
|-Warnaserror를 Visual Studio IDE에서 모든 경고를 오류로 처리를 설정 하려면|  
|---|  
|1.  **솔루션 탐색기**에서 프로젝트를 선택합니다. **프로젝트** 메뉴에서 **속성**을 클릭합니다. <br />2.  **컴파일** 탭을 클릭합니다.<br />3.  있는지 확인 합니다 **모든 경고 사용 안 함** 확인 확인란이 선택 되지 않은 합니다.<br />4.  확인 합니다 **모든 경고를 오류로 처리** 확인란 합니다.|  
  
|-Warnaserror 특정 경고 Visual Studio IDE에서 오류를 처리 하도록 설정 하려면|  
|---|  
|1.  **솔루션 탐색기**에서 프로젝트를 선택합니다. **프로젝트** 메뉴에서 **속성**을 클릭합니다.<br />2.  **컴파일** 탭을 클릭합니다.<br />3.  있는지 확인 합니다 **모든 경고 사용 안 함** 확인 확인란이 선택 되지 않은 합니다.<br />4.  있는지 확인 합니다 **모든 경고를 오류로 처리** 확인 확인란이 선택 되지 않은 합니다.<br />5.  선택 **오류** 에서 합니다 **알림** 경고를 오류로 처리 되어야 하는 인접 한 열입니다.|  
  
## <a name="example"></a>예제  
 다음 코드에서는 `In.vb` 를 처음으로 찾은 모든 경고에 대 한 오류를 표시 하도록 컴파일러에 지시 합니다.  
  
```console
vbc -warnaserror in.vb  
```  
  
## <a name="example"></a>예제  
 다음 코드에서는 `T2.vb` 만 사용 하지 않는 로컬 변수 (42024)에 대 한 경고를 오류로 처리 합니다.  
  
```console
vbc -warnaserror:42024 t2.vb  
```  
  
## <a name="see-also"></a>참고 항목  
 [Visual Basic 명령줄 컴파일러](../../../visual-basic/reference/command-line-compiler/index.md)  
 [샘플 컴파일 명령줄](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)
