---
title: .NET Framework로 Windows 기반 클라이언트 응용 프로그램 개발
ms.date: 01/09/2018
helpviewer_keywords:
- client application services
- applications [Windows Forms]
- Windows Presentation Foundation, in Visual Studio
- WPF, in Visual Studio
- Windows applications
- rich client applications
- .NET applications, Windows applications
- Visual Basic code, creating applications
- Visual C#, creating applications
- client/server applications, Windows applications
ms.assetid: 2dfb50b7-5af2-4e12-9bbb-c5ade0e39a68
ms.openlocfilehash: 27bd71d4caf59a44a45c70217aa351cf43a5c1c7
ms.sourcegitcommit: fd8d4587cc26e53f0e27e230d6e27d828ef4306b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2018
ms.locfileid: "49349123"
---
# <a name="developing-client-applications-with-the-net-framework"></a><span data-ttu-id="66ba5-102">.NET Framework로 클라이언트 응용 프로그램 개발</span><span class="sxs-lookup"><span data-stu-id="66ba5-102">Developing client applications with the .NET Framework</span></span>

<span data-ttu-id="66ba5-103">.NET Framework를 사용하여 Windows 기반 응용 프로그램을 개발하는 데는 몇 가지 방법이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66ba5-103">There are several ways to develop Windows-based applications with the .NET Framework.</span></span> <span data-ttu-id="66ba5-104">이러한 도구 및 프레임워크 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66ba5-104">You can use any of these tools and frameworks:</span></span> 

* [<span data-ttu-id="66ba5-105">UWP(유니버설 Windows 플랫폼)</span><span class="sxs-lookup"><span data-stu-id="66ba5-105">Universal Windows Platform (UWP)</span></span>](https://developer.microsoft.com/windows/apps)
* [<span data-ttu-id="66ba5-106">WPF(Windows Presentation Foundation)</span><span class="sxs-lookup"><span data-stu-id="66ba5-106">Windows Presentation Foundation (WPF)</span></span>](../../docs/framework/wpf/index.md)
* [<span data-ttu-id="66ba5-107">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="66ba5-107">Windows Forms</span></span>](../../docs/framework/winforms/index.md)

<span data-ttu-id="66ba5-108">이 섹션에는 Windows Presentation Foundation 또는 Windows Forms를 사용하여 Windows 기반 응용 프로그램을 만드는 방법을 설명하는 항목이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66ba5-108">This section contains topics that describe how to create Windows-based applications by using Windows Presentation Foundation or by using Windows Forms.</span></span> <span data-ttu-id="66ba5-109">그러나 .NET Framework를 사용하여 dnpq 응용 프로그램을 만들고 Microsoft 스토어를 통해 사용할 수 있는 컴퓨터 또는 장치용 클라이언트 응용 프로그램을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66ba5-109">However, you can also create web applications using the .NET Framework, and client applications for computers or devices that you make available through the Microsoft Store.</span></span>
 
## <a name="in-this-section"></a><span data-ttu-id="66ba5-110">단원 내용</span><span class="sxs-lookup"><span data-stu-id="66ba5-110">In this section</span></span>

[<span data-ttu-id="66ba5-111">Windows Presentation Foundation</span><span class="sxs-lookup"><span data-stu-id="66ba5-111">Windows Presentation Foundation</span></span>](../../docs/framework/wpf/index.md)  
<span data-ttu-id="66ba5-112">WPF를 사용한 응용 프로그램 개발 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="66ba5-112">Provides information about developing applications by using WPF.</span></span>

[<span data-ttu-id="66ba5-113">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="66ba5-113">Windows Forms</span></span>](../../docs/framework/winforms/index.md)  
<span data-ttu-id="66ba5-114">Windows Forms를 사용한 응용 프로그램 개발 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="66ba5-114">Provides information about developing applications by using Windows Forms.</span></span>

[<span data-ttu-id="66ba5-115">일반 클라이언트 기술</span><span class="sxs-lookup"><span data-stu-id="66ba5-115">Common Client Technologies</span></span>](../../docs/framework/common-client-technologies/index.md)  
<span data-ttu-id="66ba5-116">클라이언트 응용 프로그램을 개발할 때 사용할 수 있는 추가 기술에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="66ba5-116">Provides information about additional technologies that can be used when developing client applications.</span></span>

## <a name="related-sections"></a><span data-ttu-id="66ba5-117">관련 단원</span><span class="sxs-lookup"><span data-stu-id="66ba5-117">Related sections</span></span>

[<span data-ttu-id="66ba5-118">유니버설 Windows 플랫폼</span><span class="sxs-lookup"><span data-stu-id="66ba5-118">Universal Windows Platform</span></span>](https://developer.microsoft.com/windows/apps)  
<span data-ttu-id="66ba5-119">Windows 스토어를 통해 사용자에게 제공할 수 있는 Windows 10용 응용 프로그램을 만드는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="66ba5-119">Describes how to create applications for Windows 10 that you can make available to users through the Windows Store.</span></span>

[<span data-ttu-id="66ba5-120">UWP 앱용 .NET</span><span class="sxs-lookup"><span data-stu-id="66ba5-120">.NET for UWP apps</span></span>](https://msdn.microsoft.com/library/windows/apps/mt185501.aspx)  
<span data-ttu-id="66ba5-121">Windows 컴퓨터와 장치에 배포할 수 있는 스토어 앱에 대한 .NET Framework 지원을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="66ba5-121">Describes the .NET Framework support for Store apps, which can be deployed to Windows computers and devices.</span></span>

<span data-ttu-id="66ba5-122">[Windows Phone Silverlight용 .NET API](https://docs.microsoft.com/previous-versions/windows/apps/jj207211\(v=vs.105\))</span><span class="sxs-lookup"><span data-stu-id="66ba5-122">[.NET API for Windows Phone Silverlight](https://docs.microsoft.com/previous-versions/windows/apps/jj207211\(v=vs.105\))</span></span>  
<span data-ttu-id="66ba5-123">Windows Phone Silverlight로 앱을 빌드하는 데 사용할 수 있는 .NET Framework API를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="66ba5-123">Lists the .NET Framework APIs you can use for building apps with Windows Phone Silverlight.</span></span>
  
[<span data-ttu-id="66ba5-124">여러 플랫폼 개발</span><span class="sxs-lookup"><span data-stu-id="66ba5-124">Developing for Multiple Platforms</span></span>](../../docs/standard/cross-platform/index.md)  
<span data-ttu-id="66ba5-125">.NET Framework를 사용하여 여러 클라이언트 앱 형식을 대상으로 지정할 수 있는 다양한 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="66ba5-125">Describes the different methods you can use the .NET Framework to target multiple client app types.</span></span>

[<span data-ttu-id="66ba5-126">ASP.NET 웹 사이트 시작</span><span class="sxs-lookup"><span data-stu-id="66ba5-126">Get Started with ASP.NET Web Sites</span></span>](https://www.asp.net/get-started/websites)  
<span data-ttu-id="66ba5-127">ASP.NET을 사용하여 웹앱을 개발할 수 있는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="66ba5-127">Describes the ways you can develop web apps using ASP.NET.</span></span>

## <a name="see-also"></a><span data-ttu-id="66ba5-128">참고 항목</span><span class="sxs-lookup"><span data-stu-id="66ba5-128">See also</span></span>

[<span data-ttu-id="66ba5-129">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="66ba5-129">.NET Standard</span></span>](../../docs/standard/net-standard.md)  
[<span data-ttu-id="66ba5-130">개요</span><span class="sxs-lookup"><span data-stu-id="66ba5-130">Overview</span></span>](../../docs/framework/get-started/overview.md)  
[<span data-ttu-id="66ba5-131">개발 가이드</span><span class="sxs-lookup"><span data-stu-id="66ba5-131">Development Guide</span></span>](../../docs/framework/development-guide.md)  
[<span data-ttu-id="66ba5-132">Windows 서비스 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="66ba5-132">Windows Service Applications</span></span>](../../docs/framework/windows-services/index.md)  
