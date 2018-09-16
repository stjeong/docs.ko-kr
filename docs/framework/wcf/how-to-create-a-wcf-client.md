---
title: '방법: Windows Communication Foundation 클라이언트 만들기'
ms.date: 03/30/2017
helpviewer_keywords:
- clients [WCF], running
- WCF clients [WCF], running
ms.assetid: a67884cc-1c4b-416b-8c96-5c954099f19f
ms.openlocfilehash: e5655a6fdc06e69d801cb38b7ee7412450f0d34c
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45674145"
---
# <a name="how-to-create-a-windows-communication-foundation-client"></a>방법: Windows Communication Foundation 클라이언트 만들기

Windows Communication Foundation (WCF) 응용 프로그램을 만드는 데 필요한 6 가지 작업 중 네 번째입니다. 6가지 모든 작업에 대한 개요는 [초보자를 위한 자습서](../../../docs/framework/wcf/getting-started-tutorial.md) 항목을 참조하세요.

이 항목에서는 WCF 서비스에서 메타 데이터를 검색 하 고 서비스에 액세스할 수 있는 WCF 프록시를 만드는 데 사용 하는 방법을 설명 합니다. 이 작업은 Visual Studio에서 제공하는 서비스 참조 추가 기능을 사용하여 완료합니다. 이 도구는 서비스의 MEX 엔드포인트에서 메타데이터를 가져와 사용자가 선택한 언어를 사용하여 클라이언트 프록시에 대한 관리되는 소스 코드 파일을 생성합니다(기본적으로 C#). 클라이언트 프록시를 만드는 것 이외에 해당 도구는 클라이언트에 대한 구성 파일도 만들거나 업데이트합니다. 이 구성 파일을 사용하여 클라이언트 응용 프로그램에서 해당 엔드포인트 중 하나의 서비스에 연결할 수 있습니다.

> [!NOTE]
> 사용할 수도 있습니다는 [ServiceModel Metadata 유틸리티 도구 (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) Visual Studio 내에서 서비스 참조 추가 사용 하는 대신 구성과 프록시 클래스를 생성 하는 도구입니다.

> [!WARNING]
> 클래스 라이브러리 프로젝트에서 WCF 서비스를 호출할 때 [!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)] 프록시 및 관련된 구성 파일을 자동으로 생성 하는 서비스 참조 추가 기능을 사용할 수 있습니다.  이 구성 파일은 클래스 라이브러리 프로젝트에서는 사용되지 않습니다. 생성된 구성 파일의 설정을 클래스 라이브러리를 호출하는 실행 파일의 app.config 파일에 추가해야 합니다.

 클라이언트 응용 프로그램은 생성된 프록시 클래스를 사용하여 서비스와 통신합니다. 이 절차에 설명 되어 [방법: 클라이언트를 사용 하 여](../../../docs/framework/wcf/how-to-use-a-wcf-client.md)입니다.

## <a name="to-create-a-windows-communication-foundation-client"></a>Windows Communication Foundation 클라이언트를 만들려면

1.  Getting Started 솔루션을 선택 하 고, 마우스 오른쪽 단추로 클릭 하 여 새 콘솔 응용 프로그램 프로젝트를 만듭니다 **추가**하십시오 **새 프로젝트**합니다. 대화 상자의 왼쪽에 있는 **새 프로젝트 추가** 대화 상자에서 **C#** 또는 **VB** 아래의 **Windows**를 선택합니다. 대화 상자 가운데에서 **콘솔 응용 프로그램**을 선택합니다. 프로젝트 이름을 `GettingStartedClient`로 지정합니다.

2.  마우스 오른쪽 단추로 클릭 하 여 GettingStartedClient 프로젝트의 대상 프레임 워크로.NET Framework 4.5로 **GettingStartedClient** 솔루션 탐색기에서 선택 하 고 **속성**합니다. **대상 프레임워크** 드롭다운 목록에서 **.NET Framework 4.5**를 선택합니다. VB 프로젝트는 방법은 약간 다릅니다. GettingStartedClient 프로젝트 속성 대화 상자에서에 대 한 대상 프레임 워크 설정을 클릭 합니다 **컴파일** 화면의 왼쪽에 탭을 클릭 한 다음는 **고급 컴파일 옵션** 대화 상자의 왼쪽 아래 모서리에 있는 단추입니다. 그런 다음, **대상 프레임워크** 드롭다운 상자에서 **.NET Framework 4.5**를 선택합니다.

     대상 프레임 워크를 설정 하면 Visual Studio 2011에서 솔루션 다시 로드 키를 눌러 **확인** 메시지가 표시 되 면 합니다.

3.  GettingStartedClient 프로젝트를 마우스 오른쪽 단추로 클릭 하 여 System.ServiceModel에 대 한 참조를 추가 합니다 **참조** 폴더 선택 솔루션 탐색기에서 GettingStartedClient 프로젝트 아래의 **추가** 참조입니다. **참조 추가** 대화 상자에서 대화 상자 왼쪽의 **프레임워크**를 선택합니다. 검색 어셈블리 텍스트 상자에 `System.ServiceModel`을 입력합니다. 대화 상자 가운데에서 **System.ServiceModel**을 선택하고 **추가** 단추를 클릭한 다음, **닫기** 단추를 클릭합니다. 클릭 하 여 솔루션을 저장 합니다 **모두 저장** 주 메뉴 아래 단추입니다.

4.  다음에 계산기 서비스에 대 한 서비스 참조를 추가할 수 있습니다. 그렇게 하기 전에 GettingStartedHost 콘솔 응용 프로그램을 실행해야 합니다. 호스트가 실행 되 면 마우스 오른쪽 단추로 클릭 합니다 **참조** 폴더에서 GettingStartedClient 프로젝트 아래의 **솔루션 탐색기** 선택한 **추가**  >   **서비스 참조**합니다. 주소 상자에 다음 URL 입력 합니다 **서비스 참조 추가** 대화: [ http://localhost:8000/GettingStartedClient/Service ](http://localhost:8000/GettingStartedClient/Service) 클릭 합니다 **이동** 단추. 그런 다음 서비스 목록 상자에 CalculatorService는 표시 합니다. CalculatorService를 두 번 클릭 하 고 확장 하 고 서비스에서 구현 되는 서비스 계약을 보여 줍니다. 클릭 하 고 기본 네임 스페이스를 유지 합니다 **확인** 단추입니다.

     Visual Studio를 사용하여 서비스에 대한 참조를 추가하면 솔루션 탐색기에서 GettingStartedClient 프로젝트 아래의 Service References 폴더에 새 항목이 나타납니다.  사용 하는 경우는 [ServiceModel Metadata 유틸리티 도구 (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) 도구 소스 코드 파일과 app.config 파일이 생성 됩니다.

     명령줄 도구를 사용할 수도 있습니다 [ServiceModel Metadata 유틸리티 도구 (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) 클라이언트 코드를 만들려면 적절 한 스위치를 사용 하 여 합니다. 다음 예제에서는 서비스에 대해 코드 파일 및 구성 파일을 생성합니다. 첫 번째 예제는 VB에서 프록시를 생성하는 방법을 보여 주고 두 번째 예제는 C#에서 프록시를 생성하는 방법을 보여 줍니다.

    ```
    svcutil.exe /language:vb /out:generatedProxy.vb /config:app.config http://localhost:8000/GettingStartedClient/service
    ```

    ```csharp
    svcutil.exe /language:cs /out:generatedProxy.cs /config:app.config http://localhost:8000/GettingStartedClient/service
    ```

 클라이언트 응용 프로그램이 계산기 서비스를 호출하기 위해 사용할 프록시가 만들어졌습니다. 시리즈의 다음 항목으로 이동: [방법: 클라이언트 구성](../../../docs/framework/wcf/how-to-configure-a-basic-wcf-client.md)

## <a name="see-also"></a>참고 항목

- [ServiceModel Metadata 유틸리티 도구(Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
- [시작](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [자체 호스팅](../../../docs/framework/wcf/samples/self-host.md)
- [방법: 구성 파일을 사용하여 서비스의 메타데이터 게시](../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)
- [방법: Svcutil.exe를 사용하여 메타데이터 문서 다운로드](../../../docs/framework/wcf/feature-details/how-to-use-svcutil-exe-to-download-metadata-documents.md)
