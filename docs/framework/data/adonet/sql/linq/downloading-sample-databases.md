---
title: ADO.NET 코드 샘플에 대 한 샘플 데이터베이스를 가져옵니다.
description: SQL Server 및 관리 도구 뿐만 아니라 ADO.NET 설명서의 코드 샘플에 사용 된 샘플 데이터베이스 다운로드
ms.date: 10/12/2018
ms.assetid: ef9d69a1-9461-43fe-94bb-7c836754bcb5
ms.openlocfilehash: 75ae1895d683b669f51b33130fc2f47010e39814
ms.sourcegitcommit: fd8d4587cc26e53f0e27e230d6e27d828ef4306b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2018
ms.locfileid: "49347520"
---
# <a name="get-the-sample-databases-for-adonet-code-samples"></a>ADO.NET 코드 샘플에 대 한 샘플 데이터베이스를 가져옵니다.

다양 한 샘플 및 연습에는 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 설명서 예제 데이터베이스 및 SQL Server Express를 사용 합니다. Microsoft에서 이러한 제품을 무료로 다운로드할 수 있습니다.

## <a name="get-the-adventureworks-sample-database"></a>AdventureWorks 예제 데이터베이스를 가져오려면

AdventureWorks 예제 데이터베이스를 다음 GitHub 리포지토리에서 다운로드 합니다.

[AdventureWorks 예제 데이터베이스](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks)

데이터베이스 백업 중 하나를 다운로드 한 후 (\*.bak) 파일을 SQL Server Management Studio (SSMS)를 사용 하 여 SQL Server 인스턴스에 백업을 복원 합니다. 참조 [SQL Server Management Studio를 가져오려면](#get_ssms)합니다.

## <a name="get-the-northwind-sample-database"></a>Northwind 샘플 데이터베이스를 가져오려면

Microsoft 다운로드 센터에서 다음 페이지에서 Northwind 샘플 데이터베이스를 다운로드 합니다.

[Northwind 및 Pubs 샘플 데이터베이스](https://go.microsoft.com/fwlink?linkid=64296)

파일을 다운로드 한 후에 데이터베이스 및 스크립트를 추출 하는 파일을 두 번 클릭 합니다. 기본적으로 파일 폴더에 설치 된 `<drive>:\SQL Server 2000 Sample Databases`합니다.

Northwind 데이터베이스를 사용 하려면 먼저 다음 작업 중 하나를 수행 해야 합니다.

- 실행 하 여 SQL Server 인스턴스에서 데이터베이스를 다시는 `instnwnd.sql` 설치 폴더에서 스크립트 파일입니다.

- 연결 된 `northwnd.mdf` 해당 파일 `*.ldf` SQL Server 인스턴스의 로그 파일입니다.

## <a name="get_sql"></a> SQL Server Express 얻기

SQL Server Express는 무료의 초급 수준 버전 SQL server 응용 프로그램과 함께 재배포할 수 있습니다. 다음 페이지에서 SQL Server Express를 다운로드 합니다.
  
[SQL Server Express Edition](https://www.microsoft.com/sql-server/sql-server-editions-express)

사용 중인 경우 [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), SQL Server Express LocalDB Professional 이상 버전 뿐만 아니라 Community edition에 포함 됩니다.  

## <a name="get_ssms"></a> SQL Server Management Studio 다운로드
보기 또는 다운로드 한 데이터베이스를 수정 하려는 경우에 SQL Server Management Studio (SSMS)를 사용할 수 있습니다. 다음 페이지에서 SSMS를 다운로드 합니다.

[SQL Server Management Studio (SSMS) 다운로드](/sql/ssms/download-sql-server-management-studio-ssms) 

볼 수 있으며 Visual Studio 통합된 개발 환경 (IDE)에서 데이터베이스를 관리할 수도 있습니다. [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)에서 데이터베이스에 연결 **SQL Server 개체 탐색기**, 데이터베이스에 데이터 연결을 만들거나 **서버 탐색기**합니다. 이러한 탐색기 창에서 엽니다는 **보기** 메뉴.
  
## <a name="see-also"></a>참고자료

- [시작](../../../../../../docs/framework/data/adonet/sql/linq/getting-started.md)
