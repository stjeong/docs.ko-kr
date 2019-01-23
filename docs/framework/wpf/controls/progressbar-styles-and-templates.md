---
title: ProgressBar 스타일 및 템플릿
ms.date: 03/30/2017
helpviewer_keywords:
- parts [WPF], ProgressBar
- ProgressBar [WPF], styles and templates
- styles [WPF], ProgressBar
- ControlTemplate [WPF], ProgressBar
- templates [WPF], ProgressBar
- states [WPF], ProgressBar
ms.assetid: 935aa600-16e6-4947-a905-37a189a583dd
ms.openlocfilehash: 7e410642e6153ed8064b2ddfb38fddd9cce6f4de
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54525381"
---
# <a name="progressbar-styles-and-templates"></a><span data-ttu-id="0cc6a-102">ProgressBar 스타일 및 템플릿</span><span class="sxs-lookup"><span data-stu-id="0cc6a-102">ProgressBar Styles and Templates</span></span>
<span data-ttu-id="0cc6a-103">이 항목에서는 스타일 및 템플릿에 대해 설명 합니다 <xref:System.Windows.Controls.ProgressBar> 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cc6a-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.ProgressBar> control.</span></span> <span data-ttu-id="0cc6a-104">기본값을 수정할 수 있습니다 <xref:System.Windows.Controls.ControlTemplate> 고유한 모양을 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0cc6a-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="0cc6a-105">자세한 내용은 [ControlTemplate을 만들어 기존 컨트롤의 모양 사용자 지정](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0cc6a-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="progressbar-parts"></a><span data-ttu-id="0cc6a-106">ProgressBar 파트</span><span class="sxs-lookup"><span data-stu-id="0cc6a-106">ProgressBar Parts</span></span>  
 <span data-ttu-id="0cc6a-107">다음 표에서 대 한 명명된 된 파트를 <xref:System.Windows.Controls.ProgressBar> 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cc6a-107">The following table lists the named parts for the <xref:System.Windows.Controls.ProgressBar> control.</span></span>  
  
|<span data-ttu-id="0cc6a-108">파트</span><span class="sxs-lookup"><span data-stu-id="0cc6a-108">Part</span></span>|<span data-ttu-id="0cc6a-109">형식</span><span class="sxs-lookup"><span data-stu-id="0cc6a-109">Type</span></span>|<span data-ttu-id="0cc6a-110">설명</span><span class="sxs-lookup"><span data-stu-id="0cc6a-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="0cc6a-111">PART_Indicator</span><span class="sxs-lookup"><span data-stu-id="0cc6a-111">PART_Indicator</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="0cc6a-112">진행률을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0cc6a-112">The object that indicates progress.</span></span>|  
|<span data-ttu-id="0cc6a-113">PART_Track</span><span class="sxs-lookup"><span data-stu-id="0cc6a-113">PART_Track</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="0cc6a-114">진행률 표시기의 경로 정의 하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0cc6a-114">The object that defines the path of the progress indicator.</span></span>|  
|<span data-ttu-id="0cc6a-115">PART_GlowRect</span><span class="sxs-lookup"><span data-stu-id="0cc6a-115">PART_GlowRect</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="0cc6a-116">진행률 표시줄을 장식 하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0cc6a-116">An object that embellishes the progress bar.</span></span>|  
  
## <a name="progressbar-states"></a><span data-ttu-id="0cc6a-117">ProgressBar 상태</span><span class="sxs-lookup"><span data-stu-id="0cc6a-117">ProgressBar States</span></span>  
 <span data-ttu-id="0cc6a-118">다음 표에서 대 한 시각적 상태를 <xref:System.Windows.Controls.ProgressBar> 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cc6a-118">The following table lists the visual states for the <xref:System.Windows.Controls.ProgressBar> control.</span></span>  
  
|<span data-ttu-id="0cc6a-119">VisualState 이름</span><span class="sxs-lookup"><span data-stu-id="0cc6a-119">VisualState Name</span></span>|<span data-ttu-id="0cc6a-120">VisualStateGroup 이름</span><span class="sxs-lookup"><span data-stu-id="0cc6a-120">VisualStateGroup Name</span></span>|<span data-ttu-id="0cc6a-121">설명</span><span class="sxs-lookup"><span data-stu-id="0cc6a-121">Description</span></span>|  
|----------------------|---------------------------|-----------------|  
|<span data-ttu-id="0cc6a-122">비활성화 상태</span><span class="sxs-lookup"><span data-stu-id="0cc6a-122">Determinate</span></span>|<span data-ttu-id="0cc6a-123">CommonStates</span><span class="sxs-lookup"><span data-stu-id="0cc6a-123">CommonStates</span></span>|<span data-ttu-id="0cc6a-124"><xref:System.Windows.Controls.ProgressBar> 기반의 진행률 보고를 <xref:System.Windows.Controls.Primitives.RangeBase.Value%2A> 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="0cc6a-124"><xref:System.Windows.Controls.ProgressBar> reports progress based on the <xref:System.Windows.Controls.Primitives.RangeBase.Value%2A> property.</span></span>|  
|<span data-ttu-id="0cc6a-125">비활성화</span><span class="sxs-lookup"><span data-stu-id="0cc6a-125">Indeterminate</span></span>|<span data-ttu-id="0cc6a-126">CommonStates</span><span class="sxs-lookup"><span data-stu-id="0cc6a-126">CommonStates</span></span>|<span data-ttu-id="0cc6a-127"><xref:System.Windows.Controls.ProgressBar> 반복 패턴을 사용 하 여 제네릭 진행률을 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cc6a-127"><xref:System.Windows.Controls.ProgressBar> reports generic progress with a repeating pattern.</span></span>|  
|<span data-ttu-id="0cc6a-128">유효</span><span class="sxs-lookup"><span data-stu-id="0cc6a-128">Valid</span></span>|<span data-ttu-id="0cc6a-129">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="0cc6a-129">ValidationStates</span></span>|<span data-ttu-id="0cc6a-130">컨트롤에서 사용 된 <xref:System.Windows.Controls.Validation> 클래스 및 <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> 연결 된 속성은 `false`합니다.</span><span class="sxs-lookup"><span data-stu-id="0cc6a-130">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="0cc6a-131">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="0cc6a-131">InvalidFocused</span></span>|<span data-ttu-id="0cc6a-132">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="0cc6a-132">ValidationStates</span></span>|<span data-ttu-id="0cc6a-133">합니다 <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> 연결 된 속성은 `true` 가 컨트롤에 포커스가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0cc6a-133">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="0cc6a-134">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="0cc6a-134">InvalidUnfocused</span></span>|<span data-ttu-id="0cc6a-135">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="0cc6a-135">ValidationStates</span></span>|<span data-ttu-id="0cc6a-136">합니다 <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> 연결 된 속성은 `true` 가 컨트롤에 포커스가 없는 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cc6a-136">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="progressbar-controltemplate-example"></a><span data-ttu-id="0cc6a-137">ProgressBar ControlTemplate 예제</span><span class="sxs-lookup"><span data-stu-id="0cc6a-137">ProgressBar ControlTemplate Example</span></span>  
 <span data-ttu-id="0cc6a-138">다음 예제에서는 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Controls.ControlTemplate> 에 대 한는 <xref:System.Windows.Controls.ProgressBar> 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cc6a-138">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.ProgressBar> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#ProgressBar](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/progressbar.xaml#progressbar)]  
  
 <span data-ttu-id="0cc6a-139">앞의 예제에서는 다음 리소스를 하나 이상 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0cc6a-139">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="0cc6a-140">전체 샘플을 보려면 [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating)(ControlTemplate으로 스타일 지정 샘플)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0cc6a-140">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0cc6a-141">참고자료</span><span class="sxs-lookup"><span data-stu-id="0cc6a-141">See also</span></span>
- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="0cc6a-142">Control 스타일 및 템플릿</span><span class="sxs-lookup"><span data-stu-id="0cc6a-142">Control Styles and Templates</span></span>](../../../../docs/framework/wpf/controls/control-styles-and-templates.md)
- [<span data-ttu-id="0cc6a-143">컨트롤 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="0cc6a-143">Control Customization</span></span>](../../../../docs/framework/wpf/controls/control-customization.md)
- [<span data-ttu-id="0cc6a-144">스타일 지정 및 템플릿</span><span class="sxs-lookup"><span data-stu-id="0cc6a-144">Styling and Templating</span></span>](../../../../docs/framework/wpf/controls/styling-and-templating.md)
- [<span data-ttu-id="0cc6a-145">ControlTemplate을 만들어 기존 컨트롤의 모양 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="0cc6a-145">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)
