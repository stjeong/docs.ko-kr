---
title: '방법: 한 번에 여러 개체 검색'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 18aff4d8-bde8-461b-9960-ccabb24e9d22
ms.openlocfilehash: 31091b6634c9d95c008929680620fb66d95d473c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54653790"
---
# <a name="how-to-retrieve-many-objects-at-once"></a>방법: 한 번에 여러 개체 검색
<xref:System.Data.Linq.DataLoadOptions.LoadWith%2A>를 사용하여 한 쿼리에서 여러 개체를 검색할 수 있습니다.  
  
## <a name="example"></a>예제  
 다음 코드에서는 <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A> 메서드를 사용하여 `Customer` 및 `Order` 개체를 모두 검색합니다.  
  
 [!code-csharp[DLinqQueryConcepts#9](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryConcepts/cs/Program.cs#9)]
 [!code-vb[DLinqQueryConcepts#9](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryConcepts/vb/Module1.vb#9)]  
  
## <a name="see-also"></a>참고자료
- [쿼리 개념](../../../../../../docs/framework/data/adonet/sql/linq/query-concepts.md)
