---
title: '방법: DataRepeater 컨트롤 (Visual Studio)의 모양 변경'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataRepeater, customizing
- DataRepeater, changing run time appearance
ms.assetid: 2af6dfce-760b-489e-b863-8da967f315c3
ms.openlocfilehash: e5508329ba716b53eff0c9e1bfe13e190fa1fd85
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54716637"
---
# <a name="how-to-change-the-appearance-of-a-datarepeater-control-visual-studio"></a><span data-ttu-id="2f10b-102">방법: DataRepeater 컨트롤 (Visual Studio)의 모양 변경</span><span class="sxs-lookup"><span data-stu-id="2f10b-102">How to: Change the Appearance of a DataRepeater Control (Visual Studio)</span></span>
<span data-ttu-id="2f10b-103">모양을 변경할 수 있습니다는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 속성을 설정 하 여 디자인 타임 또는 런타임에 처리 하 여 컨트롤을 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem> 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="2f10b-103">You can change the appearance of a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control at design time by setting properties or at run time by handling the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem> event.</span></span>  
  
 <span data-ttu-id="2f10b-104">컨트롤의 항목 템플릿 섹션을 선택한 경우 디자인 타임에 설정 하는 속성 각각에 대해 반복 됩니다 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem> 런타임 시.</span><span class="sxs-lookup"><span data-stu-id="2f10b-104">Properties that you set at design time when the item template section of the control is selected will be repeated for each <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem> at run time.</span></span> <span data-ttu-id="2f10b-105">모양과 관련 된 속성을 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 런타임 시 컨테이너의 일부가 되는 경우에만 그대로 살펴보기 컨트롤 자체는 표시 됩니다 (경우에 예를 들어를 <xref:System.Windows.Forms.Control.Padding%2A> 큰 값으로 설정).</span><span class="sxs-lookup"><span data-stu-id="2f10b-105">Appearance-related properties of the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control itself will be visible at run time only if a part of the container is left uncovered (for example, if the <xref:System.Windows.Forms.Control.Padding%2A> property is set to a large value).</span></span>  
  
 <span data-ttu-id="2f10b-106">런타임 시 모양 관련 속성을 설정할 수 있습니다 기반 조건에.</span><span class="sxs-lookup"><span data-stu-id="2f10b-106">At run time, appearance-related properties can be set based on conditions.</span></span> <span data-ttu-id="2f10b-107">예를 들어, 일정 관리 응용 프로그램에서 사용자에 게 경고할 기한 항목은 항목의 배경색을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f10b-107">For example, in a scheduling application, you might change the background color of an item to warn users when an item is past due.</span></span> <span data-ttu-id="2f10b-108">에 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem> 같은 조건문에서 속성을 설정 하는 경우 이벤트 처리기 `If…Then`을 사용 해야는 `Else` 절 조건에 맞지 않을 때 모양을 지정할 수.</span><span class="sxs-lookup"><span data-stu-id="2f10b-108">In the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem> event handler, if you set a property in a conditional statement such as `If…Then`, you must also use an `Else` clause to specify the appearance when the condition is not met.</span></span>  
  
### <a name="to-change-the-appearance-at-design-time"></a><span data-ttu-id="2f10b-109">디자인 타임 모양을 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="2f10b-109">To change the appearance at design time</span></span>  
  
1.  <span data-ttu-id="2f10b-110">Windows Forms 디자이너에서의 항목 템플릿 (위) 영역을 선택 합니다 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f10b-110">In the Windows Forms Designer, select the item template (upper) region of the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control.</span></span>  
  
2.  <span data-ttu-id="2f10b-111">속성 창에서 속성을 선택 하 고 값을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f10b-111">In the Properties window, select a property and change the value.</span></span> <span data-ttu-id="2f10b-112">모양에 영향을 주는 공용 속성에 포함 <xref:System.Windows.Forms.Control.BackColor%2A>, <xref:System.Windows.Forms.Control.BackgroundImage%2A>를 <xref:System.Windows.Forms.Panel.BorderStyle%2A>, 및 <xref:System.Windows.Forms.Control.ForeColor%2A>합니다.</span><span class="sxs-lookup"><span data-stu-id="2f10b-112">Common properties that affect appearance include <xref:System.Windows.Forms.Control.BackColor%2A>, <xref:System.Windows.Forms.Control.BackgroundImage%2A>, <xref:System.Windows.Forms.Panel.BorderStyle%2A>, and <xref:System.Windows.Forms.Control.ForeColor%2A>.</span></span>  
  
### <a name="to-change-the-appearance-at-run-time"></a><span data-ttu-id="2f10b-113">런타임 시 모양을 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="2f10b-113">To change the appearance at run time</span></span>  
  
1.  <span data-ttu-id="2f10b-114">코드 편집기의 이벤트 드롭다운 목록에서 **DrawItem**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="2f10b-114">In the Code Editor, in the Event drop-down list, click **DrawItem**.</span></span>  
  
2.  <span data-ttu-id="2f10b-115">에 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem> 이벤트 처리기 속성을 설정 하는 코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f10b-115">In the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem> event handler, add code to set the properties:</span></span>  
  
     [!code-csharp[VbPowerPacksDataRepeaterAppearance#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio_1.cs)]
     [!code-vb[VbPowerPacksDataRepeaterAppearance#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio_1.vb)]  
  
## <a name="example"></a><span data-ttu-id="2f10b-116">예제</span><span class="sxs-lookup"><span data-stu-id="2f10b-116">Example</span></span>  
 <span data-ttu-id="2f10b-117">에 대 한 일부 일반적인 사용자 지정을 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 컨트롤 포함의 색을 교대로 반복 되는 조건에 따라 필드의 색을 변경 하는 행을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f10b-117">Some common customizations for the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control include displaying the rows in alternating colors and changing the color of a field based on a condition.</span></span> <span data-ttu-id="2f10b-118">다음 예제에서는 이러한 사용자 지정을 수행 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2f10b-118">The following example shows how to perform these customizations.</span></span> <span data-ttu-id="2f10b-119">이 예에서는 있다고 가정 된 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> Northwind 데이터베이스의 Products 테이블에 바인딩된 컨트롤입니다.</span><span class="sxs-lookup"><span data-stu-id="2f10b-119">This example assumes that you have a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control that is bound to the Products table in the Northwind database.</span></span>  
  
 [!code-vb[VbPowerPacksDataRepeaterAlternateBackColor#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio_2.vb)]
 [!code-csharp[VbPowerPacksDataRepeaterAlternateBackColor#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio_2.cs)]  
  
 <span data-ttu-id="2f10b-120">이러한 사용자 지정 둘 다 제공 해야 하는 조건의 양쪽 모두에 대 한 속성을 설정 하는 코드를 참고 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f10b-120">Note that for both of these customizations, you must provide code to set the properties for both sides of the condition.</span></span> <span data-ttu-id="2f10b-121">지정 하지 않으면 경우는 `Else` 조건 런타임에 예기치 않은 결과가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f10b-121">If you do not specify the `Else` condition, you will see unexpected results at run time.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2f10b-122">참고자료</span><span class="sxs-lookup"><span data-stu-id="2f10b-122">See also</span></span>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem>
- [<span data-ttu-id="2f10b-123">DataRepeater 컨트롤 소개</span><span class="sxs-lookup"><span data-stu-id="2f10b-123">Introduction to the DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)
- [<span data-ttu-id="2f10b-124">DataRepeater 컨트롤 문제 해결</span><span class="sxs-lookup"><span data-stu-id="2f10b-124">Troubleshooting the DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
- [<span data-ttu-id="2f10b-125">방법: DataRepeater 컨트롤의 바인딩된 데이터 표시</span><span class="sxs-lookup"><span data-stu-id="2f10b-125">How to: Display Bound Data in a DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-display-bound-data-in-a-datarepeater-control-visual-studio.md)
- [<span data-ttu-id="2f10b-126">방법: DataRepeater 컨트롤의 바인딩되지 않은 컨트롤 표시</span><span class="sxs-lookup"><span data-stu-id="2f10b-126">How to: Display Unbound Controls in a DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-display-unbound-controls-in-a-datarepeater-control-visual-studio.md)
- [<span data-ttu-id="2f10b-127">방법: DataRepeater 컨트롤의 항목 머리글 표시</span><span class="sxs-lookup"><span data-stu-id="2f10b-127">How to: Display Item Headers in a DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-display-item-headers-in-a-datarepeater-control-visual-studio.md)
