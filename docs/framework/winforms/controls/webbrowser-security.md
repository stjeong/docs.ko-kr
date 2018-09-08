---
title: WebBrowser 보안
ms.date: 03/30/2017
helpviewer_keywords:
- WebBrowser control [Windows Forms], security
- security [Windows Forms], WebBrowser control
ms.assetid: 0968846e-48ee-485a-9797-65b5b9a622f8
ms.openlocfilehash: 683c6ad4cbc55a889f4a0c1d20ebe8e8a2669a13
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44062733"
---
# <a name="webbrowser-security"></a><span data-ttu-id="6a4ab-102">WebBrowser 보안</span><span class="sxs-lookup"><span data-stu-id="6a4ab-102">WebBrowser Security</span></span>
<span data-ttu-id="6a4ab-103"><xref:System.Windows.Forms.WebBrowser> 컨트롤은 완전 신뢰 수준에서 작동 하도록 설계 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6a4ab-103">The <xref:System.Windows.Forms.WebBrowser> control is designed to work in full trust only.</span></span> <span data-ttu-id="6a4ab-104">컨트롤에 표시 된 HTML 콘텐츠를 외부 웹 서버에서 가져올 수 있습니다 하 고 스크립트 또는 웹 컨트롤의 형태로 비관리 코드를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a4ab-104">The HTML content displayed in the control can come from external Web servers and may contain unmanaged code in the form of scripts or Web controls.</span></span> <span data-ttu-id="6a4ab-105">사용 하는 경우는 <xref:System.Windows.Forms.WebBrowser> 이 이런 컨트롤에서에서 컨트롤은 있지만 관리 되는 Internet Explorer를 사용할 때 보다 덜 안전 <xref:System.Windows.Forms.WebBrowser> 컨트롤 사용 해도 이러한 비관리 코드 실행에서 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a4ab-105">If you use the <xref:System.Windows.Forms.WebBrowser> control in this situation, the control is no less secure than Internet Explorer would be, but the managed <xref:System.Windows.Forms.WebBrowser> control does not prevent such unmanaged code from running.</span></span>  
  
 <span data-ttu-id="6a4ab-106">내부 ActiveX와 관련 된 보안 문제에 대 한 자세한 내용은 `WebBrowser` 제어를 참조 하십시오 [WebBrowser 컨트롤](https://go.microsoft.com/fwlink/?LinkId=198812)합니다.</span><span class="sxs-lookup"><span data-stu-id="6a4ab-106">For more information about security issues relating to the underlying ActiveX `WebBrowser` control, see [WebBrowser Control](https://go.microsoft.com/fwlink/?LinkId=198812).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6a4ab-107">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6a4ab-107">See Also</span></span>  
 <xref:System.Windows.Forms.WebBrowser>  
 [<span data-ttu-id="6a4ab-108">WebBrowser 컨트롤 개요</span><span class="sxs-lookup"><span data-stu-id="6a4ab-108">WebBrowser Control Overview</span></span>](../../../../docs/framework/winforms/controls/webbrowser-control-overview.md)  
 [<span data-ttu-id="6a4ab-109">WebBrowser 컨트롤</span><span class="sxs-lookup"><span data-stu-id="6a4ab-109">WebBrowser Control</span></span>](https://go.microsoft.com/fwlink/?LinkId=198812)
