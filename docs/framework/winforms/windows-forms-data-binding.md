---
title: Windows Forms 데이터 바인딩
ms.date: 03/30/2017
helpviewer_keywords:
- data [Windows Forms]
- Windows Forms, data binding
- data [Windows Forms], architecture
- Windows Forms controls, data binding
ms.assetid: c3826d8e-ea25-4ad4-a669-45bfb19192aa
ms.openlocfilehash: cfb4c59c76142420f479b0b16a6d80317e98d159
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43486012"
---
# <a name="windows-forms-data-binding"></a><span data-ttu-id="d1127-102">Windows Forms 데이터 바인딩</span><span class="sxs-lookup"><span data-stu-id="d1127-102">Windows Forms Data Binding</span></span>
<span data-ttu-id="d1127-103">Windows Forms의 데이터 바인딩은 폼의 컨트롤에서 데이터 소스의 정보를 표시하고 변경하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-103">Data binding in Windows Forms gives you the means to display and make changes to information from a data source in controls on the form.</span></span> <span data-ttu-id="d1127-104">기존의 데이터 소스뿐 아니라 데이터를 포함하는 거의 모든 구조에 바인딩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-104">You can bind to both traditional data sources as well as almost any structure that contains data.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="d1127-105">섹션 내용</span><span class="sxs-lookup"><span data-stu-id="d1127-105">In This Section</span></span>  
 [<span data-ttu-id="d1127-106">데이터 바인딩 및 Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d1127-106">Data Binding and Windows Forms</span></span>](../../../docs/framework/winforms/data-binding-and-windows-forms.md)  
 <span data-ttu-id="d1127-107">Windows Forms의 데이터 바인딩에 대한 개요를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-107">Provides an overview of data binding in Windows Forms.</span></span>  
  
 [<span data-ttu-id="d1127-108">Windows Forms에서 지원하는 데이터 소스</span><span class="sxs-lookup"><span data-stu-id="d1127-108">Data Sources Supported by Windows Forms</span></span>](../../../docs/framework/winforms/data-sources-supported-by-windows-forms.md)  
 <span data-ttu-id="d1127-109">Windows Forms에서 사용할 수 있는 데이터 소스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-109">Describes the data sources that can be used with Windows Forms.</span></span>  
  
 [<span data-ttu-id="d1127-110">데이터 바인딩과 관련된 인터페이스</span><span class="sxs-lookup"><span data-stu-id="d1127-110">Interfaces Related to Data Binding</span></span>](../../../docs/framework/winforms/interfaces-related-to-data-binding.md)  
 <span data-ttu-id="d1127-111">Windows Forms 데이터 바인딩과 함께 사용되는 여러 인터페이스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-111">Describes several of the interfaces used with Windows Forms data binding.</span></span>  
  
 [<span data-ttu-id="d1127-112">방법: Windows Forms에서 데이터 탐색</span><span class="sxs-lookup"><span data-stu-id="d1127-112">How to: Navigate Data in Windows Forms</span></span>](../../../docs/framework/winforms/how-to-navigate-data-in-windows-forms.md)  
 <span data-ttu-id="d1127-113">데이터 소스의 항목을 탐색하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-113">Shows how to navigate through items in a data source.</span></span>  
  
 [<span data-ttu-id="d1127-114">Windows Forms 데이터 바인딩의 변경 알림</span><span class="sxs-lookup"><span data-stu-id="d1127-114">Change Notification in Windows Forms Data Binding</span></span>](../../../docs/framework/winforms/change-notification-in-windows-forms-data-binding.md)  
 <span data-ttu-id="d1127-115">Windows Forms 데이터 바인딩에 대한 다양한 유형의 변경 알림을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-115">Describes different types of change notification for Windows Forms data binding.</span></span>  
  
 [<span data-ttu-id="d1127-116">방법: INotifyPropertyChanged 인터페이스 구현</span><span class="sxs-lookup"><span data-stu-id="d1127-116">How to: Implement the INotifyPropertyChanged Interface</span></span>](../../../docs/framework/winforms/how-to-implement-the-inotifypropertychanged-interface.md)  
 <span data-ttu-id="d1127-117"><xref:System.ComponentModel.INotifyPropertyChanged> 인터페이스를 구현하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-117">Shows how to implement the <xref:System.ComponentModel.INotifyPropertyChanged> interface.</span></span> <span data-ttu-id="d1127-118">인터페이스는 비즈니스 개체의 속성 변경 내용을 바인딩된 컨트롤에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-118">The interface  communicates to a bound control the property changes on a business object</span></span>  
  
 [<span data-ttu-id="d1127-119">방법: PropertyNameChanged 패턴 적용</span><span class="sxs-lookup"><span data-stu-id="d1127-119">How to: Apply the PropertyNameChanged Pattern</span></span>](../../../docs/framework/winforms/how-to-apply-the-propertynamechanged-pattern.md)  
 <span data-ttu-id="d1127-120">적용 하는 방법을 보여 줍니다 합니다 *PropertyName*패턴을 Windows Forms 사용자 정의 컨트롤의 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-120">Shows how to apply the *PropertyName*Changed pattern to properties of a Windows Forms user control.</span></span>  
  
 [<span data-ttu-id="d1127-121">방법: ITypedList 인터페이스 구현</span><span class="sxs-lookup"><span data-stu-id="d1127-121">How to: Implement the ITypedList Interface</span></span>](../../../docs/framework/winforms/how-to-implement-the-itypedlist-interface.md)  
 <span data-ttu-id="d1127-122"><xref:System.ComponentModel.ITypedList> 인터페이스를 구현하여 바인딩 가능한 목록에 대한 스키마 검색을 사용하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-122">Shows how to enable discovery of the schema for a bindable list by implementing the <xref:System.ComponentModel.ITypedList> interface.</span></span>  
  
 [<span data-ttu-id="d1127-123">방법: IListSource 인터페이스 구현</span><span class="sxs-lookup"><span data-stu-id="d1127-123">How to: Implement the IListSource Interface</span></span>](../../../docs/framework/winforms/how-to-implement-the-ilistsource-interface.md)  
 <span data-ttu-id="d1127-124"><xref:System.ComponentModel.IListSource> 인터페이스를 구현하여 <xref:System.Collections.IList>를 구현하지 않지만 다른 위치에서 목록을 제공하는 바인딩 가능한 클래스를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-124">Shows how to implement the <xref:System.ComponentModel.IListSource> interface to create a bindable class does not implement <xref:System.Collections.IList>, but provides a list from another location.</span></span>  
  
 [<span data-ttu-id="d1127-125">방법: 동일한 데이터 소스에 바인딩된 여러 컨트롤의 동기화 상태가 유지되도록 설정</span><span class="sxs-lookup"><span data-stu-id="d1127-125">How to: Ensure Multiple Controls Bound to the Same Data Source Remain Synchronized</span></span>](../../../docs/framework/winforms/multiple-controls-bound-to-data-source-synchronized.md)  
 <span data-ttu-id="d1127-126"><xref:System.Windows.Forms.BindingSource.BindingComplete> 이벤트를 처리하여 데이터 소스에 바인딩된 모든 컨트롤의 동기화 상태가 유지되도록 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-126">Shows how to handle the <xref:System.Windows.Forms.BindingSource.BindingComplete> event to ensure all controls bound to a data source remain synchronized.</span></span>  
  
 [<span data-ttu-id="d1127-127">방법: 자식 테이블에서 선택된 행이 올바른 위치에 유지되도록 설정</span><span class="sxs-lookup"><span data-stu-id="d1127-127">How to: Ensure the Selected Row in a Child Table Remains at the Correct Position</span></span>](../../../docs/framework/winforms/ensure-the-selected-row-in-a-child-table-correct.md)  
 <span data-ttu-id="d1127-128">부모 테이블의 필드가 변경될 때 자식 테이블의 선택된 행이 변경되지 않도록 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-128">Shows how to ensure the selected row of a child table does not change, when a change is made to a field of the parent table.</span></span>  
  
 <span data-ttu-id="d1127-129">도 참조 하세요 [인터페이스와 관련 된 데이터 바인딩](https://msdn.microsoft.com/library/41e17s4b\(v=vs.110\))를 [방법: Windows Forms에서 데이터 이동](https://msdn.microsoft.com/library/b63ha24w\(v=vs.110\))를 [하는 방법: Windows Form에 단순 바인딩된 컨트롤 만들기](https://msdn.microsoft.com/library/sw223a62\(v=vs.110\))합니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-129">Also see [Interfaces Related to Data Binding](https://msdn.microsoft.com/library/41e17s4b\(v=vs.110\)), [How to: Navigate Data in Windows Forms](https://msdn.microsoft.com/library/b63ha24w\(v=vs.110\)), [How to: Create a Simple-Bound Control on a Windows Form](https://msdn.microsoft.com/library/sw223a62\(v=vs.110\)).</span></span>  
  
## <a name="reference"></a><span data-ttu-id="d1127-130">참조</span><span class="sxs-lookup"><span data-stu-id="d1127-130">Reference</span></span>  
 <xref:System.Windows.Forms.Binding?displayProperty=nameWithType>  
 <span data-ttu-id="d1127-131">바인딩 가능한 구성 요소와 데이터 소스 간의 바인딩을 나타내는 클래스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-131">Describes the class that represents the binding between a bindable component and a data source.</span></span>  
  
 <xref:System.Windows.Forms.BindingSource?displayProperty=nameWithType>  
 <span data-ttu-id="d1127-132">컨트롤에 바인딩하기 위해 데이터 소스를 캡슐화하는 클래스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-132">Describes the class that encapsulates a data source for binding to controls.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="d1127-133">관련 단원</span><span class="sxs-lookup"><span data-stu-id="d1127-133">Related Sections</span></span>  
 [<span data-ttu-id="d1127-134">BindingSource 구성 요소</span><span class="sxs-lookup"><span data-stu-id="d1127-134">BindingSource Component</span></span>](../../../docs/framework/winforms/controls/bindingsource-component.md)  
 <span data-ttu-id="d1127-135"><xref:System.Windows.Forms.BindingSource> 구성 요소를 사용하는 방법을 보여 주는 항목 목록을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-135">Contains a list of topics that demonstrate how to use the <xref:System.Windows.Forms.BindingSource> component.</span></span>  
  
 [<span data-ttu-id="d1127-136">DataGridView 컨트롤</span><span class="sxs-lookup"><span data-stu-id="d1127-136">DataGridView Control</span></span>](../../../docs/framework/winforms/controls/datagridview-control-windows-forms.md)  
 <span data-ttu-id="d1127-137">바인딩 가능한 datagrid 컨트롤을 사용하는 방법을 보여 주는 항목 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-137">Provides a list of topics that demonstrate how to use a bindable datagrid control.</span></span>  
  
 <span data-ttu-id="d1127-138">도 참조 하세요 [Visual Studio에서 데이터 액세스](/visualstudio/data-tools/accessing-data-in-visual-studio)합니다.</span><span class="sxs-lookup"><span data-stu-id="d1127-138">Also see [Accessing Data in Visual Studio](/visualstudio/data-tools/accessing-data-in-visual-studio).</span></span>
