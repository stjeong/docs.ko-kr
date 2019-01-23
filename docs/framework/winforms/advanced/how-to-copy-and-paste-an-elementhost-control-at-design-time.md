---
title: '방법: 복사 하 고 디자인 타임에 ElementHost 컨트롤을 붙여 넣습니다.'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, content copying and pasting
- interoperability [WPF]
- ElementHost control [Windows Forms], copying and pasting at design time
- WPF user control [Windows Forms], hosting in Windows Forms
ms.assetid: e570375d-2a68-44ba-b4f7-c781af2d20e8
ms.openlocfilehash: 6ff1ccc5e8f188bdec2e09048974fdc20a785920
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54572633"
---
# <a name="how-to-copy-and-paste-an-elementhost-control-at-design-time"></a><span data-ttu-id="50b85-102">방법: 복사 하 고 디자인 타임에 ElementHost 컨트롤을 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="50b85-102">How to: Copy and Paste an ElementHost Control at Design Time</span></span>
<span data-ttu-id="50b85-103">이 절차에서는 Windows Form에 Windows Presentation Foundation (WPF) 컨트롤을 복사 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="50b85-103">This procedure shows you how to copy a Windows Presentation Foundation (WPF) control on a Windows Form.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="50b85-104">표시되는 대화 상자와 메뉴 명령은 활성 설정이나 버전에 따라 도움말에서 설명하는 것과 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50b85-104">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="50b85-105">설정을 변경하려면 **도구** 메뉴에서 **설정 가져오기 및 내보내기** 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="50b85-105">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="50b85-106">자세한 내용은 [Visual Studio IDE 개인 설정](/visualstudio/ide/personalizing-the-visual-studio-ide)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="50b85-106">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-copy-and-paste-an-elementhost-control-at-design-time"></a><span data-ttu-id="50b85-107">복사 하 여 디자인 타임에 ElementHost 컨트롤을 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="50b85-107">To copy and paste an ElementHost control at design time</span></span>  
  
1.  <span data-ttu-id="50b85-108">새 WPF 추가 <xref:System.Windows.Controls.UserControl> Windows Forms 프로젝트에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50b85-108">Add a new WPF <xref:System.Windows.Controls.UserControl> to your Windows Forms project.</span></span> <span data-ttu-id="50b85-109">컨트롤 형식의 기본 이름인 `UserControl1.xaml`을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="50b85-109">Use the default name for the control type, `UserControl1.xaml`.</span></span> <span data-ttu-id="50b85-110">자세한 내용은 [연습: 디자인 타임에 Windows Forms에서 새 WPF 콘텐츠 만들기](../../../../docs/framework/winforms/advanced/walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="50b85-110">For more information, see [Walkthrough: Creating New WPF Content on Windows Forms at Design Time](../../../../docs/framework/winforms/advanced/walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).</span></span>  
  
2.  <span data-ttu-id="50b85-111">에 **속성** 창에서 값을 설정 합니다 <xref:System.Windows.FrameworkElement.Width%2A> 및 <xref:System.Windows.FrameworkElement.Height%2A> 의 속성 `UserControl1` 를 `200`합니다.</span><span class="sxs-lookup"><span data-stu-id="50b85-111">In the **Properties** window, set the value of the <xref:System.Windows.FrameworkElement.Width%2A> and <xref:System.Windows.FrameworkElement.Height%2A> properties of `UserControl1` to `200`.</span></span>  
  
3.  <span data-ttu-id="50b85-112"><xref:System.Windows.Controls.Control.Background%2A> 속성 값을 `Blue`로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="50b85-112">Set the value of the <xref:System.Windows.Controls.Control.Background%2A> property to `Blue`.</span></span>  
  
4.  <span data-ttu-id="50b85-113">프로젝트를 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="50b85-113">Build the project.</span></span>  
  
5.  <span data-ttu-id="50b85-114">Windows Forms 디자이너에서 `Form1`을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="50b85-114">Open `Form1` in the Windows Forms Designer.</span></span>  
  
6.  <span data-ttu-id="50b85-115">합니다 **도구 상자**의 인스턴스를 끌어 `UserControl1` 폼입니다.</span><span class="sxs-lookup"><span data-stu-id="50b85-115">From the **Toolbox**, drag an instance of `UserControl1` onto the form.</span></span>  
  
     <span data-ttu-id="50b85-116">`UserControl1` 인스턴스가 `elementHost1`이라는 새 <xref:System.Windows.Forms.Integration.ElementHost> 컨트롤에서 호스트됩니다.</span><span class="sxs-lookup"><span data-stu-id="50b85-116">An instance of `UserControl1` is hosted in a new <xref:System.Windows.Forms.Integration.ElementHost> control named `elementHost1`.</span></span>  
  
7.  <span data-ttu-id="50b85-117">`elementHost1`을 선택하고 Ctrl+C를 눌러 클립보드에 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="50b85-117">With `elementHost1` selected, press CTRL+C to copy it to the clipboard.</span></span>  
  
8.  <span data-ttu-id="50b85-118">복사한 컨트롤을 폼으로 붙여 넣으려면 CTRL + V 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="50b85-118">Press CTRL+V to paste the copied control onto the form.</span></span>  
  
     <span data-ttu-id="50b85-119">새 <xref:System.Windows.Forms.Integration.ElementHost> 제어 라는 `elementHost2` 폼에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="50b85-119">A new <xref:System.Windows.Forms.Integration.ElementHost> control named `elementHost2` is created on the form.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="50b85-120">참고자료</span><span class="sxs-lookup"><span data-stu-id="50b85-120">See also</span></span>

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [<span data-ttu-id="50b85-121">마이그레이션 및 상호 운용성</span><span class="sxs-lookup"><span data-stu-id="50b85-121">Migration and Interoperability</span></span>](../../../../docs/framework/wpf/advanced/migration-and-interoperability.md)
- [<span data-ttu-id="50b85-122">WPF 컨트롤 사용</span><span class="sxs-lookup"><span data-stu-id="50b85-122">Using WPF Controls</span></span>](../../../../docs/framework/winforms/advanced/using-wpf-controls.md)
- [<span data-ttu-id="50b85-123">Visual Studio에서 XAML 디자인</span><span class="sxs-lookup"><span data-stu-id="50b85-123">Design XAML in Visual Studio</span></span>](/visualstudio/designers/designing-xaml-in-visual-studio)
