---
title: '연습: 확장 가능한 응용 프로그램 만들기'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- views [.NET Framework], add-in pipeline
- host-side adapters for add-ins [.NET Framework]
- add-in pipeline [.NET Framework], creating
- add-in-side adapter [.NET Framework]
- contracts for add-in pipelines [.NET Framework]
ms.assetid: 694a33c5-a040-450d-aed5-ac49fc88ce61
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 63780583d035d6fab6b3a79424857b82a910ef09
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50183895"
---
# <a name="walkthrough-creating-an-extensible-application"></a>연습: 확장 가능한 응용 프로그램 만들기
이 연습에서는 간단한 계산기 기능을 수행 하는 추가 기능에 대 한 파이프라인을 만드는 방법을 설명 합니다. 실제 시나리오; 보여 주지 않지만 대신, 파이프라인 및 방법으로 추가 기능 서비스를 제공할 수는 호스트의 기본 기능을 보여 줍니다.  
  
 이 연습에서는 다음 작업을 설명합니다.  
  
-   Visual Studio 솔루션을 만드는 중입니다.  
  
-   파이프라인 디렉터리 구조를 만드는 중입니다.  
  
-   계약 및 뷰를 만드는 중입니다.  
  
-   추가 기능 쪽 어댑터를 만드는 중입니다.  
  
-   호스트 쪽 어댑터를 만드는 중입니다.  
  
-   호스트를 만드는 중입니다.  
  
-   추가 기능에서 만드는 중입니다.  
  
-   파이프라인을 배포 합니다.  
  
-   호스트 응용 프로그램을 실행 합니다.  
  
 이 파이프라인만 직렬화 가능 형식 전달 (<xref:System.Double> 고 <xref:System.String>), 호스트와 추가 기능 사이입니다. 복잡 한 데이터 형식의 컬렉션을 전달 하는 방법을 보여 주는 예제를 참조 하세요 [연습: 추가 기능 및 호스트 간의 컬렉션 전달](https://msdn.microsoft.com/library/b532c604-548e-4fab-b11c-377257dd0ee5)합니다.  
  
 이 파이프라인에 대 한 계약의 네 가지 산술 작업 개체 모델을 정의 합니다: 추가, 빼기, 곱하기, 및 분할 합니다. 호스트가 2 + 2와 같은 계산 수식을 사용 하 여 추가 기능에서 제공 하 고 추가 호스트에 결과 반환 합니다.  
  
 버전 2는 계산기 추가 기능에 추가 계산 기능을 제공 하 고 버전 관리를 보여 줍니다. 설명한 것 [연습: 호스트 변경 내용으로 사용 하도록 설정 하면 이전 버전과 호환성](https://msdn.microsoft.com/library/6fa15bb5-8f04-407d-bd7d-675dc043c848)합니다.  
  
## <a name="prerequisites"></a>전제 조건  
 이 연습을 진행하려면 먼저 다음 작업을 수행해야 합니다.  
  
-   Visual Studio.  
  
## <a name="creating-a-visual-studio-solution"></a>Visual Studio 솔루션 만들기  
 파이프라인 세그먼트의 프로젝트를 포함 하도록 Visual Studio에서 솔루션을 사용 합니다.  
  
#### <a name="to-create-the-pipeline-solution"></a>파이프라인 솔루션을 만들려면  
  
1.  Visual Studio에서 명명 된 새 프로젝트를 만듭니다 `Calc1Contract`합니다. 기반으로 합니다 **클래스 라이브러리** 템플릿.  
  
2.  솔루션의 이름을 `CalculatorV1`로 지정합니다.  
  
## <a name="creating-the-pipeline-directory-structure"></a>파이프라인 디렉터리 구조 만들기  
 추가 기능 모델은 지정 된 디렉터리 구조에 배치 될 파이프라인 세그먼트 어셈블리 필요 합니다. 파이프라인 구조에 대 한 자세한 내용은 참조 하세요. [파이프라인 개발 요구 사항](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5)합니다.  
  
#### <a name="to-create-the-pipeline-directory-structure"></a>파이프라인 디렉터리 구조를 만들려면  
  
1.  어디서 나 컴퓨터에 응용 프로그램 폴더를 만듭니다.  
  
2.  해당 폴더에서 다음 구조를 만듭니다.  
  
    ```  
    Pipeline  
      AddIns  
        CalcV1  
        CalcV2  
      AddInSideAdapters  
      AddInViews  
      Contracts  
      HostSideAdapters  
    ```  
  
     파이프라인 폴더 구조에 응용 프로그램 폴더에 배치할 필요는 없습니다. 편의 위해 여기 수행 됩니다. 연습을 적절 한 단계에서 파이프라인 폴더 구조가 다른 위치에 코드를 변경 하는 방법에 설명 합니다. 디렉터리 요구 사항에 파이프라인의 설명을 참조 하세요 [파이프라인 개발 요구 사항](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5)합니다.  
  
    > [!NOTE]
    >  합니다 `CalcV2` 폴더는이 연습에서 사용 되지 않으므로 자리 표시자 [연습: 호스트 변경 내용으로 사용 하도록 설정 하면 이전 버전과 호환성](https://msdn.microsoft.com/library/6fa15bb5-8f04-407d-bd7d-675dc043c848)합니다.  
  
## <a name="creating-the-contract-and-views"></a>계약 및 뷰 만들기  
 이 파이프라인에 대 한 계약 세그먼트를 정의 합니다 `ICalc1Contract` 4 개의 메서드를 정의 하는 인터페이스: `add`를 `subtract`, `multiply`, 및 `divide`합니다.  
  
#### <a name="to-create-the-contract"></a>계약을 만들려면  
  
1.  명명 된 Visual Studio 솔루션에서 `CalculatorV1`엽니다는 `Calc1Contract` 프로젝트.  
  
2.  **솔루션 탐색기**에 다음 어셈블리에 대 한 참조를 추가 합니다 `Calc1Contract` 프로젝트:  
  
     System.AddIn.Contract.dll  
  
     System.AddIn.dll  
  
3.  **솔루션 탐색기**에 새로 추가 되는 기본 클래스를 제외 **클래스 라이브러리** 프로젝트입니다.  
  
4.  **솔루션 탐색기**, 프로젝트에 새 항목 추가 사용 하 여 합니다 **인터페이스** 템플릿. 에 **새 항목 추가** 대화 상자에서 이름 인터페이스 `ICalc1Contract`합니다.  
  
5.  인터페이스 파일에 네임 스페이스 참조를 추가 <xref:System.AddIn.Contract> 고 <xref:System.AddIn.Pipeline>입니다.  
  
6.  다음 코드를 사용 하 여이 계약 세그먼트를 완료 합니다. 이 인터페이스를 포함 해야 하는 참고를 <xref:System.AddIn.Pipeline.AddInContractAttribute> 특성입니다.  
  
     [!code-csharp[AddInP1Contract#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1Contract/cs/ICalc1Contract.cs#1)]
     [!code-vb[AddInP1Contract#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1Contract/vb/ICalc1Contract.vb#1)]  
  
7.  필요에 따라 Visual Studio 솔루션을 빌드하십시오. 최종 절차는 있지만 각 프로시저 각 프로젝트 인지 확인 한 후 빌드 수정 될 때까지 솔루션을 실행할 수 없습니다.  
  
 추가 기능 뷰 및 호스트 보기 때문에 추가 기능에서 일반적으로 동일한 코드를 첫 번째 버전의 추가 기능에서 특히가 동시에 뷰를 쉽게 만들 수 있습니다. 하나의 인수에 따라 다릅니다: 추가 기능 뷰 필요를 <xref:System.AddIn.Pipeline.AddInBaseAttribute> 특성을 추가 기능의 호스트 뷰 특성이 필요 합니다.  
  
#### <a name="to-create-the-add-in-view"></a>추가 기능 뷰를 만들려면  
  
1.  라는 새 프로젝트 추가 `Calc1AddInView` 에 `CalculatorV1` 솔루션입니다. 기반으로 합니다 **클래스 라이브러리** 템플릿.  
  
2.  **솔루션 탐색기**, 탐색기에 대 한 참조를 추가 합니다 `Calc1AddInView` 프로젝트입니다.  
  
3.  **솔루션 탐색기**에 새로 추가 되는 기본 클래스를 제외 **클래스 라이브러리** 프로젝트 및 프로젝트에 새 항목 추가 사용 하 여 합니다 **인터페이스** 템플릿. 에 **새 항목 추가** 대화 상자에서 이름 인터페이스 `ICalculator`합니다.  
  
4.  인터페이스 파일에 네임 스페이스 참조를 추가 <xref:System.AddIn.Pipeline>합니다.  
  
5.  다음 코드를 사용 하 여이 추가 기능 뷰를 완료 합니다. 이 인터페이스를 포함 해야 하는 참고를 <xref:System.AddIn.Pipeline.AddInBaseAttribute> 특성입니다.  
  
     [!code-csharp[AddInP1AddInViews#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1AddInViews/cs/Calc1AddInView.cs#1)]
     [!code-vb[AddInP1AddInViews#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1AddInViews/vb/Calc1AddInView.vb#1)]  
  
6.  필요에 따라 Visual Studio 솔루션을 빌드하십시오.  
  
#### <a name="to-create-the-host-view-of-the-add-in"></a>추가 기능의 호스트 뷰를 만들려면  
  
1.  라는 새 프로젝트 추가 `Calc1HVA` 에 `CalculatorV1` 솔루션입니다. 기반으로 합니다 **클래스 라이브러리** 템플릿.  
  
2.  **솔루션 탐색기**에 새로 추가 되는 기본 클래스를 제외 **클래스 라이브러리** 프로젝트 및 프로젝트에 새 항목 추가 사용 하 여 합니다 **인터페이스** 템플릿. 에 **새 항목 추가** 대화 상자에서 이름 인터페이스 `ICalculator`합니다.  
  
3.  인터페이스 파일에 추가 기능의 호스트 뷰를 완료 하려면 다음 코드를 사용 합니다.  
  
     [!code-csharp[AddInP1HVA#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1HVA/cs/calc1hva.cs#1)]
     [!code-vb[AddInP1HVA#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1HVA/vb/Calc1HVA.vb#1)]  
  
4.  필요에 따라 Visual Studio 솔루션을 빌드하십시오.  
  
## <a name="creating-the-add-in-side-adapter"></a>추가 기능 쪽 어댑터 만들기  
 이 추가 기능 쪽 어댑터 하나 뷰-계약 어댑터 이루어져 있습니다. 이 파이프라인 세그먼트 추가 뷰에서 계약 형식을 변환합니다.  
  
 이 파이프라인에서 추가 기능에서 서비스 호스트를 제공 하 고 형식 호스트에 추가 기능에서 흐름입니다. 형식이 없습니다. 추가 기능에 호스트에서 흐름을 하기 때문에이 파이프라인의 추가 기능 쪽에서 계약-뷰 어댑터를 포함할 필요가 없습니다.  
  
#### <a name="to-create-the-add-in-side-adapter"></a>추가 기능 쪽 어댑터를 만들려면  
  
1.  라는 새 프로젝트 추가 `Calc1AddInSideAdapter` 에 `CalculatorV1` 솔루션입니다. 기반으로 합니다 **클래스 라이브러리** 템플릿.  
  
2.  **솔루션 탐색기**에 다음 어셈블리에 대 한 참조를 추가 합니다 `Calc1AddInSideAdapter` 프로젝트:  
  
     System.AddIn.dll  
  
     System.AddIn.Contract.dll  
  
3.  인접 한 파이프라인 세그먼트에 대 한 프로젝트에 프로젝트 참조를 추가 합니다.  
  
     `Calc1AddInView`  
  
     `Calc1Contract`  
  
4.  각 프로젝트 참조를 선택 및 **속성** 설정 **로컬 복사** 하 **False**합니다. Visual basic에서 사용 하 여는 **참조** 탭 **프로젝트 속성** 설정 하려면 **로컬 복사** 하 **False** 두 프로젝트 참조에 대 한 합니다.  
  
5.  프로젝트의 기본 클래스 이름 바꾸기 `CalculatorViewToContractAddInSideAdapter`합니다.  
  
6.  클래스 파일에서 네임 스페이스 참조를 추가 <xref:System.AddIn.Pipeline>합니다.  
  
7.  클래스 파일에서 인접 한 세그먼트에 대 한 네임 스페이스 참조를 추가 합니다. `CalcAddInViews` 고 `CalculatorContracts`입니다. (이러한 네임 스페이스 참조는 Visual basic에서는 `Calc1AddInView.CalcAddInViews` 및 `Calc1Contract.CalculatorContracts`않으면 Visual Basic 프로젝트에서 기본 네임 스페이스를 해제 했습니다.)  
  
8.  적용 합니다 <xref:System.AddIn.Pipeline.AddInAdapterAttribute> 특성을 `CalculatorViewToContractAddInSideAdapter` 클래스에 추가 기능 쪽 어댑터와 식별 합니다.  
  
9. 확인 합니다 `CalculatorViewToContractAddInSideAdapter` 클래스 상속 <xref:System.AddIn.Pipeline.ContractBase>의 기본 구현을 제공 하는 합니다 <xref:System.AddIn.Contract.IContract> 인터페이스 및 파이프라인에 대 한 계약 인터페이스를 구현 `ICalc1Contract`합니다.  
  
10. 받아들이는 public 생성자를 추가 `ICalculator`private 필드에 캐시를 기본 클래스 생성자를 호출 합니다.  
  
11. 멤버를 구현 하 `ICalc1Contract`, 해당 멤버를 호출 하기만 하면 됩니다는 `ICalculator` 인스턴스 생성자에 전달 되는 결과 반환 합니다. 이 보기를 조정 (`ICalculator`) 계약 (`ICalc1Contract`).  
  
     다음 코드에서는 완성 된 추가 기능 쪽 어댑터를 보여 줍니다.  
  
     [!code-csharp[AddInP1AddInSideAdapters#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1AddInSideAdapters/cs/Calc1ViewToContractAddInSideAdapter.cs#1)]
     [!code-vb[AddInP1AddInSideAdapters#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1AddInSideAdapters/vb/Calc1ViewToContractAddInSideAdapter.vb#1)]  
  
12. 필요에 따라 Visual Studio 솔루션을 빌드하십시오.  
  
## <a name="creating-the-host-side-adapter"></a>호스트 쪽 어댑터 만들기  
 이 호스트 쪽 어댑터가 하나의 계약-뷰 어댑터 이루어져 있습니다. 이 세그먼트에는 추가 기능의 호스트 뷰를 계약을 조정 됩니다.  
  
 이 파이프라인에서 추가 기능에서 서비스를 제공 호스트 및 형식 흐름 호스트에 추가 기능에서. 형식이 없습니다. 추가 기능에 호스트에서 흐름을 하기 때문에 뷰-계약 어댑터를 포함할 필요가 없습니다.  
  
 수명 관리를 구현 하려면 사용을 <xref:System.AddIn.Pipeline.ContractHandle> 계약의 수명 토큰을 연결 하는 개체입니다. 작업 수명 관리를 위해이 핸들에 대 한 참조를 유지 해야 합니다. 토큰이 적용 되 면 더 이상 사용 되지 않으며 가비지 수집에 사용할 수 있도록 하는 경우 개체의 추가 기능 시스템을 삭제할 수 때문에 없는 추가 프로그래밍이 필요 합니다. 자세한 내용은 [수명 관리](https://msdn.microsoft.com/library/57a9c87e-394c-4fef-89f2-aa4223a2aeb5)를 참조하세요.  
  
#### <a name="to-create-the-host-side-adapter"></a>호스트 쪽 어댑터를 만들려면  
  
1.  라는 새 프로젝트 추가 `Calc1HostSideAdapter` 에 `CalculatorV1` 솔루션입니다. 기반으로 합니다 **클래스 라이브러리** 템플릿.  
  
2.  **솔루션 탐색기**에 다음 어셈블리에 대 한 참조를 추가 합니다 `Calc1HostSideAdapter` 프로젝트:  
  
     System.AddIn.dll  
  
     System.AddIn.Contract.dll  
  
3.  인접 한 세그먼트에 대 한 프로젝트에 프로젝트 참조를 추가 합니다.  
  
     `Calc1Contract`  
  
     `Calc1HVA`  
  
4.  각 프로젝트 참조를 선택 및 **속성** 설정 **로컬 복사** 하 **False**합니다. Visual basic에서 사용 하 여는 **참조** 탭 **프로젝트 속성** 설정 하려면 **로컬 복사** 하 **False** 두 프로젝트 참조에 대 한 합니다.  
  
5.  프로젝트의 기본 클래스 이름 바꾸기 `CalculatorContractToViewHostSideAdapter`합니다.  
  
6.  클래스 파일에서 네임 스페이스 참조를 추가 <xref:System.AddIn.Pipeline>합니다.  
  
7.  클래스 파일에서 인접 한 세그먼트에 대 한 네임 스페이스 참조를 추가 합니다. `CalcHVAs` 고 `CalculatorContracts`입니다. (이러한 네임 스페이스 참조는 Visual basic에서는 `Calc1HVA.CalcHVAs` 및 `Calc1Contract.CalculatorContracts`않으면 Visual Basic 프로젝트에서 기본 네임 스페이스를 해제 했습니다.)  
  
8.  적용 합니다 <xref:System.AddIn.Pipeline.HostAdapterAttribute> 특성을 `CalculatorContractToViewHostSideAdapter` 클래스에 호스트 측 어댑터 세그먼트로 식별 합니다.  
  
9. 확인 합니다 `CalculatorContractToViewHostSideAdapter` 추가 기능의 호스트 뷰를 나타내는 인터페이스를 구현 하는 클래스: `Calc1HVAs.ICalculator` (`Calc1HVA.CalcHVAs.ICalculator` Visual basic에서).  
  
10. 파이프라인 계약 형식을 받아들이는 public 생성자를 추가 `ICalc1Contract`합니다. 생성자는 계약에 대 한 참조를 캐시 해야 합니다. 만들기 및 새 캐시도 해야 <xref:System.AddIn.Pipeline.ContractHandle> 추가 기능의 수명을 관리 하는 계약에 대 한 합니다.  
  
    > [!IMPORTANT]
    >  <xref:System.AddIn.Pipeline.ContractHandle> 수명 관리 하는 중요 합니다. 에 대 한 참조를 유지 하지 못하는 경우를 <xref:System.AddIn.Pipeline.ContractHandle> 개체를 가비지 컬렉션 후 회수는 프로그램에서 사용 되지 않는 경우 파이프라인 종료 됩니다. 와 같은 진단 하기 어려운 오류가 발생할 수 있습니다이 <xref:System.AppDomainUnloadedException>합니다. 종료는 파이프라인의 일반 단계 이므로이 조건은 오류로 검색할 수명 관리 코드에 대 한 방법이 있습니다.  
  
11. 멤버를 구현 하 `ICalculator`, 해당 멤버를 호출 하기만 하면 됩니다는 `ICalc1Contract` 인스턴스 생성자에 전달 되는 결과 반환 합니다. 이 적응 계약 (`ICalc1Contract`) 보기로 (`ICalculator`).  
  
     다음 코드에서는 완성 된 호스트 쪽 어댑터를 보여 줍니다.  
  
     [!code-csharp[AddInP1HostSideAdapters#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1HostSideAdapters/cs/Calc1ContractToViewHostSideAdapter.cs#1)]
     [!code-vb[AddInP1HostSideAdapters#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1HostSideAdapters/vb/Calc1ContractToViewHostSideAdapter.vb#1)]  
  
12. 필요에 따라 Visual Studio 솔루션을 빌드하십시오.  
  
## <a name="creating-the-host"></a>호스트 만들기  
 호스트 응용 프로그램 추가 기능에서 추가 기능의 호스트 뷰를 통해 상호 작용합니다. 추가 기능 검색 및 활성화 메서드 제공한 사용 합니다 <xref:System.AddIn.Hosting.AddInStore> 고 <xref:System.AddIn.Hosting.AddInToken> 다음을 수행 하는 클래스:  
  
-   파이프라인 및 추가 정보 캐시를 업데이트 합니다.  
  
-   호스트 뷰 유형의 추가 기능 찾기 `ICalculator`, 지정 된 파이프라인 루트 디렉터리 아래입니다.  
  
-   사용자 지정 하는 추가 기능에서 사용 하 라는 메시지가 표시 합니다.  
  
-   선택한 추가 기능에 지정 된 보안 신뢰 수준으로 새 응용 프로그램 도메인에서 활성화 합니다.  
  
-   사용자 지정 실행 `RunCalculator` 메서드를 추가 기능에 호스트 뷰로 지정 된 대로 추가-메서드를 호출 합니다.  
  
#### <a name="to-create-the-host"></a>호스트를 만들려면  
  
1.  라는 새 프로젝트 추가 `Calc1Host` 에 `CalculatorV1` 솔루션입니다. 기반으로 합니다 **콘솔 응용 프로그램** 템플릿.  
  
2.  **솔루션 탐색기**, 탐색기에 대 한 참조를 추가 합니다 `Calc1Host` 프로젝트입니다.  
  
3.  프로젝트 참조를 추가 합니다 `Calc1HVA` 프로젝트입니다. 프로젝트 참조를 선택 및 **속성** 설정 **로컬 복사** 하 **False**합니다. Visual basic에서 사용 하 여는 **참조** 탭 **프로젝트 속성** 설정 하려면 **로컬 복사** 하 **False**합니다.  
  
4.  클래스 파일 (Visual Basic의 모듈)의 이름을 `MathHost1`입니다.  
  
5.  Visual basic에서 사용 하 여는 **응용 프로그램** 탭의 **프로젝트 속성** 대화 상자를 **시작 개체** 에 **Sub Main**합니다.  
  
6.  클래스 또는 모듈 파일에서 네임 스페이스 참조를 추가 <xref:System.AddIn.Hosting>합니다.  
  
7.  클래스 또는 모듈 파일에서의 추가 기능 호스트 뷰에 대 한 네임 스페이스 참조를 추가 합니다. `CalcHVAs`합니다. (Visual Basic에서이 네임 스페이스 참조는 `Calc1HVA.CalcHVAs`않으면 Visual Basic 프로젝트에서 기본 네임 스페이스를 해제 했습니다.)  
  
8.  **솔루션 탐색기**, 솔루션을 선택 및 합니다 **프로젝트** 메뉴 **속성**합니다. 에 **솔루션 속성 페이지** 대화 상자에서를 **단일 시작 프로젝트** 이 호스트 응용 프로그램 프로젝트를 합니다.  
  
9. 클래스 또는 모듈 파일에서 사용 된 <xref:System.AddIn.Hosting.AddInStore.Update%2A?displayProperty=nameWithType> 캐시를 업데이트 하는 방법입니다. 사용 된 <xref:System.AddIn.Hosting.AddInStore.FindAddIn%2A?displayProperty=nameWithType> 토큰의 컬렉션을 가져와서 사용 하는 메서드는 <xref:System.AddIn.Hosting.AddInToken.Activate%2A?displayProperty=nameWithType> 추가 기능을 활성화 하는 방법.  
  
     다음 코드에서는 완성 된 호스트 응용 프로그램을 보여 줍니다.  
  
     [!code-csharp[AddInP1Host#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1Host/cs/MathHost1.cs#1)]
     [!code-vb[AddInP1Host#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1Host/vb/MathHost1.vb#1)]  
  
    > [!NOTE]
    >  이 코드는 파이프라인 폴더 구조가 응용 프로그램 폴더에 있는지를 가정 합니다. 에 있는 경우 다른 위치를 설정 하는 코드 줄을 변경 합니다 `addInRoot` 변수 변수의 파이프라인 디렉터리 구조에 대 한 경로 포함 되도록 합니다.  
  
     코드를 사용 하는 `ChooseCalculator` 토큰을 나열 하 고 추가 기능을 선택 하 라는 메시지가 메서드. `RunCalculator` 메서드 간단한 수학 식에 대 한 라는 메시지를 사용 하 여 식을 구문 분석 된 `Parser` 클래스 및 추가 기능에서 반환 하는 결과 표시 합니다.  
  
10. 필요에 따라 Visual Studio 솔루션을 빌드하십시오.  
  
## <a name="creating-the-add-in"></a>추가 기능 만들기  
 추가 기능에서 추가 기능 뷰 지정한 메서드를 구현 합니다. 이 추가 기능에서 구현 된 `Add`, `Subtract`, `Multiply`, 및 `Divide` 작업과 호스트에 결과 반환 합니다.  
  
#### <a name="to-create-the-add-in"></a>추가 기능을 만드는  
  
1.  라는 새 프로젝트 추가 `AddInCalcV1` 에 `CalculatorV1` 솔루션입니다. 기반으로 합니다 **클래스 라이브러리** 템플릿.  
  
2.  **솔루션 탐색기**, 프로젝트 탐색기에 대 한 참조를 추가 합니다.  
  
3.  프로젝트 참조를 추가 합니다 `Calc1AddInView` 프로젝트입니다. 프로젝트 참조를 선택 및 **속성**설정 **로컬 복사** 하 **False**합니다. Visual basic에서 사용 하 여는 **참조** 탭의 **프로젝트 속성** 설정 하려면 **로컬 복사** 에 **False** 프로젝트 참조에 대 한 합니다.  
  
4.  클래스의 이름을 `AddInCalcV1`입니다.  
  
5.  클래스 파일에서 네임 스페이스 참조를 추가 <xref:System.AddIn> , 추가 기능 뷰 세그먼트: `CalcAddInViews` (`Calc1AddInView.CalcAddInViews` Visual basic에서).  
  
6.  적용 합니다 <xref:System.AddIn.AddInAttribute> 특성을 `AddInCalcV1` 클래스에 추가 기능으로 클래스를 식별 합니다.  
  
7.  확인 합니다 `AddInCalcV1` 추가 기능 뷰를 나타내는 인터페이스를 구현 하는 클래스: `CalcAddInViews.ICalculator` (`Calc1AddInView.CalcAddInViews.ICalculator` Visual basic에서).  
  
8.  멤버를 구현 `ICalculator` 적절 한 계산의 결과 반환 합니다.  
  
     다음 코드는 완료 된 추가 기능을 보여 줍니다.  
  
     [!code-csharp[AddInP1AddInCalcV1#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1AddInCalcV1/cs/AddInCalcV1.cs#1)]
     [!code-vb[AddInP1AddInCalcV1#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1AddInCalcV1/vb/AddInCalcV1.vb#1)]  
  
9. 필요에 따라 Visual Studio 솔루션을 빌드하십시오.  
  
## <a name="deploying-the-pipeline"></a>파이프라인 배포  
 이제를 빌드하고 파이프라인 디렉터리 구조에 추가 기능 세그먼트를 배포할 준비가 되었습니다.  
  
#### <a name="to-deploy-the-segments-to-the-pipeline"></a>파이프라인 세그먼트를 배포 하려면  
  
1.  솔루션의 각 프로젝트에 대해 사용 하 여 합니다 **빌드** 탭 **프로젝트 속성** (합니다 **컴파일** Visual Basic의 탭)의 값을 설정 하는 **출력 경로**  (합니다 **빌드 출력 경로** Visual basic에서). 응용 프로그램 폴더 이름을 지정할 경우 `MyApp`, 프로젝트는 다음 폴더에 넣는 예를 들어:  
  
    |프로젝트|Path|  
    |-------------|----------|  
    |AddInCalcV1|MyApp\Pipeline\AddIns\CalcV1|  
    |Calc1AddInSideAdapter|MyApp\Pipeline\AddInSideAdapters|  
    |Calc1AddInView|MyApp\Pipeline\AddInViews|  
    |Calc1Contract|MyApp\Pipeline\Contracts|  
    |Calc1Host|MyApp|  
    |Calc1HostSideAdapter|MyApp\Pipeline\HostSideAdapters|  
    |Calc1HVA|MyApp|  
  
    > [!NOTE]
    >  응용 프로그램 폴더 이외의 위치에서 파이프라인 폴더 구조를 결정 하는 경우 그에 따라 표에 표시 된 경로 수정 해야 합니다. 디렉터리 요구 사항에 파이프라인의 설명을 참조 하세요 [파이프라인 개발 요구 사항](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5)합니다.  
  
2.  Visual Studio 솔루션을 빌드합니다.  
  
3.  응용 프로그램 및 파이프라인 디렉터리 어셈블리 올바른 디렉터리에 복사 된 하 고 어셈블리의 추가 복사본이 된 잘못 된 폴더에 설치 되어 있는지 확인 합니다.  
  
    > [!NOTE]
    >  변경 되지 않은 경우 **로컬 복사** 에 **False** 에 대 한 합니다 `Calc1AddInView` 프로젝트에서 참조를 `AddInCalcV1` 프로젝트 로더 컨텍스트 문제 못합니다에서 추가 기능을 찾을.  
  
     배포 파이프라인에 대 한 내용은 [파이프라인 개발 요구 사항](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5)합니다.  
  
## <a name="running-the-host-application"></a>호스트 응용 프로그램 실행  
 이제 호스트를 실행 하 고 추가 기능에서 상호 작용할 준비가 되었습니다.  
  
#### <a name="to-run-the-host-application"></a>호스트 응용 프로그램을 실행 하려면  
  
1.  명령 프롬프트에서 응용 프로그램 디렉터리로 이동 하 고 호스트 응용 프로그램을 실행 `Calc1Host.exe`합니다.  
  
2.  호스트 사용 가능한 추가 기능을 모두 찾습니다 해당 형식의 추가 기능을 선택 하 라는 메시지가 표시 됩니다. 입력 **1** 추가 기능에 사용할 수 있습니다.  
  
3.  와 같은 수식을 계산기에서 입력 **2 + 2**합니다. 숫자 및 연산자 사이 공백이 있어야 합니다.  
  
4.  형식 **종료** 누릅니다 합니다 **Enter** 키 응용 프로그램을 닫습니다.  
  
## <a name="see-also"></a>참고 항목  
- [연습: 호스트 변경으로 이전 버전과 호환성 설정](https://msdn.microsoft.com/library/6fa15bb5-8f04-407d-bd7d-675dc043c848)  
-  [연습: 호스트와 추가 기능 간의 컬렉션 전달](https://msdn.microsoft.com/library/b532c604-548e-4fab-b11c-377257dd0ee5)  
-  [파이프라인 개발 요구 사항](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5)  
-  [계약, 뷰 및 어댑터](https://msdn.microsoft.com/library/a6460173-9507-4b87-8c07-d4ee245d715c)  
-  [파이프라인 개발](../../../docs/framework/add-ins/pipeline-development.md)
