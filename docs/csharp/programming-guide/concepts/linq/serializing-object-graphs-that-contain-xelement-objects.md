---
title: XElement 개체를 포함하는 개체 그래프 serialize(C#)
ms.date: 07/20/2015
ms.assetid: fcbc3951-3cc4-4d0f-9259-e97549ed68f0
ms.openlocfilehash: db7354598fc84c6fa3f8ec4e5b53799030459387
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54569143"
---
# <a name="serializing-object-graphs-that-contain-xelement-objects-c"></a><span data-ttu-id="c4853-102">XElement 개체를 포함하는 개체 그래프 serialize(C#)</span><span class="sxs-lookup"><span data-stu-id="c4853-102">Serializing Object Graphs that Contain XElement Objects (C#)</span></span>
<span data-ttu-id="c4853-103">이 항목에서는 <xref:System.Xml.Linq.XElement> 형식의 개체에 대한 참조가 포함된 개체 그래프를 serialize하는 기능에 대해 소개합니다.</span><span class="sxs-lookup"><span data-stu-id="c4853-103">This topic introduces the capability of serializing object graphs that contain references to objects of type <xref:System.Xml.Linq.XElement>.</span></span> <span data-ttu-id="c4853-104">이러한 유형의 serialize를 용이하게 수행하기 위해 <xref:System.Xml.Linq.XElement>는 <xref:System.Xml.Serialization.IXmlSerializable> 인터페이스를 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="c4853-104">To facility this type of serializing, <xref:System.Xml.Linq.XElement> implements the <xref:System.Xml.Serialization.IXmlSerializable> interface.</span></span>  
  
 <span data-ttu-id="c4853-105"><xref:System.Xml.Linq.XElement> 클래스만 serialization을 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="c4853-105">Note that only the <xref:System.Xml.Linq.XElement> class implements serialization.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="c4853-106">섹션 내용</span><span class="sxs-lookup"><span data-stu-id="c4853-106">In This Section</span></span>  
  
|<span data-ttu-id="c4853-107">항목</span><span class="sxs-lookup"><span data-stu-id="c4853-107">Topic</span></span>|<span data-ttu-id="c4853-108">설명</span><span class="sxs-lookup"><span data-stu-id="c4853-108">Description</span></span>|  
|-----------|-----------------|  
|[<span data-ttu-id="c4853-109">방법: XmlSerializer를 사용하여 serialize(C#)</span><span class="sxs-lookup"><span data-stu-id="c4853-109">How to: Serialize Using XmlSerializer (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-serialize-using-xmlserializer.md)|<span data-ttu-id="c4853-110"><xref:System.Xml.Serialization.XmlSerializer>를 사용하여 serialize하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c4853-110">Demonstrates how to serialize using <xref:System.Xml.Serialization.XmlSerializer>.</span></span>|  
|[<span data-ttu-id="c4853-111">방법: DataContractSerializer를 사용하여 serialize(C#)</span><span class="sxs-lookup"><span data-stu-id="c4853-111">How to: Serialize Using DataContractSerializer (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-serialize-using-datacontractserializer.md)|<span data-ttu-id="c4853-112"><xref:System.Runtime.Serialization.DataContractSerializer>를 사용하여 serialize하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c4853-112">Demonstrates how to serialize using <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c4853-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c4853-113">See also</span></span>

- [<span data-ttu-id="c4853-114">고급 LINQ to XML 프로그래밍(C#)</span><span class="sxs-lookup"><span data-stu-id="c4853-114">Advanced LINQ to XML Programming (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/advanced-linq-to-xml-programming.md)
