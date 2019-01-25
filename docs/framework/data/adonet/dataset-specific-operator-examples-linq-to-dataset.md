---
title: DataSet별 연산자 예제(LINQ to DataSet)
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 8fdd64af-6ad0-46cd-91c8-dbe26620eeb1
ms.openlocfilehash: 92daf1dff3d473016d92b359ea6f75295a9dbd37
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54739034"
---
# <a name="dataset-specific-operator-examples-linq-to-dataset"></a><span data-ttu-id="0e60a-102">DataSet별 연산자 예제(LINQ to DataSet)</span><span class="sxs-lookup"><span data-stu-id="0e60a-102">DataSet-Specific Operator Examples (LINQ to DataSet)</span></span>
<span data-ttu-id="0e60a-103">이 항목의 예제에서는 <xref:System.Data.DataTableExtensions.CopyToDataTable%2A> 메서드와 <xref:System.Data.DataRowComparer> 클래스를 사용하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0e60a-103">The examples in this topic demonstrate how to use the <xref:System.Data.DataTableExtensions.CopyToDataTable%2A> method and the <xref:System.Data.DataRowComparer> class.</span></span>  
  
 <span data-ttu-id="0e60a-104">합니다 `FillDataSet` 에이 예제에서 사용 하는 방법이 지정 되어 [는 DataSet에 데이터 로드](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="0e60a-104">The `FillDataSet` method used in these examples is specified in [Loading Data Into a DataSet](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md).</span></span>  
  
 <span data-ttu-id="0e60a-105">이 항목의 예제에서는 AdventureWorks 샘플 데이터베이스의 Contact, Address, Product, SalesOrderHeader 및 SalesOrderDetail 테이블을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0e60a-105">The examples in this topic use the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="0e60a-106">이 항목의 예제에서는 다음을 사용 `using` / `Imports` 문:</span><span class="sxs-lookup"><span data-stu-id="0e60a-106">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#importsusing)]  
  
 <span data-ttu-id="0e60a-107">자세한 내용은 [방법: Visual Studio에서 LINQ to DataSet 프로젝트 만들기](../../../../docs/framework/data/adonet/how-to-create-a-linq-to-dataset-project-in-vs.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="0e60a-107">For more information, see [How to: Create a LINQ to DataSet Project In Visual Studio](../../../../docs/framework/data/adonet/how-to-create-a-linq-to-dataset-project-in-vs.md).</span></span>  
  
## <a name="copytodatatable"></a><span data-ttu-id="0e60a-108">CopyToDataTable</span><span class="sxs-lookup"><span data-stu-id="0e60a-108">CopyToDataTable</span></span>  
  
### <a name="example"></a><span data-ttu-id="0e60a-109">예제</span><span class="sxs-lookup"><span data-stu-id="0e60a-109">Example</span></span>  
 <span data-ttu-id="0e60a-110">이 예제에서는 <xref:System.Data.DataTable> 메서드를 사용하여 쿼리 결과가 있는 <xref:System.Data.DataTableExtensions.CopyToDataTable%2A>을 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="0e60a-110">This example loads a <xref:System.Data.DataTable> with query results by using the <xref:System.Data.DataTableExtensions.CopyToDataTable%2A> method.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#LoadDataTableWithQueryResults](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#loaddatatablewithqueryresults)]
 [!code-vb[DP LINQ to DataSet Examples#LoadDataTableWithQueryResults](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#loaddatatablewithqueryresults)]  
  
## <a name="datarowcomparer"></a><span data-ttu-id="0e60a-111">DataRowComparer</span><span class="sxs-lookup"><span data-stu-id="0e60a-111">DataRowComparer</span></span>  
  
### <a name="example"></a><span data-ttu-id="0e60a-112">예제</span><span class="sxs-lookup"><span data-stu-id="0e60a-112">Example</span></span>  
 <span data-ttu-id="0e60a-113">이 예제에서는 <xref:System.Data.DataRowComparer>를 사용하여 서로 다른 두 데이터 행을 비교합니다.</span><span class="sxs-lookup"><span data-stu-id="0e60a-113">This example compares two different data rows by using <xref:System.Data.DataRowComparer>.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#CompareDifferentDataRows](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#comparedifferentdatarows)]  
  
## <a name="see-also"></a><span data-ttu-id="0e60a-114">참고자료</span><span class="sxs-lookup"><span data-stu-id="0e60a-114">See also</span></span>
- [<span data-ttu-id="0e60a-115">데이터를 데이터 세트에 로드</span><span class="sxs-lookup"><span data-stu-id="0e60a-115">Loading Data Into a DataSet</span></span>](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md)
- [<span data-ttu-id="0e60a-116">LINQ to DataSet 예제</span><span class="sxs-lookup"><span data-stu-id="0e60a-116">LINQ to DataSet Examples</span></span>](../../../../docs/framework/data/adonet/linq-to-dataset-examples.md)
