---
title: '방법: DataRepeater 컨트롤 (Visual Studio)의 바인딩되지 않은 컨트롤 표시'
ms.date: 07/20/2015
helpviewer_keywords:
- DataRepeater, adding unbound controls
- DataRepeater
- displaying unbound data
ms.assetid: f234fa40-5a13-4209-930e-7c5f81e86e66
ms.openlocfilehash: a20e1ba83d1963bc3d4c135817767ee02fcbdeda
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54730791"
---
# <a name="how-to-display-unbound-controls-in-a-datarepeater-control-visual-studio"></a><span data-ttu-id="7d844-102">방법: DataRepeater 컨트롤 (Visual Studio)의 바인딩되지 않은 컨트롤 표시</span><span class="sxs-lookup"><span data-stu-id="7d844-102">How to: Display Unbound Controls in a DataRepeater Control (Visual Studio)</span></span>
<span data-ttu-id="7d844-103">바인딩된 컨트롤 외에도 다른 컨트롤을 추가 하려는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>정적 레이블 또는 각 항목에 대해 반복 되는 이미지 등의 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 컨트롤.</span><span class="sxs-lookup"><span data-stu-id="7d844-103">In addition to bound controls, you may want to add other controls to a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>, such as a static label or an image that is repeated on each item in the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7d844-104">바인딩된 컨트롤을 하나 이상 있어야 합니다 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 또는 아무 것도 런타임에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d844-104">You must also have at least one bound control on the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> or nothing will be displayed at run time.</span></span>  
  
### <a name="to-add-unbound-controls-to-a-datarepeater"></a><span data-ttu-id="7d844-105">DataRepeater에 바인딩되지 않은 컨트롤을 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="7d844-105">To add unbound controls to a DataRepeater</span></span>  
  
1.  <span data-ttu-id="7d844-106">끌어서를 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 에서 제어 합니다 **Visual Basic PowerPacks** 탭에 **도구 상자** 폼 이나 컨테이너 컨트롤에.</span><span class="sxs-lookup"><span data-stu-id="7d844-106">Drag a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control from the **Visual Basic PowerPacks** tab in the **Toolbox** to a form or container control.</span></span>  
  
2.  <span data-ttu-id="7d844-107">핸들 크기 조정 및 위치를 끌어서 크기와 컨트롤을 배치 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d844-107">Drag the sizing and position handles to size and position the control.</span></span>  
  
     <span data-ttu-id="7d844-108">또한 크기를 변경 하 여 컨트롤을 배치 합니다 **크기** 하 고 **위치** 속성 창에서 속성.</span><span class="sxs-lookup"><span data-stu-id="7d844-108">You can also size and position the control by changing the **Size** and **Position** properties in the Properties window.</span></span>  
  
3.  <span data-ttu-id="7d844-109">하나 이상의 데이터 바인딩된 컨트롤을 추가 합니다 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d844-109">Add at least one data-bound control to the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control.</span></span> <span data-ttu-id="7d844-110">자세한 내용은 [방법: DataRepeater 컨트롤의 바인딩된 데이터 표시](../../../visual-basic/developing-apps/windows-forms/how-to-display-bound-data-in-a-datarepeater-control-visual-studio.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="7d844-110">For more information, see [How to: Display Bound Data in a DataRepeater Control](../../../visual-basic/developing-apps/windows-forms/how-to-display-bound-data-in-a-datarepeater-control-visual-studio.md).</span></span>  
  
4.  <span data-ttu-id="7d844-111">컨트롤을 끌어 합니다 **도구 상자** 의 항목 템플릿 영역으로는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 컨트롤입니다.</span><span class="sxs-lookup"><span data-stu-id="7d844-111">Drag a control from the **Toolbox** onto the item template region of the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control.</span></span>  
  
     <span data-ttu-id="7d844-112">컨트롤에는 두 개의 사각형 영역을 참고 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d844-112">Note that the control has two rectangular regions.</span></span> <span data-ttu-id="7d844-113">내부 지역은 합니다 *항목 템플릿을*; 템플릿에 추가 된 컨트롤의 각 항목에 반복 됩니다는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 런타임 시 컨트롤입니다.</span><span class="sxs-lookup"><span data-stu-id="7d844-113">The inner region is the *item template*; controls added to the template will be repeated in each item in the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control at run time.</span></span> <span data-ttu-id="7d844-114">외부 지역은 합니다 *뷰포트*, 여기서 항목이 표시 될,이 영역에 추가 된 컨트롤을 런타임에 표시 되지 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7d844-114">The outer region is the *viewport*, where the items will be displayed; controls that are added to this region will not be displayed at run time.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7d844-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="7d844-115">See also</span></span>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>
- [<span data-ttu-id="7d844-116">DataRepeater 컨트롤 소개</span><span class="sxs-lookup"><span data-stu-id="7d844-116">Introduction to the DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)
- [<span data-ttu-id="7d844-117">DataRepeater 컨트롤 문제 해결</span><span class="sxs-lookup"><span data-stu-id="7d844-117">Troubleshooting the DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
- [<span data-ttu-id="7d844-118">방법: DataRepeater 컨트롤의 바인딩된 데이터 표시</span><span class="sxs-lookup"><span data-stu-id="7d844-118">How to: Display Bound Data in a DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-display-bound-data-in-a-datarepeater-control-visual-studio.md)
- [<span data-ttu-id="7d844-119">방법: 두 개의 DataRepeater 컨트롤 (Visual Studio)를 사용 하 여 마스터/세부 폼 만들기</span><span class="sxs-lookup"><span data-stu-id="7d844-119">How to: Create a Master/Detail Form by Using Two DataRepeater Controls (Visual Studio)</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-create-a-master-detail-form-by-using-two-datarepeater-controls.md)
- [<span data-ttu-id="7d844-120">방법: DataRepeater 컨트롤의 모양 변경</span><span class="sxs-lookup"><span data-stu-id="7d844-120">How to: Change the Appearance of a DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)
