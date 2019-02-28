---
title: <example> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- example XML tag
- <example> XML tag
ms.assetid: 90eeda1c-3fc4-427c-879c-5046d265a97c
ms.openlocfilehash: a1dea0bcc40de8dea986e93a25617f607383ec21
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56969221"
---
# <a name="example-visual-basic"></a><span data-ttu-id="a913b-102">\<예제 > (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a913b-102">\<example> (Visual Basic)</span></span>
<span data-ttu-id="a913b-103">멤버에 대 한 예제를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a913b-103">Specifies an example for the member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a913b-104">구문</span><span class="sxs-lookup"><span data-stu-id="a913b-104">Syntax</span></span>  
  
```xml  
<example>description</example>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a913b-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a913b-105">Parameters</span></span>  
 `description`  
 <span data-ttu-id="a913b-106">코드 샘플에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="a913b-106">A description of the code sample.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a913b-107">설명</span><span class="sxs-lookup"><span data-stu-id="a913b-107">Remarks</span></span>  
 <span data-ttu-id="a913b-108">`<example>` 태그는 메서드 또는 기타 라이브러리 멤버를 사용 하는 방법의 예제를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a913b-108">The `<example>` tag lets you specify an example of how to use a method or other library member.</span></span> <span data-ttu-id="a913b-109">여기에는 일반적으로 [\<code>](../../../visual-basic/language-reference/xmldoc/code.md) 태그를 같이 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a913b-109">This commonly involves using the [\<code>](../../../visual-basic/language-reference/xmldoc/code.md) tag.</span></span>  
  
 <span data-ttu-id="a913b-110">[/doc](../../../visual-basic/reference/command-line-compiler/doc.md)로 컴파일하여 문서 주석을 파일로 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="a913b-110">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a913b-111">예제</span><span class="sxs-lookup"><span data-stu-id="a913b-111">Example</span></span>  
 <span data-ttu-id="a913b-112">이 예제에서는 합니다 `<example>` 태그 사용에 대 한 예제를 포함 하는 `ID` 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="a913b-112">This example uses the `<example>` tag to include an example for using the `ID` field.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="a913b-113">참고자료</span><span class="sxs-lookup"><span data-stu-id="a913b-113">See also</span></span>
- [<span data-ttu-id="a913b-114">XML 주석 태그</span><span class="sxs-lookup"><span data-stu-id="a913b-114">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
