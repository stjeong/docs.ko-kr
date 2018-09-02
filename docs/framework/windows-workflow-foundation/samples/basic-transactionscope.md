---
title: 기본 TransactionScope
ms.date: 03/30/2017
ms.assetid: 1e22b76a-76de-43b4-9be7-7a86ed3d5a44
ms.openlocfilehash: b3c673040d40ca91d8ab4a79e847d61e6f507ed1
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43415425"
---
# <a name="basic-transactionscope"></a>기본 TransactionScope
이 샘플은 <xref:System.Activities.Statements.TransactionScope> 인스턴스를 중첩시키는 방법을 보여 주는 네 개의 시나리오로 구성되어 있습니다. 첫 번째 시나리오에서는 작성자가 생성에 대해 알지 못하는 타사 활동을 중첩시키는 방법을 보여 줍니다. 두 번째와 세 번째 시나리오에서는 제한 시간을 적용하는 방법을 보여 주고 마지막 시나리오에서는 <xref:System.Activities.Statements.TransactionScope.AbortInstanceOnTransactionFailure%2A> 설정을 보여 줍니다.  
  
## <a name="nesting-of-transactionscopeactivity"></a>TransactionScopeActivity 중첩  
 첫 번째 시나리오의 워크플로는 두 <xref:System.Activities.Statements.WriteLine> 활동과 한 <xref:System.Activities.Statements.TransactionScope> 활동의 시퀀스로 구성되어 있습니다. <xref:System.Activities.Statements.TransactionScope>의 본문은 둘 이상의 <xref:System.Activities.Statements.WriteLine> 활동, 트랜잭션의 로컬 식별자를 출력하는 사용자 지정 활동 및 타사 활동으로 이루어진 시퀀스입니다. 타사 활동 `TransactionScopeTest`에는 <xref:System.Activities.Statements.TransactionScope>가 포함되어 있지만 워크플로 작성자는 이를 알 수 없습니다. 이 시나리오에서는 <xref:System.Activities.Statements.TransactionScope> 활동이 중첩될 수 있음을 보여 줍니다.  
  
## <a name="time-outs"></a>제한 시간  
 두 번째 시나리오의 워크플로는 첫 번째 시나리오와 거의 동일하지만 `TransactionScopeTest`가 <xref:System.Activities.Statements.TransactionScope>로 대체되었다는 차이점이 있습니다. <xref:System.Activities.Statements.TransactionScope>의 본문은 5초의 지연 시간을 나타내며 트랜잭션 제한 시간은 2초로 설정됩니다. 외부 <xref:System.Activities.Statements.TransactionScope>의 제한 시간은 10초로 설정됩니다. 범위의 최소 제한 시간이 적용되어 트랜잭션이 시간 초과됩니다.  
  
 세 번째 시나리오의 워크플로는 두 번째 시나리오와 거의 동일하지만 지연 활동이 내부 <xref:System.Activities.Statements.TransactionScope>에서 외부 <xref:System.Activities.Statements.TransactionScope>의 본문에 해당하는 시퀀스에서 해당 위치 바로 다음의 위치로 이동되었다는 차이점이 있습니다. 트랜잭션은 여전히 제한 시간이 적용되지만 내부 <xref:System.Activities.Statements.TransactionScope>의 제한 시간 2초는 더 이상 적용되지 않습니다. 대신 외부 <xref:System.Activities.Statements.TransactionScope> 제한 시간이 초과되는 10초 후에 트랜잭션이 시간 초과됩니다.  
  
## <a name="aborting-on-transaction-failure"></a>트랜잭션 실패 시 중단  
 이 워크플로는 세 번째 시나리오와 유사하지만 <xref:System.Activities.Statements.TransactionScope.AbortInstanceOnTransactionFailure%2A> 속성에 의해 제한 시간이 대체되었다는 차이점이 있습니다. 모든 내부 자식 항목의 플래그(설정된 경우)는 외부 <xref:System.Activities.Statements.TransactionScope>와 일치해야 합니다. 이 시나리오에서는 그렇지 않으므로 워크플로가 열릴 때 예외가 throw됩니다.  
  
#### <a name="to-run-the-sample"></a>이 샘플을 실행하려면  
  
1.  [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]에서 BasicTransactionScopeSample.sln 솔루션을 엽니다.  
  
2.  솔루션을 빌드하려면 CTRL + SHIFT + b 또는 선택 **솔루션 빌드** 에서 합니다 **빌드** 메뉴.  
  
3.  빌드가 성공 되 면 f5 키를 누르거나 **디버깅 시작** 에서 합니다 **디버그** 메뉴. 또는 CTRL + F5 키를 눌러 수도 있고 선택할 **디버깅 하지 않고 시작** 에서 **디버그** 메뉴 디버깅 하지 않고 실행 합니다.  
  
> [!IMPORTANT]
>  컴퓨터에 이 샘플이 이미 설치되어 있을 수도 있습니다. 계속하기 전에 다음(기본) 디렉터리를 확인하세요.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  이 디렉터리가 없으면로 이동 [Windows Communication Foundation (WCF) 및.NET Framework 4 용 Windows WF (Workflow Foundation) 샘플](https://go.microsoft.com/fwlink/?LinkId=150780) 모든 Windows Communication Foundation (WCF)를 다운로드 하 고 [!INCLUDE[wf1](../../../../includes/wf1-md.md)] 샘플. 이 샘플은 다음 디렉터리에 있습니다.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Transactions\BasicTransactionScope`