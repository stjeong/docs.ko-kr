---
title: '방법: 문자열 구문 분석(C#)'
ms.date: 07/20/2015
ms.assetid: 81e5686c-9658-42d8-a7e3-b11be0a2c98b
ms.openlocfilehash: b6b955d2cc9a3ea0c6e17e68639ad7fc677c3fc7
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43744802"
---
# <a name="how-to-parse-a-string-c"></a><span data-ttu-id="a3f1a-102">방법: 문자열 구문 분석(C#)</span><span class="sxs-lookup"><span data-stu-id="a3f1a-102">How to: Parse a String (C#)</span></span>
<span data-ttu-id="a3f1a-103">이 항목에서는 C#에서 문자열의 구문을 분석하여 XML 트리를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a3f1a-103">This topic shows how to parse a string to create an XML tree in C#.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a3f1a-104">예</span><span class="sxs-lookup"><span data-stu-id="a3f1a-104">Example</span></span>  
 <span data-ttu-id="a3f1a-105">다음 C# 코드에서는 문자열의 구문을 분석하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a3f1a-105">The following C# code shows how to parse a string.</span></span>  
  
```csharp  
XElement contacts = XElement.Parse(  
    @"<Contacts>  
        <Contact>  
            <Name>Patrick Hines</Name>  
            <Phone Type=""home"">206-555-0144</Phone>  
            <Phone type=""work"">425-555-0145</Phone>  
            <Address>  
            <Street1>123 Main St</Street1>  
            <City>Mercer Island</City>  
            <State>WA</State>  
            <Postal>68042</Postal>  
            </Address>  
            <NetWorth>10</NetWorth>  
        </Contact>  
        <Contact>  
            <Name>Gretchen Rivas</Name>  
            <Phone Type=""mobile"">206-555-0163</Phone>  
            <Address>  
            <Street1>123 Main St</Street1>  
            <City>Mercer Island</City>  
            <State>WA</State>  
            <Postal>68042</Postal>  
            </Address>  
            <NetWorth>11</NetWorth>  
        </Contact>  
    </Contacts>");  
Console.WriteLine(contacts);  
```  
  
## <a name="see-also"></a><span data-ttu-id="a3f1a-106">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a3f1a-106">See Also</span></span>

- [<span data-ttu-id="a3f1a-107">XML 구문 분석(C#)</span><span class="sxs-lookup"><span data-stu-id="a3f1a-107">Parsing XML (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/parsing-xml.md)
