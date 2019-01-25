---
title: '방법: TextBox 컨트롤에서 탭 문자 사용'
ms.date: 03/30/2017
helpviewer_keywords:
- TextBox control [WPF], enabling tab characters
- tab characters [WPF], enabling
ms.assetid: 14b1b064-61f7-4958-be63-88d85b868d03
ms.openlocfilehash: de3336838ba35a70575ec2549c79faf04be2e7a5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54743610"
---
# <a name="how-to-enable-tab-characters-in-a-textbox-control"></a><span data-ttu-id="a4f44-102">방법: TextBox 컨트롤에서 탭 문자 사용</span><span class="sxs-lookup"><span data-stu-id="a4f44-102">How to: Enable Tab Characters in a TextBox Control</span></span>
<span data-ttu-id="a4f44-103">탭 문자에 대 한 동의가 일반 입력으로 사용 하도록 설정 하는 방법을 보여 주는이 예제는 <xref:System.Windows.Controls.TextBox> 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f44-103">This example shows how to enable the acceptance of tab characters as normal input in a <xref:System.Windows.Controls.TextBox> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a4f44-104">예제</span><span class="sxs-lookup"><span data-stu-id="a4f44-104">Example</span></span>  
 <span data-ttu-id="a4f44-105">탭 문자에 대 한 동의가에서 입력으로 사용 하도록 설정 하려면을 <xref:System.Windows.Controls.TextBox> 컨트롤을 <xref:System.Windows.Controls.Primitives.TextBoxBase.AcceptsTab%2A> 특성을 **true**합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f44-105">To enable the acceptance of tab characters as input in a <xref:System.Windows.Controls.TextBox> control, set the <xref:System.Windows.Controls.Primitives.TextBoxBase.AcceptsTab%2A> attribute to **true**.</span></span>  
  
 [!code-xaml[TextBox_EnablingTab#_AcceptsTab](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextBox_EnablingTab/CS/Window1.xaml#_acceptstab)]  
  
## <a name="see-also"></a><span data-ttu-id="a4f44-106">참고자료</span><span class="sxs-lookup"><span data-stu-id="a4f44-106">See also</span></span>
- [<span data-ttu-id="a4f44-107">TextBox 개요</span><span class="sxs-lookup"><span data-stu-id="a4f44-107">TextBox Overview</span></span>](../../../../docs/framework/wpf/controls/textbox-overview.md)
- [<span data-ttu-id="a4f44-108">RichTextBox 개요</span><span class="sxs-lookup"><span data-stu-id="a4f44-108">RichTextBox Overview</span></span>](../../../../docs/framework/wpf/controls/richtextbox-overview.md)
