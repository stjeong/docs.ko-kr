---
title: '방법: 비동기 데이터 서비스 쿼리 (WCF Data Services)를 실행 합니다.'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, asynchronous operations
- asynchronous operations [WCF Data Services]
ms.assetid: 902a2dc1-d0e9-4b00-90a8-becc4cb1f6a7
ms.openlocfilehash: afc12fc0965a8f6cffe1f214cae1a6d108c686d9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54621775"
---
# <a name="how-to-execute-asynchronous-data-service-queries-wcf-data-services"></a>방법: 비동기 데이터 서비스 쿼리 (WCF Data Services)를 실행 합니다.
[!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] 클라이언트 라이브러리를 사용하면 쿼리를 실행하고 변경 내용을 저장하는 것과 같은 클라이언트-서버 작업을 비동기식으로 수행할 수 있습니다. 자세한 내용은 [비동기 작업](../../../../docs/framework/data/wcf/asynchronous-operations-wcf-data-services.md)합니다.  
  
> [!NOTE]
>  지정된 스레드에 대해 콜백을 호출해야 하는 응용 프로그램에서는 <xref:System.Data.Services.Client.DataServiceQuery%601.EndExecute%2A> 메서드 실행을 명시적으로 마샬링해야 합니다. 자세한 내용은 [비동기 작업](../../../../docs/framework/data/wcf/asynchronous-operations-wcf-data-services.md)합니다.  
  
 이 항목의 예제에서는 Northwind 샘플 데이터 서비스 및 자동 생성된 클라이언트 데이터 서비스 클래스를 사용합니다. 이 서비스 및 클라이언트 데이터 클래스를 수행할 때 생성 됩니다는 [WCF Data Services 퀵 스타트](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md)합니다.  
  
## <a name="example"></a>예제  
 다음 예제에서는 <xref:System.Data.Services.Client.DataServiceQuery%601.BeginExecute%2A> 메서드 호출을 통해 쿼리를 시작하여 비동기 쿼리를 실행하는 방법을 보여 줍니다. 인라인 대리자는 <xref:System.Data.Services.Client.DataServiceQuery%601.EndExecute%2A> 메서드를 호출하여 쿼리 결과를 표시합니다.  
  
 [!code-csharp[Astoria Northwind Client#ExecuteQueryAsync](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria northwind client/cs/source.cs#executequeryasync)]
 [!code-vb[Astoria Northwind Client#ExecuteQueryAsync](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria northwind client/vb/source.vb#executequeryasync)]  
  
## <a name="see-also"></a>참고자료
- [WCF Data Services 클라이언트 라이브러리](../../../../docs/framework/data/wcf/wcf-data-services-client-library.md)
