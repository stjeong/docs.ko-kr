---
title: DataRepeater 컨트롤의 가상 모드(Visual Studio)
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- virtual data binding [Visual Basic]
- DataRepeater
- DataRepeater, virtual mode
ms.assetid: 5fb805dc-2d8b-4139-b1e3-86e4c2667221
ms.openlocfilehash: 3988c16746606de9f20f9a66b87539b6cea04758
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54700808"
---
# <a name="virtual-mode-in-the-datarepeater-control-visual-studio"></a>DataRepeater 컨트롤의 가상 모드(Visual Studio)
대량의의 표 형식 데이터를 표시 하려는 경우는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 컨트롤을 설정 하 여 성능을 향상 시킬 수 있습니다는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.VirtualMode%2A> 속성을 `True` 명시적으로 해당 데이터 소스를 사용 하 여 컨트롤의 상호 작용을 관리 합니다. <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 제어 하 여 데이터 소스와 상호 작용 하 고 런타임에 필요에 따라 데이터를 표시 하려면 처리할 수 있는 몇 가지 이벤트를 제공 합니다.  
  
## <a name="how-virtual-mode-works"></a>가상 모드 작동 방식  
 에 대 한 가장 일반적인 시나리오를 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 컨트롤의 자식 컨트롤을 바인딩하는 것을 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate%2A> 에 대 한 데이터 디자인 타임에 원본 및 허용를 <xref:System.Windows.Forms.BindingSource> 앞뒤로 필요에 따라 데이터를 전달 하 합니다. 가상 모드를 사용 하면 컨트롤을 데이터 원본에 바인딩되지 않은 이며 데이터 전달 됩니다 앞뒤로 기본 데이터 원본으로 런타임 시.  
  
 경우는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.VirtualMode%2A> 속성이 `True`에서 컨트롤을 추가 하 여 사용자 인터페이스를 만들는 **도구 상자** 바인딩된 컨트롤을 추가 하는 대신를 **데이터 원본** 창.  
  
 컨트롤에서 컨트롤에 따라 이벤트가 발생 하 고 데이터의 표시를 처리 하는 코드를 추가 해야 합니다. 새 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem> 스크롤될, 합니다 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemValueNeeded> 이벤트가 각 컨트롤에 한 번씩 발생 하 고 각 컨트롤에 대 한 값을 제공 해야는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemValueNeeded> 이벤트 처리기입니다.  
  
 사용자가 컨트롤 중 하나에서 데이터가 변경 되 면는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemValuePushed> 이벤트가 발생 하 고 데이터의 유효성을 검사 하 고 데이터 원본에 저장 해야 합니다.  
  
 사용자는 새 항목을 추가 하는 경우는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.NewItemNeeded> 이벤트가 발생 합니다. 이 이벤트 처리기를 사용 하 여 데이터 원본에 새 레코드를 만듭니다. 의도 하지 않은 변경 내용이 방지 하려면 모니터링 해야 합니다 <xref:System.Windows.Forms.Control.KeyDown> 각 컨트롤 및 호출에 대 한 이벤트 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.CancelEdit%2A> ESC 키를 누를 경우.  
  
 데이터 소스가 변경 하는 경우 새로 고칠 수 있습니다 합니다 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 호출 하 여 컨트롤을 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.BeginResetItemTemplate%2A> 및 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.EndResetItemTemplate%2A> 메서드. 순서에서 두 메서드를 호출 해야 합니다.  
  
 에 대 한 이벤트 처리기를 구현 해야 하는 마지막으로 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemsRemoved> 항목을 삭제 하는 경우 및 필요에 따라 발생 하는 이벤트를 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.UserDeletingItems> 및 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.UserDeletedItems> DELETE 키를 눌러 항목을 삭제 하는 사용자 때마다 발생 하는 이벤트입니다.  
  
## <a name="implementing-virtual-mode"></a>가상 모드 구현  
 가상 모드 구현 하는 데 필요한 단계는 다음과가 같습니다.  
  
#### <a name="to-implement-virtual-mode"></a>가상 모드 구현  
  
1.  끌어서를 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 에서 제어 합니다 **Visual Basic PowerPacks** 탭에 **도구 상자** 폼 이나 컨테이너 컨트롤에. <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.VirtualMode%2A> 속성을 `True`으로 설정합니다.  
  
2.  컨트롤을 끌어 합니다 **도구 상자** 의 항목 템플릿 영역 (위쪽 영역)으로 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 컨트롤입니다. 각 필드를 표시 하려는 데이터 원본에 대해 하나의 제어를 해야 합니다.  
  
3.  에 대 한 처리기를 구현 합니다 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemValueNeeded> 각 컨트롤에 대 한 값을 제공 하는 이벤트입니다. 이 이벤트는 새 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem> 스크롤될 합니다. 코드는 다음 예와 같이, 라는 데이터 원본에 대 한 인 `Employees`합니다.  
  
     [!code-vb[VbPowerPacksDataRepeaterVirtualMode#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/virtual-mode-in-the-datarepeater-control-visual-studio_1.vb)]
     [!code-csharp[VbPowerPacksDataRepeaterVirtualMode#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/virtual-mode-in-the-datarepeater-control-visual-studio_1.cs)]  
  
4.  에 대 한 처리기를 구현 합니다 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemValuePushed> 이벤트 데이터를 저장 합니다. 이 이벤트는 사용자의 자식 컨트롤에 변경 내용이 커밋될 때 발생 합니다 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem>합니다. 코드는 다음 예와 같이, 라는 데이터 원본에 대 한 인 `Employees`합니다.  
  
     [!code-vb[VbPowerPacksDataRepeaterVirtualMode#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/virtual-mode-in-the-datarepeater-control-visual-studio_2.vb)]
     [!code-csharp[VbPowerPacksDataRepeaterVirtualMode#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/virtual-mode-in-the-datarepeater-control-visual-studio_2.cs)]  
  
5.  각 자식 컨트롤에 대 한 처리기를 구현 <xref:System.Windows.Forms.Control.KeyDown> 이벤트 및 ESC 키를 모니터링 합니다. 호출을 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.CancelEdit%2A> 방지 하기 위해 메서드를 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemValuePushed> 이벤트가 발생 하지. 코드에는 다음 예제와 유사 합니다.  
  
     [!code-vb[VbPowerPacksDataRepeaterVirtualMode#3](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/virtual-mode-in-the-datarepeater-control-visual-studio_3.vb)]
     [!code-csharp[VbPowerPacksDataRepeaterVirtualMode#3](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/virtual-mode-in-the-datarepeater-control-visual-studio_3.cs)]  
  
6.  에 대 한 처리기를 구현 합니다 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.NewItemNeeded> 이벤트입니다. 이 이벤트는 사용자가 새 항목이 추가 된 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 컨트롤입니다. 코드는 다음 예와 같이, 라는 데이터 원본에 대 한 인 `Employees`합니다.  
  
     [!code-vb[VbPowerPacksDataRepeaterVirtualMode#4](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/virtual-mode-in-the-datarepeater-control-visual-studio_4.vb)]
     [!code-csharp[VbPowerPacksDataRepeaterVirtualMode#4](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/virtual-mode-in-the-datarepeater-control-visual-studio_4.cs)]  
  
7.  에 대 한 처리기를 구현 합니다 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemsRemoved> 이벤트입니다. 이 이벤트는 사용자는 기존 항목을 삭제할 때 발생 합니다. 코드는 다음 예와 같이, 라는 데이터 원본에 대 한 인 `Employees`합니다.  
  
     [!code-vb[VbPowerPacksDataRepeaterVirtualMode#5](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/virtual-mode-in-the-datarepeater-control-visual-studio_5.vb)]
     [!code-csharp[VbPowerPacksDataRepeaterVirtualMode#5](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/virtual-mode-in-the-datarepeater-control-visual-studio_5.cs)]  
  
8.  처리기에 대 한 제어 수준 유효성 검사를 위해 필요에 따라 구현 하는 <xref:System.Windows.Forms.Control.Validating> 자식 컨트롤의 이벤트입니다. 코드에는 다음 예제와 유사 합니다.  
  
     [!code-vb[VbPowerPacksDataRepeaterVirtualMode#6](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/virtual-mode-in-the-datarepeater-control-visual-studio_6.vb)]
     [!code-csharp[VbPowerPacksDataRepeaterVirtualMode#6](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/virtual-mode-in-the-datarepeater-control-visual-studio_6.cs)]  
  
## <a name="see-also"></a>참고자료
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemValuePushed>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.NewItemNeeded>
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemValueNeeded>
- [DataRepeater 컨트롤 소개](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)
