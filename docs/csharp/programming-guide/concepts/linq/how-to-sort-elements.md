---
title: '방법: 요소 정렬(C#)'
ms.date: 07/20/2015
ms.assetid: aee6fbbc-81fd-4b3e-b40f-6ed7b3bd3fee
ms.openlocfilehash: 66a41fc018b2df64aa95c24d1d698b6c38fd189a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54640786"
---
# <a name="how-to-sort-elements-c"></a>방법: 요소 정렬(C#)
이 예제에서는 결과를 정렬하는 쿼리를 작성하는 방법을 보여 줍니다.  
  
## <a name="example"></a>예제  
 이 예제에서는 XML 문서로을 사용합니다. [샘플 XML 파일: 숫자 데이터(LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-numerical-data-linq-to-xml.md).  
  
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
  
 이 코드의 결과는 다음과 같습니다.  
  
```  
0.99  
4.95  
6.99  
24.50  
29.00  
66.00  
89.99  
```  
  
## <a name="example"></a>예제  
 다음 예제에서는 네임스페이스에 있는 XML에 대한 동일한 쿼리를 보여 줍니다. 자세한 내용은 [XML 네임스페이스 작업(C#)](../../../../csharp/programming-guide/concepts/linq/working-with-xml-namespaces.md)을 참조하세요.  
  
 이 예제에서는 XML 문서로을 사용합니다. [샘플 XML 파일: 네임스페이스의 숫자 데이터](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-numerical-data-in-a-namespace.md).  
  
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
  
 이 코드의 결과는 다음과 같습니다.  
  
```  
0.99  
4.95  
6.99  
24.50  
29.00  
66.00  
89.99  
```  
  
## <a name="see-also"></a>참고 항목

- [데이터 정렬(C#)](../../../../csharp/programming-guide/concepts/linq/sorting-data.md)
- [기본 쿼리(LINQ to XML)(C#)](../../../../csharp/programming-guide/concepts/linq/basic-queries-linq-to-xml.md)
