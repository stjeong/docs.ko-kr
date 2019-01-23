---
title: '방법: (Visual Studio) 도형 간 탭 이동 사용'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Line control [Visual Basic], implementing tabbing
- Shape control [Visual Basic], implementing tabbing
ms.assetid: 09731b34-3900-4fcb-a9df-ce5280328433
ms.openlocfilehash: c47d94317008af57907b747e53bd13ae7ca229f5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54498283"
---
# <a name="how-to-enable-tabbing-between-shapes-visual-studio"></a><span data-ttu-id="86f40-102">방법: (Visual Studio) 도형 간 탭 이동 사용</span><span class="sxs-lookup"><span data-stu-id="86f40-102">How to: Enable Tabbing Between Shapes (Visual Studio)</span></span>
<span data-ttu-id="86f40-103">Line 및 shape 컨트롤 없는 `TabStop` 또는 `TabIndex` 있지만 속성을 설정할 수 있습니다. 여전히 간의 탭 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="86f40-103">Line and shape controls do not have `TabStop` or `TabIndex` properties, but you can still enable tabbing among them.</span></span> <span data-ttu-id="86f40-104">다음 예에서 셰이프; 사이의 탭은 탭 키와 CTRL 키를 눌러 단추 간을 이동 하는 TAB 키만 누르면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="86f40-104">In the following example, pressing both the CTRL and the TAB keys will tab between shapes; pressing only the TAB key will tab between the buttons.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="86f40-105">일부 Visual Studio 사용자 인터페이스 요소의 경우 다음 지침에 설명된 것과 다른 이름 또는 위치가 시스템에 표시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86f40-105">Your computer might show different names or locations for some of the Visual Studio user interface elements in the following instructions.</span></span> <span data-ttu-id="86f40-106">이러한 요소는 사용하는 Visual Studio 버전 및 설정에 따라 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="86f40-106">The Visual Studio edition that you have and the settings that you use determine these elements.</span></span> <span data-ttu-id="86f40-107">자세한 내용은 [Visual Studio IDE 개인 설정](/visualstudio/ide/personalizing-the-visual-studio-ide)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="86f40-107">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
## <a name="to-enable-tabbing-among-shapes"></a><span data-ttu-id="86f40-108">도형 간 탭 이동 사용 하도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="86f40-108">To enable tabbing among shapes</span></span>  
  
1.  <span data-ttu-id="86f40-109">세 개의 끌어 <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape> 컨트롤 및 두 개의 <xref:System.Windows.Forms.Button> 에서 제어 합니다 **도구 상자** 양식에 합니다.</span><span class="sxs-lookup"><span data-stu-id="86f40-109">Drag three <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape> controls and two <xref:System.Windows.Forms.Button> controls from the **Toolbox** to a form.</span></span>  
  
2.  <span data-ttu-id="86f40-110">에 **코드 편집기**에 추가 `Imports` 또는 `using` 모듈의 맨 위에 있는 문을:</span><span class="sxs-lookup"><span data-stu-id="86f40-110">In the **Code Editor**, add an `Imports` or `using` statement at the top of the module:</span></span>  
  
```vb  
Imports Microsoft.VisualBasic.PowerPacks  
```  
  
```csharp  
using Microsoft.VisualBasic.PowerPacks;  
```  

3.  <span data-ttu-id="86f40-111">이벤트 프로시저에 다음 코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="86f40-111">Add the following code in an event procedure:</span></span>  
  
[!code-csharp[VbPowerPacksTabbing#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-enable-tabbing-between-shapes-visual-studio_1.cs)]
[!code-vb[VbPowerPacksTabbing#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-enable-tabbing-between-shapes-visual-studio_1.vb)]  
  
4.  <span data-ttu-id="86f40-112">다음 코드를 추가 합니다 `Button1_PreviewKeyDown` 이벤트 프로시저:</span><span class="sxs-lookup"><span data-stu-id="86f40-112">Add the following code in the `Button1_PreviewKeyDown` event procedure:</span></span>  
  
[!code-csharp[VbPowerPacksTabbing#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-enable-tabbing-between-shapes-visual-studio_2.cs)]
[!code-vb[VbPowerPacksTabbing#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-enable-tabbing-between-shapes-visual-studio_2.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="86f40-113">참고자료</span><span class="sxs-lookup"><span data-stu-id="86f40-113">See also</span></span>
- [<span data-ttu-id="86f40-114">방법: OvalShape 및 RectangleShape 컨트롤을 사용 하 여 도형 그리기</span><span class="sxs-lookup"><span data-stu-id="86f40-114">How to: Draw Shapes with the OvalShape and RectangleShape Controls</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-draw-shapes-with-the-ovalshape-and-rectangleshape-controls.md)
- [<span data-ttu-id="86f40-115">방법: LineShape 컨트롤로 선 그리기</span><span class="sxs-lookup"><span data-stu-id="86f40-115">How to: Draw Lines with the LineShape Control</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-draw-lines-with-the-lineshape-control-visual-studio.md)
- [<span data-ttu-id="86f40-116">Line 및 Shape 컨트롤 소개</span><span class="sxs-lookup"><span data-stu-id="86f40-116">Introduction to the Line and Shape Controls</span></span>](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-line-and-shape-controls-visual-studio.md)
