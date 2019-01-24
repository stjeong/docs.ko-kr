---
title: '방법: 이미지를 축소판으로 로드'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- loading images as thumbnails [WPF]
- images [WPF], loading as thumbnails
- thumbnails [WPF], loading images as
ms.assetid: 02e055a0-54df-499a-b8b6-ab6ff7535cff
ms.openlocfilehash: d92a489f19f8c7160bed5ec83535bdc33cfe561b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54735989"
---
# <a name="how-to-load-an-image-as-a-thumbnail"></a>방법: 이미지를 축소판으로 로드
다음 예제에서는 로드 하는 방법을 보여 줍니다는 <xref:System.Windows.Controls.Image> 응용 프로그램 메모리를 절약 하기 위해를 축소판으로 합니다.  
  
## <a name="example"></a>예제  
 다음 예제에서는 합니다 <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> 의 속성을 <xref:System.Windows.Media.Imaging.BitmapImage> 에서 [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] 이미지를 로드 하는 데 필요한 메모리를 줄일 수입니다.  
  
 [!code-xaml[ImageElementExample_snip#ImageSimpleExampleInlineMarkup](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample_snip/CSharp/ImageSimpleExample.xaml#imagesimpleexampleinlinemarkup)]  
  
## <a name="example"></a>예제  
 다음 예제에서는 합니다 <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> 의 속성을 <xref:System.Windows.Media.Imaging.BitmapImage> 이미지를 로드 하는 데 필요한 메모리를 줄이기 위해 코드에서.  
  
 [!code-csharp[ImageElementExample_snip#ImageSimpleExampleInlineCode1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample_snip/CSharp/ImageSimpleExample.xaml.cs#imagesimpleexampleinlinecode1)]
 [!code-vb[ImageElementExample_snip#ImageSimpleExampleInlineCode1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample_snip/VB/ImageSimpleExample.xaml.vb#imagesimpleexampleinlinecode1)]  
  
## <a name="see-also"></a>참고자료
- [이미징 개요](../../../../docs/framework/wpf/graphics-multimedia/imaging-overview.md)
