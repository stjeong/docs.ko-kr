---
title: '연습: WPF에서 Direct3D9 콘텐츠 호스팅'
ms.date: 03/30/2017
helpviewer_keywords:
- Direct3D9 [WPF interoperability], hosting Direct3D9 content
- WPF [WPF], hosting Direct3D9 content
ms.assetid: 60983736-0ab5-42cc-8b16-e9fbde261a43
ms.openlocfilehash: 5e7edfbeb9a3cddcdcd81d9c87e5e85bfc947339
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44188711"
---
# <a name="walkthrough-hosting-direct3d9-content-in-wpf"></a><span data-ttu-id="cf435-102">연습: WPF에서 Direct3D9 콘텐츠 호스팅</span><span class="sxs-lookup"><span data-stu-id="cf435-102">Walkthrough: Hosting Direct3D9 Content in WPF</span></span>
<span data-ttu-id="cf435-103">이 연습에서는 Windows Presentation Foundation (WPF) 응용 프로그램에서 호스팅할 Direct3D9 콘텐츠를 호스트 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-103">This walkthrough shows how to host Direct3D9 content in a Windows Presentation Foundation (WPF) application.</span></span>  
  
 <span data-ttu-id="cf435-104">이 연습에서는 다음 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-104">In this walkthrough, you perform the following tasks:</span></span>  
  
-   <span data-ttu-id="cf435-105">Direct3D9 콘텐츠를 호스트할 WPF 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-105">Create a WPF project to host the Direct3D9 content.</span></span>  
  
-   <span data-ttu-id="cf435-106">Direct3D9 콘텐츠를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-106">Import the Direct3D9 content.</span></span>  
  
-   <span data-ttu-id="cf435-107">Direct3D9 콘텐츠를 사용 하 여 표시 된 <xref:System.Windows.Interop.D3DImage> 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-107">Display the Direct3D9 content by using the <xref:System.Windows.Interop.D3DImage> class.</span></span>  
  
 <span data-ttu-id="cf435-108">작업을 완료 하는 경우에 WPF 응용 프로그램에서 호스팅할 Direct3D9 콘텐츠를 호스트 하는 방법을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-108">When you are finished, you will know how to host Direct3D9 content in a WPF application.</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="cf435-109">전제 조건</span><span class="sxs-lookup"><span data-stu-id="cf435-109">Prerequisites</span></span>  
 <span data-ttu-id="cf435-110">이 연습을 완료하려면 다음 구성 요소가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-110">You need the following components to complete this walkthrough:</span></span>  
  
-   [!INCLUDE[vs_dev10_long](../../../../includes/vs-dev10-long-md.md)]<span data-ttu-id="cf435-111">.</span><span class="sxs-lookup"><span data-stu-id="cf435-111">.</span></span>  
  
-   <span data-ttu-id="cf435-112">DirectX SDK 9 이상입니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-112">DirectX SDK 9 or later.</span></span>  
  
-   <span data-ttu-id="cf435-113">WPF와 호환 가능한 형식에서 호스팅할 Direct3D9 콘텐츠를 포함 하는 DLL입니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-113">A DLL that contains Direct3D9 content in a WPF-compatible format.</span></span> <span data-ttu-id="cf435-114">자세한 내용은 [WPF 및 Direct3D9 상호 운용성](../../../../docs/framework/wpf/advanced/wpf-and-direct3d9-interoperation.md) 하 고 [연습: WPF에서 호스팅에 대 한 Direct3D9 콘텐츠 만들기](../../../../docs/framework/wpf/advanced/walkthrough-creating-direct3d9-content-for-hosting-in-wpf.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-114">For more information, see [WPF and Direct3D9 Interoperation](../../../../docs/framework/wpf/advanced/wpf-and-direct3d9-interoperation.md) and [Walkthrough: Creating Direct3D9 Content for Hosting in WPF](../../../../docs/framework/wpf/advanced/walkthrough-creating-direct3d9-content-for-hosting-in-wpf.md).</span></span>  
  
## <a name="creating-the-wpf-project"></a><span data-ttu-id="cf435-115">WPF 프로젝트 만들기</span><span class="sxs-lookup"><span data-stu-id="cf435-115">Creating the WPF Project</span></span>  
 <span data-ttu-id="cf435-116">첫 번째 단계는 WPF 응용 프로그램에 대 한 프로젝트를 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-116">The first step is to create the project for the WPF application.</span></span>  
  
#### <a name="to-create-the-wpf-project"></a><span data-ttu-id="cf435-117">WPF 프로젝트를 만들려면</span><span class="sxs-lookup"><span data-stu-id="cf435-117">To create the WPF project</span></span>  
  
-   <span data-ttu-id="cf435-118">새 WPF 응용 프로그램 프로젝트 만들기의 Visual C# `D3DHost`합니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-118">Create a new WPF Application project in Visual C# named `D3DHost`.</span></span> <span data-ttu-id="cf435-119">자세한 내용은 [방법: 새 WPF 응용 프로그램 프로젝트 만들기](https://msdn.microsoft.com/library/1f6aea7a-33e1-4d3f-8555-1daa42e95d82)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cf435-119">For more information, see [How to: Create a New WPF Application Project](https://msdn.microsoft.com/library/1f6aea7a-33e1-4d3f-8555-1daa42e95d82).</span></span>  
  
     <span data-ttu-id="cf435-120">MainWindow.xaml 열립니다는 [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)]합니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-120">MainWindow.xaml opens in the [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)].</span></span>  
  
## <a name="importing-the-direct3d9-content"></a><span data-ttu-id="cf435-121">Direct3D9 콘텐츠 가져오기</span><span class="sxs-lookup"><span data-stu-id="cf435-121">Importing the Direct3D9 Content</span></span>  
 <span data-ttu-id="cf435-122">사용 하 여 관리 되지 않는 DLL에서 호스팅할 Direct3D9 콘텐츠를 가져오기는 `DllImport` 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-122">You import the Direct3D9 content from an unmanaged DLL by using the `DllImport` attribute.</span></span>  
  
#### <a name="to-import-direct3d9-content"></a><span data-ttu-id="cf435-123">Direct3D9 콘텐츠를 가져오려면</span><span class="sxs-lookup"><span data-stu-id="cf435-123">To import Direct3D9 content</span></span>  
  
1.  <span data-ttu-id="cf435-124">코드 편집기에서 MainWindow.xaml.cs를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-124">Open MainWindow.xaml.cs in the Code Editor.</span></span>  
  
2.  <span data-ttu-id="cf435-125">자동으로 생성 된 코드를 다음 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-125">Replace the automatically generated code with the following code.</span></span>  
  
     [!code-csharp[System.Windows.Interop.D3DImage#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/CS/window1.xaml.cs#1)]  
  
## <a name="hosting-the-direct3d9-content"></a><span data-ttu-id="cf435-126">Direct3D9 콘텐츠 호스팅</span><span class="sxs-lookup"><span data-stu-id="cf435-126">Hosting the Direct3D9 Content</span></span>  
 <span data-ttu-id="cf435-127">마지막으로 사용 하는 <xref:System.Windows.Interop.D3DImage> Direct3D9 콘텐츠를 호스트 하는 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-127">Finally, use the <xref:System.Windows.Interop.D3DImage> class to host the Direct3D9 content.</span></span>  
  
#### <a name="to-host-the-direct3d9-content"></a><span data-ttu-id="cf435-128">Direct3D9 콘텐츠를 호스트 하려면</span><span class="sxs-lookup"><span data-stu-id="cf435-128">To host the Direct3D9 content</span></span>  
  
1.  <span data-ttu-id="cf435-129">MainWindow.xaml에 다음 XAML을 사용 하 여 자동으로 생성 된 XAML을 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-129">In MainWindow.xaml, replace the automatically generated XAML with the following XAML.</span></span>  
  
     [!code-xaml[System.Windows.Interop.D3DImage#10](../../../../samples/snippets/csharp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/CS/window1.xaml#10)]  
  
2.  <span data-ttu-id="cf435-130">프로젝트를 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-130">Build the project.</span></span>  
  
3.  <span data-ttu-id="cf435-131">Direct3D9 콘텐츠 bin/Debug 폴더를 포함 하는 DLL을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-131">Copy the DLL that contains the Direct3D9 content to the bin/Debug folder.</span></span>  
  
4.  <span data-ttu-id="cf435-132">F5 키를 눌러 프로젝트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-132">Press F5 to run the project.</span></span>  
  
     <span data-ttu-id="cf435-133">WPF 응용 프로그램 내에서 호스팅할 Direct3D9 콘텐츠 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf435-133">The Direct3D9 content appears within the WPF application.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cf435-134">참고 항목</span><span class="sxs-lookup"><span data-stu-id="cf435-134">See Also</span></span>  
 <xref:System.Windows.Interop.D3DImage>  
 [<span data-ttu-id="cf435-135">Direct3D9 및 WPF 상호 운용성을 위한 성능 고려 사항</span><span class="sxs-lookup"><span data-stu-id="cf435-135">Performance Considerations for Direct3D9 and WPF Interoperability</span></span>](../../../../docs/framework/wpf/advanced/performance-considerations-for-direct3d9-and-wpf-interoperability.md)
