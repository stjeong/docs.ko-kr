---
title: 사용자 지정 활동 작성 시작
ms.date: 03/30/2017
ms.assetid: 3902f5fa-8a43-4048-8a6a-6b15472f90f0
ms.openlocfilehash: 4d9c140ca230750ca1119b33252b1edb8796d458
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43405230"
---
# <a name="getting-started-writing-a-custom-activity"></a>사용자 지정 활동 작성 시작
이 샘플에서는 간단한 사용자 지정 활동을 XAML로 정의하는 방법을 보여 줍니다. 활동에는 `Rhyme`이라는 이름이 지정되고 활동의 논리는 세 <xref:System.Activities.Statements.WriteLine> 활동으로 구성된 시퀀스입니다.  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>샘플을 설치, 빌드 및 실행하려면  
  
1.  엽니다는 **Simple.sln** 샘플 솔루션 [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]합니다.  
  
2.  솔루션을 빌드하고 실행합니다.  
  
> [!IMPORTANT]
>  컴퓨터에 이 샘플이 이미 설치되어 있을 수도 있습니다. 계속하기 전에 다음(기본) 디렉터리를 확인하세요.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  이 디렉터리가 없으면로 이동 [Windows Communication Foundation (WCF) 및.NET Framework 4 용 Windows WF (Workflow Foundation) 샘플](https://go.microsoft.com/fwlink/?LinkId=150780) 모든 Windows Communication Foundation (WCF)를 다운로드 하 고 [!INCLUDE[wf1](../../../../includes/wf1-md.md)] 샘플. 이 샘플은 다음 디렉터리에 있습니다.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\CustomActivities\Composite\GettingStarted`