---
title: '방법: 요소 컬렉션 검색(LINQ to XML)(C#)'
ms.date: 07/20/2015
ms.assetid: b849668c-7976-4974-b8e1-1cd587d34258
ms.openlocfilehash: 8d01c0499f031ae22fd6383dd77b36e444704c46
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54675004"
---
# <a name="how-to-retrieve-a-collection-of-elements-linq-to-xml-c"></a><span data-ttu-id="ee6ba-102">방법: 요소 컬렉션 검색(LINQ to XML)(C#)</span><span class="sxs-lookup"><span data-stu-id="ee6ba-102">How to: Retrieve a Collection of Elements (LINQ to XML) (C#)</span></span>
<span data-ttu-id="ee6ba-103">이 항목에서는 <xref:System.Xml.Linq.XContainer.Elements%2A> 메서드를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ee6ba-103">This topic demonstrates the <xref:System.Xml.Linq.XContainer.Elements%2A> method.</span></span> <span data-ttu-id="ee6ba-104">이 메서드는 요소의 자식 요소 컬렉션을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ee6ba-104">This method retrieves a collection of the child elements of an element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ee6ba-105">예제</span><span class="sxs-lookup"><span data-stu-id="ee6ba-105">Example</span></span>  
 <span data-ttu-id="ee6ba-106">이 예제에서는 `purchaseOrder` 요소의 자식 요소를 반복합니다.</span><span class="sxs-lookup"><span data-stu-id="ee6ba-106">This example iterates through the child elements of the `purchaseOrder` element.</span></span>  
  
 <span data-ttu-id="ee6ba-107">이 예제에서는 XML 문서로을 사용합니다. [샘플 XML 파일: 일반적인 구매 주문(LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-typical-purchase-order-linq-to-xml-1.md).</span><span class="sxs-lookup"><span data-stu-id="ee6ba-107">This example uses the following XML document: [Sample XML File: Typical Purchase Order (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-typical-purchase-order-linq-to-xml-1.md).</span></span>  
  
```csharp  
XElement po = XElement.Load("PurchaseOrder.xml");  
IEnumerable<XElement> childElements =  
    from el in po.Elements()  
    select el;  
foreach (XElement el in childElements)  
    Console.WriteLine("Name: " + el.Name);  
```  
  
 <span data-ttu-id="ee6ba-108">이 예제의 결과는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ee6ba-108">This example produces the following output.</span></span>  
  
```  
Name: Address  
Name: Address  
Name: DeliveryNotes  
Name: Items  
```  
  
## <a name="see-also"></a><span data-ttu-id="ee6ba-109">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ee6ba-109">See also</span></span>

- [<span data-ttu-id="ee6ba-110">LINQ to XML 축(C#)</span><span class="sxs-lookup"><span data-stu-id="ee6ba-110">LINQ to XML Axes (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-axes.md)
