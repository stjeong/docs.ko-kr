---
title: 변수(Entity SQL)
ms.date: 03/30/2017
ms.assetid: 3eed222a-f8f6-46b6-9cd5-220cc0e4e5d8
ms.openlocfilehash: a16c450401eee1021aeef885fba129c943a87fd7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54742274"
---
# <a name="variables-entity-sql"></a><span data-ttu-id="dac2e-102">변수(Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="dac2e-102">Variables (Entity SQL)</span></span>
## <a name="variable"></a><span data-ttu-id="dac2e-103">변수</span><span class="sxs-lookup"><span data-stu-id="dac2e-103">Variable</span></span>  
 <span data-ttu-id="dac2e-104">변수 식은 현재 범위에 정의된 명명된 식에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="dac2e-104">A variable expression is a reference to a named expression defined in the current scope.</span></span> <span data-ttu-id="dac2e-105">변수 참조는 유효 해야 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 식별자에 정의 된 대로 [식별자](../../../../../../docs/framework/data/adonet/ef/language-reference/identifiers-entity-sql.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="dac2e-105">A variable reference must be a valid [!INCLUDE[esql](../../../../../../includes/esql-md.md)] identifier, as defined in [Identifiers](../../../../../../docs/framework/data/adonet/ef/language-reference/identifiers-entity-sql.md).</span></span>  
  
 <span data-ttu-id="dac2e-106">다음 예제에서는 식에서 변수 사용을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dac2e-106">The following example shows the use of a variable in the expression.</span></span> <span data-ttu-id="dac2e-107">FROM 절의 `c`는 변수 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="dac2e-107">The `c` in the FROM clause is the definition of the variable.</span></span> <span data-ttu-id="dac2e-108">SELECT 절의 `c` 사용은 변수 참조를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dac2e-108">The use of `c` in the SELECT clause represents the variable reference.</span></span>  
  
```  
select c   
from LOB.customers as c  
```  
  
## <a name="see-also"></a><span data-ttu-id="dac2e-109">참고자료</span><span class="sxs-lookup"><span data-stu-id="dac2e-109">See also</span></span>
- [<span data-ttu-id="dac2e-110">식별자</span><span class="sxs-lookup"><span data-stu-id="dac2e-110">Identifiers</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/identifiers-entity-sql.md)
- [<span data-ttu-id="dac2e-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="dac2e-111">Parameters</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/parameters-entity-sql.md)
- [<span data-ttu-id="dac2e-112">Entity SQL 개요</span><span class="sxs-lookup"><span data-stu-id="dac2e-112">Entity SQL Overview</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
