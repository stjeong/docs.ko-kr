---
title: '&lt;값&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <value> XML tag
- value XML tag
ms.assetid: 0b84b02e-9e6d-41b5-a926-0d5dc76dacb5
ms.openlocfilehash: ef14836c438cf6a1de300270d9882c1e53e716ee
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43855935"
---
# <a name="ltvaluegt-visual-basic"></a><span data-ttu-id="84269-102">&lt;값&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="84269-102">&lt;value&gt; (Visual Basic)</span></span>
<span data-ttu-id="84269-103">속성의 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="84269-103">Specifies the description of a property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="84269-104">구문</span><span class="sxs-lookup"><span data-stu-id="84269-104">Syntax</span></span>  
  
```xml  
<value>property-description</value>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="84269-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="84269-105">Parameters</span></span>  
 `property-description`  
 <span data-ttu-id="84269-106">속성에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="84269-106">A description for the property.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="84269-107">설명</span><span class="sxs-lookup"><span data-stu-id="84269-107">Remarks</span></span>  
 <span data-ttu-id="84269-108">사용 된 `<value>` 속성을 설명 하는 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="84269-108">Use the `<value>` tag to describe a property.</span></span> <span data-ttu-id="84269-109">Visual Studio 개발 환경에서 코드 마법사를 사용 하는 속성에 추가 하는 추가 된 [ \<요약 >](../../../visual-basic/language-reference/xmldoc/summary.md) 새 속성에 대 한 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="84269-109">Note that when you add a property using the code wizard in the Visual Studio development environment, it will add a [\<summary>](../../../visual-basic/language-reference/xmldoc/summary.md) tag for the new property.</span></span> <span data-ttu-id="84269-110">수동으로 추가 해야 합니다는 `<value>` 속성을 나타내는 값을 설명 하는 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="84269-110">You should then manually add a `<value>` tag to describe the value that the property represents.</span></span>  
  
 <span data-ttu-id="84269-111">[/doc](../../../visual-basic/reference/command-line-compiler/doc.md)로 컴파일하여 문서 주석을 파일로 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="84269-111">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="84269-112">예제</span><span class="sxs-lookup"><span data-stu-id="84269-112">Example</span></span>  
 <span data-ttu-id="84269-113">이 예제에서는 합니다 `<value>` 값에 대해 설명 하는 태그를 `Counter` 속성에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="84269-113">This example uses the `<value>` tag to describe what value the `Counter` property holds.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#1](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/value_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="84269-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="84269-114">See Also</span></span>  
 [<span data-ttu-id="84269-115">XML 주석 태그</span><span class="sxs-lookup"><span data-stu-id="84269-115">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
