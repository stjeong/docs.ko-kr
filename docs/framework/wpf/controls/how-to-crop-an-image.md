---
title: '방법: 이미지 잘라내기'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [WPF], cropping
- cropping images [WPF]
ms.assetid: c6bba109-c6e7-4cf8-bfe6-9cf8d01bb4fc
ms.openlocfilehash: 189cb92d581ccc9209ebdb4de18487951d17818a
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2018
ms.locfileid: "49308281"
---
# <a name="how-to-crop-an-image"></a>방법: 이미지 잘라내기
이 예제를 사용 하 여 이미지를 자르는 방법을 보여 줍니다 <xref:System.Windows.Media.Imaging.CroppedBitmap>합니다.  
  
 <xref:System.Windows.Media.Imaging.CroppedBitmap> 파일에 저장할 이미지의 버전을 자른된 인코딩할 때 사용 주로 됩니다. 표시 목적으로 참조에 대 한 이미지를 [클립 영역을 만들](https://msdn.microsoft.com/library/56e4bed6-78d7-4292-b917-d72d0b3e4376) 항목입니다.  
  
## <a name="example"></a>예제  
 다음 [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] 아래의 샘플에 사용 되는 리소스를 정의 합니다.  
  
 [!code-xaml[imageelementexample#CroppedXAML1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml1)]  
  
 다음 예제에서는 사용 하 여 이미지를 <xref:System.Windows.Media.Imaging.CroppedBitmap> 원본으로 합니다.  
  
 [!code-xaml[imageelementexample#CroppedXAML2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml2)]  
  
 [!code-csharp[imageelementexample#CroppedCSharp1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml.cs#croppedcsharp1)]
 [!code-vb[imageelementexample#CroppedCSharp1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample/VB/CroppedImageExample.xaml.vb#croppedcsharp1)]  
  
 합니다 <xref:System.Windows.Media.Imaging.CroppedBitmap> 다른 원본으로 사용할 수도 있습니다 <xref:System.Windows.Media.Imaging.CroppedBitmap>, 자르기 체 이닝 합니다. <xref:System.Windows.Media.Imaging.CroppedBitmap.SourceRect%2A> 비트맵 및 초기 이미지가 아닌 잘려진 소스와 관련 된 값을 사용 합니다.  
  
 [!code-xaml[imageelementexample#CroppedXAML3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml3)]  
  
 [!code-csharp[imageelementexample#CroppedCSharp2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml.cs#croppedcsharp2)]
 [!code-vb[imageelementexample#CroppedCSharp2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample/VB/CroppedImageExample.xaml.vb#croppedcsharp2)]  
  
## <a name="see-also"></a>참고 항목  
 [클립 영역 만들기](https://msdn.microsoft.com/library/56e4bed6-78d7-4292-b917-d72d0b3e4376)
