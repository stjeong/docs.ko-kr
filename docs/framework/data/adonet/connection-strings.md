---
title: ADO.NET의 연결 문자열
ms.date: 03/30/2017
ms.assetid: 745c5f95-2f02-4674-b378-6d51a7ec2490
ms.openlocfilehash: 1e6e2b6870195c99279639e1f4576a30b7126d4d
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48583697"
---
# <a name="connection-strings-in-adonet"></a>ADO.NET의 연결 문자열
.NET Framework 2.0에서는 연결 문자열 작성기 클래스에 새로운 키워드를 추가하는 기능을 비롯하여 연결 문자열로 작업하는 데 사용할 수 있는 새로운 기능을 지원합니다. 이러한 기능을 사용하여 런타임에 유효한 연결 문자열을 작성할 수 있습니다.  
  
연결 문자열에는 데이터 공급자에서 데이터 소스에 매개 변수로 전달되는 초기화 정보가 있습니다. 연결 문자열 구문은 데이터 공급자에 따라 다르며 연결을 여는 동안 연결 문자열이 구문 분석됩니다. 구문 오류가 있으면 런타임 예외가 발생하지만, 다른 오류는 데이터 소스에서 연결 정보를 받은 후에만 발생합니다. 유효성을 검사한 후 데이터 소스에서 연결 문자열에 지정된 옵션을 적용하고 연결을 엽니다.
  
연결 문자열 형식은 키/값 매개 변수 쌍의 세미콜론으로 구분된 목록입니다.
  
    keyword1=value; keyword2=value;
  
키워드는 대/소문자 구분 하지 않습니다. 그러나 값을 않을 대/소문자 구분, 데이터 원본에 따라 합니다. 키워드와 값이 포함 될 수 있습니다 [공백 문자](https://en.wikipedia.org/wiki/Whitespace_character#Unicode)선행 및 후행 공백을 키워드에서 무시 되 고 따옴표가 있지만 값입니다.

값에 세미콜론을 포함 되어 있으면 [유니코드 제어 문자](https://en.wikipedia.org/wiki/Unicode_control_characters), 선행 또는 후행 공백을 묶어야 합니다 작은따옴표 또는 큰따옴표, 예를 들어:

    Keyword=" whitespace  ";
    Keyword='special;character';

바깥쪽 문자 값이 포함 될 수 있습니다. 따라서를 큰따옴표로 묶어만 하 고 그 반대의 경우도 마찬가지 작은따옴표를 포함 하는 값을 묶을 수 있습니다.

    Keyword='double"quotation;mark';
    Keyword="single'quotation;mark";

등호 기호 뿐만 아니라 자체에 따옴표 필요 하지 않습니다, 이스케이프 다음 연결 문자열을 유효한 되므로:

    Keyword=no "escaping" 'required';
    Keyword=a=b=c

두 번째 예의 값은 각 값은 다음 세미콜론 이나 문자열의 끝까지 내용은 이후 `a=b=c`, 최종 세미콜론 선택 사항입니다.

유효한 연결 문자열 구문은 공급자에 따라 다르며 ODBC와 유사한 초기 API에서부터 수년에 걸쳐 발전해 왔습니다. .NET Framework Data Provider for SQL Server(SqlClient)는 이전 구문의 많은 요소를 통합하므로 대개 일반적인 연결 문자열 구문보다 융통성이 뛰어납니다. 연결 문자열 구문 요소에는 유효하게 사용할 수 있는 동의어가 많지만 구문과 맞춤법을 잘못 입력하는 일부 경우에는 문제가 발생할 수 있습니다. 예를 들어 "`Integrated Security=true`"는 유효하지만 "`IntegratedSecurity=true`"는 오류를 일으킵니다. 또한 유효성이 검증되지 않은 사용자 입력을 통해 런타임에 구성된 연결 문자열은 문자열 삽입 공격으로 이어져 데이터 소스의 보안을 위협할 수 있습니다.
  
이러한 문제를 해결하기 위해 ADO.NET 2.0에서는 각 .NET Framework 데이터 공급자에 사용할 수 있는 새로운 연결 문자열 작성기가 도입되었습니다. 키워드는 속성으로 노출되므로 데이터 소스에 제출하기 전에 연결 문자열 구문의 유효성을 검사할 수 있습니다.
  
## <a name="in-this-section"></a>섹션 내용  
 [연결 문자열 작성기](../../../../docs/framework/data/adonet/connection-string-builders.md)  
 `ConnectionStringBuilder` 클래스를 사용하여 런타임에 유효한 연결 문자열을 구성하는 방법을 보여 줍니다.
  
 [연결 문자열 및 구성 파일](../../../../docs/framework/data/adonet/connection-strings-and-configuration-files.md)  
 구성 파일에서 연결 문자열을 저장하고 검색하는 방법을 보여 줍니다.
  
 [연결 문자열 구문](../../../../docs/framework/data/adonet/connection-string-syntax.md)  
 `SqlClient`, `OracleClient`, `OleDb` 및 `Odbc`에 대한 공급자별 연결 문자열을 구성하는 방법을 설명합니다.
  
 [연결 정보 보호](../../../../docs/framework/data/adonet/protecting-connection-information.md)  
 데이터 소스 연결에 사용되는 정보를 보호하는 기법을 보여 줍니다.
  
## <a name="see-also"></a>참고 항목  
 [데이터 소스에 연결](/cpp/data/odbc/connecting-to-a-data-source)  
 [ADO.NET 관리되는 공급자 및 데이터 집합 개발자 센터](https://go.microsoft.com/fwlink/?LinkId=217917)
