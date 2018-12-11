---
title: ADO.NET 코드 샘플에 대 한 샘플 SQL Server 데이터베이스를 가져옵니다.
description: SQL Server 및 관리 도구 뿐만 아니라 ADO.NET 설명서의 코드 샘플에 사용 된 샘플 SQL Server 데이터베이스를 다운로드 합니다.
ms.date: 10/18/2018
ms.assetid: ef9d69a1-9461-43fe-94bb-7c836754bcb5
ms.openlocfilehash: 8ab65f992c9cf2b65271a237fa06eb96e358ae6a
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53153490"
---
# <a name="get-the-sample-databases-for-adonet-code-samples"></a><span data-ttu-id="cced4-103">ADO.NET 코드 샘플에 대 한 샘플 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-103">Get the sample databases for ADO.NET code samples</span></span>

<span data-ttu-id="cced4-104">다양 한 예제 및 연습에는 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 설명서 샘플 SQL Server 데이터베이스 및 SQL Server Express를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-104">A number of examples and walkthroughs in the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] documentation use sample SQL Server databases and SQL Server Express.</span></span> <span data-ttu-id="cced4-105">Microsoft에서 이러한 제품을 무료로 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-105">You can download these products free of charge from Microsoft.</span></span>

## <a name="get-the-northwind-sample-database-for-sql-server"></a><span data-ttu-id="cced4-106">SQL Server 용 Northwind 샘플 데이터베이스를 가져오려면</span><span class="sxs-lookup"><span data-stu-id="cced4-106">Get the Northwind sample database for SQL Server</span></span>

<span data-ttu-id="cced4-107">스크립트를 다운로드 `instnwnd.sql` 다음 GitHub 리포지토리를 만들고 SQL Server 용 Northwind 샘플 데이터베이스 로드에서:</span><span class="sxs-lookup"><span data-stu-id="cced4-107">Download the script `instnwnd.sql` from the following GitHub repository to create and load the Northwind sample database for SQL Server:</span></span>

[<span data-ttu-id="cced4-108">Microsoft SQL Server 용 Northwind 및 pubs 샘플 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="cced4-108">Northwind and pubs sample databases for Microsoft SQL Server</span></span>](https://github.com/Microsoft/sql-server-samples/tree/master/samples/databases/northwind-pubs)

<span data-ttu-id="cced4-109">다운로드 한 실행 해야 하는 Northwind 데이터베이스를 사용 하려면 먼저 `instnwnd.sql` 스크립트 파일을 사용 하 여 SQL Server 인스턴스에서 데이터베이스를 다시 만드는 [SQL Server Management Studio](#get_ssms) 또는 유사한 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-109">Before you can use the Northwind database, you have to run the downloaded `instnwnd.sql` script file to recreate the database on an instance of SQL Server by using [SQL Server Management Studio](#get_ssms) or a similar tool.</span></span> <span data-ttu-id="cced4-110">리포지토리의 추가 정보 파일의 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-110">Follow the instructions in the Readme file in the repository.</span></span>

> [!TIP]
> <span data-ttu-id="cced4-111">Microsoft Access 용 Northwind 데이터베이스에 대 한 찾고 볼 [Microsoft Access 용 Northwind 샘플 데이터베이스 설치](#northwind_access)합니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-111">If you're looking for the Northwind database for Microsoft Access, see [Install the Northwind sample database for Microsoft Access](#northwind_access).</span></span>

## <a name="get-the-adventureworks-sample-database-for-sql-server"></a><span data-ttu-id="cced4-112">SQL Server에 대 한 AdventureWorks 예제 데이터베이스를 가져오려면</span><span class="sxs-lookup"><span data-stu-id="cced4-112">Get the AdventureWorks sample database for SQL Server</span></span>

<span data-ttu-id="cced4-113">다음 GitHub 리포지토리에서 SQL Server 용 AdventureWorks 샘플 데이터베이스를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-113">Download the AdventureWorks sample database for SQL Server from the following GitHub repository:</span></span>

[<span data-ttu-id="cced4-114">AdventureWorks 예제 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="cced4-114">AdventureWorks sample databases</span></span>](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks)

<span data-ttu-id="cced4-115">데이터베이스 백업 중 하나를 다운로드 한 후 (\*.bak) 파일을 SQL Server Management Studio (SSMS)를 사용 하 여 SQL Server 인스턴스에 백업을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-115">After you download one of the database backup (\*.bak) files, restore the backup to an instance of SQL Server by using SQL Server Management Studio (SSMS).</span></span> <span data-ttu-id="cced4-116">참조 [SQL Server Management Studio를 가져오려면](#get_ssms)합니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-116">See [Get SQL Server Management Studio](#get_ssms).</span></span>

## <a name="get_sql"></a> <span data-ttu-id="cced4-117">SQL Server Express 얻기</span><span class="sxs-lookup"><span data-stu-id="cced4-117">Get SQL Server Express</span></span>

<span data-ttu-id="cced4-118">SQL Server Express는 무료의 초급 수준 버전 SQL server 응용 프로그램과 함께 재배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-118">SQL Server Express is a free, entry-level edition of SQL Server that you can redistribute with applications.</span></span> <span data-ttu-id="cced4-119">다음 페이지에서 SQL Server Express를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-119">Download SQL Server Express from the following page:</span></span>
  
[<span data-ttu-id="cced4-120">SQL Server Express Edition</span><span class="sxs-lookup"><span data-stu-id="cced4-120">SQL Server Express Edition</span></span>](https://www.microsoft.com/sql-server/sql-server-editions-express)

<span data-ttu-id="cced4-121">사용 중인 경우 [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), SQL Server Express LocalDB Professional 이상 버전 뿐만 아니라 Visual Studio의 무료 Community edition에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-121">If you're using [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), SQL Server Express LocalDB is included in the free Community edition of Visual Studio, as well as the Professional and higher editions.</span></span>  

## <a name="get_ssms"></a> <span data-ttu-id="cced4-122">SQL Server Management Studio 다운로드</span><span class="sxs-lookup"><span data-stu-id="cced4-122">Get SQL Server Management Studio</span></span>
<span data-ttu-id="cced4-123">보기 또는 다운로드 한 데이터베이스를 수정 하려는 경우에 SQL Server Management Studio (SSMS)를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-123">If you want to view or modify a database that you've downloaded, you can use SQL Server Management Studio (SSMS).</span></span> <span data-ttu-id="cced4-124">다음 페이지에서 SSMS를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-124">Download SSMS from the following page:</span></span>

[<span data-ttu-id="cced4-125">SQL Server Management Studio (SSMS) 다운로드</span><span class="sxs-lookup"><span data-stu-id="cced4-125">Download SQL Server Management Studio (SSMS)</span></span>](/sql/ssms/download-sql-server-management-studio-ssms) 

<span data-ttu-id="cced4-126">볼 수 있으며 Visual Studio 통합된 개발 환경 (IDE)에서 데이터베이스를 관리할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-126">You can also view and manage databases in the Visual Studio integrated development environment (IDE).</span></span> <span data-ttu-id="cced4-127">[Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)에서 데이터베이스에 연결 **SQL Server 개체 탐색기**, 데이터베이스에 데이터 연결을 만들거나 **서버 탐색기**합니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-127">In [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), connect to the database from **SQL Server Object Explorer**, or create a Data Connection to the database in **Server Explorer**.</span></span> <span data-ttu-id="cced4-128">이러한 탐색기 창에서 엽니다는 **보기** 메뉴.</span><span class="sxs-lookup"><span data-stu-id="cced4-128">Open these explorer panes from the **View** menu.</span></span>

## <a name="northwind_access"></a> <span data-ttu-id="cced4-129">Microsoft Access 용 Northwind 샘플 데이터베이스 설치</span><span class="sxs-lookup"><span data-stu-id="cced4-129">Install the Northwind sample database for Microsoft Access</span></span>

<span data-ttu-id="cced4-130">Microsoft Access 용 Northwind 샘플 데이터베이스는 Microsoft 다운로드 센터에서 사용할 수 없는 경우</span><span class="sxs-lookup"><span data-stu-id="cced4-130">The Northwind sample database for Microsoft Access is not available on the Microsoft Download Center.</span></span> <span data-ttu-id="cced4-131">Access 내에서 직접 Northwind를 설치 하려면 다음 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-131">To install Northwind directly from within Access, do the following things:</span></span>

1. <span data-ttu-id="cced4-132">액세스를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-132">Open Access.</span></span>

1. <span data-ttu-id="cced4-133">Enter **Northwind** 에 **온라인 템플릿 검색** 상자를 선택한 후 **Enter**합니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-133">Enter **Northwind** in the **Search for Online Templates** box, and then select **Enter**.</span></span>

1. <span data-ttu-id="cced4-134">결과 화면에서 선택 **Northwind**합니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-134">On the results screen, select **Northwind**.</span></span> <span data-ttu-id="cced4-135">Northwind 데이터베이스에 대 한 설명을 사용 하 여 새 창이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-135">A new window opens with a description of the Northwind database.</span></span>

1. <span data-ttu-id="cced4-136">새 창에서에 **파일 이름** 텍스트 상자에서 Northwind 데이터베이스에 대 한 파일 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-136">In the new window, in the **File Name** text box, provide a filename for your copy of the Northwind database.</span></span>

1. <span data-ttu-id="cced4-137">**만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-137">Select **Create**.</span></span> <span data-ttu-id="cced4-138">액세스는 Northwind 데이터베이스를 다운로드 하 고 파일을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-138">Access downloads the Northwind database and prepares the file.</span></span>

1. <span data-ttu-id="cced4-139">이 프로세스가 완료 되 면 데이터베이스가 시작 화면이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="cced4-139">When this process is complete, the database opens with a Welcome screen.</span></span>

## <a name="see-also"></a><span data-ttu-id="cced4-140">참고 항목</span><span class="sxs-lookup"><span data-stu-id="cced4-140">See also</span></span>

- [<span data-ttu-id="cced4-141">시작</span><span class="sxs-lookup"><span data-stu-id="cced4-141">Getting Started</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/getting-started.md)
