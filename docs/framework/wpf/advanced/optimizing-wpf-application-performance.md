---
title: WPF 애플리케이션 성능 최적화
ms.date: 03/30/2017
helpviewer_keywords:
- application rendering [WPF], performance
- application optimization [WPF]
- applications [WPF], optimizing
- WPF application [WPF], optimizing
ms.assetid: ac8c6aa3-3c68-4a24-9827-3b6c829c1ebf
ms.openlocfilehash: 45618e6180cbe0206eb120fc71726d0b8de5f06d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54511590"
---
# <a name="optimizing-wpf-application-performance"></a><span data-ttu-id="31e63-102">WPF 애플리케이션 성능 최적화</span><span class="sxs-lookup"><span data-stu-id="31e63-102">Optimizing WPF Application Performance</span></span>
<span data-ttu-id="31e63-103">이 섹션에 대 한 참조로 제공 됩니다 [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] 응용 프로그램 개발자가 응용 프로그램의 성능을 개선 하는 방법을 찾고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31e63-103">This section is intended as a reference for [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] application developers who are looking for ways to improve the performance of their applications.</span></span> <span data-ttu-id="31e63-104">Microsoft.NET Framework의 새로운 개발자 인지 및 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]를 먼저 잘 이해 해야 플랫폼 모두를 사용 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="31e63-104">If you are a developer who is new to the Microsoft .NET Framework and [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)], you should first familiarize yourself with both platforms.</span></span> <span data-ttu-id="31e63-105">이 섹션에서는 둘 다에 대 한 실무 지식이 있다고 가정 하 고 이미 응용 프로그램을 시작 하 고 실행 충분히 파악 하는 프로그래머에 대 한 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31e63-105">This section assumes working knowledge of both, and is written for programmers who already know enough to get their applications up and running.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="31e63-106">이 섹션에 제공 된 성능 데이터를 기반으로 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] RAM과 ATI Radeon 9700 512를 사용 하 여 2.8ghz PC에서 실행 중인 응용 프로그램 그래픽 카드.</span><span class="sxs-lookup"><span data-stu-id="31e63-106">The performance data provided in this section are based on [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] applications running on a 2.8 GHz PC with 512 RAM and an ATI Radeon 9700 graphics card.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="31e63-107">섹션 내용</span><span class="sxs-lookup"><span data-stu-id="31e63-107">In This Section</span></span>  
 [<span data-ttu-id="31e63-108">응용 프로그램 성능 계획</span><span class="sxs-lookup"><span data-stu-id="31e63-108">Planning for Application Performance</span></span>](../../../../docs/framework/wpf/advanced/planning-for-application-performance.md)  
  
 [<span data-ttu-id="31e63-109">하드웨어 이용</span><span class="sxs-lookup"><span data-stu-id="31e63-109">Taking Advantage of Hardware</span></span>](../../../../docs/framework/wpf/advanced/optimizing-performance-taking-advantage-of-hardware.md)  
  
 [<span data-ttu-id="31e63-110">레이아웃 및 디자인</span><span class="sxs-lookup"><span data-stu-id="31e63-110">Layout and Design</span></span>](../../../../docs/framework/wpf/advanced/optimizing-performance-layout-and-design.md)  
  
 [<span data-ttu-id="31e63-111">2차원 그래픽 및 이미징</span><span class="sxs-lookup"><span data-stu-id="31e63-111">2D Graphics and Imaging</span></span>](../../../../docs/framework/wpf/advanced/optimizing-performance-2d-graphics-and-imaging.md)  
  
 [<span data-ttu-id="31e63-112">개체 동작</span><span class="sxs-lookup"><span data-stu-id="31e63-112">Object Behavior</span></span>](../../../../docs/framework/wpf/advanced/optimizing-performance-object-behavior.md)  
  
 [<span data-ttu-id="31e63-113">응용 프로그램 리소스</span><span class="sxs-lookup"><span data-stu-id="31e63-113">Application Resources</span></span>](../../../../docs/framework/wpf/advanced/optimizing-performance-application-resources.md)  
  
 [<span data-ttu-id="31e63-114">텍스트</span><span class="sxs-lookup"><span data-stu-id="31e63-114">Text</span></span>](../../../../docs/framework/wpf/advanced/optimizing-performance-text.md)  
  
 [<span data-ttu-id="31e63-115">데이터 바인딩</span><span class="sxs-lookup"><span data-stu-id="31e63-115">Data Binding</span></span>](../../../../docs/framework/wpf/advanced/optimizing-performance-data-binding.md)  
  
 [<span data-ttu-id="31e63-116">컨트롤</span><span class="sxs-lookup"><span data-stu-id="31e63-116">Controls</span></span>](../../../../docs/framework/wpf/advanced/optimizing-performance-controls.md)  
  
 [<span data-ttu-id="31e63-117">기타 성능 권장 사항</span><span class="sxs-lookup"><span data-stu-id="31e63-117">Other Performance Recommendations</span></span>](../../../../docs/framework/wpf/advanced/optimizing-performance-other-recommendations.md)  
  
 [<span data-ttu-id="31e63-118">응용 프로그램 시작 시간</span><span class="sxs-lookup"><span data-stu-id="31e63-118">Application Startup Time</span></span>](../../../../docs/framework/wpf/advanced/application-startup-time.md)  
  
## <a name="see-also"></a><span data-ttu-id="31e63-119">참고자료</span><span class="sxs-lookup"><span data-stu-id="31e63-119">See also</span></span>
- <xref:System.Windows.Media.RenderOptions>
- <xref:System.Windows.Media.RenderCapability>
- [<span data-ttu-id="31e63-120">그래픽 렌더링 계층</span><span class="sxs-lookup"><span data-stu-id="31e63-120">Graphics Rendering Tiers</span></span>](../../../../docs/framework/wpf/advanced/graphics-rendering-tiers.md)
- [<span data-ttu-id="31e63-121">WPF 그래픽 렌더링 개요</span><span class="sxs-lookup"><span data-stu-id="31e63-121">WPF Graphics Rendering Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/wpf-graphics-rendering-overview.md)
- [<span data-ttu-id="31e63-122">레이아웃</span><span class="sxs-lookup"><span data-stu-id="31e63-122">Layout</span></span>](../../../../docs/framework/wpf/advanced/layout.md)
- [<span data-ttu-id="31e63-123">WPF의 트리</span><span class="sxs-lookup"><span data-stu-id="31e63-123">Trees in WPF</span></span>](../../../../docs/framework/wpf/advanced/trees-in-wpf.md)
- [<span data-ttu-id="31e63-124">Drawing 개체 개요</span><span class="sxs-lookup"><span data-stu-id="31e63-124">Drawing Objects Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/drawing-objects-overview.md)
- [<span data-ttu-id="31e63-125">DrawingVisual 개체 사용</span><span class="sxs-lookup"><span data-stu-id="31e63-125">Using DrawingVisual Objects</span></span>](../../../../docs/framework/wpf/graphics-multimedia/using-drawingvisual-objects.md)
- [<span data-ttu-id="31e63-126">종속성 속성 개요</span><span class="sxs-lookup"><span data-stu-id="31e63-126">Dependency Properties Overview</span></span>](../../../../docs/framework/wpf/advanced/dependency-properties-overview.md)
- [<span data-ttu-id="31e63-127">Freezable 개체 개요</span><span class="sxs-lookup"><span data-stu-id="31e63-127">Freezable Objects Overview</span></span>](../../../../docs/framework/wpf/advanced/freezable-objects-overview.md)
- [<span data-ttu-id="31e63-128">XAML 리소스</span><span class="sxs-lookup"><span data-stu-id="31e63-128">XAML Resources</span></span>](../../../../docs/framework/wpf/advanced/xaml-resources.md)
- [<span data-ttu-id="31e63-129">WPF의 문서</span><span class="sxs-lookup"><span data-stu-id="31e63-129">Documents in WPF</span></span>](../../../../docs/framework/wpf/advanced/documents-in-wpf.md)
- [<span data-ttu-id="31e63-130">서식 있는 텍스트 그리기</span><span class="sxs-lookup"><span data-stu-id="31e63-130">Drawing Formatted Text</span></span>](../../../../docs/framework/wpf/advanced/drawing-formatted-text.md)
- [<span data-ttu-id="31e63-131">WPF의 입력 체계</span><span class="sxs-lookup"><span data-stu-id="31e63-131">Typography in WPF</span></span>](../../../../docs/framework/wpf/advanced/typography-in-wpf.md)
- [<span data-ttu-id="31e63-132">데이터 바인딩 개요</span><span class="sxs-lookup"><span data-stu-id="31e63-132">Data Binding Overview</span></span>](../../../../docs/framework/wpf/data/data-binding-overview.md)
- [<span data-ttu-id="31e63-133">탐색 개요</span><span class="sxs-lookup"><span data-stu-id="31e63-133">Navigation Overview</span></span>](../../../../docs/framework/wpf/app-development/navigation-overview.md)
- [<span data-ttu-id="31e63-134">애니메이션에 대한 유용한 정보</span><span class="sxs-lookup"><span data-stu-id="31e63-134">Animation Tips and Tricks</span></span>](../../../../docs/framework/wpf/graphics-multimedia/animation-tips-and-tricks.md)
- [<span data-ttu-id="31e63-135">연습: WPF 응용 프로그램에서 응용 프로그램 데이터 캐싱</span><span class="sxs-lookup"><span data-stu-id="31e63-135">Walkthrough: Caching Application Data in a WPF Application</span></span>](../../../../docs/framework/wpf/advanced/walkthrough-caching-application-data-in-a-wpf-application.md)
