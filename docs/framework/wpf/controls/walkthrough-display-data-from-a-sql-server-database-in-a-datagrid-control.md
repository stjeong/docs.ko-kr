---
title: '연습: DataGrid 컨트롤에서 SQL Server 데이터베이스의 데이터 표시'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGrid [WPF], displaying data from SQL Server
- controls [WPF], DataGrid
ms.assetid: 6810b048-0a23-4f86-bfa5-97f92b3cfab4
ms.openlocfilehash: 1421d076ff202ec87a9d861ab2c7d1c1cdcdc1b7
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43408192"
---
# <a name="walkthrough-display-data-from-a-sql-server-database-in-a-datagrid-control"></a><span data-ttu-id="cb21f-102">연습: DataGrid 컨트롤에서 SQL Server 데이터베이스의 데이터 표시</span><span class="sxs-lookup"><span data-stu-id="cb21f-102">Walkthrough: Display Data from a SQL Server Database in a DataGrid Control</span></span>
<span data-ttu-id="cb21f-103">이 연습에서는 SQL Server 데이터베이스에서 데이터를 검색 하 고이 해당 데이터를 표시 한 <xref:System.Windows.Controls.DataGrid> 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-103">In this walkthrough, you retrieve data from a SQL Server database and display that data in a <xref:System.Windows.Controls.DataGrid> control.</span></span> <span data-ttu-id="cb21f-104">ADO.NET Entity Framework를 사용 하 여 데이터를 나타내고, LINQ를 사용 하 여 엔터티 클래스에서 지정된 된 데이터를 검색 하는 쿼리를 작성 하는 엔터티 클래스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-104">You use the ADO.NET Entity Framework to create the entity classes that represent the data, and use LINQ to write a query that retrieves the specified data from an entity class.</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="cb21f-105">전제 조건</span><span class="sxs-lookup"><span data-stu-id="cb21f-105">Prerequisites</span></span>  
 <span data-ttu-id="cb21f-106">이 연습을 완료하려면 다음 구성 요소가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-106">You need the following components to complete this walkthrough:</span></span>  
  
-   [!INCLUDE[vs_dev11_long](../../../../includes/vs-dev11-long-md.md)]<span data-ttu-id="cb21f-107">.</span><span class="sxs-lookup"><span data-stu-id="cb21f-107">.</span></span>  
  
-   <span data-ttu-id="cb21f-108">SQL Server 또는 연결 된 AdventureWorks 샘플 데이터베이스가 있는 SQL Server Express의 실행 중인 인스턴스에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-108">Access to a running instance of SQL Server or SQL Server Express that has the AdventureWorks sample database attached to it.</span></span> <span data-ttu-id="cb21f-109">AdventureWorks 데이터베이스를 다운로드할 수 있습니다 합니다 [GitHub](https://github.com/Microsoft/sql-server-samples/releases)합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-109">You can download the AdventureWorks database from the [GitHub](https://github.com/Microsoft/sql-server-samples/releases).</span></span>  
  
### <a name="to-create-entity-classes"></a><span data-ttu-id="cb21f-110">엔터티 클래스를 만들려면</span><span class="sxs-lookup"><span data-stu-id="cb21f-110">To create entity classes</span></span>  
  
1.  <span data-ttu-id="cb21f-111">Visual Basic 또는 C#에서 새 WPF 응용 프로그램 프로젝트를 만들고 이름을 `DataGridSQLExample`입니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-111">Create a new WPF Application project in Visual Basic or C#, and name it `DataGridSQLExample`.</span></span>  
  
2.  <span data-ttu-id="cb21f-112">솔루션 탐색기에서 프로젝트를 마우스 오른쪽 **추가**를 선택한 후 **새 항목**합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-112">In Solution Explorer, right-click your project, point to **Add**, and then select **New Item**.</span></span>  
  
     <span data-ttu-id="cb21f-113">새 항목 추가 대화 상자가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-113">The Add New Item dialog box appears.</span></span>  
  
3.  <span data-ttu-id="cb21f-114">설치 된 템플릿 창에서 선택 **데이터** 템플릿의 목록에서 선택 하 고 **ADO.NET 엔터티 데이터 모드**l입니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-114">In the Installed Templates pane, select **Data** and in the list of templates, select **ADO.NET Entity Data Mode**l.</span></span>  
  
     <span data-ttu-id="cb21f-115">![ADO.NET 엔터티 데이터 모델 선택](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step1.png "DataGrid_SQL_EF_Step1")</span><span class="sxs-lookup"><span data-stu-id="cb21f-115">![Select ADO.NET Entity Data Model](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step1.png "DataGrid_SQL_EF_Step1")</span></span>  
  
4.  <span data-ttu-id="cb21f-116">파일 이름을 `AdventureWorksModel.edmx` 을 클릭 한 다음 **추가**합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-116">Name the file `AdventureWorksModel.edmx` and then click **Add**.</span></span>  
  
     <span data-ttu-id="cb21f-117">엔터티 데이터 모델 마법사가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-117">The Entity Data Model Wizard appears.</span></span>  
  
5.  <span data-ttu-id="cb21f-118">Model 콘텐츠 선택 화면에서 선택 **데이터베이스에서 생성** 을 클릭 한 다음 **다음**합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-118">In the Choose Model Contents screen, select **Generate from database** and then click **Next**.</span></span>  
  
     <span data-ttu-id="cb21f-119">![데이터베이스 옵션에서 생성 선택](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step2.png "DataGrid_SQL_EF_Step2")</span><span class="sxs-lookup"><span data-stu-id="cb21f-119">![Select Generate from database option](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step2.png "DataGrid_SQL_EF_Step2")</span></span>  
  
6.  <span data-ttu-id="cb21f-120">데이터 연결 선택 화면에서 AdventureWorksLT2008 데이터베이스에 대 한 연결을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-120">In the Choose Your Data Connection screen, provide the connection to your AdventureWorksLT2008 database.</span></span> <span data-ttu-id="cb21f-121">자세한 내용은 [데이터 연결 선택 대화 상자](https://go.microsoft.com/fwlink/?LinkId=160190)합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-121">For more information, see [Choose Your Data Connection Dialog Box](https://go.microsoft.com/fwlink/?LinkId=160190).</span></span>  
  
     <span data-ttu-id="cb21f-122">![데이터베이스 연결을 제공](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step3.png "DataGrid_SQL_EF_Step3")</span><span class="sxs-lookup"><span data-stu-id="cb21f-122">![Provide connection to database](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step3.png "DataGrid_SQL_EF_Step3")</span></span>  
  
7.  <span data-ttu-id="cb21f-123">이름 인지 확인 `AdventureWorksLT2008Entities` 하 고는 **으로 App.Config의 entity 연결 설정 저장** 확인란을 선택한 다음 클릭 **다음**합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-123">Make sure that the name is `AdventureWorksLT2008Entities` and that the **Save entity connection settings in App.Config as** check box is selected, and then click **Next**.</span></span>  
  
8.  <span data-ttu-id="cb21f-124">데이터베이스 개체 선택 화면에서 테이블 노드를 확장 하 고 선택 합니다 **제품** 하 고 **ProductCategory** 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-124">In the Choose Your Database Objects screen, expand the Tables node, and select the **Product** and **ProductCategory** tables.</span></span>  
  
     <span data-ttu-id="cb21f-125">모든 테이블;에 대 한 엔터티 클래스를 생성할 수 있습니다. 그러나이 예제의에서 데이터를 검색할 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-125">You can generate entity classes for all of the tables; however, in this example you only retrieve data from those two tables.</span></span>  
  
     <span data-ttu-id="cb21f-126">![Product 및 ProductCategory 테이블에서 선택](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step4.png "DataGrid_SQL_EF_Step4")</span><span class="sxs-lookup"><span data-stu-id="cb21f-126">![Select Product and ProductCategory from tables](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step4.png "DataGrid_SQL_EF_Step4")</span></span>  
  
9. <span data-ttu-id="cb21f-127">**마침**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-127">Click **Finish**.</span></span>  
  
     <span data-ttu-id="cb21f-128">Product 및 ProductCategory 엔터티는 Entity Designer에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-128">The Product and ProductCategory entities are displayed in the Entity Designer.</span></span>  
  
     <span data-ttu-id="cb21f-129">![Product 및 ProductCategory 엔터티 모델](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step5.png "DataGrid_SQL_EF_Step5")</span><span class="sxs-lookup"><span data-stu-id="cb21f-129">![Product and ProductCategory entity models](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step5.png "DataGrid_SQL_EF_Step5")</span></span>  
  
### <a name="to-retrieve-and-present-the-data"></a><span data-ttu-id="cb21f-130">검색 하 여 데이터를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-130">To retrieve and present the data</span></span>  
  
1.  <span data-ttu-id="cb21f-131">MainWindow.xaml 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-131">Open the MainWindow.xaml file.</span></span>  
  
2.  <span data-ttu-id="cb21f-132">설정 합니다 <xref:System.Windows.FrameworkElement.Width%2A> 속성에는 <xref:System.Windows.Window> 450으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-132">Set the <xref:System.Windows.FrameworkElement.Width%2A> property on the <xref:System.Windows.Window> to 450.</span></span>  
  
3.  <span data-ttu-id="cb21f-133">XAML 편집기에서 다음을 추가 <xref:System.Windows.Controls.DataGrid> 간의 태그를 `<Grid>` 및 `</Grid>` 추가할 태그를 <xref:System.Windows.Controls.DataGrid> 라는 `dataGrid1`.</span><span class="sxs-lookup"><span data-stu-id="cb21f-133">In the XAML editor, add the following <xref:System.Windows.Controls.DataGrid> tag between the `<Grid>` and `</Grid>` tags to add a <xref:System.Windows.Controls.DataGrid> named `dataGrid1`.</span></span>  
  
     [!code-xaml[DataGrid_SQL_EF_Walkthrough#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_SQL_EF_Walkthrough/CS/MainWindow.xaml#3)]  
  
     <span data-ttu-id="cb21f-134">![DataGrid가 있는 창](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step6.png "DataGrid_SQL_EF_Step6")</span><span class="sxs-lookup"><span data-stu-id="cb21f-134">![Window with DataGrid](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step6.png "DataGrid_SQL_EF_Step6")</span></span>  
  
4.  <span data-ttu-id="cb21f-135"><xref:System.Windows.Window>를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-135">Select the <xref:System.Windows.Window>.</span></span>  
  
5.  <span data-ttu-id="cb21f-136">에 대 한 이벤트 처리기를 만들고 속성 창 또는 XAML 편집기를 사용 하는 <xref:System.Windows.Window> 라는 `Window_Loaded` 에 대 한는 <xref:System.Windows.FrameworkElement.Loaded> 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-136">Using the Properties window or XAML editor, create an event handler for the <xref:System.Windows.Window> named `Window_Loaded` for the <xref:System.Windows.FrameworkElement.Loaded> event.</span></span> <span data-ttu-id="cb21f-137">자세한 내용은 [방법: 간단한 이벤트 처리기를 만들고](https://msdn.microsoft.com/library/b1456e07-9dec-4354-99cf-18666b64f480)합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-137">For more information, see [How to: Create a Simple Event Handler](https://msdn.microsoft.com/library/b1456e07-9dec-4354-99cf-18666b64f480).</span></span>  
  
     <span data-ttu-id="cb21f-138">다음은 XAML MainWindow.xaml에 대 한 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-138">The following shows the XAML for MainWindow.xaml.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="cb21f-139">Visual Basic의 경우 MainWindow.xaml의 첫 번째 줄을 사용 하는 경우 대체 `x:Class="DataGridSQLExample.MainWindow"` 사용 하 여 `x:Class="MainWindow"`입니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-139">If you are using Visual Basic, in the first line of MainWindow.xaml, replace `x:Class="DataGridSQLExample.MainWindow"` with `x:Class="MainWindow"`.</span></span>  
  
     [!code-xaml[DataGrid_SQL_EF_Walkthrough#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_SQL_EF_Walkthrough/CS/MainWindow.xaml#1)]  
  
6.  <span data-ttu-id="cb21f-140">(MainWindow.xaml.vb 또는 MainWindow.xaml.cs)의 코드 숨김 파일을 엽니다는 <xref:System.Windows.Window>합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-140">Open the code-behind file (MainWindow.xaml.vb or MainWindow.xaml.cs) for the <xref:System.Windows.Window>.</span></span>  
  
7.  <span data-ttu-id="cb21f-141">조인된 된 테이블의 특정 값만 검색 하 고 설정에 다음 코드를 추가 합니다 <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> 의 속성을 <xref:System.Windows.Controls.DataGrid> 쿼리의 결과에.</span><span class="sxs-lookup"><span data-stu-id="cb21f-141">Add the following code to retrieve only specific values from the joined tables and set the <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> property of the <xref:System.Windows.Controls.DataGrid> to the results of the query.</span></span>  
  
     [!code-csharp[DataGrid_SQL_EF_Walkthrough#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_SQL_EF_Walkthrough/CS/MainWindow.xaml.cs#2)]
     [!code-vb[DataGrid_SQL_EF_Walkthrough#2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DataGrid_SQL_EF_Walkthrough/VB/MainWindow.xaml.vb#2)]  
  
8.  <span data-ttu-id="cb21f-142">예제를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-142">Run the example.</span></span>  
  
     <span data-ttu-id="cb21f-143">표시 된 <xref:System.Windows.Controls.DataGrid> 데이터를 표시 하는 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb21f-143">You should see a <xref:System.Windows.Controls.DataGrid> that displays data.</span></span>  
  
     <span data-ttu-id="cb21f-144">![SQL database에서 데이터를 사용 하 여 DataGrid](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step7.png "DataGrid_SQL_EF_Step7")</span><span class="sxs-lookup"><span data-stu-id="cb21f-144">![DataGrid with data from SQL database](../../../../docs/framework/wpf/controls/media/datagrid-sql-ef-step7.png "DataGrid_SQL_EF_Step7")</span></span>  
  
## <a name="next-steps"></a><span data-ttu-id="cb21f-145">다음 단계</span><span class="sxs-lookup"><span data-stu-id="cb21f-145">Next Steps</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cb21f-146">참고 항목</span><span class="sxs-lookup"><span data-stu-id="cb21f-146">See Also</span></span>  
 <xref:System.Windows.Controls.DataGrid>  
 [<span data-ttu-id="cb21f-147">어떻게 수행 할까요 시작 WPF 응용 프로그램에서 Entity Framework 사용</span><span class="sxs-lookup"><span data-stu-id="cb21f-147">How Do I: Get Started with Entity Framework in WPF Applications?</span></span>](https://go.microsoft.com/fwlink/?LinkId=159868)
