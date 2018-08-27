---
title: '연습: Windows Forms에서 3-D WPF 복합 컨트롤 호스팅'
ms.date: 08/18/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hosting WPF content in Windows Forms [WPF]
- composite controls [WPF], hosting WPF in
ms.assetid: 486369a9-606a-4a3b-b086-a06f2119c7b0
ms.openlocfilehash: b9642cec30c5e929102616577d9f2b1b2544c6d0
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42932268"
---
# <a name="walkthrough-hosting-a-3-d-wpf-composite-control-in-windows-forms"></a><span data-ttu-id="eacd2-102">연습: Windows Forms에서 3-D WPF 복합 컨트롤 호스팅</span><span class="sxs-lookup"><span data-stu-id="eacd2-102">Walkthrough: Hosting a 3-D WPF Composite Control in Windows Forms</span></span>

<span data-ttu-id="eacd2-103">이 연습을 만드는 방법을 보여 줍니다.를 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] 복합 제어 하 고 호스트에서 [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] 컨트롤 및 사용 하 여 폼을 <xref:System.Windows.Forms.Integration.ElementHost> 컨트롤입니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-103">This walkthrough demonstrates how you can create a [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] composite control and host it in [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] controls and forms by using the <xref:System.Windows.Forms.Integration.ElementHost> control.</span></span>

<span data-ttu-id="eacd2-104">이 연습에서는 상속을 구현 된 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl> 두 자식 컨트롤이 들어 있는입니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-104">In this walkthrough, you will implement a [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl> that contains two child controls.</span></span> <span data-ttu-id="eacd2-105"><xref:System.Windows.Controls.UserControl> 3 차원 (3-D) 원뿔을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-105">The <xref:System.Windows.Controls.UserControl> displays a three-dimensional (3-D) cone.</span></span> <span data-ttu-id="eacd2-106">3 차원 개체를 렌더링 하는 것은 훨씬 쉽게 통합할 합니다 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] 보다 사용 하 여 [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]입니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-106">Rendering 3-D objects is much easier with the [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] than with [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)].</span></span> <span data-ttu-id="eacd2-107">따라서 편이 호스트에는 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl> 클래스에서 3 차원 그래픽을 만들 [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]합니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-107">Therefore, it makes sense to host a [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl> class to create 3-D graphics in [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)].</span></span>

<span data-ttu-id="eacd2-108">이 연습에서 설명하는 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-108">Tasks illustrated in this walkthrough include:</span></span>

-   <span data-ttu-id="eacd2-109">만들기는 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl>합니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-109">Creating the [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl>.</span></span>

-   <span data-ttu-id="eacd2-110">Windows Forms 호스트 프로젝트를 만드는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-110">Creating the Windows Forms host project.</span></span>

-   <span data-ttu-id="eacd2-111">호스팅하는 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl>합니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-111">Hosting the [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl>.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="eacd2-112">전제 조건</span><span class="sxs-lookup"><span data-stu-id="eacd2-112">Prerequisites</span></span>

<span data-ttu-id="eacd2-113">이 연습을 완료하려면 다음 구성 요소가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-113">You need the following components to complete this walkthrough:</span></span>

-   <span data-ttu-id="eacd2-114">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="eacd2-114">Visual Studio 2017</span></span>

<a name="To_Create_the_UserControl"></a>
## <a name="create-the-usercontrol"></a><span data-ttu-id="eacd2-115">UserControl 만들기</span><span class="sxs-lookup"><span data-stu-id="eacd2-115">Create the UserControl</span></span>

1.  <span data-ttu-id="eacd2-116">만들기는 **WPF 사용자 정의 컨트롤 라이브러리** 라는 프로젝트 `HostingWpfUserControlInWf`합니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-116">Create a **WPF User Control Library** project named `HostingWpfUserControlInWf`.</span></span>

2.  <span data-ttu-id="eacd2-117">Usercontrol1.xaml이에서 엽니다는 [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)]합니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-117">Open UserControl1.xaml in the [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)].</span></span>

3.  <span data-ttu-id="eacd2-118">생성된 된 코드를 다음 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-118">Replace the generated code with the following code:</span></span>

     [!code-xaml[HostingWpfUserControlInWf#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HostingWpfUserControlInWf/CSharp/HostingWpfUserControlInWf/ConeControl.xaml#1)]

     <span data-ttu-id="eacd2-119">이 코드는 정의 <xref:System.Windows.Controls.UserControl?displayProperty=nameWithType> 두 자식 컨트롤이 들어 있는입니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-119">This code defines a <xref:System.Windows.Controls.UserControl?displayProperty=nameWithType> that contains two child controls.</span></span> <span data-ttu-id="eacd2-120">첫 번째 자식 컨트롤은는 <xref:System.Windows.Controls.Label?displayProperty=nameWithType> ; 두 번째는는 <xref:System.Windows.Controls.Viewport3D> 3 차원 원뿔을 표시 하는 컨트롤입니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-120">The first child control is a <xref:System.Windows.Controls.Label?displayProperty=nameWithType> control; the second is a <xref:System.Windows.Controls.Viewport3D> control that displays a 3-D cone.</span></span>

<a name="To_Create_the_Windows_Forms_Host_Project"></a>
## <a name="create-the-host-project"></a><span data-ttu-id="eacd2-121">호스트 프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="eacd2-121">Create the host project</span></span>

1.  <span data-ttu-id="eacd2-122">추가 된 **WPF 앱 (.NET Framework)** 라는 프로젝트 `WpfUserControlHost` 솔루션입니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-122">Add a **WPF App (.NET Framework)** project named `WpfUserControlHost` to the solution.</span></span> <span data-ttu-id="eacd2-123">자세한 내용은 [방법: 새 WPF 응용 프로그램 프로젝트 만들기](http://msdn.microsoft.com/library/1f6aea7a-33e1-4d3f-8555-1daa42e95d82)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eacd2-123">For more information, see [How to: Create a New WPF Application Project](http://msdn.microsoft.com/library/1f6aea7a-33e1-4d3f-8555-1daa42e95d82).</span></span>

2.  <span data-ttu-id="eacd2-124">**솔루션 탐색기**, WindowsFormsIntegration.dll 이라는 WindowsFormsIntegration 어셈블리에 대 한 참조를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-124">In **Solution Explorer**, add a reference to the WindowsFormsIntegration assembly, which is named WindowsFormsIntegration.dll.</span></span>

3.  <span data-ttu-id="eacd2-125">다음에 대 한 참조를 추가 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] 어셈블리:</span><span class="sxs-lookup"><span data-stu-id="eacd2-125">Add references to the following [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] assemblies:</span></span>

    -   <span data-ttu-id="eacd2-126">PresentationCore</span><span class="sxs-lookup"><span data-stu-id="eacd2-126">PresentationCore</span></span>

    -   <span data-ttu-id="eacd2-127">PresentationFramework</span><span class="sxs-lookup"><span data-stu-id="eacd2-127">PresentationFramework</span></span>

    -   <span data-ttu-id="eacd2-128">WindowsBase</span><span class="sxs-lookup"><span data-stu-id="eacd2-128">WindowsBase</span></span>

4.  <span data-ttu-id="eacd2-129">에 대 한 참조를 추가 합니다 `HostingWpfUserControlInWf` 프로젝트입니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-129">Add a reference to the `HostingWpfUserControlInWf` project.</span></span>

5.  <span data-ttu-id="eacd2-130">솔루션 탐색기에서 설정 된 `WpfUserControlHost` 프로젝트를 시작 프로젝트로 합니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-130">In Solution Explorer, set the `WpfUserControlHost` project to be the startup project.</span></span>

<a name="To_Host_the_Windows_Presentation_Foundation"></a>
## <a name="host-the-usercontrol"></a><span data-ttu-id="eacd2-131">UserControl 호스트</span><span class="sxs-lookup"><span data-stu-id="eacd2-131">Host the UserControl</span></span>

1.  <span data-ttu-id="eacd2-132">Windows Forms 디자이너에서 Form1을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-132">In the Windows Forms Designer, open Form1.</span></span>

2.  <span data-ttu-id="eacd2-133">속성 창에서 클릭 **이벤트**를 차례로 두 번 클릭 합니다 <xref:System.Windows.Forms.Form.Load> 이벤트를 이벤트 처리기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-133">In the Properties window, click **Events**, and then double-click the <xref:System.Windows.Forms.Form.Load> event to create an event handler.</span></span>

     <span data-ttu-id="eacd2-134">새로 생성 된 코드 편집기가 열립니다 `Form1_Load` 이벤트 처리기입니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-134">The Code Editor opens to the newly generated `Form1_Load` event handler.</span></span>

3.  <span data-ttu-id="eacd2-135">Form1.cs의 코드를 다음 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-135">Replace the code in Form1.cs with the following code.</span></span>

     <span data-ttu-id="eacd2-136">합니다 `Form1_Load` 이벤트 처리기의 인스턴스를 만듭니다 `UserControl1` 초기화를 추가 하 고는 <xref:System.Windows.Forms.Integration.ElementHost> 컨트롤의 자식 컨트롤 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-136">The `Form1_Load` event handler creates an instance of `UserControl1` and adds itto the <xref:System.Windows.Forms.Integration.ElementHost> control's collection of child controls.</span></span> <span data-ttu-id="eacd2-137"><xref:System.Windows.Forms.Integration.ElementHost> 컨트롤이 자식 컨트롤의 폼의 컬렉션에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-137">The <xref:System.Windows.Forms.Integration.ElementHost> control is added to the form's collection of child controls.</span></span>

     [!code-csharp[HostingWpfUserControlInWf#10](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HostingWpfUserControlInWf/CSharp/WpfUserControlHost/Form1.cs#10)]
     [!code-vb[HostingWpfUserControlInWf#10](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HostingWpfUserControlInWf/VisualBasic/WpfUserControlHost/Form1.vb#10)]

4.  <span data-ttu-id="eacd2-138">**F5** 키를 눌러 응용 프로그램을 빌드하고 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="eacd2-138">Press **F5** to build and run the application.</span></span>

## <a name="see-also"></a><span data-ttu-id="eacd2-139">참고 항목</span><span class="sxs-lookup"><span data-stu-id="eacd2-139">See Also</span></span>

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [<span data-ttu-id="eacd2-140">WPF 디자이너</span><span class="sxs-lookup"><span data-stu-id="eacd2-140">WPF Designer</span></span>](http://msdn.microsoft.com/library/c6c65214-8411-4e16-b254-163ed4099c26)
- [<span data-ttu-id="eacd2-141">연습: Windows Forms에서 WPF 복합 컨트롤 호스팅</span><span class="sxs-lookup"><span data-stu-id="eacd2-141">Walkthrough: Hosting a WPF Composite Control in Windows Forms</span></span>](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-wpf-composite-control-in-windows-forms.md)
- [<span data-ttu-id="eacd2-142">연습: WPF에서 Windows Forms 복합 컨트롤 호스팅</span><span class="sxs-lookup"><span data-stu-id="eacd2-142">Walkthrough: Hosting a Windows Forms Composite Control in WPF</span></span>](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-windows-forms-composite-control-in-wpf.md)
- [<span data-ttu-id="eacd2-143">Windows Forms 샘플에서 WPF 복합 컨트롤 호스팅</span><span class="sxs-lookup"><span data-stu-id="eacd2-143">Hosting a WPF Composite Control in Windows Forms Sample</span></span>](http://go.microsoft.com/fwlink/?LinkID=160001)