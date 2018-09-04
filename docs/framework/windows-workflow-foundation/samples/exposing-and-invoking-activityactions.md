---
title: ActivityAction 노출 및 호출
ms.date: 03/30/2017
ms.assetid: 97ce4797-426e-463d-9cc4-1261afad6df4
ms.openlocfilehash: f36d88fc54e5150927113ed8825fbccad84129d4
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43520125"
---
# <a name="exposing-and-invoking-activityactions"></a>ActivityAction 노출 및 호출
이 샘플에서는 <xref:System.Activities.ActivityAction>이 있는 사용자 지정 활동을 개발하는 방법을 보여 줍니다. 또한 <xref:System.Activities.ActivityAction>의 구현을 제공하여 이 활동을 사용하는 방법도 보여 줍니다.  
  
 <xref:System.Activities.ActivityAction> "허점" 특정 시그니처를 사용 하 여 작업 사용자 사용자 지정 동작을 연결할 수 있는 노출 하는 활동 작성자를 허용 합니다. 예를 들어, 합니다 <!--zz <xref:System.Activities.Statements.ForEach>--> `System.Activities.Statements.ForEach` 활동에 (작동 하는 항목의 컬렉션을 통해)는 <xref:System.Activities.ActivityAction> 작업 사용자의 현재 반복 항목에서 작동 하는 동작을 플러그 인할에서 수 있는 합니다.  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>샘플을 설치, 빌드 및 실행하려면  
  
1.  엽니다는 **ActivityAction.sln** 샘플 솔루션 [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]합니다.  
  
2.  솔루션을 빌드하고 실행합니다.  
  
> [!IMPORTANT]
>  컴퓨터에 이 샘플이 이미 설치되어 있을 수도 있습니다. 계속하기 전에 다음(기본) 디렉터리를 확인하세요.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  이 디렉터리가 없으면로 이동 [Windows Communication Foundation (WCF) 및.NET Framework 4 용 Windows WF (Workflow Foundation) 샘플](https://go.microsoft.com/fwlink/?LinkId=150780) 모든 Windows Communication Foundation (WCF)를 다운로드 하 고 [!INCLUDE[wf1](../../../../includes/wf1-md.md)] 샘플. 이 샘플은 다음 디렉터리에 있습니다.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\CustomActivities\Code-Bodied\ActivityAction`