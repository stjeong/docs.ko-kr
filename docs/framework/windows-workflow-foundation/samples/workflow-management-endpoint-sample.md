---
title: 워크플로 관리 엔드포인트 샘플
ms.date: 03/30/2017
ms.assetid: 3ac6e08f-c43d-4bb7-83c3-e3890a4dac03
ms.openlocfilehash: 3d99cbef20895381f5e40ee939e1d94a409f1391
ms.sourcegitcommit: f513a91160b3fec289dd06646d0d6f81f8fcf910
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46287571"
---
# <a name="workflow-management-endpoint-sample"></a>워크플로 관리 엔드포인트 샘플
이 샘플에서는 워크플로 제어 엔드포인트를 사용하여 로컬 및 원격으로 워크플로를 만들고 실행하는 방법과 제어 엔드포인트를 호스트하고 제어 엔드포인트를 호출하여 워크플로 인스턴스를 만들고 실행하는 클라이언트를 작성하는 방법을 보여 줍니다. 워크플로는 서비스가 아닙니다.  
  
 샘플의 서비스 쪽에서 워크플로가 WorkflowServiceHost로 호스트되고 WorkflowControlEndpoint가 추가되므로 클라이언트는 일시 중단, 시작 등의 제어 작업을 수행할 수 있습니다. 사용자 정의 CreationEndpoint도 추가되어 워크플로를 만들 수 있습니다. 그런 다음 서비스는 이러한 끝점을 사용하여 일시 중단 상태의 워크플로를 시작한 후 워크플로를 다시 시작합니다. 클라이언트는 동일한 작업을 클라이언트 코드에서 수행합니다. 이 대 한 자세한 내용은 인터페이스에 대 한 [워크플로 제어 끝점](../../../../docs/framework/wcf/feature-details/workflow-control-endpoint.md) 고 [방법: IIS에서 서비스가 아닌 워크플로 호스팅](../../../../docs/framework/wcf/feature-details/how-to-host-a-non-service-workflow-in-iis.md)  
  
#### <a name="to-run-the-sample"></a>이 샘플을 실행하려면  
  
1.  관리자 권한으로 [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]을 실행합니다.  
  
2.  [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]에서 ManagementEndpoint.sln 솔루션을 엽니다.  
  
3.  솔루션을 빌드하려면 CTRL + SHIFT + b 또는 선택 **솔루션 빌드** 에서 합니다 **빌드** 메뉴.  
  
4.  ManagementEndpoint.exe 응용 프로그램을 시작합니다.  
  
5.  Client.exe 응용 프로그램을 시작합니다.  
  
> [!IMPORTANT]
>  컴퓨터에 이 샘플이 이미 설치되어 있을 수도 있습니다. 계속하기 전에 다음(기본) 디렉터리를 확인하세요.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  이 디렉터리가 없으면로 이동 [Windows Communication Foundation (WCF) 및.NET Framework 4 용 Windows WF (Workflow Foundation) 샘플](https://go.microsoft.com/fwlink/?LinkId=150780) 모든 Windows Communication Foundation (WCF)를 다운로드 하 고 [!INCLUDE[wf1](../../../../includes/wf1-md.md)] 샘플. 이 샘플은 다음 디렉터리에 있습니다.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Execution\ManagementEndpoint`