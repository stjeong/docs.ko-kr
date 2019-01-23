---
title: 제네릭 목록으로 시퀀스 변환
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7ab76d93-6898-4e75-b76f-290a66ecead8
ms.openlocfilehash: 326b4360323f306d07a3b47df506c6427a980a32
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54630790"
---
# <a name="convert-a-sequence-to-a-generic-list"></a>제네릭 목록으로 시퀀스 변환
<xref:System.Linq.Enumerable.ToList%2A>를 사용하여 시퀀스에서 제네릭 목록을 만듭니다.  
  
## <a name="example"></a>예제  
 다음 예제에서는 <xref:System.Linq.Enumerable.ToList%2A>를 사용하여 제네릭 <xref:System.Collections.Generic.List%601>에 대한 쿼리를 즉시 평가합니다.  
  
 [!code-csharp[DLinqQueryExamples#45](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#45)]
 [!code-vb[DLinqQueryExamples#45](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#45)]  
  
## <a name="see-also"></a>참고자료
- [쿼리 예제](../../../../../../docs/framework/data/adonet/sql/linq/query-examples.md)
