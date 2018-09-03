---
title: IfElse With Rules
ms.date: 03/30/2017
ms.assetid: c4ad9bb2-9037-413a-8b14-59ed7b927a9e
ms.openlocfilehash: 31906f04149a0ca7659201965ca565c7fa2af305
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43483008"
---
# <a name="ifelse-with-rules"></a>IfElse With Rules
이 샘플에서는 <xref:System.Workflow.Activities.IfElseActivity> 활동에 규칙 조건을 사용하는 방법을 보여 줍니다.  
  
 이 샘플은 호스트로부터 `OrderValue` 매개 변수를 전달합니다. 이 매개 변수의 값은 <xref:System.Workflow.Activities.IfElseActivity> 활동의 첫 번째 분기에 대한 규칙 조건에 사용됩니다. 값이 10,000 보다 작으면, 첫 번째 분기가 실행 되며, 및 <xref:System.Workflow.Activities.CodeActivity> 첫 번째 분기에서 활동 출력 **관리자 승인 받기** 콘솔. 값이 10,000 보다 크면 합니다 <xref:System.Workflow.Activities.CodeActivity> 두 번째 분기의 활동이 실행 되 고 인쇄 **VP 승인**합니다.  
  
### <a name="to-build-the-sample"></a>이 샘플을 빌드하려면  
  
1.  [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]에서 솔루션을 엽니다.  
  
2.  Ctrl+Shift+B를 눌러 솔루션을 빌드합니다.  
  
3.  Ctrl+F5를 눌러 디버깅 없이 솔루션을 실행합니다.  
  
### <a name="to-run-the-sample"></a>이 샘플을 실행하려면  
  
-   SDK 명령 프롬프트 창에서 샘플의 주 폴더 아래에 있는 IfElseWithRules\bin\debug 폴더 또는 IfElseWithRules\bin 폴더(Visual Basic 버전 샘플의 경우)의 .exe 파일을 실행합니다.  
  
> [!IMPORTANT]
>  컴퓨터에 이 샘플이 이미 설치되어 있을 수도 있습니다. 계속하기 전에 다음(기본) 디렉터리를 확인하세요.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  이 디렉터리가 없으면로 이동 [Windows Communication Foundation (WCF) 및.NET Framework 4 용 Windows WF (Workflow Foundation) 샘플](https://go.microsoft.com/fwlink/?LinkId=150780) 모든 Windows Communication Foundation (WCF)를 다운로드 하 고 [!INCLUDE[wf1](../../../../includes/wf1-md.md)] 샘플. 이 샘플은 다음 디렉터리에 있습니다.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Rules\IfElseWithRules`  
  
## <a name="see-also"></a>참고 항목  
 <xref:System.Workflow.Activities.Rules>  
 <xref:System.Workflow.Activities.IfElseActivity>  
 <xref:System.Workflow.Activities.CodeActivity>  
 <xref:System.Workflow.Activities.Rules.RuleDefinitions>
