---
title: Visual Basic에서 XML에 액세스
ms.date: 07/20/2015
helpviewer_keywords:
- LINQ to XML [Visual Basic], accessing XML
- Visual Basic code, XML
- accessing XML [Visual Basic], axis properties
- XML [Visual Basic], axis properties
- XML [Visual Basic], accessing
ms.assetid: c47f88b2-3cbc-4bb1-b4b9-be60f71ffc6a
ms.openlocfilehash: 0540c52cf3e4cd7594f051c10832ea99cf58a34e
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43734384"
---
# <a name="accessing-xml-in-visual-basic"></a><span data-ttu-id="9c15f-102">Visual Basic에서 XML에 액세스</span><span class="sxs-lookup"><span data-stu-id="9c15f-102">Accessing XML in Visual Basic</span></span>
<span data-ttu-id="9c15f-103">XML 축 속성에 액세스 하 고 탐색을 제공 하는 Visual Basic [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] 구조입니다.</span><span class="sxs-lookup"><span data-stu-id="9c15f-103">Visual Basic provides XML axis properties for accessing and navigating [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] structures.</span></span> <span data-ttu-id="9c15f-104">이러한 속성에는 XML 이름을 지정 하 여 요소 및 특성에 액세스할 수 있도록 특수 구문을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c15f-104">These properties use a special syntax to enable you to access elements and attributes by specifying the XML names.</span></span>  
  
 <span data-ttu-id="9c15f-105">다음 표에서 XML 요소 및 Visual Basic의 특성에 액세스할 수 있도록 하는 언어 기능을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9c15f-105">The following table lists the language features that enable you to access XML elements and attributes in Visual Basic.</span></span>  
  
### <a name="xml-axis-properties"></a><span data-ttu-id="9c15f-106">XML 축 속성</span><span class="sxs-lookup"><span data-stu-id="9c15f-106">XML Axis Properties</span></span>  
  
|<span data-ttu-id="9c15f-107">속성 설명</span><span class="sxs-lookup"><span data-stu-id="9c15f-107">Property description</span></span>|<span data-ttu-id="9c15f-108">예제</span><span class="sxs-lookup"><span data-stu-id="9c15f-108">Example</span></span>|<span data-ttu-id="9c15f-109">설명</span><span class="sxs-lookup"><span data-stu-id="9c15f-109">Description</span></span>|  
|--------------------------|-------------|-----------------|  
|<span data-ttu-id="9c15f-110">*자식 축*</span><span class="sxs-lookup"><span data-stu-id="9c15f-110">*child axis*</span></span>|`contact.<phone>`|<span data-ttu-id="9c15f-111">모든 가져옵니다 `phone` 의 자식 요소는 요소는 `contact` 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="9c15f-111">Gets all `phone` elements that are child elements of the `contact` element.</span></span>|  
|<span data-ttu-id="9c15f-112">*특성 축*</span><span class="sxs-lookup"><span data-stu-id="9c15f-112">*attribute axis*</span></span>|`phone.@type`|<span data-ttu-id="9c15f-113">모든 가져옵니다 `type` 특성을 `phone` 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="9c15f-113">Gets all `type` attributes of the `phone` element.</span></span>|  
|<span data-ttu-id="9c15f-114">*descendant 축*</span><span class="sxs-lookup"><span data-stu-id="9c15f-114">*descendant axis*</span></span>|`contacts...<name>`|<span data-ttu-id="9c15f-115">모두 가져옵니다 `name` 의 요소는 `contacts` 발생 하는 계층 구조에서 얼마나 깊이 관계 없이 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="9c15f-115">Gets all `name` elements of the `contacts` element, regardless of how deep in the hierarchy they occur.</span></span>|  
|<span data-ttu-id="9c15f-116">*확장명 인덱서*</span><span class="sxs-lookup"><span data-stu-id="9c15f-116">*extension indexer*</span></span>|`contacts...<name>(0)`|<span data-ttu-id="9c15f-117">첫 번째 가져옵니다 `name` 시퀀스의 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="9c15f-117">Gets the first `name` element from the sequence.</span></span>|  
|<span data-ttu-id="9c15f-118">*값*</span><span class="sxs-lookup"><span data-stu-id="9c15f-118">*value*</span></span>|`contacts...<name>.Value`|<span data-ttu-id="9c15f-119">시퀀스의 첫 번째 개체의 문자열 표현을 가져옵니다 또는 `Nothing` 시퀀스가 비어 있는 경우.</span><span class="sxs-lookup"><span data-stu-id="9c15f-119">Gets the string representation of the first object in the sequence, or `Nothing` if the sequence is empty.</span></span>|  
  
## <a name="in-this-section"></a><span data-ttu-id="9c15f-120">섹션 내용</span><span class="sxs-lookup"><span data-stu-id="9c15f-120">In This Section</span></span>  
 [<span data-ttu-id="9c15f-121">방법: XML 하위 요소 액세스</span><span class="sxs-lookup"><span data-stu-id="9c15f-121">How to: Access XML Descendant Elements</span></span>](../../../../visual-basic/programming-guide/language-features/xml/how-to-access-xml-descendant-elements.md)  
 <span data-ttu-id="9c15f-122">지정 된 이름이 지정된 된 XML 요소 아래에 포함 된 모든 XML 요소에 액세스 하려면 하위 축 속성을 사용 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9c15f-122">Shows how to use a descendant axis property to access all XML elements that have a specified name and that are contained under a specified XML element.</span></span>  
  
 [<span data-ttu-id="9c15f-123">방법: XML 자식 요소 액세스</span><span class="sxs-lookup"><span data-stu-id="9c15f-123">How to: Access XML Child Elements</span></span>](../../../../visual-basic/programming-guide/language-features/xml/how-to-access-xml-child-elements.md)  
 <span data-ttu-id="9c15f-124">자식을 사용 하는 방법을 XML 요소에 지정 된 이름이 있는 모든 XML 자식 요소에 액세스 하려면 축 속성을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9c15f-124">Shows how to use a child axis property to access all XML child elements that have a specified name in an XML element.</span></span>  
  
 [<span data-ttu-id="9c15f-125">방법: XML 특성 액세스</span><span class="sxs-lookup"><span data-stu-id="9c15f-125">How to: Access XML Attributes</span></span>](../../../../visual-basic/programming-guide/language-features/xml/how-to-access-xml-attributes.md)  
 <span data-ttu-id="9c15f-126">특성 축 속성을 사용 하 여 XML 요소에 지정 된 이름이 있는 모든 XML 특성에 액세스 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9c15f-126">Shows how to use an attribute axis property to access all XML attributes that have a specified name in an XML element.</span></span>  
  
 [<span data-ttu-id="9c15f-127">방법: XML 네임스페이스 접두사 선언 및 사용</span><span class="sxs-lookup"><span data-stu-id="9c15f-127">How to: Declare and Use XML Namespace Prefixes</span></span>](../../../../visual-basic/programming-guide/language-features/xml/how-to-declare-and-use-xml-namespace-prefixes.md)  
 <span data-ttu-id="9c15f-128">XML 네임 스페이스 접두사를 선언 하 고 만들고 XML 요소에 액세스를 사용 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9c15f-128">Shows how to declare an XML namespace prefix and use it to create and access XML elements.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="9c15f-129">관련 단원</span><span class="sxs-lookup"><span data-stu-id="9c15f-129">Related Sections</span></span>  
 [<span data-ttu-id="9c15f-130">XML 축 속성</span><span class="sxs-lookup"><span data-stu-id="9c15f-130">XML Axis Properties</span></span>](../../../../visual-basic/language-reference/xml-axis/index.md)  
 <span data-ttu-id="9c15f-131">다양 한 XML 액세스 속성을 설명 하는 섹션에 대 한 링크를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c15f-131">Provides links to sections describing the various XML access properties.</span></span>  
  
 [<span data-ttu-id="9c15f-132">Visual Basic의 LINQ to XML 개요</span><span class="sxs-lookup"><span data-stu-id="9c15f-132">Overview of LINQ to XML in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/xml/overview-of-linq-to-xml.md)  
 <span data-ttu-id="9c15f-133">사용 하 여 소개 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] Visual Basic의 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c15f-133">Provides an introduction to using [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] in Visual Basic.</span></span>  
  
 [<span data-ttu-id="9c15f-134">Visual Basic에서 XML 만들기</span><span class="sxs-lookup"><span data-stu-id="9c15f-134">Creating XML in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)  
 <span data-ttu-id="9c15f-135">Visual Basic의 XML 리터럴을 사용 하 여 소개를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c15f-135">Provides an introduction to using XML literals in Visual Basic.</span></span>  
  
 [<span data-ttu-id="9c15f-136">Visual Basic에서 XML 조작</span><span class="sxs-lookup"><span data-stu-id="9c15f-136">Manipulating XML in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/xml/manipulating-xml.md)  
 <span data-ttu-id="9c15f-137">로드 하 고 Visual Basic의 XML을 수정 하는 방법에 대 한 섹션에 대 한 링크를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c15f-137">Provides links to sections about loading and modifying XML in Visual Basic.</span></span>  
  
 [<span data-ttu-id="9c15f-138">XML</span><span class="sxs-lookup"><span data-stu-id="9c15f-138">XML</span></span>](../../../../visual-basic/programming-guide/language-features/xml/index.md)  
 <span data-ttu-id="9c15f-139">사용 하는 방법을 설명 하는 섹션에 대 한 링크를 제공 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] Visual Basic의 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c15f-139">Provides links to sections describing how to use [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] in Visual Basic.</span></span>
