---
title: '연습: 디자인 타임에 호스팅된 WPF 요소의 속성 변경'
ms.date: 03/30/2017
helpviewer_keywords:
- WPF content [Windows Forms], changing properties at design time
- Windows Forms, changing properties of WPF content at design time
- WPF content [Windows Forms], hosting in Windows Forms
- interoperability [WPF]
ms.assetid: a1f7a90c-0bbb-4781-8c3c-8cc8bef2488d
ms.openlocfilehash: 15cab9266af5840aa4b37a62b71bd5010b7a859a
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43535644"
---
# <a name="walkthrough-changing-properties-of-a-hosted-wpf-element-at-design-time"></a><span data-ttu-id="77b9d-102">연습: 디자인 타임에 호스팅된 WPF 요소의 속성 변경</span><span class="sxs-lookup"><span data-stu-id="77b9d-102">Walkthrough: Changing Properties of a Hosted WPF Element at Design Time</span></span>
<span data-ttu-id="77b9d-103">이 연습에서는 Windows Forms에 호스트된 WPF(Windows Presentation Foundation) 컨트롤의 속성 값을 변경하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-103">This walkthrough shows you how to change property values of a Windows Presentation Foundation (WPF) control hosted on a Windows Form.</span></span>  
  
 <span data-ttu-id="77b9d-104">이 연습에서는 다음 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-104">In this walkthrough, you perform the following tasks:</span></span>  
  
-   <span data-ttu-id="77b9d-105">프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-105">Create the project.</span></span>  
  
-   <span data-ttu-id="77b9d-106">WPF 컨트롤을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-106">Create the WPF control.</span></span>  
  
-   <span data-ttu-id="77b9d-107">Windows Form에서 WPF 컨트롤을 호스트합니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-107">Host the WPF controls on a Windows Form.</span></span>  
  
-   <span data-ttu-id="77b9d-108">Visual Studio용 WPF 디자이너를 사용하여 속성 값을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-108">Use the WPF Designer for Visual Studio to change property values.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="77b9d-109">표시되는 대화 상자와 메뉴 명령은 활성 설정이나 버전에 따라 도움말에서 설명하는 것과 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-109">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="77b9d-110">설정을 변경하려면 **도구** 메뉴에서 **설정 가져오기 및 내보내기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-110">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="77b9d-111">자세한 내용은 [Visual Studio IDE 개인 설정](/visualstudio/ide/personalizing-the-visual-studio-ide)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="77b9d-111">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="77b9d-112">전제 조건</span><span class="sxs-lookup"><span data-stu-id="77b9d-112">Prerequisites</span></span>  
 <span data-ttu-id="77b9d-113">이 연습을 완료하려면 다음 구성 요소가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-113">You need the following components to complete this walkthrough:</span></span>  
  
-   [!INCLUDE[vs_dev11_long](../../../../includes/vs-dev11-long-md.md)]<span data-ttu-id="77b9d-114">.</span><span class="sxs-lookup"><span data-stu-id="77b9d-114">.</span></span>  
  
## <a name="creating-the-project"></a><span data-ttu-id="77b9d-115">프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="77b9d-115">Creating the Project</span></span>  
 <span data-ttu-id="77b9d-116">첫 번째 단계에서는 Windows Forms 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-116">The first step is to create the Windows Forms project.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="77b9d-117">WPF 콘텐츠를 호스트하는 경우 C# 및 Visual Basic 프로젝트만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-117">When hosting WPF content, only C# and Visual Basic projects are supported.</span></span>  
  
#### <a name="to-create-the-project"></a><span data-ttu-id="77b9d-118">프로젝트를 만들려면</span><span class="sxs-lookup"><span data-stu-id="77b9d-118">To create the project</span></span>  
  
-   <span data-ttu-id="77b9d-119">Visual Basic 또는 Visual C#에서 새 Windows Forms 응용 프로그램 프로젝트를 만들 `WpfHost`합니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-119">Create a new Windows Forms Application project in Visual Basic or Visual C# named `WpfHost`.</span></span>  
  
## <a name="creating-the-wpf-control"></a><span data-ttu-id="77b9d-120">WPF 컨트롤 만들기</span><span class="sxs-lookup"><span data-stu-id="77b9d-120">Creating the WPF Control</span></span>  
 <span data-ttu-id="77b9d-121">프로젝트에 WPF 컨트롤을 추가한 후 폼에 정렬할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-121">After you add a WPF control to the project, you can arrange it on the form.</span></span>  
  
#### <a name="to-create-wpf-controls"></a><span data-ttu-id="77b9d-122">WPF 컨트롤을 만들려면</span><span class="sxs-lookup"><span data-stu-id="77b9d-122">To create WPF controls</span></span>  
  
1.  <span data-ttu-id="77b9d-123">프로젝트에 새 WPF <xref:System.Windows.Controls.UserControl>을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-123">Add a new WPF <xref:System.Windows.Controls.UserControl> to the project.</span></span> <span data-ttu-id="77b9d-124">컨트롤 형식의 기본 이름인 `UserControl1.xaml`을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-124">Use the default name for the control type, `UserControl1.xaml`.</span></span> <span data-ttu-id="77b9d-125">자세한 내용은 [연습: 만드는 새 WPF 콘텐츠 디자인 타임에 Windows Forms에서](../../../../docs/framework/winforms/advanced/walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-125">For more information, see [Walkthrough: Creating New WPF Content on Windows Forms at Design Time](../../../../docs/framework/winforms/advanced/walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).</span></span>  
  
2.  <span data-ttu-id="77b9d-126">에 **속성** 창에서 값을 설정 합니다 <xref:System.Windows.Controls.Control.Background%2A> 속성을 `Blue`입니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-126">In the **Properties** window, set the value of the <xref:System.Windows.Controls.Control.Background%2A> property to `Blue`.</span></span>  
  
3.  <span data-ttu-id="77b9d-127">프로젝트를 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-127">Build the project.</span></span>  
  
## <a name="changing-property-values-on-the-wpf-control"></a><span data-ttu-id="77b9d-128">WPF 컨트롤의 속성 값 변경</span><span class="sxs-lookup"><span data-stu-id="77b9d-128">Changing Property Values on the WPF Control</span></span>  
 <span data-ttu-id="77b9d-129"><xref:System.Windows.Forms.Integration.ElementHost> 스마트 태그를 사용하면 WPF 디자이너에서 호스트된 WPF의 속성을 쉽게 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-129">The <xref:System.Windows.Forms.Integration.ElementHost> smart tag makes it easy to change properties of hosted WPF content by using the WPF Designer.</span></span>  
  
#### <a name="to-host-a-wpf-control"></a><span data-ttu-id="77b9d-130">WPF 컨트롤을 호스트하려면</span><span class="sxs-lookup"><span data-stu-id="77b9d-130">To host a WPF control</span></span>  
  
1.  <span data-ttu-id="77b9d-131">Windows Forms 디자이너에서 `Form1`을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-131">Open `Form1` in the Windows Forms Designer.</span></span>  
  
2.  <span data-ttu-id="77b9d-132">에 **도구 상자**를 **WPF 사용자 정의 컨트롤** 탭을 두 번 클릭 `UserControl1` 의 인스턴스를 만드는 `UserControl1` 폼에.</span><span class="sxs-lookup"><span data-stu-id="77b9d-132">In the **Toolbox**, in the **WPF User Controls** tab, double-click `UserControl1` to create an instance of `UserControl1` on the form.</span></span>  
  
     <span data-ttu-id="77b9d-133">`UserControl1` 인스턴스가 `elementHost1`이라는 새 <xref:System.Windows.Forms.Integration.ElementHost> 컨트롤에서 호스트됩니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-133">The instance of `UserControl1` is hosted in a new <xref:System.Windows.Forms.Integration.ElementHost> control named `elementHost1`.</span></span>  
  
3.  <span data-ttu-id="77b9d-134">에 **ElementHost 작업** 스마트 태그 패널 **호스팅된 콘텐츠 편집**합니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-134">In the **ElementHost Tasks** smart tag panel, select **Edit Hosted Content**.</span></span>  
  
     <span data-ttu-id="77b9d-135">UserControl1.xaml이 WPF 디자이너에서 열립니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-135">UserControl1.xaml opens in the WPF Designer.</span></span>  
  
4.  <span data-ttu-id="77b9d-136">에 **속성** 창에서 값을 설정 합니다 <xref:System.Windows.Controls.Control.Background%2A> 속성을 `Red`입니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-136">In the **Properties** window, set the value of the <xref:System.Windows.Controls.Control.Background%2A> property to `Red`.</span></span>  
  
5.  <span data-ttu-id="77b9d-137">프로젝트를 다시 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-137">Rebuild the project.</span></span>  
  
6.  <span data-ttu-id="77b9d-138">Windows Forms 디자이너에서 `Form1`을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-138">Open `Form1` in the Windows Forms Designer.</span></span>  
  
     <span data-ttu-id="77b9d-139">`UserControl1` 인스턴스의 배경색이 빨간색입니다.</span><span class="sxs-lookup"><span data-stu-id="77b9d-139">The instance of `UserControl1` has a red background.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77b9d-140">참고 항목</span><span class="sxs-lookup"><span data-stu-id="77b9d-140">See Also</span></span>  
 <xref:System.Windows.Forms.Integration.ElementHost>  
 <xref:System.Windows.Forms.Integration.WindowsFormsHost>  
 [<span data-ttu-id="77b9d-141">방법: TableLayoutPanel 컨트롤의 자식 컨트롤 고정 및 도킹</span><span class="sxs-lookup"><span data-stu-id="77b9d-141">How to: Anchor and Dock Child Controls in a TableLayoutPanel Control</span></span>](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)  
 [<span data-ttu-id="77b9d-142">방법: 디자인 타임에 컨트롤을 양식의 가장자리에 맞춤</span><span class="sxs-lookup"><span data-stu-id="77b9d-142">How to: Align a Control to the Edges of Forms at Design Time</span></span>](../../../../docs/framework/winforms/controls/how-to-align-a-control-to-the-edges-of-forms-at-design-time.md)  
 [<span data-ttu-id="77b9d-143">연습: Windows Forms에서 맞춤선을 사용하여 컨트롤 정렬</span><span class="sxs-lookup"><span data-stu-id="77b9d-143">Walkthrough: Arranging Controls on Windows Forms Using Snaplines</span></span>](../../../../docs/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)  
 [<span data-ttu-id="77b9d-144">마이그레이션 및 상호 운용성</span><span class="sxs-lookup"><span data-stu-id="77b9d-144">Migration and Interoperability</span></span>](../../../../docs/framework/wpf/advanced/migration-and-interoperability.md)  
 [<span data-ttu-id="77b9d-145">WPF 컨트롤 사용</span><span class="sxs-lookup"><span data-stu-id="77b9d-145">Using WPF Controls</span></span>](../../../../docs/framework/winforms/advanced/using-wpf-controls.md)  
 [<span data-ttu-id="77b9d-146">Visual Studio에서 XAML 디자인</span><span class="sxs-lookup"><span data-stu-id="77b9d-146">Design XAML in Visual Studio</span></span>](/visualstudio/designers/designing-xaml-in-visual-studio)
