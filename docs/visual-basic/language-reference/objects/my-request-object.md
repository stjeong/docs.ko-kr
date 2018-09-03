---
title: My.Request 개체 (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- My.MyWebExtension.Request
- My.Request
helpviewer_keywords:
- My.Request object
ms.assetid: 93d5f0e2-6b60-4a2c-8652-d90216f6ad10
ms.openlocfilehash: f2c43afb723944293907d0efbb4cf3cc66a40e1e
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43485614"
---
# <a name="myrequest-object"></a><span data-ttu-id="5e1db-102">My.Request 개체</span><span class="sxs-lookup"><span data-stu-id="5e1db-102">My.Request Object</span></span>
<span data-ttu-id="5e1db-103">요청된 페이지에 대한 <xref:System.Web.HttpRequest> 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5e1db-103">Gets the <xref:System.Web.HttpRequest> object for the requested page.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5e1db-104">설명</span><span class="sxs-lookup"><span data-stu-id="5e1db-104">Remarks</span></span>  
 <span data-ttu-id="5e1db-105">`My.Request` 개체에는 현재 HTTP 요청에 대한 정보가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e1db-105">The `My.Request` object contains information about the current HTTP request.</span></span>  
  
 <span data-ttu-id="5e1db-106">`My.Request` 개체는 ASP.NET 응용 프로그램에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e1db-106">The `My.Request` object is available only for ASP.NET applications.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5e1db-107">예제</span><span class="sxs-lookup"><span data-stu-id="5e1db-107">Example</span></span>  
 <span data-ttu-id="5e1db-108">다음 예제에서 헤더 컬렉션을 가져옵니다 합니다 `My.Request` 사용 하 여 개체를 `My.Response` ASP.NET 페이지에 쓸 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5e1db-108">The following example gets the header collection from the `My.Request` object and uses the `My.Response` object to write it to the ASP.NET page.</span></span>  
  
 [!code-vb[VbVbalrMyWeb#1](../../../visual-basic/language-reference/objects/codesnippet/VisualBasic/my-request-object_1.aspx)]  
  
## <a name="see-also"></a><span data-ttu-id="5e1db-109">참고 항목</span><span class="sxs-lookup"><span data-stu-id="5e1db-109">See Also</span></span>  
 <xref:System.Web.HttpRequest>  
 [<span data-ttu-id="5e1db-110">My.Response 개체</span><span class="sxs-lookup"><span data-stu-id="5e1db-110">My.Response Object</span></span>](../../../visual-basic/language-reference/objects/my-response-object.md)
