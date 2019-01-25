---
title: '방법: Visual로 비트맵 만들기'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bitmaps [WPF], rendering from visuals
- visuals [WPF], rendering to bitmaps
ms.assetid: 103fc7f5-7306-4026-9d61-2005e79959f3
ms.openlocfilehash: dbbf7691508e5e5ddf3ed3af768f757ee0c3f20c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54705455"
---
# <a name="how-to-create-a-bitmap-from-a-visual"></a>방법: Visual로 비트맵 만들기
비트맵을 만드는 방법을 보여 주는이 예제는 <xref:System.Windows.Media.Visual>합니다. A <xref:System.Windows.Media.DrawingVisual> 와 함께 렌더링 된 <xref:System.Windows.Media.FormattedText>합니다. 합니다 <xref:System.Windows.Media.Visual> 다음에 렌더링 되는 <xref:System.Windows.Media.Imaging.RenderTargetBitmap> 지정된 된 텍스트의 비트맵을 만들 합니다.  
  
## <a name="example"></a>예제  
 [!code-csharp[ImagingSnippetGallery_procedural_snip#CreateRTBImage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/CSharp/RenderTargetBitmapExample.cs#creatertbimage)]
 [!code-vb[ImagingSnippetGallery_procedural_snip#CreateRTBImage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/VB/RenderTargetBitmapExample.vb#creatertbimage)]  
  
## <a name="see-also"></a>참고자료
- <xref:System.Windows.Media.DrawingContext>
- [이미징 개요](../../../../docs/framework/wpf/graphics-multimedia/imaging-overview.md)
- [Drawing 개체 개요](../../../../docs/framework/wpf/graphics-multimedia/drawing-objects-overview.md)
- [DrawingVisual 개체 사용](../../../../docs/framework/wpf/graphics-multimedia/using-drawingvisual-objects.md)
