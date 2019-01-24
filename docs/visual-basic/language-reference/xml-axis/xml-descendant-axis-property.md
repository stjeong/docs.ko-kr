---
title: XML 하위 항목 축 속성(Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.XmlPropertyDescendantsAxis
helpviewer_keywords:
- Visual Basic code, accessing XML
- XML descendant axis property [Visual Basic]
- descendant axis property [Visual Baisc]
- XML axis [Visual Basic], descendant
- XML [Visual Basic], accessing
ms.assetid: a178f85b-5d54-438f-8479-40b62af6fe76
ms.openlocfilehash: 3b8d13e606f28896cae88162d572470e49af3739
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54730284"
---
# <a name="xml-descendant-axis-property-visual-basic"></a><span data-ttu-id="cf460-102">XML 하위 항목 축 속성(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="cf460-102">XML Descendant Axis Property (Visual Basic)</span></span>
<span data-ttu-id="cf460-103">다음의 하위 항목에 액세스할 수:는 <xref:System.Xml.Linq.XElement> 개체를 <xref:System.Xml.Linq.XDocument> 개체의 컬렉션인 <xref:System.Xml.Linq.XElement> 개체나 컬렉션 <xref:System.Xml.Linq.XDocument> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-103">Provides access to the descendants of the following: an <xref:System.Xml.Linq.XElement> object, an <xref:System.Xml.Linq.XDocument> object, a collection of <xref:System.Xml.Linq.XElement> objects, or a collection of <xref:System.Xml.Linq.XDocument> objects.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cf460-104">구문</span><span class="sxs-lookup"><span data-stu-id="cf460-104">Syntax</span></span>  
  
```  
object...<descendant>  
```  
  
## <a name="parts"></a><span data-ttu-id="cf460-105">요소</span><span class="sxs-lookup"><span data-stu-id="cf460-105">Parts</span></span>  
 `object`  
 <span data-ttu-id="cf460-106">필수 요소.</span><span class="sxs-lookup"><span data-stu-id="cf460-106">Required.</span></span> <span data-ttu-id="cf460-107"><xref:System.Xml.Linq.XElement> 개체, <xref:System.Xml.Linq.XDocument> 개체, <xref:System.Xml.Linq.XElement> 개체의 컬렉션 또는 <xref:System.Xml.Linq.XDocument> 개체의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-107">An <xref:System.Xml.Linq.XElement> object, an <xref:System.Xml.Linq.XDocument> object, a collection of <xref:System.Xml.Linq.XElement> objects, or a collection of <xref:System.Xml.Linq.XDocument> objects.</span></span>  
  
 <span data-ttu-id="cf460-108">...<</span><span class="sxs-lookup"><span data-stu-id="cf460-108">...<</span></span>  
 <span data-ttu-id="cf460-109">필수 요소.</span><span class="sxs-lookup"><span data-stu-id="cf460-109">Required.</span></span> <span data-ttu-id="cf460-110">하위 축 속성의 시작을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-110">Denotes the start of a descendant axis property.</span></span>  
  
 `descendant`  
 <span data-ttu-id="cf460-111">필수 요소.</span><span class="sxs-lookup"><span data-stu-id="cf460-111">Required.</span></span> <span data-ttu-id="cf460-112">폼에 액세스 하려면 하위 노드의 이름을 [`prefix``:`]`name`합니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-112">Name of the descendant nodes to access, of the form [`prefix``:`]`name`.</span></span>  
  
|<span data-ttu-id="cf460-113">파트</span><span class="sxs-lookup"><span data-stu-id="cf460-113">Part</span></span>|<span data-ttu-id="cf460-114">설명</span><span class="sxs-lookup"><span data-stu-id="cf460-114">Description</span></span>|  
|----------|-----------------|  
|`prefix`|<span data-ttu-id="cf460-115">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-115">Optional.</span></span> <span data-ttu-id="cf460-116">하위 노드에 대 한 XML 네임 스페이스 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-116">XML namespace prefix for the descendant node.</span></span> <span data-ttu-id="cf460-117">사용 하 여 정의 된 전역 XML 네임 스페이스 여야는 `Imports` 문입니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-117">Must be a global XML namespace that is defined by using an `Imports` statement.</span></span>|  
|`name`|<span data-ttu-id="cf460-118">필수 요소.</span><span class="sxs-lookup"><span data-stu-id="cf460-118">Required.</span></span> <span data-ttu-id="cf460-119">하위 노드의 로컬 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-119">Local name of the descendant node.</span></span> <span data-ttu-id="cf460-120">참조 [선언 된 XML 요소 및 특성의 이름을](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md)입니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-120">See [Names of Declared XML Elements and Attributes](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).</span></span>|  
  
 \>  
 <span data-ttu-id="cf460-121">필수 요소.</span><span class="sxs-lookup"><span data-stu-id="cf460-121">Required.</span></span> <span data-ttu-id="cf460-122">하위 축 속성의 끝을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-122">Denotes the end of a descendant axis property.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cf460-123">반환 값</span><span class="sxs-lookup"><span data-stu-id="cf460-123">Return Value</span></span>  
 <span data-ttu-id="cf460-124"><xref:System.Xml.Linq.XElement> 개체의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-124">A collection of <xref:System.Xml.Linq.XElement> objects.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cf460-125">설명</span><span class="sxs-lookup"><span data-stu-id="cf460-125">Remarks</span></span>  
 <span data-ttu-id="cf460-126">이름으로 하위 노드에 액세스 하는 XML 하위 축 속성을 사용할 수는 <xref:System.Xml.Linq.XElement> 또는 <xref:System.Xml.Linq.XDocument> 개체 또는 컬렉션 <xref:System.Xml.Linq.XElement> 또는 <xref:System.Xml.Linq.XDocument> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-126">You can use an XML descendant axis property to access descendant nodes by name from an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument> object, or from a collection of <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument> objects.</span></span> <span data-ttu-id="cf460-127">XML을 사용 하 여 `Value` 반환된 된 컬렉션의 첫 번째 하위 노드의 값에 액세스 하는 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-127">Use the XML `Value` property to access the value of the first descendant node in the returned collection.</span></span> <span data-ttu-id="cf460-128">자세한 내용은 [XML 값 속성](../../../visual-basic/language-reference/xml-axis/xml-value-property.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-128">For more information, see [XML Value Property](../../../visual-basic/language-reference/xml-axis/xml-value-property.md).</span></span>  
  
 <span data-ttu-id="cf460-129">Visual Basic 컴파일러는 하위 항목 축 속성에 대 한 호출으로 변환 합니다는 <xref:System.Xml.Linq.XContainer.Descendants%2A> 메서드.</span><span class="sxs-lookup"><span data-stu-id="cf460-129">The Visual Basic compiler converts descendant axis properties into calls to the <xref:System.Xml.Linq.XContainer.Descendants%2A> method.</span></span>  
  
## <a name="xml-namespaces"></a><span data-ttu-id="cf460-130">XML 네임스페이스</span><span class="sxs-lookup"><span data-stu-id="cf460-130">XML Namespaces</span></span>  
 <span data-ttu-id="cf460-131">하위 축 속성의 이름을 사용 하 여 전역적으로 선언 된 XML 네임 스페이스만 사용할 수는 `Imports` 문입니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-131">The name in a descendant axis property can use only XML namespaces declared globally with the `Imports` statement.</span></span> <span data-ttu-id="cf460-132">XML 요소 리터럴 내에서 로컬로 선언 된 XML 네임 스페이스를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-132">It cannot use XML namespaces declared locally within XML element literals.</span></span> <span data-ttu-id="cf460-133">자세한 내용은 [Imports 문 (XML Namespace)](../../../visual-basic/language-reference/statements/imports-statement-xml-namespace.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-133">For more information, see [Imports Statement (XML Namespace)](../../../visual-basic/language-reference/statements/imports-statement-xml-namespace.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="cf460-134">예제</span><span class="sxs-lookup"><span data-stu-id="cf460-134">Example</span></span>  
 <span data-ttu-id="cf460-135">다음 예제에서는 명명 된 첫 번째 하위 노드의 값에 액세스 하는 방법을 보여 줍니다 `name` 이라는 모든 하위 노드의 값 `phone` 에서 `contacts` 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-135">The following example shows how to access the value of the first descendant node named `name` and the values of all descendant nodes named `phone` from the `contacts` object.</span></span>  
  
 [!code-vb[VbXMLSamples#25](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-descendant-axis-property_1.vb)]  
  
 <span data-ttu-id="cf460-136">이 코드의 텍스트는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-136">This code displays the following text:</span></span>  
  
 `Name: Patrick Hines`  
  
 `Home Phone = 206-555-0144`  
  
## <a name="example"></a><span data-ttu-id="cf460-137">예제</span><span class="sxs-lookup"><span data-stu-id="cf460-137">Example</span></span>  
 <span data-ttu-id="cf460-138">다음 예제에서는 `ns`를 XML 네임스페이스 접두사로 선언한 다음</span><span class="sxs-lookup"><span data-stu-id="cf460-138">The following example declares `ns` as an XML namespace prefix.</span></span> <span data-ttu-id="cf460-139">다음 네임 스페이스의 접두사는 XML 리터럴을 만들고 정규화 된 이름 사용 하 여 첫 번째 자식 노드의 값에 액세스를 사용 하 여 `ns:name`입니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-139">It then uses the prefix of the namespace to create an XML literal and access the value of the first child node with the qualified name `ns:name`.</span></span>  
  
 [!code-vb[VbXMLSamples#26](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-descendant-axis-property_2.vb)]  
  
 <span data-ttu-id="cf460-140">이 코드의 텍스트는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cf460-140">This code displays the following text:</span></span>  
  
 `Name: Patrick Hines`  
  
## <a name="see-also"></a><span data-ttu-id="cf460-141">참고자료</span><span class="sxs-lookup"><span data-stu-id="cf460-141">See also</span></span>
- <xref:System.Xml.Linq.XElement>
- [<span data-ttu-id="cf460-142">XML 축 속성</span><span class="sxs-lookup"><span data-stu-id="cf460-142">XML Axis Properties</span></span>](../../../visual-basic/language-reference/xml-axis/index.md)
- [<span data-ttu-id="cf460-143">XML 리터럴</span><span class="sxs-lookup"><span data-stu-id="cf460-143">XML Literals</span></span>](../../../visual-basic/language-reference/xml-literals/index.md)
- [<span data-ttu-id="cf460-144">Visual Basic에서 XML 만들기</span><span class="sxs-lookup"><span data-stu-id="cf460-144">Creating XML in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
- [<span data-ttu-id="cf460-145">선언된 XML 요소 및 특성의 이름</span><span class="sxs-lookup"><span data-stu-id="cf460-145">Names of Declared XML Elements and Attributes</span></span>](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md)
