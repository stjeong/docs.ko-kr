---
title: '방법: 읽기 전용 Freezable의 쓰기 가능한 복사본 가져오기'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- cloning Freezable objects [WPF]
- Freezable objects [WPF], modifiable clones
ms.assetid: d028de61-bbe9-4d62-b656-8fe3b1b2ca24
ms.openlocfilehash: 2853b1e02e1223cbb2b6dff4acbddb0a41d882cb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54629958"
---
# <a name="how-to-obtain-a-writable-copy-of-a-read-only-freezable"></a>방법: 읽기 전용 Freezable의 쓰기 가능한 복사본 가져오기
사용 하는 방법을 보여 주는이 예제는 <xref:System.Windows.Freezable.Clone%2A> 메서드는 읽기 전용의 쓰기 가능한 복사본을 만드는 <xref:System.Windows.Freezable>합니다.  
  
 뒤를 <xref:System.Windows.Freezable> 개체가 표시 된 읽기 전용 ("고정")으로 수정할 수 없습니다. 그러나 사용할 수는 <xref:System.Windows.Freezable.Clone%2A> 고정된 된 개체의 수정 가능한 복제본을 만드는 방법.  
  
## <a name="example"></a>예제  
 다음 예제에서는 고정 된의 수정 가능한 복제본을 <xref:System.Windows.Media.SolidColorBrush> 개체입니다.  
  
 [!code-csharp[freezablesample_procedural#CloneExample](../../../../samples/snippets/csharp/VS_Snippets_Wpf/freezablesample_procedural/CSharp/freezablesample.cs#cloneexample)]
 [!code-vb[freezablesample_procedural#CloneExample](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/freezablesample_procedural/visualbasic/freezablesample.vb#cloneexample)]  
  
 에 대 한 자세한 내용은 <xref:System.Windows.Freezable> 개체를 참조 합니다 [Freezable 개체 개요](../../../../docs/framework/wpf/advanced/freezable-objects-overview.md)합니다.  
  
## <a name="see-also"></a>참고자료
- <xref:System.Windows.Freezable>
- <xref:System.Windows.Freezable.CloneCurrentValue%2A>
- [Freezable 개체 개요](../../../../docs/framework/wpf/advanced/freezable-objects-overview.md)
- [방법 항목](../../../../docs/framework/wpf/advanced/base-elements-how-to-topics.md)
