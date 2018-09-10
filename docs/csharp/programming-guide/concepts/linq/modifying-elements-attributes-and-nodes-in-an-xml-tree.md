---
title: XML 트리에서 요소, 특성 및 노드 수정3
ms.date: 07/20/2015
ms.assetid: 0ed22e4e-4c6b-4eb1-b0eb-06685efd8c33
ms.openlocfilehash: 9567d0c6c5cd4853eeb2a86066cd1a805f20a031
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43777352"
---
# <a name="modifying-elements-attributes-and-nodes-in-an-xml-tree"></a><span data-ttu-id="3dc61-102">XML 트리에서 요소, 특성 및 노드 수정</span><span class="sxs-lookup"><span data-stu-id="3dc61-102">Modifying Elements, Attributes, and Nodes in an XML Tree</span></span>
<span data-ttu-id="3dc61-103">다음 표에는 요소, 해당 요소의 자식 요소 또는 특성을 수정하는 데 사용할 수 있는 메서드와 속성이 요약되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-103">The following table summarizes the methods and properties that you can use to modify an element, its child elements, or its attributes.</span></span>  
  
 <span data-ttu-id="3dc61-104">다음 메서드는 <xref:System.Xml.Linq.XElement>를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-104">The following methods modify an <xref:System.Xml.Linq.XElement>.</span></span>  
  
|<span data-ttu-id="3dc61-105">메서드</span><span class="sxs-lookup"><span data-stu-id="3dc61-105">Method</span></span>|<span data-ttu-id="3dc61-106">설명</span><span class="sxs-lookup"><span data-stu-id="3dc61-106">Description</span></span>|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XElement.Parse%2A?displayProperty=nameWithType>|<span data-ttu-id="3dc61-107">요소를 구문 분석된 XML로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-107">Replaces an element with parsed XML.</span></span>|  
|<xref:System.Xml.Linq.XElement.RemoveAll%2A?displayProperty=nameWithType>|<span data-ttu-id="3dc61-108">요소의 모든 내용(자식 노드와 특성)을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-108">Removes all content (child nodes and attributes) of an element.</span></span>|  
|<xref:System.Xml.Linq.XElement.RemoveAttributes%2A?displayProperty=nameWithType>|<span data-ttu-id="3dc61-109">요소의 특성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-109">Removes the attributes of an element.</span></span>|  
|<xref:System.Xml.Linq.XElement.ReplaceAll%2A?displayProperty=nameWithType>|<span data-ttu-id="3dc61-110">요소의 모든 내용(자식 노드와 특성)을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-110">Replaces all content (child nodes and attributes) of an element.</span></span>|  
|<xref:System.Xml.Linq.XElement.ReplaceAttributes%2A?displayProperty=nameWithType>|<span data-ttu-id="3dc61-111">요소의 특성을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-111">Replaces the attributes of an element.</span></span>|  
|<xref:System.Xml.Linq.XElement.SetAttributeValue%2A?displayProperty=nameWithType>|<span data-ttu-id="3dc61-112">특성의 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-112">Sets the value of an attribute.</span></span> <span data-ttu-id="3dc61-113">특성이 없으면 특성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-113">Creates the attribute if it doesn't exist.</span></span> <span data-ttu-id="3dc61-114">값이 `null`로 설정되어 있으면 특성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-114">If the value is set to `null`, removes the attribute.</span></span>|  
|<xref:System.Xml.Linq.XElement.SetElementValue%2A?displayProperty=nameWithType>|<span data-ttu-id="3dc61-115">자식 요소의 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-115">Sets the value of a child element.</span></span> <span data-ttu-id="3dc61-116">요소가 없으면 요소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-116">Creates the element if it doesn't exist.</span></span> <span data-ttu-id="3dc61-117">값이 `null`로 설정되어 있으면 요소를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-117">If the value is set to `null`, removes the element.</span></span>|  
|<xref:System.Xml.Linq.XElement.Value%2A?displayProperty=nameWithType>|<span data-ttu-id="3dc61-118">요소의 내용(자식 노드)을 지정된 텍스트로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-118">Replaces the content (child nodes) of an element with the specified text.</span></span>|  
|<xref:System.Xml.Linq.XElement.SetValue%2A?displayProperty=nameWithType>|<span data-ttu-id="3dc61-119">요소의 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-119">Sets the value of an element.</span></span>|  
  
 <span data-ttu-id="3dc61-120">다음 메서드는 <xref:System.Xml.Linq.XAttribute>를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-120">The following methods modify an <xref:System.Xml.Linq.XAttribute>.</span></span>  
  
|<span data-ttu-id="3dc61-121">메서드</span><span class="sxs-lookup"><span data-stu-id="3dc61-121">Method</span></span>|<span data-ttu-id="3dc61-122">설명</span><span class="sxs-lookup"><span data-stu-id="3dc61-122">Description</span></span>|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XAttribute.Value%2A?displayProperty=nameWithType>|<span data-ttu-id="3dc61-123">특성의 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-123">Sets the value of an attribute.</span></span>|  
|<xref:System.Xml.Linq.XAttribute.SetValue%2A?displayProperty=nameWithType>|<span data-ttu-id="3dc61-124">특성의 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-124">Sets the value of an attribute.</span></span>|  
  
 <span data-ttu-id="3dc61-125">다음 메서드는 <xref:System.Xml.Linq.XNode>(<xref:System.Xml.Linq.XElement> 또는 <xref:System.Xml.Linq.XDocument> 포함)를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-125">The following methods modify an <xref:System.Xml.Linq.XNode> (including an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument>).</span></span>  
  
|<span data-ttu-id="3dc61-126">메서드</span><span class="sxs-lookup"><span data-stu-id="3dc61-126">Method</span></span>|<span data-ttu-id="3dc61-127">설명</span><span class="sxs-lookup"><span data-stu-id="3dc61-127">Description</span></span>|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XNode.ReplaceWith%2A?displayProperty=nameWithType>|<span data-ttu-id="3dc61-128">노드를 새 내용으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-128">Replaces a node with new content.</span></span>|  
  
 <span data-ttu-id="3dc61-129">다음 메서드는 <xref:System.Xml.Linq.XContainer>(<xref:System.Xml.Linq.XElement> 또는 <xref:System.Xml.Linq.XDocument>)를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-129">The following methods modify an <xref:System.Xml.Linq.XContainer> (an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument>).</span></span>  
  
|<span data-ttu-id="3dc61-130">메서드</span><span class="sxs-lookup"><span data-stu-id="3dc61-130">Method</span></span>|<span data-ttu-id="3dc61-131">설명</span><span class="sxs-lookup"><span data-stu-id="3dc61-131">Description</span></span>|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XContainer.ReplaceNodes%2A?displayProperty=nameWithType>|<span data-ttu-id="3dc61-132">자식 노드를 새 내용으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="3dc61-132">Replaces the children nodes with new content.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3dc61-133">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3dc61-133">See Also</span></span>

- [<span data-ttu-id="3dc61-134">XML 트리 수정(LINQ to XML)(C#)</span><span class="sxs-lookup"><span data-stu-id="3dc61-134">Modifying XML Trees (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/modifying-xml-trees-linq-to-xml.md)
