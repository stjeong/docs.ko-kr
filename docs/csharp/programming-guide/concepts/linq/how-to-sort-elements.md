---
title: '방법: 요소 정렬(C#)'
ms.date: 07/20/2015
ms.assetid: aee6fbbc-81fd-4b3e-b40f-6ed7b3bd3fee
ms.openlocfilehash: 7548f183736ac9ed0ed09d3be775b3ffde6cb255
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "44042610"
---
# <a name="how-to-sort-elements-c"></a><span data-ttu-id="f7272-102">방법: 요소 정렬(C#)</span><span class="sxs-lookup"><span data-stu-id="f7272-102">How to: Sort Elements (C#)</span></span>
<span data-ttu-id="f7272-103">이 예제에서는 결과를 정렬하는 쿼리를 작성하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f7272-103">This example shows how to write a query that sorts its results.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f7272-104">예</span><span class="sxs-lookup"><span data-stu-id="f7272-104">Example</span></span>  
 <span data-ttu-id="f7272-105">이 예제에서는 XML 문서 [샘플 XML 파일: 숫자 데이터(LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-numerical-data-linq-to-xml.md)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f7272-105">This example uses the following XML document: [Sample XML File: Numerical Data (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-numerical-data-linq-to-xml.md).</span></span>  
  
```csharp  
XElement root = XElement.Load("Data.xml");  
IEnumerable<decimal> prices =  
    from el in root.Elements("Data")  
    let price = (decimal)el.Element("Price")  
    orderby price  
    select price;  
foreach (decimal el in prices)  
    Console.WriteLine(el);  
```  
  
 <span data-ttu-id="f7272-106">이 코드의 결과는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f7272-106">This code produces the following output:</span></span>  
  
```  
0.99  
4.95  
6.99  
24.50  
29.00  
66.00  
89.99  
```  
  
## <a name="example"></a><span data-ttu-id="f7272-107">예</span><span class="sxs-lookup"><span data-stu-id="f7272-107">Example</span></span>  
 <span data-ttu-id="f7272-108">다음 예제에서는 네임스페이스에 있는 XML에 대한 동일한 쿼리를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f7272-108">The following example shows the same query for XML that is in a namespace.</span></span> <span data-ttu-id="f7272-109">자세한 내용은 [XML 네임스페이스 작업(C#)](../../../../csharp/programming-guide/concepts/linq/working-with-xml-namespaces.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f7272-109">For more information, see [Working with XML Namespaces (C#)](../../../../csharp/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span></span>  
  
 <span data-ttu-id="f7272-110">이 예제에서는 XML 문서 [샘플 XML 파일: 네임스페이스의 숫자 데이터](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-numerical-data-in-a-namespace.md)를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f7272-110">This example uses the following XML document: [Sample XML File: Numerical Data in a Namespace](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-numerical-data-in-a-namespace.md).</span></span>  
  
```csharp  
XElement root = XElement.Load("DataInNamespace.xml");  
XNamespace aw = "http://www.adatum.com";  
IEnumerable<decimal> prices =  
    from el in root.Elements(aw + "Data")  
    let price = (decimal)el.Element(aw + "Price")  
    orderby price  
    select price;  
foreach (decimal el in prices)  
    Console.WriteLine(el);  
```  
  
 <span data-ttu-id="f7272-111">이 코드의 결과는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f7272-111">This code produces the following output:</span></span>  
  
```  
0.99  
4.95  
6.99  
24.50  
29.00  
66.00  
89.99  
```  
  
## <a name="see-also"></a><span data-ttu-id="f7272-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f7272-112">See Also</span></span>

- [<span data-ttu-id="f7272-113">데이터 정렬(C#)</span><span class="sxs-lookup"><span data-stu-id="f7272-113">Sorting Data (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/sorting-data.md)  
- [<span data-ttu-id="f7272-114">기본 쿼리(LINQ to XML)(C#)</span><span class="sxs-lookup"><span data-stu-id="f7272-114">Basic Queries (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/basic-queries-linq-to-xml.md)
