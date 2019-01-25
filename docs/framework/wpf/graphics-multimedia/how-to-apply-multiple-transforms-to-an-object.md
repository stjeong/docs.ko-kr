---
title: '방법: 개체에 다중 변환 적용'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- grouping Transform objects [WPF]
- Transform objects [WPF], grouping
- graphics [WPF], grouping Transform objects
- TransformGroup [WPF]
ms.assetid: 98cd1921-12bc-4bf5-8193-529228fb7402
ms.openlocfilehash: dc9b7c052d9deb4d1167c813a6ce652c99983a9f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54649455"
---
# <a name="how-to-apply-multiple-transforms-to-an-object"></a><span data-ttu-id="260d5-102">방법: 개체에 다중 변환 적용</span><span class="sxs-lookup"><span data-stu-id="260d5-102">How to: Apply Multiple Transforms to an Object</span></span>
<span data-ttu-id="260d5-103">사용 하는 방법을 보여 주는이 예제는 <xref:System.Windows.Media.TransformGroup> 둘 이상의 그룹에 <xref:System.Windows.Media.Transform> 개체를 단일 복합 <xref:System.Windows.Media.Transform>합니다.</span><span class="sxs-lookup"><span data-stu-id="260d5-103">This example shows how to use a <xref:System.Windows.Media.TransformGroup> to group two or more <xref:System.Windows.Media.Transform> objects into a single composite <xref:System.Windows.Media.Transform>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="260d5-104">예제</span><span class="sxs-lookup"><span data-stu-id="260d5-104">Example</span></span>  
 <span data-ttu-id="260d5-105">다음 예제에서는 <xref:System.Windows.Media.TransformGroup> 적용 하는 <xref:System.Windows.Media.ScaleTransform> 및 <xref:System.Windows.Media.RotateTransform> 에 <xref:System.Windows.Controls.Button>.</span><span class="sxs-lookup"><span data-stu-id="260d5-105">The following example uses a <xref:System.Windows.Media.TransformGroup> to apply a <xref:System.Windows.Media.ScaleTransform> and a <xref:System.Windows.Media.RotateTransform> to a <xref:System.Windows.Controls.Button>.</span></span>  
  
 [!code-xaml[Transforms_snip#MultipleTransformExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/MultipleTransformExample.xaml#multipletransformexamplewholepage)]  
  
 [!code-csharp[Transforms_Procedural_snip#MultipleTransformsCodeExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_Procedural_snip/CSharp/MultipleTransformsExample.cs#multipletransformscodeexamplewholepage)]
 [!code-vb[Transforms_Procedural_snip#MultipleTransformsCodeExampleWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/Transforms_Procedural_snip/VisualBasic/MultipleTransformsExample.vb#multipletransformscodeexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="260d5-106">참고자료</span><span class="sxs-lookup"><span data-stu-id="260d5-106">See also</span></span>
- <xref:System.Windows.UIElement.RenderTransform%2A>
- <xref:System.Windows.Media.TransformGroup>
- [<span data-ttu-id="260d5-107">Transform 개요</span><span class="sxs-lookup"><span data-stu-id="260d5-107">Transforms Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)
- [<span data-ttu-id="260d5-108">2차원 변환 샘플</span><span class="sxs-lookup"><span data-stu-id="260d5-108">2-D Transforms Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=158252)
