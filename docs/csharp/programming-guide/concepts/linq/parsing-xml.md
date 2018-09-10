---
title: XML 구문 분석(C#)
ms.date: 07/20/2015
ms.assetid: 7ea83f83-a779-423a-9875-4ea4e51f97fc
ms.openlocfilehash: a2dc3043c8cbf8138a164ab06d8394e4c859fa50
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43523030"
---
# <a name="parsing-xml-c"></a><span data-ttu-id="289b0-102">XML 구문 분석(C#)</span><span class="sxs-lookup"><span data-stu-id="289b0-102">Parsing XML (C#)</span></span>
<span data-ttu-id="289b0-103">이 단원의 항목에서는 XML 문서의 구문을 분석하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="289b0-103">The topics in this section describe how to parse XML documents.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="289b0-104">섹션 내용</span><span class="sxs-lookup"><span data-stu-id="289b0-104">In This Section</span></span>  
  
|<span data-ttu-id="289b0-105">항목</span><span class="sxs-lookup"><span data-stu-id="289b0-105">Topic</span></span>|<span data-ttu-id="289b0-106">설명</span><span class="sxs-lookup"><span data-stu-id="289b0-106">Description</span></span>|  
|-----------|-----------------|  
|[<span data-ttu-id="289b0-107">방법: 문자열 구문 분석(C#)</span><span class="sxs-lookup"><span data-stu-id="289b0-107">How to: Parse a String (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-parse-a-string.md)|<span data-ttu-id="289b0-108">문자열의 구문을 분석하여 XML 트리를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="289b0-108">Shows how to parse a string to create an XML tree.</span></span>|  
|[<span data-ttu-id="289b0-109">방법: 파일에서 XML 로드(C#)</span><span class="sxs-lookup"><span data-stu-id="289b0-109">How to: Load XML from a File (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-load-xml-from-a-file.md)|<span data-ttu-id="289b0-110"><xref:System.Xml.Linq.XElement.Load%2A> 메서드를 사용하여 URI에서 XML을 로드하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="289b0-110">Shows how to load XML from a URI using the <xref:System.Xml.Linq.XElement.Load%2A> method.</span></span>|  
|[<span data-ttu-id="289b0-111">XML을 로드 또는 구문 분석할 때 공백 유지</span><span class="sxs-lookup"><span data-stu-id="289b0-111">Preserving White Space while Loading or Parsing XML</span></span>](../../../../csharp/programming-guide/concepts/linq/preserving-white-space-while-loading-or-parsing-xml1.md)|<span data-ttu-id="289b0-112">XML 트리를 로드하는 동안 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)]의 공백 동작을 제어하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="289b0-112">Describes how to control the white space behavior of [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] while loading XML trees.</span></span>|  
|[<span data-ttu-id="289b0-113">방법: 구문 분석 오류 Catch(C#)</span><span class="sxs-lookup"><span data-stu-id="289b0-113">How to: Catch Parsing Errors (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-catch-parsing-errors.md)|<span data-ttu-id="289b0-114">잘못 구성되었거나 유효하지 않은 XML을 검색하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="289b0-114">Shows how to detect badly formed or invalid XML.</span></span>|  
|[<span data-ttu-id="289b0-115">방법: XmlReader에서 트리 조각 만들기(C#)</span><span class="sxs-lookup"><span data-stu-id="289b0-115">How to: Create a Tree from an XmlReader (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-create-a-tree-from-an-xmlreader.md)|<span data-ttu-id="289b0-116"><xref:System.Xml.XmlReader>에서 XML 트리를 직접 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="289b0-116">Shows how to create an XML tree directly from an <xref:System.Xml.XmlReader>.</span></span>|  
|[<span data-ttu-id="289b0-117">방법: XmlReader에서 XML 조각 스트리밍(C#)</span><span class="sxs-lookup"><span data-stu-id="289b0-117">How to: Stream XML Fragments from an XmlReader (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-stream-xml-fragments-from-an-xmlreader.md)|<span data-ttu-id="289b0-118"><xref:System.Xml.XmlReader>를 사용하여 XML 조각을 스트림하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="289b0-118">Shows how to stream XML fragments by using an <xref:System.Xml.XmlReader>.</span></span><br /><br /> <span data-ttu-id="289b0-119">예상할 수 없는 큰 크기의 XML 파일을 처리해야 하는 경우 전체 XML 트리를 메모리에 로드하는 것이 가능하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="289b0-119">When you have to process arbitrarily large XML files, it might not be feasible to load the whole XML tree into memory.</span></span> <span data-ttu-id="289b0-120">이러한 경우 XML 조각을 스트림할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="289b0-120">Instead, you can stream XML fragments.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="289b0-121">참고 항목</span><span class="sxs-lookup"><span data-stu-id="289b0-121">See Also</span></span>

- [<span data-ttu-id="289b0-122">XML 트리 만들기(C#)</span><span class="sxs-lookup"><span data-stu-id="289b0-122">Creating XML Trees (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/creating-xml-trees.md)
