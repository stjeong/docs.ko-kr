---
title: '방법: 복합 형식을 반환하는 쿼리 실행'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: c2209fdb-70ef-4dea-8bb8-097fe96f5563
ms.openlocfilehash: 013f1980d2ea13927871719aeea293cfce38b4d5
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43861896"
---
# <a name="how-to-execute-a-query-that-returns-complex-types"></a>방법: 복합 형식을 반환하는 쿼리 실행
이 항목에서는 복합 형식의 속성이 포함된 엔터티 형식 개체를 반환하는 [!INCLUDE[esql](../../../../../includes/esql-md.md)] 쿼리를 실행하는 방법을 보여 줍니다.  
  
### <a name="to-run-the-code-in-this-example"></a>이 예제의 코드를 실행하려면  
  
1.  추가 합니다 [AdventureWorks Sales 모델](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) 프로젝트에 사용 하도록 프로젝트를 구성 하 고는 [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]합니다. 자세한 내용은 [방법: 엔터티 데이터 모델 마법사를 사용 하 여](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d)입니다.  
  
2.  응용 프로그램의 코드 페이지에서 다음 `using` 문(Visual Basic에서는 `Imports`)을 추가합니다.  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
3.  모델을 표시 하려면.edmx 파일을 두 번 클릭 합니다 [Model 브라우저 창](https://msdn.microsoft.com/library/94e836e8-a5ea-47ff-aa3e-599d8a02ebfd) 엔터티 디자이너입니다. Entity Designer 화면에서 선택 합니다 `Email` 및 `Phone` 의 속성을 `Contact` 엔터티 형식에 다음 마우스 오른쪽 단추로 **새 복합 형식으로 리팩터링**합니다.  
  
4.  선택 된 새 복합 형식이 `Email` 하 고 `Phone` 속성에 추가 됩니다는 **Model 브라우저**합니다. 복합 형식에 기본 이름이 지정 됩니다:으로 형식 이름 바꾸기 `EmailPhone` 에 **속성** 창. 또한 새 `ComplexProperty` 속성이 `Contact` 엔터티 형식에 추가됩니다. 속성의 이름을 `EmailPhoneComplexType.`으로 바꿉니다.  
  
     만들고 복합 형식을 엔터티 데이터 모델 마법사를 사용 하 여 수정 하는 방법에 대 한 정보를 참조 하세요. [방법: 기존 속성을 복합 형식 속성으로 리팩터링](https://msdn.microsoft.com/library/5b2eb3b3-693d-42cb-b43a-405812d677eb) 및 [방법: 만들기 및 복합 형식 수정](https://msdn.microsoft.com/library/afb8e206-0ffe-4597-b6d4-6ab566897e1d).  
  
## <a name="example"></a>예제  
 컬렉션을 반환 하는 쿼리를 실행 하는 다음 예제 `Contact` 개체 및의 두 속성을 표시 합니다 `Contact` 개체: `ContactID` 값과는 `EmailPhoneComplexType` 복합 형식입니다.  
  
 [!code-csharp[DP EntityServices Concepts#ComplexTypeWithEntityCommand](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#complextypewithentitycommand)]
 [!code-vb[DP EntityServices Concepts#ComplexTypeWithEntityCommand](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#complextypewithentitycommand)]
