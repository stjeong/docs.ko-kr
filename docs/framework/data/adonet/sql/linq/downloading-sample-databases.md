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
# <a name="get-the-sample-databases-for-adonet-code-samples"></a>ADO.NET 코드 샘플에 대 한 샘플 데이터베이스를 가져옵니다.

다양 한 예제 및 연습에는 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 설명서 샘플 SQL Server 데이터베이스 및 SQL Server Express를 사용 합니다. Microsoft에서 이러한 제품을 무료로 다운로드할 수 있습니다.

## <a name="get-the-northwind-sample-database-for-sql-server"></a>SQL Server 용 Northwind 샘플 데이터베이스를 가져오려면

스크립트를 다운로드 `instnwnd.sql` 다음 GitHub 리포지토리를 만들고 SQL Server 용 Northwind 샘플 데이터베이스 로드에서:

[Microsoft SQL Server 용 Northwind 및 pubs 샘플 데이터베이스](https://github.com/Microsoft/sql-server-samples/tree/master/samples/databases/northwind-pubs)

다운로드 한 실행 해야 하는 Northwind 데이터베이스를 사용 하려면 먼저 `instnwnd.sql` 스크립트 파일을 사용 하 여 SQL Server 인스턴스에서 데이터베이스를 다시 만드는 [SQL Server Management Studio](#get_ssms) 또는 유사한 도구입니다. 리포지토리의 추가 정보 파일의 지침을 따릅니다.

> [!TIP]
> Microsoft Access 용 Northwind 데이터베이스에 대 한 찾고 볼 [Microsoft Access 용 Northwind 샘플 데이터베이스 설치](#northwind_access)합니다.

## <a name="get-the-adventureworks-sample-database-for-sql-server"></a>SQL Server에 대 한 AdventureWorks 예제 데이터베이스를 가져오려면

다음 GitHub 리포지토리에서 SQL Server 용 AdventureWorks 샘플 데이터베이스를 다운로드 합니다.

[AdventureWorks 예제 데이터베이스](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks)

데이터베이스 백업 중 하나를 다운로드 한 후 (\*.bak) 파일을 SQL Server Management Studio (SSMS)를 사용 하 여 SQL Server 인스턴스에 백업을 복원 합니다. 참조 [SQL Server Management Studio를 가져오려면](#get_ssms)합니다.

## <a name="get_sql"></a> SQL Server Express 얻기

SQL Server Express는 무료의 초급 수준 버전 SQL server 응용 프로그램과 함께 재배포할 수 있습니다. 다음 페이지에서 SQL Server Express를 다운로드 합니다.
  
[SQL Server Express Edition](https://www.microsoft.com/sql-server/sql-server-editions-express)

사용 중인 경우 [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), SQL Server Express LocalDB Professional 이상 버전 뿐만 아니라 Visual Studio의 무료 Community edition에 포함 됩니다.  

## <a name="get_ssms"></a> SQL Server Management Studio 다운로드
보기 또는 다운로드 한 데이터베이스를 수정 하려는 경우에 SQL Server Management Studio (SSMS)를 사용할 수 있습니다. 다음 페이지에서 SSMS를 다운로드 합니다.

[SQL Server Management Studio (SSMS) 다운로드](/sql/ssms/download-sql-server-management-studio-ssms) 

볼 수 있으며 Visual Studio 통합된 개발 환경 (IDE)에서 데이터베이스를 관리할 수도 있습니다. [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)에서 데이터베이스에 연결 **SQL Server 개체 탐색기**, 데이터베이스에 데이터 연결을 만들거나 **서버 탐색기**합니다. 이러한 탐색기 창에서 엽니다는 **보기** 메뉴.

## <a name="northwind_access"></a> Microsoft Access 용 Northwind 샘플 데이터베이스 설치

Microsoft Access 용 Northwind 샘플 데이터베이스는 Microsoft 다운로드 센터에서 사용할 수 없는 경우 Access 내에서 직접 Northwind를 설치 하려면 다음 작업을 수행 합니다.

1. 액세스를 엽니다.

1. Enter **Northwind** 에 **온라인 템플릿 검색** 상자를 선택한 후 **Enter**합니다.

1. 결과 화면에서 선택 **Northwind**합니다. Northwind 데이터베이스에 대 한 설명을 사용 하 여 새 창이 열립니다.

1. 새 창에서에 **파일 이름** 텍스트 상자에서 Northwind 데이터베이스에 대 한 파일 이름을 제공 합니다.

1. **만들기**를 선택합니다. 액세스는 Northwind 데이터베이스를 다운로드 하 고 파일을 준비 합니다.

1. 이 프로세스가 완료 되 면 데이터베이스가 시작 화면이 열립니다.

## <a name="see-also"></a>참고 항목

- [시작](../../../../../../docs/framework/data/adonet/sql/linq/getting-started.md)
