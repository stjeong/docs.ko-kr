---
title: '방법: 액세스 관련 항목에는 Windows Forms ComboBox, ListBox 또는 CheckedListBox 컨트롤'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ComboBox control [Windows Forms], accessing items
- ListBox control [Windows Forms], returning item information
- list boxes [Windows Forms], accessing items
- ListBox control [Windows Forms], accessing items
- combo boxes [Windows Forms], accessing items
- CheckedListBox control [Windows Forms], accessing items
ms.assetid: 1216742f-bcf9-4ff8-8a62-d7c9053c2b96
ms.openlocfilehash: b6478c24550f9f32ea75899521f7aa610ef12955
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54656702"
---
# <a name="how-to-access-specific-items-in-a-windows-forms-combobox-listbox-or-checkedlistbox-control"></a><span data-ttu-id="de5f4-102">방법: 액세스 관련 항목에는 Windows Forms ComboBox, ListBox 또는 CheckedListBox 컨트롤</span><span class="sxs-lookup"><span data-stu-id="de5f4-102">How to: Access Specific Items in a Windows Forms ComboBox, ListBox, or CheckedListBox Control</span></span>
<span data-ttu-id="de5f4-103">Windows Forms 콤보 상자, 목록 상자 또는 선택된 목록 상자에서 특정 항목에 액세스 하기 필수 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="de5f4-103">Accessing specific items in a Windows Forms combo box, list box, or checked list box is an essential task.</span></span> <span data-ttu-id="de5f4-104">이 통해 프로그래밍 방식으로 지정된 된 위치에서 목록에는 무엇이 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="de5f4-104">It enables you to programmatically determine what is in a list, at any given position.</span></span>  
  
### <a name="to-access-a-specific-item"></a><span data-ttu-id="de5f4-105">특정 항목에 액세스 하려면</span><span class="sxs-lookup"><span data-stu-id="de5f4-105">To access a specific item</span></span>  
  
1.  <span data-ttu-id="de5f4-106">쿼리는 `Items` 특정 항목의 인덱스를 사용 하 여 컬렉션:</span><span class="sxs-lookup"><span data-stu-id="de5f4-106">Query the `Items` collection using the index of the specific item:</span></span>  
  
    ```vb  
    Private Function GetItemText(i As Integer) As String  
       ' Return the text of the item using the index:  
       Return ComboBox1.Items(i).ToString  
    End Function  
    ```  
  
    ```csharp  
    private string GetItemText(int i)  
    {  
       // Return the text of the item using the index:  
       return (comboBox1.Items[i].ToString());  
    }  
    ```  
  
    ```cpp  
    private:  
       String^ GetItemText(int i)  
       {  
          // Return the text of the item using the index:  
          return (comboBox1->Items->Item[i]->ToString());  
       }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="de5f4-107">참고자료</span><span class="sxs-lookup"><span data-stu-id="de5f4-107">See also</span></span>
- <xref:System.Windows.Forms.ComboBox>
- <xref:System.Windows.Forms.ListBox>
- <xref:System.Windows.Forms.CheckedListBox>
- [<span data-ttu-id="de5f4-108">옵션 목록 표시에 사용된 Windows Forms 컨트롤</span><span class="sxs-lookup"><span data-stu-id="de5f4-108">Windows Forms Controls Used to List Options</span></span>](../../../../docs/framework/winforms/controls/windows-forms-controls-used-to-list-options.md)
