---
title: ActivityAction 노출 및 호출
ms.date: 03/30/2017
ms.assetid: 97ce4797-426e-463d-9cc4-1261afad6df4
ms.openlocfilehash: 99207c33d82ec9028da2355cc792c366dc5e0cc6
ms.sourcegitcommit: 3ab9254890a52a50762995fa6d7d77a00348db7e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/20/2018
ms.locfileid: "46479756"
---
# <a name="exposing-and-invoking-activityactions"></a>ActivityAction 노출 및 호출
이 샘플에서는 <xref:System.Activities.ActivityAction>이 있는 사용자 지정 활동을 개발하는 방법을 보여 줍니다. 또한 <xref:System.Activities.ActivityAction>의 구현을 제공하여 이 활동을 사용하는 방법도 보여 줍니다.  
  
 <xref:System.Activities.ActivityAction> "허점" 특정 시그니처를 사용 하 여 작업 사용자 사용자 지정 동작을 연결할 수 있는 노출 하는 활동 작성자를 허용 합니다. 예를 들어 항목 컬렉션에 대해 작동하는 <xref:System.Activities.Statements.ForEach%601> 활동에 <xref:System.Activities.ActivityAction>이 있으며 이를 통해 활동 사용자가 현재 반복 항목에 대해 작동하는 동작을 플러그 인할 수 있습니다.  
  
## <a name="to-set-up-build-and-run-the-sample"></a>샘플을 설치, 빌드 및 실행하려면  
  
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