---
title: '방법: 단색 브러시 만들기'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- solid color brushes
- brushes [Windows Forms], examples
- brushes [Windows Forms], creating solid
ms.assetid: 85c3fe7d-fb1d-4591-8a9f-d75b556b90af
ms.openlocfilehash: 0943bd1d5e05a1d726f0f6c55e372b9ff70cc4ca
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54632272"
---
# <a name="how-to-create-a-solid-brush"></a><span data-ttu-id="0b33b-102">방법: 단색 브러시 만들기</span><span class="sxs-lookup"><span data-stu-id="0b33b-102">How to: Create a Solid Brush</span></span>
<span data-ttu-id="0b33b-103">이 예제에서는 만듭니다는 <xref:System.Drawing.SolidBrush> 에서 사용할 수 있는 개체를 <xref:System.Drawing.Graphics> 모양을 채우는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0b33b-103">This example creates a <xref:System.Drawing.SolidBrush> object that can be used by a <xref:System.Drawing.Graphics> object for filling shapes.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0b33b-104">예제</span><span class="sxs-lookup"><span data-stu-id="0b33b-104">Example</span></span>  
 [!code-cpp[System.Drawing.ConceptualHowTos#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#1)]
 [!code-csharp[System.Drawing.ConceptualHowTos#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#1)]
 [!code-vb[System.Drawing.ConceptualHowTos#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#1)]  
  
## <a name="robust-programming"></a><span data-ttu-id="0b33b-105">강력한 프로그래밍</span><span class="sxs-lookup"><span data-stu-id="0b33b-105">Robust Programming</span></span>  
 <span data-ttu-id="0b33b-106">호출 해야 사용을 완료 한 후 <xref:System.IDisposable.Dispose%2A> 브러시 개체와 같은 시스템 리소스를 사용 하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0b33b-106">After you have finished using them, you should call <xref:System.IDisposable.Dispose%2A> on objects that consume system resources, such as brush objects.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b33b-107">참고자료</span><span class="sxs-lookup"><span data-stu-id="0b33b-107">See also</span></span>
- <xref:System.Drawing.SolidBrush>
- <xref:System.Drawing.Brush>
- [<span data-ttu-id="0b33b-108">그래픽 프로그래밍 시작</span><span class="sxs-lookup"><span data-stu-id="0b33b-108">Getting Started with Graphics Programming</span></span>](../../../../docs/framework/winforms/advanced/getting-started-with-graphics-programming.md)
- [<span data-ttu-id="0b33b-109">GDI+의 브러시 및 채워진 도형</span><span class="sxs-lookup"><span data-stu-id="0b33b-109">Brushes and Filled Shapes in GDI+</span></span>](../../../../docs/framework/winforms/advanced/brushes-and-filled-shapes-in-gdi.md)
- [<span data-ttu-id="0b33b-110">브러시를 사용하여 도형 채우기</span><span class="sxs-lookup"><span data-stu-id="0b33b-110">Using a Brush to Fill Shapes</span></span>](../../../../docs/framework/winforms/advanced/using-a-brush-to-fill-shapes.md)
