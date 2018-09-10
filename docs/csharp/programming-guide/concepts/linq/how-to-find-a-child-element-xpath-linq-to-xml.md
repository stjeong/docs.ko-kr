---
title: '방법: 자식 요소 찾기(XPath 및 LINQ to XML)(C#)'
ms.date: 07/20/2015
ms.assetid: 4fa6182d-6196-4ed1-9c9e-82949ff89c71
ms.openlocfilehash: 3027914d87b8245af16b4864c0f558158ab253a1
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43503769"
---
# <a name="how-to-find-a-child-element-xpath-linq-to-xml-c"></a><span data-ttu-id="d397d-102">방법: 자식 요소 찾기(XPath 및 LINQ to XML)(C#)</span><span class="sxs-lookup"><span data-stu-id="d397d-102">How to: Find a Child Element (XPath-LINQ to XML) (C#)</span></span>
<span data-ttu-id="d397d-103">이 항목에서는 XPath 자식 요소 축과 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] <xref:System.Xml.Linq.XContainer.Element%2A> 메서드를 비교합니다.</span><span class="sxs-lookup"><span data-stu-id="d397d-103">This topic compares the XPath child element axis to the [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] <xref:System.Xml.Linq.XContainer.Element%2A> method.</span></span>  
  
 <span data-ttu-id="d397d-104">XPath 식은 `DeliveryNotes`입니다.</span><span class="sxs-lookup"><span data-stu-id="d397d-104">The XPath expression is `DeliveryNotes`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d397d-105">예</span><span class="sxs-lookup"><span data-stu-id="d397d-105">Example</span></span>  
 <span data-ttu-id="d397d-106">이 예제에서는 자식 요소 `DeliveryNotes`를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d397d-106">This example finds the child element `DeliveryNotes`.</span></span>  
  
 <span data-ttu-id="d397d-107">이 예제에서는 XML 문서 [샘플 XML 파일: 여러 구매 주문(LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-multiple-purchase-orders-linq-to-xml.md)을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d397d-107">This example uses the following XML document: [Sample XML File: Multiple Purchase Orders (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-multiple-purchase-orders-linq-to-xml.md).</span></span>  
  
```csharp  
XDocument cpo = XDocument.Load("PurchaseOrders.xml");  
XElement po = cpo.Root.Element("PurchaseOrder");  
  
// LINQ to XML query  
XElement el1 = po.Element("DeliveryNotes");  
  
// XPath expression  
XElement el2 = po.XPathSelectElement("DeliveryNotes");  
// same as "child::DeliveryNotes"  
// same as "./DeliveryNotes"  
  
if (el1 == el2)  
    Console.WriteLine("Results are identical");  
else  
    Console.WriteLine("Results differ");  
Console.WriteLine(el1);  
```  
  
 <span data-ttu-id="d397d-108">이 예제는 다음과 같은 출력을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d397d-108">This example produces the following output:</span></span>  
  
```  
Results are identical  
<DeliveryNotes>Please leave packages in shed by driveway.</DeliveryNotes>  
```  
  
## <a name="see-also"></a><span data-ttu-id="d397d-109">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d397d-109">See Also</span></span>

- [<span data-ttu-id="d397d-110">XPath 사용자를 위한 LINQ to XML(C#)</span><span class="sxs-lookup"><span data-stu-id="d397d-110">LINQ to XML for XPath Users (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
