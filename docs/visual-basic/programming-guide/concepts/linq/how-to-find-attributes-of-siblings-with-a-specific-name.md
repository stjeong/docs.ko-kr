---
title: '방법: (XPath 및 LINQ to XML) 특정 이름으로 형제의 특성 찾기 (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: 83b3ddca-830a-4b71-9756-9e4bdf907302
ms.openlocfilehash: ce97cbc4b8b1105e8431016a9c296c158cf0091c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54596191"
---
# <a name="how-to-find-attributes-of-siblings-with-a-specific-name-xpath-linq-to-xml-visual-basic"></a>방법: (XPath 및 LINQ to XML) 특정 이름으로 형제의 특성 찾기 (Visual Basic)
이 항목에서는 컨텍스트 노드에 대한 형제의 특성을 모두 찾는 방법을 보여 줍니다. 특정 이름을 가진 특성만 컬렉션에 반환됩니다.  
  
 XPath 식은 다음과 같습니다.  
  
 `../Book/@id`  
  
## <a name="example"></a>예제  
 이 예제에서는 먼저 `Book` 요소를 찾은 다음 `Book`이라는 모든 형제 요소를 찾고 `id`라는 모든 특성을 찾습니다. 결과는 특성의 컬렉션입니다.  
  
 이 예제에서는 XML 문서로 을 사용합니다. [샘플 XML 파일: Books (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-books-linq-to-xml.md)합니다.  
  
```vb  
Dim books as XDocument = XDocument.Load("Books.xml")  
Dim book As XElement = books.Root.<Book>(0)  
  
' LINQ to XML query  
Dim list1 As IEnumerable(Of XAttribute) = _  
    From el In book.Parent.<Book> _  
    Select el.Attribute("id")  
  
' XPath expression  
Dim list2 As IEnumerable(Of XAttribute) = DirectCast(book. _  
    XPathEvaluate("../Book/@id"), IEnumerable).Cast(Of XAttribute)()  
  
If list1.Count() = list2.Count() And _  
        (list1.Intersect(list2)).Count() = list1.Count() Then  
    Console.WriteLine("Results are identical")  
Else  
    Console.WriteLine("Results differ")  
End If  
  
For Each el As XAttribute In list1  
    Console.WriteLine(el)  
Next  
```  
  
 이 예제는 다음과 같은 출력을 생성합니다.  
  
```  
Results are identical  
id="bk101"  
id="bk102"  
```  
  
## <a name="see-also"></a>참고자료
- [XPath 사용자 (Visual Basic)를 위한 LINQ to XML](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
