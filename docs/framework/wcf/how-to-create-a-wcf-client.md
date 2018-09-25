---
title: '방법: Windows Communication Foundation 클라이언트 만들기'
ms.date: 09/14/2018
helpviewer_keywords:
- clients [WCF], running
- WCF clients [WCF], running
ms.assetid: a67884cc-1c4b-416b-8c96-5c954099f19f
ms.openlocfilehash: 1eadb5008575a1a53d685db14d68e42d0dce1360
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47070678"
---
# <a name="how-to-create-a-windows-communication-foundation-client"></a>방법: Windows Communication Foundation 클라이언트 만들기

Windows Communication Foundation (WCF) 응용 프로그램을 만드는 데 필요한 6 가지 작업 중 네 번째입니다. 6가지 모든 작업에 대한 개요는 [초보자를 위한 자습서](../../../docs/framework/wcf/getting-started-tutorial.md) 항목을 참조하세요.

이 항목에서는 WCF 서비스에서 메타 데이터를 검색 하 고 서비스에 액세스할 수 있는 WCF 프록시를 만드는 데 사용 하는 방법을 설명 합니다. 사용 하 여이 작업을 완료 합니다 **서비스 참조 추가** Visual Studio에서 제공 하는 기능입니다. 이 도구는 서비스의 MEX 엔드포인트에서 메타데이터를 가져와 사용자가 선택한 언어를 사용하여 클라이언트 프록시에 대한 관리되는 소스 코드 파일을 생성합니다(기본적으로 C#). 클라이언트 프록시를 만드는 것 이외에 해당 도구는 클라이언트에 대한 구성 파일도 만들거나 업데이트합니다. 이 구성 파일을 사용하여 클라이언트 응용 프로그램에서 해당 엔드포인트 중 하나의 서비스에 연결할 수 있습니다.

> [!NOTE]
> 사용할 수도 있습니다는 [ServiceModel Metadata 유틸리티 도구 (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) 도구를 사용 하는 대신 구성과 프록시 클래스 생성 **서비스 참조 추가** Visual Studio에서.

> [!NOTE]
> Visual Studio에서 클래스 라이브러리 프로젝트에서 WCF 서비스를 호출할 때 사용할 수는 **서비스 참조 추가** 프록시 및 관련된 구성 파일을 자동으로 생성 하는 기능입니다. 이 구성 파일은 클래스 라이브러리 프로젝트에서는 사용되지 않습니다. 클래스 라이브러리를 호출 하는 실행 파일에 대 한 app.config 파일에 생성된 된 구성 파일에 설정을 추가 해야 합니다.

클라이언트 응용 프로그램은 생성된 프록시 클래스를 사용하여 서비스와 통신합니다. 이 절차에 설명 되어 [방법: 클라이언트를 사용 하 여](../../../docs/framework/wcf/how-to-use-a-wcf-client.md)입니다.

## <a name="to-create-a-windows-communication-foundation-client"></a>Windows Communication Foundation 클라이언트를 만들려면

1. Visual Studio에서 새 콘솔 응용 프로그램 프로젝트를 만듭니다. Getting Started 솔루션을 마우스 오른쪽 단추로 클릭 **솔루션 탐색기** 선택한 **추가** > **새 프로젝트**합니다. 에 **새 프로젝트 추가** 대화 상자의 왼쪽에 있는 선택에서 **Windows Desktop** 에서 범주 **Visual C#** 또는 **Visual Basic**합니다. 선택 된 **콘솔 앱 (.NET Framework)** 템플릿을 선택한 후 프로젝트 이름을 **GettingStartedClient**합니다.

2. GettingStartedClient 프로젝트에 System.ServiceModel에 대 한 참조를 추가 합니다. 마우스 오른쪽 단추로 클릭 합니다 **참조** GettingStartedClient 프로젝트에서 폴더 **솔루션 탐색기**를 선택한 후 **참조 추가**합니다. 에 **참조 추가** 대화 상자에서 **프레임 워크** 대화 상자의 왼쪽에서 **어셈블리**합니다. 찾기 및 선택 **System.ServiceModel**를 선택한 후 **확인**합니다. 선택 하 여 솔루션을 저장할 **파일** > **모두 저장**합니다.

3. 계산기 서비스에 대 한 서비스 참조를 추가 합니다.

   1. 먼저 GettingStartedHost 콘솔 응용 프로그램을 시작 합니다.

   2. 호스트가 실행 되 면 마우스 오른쪽 단추로 클릭 합니다 **참조** 폴더에서 GettingStartedClient 프로젝트 아래의 **솔루션 탐색기** 선택한 **추가**  >   **서비스 참조**합니다.

   3. 주소 상자에 다음 URL을 입력 합니다 **서비스 참조 추가** 대화 상자: [http://localhost:8000/GettingStartedClient/Service](http://localhost:8000/GettingStartedClient/Service)

   4. 선택할 **이동**합니다.

   CalculatorService에 표시 되는 **Services** 목록 상자입니다. 확장 하 고 서비스에서 구현 되는 서비스 계약을 표시 하는 CalculatorService를 두 번 클릭 합니다. 기본 네임 스페이스를 그대로-선택할 **확인**합니다.

    새 항목이 나타나는 Visual Studio를 사용 하는 서비스에 대 한 참조를 추가 하면 **솔루션 탐색기** 아래의 합니다 **서비스 참조** GettingStartedClient 프로젝트 아래의 폴더입니다. 사용 하는 경우는 [ServiceModel Metadata 유틸리티 도구 (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) 도구, 소스 코드 파일 및 app.config 파일이 생성 됩니다.

    명령줄 도구를 사용할 수도 있습니다 [ServiceModel Metadata 유틸리티 도구 (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) 클라이언트 코드를 만들려면 적절 한 스위치를 사용 하 여 합니다. 다음 예제에서는 서비스에 대해 코드 파일 및 구성 파일을 생성합니다. 첫 번째 예와 VB에서 프록시를 생성 하는 방법 및 두 번째 C#에서 프록시를 생성 하는 방법을 보여 줍니다.

    ```shell
    svcutil.exe /language:vb /out:generatedProxy.vb /config:app.config http://localhost:8000/GettingStartedClient/service
    ```

    ```shell
    svcutil.exe /language:cs /out:generatedProxy.cs /config:app.config http://localhost:8000/GettingStartedClient/service
    ```

## <a name="next-steps"></a>다음 단계

클라이언트 응용 프로그램은 계산기 서비스를 호출 하는 데 사용할 수 있는 프록시를 만들었습니다. 시리즈의 다음 항목으로 진행 합니다.

> [!div class="nextstepaction"]
> [방법: 클라이언트 구성](../../../docs/framework/wcf/how-to-configure-a-basic-wcf-client.md)

## <a name="see-also"></a>참고자료

- [ServiceModel Metadata 유틸리티 도구(Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
- [시작](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [자체 호스팅](../../../docs/framework/wcf/samples/self-host.md)
- [방법: 구성 파일을 사용하여 서비스의 메타데이터 게시](../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)
- [방법: Svcutil.exe를 사용하여 메타데이터 문서 다운로드](../../../docs/framework/wcf/feature-details/how-to-use-svcutil-exe-to-download-metadata-documents.md)
