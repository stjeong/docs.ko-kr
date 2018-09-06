---
title: '&lt;주의&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <remarks> XML tag
- remarks XML tag
ms.assetid: c6241773-a7ed-41c9-9a8b-9722a0c606a9
ms.openlocfilehash: 97fca8758d9c21ac0b8f15bf9d5831750fbabe77
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43863035"
---
# <a name="ltremarksgt-visual-basic"></a><span data-ttu-id="87a57-102">&lt;주의&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="87a57-102">&lt;remarks&gt; (Visual Basic)</span></span>
<span data-ttu-id="87a57-103">멤버에 대 한 설명 부분을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="87a57-103">Specifies a remarks section for the member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="87a57-104">구문</span><span class="sxs-lookup"><span data-stu-id="87a57-104">Syntax</span></span>  
  
```xml  
<remarks>description</remarks>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="87a57-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="87a57-105">Parameters</span></span>  
 `description`  
 <span data-ttu-id="87a57-106">멤버에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="87a57-106">A description of the member.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="87a57-107">설명</span><span class="sxs-lookup"><span data-stu-id="87a57-107">Remarks</span></span>  
 <span data-ttu-id="87a57-108">사용 된 `<remarks>` 태그를 사용 하 여 지정 된 정보를 보완 하는 형식에 대 한 정보를 추가 [ \<요약 >](../../../visual-basic/language-reference/xmldoc/summary.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="87a57-108">Use the `<remarks>` tag to add information about a type, supplementing the information specified with [\<summary>](../../../visual-basic/language-reference/xmldoc/summary.md).</span></span>  
  
 <span data-ttu-id="87a57-109">이 정보는 개체 브라우저에 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="87a57-109">This information appears in the Object Browser.</span></span> <span data-ttu-id="87a57-110">개체 브라우저에 대 한 정보를 참조 하세요 [코드 구조 보기](/visualstudio/ide/viewing-the-structure-of-code)합니다.</span><span class="sxs-lookup"><span data-stu-id="87a57-110">For information about the Object Browser, see [Viewing the Structure of Code](/visualstudio/ide/viewing-the-structure-of-code).</span></span>  
  
 <span data-ttu-id="87a57-111">[/doc](../../../visual-basic/reference/command-line-compiler/doc.md)로 컴파일하여 문서 주석을 파일로 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="87a57-111">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="87a57-112">예제</span><span class="sxs-lookup"><span data-stu-id="87a57-112">Example</span></span>  
 <span data-ttu-id="87a57-113">이 예제에서는 `<remarks>` 기능을 설명 하는 태그를 `UpdateRecord` 메서드는 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87a57-113">This example uses the `<remarks>` tag to explain what the `UpdateRecord` method does.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/remarks_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="87a57-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="87a57-114">See Also</span></span>  
 [<span data-ttu-id="87a57-115">XML 주석 태그</span><span class="sxs-lookup"><span data-stu-id="87a57-115">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
