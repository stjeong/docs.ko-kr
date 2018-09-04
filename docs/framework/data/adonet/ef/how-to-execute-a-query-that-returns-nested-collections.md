---
title: '방법: 중첩된 컬렉션을 반환하는 쿼리 실행'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: f7f385f3-ffcf-4f3b-af35-de8818938e5f
ms.openlocfilehash: 5e282bce5f2519592babad0afcf7f8a326cf936d
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43530570"
---
# <a name="how-to-execute-a-query-that-returns-nested-collections"></a><span data-ttu-id="973a1-102">방법: 중첩된 컬렉션을 반환하는 쿼리 실행</span><span class="sxs-lookup"><span data-stu-id="973a1-102">How to: Execute a Query that Returns Nested Collections</span></span>
<span data-ttu-id="973a1-103">여기에서는 <xref:System.Data.EntityClient.EntityCommand> 개체를 사용하여 개념적 모델에 대해 명령을 실행하는 방법 및 <xref:System.Data.EntityClient.EntityDataReader>를 사용하여 중첩 컬렉션 결과를 검색하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="973a1-103">This shows how to execute a command against a conceptual model by using an <xref:System.Data.EntityClient.EntityCommand> object, and how to retrieve the nested collection results by using an <xref:System.Data.EntityClient.EntityDataReader>.</span></span>  
  
### <a name="to-run-the-code-in-this-example"></a><span data-ttu-id="973a1-104">이 예제의 코드를 실행하려면</span><span class="sxs-lookup"><span data-stu-id="973a1-104">To run the code in this example</span></span>  
  
1.  <span data-ttu-id="973a1-105">추가 합니다 [AdventureWorks Sales 모델](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) 프로젝트에 사용 하도록 프로젝트를 구성 하 고는 [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]합니다.</span><span class="sxs-lookup"><span data-stu-id="973a1-105">Add the [AdventureWorks Sales Model](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) to your project and configure your project to use the [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span></span> <span data-ttu-id="973a1-106">자세한 내용은 [방법: 엔터티 데이터 모델 마법사를 사용 하 여](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d)입니다.</span><span class="sxs-lookup"><span data-stu-id="973a1-106">For more information, see [How to: Use the Entity Data Model Wizard](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d).</span></span>  
  
2.  <span data-ttu-id="973a1-107">응용 프로그램의 코드 페이지에서 다음 `using` 문(Visual Basic에서는 `Imports`)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="973a1-107">In the code page for your application, add the following `using` statements (`Imports` in Visual Basic):</span></span>  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
## <a name="example"></a><span data-ttu-id="973a1-108">예제</span><span class="sxs-lookup"><span data-stu-id="973a1-108">Example</span></span>  
 <span data-ttu-id="973a1-109">A *중첩 컬렉션* 다른 컬렉션 내에 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="973a1-109">A *nested collection* is a collection that is inside another collection.</span></span> <span data-ttu-id="973a1-110">다음 코드에서는 `Contacts` 컬렉션과 각 `SalesOrderHeaders`에 연결된 `Contact`의 중첩 컬렉션을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="973a1-110">The following code retrieves a collection of `Contacts` and the nested collections of `SalesOrderHeaders` that are associated with each `Contact`.</span></span>  
  
 [!code-csharp[DP EntityServices Concepts#ReturnNestedCollectionWithEntityCommand](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#returnnestedcollectionwithentitycommand)]
 [!code-vb[DP EntityServices Concepts#ReturnNestedCollectionWithEntityCommand](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#returnnestedcollectionwithentitycommand)]  
  
## <a name="see-also"></a><span data-ttu-id="973a1-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="973a1-111">See Also</span></span>  
 [<span data-ttu-id="973a1-112">Entity Framework용 EntityClient 공급자</span><span class="sxs-lookup"><span data-stu-id="973a1-112">EntityClient Provider for the Entity Framework</span></span>](../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md)
