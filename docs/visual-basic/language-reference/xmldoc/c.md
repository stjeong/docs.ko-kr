---
title: '&lt;c&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- c XML tag
- <c> XML tag
ms.assetid: 36ad5d1b-11f7-4012-8932-41962ac327d1
ms.openlocfilehash: 06c6899895f278fdf652725a05ecc7229805f4d4
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42935360"
---
# <a name="ltcgt-visual-basic"></a><span data-ttu-id="d4548-102">&lt;c&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d4548-102">&lt;c&gt; (Visual Basic)</span></span>
<span data-ttu-id="d4548-103">설명 내의 텍스트가 코드 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d4548-103">Indicates that text within a description is code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d4548-104">구문</span><span class="sxs-lookup"><span data-stu-id="d4548-104">Syntax</span></span>  
  
```xml  
<c>text</c>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d4548-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d4548-105">Parameters</span></span>  
  
|<span data-ttu-id="d4548-106">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d4548-106">Parameter</span></span>|<span data-ttu-id="d4548-107">설명</span><span class="sxs-lookup"><span data-stu-id="d4548-107">Description</span></span>|  
|---|---|  
|`text`|<span data-ttu-id="d4548-108">코드로 표시하려는 텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="d4548-108">The text you would like to indicate as code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d4548-109">설명</span><span class="sxs-lookup"><span data-stu-id="d4548-109">Remarks</span></span>  
 <span data-ttu-id="d4548-110">`<c>` 태그 하면 설명 내의 텍스트가 코드로 표시 되어야 합니다는 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4548-110">The `<c>` tag gives you a way to indicate that text within a description should be marked as code.</span></span> <span data-ttu-id="d4548-111">여러 줄을 코드로 지정하려면 [\<code>](../../../visual-basic/language-reference/xmldoc/code.md)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d4548-111">Use [\<code>](../../../visual-basic/language-reference/xmldoc/code.md) to indicate multiple lines as code.</span></span>  
  
 <span data-ttu-id="d4548-112">[/doc](../../../visual-basic/reference/command-line-compiler/doc.md)로 컴파일하여 문서 주석을 파일로 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="d4548-112">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d4548-113">예</span><span class="sxs-lookup"><span data-stu-id="d4548-113">Example</span></span>  
 <span data-ttu-id="d4548-114">이 예제에서는 합니다 `<c>` 나타내는 요약 섹션에서 태그 `Counter` 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="d4548-114">This example uses the `<c>` tag in the summary section to indicate that `Counter` is code.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#1](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/c_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="d4548-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d4548-115">See Also</span></span>  
 [<span data-ttu-id="d4548-116">XML 주석 태그</span><span class="sxs-lookup"><span data-stu-id="d4548-116">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
