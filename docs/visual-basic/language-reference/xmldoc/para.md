---
title: '&lt;para&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <para> XML tag
- para XML tag
ms.assetid: a3a18b6c-6416-4358-94ec-37b22675fd37
ms.openlocfilehash: fa11c713a5ed5793b50865753f8bcdeaabf56e83
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44209697"
---
# <a name="ltparagt-visual-basic"></a><span data-ttu-id="19ee8-102">&lt;para&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="19ee8-102">&lt;para&gt; (Visual Basic)</span></span>
<span data-ttu-id="19ee8-103">콘텐츠를 단락으로 형식이 지정 되었는지 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19ee8-103">Specifies that the content is formatted as a paragraph.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="19ee8-104">구문</span><span class="sxs-lookup"><span data-stu-id="19ee8-104">Syntax</span></span>  
  
```xml  
<para>content</para>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="19ee8-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="19ee8-105">Parameters</span></span>  
 `content`  
 <span data-ttu-id="19ee8-106">단락의 텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="19ee8-106">The text of the paragraph.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="19ee8-107">설명</span><span class="sxs-lookup"><span data-stu-id="19ee8-107">Remarks</span></span>  
 <span data-ttu-id="19ee8-108">합니다 `<para>` 태그와 같은 태그 내에서 사용 하기 위한 것 [ \<요약 >](../../../visual-basic/language-reference/xmldoc/summary.md)를 [ \<설명 >](../../../visual-basic/language-reference/xmldoc/remarks.md), 또는 [ \<반환 >](../../../visual-basic/language-reference/xmldoc/returns.md), 텍스트에 구조를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19ee8-108">The `<para>` tag is for use inside a tag, such as [\<summary>](../../../visual-basic/language-reference/xmldoc/summary.md), [\<remarks>](../../../visual-basic/language-reference/xmldoc/remarks.md), or [\<returns>](../../../visual-basic/language-reference/xmldoc/returns.md), and lets you add structure to the text.</span></span>  
  
 <span data-ttu-id="19ee8-109">[/doc](../../../visual-basic/reference/command-line-compiler/doc.md)로 컴파일하여 문서 주석을 파일로 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="19ee8-109">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="19ee8-110">예제</span><span class="sxs-lookup"><span data-stu-id="19ee8-110">Example</span></span>  
 <span data-ttu-id="19ee8-111">이 예제에서는 합니다 `<para>` 태그에 대 한 설명 부분을 분할 하는 `UpdateRecord` 두 단락 메서드.</span><span class="sxs-lookup"><span data-stu-id="19ee8-111">This example uses the `<para>` tag to split the remarks section for the `UpdateRecord` method into two paragraphs.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/para_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="19ee8-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="19ee8-112">See Also</span></span>  
 [<span data-ttu-id="19ee8-113">XML 주석 태그</span><span class="sxs-lookup"><span data-stu-id="19ee8-113">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
