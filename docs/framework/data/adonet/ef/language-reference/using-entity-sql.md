---
title: USING(Entity SQL)
ms.date: 03/30/2017
ms.assetid: 20f58b8f-6070-4456-b7e8-5ff3d6269273
ms.openlocfilehash: a07ee1c32a93ee22b7418784fbd893e7699c553e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54744299"
---
# <a name="using-entity-sql"></a><span data-ttu-id="fadf2-102">USING(Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="fadf2-102">USING (Entity SQL)</span></span>
<span data-ttu-id="fadf2-103">쿼리 식에 사용되는 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fadf2-103">Specifies namespaces used in a query expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fadf2-104">구문</span><span class="sxs-lookup"><span data-stu-id="fadf2-104">Syntax</span></span>  
  
```  
USING [ alias = ] namespace  
```  
  
## <a name="arguments"></a><span data-ttu-id="fadf2-105">인수</span><span class="sxs-lookup"><span data-stu-id="fadf2-105">Arguments</span></span>  
 `alias`  
 <span data-ttu-id="fadf2-106">네임스페이스를 정규화하는 데 사용할 짧은 별칭을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fadf2-106">Specifies a shorter alias to qualify a namespace with.</span></span>  
  
 `namespace`  
 <span data-ttu-id="fadf2-107">유효한 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="fadf2-107">Any valid namespace.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fadf2-108">예제</span><span class="sxs-lookup"><span data-stu-id="fadf2-108">Example</span></span>  
 <span data-ttu-id="fadf2-109">다음 Entity SQL 쿼리에서는 USING 연산자를 사용하여 쿼리 식에 사용되는 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fadf2-109">The following Entity SQL query uses the USING operator to specify namespaces used in a query expression.</span></span> <span data-ttu-id="fadf2-110">이 쿼리를 컴파일하고 실행하려면 다음 단계를 수행하세요.</span><span class="sxs-lookup"><span data-stu-id="fadf2-110">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="fadf2-111">절차에 따라 [방법: PrimitiveType 결과 반환 하는 쿼리 실행](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-primitivetype-results.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="fadf2-111">Follow the procedure in [How to: Execute a Query that Returns PrimitiveType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-primitivetype-results.md).</span></span>  
  
2.  <span data-ttu-id="fadf2-112">다음 쿼리를 `ExecutePrimitiveTypeQuery` 메서드에 인수로 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="fadf2-112">Pass the following query as an argument to the `ExecutePrimitiveTypeQuery` method:</span></span>  
  
```  
using SqlServer; RAND()  
```  
  
## <a name="see-also"></a><span data-ttu-id="fadf2-113">참고자료</span><span class="sxs-lookup"><span data-stu-id="fadf2-113">See also</span></span>
- [<span data-ttu-id="fadf2-114">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="fadf2-114">Namespaces</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/namespaces-entity-sql.md)
- [<span data-ttu-id="fadf2-115">엔터티 SQL 참조</span><span class="sxs-lookup"><span data-stu-id="fadf2-115">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
