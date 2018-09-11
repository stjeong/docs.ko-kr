---
title: XML 선언으로 serialize(C#)
ms.date: 07/20/2015
ms.assetid: c237fa4a-a042-40fd-886f-17b54c66bb75
ms.openlocfilehash: 613280efc8c734c53c4af9252b4b83e2dd942f36
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/09/2018
ms.locfileid: "44222359"
---
# <a name="serializing-with-an-xml-declaration-c"></a><span data-ttu-id="1048e-102">XML 선언으로 serialize(C#)</span><span class="sxs-lookup"><span data-stu-id="1048e-102">Serializing with an XML Declaration (C#)</span></span>
<span data-ttu-id="1048e-103">이 항목에서는 serialization을 통해 XML 선언이 생성되는지 여부를 제어하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="1048e-103">This topic describes how to control whether serialization generates an XML declaration.</span></span>  
  
## <a name="xml-declaration-generation"></a><span data-ttu-id="1048e-104">XML 선언 생성</span><span class="sxs-lookup"><span data-stu-id="1048e-104">XML Declaration Generation</span></span>  
 <span data-ttu-id="1048e-105"><xref:System.IO.File> 메서드 또는 <xref:System.IO.TextWriter> 메서드를 사용하여 <xref:System.Xml.Linq.XElement.Save%2A?displayProperty=nameWithType> 또는 <xref:System.Xml.Linq.XDocument.Save%2A?displayProperty=nameWithType>로 serialize하면 XML 선언이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="1048e-105">Serializing to a <xref:System.IO.File> or a <xref:System.IO.TextWriter> using the <xref:System.Xml.Linq.XElement.Save%2A?displayProperty=nameWithType> method or the <xref:System.Xml.Linq.XDocument.Save%2A?displayProperty=nameWithType> method generates an XML declaration.</span></span> <span data-ttu-id="1048e-106"><xref:System.Xml.XmlWriter>로 serialize하면 <xref:System.Xml.XmlWriterSettings> 개체에 지정된 작성기 설정에 따라 XML 선언이 생성되는지 여부가 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="1048e-106">When you serialize to an <xref:System.Xml.XmlWriter>, the writer settings (specified in an <xref:System.Xml.XmlWriterSettings> object) determine whether an XML declaration is generated or not.</span></span>  
  
 <span data-ttu-id="1048e-107">`ToString` 메서드를 사용하여 문자열로 serialize하는 경우 생성되는 XML에는 XML 선언이 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1048e-107">If you are serializing to a string using the `ToString` method, the resulting XML will not include an XML declaration.</span></span>  
  
### <a name="serializing-with-an-xml-declaration"></a><span data-ttu-id="1048e-108">XML 선언으로 serialization</span><span class="sxs-lookup"><span data-stu-id="1048e-108">Serializing with an XML Declaration</span></span>  
 <span data-ttu-id="1048e-109">다음 예제에서는 <xref:System.Xml.Linq.XElement>를 만들고 문서를 파일에 저장한 다음 파일을 콘솔에 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="1048e-109">The following example creates an <xref:System.Xml.Linq.XElement>, saves the document to a file, and then prints the file to the console:</span></span>  
  
```csharp  
XElement root = new XElement("Root",  
    new XElement("Child", "child content")  
);  
root.Save("Root.xml");  
string str = File.ReadAllText("Root.xml");  
Console.WriteLine(str);  
```  
  
 <span data-ttu-id="1048e-110">이 예제는 다음과 같은 출력을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1048e-110">This example produces the following output:</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<Root>  
  <Child>child content</Child>  
</Root>  
```  
  
### <a name="serializing-without-an-xml-declaration"></a><span data-ttu-id="1048e-111">XML 선언을 사용하지 않고 serialize</span><span class="sxs-lookup"><span data-stu-id="1048e-111">Serializing without an XML Declaration</span></span>  
 <span data-ttu-id="1048e-112">다음 예제에서는 <xref:System.Xml.Linq.XElement>를 <xref:System.Xml.XmlWriter>에 저장하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1048e-112">The following example shows how to save an <xref:System.Xml.Linq.XElement> to an <xref:System.Xml.XmlWriter>.</span></span>  
  
```csharp  
StringBuilder sb = new StringBuilder();  
XmlWriterSettings xws = new XmlWriterSettings();  
xws.OmitXmlDeclaration = true;  
  
using (XmlWriter xw = XmlWriter.Create(sb, xws)) {  
    XElement root = new XElement("Root",  
        new XElement("Child", "child content")  
    );  
    root.Save(xw);  
}  
Console.WriteLine(sb.ToString());  
```  
  
 <span data-ttu-id="1048e-113">이 예제는 다음과 같은 출력을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1048e-113">This example produces the following output:</span></span>  
  
```xml  
<Root><Child>child content</Child></Root>  
```  
  
## <a name="see-also"></a><span data-ttu-id="1048e-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1048e-114">See Also</span></span>

- [<span data-ttu-id="1048e-115">XML 트리 serialize(C#)</span><span class="sxs-lookup"><span data-stu-id="1048e-115">Serializing XML Trees (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/serializing-xml-trees.md)
