---
title: 표준 컨트롤에 대한 UI 자동화 지원
ms.date: 03/30/2017
helpviewer_keywords:
- controls, UI Automation support for
- UI Automation, support for standard controls
ms.assetid: 3770ea8a-2655-4add-9c59-fe0610ad5084
author: Xansky
ms.author: mhopkins
ms.openlocfilehash: 68fa7753be76b0681c40e540e86b11c89e7a8ca1
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/02/2018
ms.locfileid: "48037341"
---
# <a name="ui-automation-support-for-standard-controls"></a><span data-ttu-id="a3c6b-102">표준 컨트롤에 대한 UI 자동화 지원</span><span class="sxs-lookup"><span data-stu-id="a3c6b-102">UI Automation Support for Standard Controls</span></span>
> [!NOTE]
>  <span data-ttu-id="a3c6b-103">이 설명서는 <xref:System.Windows.Automation> 네임스페이스에 정의된 관리되는 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 클래스를 사용하려는 .NET Framework 개발자를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a3c6b-103">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="a3c6b-104">에 대 한 최신 정보에 대 한 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]를 참조 하세요 [Windows Automation API: UI 자동화](https://go.microsoft.com/fwlink/?LinkID=156746)합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c6b-104">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span></span>  
  
 <span data-ttu-id="a3c6b-105">이 항목에는 [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] , [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)]및 [!INCLUDE[TLA#tla_win32](../../../includes/tlasharptla-win32-md.md)]프레임워크용으로 개발된 응용 프로그램에서 표준 컨트롤에 대한 [!INCLUDE[TLA#tla_winforms](../../../includes/tlasharptla-winforms-md.md)] 지원 정보가 들어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c6b-105">This topic contains information about [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] support for standard controls in applications developed for the [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)], [!INCLUDE[TLA#tla_win32](../../../includes/tlasharptla-win32-md.md)], and [!INCLUDE[TLA#tla_winforms](../../../includes/tlasharptla-winforms-md.md)] frameworks.</span></span>  
  
<a name="Windows_Presentation_Foundation_Controls"></a>   
## <a name="windows-presentation-foundation-controls"></a><span data-ttu-id="a3c6b-106">WPF(Windows Presentation Foundation) 컨트롤</span><span class="sxs-lookup"><span data-stu-id="a3c6b-106">Windows Presentation Foundation Controls</span></span>  
 <span data-ttu-id="a3c6b-107">사용자 상호 작용 지원 또는 정보를 제공하는 모든 [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)] 컨트롤 요소에는 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]에 대한 전체 기본 지원이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c6b-107">All [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)] control elements that provide information or support for user interaction have full native support for [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)].</span></span> <span data-ttu-id="a3c6b-108">패널 등과 같은 기타 요소는 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]에 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c6b-108">Other elements, such as panels, are not visible to [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)].</span></span>  
  
<a name="Win32_Controls"></a>   
## <a name="win32-controls"></a><span data-ttu-id="a3c6b-109">Win32 컨트롤</span><span class="sxs-lookup"><span data-stu-id="a3c6b-109">Win32 Controls</span></span>  
 <span data-ttu-id="a3c6b-110">대부분의 [!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)] 컨트롤은 UIAutomationClientsideProviders.dll의 클라이언트쪽 공급자를 통해 [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] 에 노출됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c6b-110">Most [!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)] controls are exposed to [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] through client-side providers in UIAutomationClientsideProviders.dll.</span></span> <span data-ttu-id="a3c6b-111">이 어셈블리는 UI 자동화 클라이언트 응용 프로그램과 함께 사용할 수 있도록 자동으로 등록됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c6b-111">This assembly is automatically registered for use with UI Automation client applications.</span></span>  
  
 <span data-ttu-id="a3c6b-112">전체 지원은 ComCtrl32.dll 버전 6의 컨트롤에만 제공됩니다( [!INCLUDE[TLA#tla_winxp](../../../includes/tlasharptla-winxp-md.md)] 이상에서 사용 가능).</span><span class="sxs-lookup"><span data-stu-id="a3c6b-112">Full support is provided only for controls from version 6 of ComCtrl32.dll (available with [!INCLUDE[TLA#tla_winxp](../../../includes/tlasharptla-winxp-md.md)] and later).</span></span>  
  
 <span data-ttu-id="a3c6b-113">다음과 같은 컨트롤이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c6b-113">The following controls are supported.</span></span>  
  
|<span data-ttu-id="a3c6b-114">클래스 이름</span><span class="sxs-lookup"><span data-stu-id="a3c6b-114">Class name</span></span>|<span data-ttu-id="a3c6b-115">컨트롤 종류</span><span class="sxs-lookup"><span data-stu-id="a3c6b-115">Control Type</span></span>|  
|----------------|------------------|  
|<span data-ttu-id="a3c6b-116">단추</span><span class="sxs-lookup"><span data-stu-id="a3c6b-116">Button</span></span>|<span data-ttu-id="a3c6b-117">단추</span><span class="sxs-lookup"><span data-stu-id="a3c6b-117">Button</span></span>|  
|<span data-ttu-id="a3c6b-118">단추</span><span class="sxs-lookup"><span data-stu-id="a3c6b-118">Button</span></span>|<span data-ttu-id="a3c6b-119">RadioButton</span><span class="sxs-lookup"><span data-stu-id="a3c6b-119">RadioButton</span></span>|  
|<span data-ttu-id="a3c6b-120">단추</span><span class="sxs-lookup"><span data-stu-id="a3c6b-120">Button</span></span>|<span data-ttu-id="a3c6b-121">그룹화</span><span class="sxs-lookup"><span data-stu-id="a3c6b-121">Group</span></span>|  
|<span data-ttu-id="a3c6b-122">단추</span><span class="sxs-lookup"><span data-stu-id="a3c6b-122">Button</span></span>|<span data-ttu-id="a3c6b-123">CheckBox</span><span class="sxs-lookup"><span data-stu-id="a3c6b-123">CheckBox</span></span>|  
|<span data-ttu-id="a3c6b-124">단추</span><span class="sxs-lookup"><span data-stu-id="a3c6b-124">Button</span></span>|<span data-ttu-id="a3c6b-125">하이퍼링크</span><span class="sxs-lookup"><span data-stu-id="a3c6b-125">Hyperlink</span></span>|  
|<span data-ttu-id="a3c6b-126">단추</span><span class="sxs-lookup"><span data-stu-id="a3c6b-126">Button</span></span>|<span data-ttu-id="a3c6b-127">SplitButton</span><span class="sxs-lookup"><span data-stu-id="a3c6b-127">SplitButton</span></span>|  
|<span data-ttu-id="a3c6b-128">단추</span><span class="sxs-lookup"><span data-stu-id="a3c6b-128">Button</span></span>|<span data-ttu-id="a3c6b-129">CheckBox</span><span class="sxs-lookup"><span data-stu-id="a3c6b-129">CheckBox</span></span>|  
|<span data-ttu-id="a3c6b-130">ComboBoxEx32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-130">ComboBoxEx32</span></span>|<span data-ttu-id="a3c6b-131">ComboBox</span><span class="sxs-lookup"><span data-stu-id="a3c6b-131">ComboBox</span></span>|  
|<span data-ttu-id="a3c6b-132">ComboBox</span><span class="sxs-lookup"><span data-stu-id="a3c6b-132">ComboBox</span></span>|<span data-ttu-id="a3c6b-133">ComboBox</span><span class="sxs-lookup"><span data-stu-id="a3c6b-133">ComboBox</span></span>|  
|<span data-ttu-id="a3c6b-134">편집</span><span class="sxs-lookup"><span data-stu-id="a3c6b-134">Edit</span></span>|<span data-ttu-id="a3c6b-135">문서</span><span class="sxs-lookup"><span data-stu-id="a3c6b-135">Document</span></span>|  
|<span data-ttu-id="a3c6b-136">편집</span><span class="sxs-lookup"><span data-stu-id="a3c6b-136">Edit</span></span>|<span data-ttu-id="a3c6b-137">편집</span><span class="sxs-lookup"><span data-stu-id="a3c6b-137">Edit</span></span>|  
|<span data-ttu-id="a3c6b-138">SysLink</span><span class="sxs-lookup"><span data-stu-id="a3c6b-138">SysLink</span></span>|<span data-ttu-id="a3c6b-139">하이퍼링크</span><span class="sxs-lookup"><span data-stu-id="a3c6b-139">Hyperlink</span></span>|  
|<span data-ttu-id="a3c6b-140">정적</span><span class="sxs-lookup"><span data-stu-id="a3c6b-140">Static</span></span>|<span data-ttu-id="a3c6b-141">텍스트</span><span class="sxs-lookup"><span data-stu-id="a3c6b-141">Text</span></span>|  
|<span data-ttu-id="a3c6b-142">정적</span><span class="sxs-lookup"><span data-stu-id="a3c6b-142">Static</span></span>|<span data-ttu-id="a3c6b-143">이미지</span><span class="sxs-lookup"><span data-stu-id="a3c6b-143">Image</span></span>|  
|<span data-ttu-id="a3c6b-144">SysIPAddress32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-144">SysIPAddress32</span></span>|<span data-ttu-id="a3c6b-145">사용자 지정</span><span class="sxs-lookup"><span data-stu-id="a3c6b-145">Custom</span></span>|  
|<span data-ttu-id="a3c6b-146">SysHeader32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-146">SysHeader32</span></span>|<span data-ttu-id="a3c6b-147">Header/HeaderItem</span><span class="sxs-lookup"><span data-stu-id="a3c6b-147">Header/HeaderItem</span></span>|  
|<span data-ttu-id="a3c6b-148">SysListView32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-148">SysListView32</span></span>|<span data-ttu-id="a3c6b-149">DataGrid</span><span class="sxs-lookup"><span data-stu-id="a3c6b-149">DataGrid</span></span>|  
|<span data-ttu-id="a3c6b-150">SysListView32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-150">SysListView32</span></span>|<span data-ttu-id="a3c6b-151">목록</span><span class="sxs-lookup"><span data-stu-id="a3c6b-151">List</span></span>|  
|<span data-ttu-id="a3c6b-152">ListBox</span><span class="sxs-lookup"><span data-stu-id="a3c6b-152">ListBox</span></span>|<span data-ttu-id="a3c6b-153">목록</span><span class="sxs-lookup"><span data-stu-id="a3c6b-153">List</span></span>|  
|<span data-ttu-id="a3c6b-154">ListBox</span><span class="sxs-lookup"><span data-stu-id="a3c6b-154">ListBox</span></span>|<span data-ttu-id="a3c6b-155">ListItem</span><span class="sxs-lookup"><span data-stu-id="a3c6b-155">ListItem</span></span>|  
|<span data-ttu-id="a3c6b-156">#32768</span><span class="sxs-lookup"><span data-stu-id="a3c6b-156">#32768</span></span>|<span data-ttu-id="a3c6b-157">메뉴</span><span class="sxs-lookup"><span data-stu-id="a3c6b-157">Menu</span></span>|  
|<span data-ttu-id="a3c6b-158">#32768</span><span class="sxs-lookup"><span data-stu-id="a3c6b-158">#32768</span></span>|<span data-ttu-id="a3c6b-159">MenuItem</span><span class="sxs-lookup"><span data-stu-id="a3c6b-159">MenuItem</span></span>|  
|<span data-ttu-id="a3c6b-160">msctls_progress32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-160">msctls_progress32</span></span>|<span data-ttu-id="a3c6b-161">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="a3c6b-161">ProgressBar</span></span>|  
|<span data-ttu-id="a3c6b-162">RichEdit</span><span class="sxs-lookup"><span data-stu-id="a3c6b-162">RichEdit</span></span>|<span data-ttu-id="a3c6b-163">문서.</span><span class="sxs-lookup"><span data-stu-id="a3c6b-163">Document.</span></span> <span data-ttu-id="a3c6b-164">메모를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a3c6b-164">See note.</span></span>|  
|<span data-ttu-id="a3c6b-165">RichEdit20A</span><span class="sxs-lookup"><span data-stu-id="a3c6b-165">RichEdit20A</span></span>|<span data-ttu-id="a3c6b-166">문서</span><span class="sxs-lookup"><span data-stu-id="a3c6b-166">Document</span></span>|  
|<span data-ttu-id="a3c6b-167">RichEdit20W</span><span class="sxs-lookup"><span data-stu-id="a3c6b-167">RichEdit20W</span></span>|<span data-ttu-id="a3c6b-168">문서</span><span class="sxs-lookup"><span data-stu-id="a3c6b-168">Document</span></span>|  
|<span data-ttu-id="a3c6b-169">RichEdit50W</span><span class="sxs-lookup"><span data-stu-id="a3c6b-169">RichEdit50W</span></span>|<span data-ttu-id="a3c6b-170">문서</span><span class="sxs-lookup"><span data-stu-id="a3c6b-170">Document</span></span>|  
|<span data-ttu-id="a3c6b-171">ScrollBar</span><span class="sxs-lookup"><span data-stu-id="a3c6b-171">ScrollBar</span></span>|<span data-ttu-id="a3c6b-172">슬라이더</span><span class="sxs-lookup"><span data-stu-id="a3c6b-172">Slider</span></span>|  
|<span data-ttu-id="a3c6b-173">msctls_trackbar32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-173">msctls_trackbar32</span></span>|<span data-ttu-id="a3c6b-174">슬라이더</span><span class="sxs-lookup"><span data-stu-id="a3c6b-174">Slider</span></span>|  
|<span data-ttu-id="a3c6b-175">msctls_updown32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-175">msctls_updown32</span></span>|<span data-ttu-id="a3c6b-176">Spinner</span><span class="sxs-lookup"><span data-stu-id="a3c6b-176">Spinner</span></span>|  
|<span data-ttu-id="a3c6b-177">msctls_statusbar32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-177">msctls_statusbar32</span></span>|<span data-ttu-id="a3c6b-178">StatusBar</span><span class="sxs-lookup"><span data-stu-id="a3c6b-178">StatusBar</span></span>|  
|<span data-ttu-id="a3c6b-179">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-179">SysTabControl32</span></span>|<span data-ttu-id="a3c6b-180">탭</span><span class="sxs-lookup"><span data-stu-id="a3c6b-180">Tab</span></span>|  
|<span data-ttu-id="a3c6b-181">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-181">SysTabControl32</span></span>|<span data-ttu-id="a3c6b-182">TabItem</span><span class="sxs-lookup"><span data-stu-id="a3c6b-182">TabItem</span></span>|  
|<span data-ttu-id="a3c6b-183">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-183">ToolbarWindow32</span></span>|<span data-ttu-id="a3c6b-184">ToolBar</span><span class="sxs-lookup"><span data-stu-id="a3c6b-184">ToolBar</span></span>|  
|<span data-ttu-id="a3c6b-185">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-185">ToolbarWindow32</span></span>|<span data-ttu-id="a3c6b-186">MenuItem</span><span class="sxs-lookup"><span data-stu-id="a3c6b-186">MenuItem</span></span>|  
|<span data-ttu-id="a3c6b-187">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-187">ToolbarWindow32</span></span>|<span data-ttu-id="a3c6b-188">단추</span><span class="sxs-lookup"><span data-stu-id="a3c6b-188">Button</span></span>|  
|<span data-ttu-id="a3c6b-189">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-189">ToolbarWindow32</span></span>|<span data-ttu-id="a3c6b-190">CheckBox</span><span class="sxs-lookup"><span data-stu-id="a3c6b-190">CheckBox</span></span>|  
|<span data-ttu-id="a3c6b-191">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-191">ToolbarWindow32</span></span>|<span data-ttu-id="a3c6b-192">RadioButton</span><span class="sxs-lookup"><span data-stu-id="a3c6b-192">RadioButton</span></span>|  
|<span data-ttu-id="a3c6b-193">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-193">ToolbarWindow32</span></span>|<span data-ttu-id="a3c6b-194">구분 기호</span><span class="sxs-lookup"><span data-stu-id="a3c6b-194">Separator</span></span>|  
|<span data-ttu-id="a3c6b-195">tooltips_class32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-195">tooltips_class32</span></span>|<span data-ttu-id="a3c6b-196">도구 설명</span><span class="sxs-lookup"><span data-stu-id="a3c6b-196">ToolTip</span></span>|  
|<span data-ttu-id="a3c6b-197">#32774</span><span class="sxs-lookup"><span data-stu-id="a3c6b-197">#32774</span></span>|<span data-ttu-id="a3c6b-198">도구 설명</span><span class="sxs-lookup"><span data-stu-id="a3c6b-198">ToolTip</span></span>|  
|<span data-ttu-id="a3c6b-199">ReBarWindow32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-199">ReBarWindow32</span></span>|<span data-ttu-id="a3c6b-200">Toolbar</span><span class="sxs-lookup"><span data-stu-id="a3c6b-200">Toolbar</span></span>|  
|<span data-ttu-id="a3c6b-201">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-201">SysTreeView32</span></span>|<span data-ttu-id="a3c6b-202">Tree</span><span class="sxs-lookup"><span data-stu-id="a3c6b-202">Tree</span></span>|  
|<span data-ttu-id="a3c6b-203">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-203">SysTreeView32</span></span>|<span data-ttu-id="a3c6b-204">TreeItem</span><span class="sxs-lookup"><span data-stu-id="a3c6b-204">TreeItem</span></span>|  
  
 <span data-ttu-id="a3c6b-205">**참고** RichEdit 컨트롤은 [!INCLUDE[TLA#tla_winvista](../../../includes/tlasharptla-winvista-md.md)] 와 함께 제공된 버전에서만 지원됩니다(RichEd20.dll 버전 3.1 이상 및 MsftEdit.dll 버전 4.1 이상).</span><span class="sxs-lookup"><span data-stu-id="a3c6b-205">**Note** The RichEdit control is supported only for versions shipped with [!INCLUDE[TLA#tla_winvista](../../../includes/tlasharptla-winvista-md.md)] (in RichEd20.dll version 3.1 and later, and MsftEdit.dll version 4.1 and later).</span></span>  
  
 <span data-ttu-id="a3c6b-206">다음 컨트롤은 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c6b-206">The following controls are not supported.</span></span>  
  
|<span data-ttu-id="a3c6b-207">클래스 이름</span><span class="sxs-lookup"><span data-stu-id="a3c6b-207">Class name</span></span>|<span data-ttu-id="a3c6b-208">컨트롤 종류</span><span class="sxs-lookup"><span data-stu-id="a3c6b-208">Control type</span></span>|  
|----------------|------------------|  
|<span data-ttu-id="a3c6b-209">SysAnimate32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-209">SysAnimate32</span></span>|<span data-ttu-id="a3c6b-210">이미지</span><span class="sxs-lookup"><span data-stu-id="a3c6b-210">Image</span></span>|  
|<span data-ttu-id="a3c6b-211">SysPager</span><span class="sxs-lookup"><span data-stu-id="a3c6b-211">SysPager</span></span>|<span data-ttu-id="a3c6b-212">Spinner</span><span class="sxs-lookup"><span data-stu-id="a3c6b-212">Spinner</span></span>|  
|<span data-ttu-id="a3c6b-213">SysDateTimePick32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-213">SysDateTimePick32</span></span>|<span data-ttu-id="a3c6b-214">사용자 지정</span><span class="sxs-lookup"><span data-stu-id="a3c6b-214">Custom</span></span>|  
|<span data-ttu-id="a3c6b-215">SysMonthCal32</span><span class="sxs-lookup"><span data-stu-id="a3c6b-215">SysMonthCal32</span></span>|<span data-ttu-id="a3c6b-216">일정</span><span class="sxs-lookup"><span data-stu-id="a3c6b-216">Calendar</span></span>|  
|<span data-ttu-id="a3c6b-217">MS_WINNOTE</span><span class="sxs-lookup"><span data-stu-id="a3c6b-217">MS_WINNOTE</span></span>|<span data-ttu-id="a3c6b-218">도구 설명</span><span class="sxs-lookup"><span data-stu-id="a3c6b-218">Tooltip</span></span>|  
|<span data-ttu-id="a3c6b-219">VBBubble</span><span class="sxs-lookup"><span data-stu-id="a3c6b-219">VBBubble</span></span>|<span data-ttu-id="a3c6b-220">도구 설명</span><span class="sxs-lookup"><span data-stu-id="a3c6b-220">Tooltip</span></span>|  
|<span data-ttu-id="a3c6b-221">스크롤 막대(독립 실행형 컨트롤로 사용되는 경우)</span><span class="sxs-lookup"><span data-stu-id="a3c6b-221">ScrollBar (when used as a standalone control)</span></span>|<span data-ttu-id="a3c6b-222">슬라이더</span><span class="sxs-lookup"><span data-stu-id="a3c6b-222">Slider</span></span>|  
|<span data-ttu-id="a3c6b-223">SuperGrid</span><span class="sxs-lookup"><span data-stu-id="a3c6b-223">SuperGrid</span></span>|<span data-ttu-id="a3c6b-224">사용자 지정</span><span class="sxs-lookup"><span data-stu-id="a3c6b-224">Custom</span></span>|  
  
<a name="Windows_Forms_Controls"></a>   
## <a name="windows-forms-controls"></a><span data-ttu-id="a3c6b-225">Windows Forms 컨트롤</span><span class="sxs-lookup"><span data-stu-id="a3c6b-225">Windows Forms Controls</span></span>  
 <span data-ttu-id="a3c6b-226">Windows Forms 컨트롤에 노출 되어 [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] UIAutomationClientsideProviders.dll의 클라이언트쪽 공급자를 통해.</span><span class="sxs-lookup"><span data-stu-id="a3c6b-226">Windows Forms controls are exposed to [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] through client-side providers in UIAutomationClientsideProviders.dll.</span></span> <span data-ttu-id="a3c6b-227">이 어셈블리는 UI 자동화 클라이언트 응용 프로그램과 함께 사용할 수 있도록 자동으로 등록됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c6b-227">This assembly is automatically registered for use with UI Automation client applications.</span></span>  
  
 <span data-ttu-id="a3c6b-228">Windows Forms 컨트롤에 대 한 래퍼를 관리 하는 일반적으로 [!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)] 공용 컨트롤에서 지 원하는 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c6b-228">Typically, Windows Forms controls that are managed wrappers for [!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)] common controls are supported by [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)].</span></span> <span data-ttu-id="a3c6b-229">다음과 같은 컨트롤이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c6b-229">The following controls are supported.</span></span>  
  
|<span data-ttu-id="a3c6b-230">클래스 이름</span><span class="sxs-lookup"><span data-stu-id="a3c6b-230">Class Name</span></span>|  
|----------------|  
|<span data-ttu-id="a3c6b-231">단추</span><span class="sxs-lookup"><span data-stu-id="a3c6b-231">Button</span></span>|  
|<span data-ttu-id="a3c6b-232">CheckBox</span><span class="sxs-lookup"><span data-stu-id="a3c6b-232">CheckBox</span></span>|  
|<span data-ttu-id="a3c6b-233">CheckedListBox</span><span class="sxs-lookup"><span data-stu-id="a3c6b-233">CheckedListBox</span></span>|  
|<span data-ttu-id="a3c6b-234">ColorDialog</span><span class="sxs-lookup"><span data-stu-id="a3c6b-234">ColorDialog</span></span>|  
|<span data-ttu-id="a3c6b-235">ComboBox</span><span class="sxs-lookup"><span data-stu-id="a3c6b-235">ComboBox</span></span>|  
|<span data-ttu-id="a3c6b-236">FolderBrowser</span><span class="sxs-lookup"><span data-stu-id="a3c6b-236">FolderBrowser</span></span>|  
|<span data-ttu-id="a3c6b-237">FontDialog</span><span class="sxs-lookup"><span data-stu-id="a3c6b-237">FontDialog</span></span>|  
|<span data-ttu-id="a3c6b-238">GroupBox</span><span class="sxs-lookup"><span data-stu-id="a3c6b-238">GroupBox</span></span>|  
|<span data-ttu-id="a3c6b-239">HscrollBar</span><span class="sxs-lookup"><span data-stu-id="a3c6b-239">HscrollBar</span></span>|  
|<span data-ttu-id="a3c6b-240">ImageList</span><span class="sxs-lookup"><span data-stu-id="a3c6b-240">ImageList</span></span>|  
|<span data-ttu-id="a3c6b-241">레이블</span><span class="sxs-lookup"><span data-stu-id="a3c6b-241">Label</span></span>|  
|<span data-ttu-id="a3c6b-242">ListBox</span><span class="sxs-lookup"><span data-stu-id="a3c6b-242">ListBox</span></span>|  
|<span data-ttu-id="a3c6b-243">ListView</span><span class="sxs-lookup"><span data-stu-id="a3c6b-243">ListView</span></span>|  
|<span data-ttu-id="a3c6b-244">MainMenu/ContextMenu</span><span class="sxs-lookup"><span data-stu-id="a3c6b-244">MainMenu/ContextMenu</span></span>|  
|<span data-ttu-id="a3c6b-245">MonthCalendar</span><span class="sxs-lookup"><span data-stu-id="a3c6b-245">MonthCalendar</span></span>|  
|<span data-ttu-id="a3c6b-246">NotifyIcon</span><span class="sxs-lookup"><span data-stu-id="a3c6b-246">NotifyIcon</span></span>|  
|<span data-ttu-id="a3c6b-247">OpenFileDialog</span><span class="sxs-lookup"><span data-stu-id="a3c6b-247">OpenFileDialog</span></span>|  
|<span data-ttu-id="a3c6b-248">PageSetupDialog</span><span class="sxs-lookup"><span data-stu-id="a3c6b-248">PageSetupDialog</span></span>|  
|<span data-ttu-id="a3c6b-249">PrintDialog</span><span class="sxs-lookup"><span data-stu-id="a3c6b-249">PrintDialog</span></span>|  
|<span data-ttu-id="a3c6b-250">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="a3c6b-250">ProgressBar</span></span>|  
|<span data-ttu-id="a3c6b-251">RadioButton</span><span class="sxs-lookup"><span data-stu-id="a3c6b-251">RadioButton</span></span>|  
|<span data-ttu-id="a3c6b-252">RichTextBox</span><span class="sxs-lookup"><span data-stu-id="a3c6b-252">RichTextBox</span></span>|  
|<span data-ttu-id="a3c6b-253">SaveFileDialog</span><span class="sxs-lookup"><span data-stu-id="a3c6b-253">SaveFileDialog</span></span>|  
|<span data-ttu-id="a3c6b-254">ScrollableControl</span><span class="sxs-lookup"><span data-stu-id="a3c6b-254">ScrollableControl</span></span>|  
|<span data-ttu-id="a3c6b-255">SoundPlayer</span><span class="sxs-lookup"><span data-stu-id="a3c6b-255">SoundPlayer</span></span>|  
|<span data-ttu-id="a3c6b-256">StatusBar</span><span class="sxs-lookup"><span data-stu-id="a3c6b-256">StatusBar</span></span>|  
|<span data-ttu-id="a3c6b-257">TabControl/TabPage</span><span class="sxs-lookup"><span data-stu-id="a3c6b-257">TabControl/TabPage</span></span>|  
|<span data-ttu-id="a3c6b-258">TextBox</span><span class="sxs-lookup"><span data-stu-id="a3c6b-258">TextBox</span></span>|  
|<span data-ttu-id="a3c6b-259">Timer</span><span class="sxs-lookup"><span data-stu-id="a3c6b-259">Timer</span></span>|  
|<span data-ttu-id="a3c6b-260">ToolBar</span><span class="sxs-lookup"><span data-stu-id="a3c6b-260">Toolbar</span></span>|  
|<span data-ttu-id="a3c6b-261">도구 설명</span><span class="sxs-lookup"><span data-stu-id="a3c6b-261">ToolTip</span></span>|  
|<span data-ttu-id="a3c6b-262">TrackBar</span><span class="sxs-lookup"><span data-stu-id="a3c6b-262">TrackBar</span></span>|  
|<span data-ttu-id="a3c6b-263">TreeView</span><span class="sxs-lookup"><span data-stu-id="a3c6b-263">TreeView</span></span>|  
|<span data-ttu-id="a3c6b-264">VscrollBar</span><span class="sxs-lookup"><span data-stu-id="a3c6b-264">VscrollBar</span></span>|  
|<span data-ttu-id="a3c6b-265">웹 브라우저</span><span class="sxs-lookup"><span data-stu-id="a3c6b-265">WebBrowser</span></span>|  
  
 <span data-ttu-id="a3c6b-266">다음 컨트롤은 [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] 에 대한 지원을 통해서만 [!INCLUDE[TLA#tla_aa](../../../includes/tlasharptla-aa-md.md)]에 노출됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c6b-266">The following controls are exposed to [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] only through their support for [!INCLUDE[TLA#tla_aa](../../../includes/tlasharptla-aa-md.md)].</span></span> <span data-ttu-id="a3c6b-267">일부 기능은 사용하지 못할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c6b-267">Some functionality may not be available.</span></span>  
  
|<span data-ttu-id="a3c6b-268">컨트롤 이름</span><span class="sxs-lookup"><span data-stu-id="a3c6b-268">Control Name</span></span>|  
|------------------|  
|<span data-ttu-id="a3c6b-269">BindingSource</span><span class="sxs-lookup"><span data-stu-id="a3c6b-269">BindingSource</span></span>|  
|<span data-ttu-id="a3c6b-270">DataGrid</span><span class="sxs-lookup"><span data-stu-id="a3c6b-270">DataGrid</span></span>|  
|<span data-ttu-id="a3c6b-271">DataGridView</span><span class="sxs-lookup"><span data-stu-id="a3c6b-271">DataGridView</span></span>|  
|<span data-ttu-id="a3c6b-272">DataNavigator</span><span class="sxs-lookup"><span data-stu-id="a3c6b-272">DataNavigator</span></span>|  
|<span data-ttu-id="a3c6b-273">DomainUpDown</span><span class="sxs-lookup"><span data-stu-id="a3c6b-273">DomainUpDown</span></span>|  
|<span data-ttu-id="a3c6b-274">ErrorProvider</span><span class="sxs-lookup"><span data-stu-id="a3c6b-274">ErrorProvider</span></span>|  
|<span data-ttu-id="a3c6b-275">FlowLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="a3c6b-275">FlowLayoutPanel</span></span>|  
|<span data-ttu-id="a3c6b-276">Form</span><span class="sxs-lookup"><span data-stu-id="a3c6b-276">Form</span></span>|  
|<span data-ttu-id="a3c6b-277">LinkLabel</span><span class="sxs-lookup"><span data-stu-id="a3c6b-277">LinkLabel</span></span>|  
|<span data-ttu-id="a3c6b-278">HelpProvider</span><span class="sxs-lookup"><span data-stu-id="a3c6b-278">HelpProvider</span></span>|  
|<span data-ttu-id="a3c6b-279">MaskedTextBox</span><span class="sxs-lookup"><span data-stu-id="a3c6b-279">MaskedTextBox</span></span>|  
|<span data-ttu-id="a3c6b-280">MenuStrip/ContextMenuStrip</span><span class="sxs-lookup"><span data-stu-id="a3c6b-280">MenuStrip/ContextMenuStrip</span></span>|  
|<span data-ttu-id="a3c6b-281">NumericUpDown</span><span class="sxs-lookup"><span data-stu-id="a3c6b-281">NumericUpDown</span></span>|  
|<span data-ttu-id="a3c6b-282">패널</span><span class="sxs-lookup"><span data-stu-id="a3c6b-282">Panel</span></span>|  
|<span data-ttu-id="a3c6b-283">PictureBox</span><span class="sxs-lookup"><span data-stu-id="a3c6b-283">PictureBox</span></span>|  
|<span data-ttu-id="a3c6b-284">PrintDocument</span><span class="sxs-lookup"><span data-stu-id="a3c6b-284">PrintDocument</span></span>|  
|<span data-ttu-id="a3c6b-285">PrintPreview-Control</span><span class="sxs-lookup"><span data-stu-id="a3c6b-285">PrintPreview-Control</span></span>|  
|<span data-ttu-id="a3c6b-286">PrintPreview-Dialog</span><span class="sxs-lookup"><span data-stu-id="a3c6b-286">PrintPreview-Dialog</span></span>|  
|<span data-ttu-id="a3c6b-287">PropertyGrid</span><span class="sxs-lookup"><span data-stu-id="a3c6b-287">PropertyGrid</span></span>|  
|<span data-ttu-id="a3c6b-288">UserControl</span><span class="sxs-lookup"><span data-stu-id="a3c6b-288">UserControl</span></span>|  
|<span data-ttu-id="a3c6b-289">ToolStrip</span><span class="sxs-lookup"><span data-stu-id="a3c6b-289">ToolStrip</span></span>|  
|<span data-ttu-id="a3c6b-290">TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="a3c6b-290">TableLayoutPanel</span></span>|  
|<span data-ttu-id="a3c6b-291">SplitContainer/SplitterPanel</span><span class="sxs-lookup"><span data-stu-id="a3c6b-291">SplitContainer/SplitterPanel</span></span>|  
|<span data-ttu-id="a3c6b-292">분할자</span><span class="sxs-lookup"><span data-stu-id="a3c6b-292">Splitter</span></span>|  
|<span data-ttu-id="a3c6b-293">RaftingContainer</span><span class="sxs-lookup"><span data-stu-id="a3c6b-293">RaftingContainer</span></span>|  
|<span data-ttu-id="a3c6b-294">StatusStrip</span><span class="sxs-lookup"><span data-stu-id="a3c6b-294">StatusStrip</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a3c6b-295">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a3c6b-295">See Also</span></span>  
 [<span data-ttu-id="a3c6b-296">UI 자동화 컨트롤 형식</span><span class="sxs-lookup"><span data-stu-id="a3c6b-296">UI Automation Control Types</span></span>](../../../docs/framework/ui-automation/ui-automation-control-types.md)
