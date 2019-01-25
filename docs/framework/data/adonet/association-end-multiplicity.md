---
title: 연결 End 복합성
ms.date: 03/30/2017
ms.assetid: 340926ee-aefb-4bef-92cc-453e5251fd03
ms.openlocfilehash: 6d1b31c5b5ead701fbe808b91d7191fb84dc86c8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54502639"
---
# <a name="association-end-multiplicity"></a>연결 End 복합성
*연결 end 복합성* 개수를 정의 [엔터티 형식의](../../../../docs/framework/data/adonet/entity-type.md) 한쪽 끝에 있을 수 있는 인스턴스를 [연결](../../../../docs/framework/data/adonet/association-type.md)합니다.  
  
 연결 End 복합성은 다음 값 중 하나일 수 있습니다.  
  
-   일 (1): 연결 end에는 정확히 하나의 엔터티 형식 인스턴스가 있음을 나타냅니다.  
  
-   0 또는 1 (0..1): 연결 end에 0 개 이상의 엔터티 형식 인스턴스가 있음을 나타냅니다.  
  
-   많은 (*): 연결 end에 0, 1 또는 더 많은 엔터티 형식 인스턴스가 있음을 나타냅니다.  
  
 연결은 대체로 연결 End 복합성 특성을 사용합니다. 예를 들어, 연결의 End 복합성이 한 개(1) 및 다수(*)이면 해당 연결을 일대다 연결이라고 합니다. 다음 예에서 `PublishedBy` 연결은 일대다 연결입니다. 즉, 한 명의 발행자가 많은 책을 출판하고 책 하나는 한 명의 발행자에 의해 출판됩니다. `WrittenBy` 연결은 다대다 연결입니다. 한 권의 책에 저자가 여러 명일 수 있고 한 명의 저자가 여러 책을 쓸 수도 있습니다.  
  
## <a name="example"></a>예제  
 다음 다이어그램에서는 두 연결 `PublishedBy` 및 `WrittenBy`의 개념적 모델을 보여 줍니다. `PublishedBy` 연결의 연결 End는 `Book` 및 `Publisher` 엔터티 형식입니다. `Publisher` 끝의 복합성은 한 개(1)이고 `Book` 끝의 복합성은 다수(*)입니다.  
  
 ![예제 모델이](../../../../docs/framework/data/adonet/media/examplemodel.gif "ExampleModel")  
  
 ADO.NET Entity Framework 개념적 스키마 정의 언어를 호출 하는 도메인 특정 언어 (DSL)를 사용 하 여 ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) 개념적 모델을 정의 합니다. 다음 CSDL에서는 위의 다이어그램에 표시된 `PublishedBy` 연결을 정의합니다.  
  
 [!code-xml[EDM_Example_Model#AssociationExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#associationexample)]  
  
## <a name="see-also"></a>참고자료
- [엔터티 데이터 모델의 주요 개념](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [엔터티 데이터 모델](../../../../docs/framework/data/adonet/entity-data-model.md)
