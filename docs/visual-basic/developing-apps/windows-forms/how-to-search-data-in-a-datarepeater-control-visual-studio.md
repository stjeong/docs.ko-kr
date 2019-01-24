---
title: '방법: DataRepeater 컨트롤 (Visual Studio)의 데이터 검색'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataRepeater, implementing search
- DataRepeater, searching data
ms.assetid: a8ab5d17-b94f-43c4-8dd7-d0450226d73f
ms.openlocfilehash: 514e72afc9570071f57e385574456ff7d716bad7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54654388"
---
# <a name="how-to-search-data-in-a-datarepeater-control-visual-studio"></a>방법: DataRepeater 컨트롤 (Visual Studio)의 데이터 검색
사용 하는 경우는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 특정 레코드를 통해 사용자가 검색 하는 것이 좋습니다 레코드 수를 포함 하는 컨트롤입니다. 컨트롤에 데이터를 검색 하는 대신 기본 쿼리를 통해 검색을 구현할 수 있습니다 <xref:System.Windows.Forms.BindingSource>합니다. 항목이 있으면 사용할 수 있습니다는 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.CurrentItemIndex%2A> 속성을 항목을 선택 하 고 뷰로 스크롤할 수 있습니다.  
  
### <a name="to-implement-search"></a>검색을 구현 하려면  
  
1.  <xref:System.Windows.Forms.TextBox> 도구 상자 **에서** 컨트롤이 포함된 폼으로 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 컨트롤을 끌어 옵니다.  
  
2.  속성 창에서 **Name** 속성을 **SearchTextBox**로 변경합니다.  
  
3.  <xref:System.Windows.Forms.Button> 도구 상자 **에서** 컨트롤이 포함된 폼으로 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> 컨트롤을 끌어 옵니다.  
  
4.  속성 창에서 **Name** 속성을 **SearchButton**으로 변경합니다. **Text** 속성을 **Search**로 변경합니다.  
  
5.  <xref:System.Windows.Forms.Button> 컨트롤을 두 번 클릭하여 코드 편집기를 열고 `SearchButton_Click` 이벤트 처리기에 다음 코드를 추가합니다.  
  
     [!code-vb[VbPowerPacksDataRepeaterSearch#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-search-data-in-a-datarepeater-control-visual-studio_1.vb)]
     [!code-csharp[VbPowerPacksDataRepeaterSearch#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-search-data-in-a-datarepeater-control-visual-studio_1.cs)]  
  
     대체 *ProductsBindingSource* 이름의 <xref:System.Windows.Forms.BindingSource> 에 대 한 프로그램 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>, 바꾸고 *ProductID* 검색 하려는 필드의 이름입니다.  
  
## <a name="see-also"></a>참고자료
- <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>
- [DataRepeater 컨트롤 소개](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)
- [DataRepeater 컨트롤 문제 해결](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
- [방법: DataRepeater 컨트롤의 모양 변경](../../../visual-basic/developing-apps/windows-forms/how-to-change-the-appearance-of-a-datarepeater-control-visual-studio.md)
