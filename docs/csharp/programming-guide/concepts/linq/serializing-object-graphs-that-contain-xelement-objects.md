---
title: XElement 개체를 포함하는 개체 그래프 serialize(C#)
ms.date: 07/20/2015
ms.assetid: fcbc3951-3cc4-4d0f-9259-e97549ed68f0
ms.openlocfilehash: 2e82165421d31ec234de4806b59565fa675217ef
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45698146"
---
# <a name="serializing-object-graphs-that-contain-xelement-objects-c"></a><span data-ttu-id="c71bf-102">XElement 개체를 포함하는 개체 그래프 serialize(C#)</span><span class="sxs-lookup"><span data-stu-id="c71bf-102">Serializing Object Graphs that Contain XElement Objects (C#)</span></span>
<span data-ttu-id="c71bf-103">이 항목에서는 <xref:System.Xml.Linq.XElement> 형식의 개체에 대한 참조가 포함된 개체 그래프를 serialize하는 기능에 대해 소개합니다.</span><span class="sxs-lookup"><span data-stu-id="c71bf-103">This topic introduces the capability of serializing object graphs that contain references to objects of type <xref:System.Xml.Linq.XElement>.</span></span> <span data-ttu-id="c71bf-104">이러한 유형의 serialize를 용이하게 수행하기 위해 <xref:System.Xml.Linq.XElement>는 <xref:System.Xml.Serialization.IXmlSerializable> 인터페이스를 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="c71bf-104">To facility this type of serializing, <xref:System.Xml.Linq.XElement> implements the <xref:System.Xml.Serialization.IXmlSerializable> interface.</span></span>  
  
 <span data-ttu-id="c71bf-105"><xref:System.Xml.Linq.XElement> 클래스만 serialization을 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="c71bf-105">Note that only the <xref:System.Xml.Linq.XElement> class implements serialization.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="c71bf-106">단원 내용</span><span class="sxs-lookup"><span data-stu-id="c71bf-106">In This Section</span></span>  
  
|<span data-ttu-id="c71bf-107">항목</span><span class="sxs-lookup"><span data-stu-id="c71bf-107">Topic</span></span>|<span data-ttu-id="c71bf-108">설명</span><span class="sxs-lookup"><span data-stu-id="c71bf-108">Description</span></span>|  
|-----------|-----------------|  
|[<span data-ttu-id="c71bf-109">방법: XmlSerializer를 사용하여 serialize(C#)</span><span class="sxs-lookup"><span data-stu-id="c71bf-109">How to: Serialize Using XmlSerializer (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-serialize-using-xmlserializer.md)|<span data-ttu-id="c71bf-110"><xref:System.Xml.Serialization.XmlSerializer>를 사용하여 serialize하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c71bf-110">Demonstrates how to serialize using <xref:System.Xml.Serialization.XmlSerializer>.</span></span>|  
|[<span data-ttu-id="c71bf-111">방법: DataContractSerializer를 사용하여 serialize(C#)</span><span class="sxs-lookup"><span data-stu-id="c71bf-111">How to: Serialize Using DataContractSerializer (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-serialize-using-datacontractserializer.md)|<span data-ttu-id="c71bf-112"><xref:System.Runtime.Serialization.DataContractSerializer>를 사용하여 serialize하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c71bf-112">Demonstrates how to serialize using <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c71bf-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c71bf-113">See Also</span></span>

- [<span data-ttu-id="c71bf-114">고급 LINQ to XML 프로그래밍(C#)</span><span class="sxs-lookup"><span data-stu-id="c71bf-114">Advanced LINQ to XML Programming (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/advanced-linq-to-xml-programming.md)
