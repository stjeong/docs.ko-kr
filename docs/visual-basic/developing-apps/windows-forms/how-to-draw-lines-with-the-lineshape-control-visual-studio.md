---
title: '방법: LineShape 컨트롤로 선 그리기 (Visual Studio)를 사용 하 여 선 그리기'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- LineShape control [Visual Basic]
- lines, drawing
ms.assetid: 83e71b4e-aa76-4f9b-b547-8704309fd1e5
ms.openlocfilehash: 46360c01dfaf2c6fe199725a9ecfba2248c72d6d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54596230"
---
# <a name="how-to-draw-lines-with-the-lineshape-control-visual-studio"></a><span data-ttu-id="b787d-102">방법: LineShape 컨트롤로 선 그리기 (Visual Studio)를 사용 하 여 선 그리기</span><span class="sxs-lookup"><span data-stu-id="b787d-102">How to: Draw Lines with the LineShape Control (Visual Studio)</span></span>
<span data-ttu-id="b787d-103">사용할 수는 <xref:Microsoft.VisualBasic.PowerPacks.LineShape> 디자인 타임 및 런타임에 폼 이나 컨테이너에서 가로, 세로 또는 대각선 그릴 컨트롤입니다.</span><span class="sxs-lookup"><span data-stu-id="b787d-103">You can use the <xref:Microsoft.VisualBasic.PowerPacks.LineShape> control to draw horizontal, vertical, or diagonal lines on a form or container, both at design time and at run time.</span></span>  
  
 <span data-ttu-id="b787d-104">**참고** 컴퓨터에서에서 표시할 수 있습니다 다른 이름이 나 위치 일부 Visual Studio 사용자 인터페이스 요소 다음 지침을 합니다.</span><span class="sxs-lookup"><span data-stu-id="b787d-104">**Note** Your computer might show different names or locations for some of the Visual Studio user interface elements in the following instructions.</span></span> <span data-ttu-id="b787d-105">이러한 요소는 사용하는 Visual Studio 버전 및 설정에 따라 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="b787d-105">The Visual Studio edition that you have and the settings that you use determine these elements.</span></span> <span data-ttu-id="b787d-106">자세한 내용은 [Visual Studio IDE 개인 설정](/visualstudio/ide/personalizing-the-visual-studio-ide)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b787d-106">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-draw-a-line-at-design-time"></a><span data-ttu-id="b787d-107">디자인 타임에 선 그리기</span><span class="sxs-lookup"><span data-stu-id="b787d-107">To draw a line at design time</span></span>  
  
1.  <span data-ttu-id="b787d-108">끌어를 <xref:Microsoft.VisualBasic.PowerPacks.LineShape> 에서 제어를 **Visual Basic PowerPacks** 탭에 **도구 상자** 을 폼 이나 컨테이너 컨트롤로 끌어 놓습니다.</span><span class="sxs-lookup"><span data-stu-id="b787d-108">Drag the <xref:Microsoft.VisualBasic.PowerPacks.LineShape> control from the **Visual Basic PowerPacks** tab in the **Toolbox** drag to a form or container control.</span></span>  
  
2.  <span data-ttu-id="b787d-109">크기 조정 끌어서 크기 및 줄 위치에 대 한 핸들을 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="b787d-109">Drag the sizing and move handles to size and position the line.</span></span>  
  
     <span data-ttu-id="b787d-110">크기 및 위치를 변경 하 여 줄 수도 있습니다는 `X1`, `X2`를 `Y1`, 및 `Y2` 속성에는 **속성** 창입니다.</span><span class="sxs-lookup"><span data-stu-id="b787d-110">You can also size and position the line by changing the `X1`, `X2`, `Y1`, and `Y2` properties in the **Properties** window.</span></span>  
  
3.  <span data-ttu-id="b787d-111">에 **속성** 창에서 필요에 따라 추가 속성을 설정할와 같은 `BorderStyle` 또는 `BorderColor` 줄의 모양을 변경 하려면.</span><span class="sxs-lookup"><span data-stu-id="b787d-111">In the **Properties** window, optionally set additional properties such as `BorderStyle` or `BorderColor` to change the appearance of the line.</span></span>  
  
### <a name="to-draw-a-line-at-run-time"></a><span data-ttu-id="b787d-112">런타임에 선을 그리려면</span><span class="sxs-lookup"><span data-stu-id="b787d-112">To draw a line at run time</span></span>  
  
1.  <span data-ttu-id="b787d-113">**프로젝트** 메뉴에서 **참조 추가**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b787d-113">On the **Project** menu, click **Add Reference**.</span></span>  
  
2.  <span data-ttu-id="b787d-114">에 **참조 추가** 대화 상자에서 **Microsoft.VisualBasic.PowerPacks.VS**를 클릭 하 고 **확인**합니다.</span><span class="sxs-lookup"><span data-stu-id="b787d-114">In the **Add Reference** dialog box, select **Microsoft.VisualBasic.PowerPacks.VS**, and then click **OK**.</span></span>  
  
3.  <span data-ttu-id="b787d-115">에 **코드 편집기**에 추가 `Imports` 또는 `using` 모듈의 맨 위에 있는 문을:</span><span class="sxs-lookup"><span data-stu-id="b787d-115">In the **Code Editor**, add an `Imports` or `using` statement at the top of the module:</span></span>  
  
```vb  
Imports Microsoft.VisualBasic.PowerPacks  
```  
  
```csharp  
using Microsoft.VisualBasic.PowerPacks;  
```  
  
4.  <span data-ttu-id="b787d-116">`Event` 프로시저에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b787d-116">Add the following code in an `Event` procedure:</span></span>  
  
     [!code-csharp[VbPowerPacksLine#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-draw-lines-with-the-lineshape-control-visual-studio_1.cs)]
     [!code-vb[VbPowerPacksLine#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-draw-lines-with-the-lineshape-control-visual-studio_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="b787d-117">참고자료</span><span class="sxs-lookup"><span data-stu-id="b787d-117">See also</span></span>
- <xref:Microsoft.VisualBasic.PowerPacks.LineShape>
- [<span data-ttu-id="b787d-118">Line 및 Shape 컨트롤 소개</span><span class="sxs-lookup"><span data-stu-id="b787d-118">Introduction to the Line and Shape Controls</span></span>](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-line-and-shape-controls-visual-studio.md)
- [<span data-ttu-id="b787d-119">방법: OvalShape 및 RectangleShape 컨트롤을 사용 하 여 도형 그리기</span><span class="sxs-lookup"><span data-stu-id="b787d-119">How to: Draw Shapes with the OvalShape and RectangleShape Controls</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-draw-shapes-with-the-ovalshape-and-rectangleshape-controls.md)
