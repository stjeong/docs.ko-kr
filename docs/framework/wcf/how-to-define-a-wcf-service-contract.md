---
title: '방법: Windows Communication Foundation 서비스 계약 정의'
ms.date: 09/14/2018
helpviewer_keywords:
- service contracts [WCF], defining
dev_langs:
- CSharp
- VB
ms.assetid: 67bf05b7-1d08-4911-83b7-a45d0b036fc3
ms.openlocfilehash: 9f7f696b1f5be2e96c50938f4627271d891deb32
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48582202"
---
# <a name="how-to-define-a-windows-communication-foundation-service-contract"></a>방법: Windows Communication Foundation 서비스 계약 정의
이 기본 Windows Communication Foundation (WCF) 응용 프로그램을 만드는 데 필요한 6 가지 작업 중 첫 번째입니다. 6가지 모든 작업에 대한 개요는 [초보자를 위한 자습서](../../../docs/framework/wcf/getting-started-tutorial.md) 항목을 참조하세요.

 WCF 서비스를 만들 때 첫 번째 작업은 서비스 계약 정의입니다. 서비스 계약은 서비스가 지원하는 작업을 지정합니다. 작업은 웹 서비스 메서드로 간주될 수 있습니다. C++, C# 또는 VB(Visual Basic) 인터페이스를 정의하여 계약을 만듭니다. 인터페이스의 각 메서드는 특정 서비스 작업에 해당합니다. 각 인터페이스에는 <xref:System.ServiceModel.ServiceContractAttribute>가 적용되어야 하고 각 작업에는 <xref:System.ServiceModel.OperationContractAttribute> 특성이 적용되어야 합니다. <xref:System.ServiceModel.ServiceContractAttribute> 특성을 포함하는 인터페이스 내에 있는 메서드에 <xref:System.ServiceModel.OperationContractAttribute> 특성이 없으면 서비스에 의해 해당 메서드가 노출되지 않습니다.

 이 작업에 사용되는 코드는 이 절차 다음에 나오는 예제에 제공되어 있습니다.

## <a name="define-a-service-contract"></a>서비스 계약 정의

1. 프로그램을 마우스 오른쪽 단추로 클릭 하 여 관리자 권한으로 Visual Studio를 엽니다는 **시작** 메뉴에서 **자세한** > **관리자 권한으로 실행**합니다.

2. WCF 서비스 라이브러리 프로젝트를 만듭니다.

   1. **파일** 메뉴에서 **새로 만들기** > **프로젝트**를 선택합니다.

   2. 에 **새 프로젝트** 대화 상자의 왼쪽에서 확장 **Visual C#** 또는 **Visual Basic**를 선택한 후는 **WCF** 범주입니다. 프로젝트 템플릿의 목록 대화 상자 가운데에 표시 됩니다. 선택 **WCF 서비스 라이브러리**합니다.

   3. 입력 `GettingStartedLib` 에 **이름** 텍스트 상자 및 `GettingStarted` 에서 **솔루션 이름** 대화 상자의 맨 아래에 있는 텍스트 상자에 붙여넣습니다.

   > [!NOTE]
   > 표시 되지 않는 경우는 **WCF** 프로젝트 템플릿 범주를 설치 해야 할 수 있습니다 합니다 **Windows Communication Foundation** Visual Studio의 구성 요소입니다. 에 **새 프로젝트** 대화 상자에서 링크를 클릭 **Visual Studio 설치 관리자 열기**합니다. 선택 합니다 **개별 구성 요소** 탭 한 다음 찾아서 선택 **Windows Communication Foundation** 아래 합니다 **개발 작업** 범주입니다. 선택할 **수정** 구성 요소 설치를 시작 합니다.

   Visual Studio는 3 개의 파일이 포함 된 프로젝트를 만듭니다: IService1.cs (또는 IService1.vb), Service1.cs (또는 Service1.vb) 및 App.config입니다. IService1 파일에는 기본 서비스 계약이 포함되어 있습니다. Service1 파일에는 서비스 계약의 기본 구현이 포함되어 있습니다. App.config 파일에는 Visual Studio WCF 서비스 호스트가 포함된 기본 서비스를 로드하는 데 필요한 구성이 포함되어 있습니다. WCF 서비스 호스트 도구에 대 한 자세한 내용은 참조 하세요. [WCF 서비스 호스트 (WcfSvcHost.exe)](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)

3. IService1.cs 또는 IService1.vb 파일을 열고 네임 스페이스 선언을 유지 하는 네임 스페이스 선언 안의 코드를 삭제 합니다. 다음 코드와 같이 네임스페이스 선언 내에 `ICalculator`라는 새 인터페이스를 정의합니다.

    ```csharp
    using System;
    using System.ServiceModel;

    namespace GettingStartedLib
    {
            [ServiceContract(Namespace = "http://Microsoft.ServiceModel.Samples")]
            public interface ICalculator
            {
                [OperationContract]
                double Add(double n1, double n2);
                [OperationContract]
                double Subtract(double n1, double n2);
                [OperationContract]
                double Multiply(double n1, double n2);
                [OperationContract]
                double Divide(double n1, double n2);
            }
    }
    ```

    ```vb
    Imports System.ServiceModel

    Namespace GettingStartedLib

        <ServiceContract(Namespace:="http://Microsoft.ServiceModel.Samples")> _
        Public Interface ICalculator

            <OperationContract()> _
            Function Add(ByVal n1 As Double, ByVal n2 As Double) As Double
            <OperationContract()> _
            Function Subtract(ByVal n1 As Double, ByVal n2 As Double) As Double
            <OperationContract()> _
            Function Multiply(ByVal n1 As Double, ByVal n2 As Double) As Double
            <OperationContract()> _
            Function Divide(ByVal n1 As Double, ByVal n2 As Double) As Double
        End Interface
    End Namespace
    ```

     이 계약은 온라인 계약을 정의합니다. `ICalculator` 인터페이스에는 <xref:System.ServiceModel.ServiceContractAttribute> 특성이 표시되어 있습니다. 이 특성은 계약 이름을 명확히 나타내는 데 사용하는 네임스페이스를 정의합니다. 각 계산기 연산에는 <xref:System.ServiceModel.OperationContractAttribute> 특성이 표시되어 있습니다.

## <a name="next-steps"></a>다음 단계

> [!div class="nextstepaction"]
> [방법: 서비스 계약 구현](../../../docs/framework/wcf/how-to-implement-a-wcf-contract.md)

## <a name="see-also"></a>참고자료

- <xref:System.ServiceModel.ServiceContractAttribute>
- <xref:System.ServiceModel.OperationContractAttribute>
- [방법: 서비스 계약 구현](../../../docs/framework/wcf/how-to-implement-a-wcf-contract.md)
- [시작](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [자체 호스팅](../../../docs/framework/wcf/samples/self-host.md)