---
title: My.Response 개체 (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- My.MyWebExtension.Response
- My.Response
helpviewer_keywords:
- My.Response object
ms.assetid: 626359bc-3165-40b4-bfaf-2c610e26eb5b
ms.openlocfilehash: d5f49529a2593093a234babc22f64b591ea3cc61
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43872954"
---
# <a name="myresponse-object"></a><span data-ttu-id="bd159-102">My.Response 개체</span><span class="sxs-lookup"><span data-stu-id="bd159-102">My.Response Object</span></span>
<span data-ttu-id="bd159-103">가져옵니다 합니다 <xref:System.Web.HttpResponse> 연관 된 개체는 <xref:System.Web.UI.Page>합니다.</span><span class="sxs-lookup"><span data-stu-id="bd159-103">Gets the <xref:System.Web.HttpResponse> object associated with the <xref:System.Web.UI.Page>.</span></span> <span data-ttu-id="bd159-104">이 개체를 사용하여 HTTP 응답 데이터를 클라이언트에 보낼 수 있고 이 개체는 해당 응답에 대한 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="bd159-104">This object allows you to send HTTP response data to a client and contains information about that response.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bd159-105">설명</span><span class="sxs-lookup"><span data-stu-id="bd159-105">Remarks</span></span>  
 <span data-ttu-id="bd159-106">합니다 `My.Response` 개체에 현재 포함 되어 <xref:System.Web.HttpResponse> 페이지와 연결 된 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bd159-106">The `My.Response` object contains the current <xref:System.Web.HttpResponse> object associated with the page.</span></span>  
  
 <span data-ttu-id="bd159-107">합니다 `My.Response` 개체는 사용할 수만 [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] 응용 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="bd159-107">The `My.Response` object is only available for [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] applications.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bd159-108">예제</span><span class="sxs-lookup"><span data-stu-id="bd159-108">Example</span></span>  
 <span data-ttu-id="bd159-109">다음 예제에서 헤더 컬렉션을 가져옵니다 합니다 `My.Request` 사용 하 여 개체를 `My.Response` ASP.NET 페이지에 쓸 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bd159-109">The following example gets the header collection from the `My.Request` object and uses the `My.Response` object to write it to the ASP.NET page.</span></span>  
  
 [!code-vb[VbVbalrMyWeb#1](../../../visual-basic/language-reference/objects/codesnippet/VisualBasic/my-response-object_1.aspx)]  
  
## <a name="see-also"></a><span data-ttu-id="bd159-110">참고 항목</span><span class="sxs-lookup"><span data-stu-id="bd159-110">See Also</span></span>  
 <xref:System.Web.HttpResponse>  
 [<span data-ttu-id="bd159-111">My.Request 개체</span><span class="sxs-lookup"><span data-stu-id="bd159-111">My.Request Object</span></span>](../../../visual-basic/language-reference/objects/my-request-object.md)
