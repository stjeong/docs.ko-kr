---
title: 초보자를 위한 자습서 문제 해결
ms.date: 03/30/2017
ms.assetid: 69a21511-0871-4c41-9a53-93110e84d7fd
ms.openlocfilehash: 5b8cd04ef4d98e522e255e1b7529e848351b2e0c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54695662"
---
# <a name="troubleshooting-the-getting-started-tutorial"></a>초보자를 위한 자습서 문제 해결
이 항목에서는 초보자를 위한 자습서를 수행할 때 발생하는 가장 일반적인 문제 및 해결 방법을 보여 줍니다.  
  
**하드 드라이브에서 프로젝트 파일을 찾을 수 없는 경우**

 Visual Studio 프로젝트 파일을 c:\users에 저장\\<user name>\Documents\\< Visual Studio 버전\>\Projects 합니다.  
  
**서비스 응용 프로그램을 실행 하려고 합니다. HTTP URL을 등록 하지 못했습니다 `http://+:8000/ServiceModelSamples/Service/`.** 
 **프로세스에이 네임 스페이스에 액세스 권한이 없습니다.** 

 WCF 서비스를 호스팅하는 프로세스를 관리자 권한으로 실행 되어야 합니다. 서비스를 실행 하는 경우에서 Visual Studio 내에서 실행 해야 Visual Studio를 관리자 권한으로 합니다. 이렇게 하려면 **시작**를 마우스 오른쪽 단추로 클릭 **Visual Studio \< *버전* >**  선택 하 고 **관리자 권한으로 실행**. 콘솔 창에서 명령줄 프롬프트에서 서비스를 실행 하는 경우 비슷한 방식으로 관리자 권한으로 콘솔 창을 시작 해야 합니다. 클릭 **시작**를 마우스 오른쪽 단추로 클릭 **명령 프롬프트** 선택한 **관리자 권한으로 실행**합니다.  
  
**Svcutil.exe 도구를 사용 하려고 합니다. 'svcutil'은 내부 또는 외부 명령, 실행할 수 있는 프로그램 또는 배치 파일이 아닙니다.**

 Svcutil.exe는 시스템 경로에 있어야 합니다. 가장 간단한 해결책은 명령 프롬프트를 사용하는 것입니다. 클릭 **시작**를 선택 **프로그램도**에 **Visual Studio \< *버전*>**,  **Visual Studio Tools**, 및 **Visual Studio 용 개발자 명령 프롬프트**합니다. 이 명령 프롬프트는 Visual Studio의 일부로 제공 되는 모든 도구에 대 한 올바른 위치를 시스템 경로 설정 합니다.  

**Svcutil.exe에서 생성 한 App.config 파일을 찾을 수 없습니다.**

 합니다 **기존 항목 추가** 대화 기본적으로 다음 확장명을 가진 파일만 표시:.cs,.resx,.settings,.xsd,.wsdl 합니다. 모든 파일 형식을 선택 하 여 표시 되도록 지정할 수 있습니다 **모든 파일 (\*.\*)**  의 오른쪽 아래 모서리의 드롭다운 목록 상자에는 **기존 항목 추가** 대화 상자.  


**클라이언트 응용 프로그램을 컴파일: 'CalculatorClient'에 대 한 정의가 없습니다. '\<메서드 이름 >' 및 확장 메서드 '\<메서드 이름 >' 찾을 수 없습니다 'CalculatorClient' 형식의 첫 번째 인수를 허용 (사용 하는 누락 된 지시문 또는 어셈블리 참조?)**  

`ServiceOperationAttribute`로 표시된 메서드만 외부에 노출됩니다. 생략 하는 경우는 `ServiceOperationAttribute` 의 메서드 중 하나에서 특성을 `ICalculator` 인터페이스 특성이 없습니다. 작업을 호출 하는 클라이언트 응용 프로그램을 컴파일 오류 메시지가 표시 합니다.  

**클라이언트 응용 프로그램을 컴파일: 'CalculatorClient'를 찾을 수 없는 형식 또는 네임 스페이스 이름 (사용 하는 누락 된 지시문 또는 어셈블리 참조가?)**

 클라이언트 프로젝트에 Proxy.cs 또는 Proxy.vb 파일을 추가하면 이 오류가 발생합니다.  

**클라이언트를 실행 합니다. 처리되지 않은 예외: System.ServiceModel.EndpointNotFoundException: 에 연결 하지 못했습니다 `http://localhost:8000/ServiceModelSamples/Service/CalculatorService`합니다. TCP 오류 코드 10061: 대상 컴퓨터에서 적극적으로 거부 없음 연결을 설정할 수 없습니다.**

서비스를 실행하지 않고 클라이언트 응용 프로그램을 실행하면 이 오류가 발생합니다.  
  
**처리 되지 않은 예외: System.ServiceModel.Security.SecurityNegotiationException: 사용 하 여 SOAP 보안 협상 `http://localhost:8000/ServiceModelSamples/Service/CalculatorService` 대상에 대 한 `http://localhost:8000/ServiceModelSamples/Service/CalculatorService` 실패**  

이 오류는 도메인에 참가한 컴퓨터가 네트워크에 연결할 수 없는 경우 발생합니다. 컴퓨터를 네트워크에 연결하거나 클라이언트와 서비스 모두에 대해 보안을 해제하십시오. 서비스의 경우에는 WSHttpBinding을 만드는 코드를 다음과 같이 수정합니다.  
  
```csharp
// Step 3 of the hosting procedure: Add a service endpoint  
selfhost.AddServiceEndpoint(typeof(ICalculator), new WSHttpBinding(SecurityMode.None), "CalculatorService");  
```

클라이언트에 대 한 변경 합니다  **\<보안 >** 요소 아래에 있는 합니다  **\<바인딩 >** 다음 요소:  
  
```xml
<security mode="Node" />  
```  

## <a name="see-also"></a>참고자료
- [초보자를 위한 자습서](../../../docs/framework/wcf/getting-started-tutorial.md)
- [WCF 문제 해결 퀵 스타트](../../../docs/framework/wcf/wcf-troubleshooting-quickstart.md)
- [설치 문제 해결](../../../docs/framework/wcf/troubleshooting-setup-issues.md)
