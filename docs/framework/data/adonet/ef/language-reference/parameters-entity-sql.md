---
title: 매개 변수(Entity SQL)
ms.date: 03/30/2017
ms.assetid: 8d618edd-0988-4ff2-8263-ce59448af7a5
ms.openlocfilehash: 5fa050e43e4590f61c3011a1b9bb0937da7032a3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54632389"
---
# <a name="parameters-entity-sql"></a><span data-ttu-id="e3330-102">매개 변수(Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="e3330-102">Parameters (Entity SQL)</span></span>
<span data-ttu-id="e3330-103">매개 변수는 일반적으로 호스트 언어에서 사용되는 바인딩 API를 통해 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 외부에서 정의되는 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="e3330-103">Parameters are variables that are defined outside [!INCLUDE[esql](../../../../../../includes/esql-md.md)], usually through a binding API that is used by a host language.</span></span> <span data-ttu-id="e3330-104">각 매개 변수에는 이름과 형식이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3330-104">Each parameter has a name and a type.</span></span> <span data-ttu-id="e3330-105">매개 변수 이름은 쿼리 식에서 정의 되는에 (@) 기호가 접두사로 사용 되므로 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3330-105">Parameter names are defined in query expressions with the at (@) symbol as a prefix.</span></span> <span data-ttu-id="e3330-106">쿼리에서 정의되는 속성 이름이나 다른 이름과 쉽게 구분할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3330-106">This disambiguates them from the names of properties or other names that are defined in the query.</span></span>  
  
 <span data-ttu-id="e3330-107">호스트 언어 바인딩 API는 매개 변수 바인딩을 위한 API를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e3330-107">The host-language binding API provides APIs for binding parameters.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e3330-108">예제</span><span class="sxs-lookup"><span data-stu-id="e3330-108">Example</span></span>  
  
```  
select c   
      from LOB.Customers as c   
      where c.Name = @name  
```  
  
## <a name="see-also"></a><span data-ttu-id="e3330-109">참고자료</span><span class="sxs-lookup"><span data-stu-id="e3330-109">See also</span></span>
- [<span data-ttu-id="e3330-110">엔터티 SQL 참조</span><span class="sxs-lookup"><span data-stu-id="e3330-110">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
- [<span data-ttu-id="e3330-111">Entity SQL 개요</span><span class="sxs-lookup"><span data-stu-id="e3330-111">Entity SQL Overview</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
