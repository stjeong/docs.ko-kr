---
title: TextBox 스타일 및 템플릿
ms.date: 03/30/2017
helpviewer_keywords:
- ControlTemplate [WPF], TextBox
- parts [WPF], TextBox
- states [WPF], TextBox
- styles [WPF], TextBox
- templates [WPF], TextBox
- TextBox [WPF], styles and templates
ms.assetid: aa99130c-43a1-450f-9b46-c40ae0db0cca
ms.openlocfilehash: c04c1386f4663f5893915a07a1e0896a69c5412a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54663676"
---
# <a name="textbox-styles-and-templates"></a><span data-ttu-id="4e1a9-102">TextBox 스타일 및 템플릿</span><span class="sxs-lookup"><span data-stu-id="4e1a9-102">TextBox Styles and Templates</span></span>
<span data-ttu-id="4e1a9-103">이 항목에서는 스타일 및 템플릿에 대해 설명 합니다 <xref:System.Windows.Controls.TextBox> 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.TextBox> control.</span></span> <span data-ttu-id="4e1a9-104">기본값을 수정할 수 있습니다 <xref:System.Windows.Controls.ControlTemplate> 고유한 모양을 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="4e1a9-105">자세한 내용은 [ControlTemplate을 만들어 기존 컨트롤의 모양 사용자 지정](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="textbox-parts"></a><span data-ttu-id="4e1a9-106">텍스트 상자 부분</span><span class="sxs-lookup"><span data-stu-id="4e1a9-106">TextBox Parts</span></span>  
 <span data-ttu-id="4e1a9-107">다음 표에서 대 한 명명된 된 파트를 <xref:System.Windows.Controls.TextBox> 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-107">The following table lists the named parts for the <xref:System.Windows.Controls.TextBox> control.</span></span>  
  
|<span data-ttu-id="4e1a9-108">파트</span><span class="sxs-lookup"><span data-stu-id="4e1a9-108">Part</span></span>|<span data-ttu-id="4e1a9-109">형식</span><span class="sxs-lookup"><span data-stu-id="4e1a9-109">Type</span></span>|<span data-ttu-id="4e1a9-110">설명</span><span class="sxs-lookup"><span data-stu-id="4e1a9-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="4e1a9-111">PART_ContentHost</span><span class="sxs-lookup"><span data-stu-id="4e1a9-111">PART_ContentHost</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="4e1a9-112">포함할 수 있는 시각적 요소를 <xref:System.Windows.FrameworkElement>입니다.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-112">A visual element that can contain a <xref:System.Windows.FrameworkElement>.</span></span> <span data-ttu-id="4e1a9-113">텍스트는 <xref:System.Windows.Controls.TextBox> 이 요소에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-113">The text of the <xref:System.Windows.Controls.TextBox> is displayed in this element.</span></span>|  
  
## <a name="textbox-states"></a><span data-ttu-id="4e1a9-114">텍스트 상자 상태</span><span class="sxs-lookup"><span data-stu-id="4e1a9-114">TextBox States</span></span>  
 <span data-ttu-id="4e1a9-115">다음 표에서 대 한 시각적 상태를 <xref:System.Windows.Controls.TextBox> 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-115">The following table lists the visual states for the <xref:System.Windows.Controls.TextBox> control.</span></span>  
  
|<span data-ttu-id="4e1a9-116">VisualState 이름</span><span class="sxs-lookup"><span data-stu-id="4e1a9-116">VisualState Name</span></span>|<span data-ttu-id="4e1a9-117">VisualStateGroup 이름</span><span class="sxs-lookup"><span data-stu-id="4e1a9-117">VisualStateGroup Name</span></span>|<span data-ttu-id="4e1a9-118">설명</span><span class="sxs-lookup"><span data-stu-id="4e1a9-118">Description</span></span>|  
|----------------------|---------------------------|-----------------|  
|<span data-ttu-id="4e1a9-119">보통</span><span class="sxs-lookup"><span data-stu-id="4e1a9-119">Normal</span></span>|<span data-ttu-id="4e1a9-120">CommonStates</span><span class="sxs-lookup"><span data-stu-id="4e1a9-120">CommonStates</span></span>|<span data-ttu-id="4e1a9-121">기본 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-121">The default state.</span></span>|  
|<span data-ttu-id="4e1a9-122">MouseOver</span><span class="sxs-lookup"><span data-stu-id="4e1a9-122">MouseOver</span></span>|<span data-ttu-id="4e1a9-123">CommonStates</span><span class="sxs-lookup"><span data-stu-id="4e1a9-123">CommonStates</span></span>|<span data-ttu-id="4e1a9-124">마우스 포인터가 컨트롤 위에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-124">The mouse pointer is positioned over the control.</span></span>|  
|<span data-ttu-id="4e1a9-125">사용 안 함</span><span class="sxs-lookup"><span data-stu-id="4e1a9-125">Disabled</span></span>|<span data-ttu-id="4e1a9-126">CommonStates</span><span class="sxs-lookup"><span data-stu-id="4e1a9-126">CommonStates</span></span>|<span data-ttu-id="4e1a9-127">컨트롤이 비활성화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-127">The control is disabled.</span></span>|  
|<span data-ttu-id="4e1a9-128">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4e1a9-128">ReadOnly</span></span>|<span data-ttu-id="4e1a9-129">CommonStates</span><span class="sxs-lookup"><span data-stu-id="4e1a9-129">CommonStates</span></span>|<span data-ttu-id="4e1a9-130">사용자의 텍스트를 변경할 수 없습니다는 <xref:System.Windows.Controls.TextBox>합니다.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-130">The user cannot change the text in the <xref:System.Windows.Controls.TextBox>.</span></span>|  
|<span data-ttu-id="4e1a9-131">포커스 있음</span><span class="sxs-lookup"><span data-stu-id="4e1a9-131">Focused</span></span>|<span data-ttu-id="4e1a9-132">FocusStates</span><span class="sxs-lookup"><span data-stu-id="4e1a9-132">FocusStates</span></span>|<span data-ttu-id="4e1a9-133">컨트롤에 포커스가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-133">The control has focus.</span></span>|  
|<span data-ttu-id="4e1a9-134">포커스 없음</span><span class="sxs-lookup"><span data-stu-id="4e1a9-134">Unfocused</span></span>|<span data-ttu-id="4e1a9-135">FocusStates</span><span class="sxs-lookup"><span data-stu-id="4e1a9-135">FocusStates</span></span>|<span data-ttu-id="4e1a9-136">컨트롤에 포커스가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-136">The control does not have focus.</span></span>|  
|<span data-ttu-id="4e1a9-137">유효</span><span class="sxs-lookup"><span data-stu-id="4e1a9-137">Valid</span></span>|<span data-ttu-id="4e1a9-138">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="4e1a9-138">ValidationStates</span></span>|<span data-ttu-id="4e1a9-139">컨트롤에서 사용 된 <xref:System.Windows.Controls.Validation> 클래스 및 <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> 연결 된 속성은 `false`합니다.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-139">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="4e1a9-140">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="4e1a9-140">InvalidFocused</span></span>|<span data-ttu-id="4e1a9-141">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="4e1a9-141">ValidationStates</span></span>|<span data-ttu-id="4e1a9-142">합니다 <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> 연결 된 속성은 `true` 가 컨트롤에 포커스가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-142">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="4e1a9-143">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="4e1a9-143">InvalidUnfocused</span></span>|<span data-ttu-id="4e1a9-144">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="4e1a9-144">ValidationStates</span></span>|<span data-ttu-id="4e1a9-145">합니다 <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> 연결 된 속성은 `true` 가 컨트롤에 포커스가 없는 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-145">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="textbox-controltemplate-example"></a><span data-ttu-id="4e1a9-146">텍스트 상자 ControlTemplate 예제</span><span class="sxs-lookup"><span data-stu-id="4e1a9-146">TextBox ControlTemplate Example</span></span>  
 <span data-ttu-id="4e1a9-147">다음 예제에서는 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Controls.ControlTemplate> 에 대 한는 <xref:System.Windows.Controls.TextBox> 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-147">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.TextBox> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#TextBox](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/textbox.xaml#textbox)]  
  
 <span data-ttu-id="4e1a9-148">앞의 예제에서는 다음 리소스를 하나 이상 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-148">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="4e1a9-149">전체 샘플을 보려면 [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating)(ControlTemplate으로 스타일 지정 샘플)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4e1a9-149">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4e1a9-150">참고자료</span><span class="sxs-lookup"><span data-stu-id="4e1a9-150">See also</span></span>
- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="4e1a9-151">Control 스타일 및 템플릿</span><span class="sxs-lookup"><span data-stu-id="4e1a9-151">Control Styles and Templates</span></span>](../../../../docs/framework/wpf/controls/control-styles-and-templates.md)
- [<span data-ttu-id="4e1a9-152">컨트롤 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="4e1a9-152">Control Customization</span></span>](../../../../docs/framework/wpf/controls/control-customization.md)
- [<span data-ttu-id="4e1a9-153">스타일 지정 및 템플릿</span><span class="sxs-lookup"><span data-stu-id="4e1a9-153">Styling and Templating</span></span>](../../../../docs/framework/wpf/controls/styling-and-templating.md)
- [<span data-ttu-id="4e1a9-154">ControlTemplate을 만들어 기존 컨트롤의 모양 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="4e1a9-154">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)
