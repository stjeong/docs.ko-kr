---
title: Windows Forms 컨트롤에서 이벤트 정의
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- events [Windows Forms], defining within Windows Forms custom controls
- custom controls [Windows Forms], events using code
ms.assetid: d89f1096-8061-42e2-a855-a1f053f1940a
ms.openlocfilehash: 60ae01ca63f895bfb1c7aabbe3337596cd13933d
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43732977"
---
# <a name="defining-an-event-in-windows-forms-controls"></a><span data-ttu-id="0ef28-102">Windows Forms 컨트롤에서 이벤트 정의</span><span class="sxs-lookup"><span data-stu-id="0ef28-102">Defining an Event in Windows Forms Controls</span></span>
<span data-ttu-id="0ef28-103">사용자 지정 이벤트를 정의 하는 방법에 대 한 자세한 내용은 참조 하세요 [이벤트](../../../../docs/standard/events/index.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef28-103">For details about defining custom events, see [Events](../../../../docs/standard/events/index.md).</span></span> <span data-ttu-id="0ef28-104">연결된 데이터가 없는 이벤트를 정의하는 경우에는 이벤트 데이터의 기본 형식인 <xref:System.EventArgs>를 사용하고 이벤트 대리자로 <xref:System.EventHandler>를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef28-104">If you define an event that does not have any associated data, use the base type for event data, <xref:System.EventArgs>, and use <xref:System.EventHandler> as the event delegate.</span></span> <span data-ttu-id="0ef28-105">모든 작업을 수행 하는 이벤트 멤버 및 보호 된 정의 `On` *EventName* 이벤트를 발생 시키는 메서드.</span><span class="sxs-lookup"><span data-stu-id="0ef28-105">All that remains to do is to define an event member and a protected `On`*EventName* method that raises the event.</span></span>  
  
 <span data-ttu-id="0ef28-106">다음 코드 조각은 `FlashTrackBar` 사용자 지정 컨트롤이 사용자 지정 이벤트 `ValueChanged`를 정의하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0ef28-106">The following code fragment shows how the `FlashTrackBar` custom control defines a custom event, `ValueChanged`.</span></span> <span data-ttu-id="0ef28-107">에 대 한 전체 코드는 `FlashTrackBar` 샘플을 참조 하십시오 합니다 [방법: 만들기는 Windows Forms 컨트롤 진행률을 보여 주는](../../../../docs/framework/winforms/controls/how-to-create-a-windows-forms-control-that-shows-progress.md).</span><span class="sxs-lookup"><span data-stu-id="0ef28-107">For the complete code for the `FlashTrackBar` sample, see the [How to: Create a Windows Forms Control That Shows Progress](../../../../docs/framework/winforms/controls/how-to-create-a-windows-forms-control-that-shows-progress.md).</span></span>  
  
```vb  
Option Explicit  
Option Strict  
  
Imports System  
Imports System.Windows.Forms  
Imports System.Drawing  
  
Public Class FlashTrackBar  
   Inherits Control  
  
   ' The event does not have any data, so EventHandler is adequate   
   ' as the event delegate.          
   ' Define the event member using the event keyword.  
   ' In this case, for efficiency, the event is defined   
   ' using the event property construct.  
   Public Event ValueChanged As EventHandler  
   ' The protected method that raises the ValueChanged   
   ' event when the value has actually   
   ' changed. Derived controls can override this method.    
   Protected Overridable Sub OnValueChanged(e As EventArgs)  
      RaiseEvent ValueChanged(Me, e)  
   End Sub  
End Class  
```  
  
```csharp  
using System;  
using System.Windows.Forms;  
using System.Drawing;  
  
public class FlashTrackBar : Control {  
   // The event does not have any data, so EventHandler is adequate   
   // as the event delegate.  
   private EventHandler onValueChanged;  
   // Define the event member using the event keyword.  
   // In this case, for efficiency, the event is defined   
   // using the event property construct.  
   public event EventHandler ValueChanged {  
            add {  
                onValueChanged += value;  
            }  
            remove {  
                onValueChanged -= value;  
            }  
        }  
   // The protected method that raises the ValueChanged  
   // event when the value has actually   
   // changed. Derived controls can override this method.    
   protected virtual void OnValueChanged(EventArgs e) 
   {  
       ValueChanged?.Invoke(this, e);  
   }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="0ef28-108">참고자료</span><span class="sxs-lookup"><span data-stu-id="0ef28-108">See also</span></span>

- [<span data-ttu-id="0ef28-109">Windows Forms 컨트롤의 이벤트</span><span class="sxs-lookup"><span data-stu-id="0ef28-109">Events in Windows Forms Controls</span></span>](../../../../docs/framework/winforms/controls/events-in-windows-forms-controls.md)
- [<span data-ttu-id="0ef28-110">이벤트</span><span class="sxs-lookup"><span data-stu-id="0ef28-110">Events</span></span>](../../../../docs/standard/events/index.md)
