---
title: System.Xml 사용법
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: 82302f0d-a621-4c6f-b57d-999bd61f21a6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5c3eb01e1050bc78d2b31de19a8a728af92777e8
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43863389"
---
# <a name="systemxml-usage"></a><span data-ttu-id="e7378-102">System.Xml 사용법</span><span class="sxs-lookup"><span data-stu-id="e7378-102">System.Xml Usage</span></span>
<span data-ttu-id="e7378-103">이 섹션에 있는 여러 유형의 사용 방법과 <xref:System.Xml?displayProperty=nameWithType> 네임 스페이스는 XML 데이터를 나타내는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7378-103">This section talks about usage of several types residing in <xref:System.Xml?displayProperty=nameWithType> namespaces that can be used to represent XML data.</span></span>  
  
 <span data-ttu-id="e7378-104">**X DO NOT** 사용 <xref:System.Xml.XmlNode> 또는 <xref:System.Xml.XmlDocument> XML 데이터를 표시 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7378-104">**X DO NOT** use <xref:System.Xml.XmlNode> or <xref:System.Xml.XmlDocument> to represent XML data.</span></span> <span data-ttu-id="e7378-105">인스턴스를 사용 하는 중 무엇을 선호할 <xref:System.Xml.XPath.IXPathNavigable>, <xref:System.Xml.XmlReader>를 <xref:System.Xml.XmlWriter>, 또는 하위 <xref:System.Xml.Linq.XNode> 대신 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7378-105">Favor using instances of <xref:System.Xml.XPath.IXPathNavigable>, <xref:System.Xml.XmlReader>, <xref:System.Xml.XmlWriter>, or subtypes of <xref:System.Xml.Linq.XNode> instead.</span></span> <span data-ttu-id="e7378-106">`XmlNode` 및 `XmlDocument` 공용 Api에서 공개 설계 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e7378-106">`XmlNode` and `XmlDocument` are not designed for exposing in public APIs.</span></span>  
  
 <span data-ttu-id="e7378-107">**✓ DO** 사용 `XmlReader`, `IXPathNavigable`, 또는 유형의 하위 `XNode` 입력 또는 출력을 사용 하거나 XML을 반환 하는 멤버의으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7378-107">**✓ DO** use `XmlReader`, `IXPathNavigable`, or subtypes of `XNode` as input or output of members that accept or return XML.</span></span>  
  
 <span data-ttu-id="e7378-108">대신 이러한 추상화를 사용 하 여 `XmlDocument`하십시오 `XmlNode`, 또는 <xref:System.Xml.XPath.XPathDocument>이므로 메모리 내 XML 문서의 특정 구현에서 메서드를 분리 하 고 노출 하는 가상 XML 데이터 원본과 작업할 수 있도록이 `XNode` 하십시오 `XmlReader`, 또는 <xref:System.Xml.XPath.XPathNavigator>합니다.</span><span class="sxs-lookup"><span data-stu-id="e7378-108">Use these abstractions instead of `XmlDocument`, `XmlNode`, or <xref:System.Xml.XPath.XPathDocument>, because this decouples the methods from specific implementations of an in-memory XML document and allows them to work with virtual XML data sources that expose `XNode`, `XmlReader`, or <xref:System.Xml.XPath.XPathNavigator>.</span></span>  
  
 <span data-ttu-id="e7378-109">**X DO NOT** 하위 클래스 `XmlDocument` 경우 만들려면 기본 개체 모델 또는 데이터 원본에 대 한 XML 뷰를 나타내는 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e7378-109">**X DO NOT** subclass `XmlDocument` if you want to create a type representing an XML view of an underlying object model or data source.</span></span>  
  
 <span data-ttu-id="e7378-110">*Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*</span><span class="sxs-lookup"><span data-stu-id="e7378-110">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="e7378-111">*Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span><span class="sxs-lookup"><span data-stu-id="e7378-111">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7378-112">참고자료</span><span class="sxs-lookup"><span data-stu-id="e7378-112">See also</span></span>

- [<span data-ttu-id="e7378-113">프레임워크 디자인 지침</span><span class="sxs-lookup"><span data-stu-id="e7378-113">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="e7378-114">사용 지침</span><span class="sxs-lookup"><span data-stu-id="e7378-114">Usage Guidelines</span></span>](../../../docs/standard/design-guidelines/usage-guidelines.md)
