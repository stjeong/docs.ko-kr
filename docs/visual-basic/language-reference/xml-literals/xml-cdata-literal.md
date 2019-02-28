---
title: XML CDATA 리터럴(Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.XmlLiteralCdata
helpviewer_keywords:
- CDATA literal [Visual Basic]
- XML CDATA literal [Visual Basic]
- XML literals [Visual Basic], CDATA
ms.assetid: 9eafb6a4-dd9d-4866-85e8-0654c65abc44
ms.openlocfilehash: 01a505130d566ec88a6d87e5e9ad525e449d7298
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56981246"
---
# <a name="xml-cdata-literal-visual-basic"></a><span data-ttu-id="d815e-102">XML CDATA 리터럴(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d815e-102">XML CDATA Literal (Visual Basic)</span></span>
<span data-ttu-id="d815e-103">리터럴 나타내는 <xref:System.Xml.Linq.XCData> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d815e-103">A literal representing an <xref:System.Xml.Linq.XCData> object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d815e-104">구문</span><span class="sxs-lookup"><span data-stu-id="d815e-104">Syntax</span></span>  
  
```xml  
<![CDATA[content]]>  
```  
  
## <a name="parts"></a><span data-ttu-id="d815e-105">요소</span><span class="sxs-lookup"><span data-stu-id="d815e-105">Parts</span></span>  
 `<![CDATA[`  
 <span data-ttu-id="d815e-106">필수 요소.</span><span class="sxs-lookup"><span data-stu-id="d815e-106">Required.</span></span> <span data-ttu-id="d815e-107">XML CDATA 섹션의 시작을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d815e-107">Denotes the start of the XML CDATA section.</span></span>  
  
 `content`  
 <span data-ttu-id="d815e-108">필수 요소.</span><span class="sxs-lookup"><span data-stu-id="d815e-108">Required.</span></span> <span data-ttu-id="d815e-109">XML CDATA 섹션에 표시할 텍스트 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="d815e-109">Text content to appear in the XML CDATA section.</span></span>  
  
 `]]>`  
 <span data-ttu-id="d815e-110">필수 요소.</span><span class="sxs-lookup"><span data-stu-id="d815e-110">Required.</span></span> <span data-ttu-id="d815e-111">섹션의 끝을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d815e-111">Denotes the end of the section.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d815e-112">반환 값</span><span class="sxs-lookup"><span data-stu-id="d815e-112">Return Value</span></span>  
 <span data-ttu-id="d815e-113"><xref:System.Xml.Linq.XCData> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d815e-113">An <xref:System.Xml.Linq.XCData> object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d815e-114">설명</span><span class="sxs-lookup"><span data-stu-id="d815e-114">Remarks</span></span>  
 <span data-ttu-id="d815e-115">XML CDATA 섹션에는 포함 하지만 구문 분석 되지 포함 하는 XML을 사용 하 여 해야 하는 원시 텍스트를 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d815e-115">XML CDATA sections contain raw text that should be included, but not parsed, with the XML that contains it.</span></span> <span data-ttu-id="d815e-116">XML CDATA 섹션 모든 텍스트를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d815e-116">A XML CDATA section can contain any text.</span></span> <span data-ttu-id="d815e-117">예약 된 XML 문자를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="d815e-117">This includes reserved XML characters.</span></span> <span data-ttu-id="d815e-118">XML CDATA 섹션 종료 시퀀스를 사용 하 여 "]] >"입니다.</span><span class="sxs-lookup"><span data-stu-id="d815e-118">The XML CDATA section ends with the sequence "]]>".</span></span> <span data-ttu-id="d815e-119">이 다음 사항을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="d815e-119">This implies the following points:</span></span>  
  
-   <span data-ttu-id="d815e-120">포함된 식 구분 기호는 유효한 XML CDATA 내용 때문에 XML CDATA 리터럴 포함된 식을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d815e-120">You cannot use an embedded expression in an XML CDATA literal because the embedded expression delimiters are valid XML CDATA content.</span></span>  
  
-   <span data-ttu-id="d815e-121">XML CDATA 섹션 중첩 될 수 없으므로 있으므로 `content` 값을 포함할 수 없습니다 "]] >"입니다.</span><span class="sxs-lookup"><span data-stu-id="d815e-121">XML CDATA sections cannot be nested, because `content` cannot contain the value "]]>".</span></span>  
  
 <span data-ttu-id="d815e-122">XML 주석 리터럴에서 변수에 할당할 수도 있고 XML 요소 리터럴에 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d815e-122">You can assign an XML CDATA literal to a variable, or include it in an XML element literal.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d815e-123">XML 리터럴을 여러 줄으로 나누어 입력할 수 있지만 줄 연속 문자를 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d815e-123">An XML literal can span multiple lines but does not use line continuation characters.</span></span> <span data-ttu-id="d815e-124">이 옵션을 사용 하면 XML 문서에서 콘텐츠를 복사 하 고 Visual Basic 프로그램에 직접 붙여넣을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d815e-124">This enables you to copy content from an XML document and paste it directly into a Visual Basic program.</span></span>  
  
 <span data-ttu-id="d815e-125">Visual Basic 컴파일러를 호출 하는 XML CDATA 리터럴 변환 된 <xref:System.Xml.Linq.XCData.%23ctor%2A> 생성자입니다.</span><span class="sxs-lookup"><span data-stu-id="d815e-125">The Visual Basic compiler converts the XML CDATA literal to a call to the <xref:System.Xml.Linq.XCData.%23ctor%2A> constructor.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d815e-126">예제</span><span class="sxs-lookup"><span data-stu-id="d815e-126">Example</span></span>  
 <span data-ttu-id="d815e-127">다음 예제에서는 텍스트를 포함 하는 CDATA 섹션 "리터럴 포함 될 수 있습니다 \<XML > 태그"입니다.</span><span class="sxs-lookup"><span data-stu-id="d815e-127">The following example creates a CDATA section that contains the text "Can contain literal \<XML> tags".</span></span>  
  
 [!code-vb[VbXMLSamples#23](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples11.vb#23)]  
  
## <a name="see-also"></a><span data-ttu-id="d815e-128">참고자료</span><span class="sxs-lookup"><span data-stu-id="d815e-128">See also</span></span>
- <xref:System.Xml.Linq.XCData>
- [<span data-ttu-id="d815e-129">XML 요소 리터럴</span><span class="sxs-lookup"><span data-stu-id="d815e-129">XML Element Literal</span></span>](../../../visual-basic/language-reference/xml-literals/xml-element-literal.md)
- [<span data-ttu-id="d815e-130">XML 리터럴</span><span class="sxs-lookup"><span data-stu-id="d815e-130">XML Literals</span></span>](../../../visual-basic/language-reference/xml-literals/index.md)
- [<span data-ttu-id="d815e-131">Visual Basic에서 XML 만들기</span><span class="sxs-lookup"><span data-stu-id="d815e-131">Creating XML in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
