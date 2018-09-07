---
title: '방법: GruopBox 템플릿 정의'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], GroupBox
- GroupBox control [WPF], creating templates
ms.assetid: 85a4d1a7-4753-4f4a-b26d-14fa10c1ddb5
ms.openlocfilehash: a47ce896be4d1c38147584dd80b1bc841737d526
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44062507"
---
# <a name="how-to-define-a-groupbox-template"></a><span data-ttu-id="be7a8-102">방법: GruopBox 템플릿 정의</span><span class="sxs-lookup"><span data-stu-id="be7a8-102">How to: Define a GroupBox Template</span></span>
<span data-ttu-id="be7a8-103">에 대 한 템플릿을 만드는 방법을 보여 주는이 예제는 <xref:System.Windows.Controls.GroupBox> 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="be7a8-103">This example shows how to create a template for a <xref:System.Windows.Controls.GroupBox> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="be7a8-104">예제</span><span class="sxs-lookup"><span data-stu-id="be7a8-104">Example</span></span>  
 <span data-ttu-id="be7a8-105">다음 예제에서는 정의 <xref:System.Windows.Controls.GroupBox> 컨트롤 템플릿을 사용 하 여를 <xref:System.Windows.Controls.Grid> 레이아웃에 대 한 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="be7a8-105">The following example defines a <xref:System.Windows.Controls.GroupBox> control template by using a <xref:System.Windows.Controls.Grid> control for layout.</span></span> <span data-ttu-id="be7a8-106">템플릿을 사용 하는 <xref:System.Windows.Controls.BorderGapMaskConverter> 경계를 정의 하는 <xref:System.Windows.Controls.GroupBox> 테두리를 가리지 않습니다 있도록는 <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> 콘텐츠.</span><span class="sxs-lookup"><span data-stu-id="be7a8-106">The template uses a <xref:System.Windows.Controls.BorderGapMaskConverter> to define the border of the <xref:System.Windows.Controls.GroupBox> so that the border does not obscure the <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> content.</span></span>  
  
 [!code-xaml[GroupBoxSnippet#GroupBoxTemplate](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GroupBoxSnippet/CS/Window1.xaml#groupboxtemplate)]  
  
## <a name="see-also"></a><span data-ttu-id="be7a8-107">참고 항목</span><span class="sxs-lookup"><span data-stu-id="be7a8-107">See Also</span></span>  
 <xref:System.Windows.Controls.GroupBox>  
 [<span data-ttu-id="be7a8-108">GroupBox 방법 도움말 항목</span><span class="sxs-lookup"><span data-stu-id="be7a8-108">GroupBox How-to Topics</span></span>](https://msdn.microsoft.com/library/7692e155-a4c6-428c-b7e0-64b3740daca7)
