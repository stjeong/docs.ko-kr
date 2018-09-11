---
title: '&lt;예외&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <exception> XML tag
- exception XML tag
ms.assetid: c0517549-171e-4dae-ab88-a9c1700b6eee
ms.openlocfilehash: 047805ad91d87550da80448fd10883ae58647bd6
ms.sourcegitcommit: 67de6cb5dd66a19f2180ba7e4d7aecc697f8a963
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44337696"
---
# <a name="ltexceptiongt-visual-basic"></a><span data-ttu-id="48af9-102">&lt;예외&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="48af9-102">&lt;exception&gt; (Visual Basic)</span></span>
<span data-ttu-id="48af9-103">예외를 throw 할 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48af9-103">Specifies which exceptions can be thrown.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="48af9-104">구문</span><span class="sxs-lookup"><span data-stu-id="48af9-104">Syntax</span></span>  
  
```xml  
<exception cref="member">description</exception>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="48af9-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="48af9-105">Parameters</span></span>  
 `member`  
 <span data-ttu-id="48af9-106">현재 컴파일 환경에서 사용할 수 있는 예외에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="48af9-106">A reference to an exception that is available from the current compilation environment.</span></span> <span data-ttu-id="48af9-107">컴파일러는 지정된 예외가 있으며 `member`를 출력 XML의 정식 요소 이름으로 변환하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="48af9-107">The compiler checks that the given exception exists and translates `member` to the canonical element name in the output XML.</span></span> <span data-ttu-id="48af9-108">`member`는 큰따옴표(" ")로 묶어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="48af9-108">`member` must appear within double quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="48af9-109">설명.</span><span class="sxs-lookup"><span data-stu-id="48af9-109">A description.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="48af9-110">설명</span><span class="sxs-lookup"><span data-stu-id="48af9-110">Remarks</span></span>  
 <span data-ttu-id="48af9-111">사용 된 `<exception>` 는 예외를 throw 할 수를 지정 하는 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="48af9-111">Use the `<exception>` tag to specify which exceptions can be thrown.</span></span> <span data-ttu-id="48af9-112">이 태그는 메서드 정의에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="48af9-112">This tag is applied to a method definition.</span></span>  
  
 <span data-ttu-id="48af9-113">[/doc](../../../visual-basic/reference/command-line-compiler/doc.md)로 컴파일하여 문서 주석을 파일로 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="48af9-113">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="48af9-114">예제</span><span class="sxs-lookup"><span data-stu-id="48af9-114">Example</span></span>  
 <span data-ttu-id="48af9-115">이 예제에서는 합니다 `<exception>` 예외를 설명 하는 태그는는 `IntDivide` 함수가 throw 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48af9-115">This example uses the `<exception>` tag to describe an exception that the `IntDivide` function can throw.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#3](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/exception_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="48af9-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="48af9-116">See Also</span></span>  
 [<span data-ttu-id="48af9-117">XML 주석 태그</span><span class="sxs-lookup"><span data-stu-id="48af9-117">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
