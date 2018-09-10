---
title: XPathNavigator를 사용하여 XML 데이터 편집
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: b1f91616-3115-4264-9821-c66589d11d11
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5361ef036d91435b674a1637ac8c2a9a757bf8ab
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44261774"
---
# <a name="editing-xml-data-using-xpathnavigator"></a><span data-ttu-id="b9370-102">XPathNavigator를 사용하여 XML 데이터 편집</span><span class="sxs-lookup"><span data-stu-id="b9370-102">Editing XML Data using XPathNavigator</span></span>
<span data-ttu-id="b9370-103"><xref:System.Xml.XPath.XPathNavigator> 클래스는 <xref:System.Xml.XmlDocument> 개체에 포함된 XML 문서에서 노드와 값을 삽입하거나 수정 및 제거하는 메서드를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b9370-103">The <xref:System.Xml.XPath.XPathNavigator> class provides methods to insert, modify and remove nodes and values from an XML document contained in an <xref:System.Xml.XmlDocument> object.</span></span> <span data-ttu-id="b9370-104">이러한 메서드를 사용하여 노드와 값을 삽입하거나 수정 및 제거하려면 <xref:System.Xml.XPath.XPathNavigator> 개체가 편집 가능한 상태여야 합니다. 즉, <xref:System.Xml.XPath.XPathNavigator.CanEdit%2A> 속성이 true여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9370-104">In order to use any of these methods to insert, modify, and remove nodes and values, the <xref:System.Xml.XPath.XPathNavigator> object must be editable, that is, its <xref:System.Xml.XPath.XPathNavigator.CanEdit%2A> property must be true.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="b9370-105">섹션 내용</span><span class="sxs-lookup"><span data-stu-id="b9370-105">In This Section</span></span>  
 [<span data-ttu-id="b9370-106">XPathNavigator를 사용하여 XML 데이터 삽입</span><span class="sxs-lookup"><span data-stu-id="b9370-106">Insert XML Data using XPathNavigator</span></span>](../../../../docs/standard/data/xml/insert-xml-data-using-xpathnavigator.md)  
 <span data-ttu-id="b9370-107"><xref:System.Xml.XmlDocument> 클래스를 사용하여 형제, 자식, 특성 노드 및 값을 <xref:System.Xml.XPath.XPathNavigator> 개체에 삽입하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b9370-107">Describes how to insert sibling, child, attribute nodes and values in to an <xref:System.Xml.XmlDocument> object using the <xref:System.Xml.XPath.XPathNavigator> class.</span></span>  
  
 [<span data-ttu-id="b9370-108">XPathNavigator를 사용하여 XML 데이터 수정</span><span class="sxs-lookup"><span data-stu-id="b9370-108">Modify XML Data using XPathNavigator</span></span>](../../../../docs/standard/data/xml/modify-xml-data-using-xpathnavigator.md)  
 <span data-ttu-id="b9370-109"><xref:System.Xml.XmlDocument> 클래스를 사용하여 <xref:System.Xml.XPath.XPathNavigator> 개체에서 노드와 값을 수정하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b9370-109">Describes how to modify nodes and values in an <xref:System.Xml.XmlDocument> object using the <xref:System.Xml.XPath.XPathNavigator> class.</span></span>  
  
 [<span data-ttu-id="b9370-110">XPathNavigator를 사용하여 XML 데이터 제거</span><span class="sxs-lookup"><span data-stu-id="b9370-110">Remove XML Data using XPathNavigator</span></span>](../../../../docs/standard/data/xml/remove-xml-data-using-xpathnavigator.md)  
 <span data-ttu-id="b9370-111"><xref:System.Xml.XmlDocument> 클래스를 사용하여 <xref:System.Xml.XPath.XPathNavigator> 개체에서 노드와 값을 제거하는 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b9370-111">Describes how to remove nodes and values from an <xref:System.Xml.XmlDocument> object using the <xref:System.Xml.XPath.XPathNavigator> class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b9370-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b9370-112">See also</span></span>

- <xref:System.Xml.XmlDocument>  
- <xref:System.Xml.XPath.XPathDocument>  
- <xref:System.Xml.XPath.XPathNavigator>  
- [<span data-ttu-id="b9370-113">XPath 데이터 모델을 사용하여 XML 데이터 처리</span><span class="sxs-lookup"><span data-stu-id="b9370-113">Process XML Data Using the XPath Data Model</span></span>](../../../../docs/standard/data/xml/process-xml-data-using-the-xpath-data-model.md)  
- [<span data-ttu-id="b9370-114">XPathDocument 및 XmlDocument를 사용하여 XML 데이터 읽기</span><span class="sxs-lookup"><span data-stu-id="b9370-114">Reading XML Data using XPathDocument and XmlDocument</span></span>](../../../../docs/standard/data/xml/reading-xml-data-using-xpathdocument-and-xmldocument.md)  
- [<span data-ttu-id="b9370-115">XPathNavigator를 사용하여 XML 데이터 선택, 평가 및 일치시키기</span><span class="sxs-lookup"><span data-stu-id="b9370-115">Selecting, Evaluating and Matching XML Data using XPathNavigator</span></span>](../../../../docs/standard/data/xml/selecting-evaluating-and-matching-xml-data-using-xpathnavigator.md)  
- [<span data-ttu-id="b9370-116">XPathNavigator를 사용하여 XML 데이터 액세스</span><span class="sxs-lookup"><span data-stu-id="b9370-116">Accessing XML Data using XPathNavigator</span></span>](../../../../docs/standard/data/xml/accessing-xml-data-using-xpathnavigator.md)  
- [<span data-ttu-id="b9370-117">XPathNavigator를 사용하여 스키마 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="b9370-117">Schema Validation using XPathNavigator</span></span>](../../../../docs/standard/data/xml/schema-validation-using-xpathnavigator.md)
