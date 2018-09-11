---
title: LINQ to DataSet
ms.date: 03/30/2017
ms.assetid: 743e3755-3ecb-45a2-8d9b-9ed41f0dcf17
ms.openlocfilehash: 5e1644af7e07ad3395a30e56df52b7f85cefa77c
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/11/2018
ms.locfileid: "44368192"
---
# <a name="linq-to-dataset"></a><span data-ttu-id="bd630-102">LINQ to DataSet</span><span class="sxs-lookup"><span data-stu-id="bd630-102">LINQ to DataSet</span></span>
[!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)]<span data-ttu-id="bd630-103">을 사용하면 <xref:System.Data.DataSet> 개체에 캐시된 데이터를 쉽고 빠르게 쿼리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd630-103"> makes it easier and faster to query over data cached in a <xref:System.Data.DataSet> object.</span></span> <span data-ttu-id="bd630-104">특히, [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)]을 사용하면 별도의 쿼리 언어를 사용하는 대신 프로그래밍 언어 자체에서 쿼리를 작성할 수 있으므로 간편하게 쿼리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd630-104">Specifically, [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] simplifies querying by enabling developers to write queries from the programming language itself, instead of by using a separate query language.</span></span> <span data-ttu-id="bd630-105">지금 활용할 수 컴파일 타임 구문 검사, 정적 입력 및 IntelliSense 지원을 해당 쿼리에 Visual Studio에서 제공 하는 Visual Studio 개발자에 게 특히 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd630-105">This is especially useful for Visual Studio developers, who can now take advantage of the compile-time syntax checking, static typing, and IntelliSense support provided by the Visual Studio in their queries.</span></span>  
  
 [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)]<span data-ttu-id="bd630-106">은 하나 이상의 데이터 소스에서 통합된 데이터를 쿼리하는 데도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd630-106"> can also be used to query over data that has been consolidated from one or more data sources.</span></span> <span data-ttu-id="bd630-107">이 기능은 논리적으로 집계된 데이터 쿼리, 웹 응용 프로그램의 중간 계층 캐시 등과 같이 유연하게 데이터를 표현하고 처리해야 하는 여러 시나리오에 사용될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd630-107">This enables many scenarios that require flexibility in how data is represented and handled, such as querying locally aggregated data and middle-tier caching in Web applications.</span></span> <span data-ttu-id="bd630-108">이러한 조작 방법은 일반적인 보고, 분석 및 비즈니스 인텔리전스 응용 프로그램에 특히 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="bd630-108">In particular, generic reporting, analysis, and business intelligence applications require this method of manipulation.</span></span>  
  
 <span data-ttu-id="bd630-109">[!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] 기능은 주로의 확장 메서드를 통해 노출 되는 <xref:System.Data.DataRowExtensions> 및 <xref:System.Data.DataTableExtensions> 클래스.</span><span class="sxs-lookup"><span data-stu-id="bd630-109">The [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] functionality is exposed primarily through the extension methods in the <xref:System.Data.DataRowExtensions> and <xref:System.Data.DataTableExtensions> classes.</span></span> [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)]<span data-ttu-id="bd630-110"> 기반으로 하며, 기존 사용 [!INCLUDE[ado_whidbey_long](../../../../includes/ado-whidbey-long-md.md)] 아키텍처를 대체 하기 위한 것 및 [!INCLUDE[ado_whidbey_long](../../../../includes/ado-whidbey-long-md.md)] 응용 프로그램 코드에서.</span><span class="sxs-lookup"><span data-stu-id="bd630-110"> builds on and uses the existing [!INCLUDE[ado_whidbey_long](../../../../includes/ado-whidbey-long-md.md)] architecture, and is not meant to replace [!INCLUDE[ado_whidbey_long](../../../../includes/ado-whidbey-long-md.md)] in application code.</span></span> <span data-ttu-id="bd630-111">기존 ADO.NET 2.0 코드는 [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] 응용 프로그램에서 계속 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd630-111">Existing ADO.NET 2.0 code will continue to function in a [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] application.</span></span> <span data-ttu-id="bd630-112">다음 다이어그램에서는 [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)]에 대한 [!INCLUDE[ado_whidbey_long](../../../../includes/ado-whidbey-long-md.md)]과 데이터 저장소의 관계를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bd630-112">The relationship of [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] to [!INCLUDE[ado_whidbey_long](../../../../includes/ado-whidbey-long-md.md)] and the data store is illustrated in the following diagram.</span></span>  
  
 <span data-ttu-id="bd630-113">![ADO.NET 공급자를 기반으로 하는 LINQ to DataSet](../../../../docs/framework/data/adonet/media/linqtodataset.gif "LINQtoDataSet")</span><span class="sxs-lookup"><span data-stu-id="bd630-113">![LINQ to DataSet is based on the ADO.NET Provider](../../../../docs/framework/data/adonet/media/linqtodataset.gif "LINQtoDataSet")</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="bd630-114">섹션 내용</span><span class="sxs-lookup"><span data-stu-id="bd630-114">In This Section</span></span>  
 [<span data-ttu-id="bd630-115">시작</span><span class="sxs-lookup"><span data-stu-id="bd630-115">Getting Started</span></span>](../../../../docs/framework/data/adonet/getting-started-linq-to-dataset.md)  
  
 [<span data-ttu-id="bd630-116">프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="bd630-116">Programming Guide</span></span>](../../../../docs/framework/data/adonet/programming-guide-linq-to-dataset.md)  
  
## <a name="reference"></a><span data-ttu-id="bd630-117">참조</span><span class="sxs-lookup"><span data-stu-id="bd630-117">Reference</span></span>  
 <xref:System.Data.DataTableExtensions>  
  
 <xref:System.Data.DataRowExtensions>  
  
 <xref:System.Data.DataRowComparer>  
  
## <a name="see-also"></a><span data-ttu-id="bd630-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="bd630-118">See Also</span></span>  
 [<span data-ttu-id="bd630-119">LINQ(Language-Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="bd630-119">LINQ (Language-Integrated Query)</span></span>](https://msdn.microsoft.com/library/a73c4aec-5d15-4e98-b962-1274021ea93d)  
 [<span data-ttu-id="bd630-120">LINQ 및 ADO.NET</span><span class="sxs-lookup"><span data-stu-id="bd630-120">LINQ and ADO.NET</span></span>](../../../../docs/framework/data/adonet/linq-and-ado-net.md)  
 [<span data-ttu-id="bd630-121">ADO.NET</span><span class="sxs-lookup"><span data-stu-id="bd630-121">ADO.NET</span></span>](../../../../docs/framework/data/adonet/index.md)
