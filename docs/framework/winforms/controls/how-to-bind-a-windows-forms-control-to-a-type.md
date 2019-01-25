---
title: '방법: 형식에는 Windows Forms 컨트롤 바인딩'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [Windows Forms], binding to a type
- BindingSource component [Windows Forms], binding to a type
- types [Windows Forms], binding controls to
ms.assetid: 94faeebb-d2bc-45d6-86d7-96a42661b43d
ms.openlocfilehash: 42290fa7d9d38a57e17984ae5f1a9505b099ce1e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54698286"
---
# <a name="how-to-bind-a-windows-forms-control-to-a-type"></a><span data-ttu-id="61881-102">방법: 형식에는 Windows Forms 컨트롤 바인딩</span><span class="sxs-lookup"><span data-stu-id="61881-102">How to: Bind a Windows Forms Control to a Type</span></span>
<span data-ttu-id="61881-103">데이터와 상호 작용하는 컨트롤을 빌드하는 경우 때로는 개체가 아니라 형식에 컨트롤을 바인딩할 필요가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61881-103">When you are building controls that interact with data, you will sometimes find it necessary to bind a control to a type, rather than an object.</span></span> <span data-ttu-id="61881-104">이 상황은 특히 데이터를 사용할 수 없지만 데이터 바인딩된 컨트롤이 여전히 형식의 공용 인터페이스에서 가져온 정보를 표시해야 하는 경우 디자인 타임에 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="61881-104">This situation arises especially at design time, when data may not be available, but your data-bound controls still need to display information from a type's public interface.</span></span> <span data-ttu-id="61881-105">예를 들어 웹 서비스에서 노출된 개체에 <xref:System.Windows.Forms.DataGridView> 컨트롤을 바인딩하고 디자인 타임에 <xref:System.Windows.Forms.DataGridView> 컨트롤이 사용자 지정 형식의 멤버 이름으로 해당 열의 레이블을 지정하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61881-105">For example, you may bind a <xref:System.Windows.Forms.DataGridView> control to an object exposed by a Web service and want the <xref:System.Windows.Forms.DataGridView> control to label its columns at design time with the member names of a custom type.</span></span>  
  
 <span data-ttu-id="61881-106"><xref:System.Windows.Forms.BindingSource> 구성 요소를 사용하여 컨트롤을 형식에 쉽게 바인딩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61881-106">You can easily bind a control to a type with the <xref:System.Windows.Forms.BindingSource> component.</span></span>  
  
## <a name="example"></a><span data-ttu-id="61881-107">예제</span><span class="sxs-lookup"><span data-stu-id="61881-107">Example</span></span>  
 <span data-ttu-id="61881-108">다음 코드 예제에서는 <xref:System.Windows.Forms.BindingSource> 구성 요소를 사용하여 <xref:System.Windows.Forms.DataGridView> 컨트롤을 사용자 지정 형식에 바인딩하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="61881-108">The following code example demonstrates how to bind a <xref:System.Windows.Forms.DataGridView> control to a custom type by using a <xref:System.Windows.Forms.BindingSource> component.</span></span> <span data-ttu-id="61881-109">예제를 실행하면 컨트롤에 데이터가 채워지기 전에 <xref:System.Windows.Forms.DataGridView>에 `Customer` 개체의 속성을 반영하는 레이블 열이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="61881-109">When you run the example, you'll notice the <xref:System.Windows.Forms.DataGridView> has labeled columns that reflect the properties of a `Customer` object, before the control is populated with data.</span></span> <span data-ttu-id="61881-110">예제에는 <xref:System.Windows.Forms.DataGridView> 컨트롤에 데이터를 추가하는 Add Customer 단추가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61881-110">The example has an Add Customer button to add data to the <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="61881-111">이 단추를 클릭하면 새로운 `Customer` 개체가 <xref:System.Windows.Forms.BindingSource>에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="61881-111">When you click the button, a new `Customer` object is added to the <xref:System.Windows.Forms.BindingSource>.</span></span> <span data-ttu-id="61881-112">실제 시나리오에서는 웹 서비스 또는 다른 데이터 소스를 호출하여 데이터를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61881-112">In a real-world scenario, the data might be obtained by a call to a Web service or other data source.</span></span>  
  
 [!code-csharp[System.Windows.Forms.DataConnector.BindingToType#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.BindingToType/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.DataConnector.BindingToType#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.BindingToType/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="61881-113">코드 컴파일</span><span class="sxs-lookup"><span data-stu-id="61881-113">Compiling the Code</span></span>  
 <span data-ttu-id="61881-114">이 예제에는 다음 사항이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="61881-114">This example requires:</span></span>  
  
-   <span data-ttu-id="61881-115">System 및 System.Windows.Forms 어셈블리에 대한 참조</span><span class="sxs-lookup"><span data-stu-id="61881-115">References to the System and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="61881-116">Visual Basic 또는 Visual C#에 대 한 명령줄에서이 예제를 빌드하는 방법에 대 한 내용은 [명령줄에서 빌드](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) 하거나 [csc.exe를 사용한 명령줄 빌드](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="61881-116">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="61881-117">또한 새 프로젝트에 코드를 붙여 넣어 Visual Studio에서이 예제를 빌드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61881-117">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="61881-118">또한 참조 [방법: 컴파일 및 Visual Studio를 사용 하 여 전체 Windows Forms 코드 예제를 실행](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))합니다.</span><span class="sxs-lookup"><span data-stu-id="61881-118">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61881-119">참고자료</span><span class="sxs-lookup"><span data-stu-id="61881-119">See also</span></span>
- <xref:System.Windows.Forms.BindingNavigator>
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [<span data-ttu-id="61881-120">BindingSource 구성 요소</span><span class="sxs-lookup"><span data-stu-id="61881-120">BindingSource Component</span></span>](../../../../docs/framework/winforms/controls/bindingsource-component.md)
