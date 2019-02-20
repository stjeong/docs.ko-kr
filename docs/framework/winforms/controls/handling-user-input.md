---
title: 사용자 입력 처리
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom controls [Windows Forms], user input using code
- custom controls [Windows Forms], keyboard events using code
- custom controls [Windows Forms], mouse events using code
ms.assetid: d9b12787-86f6-4022-8e0f-e12d312c4af2
ms.openlocfilehash: 8c6319929d4b419cc0a2e1cfd097bfae7d997120
ms.sourcegitcommit: acd8ed14fe94e9d4e3a7fb685fe83d05e941073c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/20/2019
ms.locfileid: "56443008"
---
# <a name="handling-user-input"></a><span data-ttu-id="4889b-102">사용자 입력 처리</span><span class="sxs-lookup"><span data-stu-id="4889b-102">Handling User Input</span></span>
<span data-ttu-id="4889b-103">이 항목에서 제공 하는 기본 키보드 및 마우스 이벤트를 설명 합니다. <xref:System.Windows.Forms.Control?displayProperty=nameWithType>합니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-103">This topic describes the main keyboard and mouse events provided by <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span></span> <span data-ttu-id="4889b-104">이벤트를 처리할 경우 컨트롤 작성자는 이벤트에 대리자를 연결하는 대신 보호된 `On`*EventName* 메서드를 재정의해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-104">When handling an event, control authors should override the protected `On`*EventName* method rather than attaching a delegate to the event.</span></span> <span data-ttu-id="4889b-105">이벤트의 검토는 [구성 요소에서 이벤트 발생](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/sh2e3k5z(v=vs.120))을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4889b-105">For a review of events, see [Raising Events from a Component](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/sh2e3k5z(v=vs.120)).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4889b-106">기본 클래스의 인스턴스는 이벤트와 연결 된 데이터가 없는 경우 <xref:System.EventArgs> 인수로 전달 되는 `On` *EventName* 메서드.</span><span class="sxs-lookup"><span data-stu-id="4889b-106">If there is no data associated with an event, an instance of the base class <xref:System.EventArgs> is passed as an argument to the `On`*EventName* method.</span></span>  
  
## <a name="keyboard-events"></a><span data-ttu-id="4889b-107">키보드 이벤트</span><span class="sxs-lookup"><span data-stu-id="4889b-107">Keyboard Events</span></span>  
 <span data-ttu-id="4889b-108">컨트롤에서 처리할 수 있는 일반적인 키보드 이벤트 <xref:System.Windows.Forms.Control.KeyDown>, <xref:System.Windows.Forms.Control.KeyPress>, 및 <xref:System.Windows.Forms.Control.KeyUp>합니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-108">The common keyboard events that your control can handle are <xref:System.Windows.Forms.Control.KeyDown>, <xref:System.Windows.Forms.Control.KeyPress>, and <xref:System.Windows.Forms.Control.KeyUp>.</span></span>  
  
|<span data-ttu-id="4889b-109">이벤트 이름</span><span class="sxs-lookup"><span data-stu-id="4889b-109">Event Name</span></span>|<span data-ttu-id="4889b-110">재정의할 메서드</span><span class="sxs-lookup"><span data-stu-id="4889b-110">Method to Override</span></span>|<span data-ttu-id="4889b-111">이벤트 설명</span><span class="sxs-lookup"><span data-stu-id="4889b-111">Description of Event</span></span>|  
|----------------|------------------------|--------------------------|  
|`KeyDown`|`void OnKeyDown(KeyEventArgs)`|<span data-ttu-id="4889b-112">키를 처음 누를 때 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-112">Raised only when a key is initially pressed.</span></span>|  
|`KeyPress`|`void OnKeyPress`<br /><br /> `(KeyPressEventArgs)`|<span data-ttu-id="4889b-113">키를 누를 때마다 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-113">Raised every time a key is pressed.</span></span> <span data-ttu-id="4889b-114">키를 누르고 있으면는 <xref:System.Windows.Forms.Control.KeyPress> 이벤트가 운영 체제에서 정의한 반복 속도로 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-114">If a key is held down, a <xref:System.Windows.Forms.Control.KeyPress> event is raised at the repeat rate defined by the operating system.</span></span>|  
|`KeyUp`|`void OnKeyUp(KeyEventArgs)`|<span data-ttu-id="4889b-115">키를 놓으면 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-115">Raised when a key is released.</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="4889b-116">키보드 입력 처리는 앞의 테이블에서 이벤트를 재정의하는 것보다 더 복잡하며 이 항목의 범위를 벗어납니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-116">Handling keyboard input is considerably more complex than overriding the events in the preceding table and is beyond the scope of this topic.</span></span> <span data-ttu-id="4889b-117">자세한 내용은 [Windows Forms의 사용자 입력](../../../../docs/framework/winforms/user-input-in-windows-forms.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4889b-117">For more information, see [User Input in Windows Forms](../../../../docs/framework/winforms/user-input-in-windows-forms.md).</span></span>  
  
## <a name="mouse-events"></a><span data-ttu-id="4889b-118">마우스 이벤트</span><span class="sxs-lookup"><span data-stu-id="4889b-118">Mouse Events</span></span>  
 <span data-ttu-id="4889b-119">컨트롤에서 처리할 수는 마우스 이벤트는 <xref:System.Windows.Forms.Control.MouseDown>, <xref:System.Windows.Forms.Control.MouseEnter>를 <xref:System.Windows.Forms.Control.MouseHover>를 <xref:System.Windows.Forms.Control.MouseLeave>를 <xref:System.Windows.Forms.Control.MouseMove>, 및 <xref:System.Windows.Forms.Control.MouseUp>합니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-119">The mouse events that your control can handle are <xref:System.Windows.Forms.Control.MouseDown>, <xref:System.Windows.Forms.Control.MouseEnter>, <xref:System.Windows.Forms.Control.MouseHover>, <xref:System.Windows.Forms.Control.MouseLeave>, <xref:System.Windows.Forms.Control.MouseMove>, and <xref:System.Windows.Forms.Control.MouseUp>.</span></span>  
  
|<span data-ttu-id="4889b-120">이벤트 이름</span><span class="sxs-lookup"><span data-stu-id="4889b-120">Event Name</span></span>|<span data-ttu-id="4889b-121">재정의할 메서드</span><span class="sxs-lookup"><span data-stu-id="4889b-121">Method to Override</span></span>|<span data-ttu-id="4889b-122">이벤트 설명</span><span class="sxs-lookup"><span data-stu-id="4889b-122">Description of Event</span></span>|  
|----------------|------------------------|--------------------------|  
|`MouseDown`|`void OnMouseDown(MouseEventArgs)`|<span data-ttu-id="4889b-123">포인터가 컨트롤 위에 있을 때 마우스 단추를 누르면 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-123">Raised when the mouse button is pressed while the pointer is over the control.</span></span>|  
|`MouseEnter`|`void OnMouseEnter(EventArgs)`|<span data-ttu-id="4889b-124">포인터가 컨트롤의 지역에 먼저 들어가면 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-124">Raised when the pointer first enters the region of the control.</span></span>|  
|`MouseHover`|`void OnMouseHover(EventArgs)`|<span data-ttu-id="4889b-125">포인터로 컨트롤을 가리키면 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-125">Raised when the pointer hovers over the control.</span></span>|  
|`MouseLeave`|`void OnMouseLeave(EventArgs)`|<span data-ttu-id="4889b-126">포인터가 컨트롤의 지역을 벗어나면 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-126">Raised when the pointer leaves the region of the control.</span></span>|  
|`MouseMove`|`void OnMouseMove(MouseEventArgs)`|<span data-ttu-id="4889b-127">포인터가 컨트롤의 지역에서 이동하면 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-127">Raised when the pointer moves in the region of the control.</span></span>|  
|`MouseUp`|`void OnMouseUp(MouseEventArgs)`|<span data-ttu-id="4889b-128">포인터가 컨트롤 위에 있거나 포인터가 컨트롤의 지역을 벗어나는 동안 마우스 단추를 놓으면 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-128">Raised when the mouse button is released while the pointer is over the control or the pointer leaves the region of the control.</span></span>|  
  
 <span data-ttu-id="4889b-129">다음 코드 조각은 재정의 하는 예를 보여 줍니다.는 <xref:System.Windows.Forms.Control.MouseDown> 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-129">The following code fragment shows an example of overriding the <xref:System.Windows.Forms.Control.MouseDown> event.</span></span>  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#7](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#7)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#7](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#7)]  
  
 <span data-ttu-id="4889b-130">다음 코드 조각은 재정의 하는 예를 보여 줍니다.는 <xref:System.Windows.Forms.Control.MouseMove> 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-130">The following code fragment shows an example of overriding the <xref:System.Windows.Forms.Control.MouseMove> event.</span></span>  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#8](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#8)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#8](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#8)]  
  
 <span data-ttu-id="4889b-131">다음 코드 조각은 재정의 하는 예를 보여 줍니다.는 <xref:System.Windows.Forms.Control.MouseUp> 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-131">The following code fragment shows an example of overriding the <xref:System.Windows.Forms.Control.MouseUp> event.</span></span>  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#9](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#9)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#9](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#9)]  
  
 <span data-ttu-id="4889b-132">에 대 한 전체 소스 코드를 `FlashTrackBar` 샘플을 참조 하십시오 [방법: 진행률을 보여 주는 Windows Forms 컨트롤 만들기](../../../../docs/framework/winforms/controls/how-to-create-a-windows-forms-control-that-shows-progress.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="4889b-132">For the complete source code for the `FlashTrackBar` sample, see [How to: Create a Windows Forms Control That Shows Progress](../../../../docs/framework/winforms/controls/how-to-create-a-windows-forms-control-that-shows-progress.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4889b-133">참고자료</span><span class="sxs-lookup"><span data-stu-id="4889b-133">See also</span></span>
- [<span data-ttu-id="4889b-134">Windows Forms 컨트롤의 이벤트</span><span class="sxs-lookup"><span data-stu-id="4889b-134">Events in Windows Forms Controls</span></span>](../../../../docs/framework/winforms/controls/events-in-windows-forms-controls.md)
- [<span data-ttu-id="4889b-135">이벤트 정의</span><span class="sxs-lookup"><span data-stu-id="4889b-135">Defining an Event</span></span>](../../../../docs/framework/winforms/controls/defining-an-event-in-windows-forms-controls.md)
- [<span data-ttu-id="4889b-136">이벤트</span><span class="sxs-lookup"><span data-stu-id="4889b-136">Events</span></span>](../../../../docs/standard/events/index.md)
- [<span data-ttu-id="4889b-137">Windows Forms에 사용자 입력</span><span class="sxs-lookup"><span data-stu-id="4889b-137">User Input in Windows Forms</span></span>](../../../../docs/framework/winforms/user-input-in-windows-forms.md)
