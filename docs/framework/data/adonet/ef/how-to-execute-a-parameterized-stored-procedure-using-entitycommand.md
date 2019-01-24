---
title: '방법: EntityCommand를 사용하여 매개 변수 있는 저장 프로시저 실행'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 4f5639bf-bb7f-4982-bb1d-c7caa4348888
ms.openlocfilehash: 11894decbb81192eb68c680149bbe9f7398f0203
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54587815"
---
# <a name="how-to-execute-a-parameterized-stored-procedure-using-entitycommand"></a><span data-ttu-id="5f180-102">방법: EntityCommand를 사용하여 매개 변수 있는 저장 프로시저 실행</span><span class="sxs-lookup"><span data-stu-id="5f180-102">How to: Execute a Parameterized Stored Procedure Using EntityCommand</span></span>
<span data-ttu-id="5f180-103">이 항목에서는 <xref:System.Data.EntityClient.EntityCommand> 클래스를 사용하여 매개 변수가 있는 저장 프로시저를 실행하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5f180-103">This topic shows how to execute a parameterized stored procedure by using the <xref:System.Data.EntityClient.EntityCommand> class.</span></span>  
  
### <a name="to-run-the-code-in-this-example"></a><span data-ttu-id="5f180-104">이 예제의 코드를 실행하려면</span><span class="sxs-lookup"><span data-stu-id="5f180-104">To run the code in this example</span></span>  
  
1.  <span data-ttu-id="5f180-105">추가 합니다 [School 모델](https://msdn.microsoft.com/library/859a9587-81ea-4a45-9bc0-f8d330e1adac) 프로젝트에 사용 하도록 프로젝트를 구성 하 고는 [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]합니다.</span><span class="sxs-lookup"><span data-stu-id="5f180-105">Add the [School Model](https://msdn.microsoft.com/library/859a9587-81ea-4a45-9bc0-f8d330e1adac) to your project and configure your project to use the [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span></span> <span data-ttu-id="5f180-106">자세한 내용은 [방법: 엔터티 데이터 모델 마법사를 사용 하 여](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d)입니다.</span><span class="sxs-lookup"><span data-stu-id="5f180-106">For more information, see [How to: Use the Entity Data Model Wizard](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d).</span></span>  
  
2.  <span data-ttu-id="5f180-107">응용 프로그램의 코드 페이지에서 다음 `using` 문(Visual Basic에서는 `Imports`)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5f180-107">In the code page for your application, add the following `using` statements (`Imports` in Visual Basic):</span></span>  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
3.  <span data-ttu-id="5f180-108">`GetStudentGrades` 저장 프로시저를 가져오고 `CourseGrade` 엔터티를 반환 형식으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f180-108">Import the `GetStudentGrades` stored procedure and specify `CourseGrade` entities as a return type.</span></span> <span data-ttu-id="5f180-109">저장된 프로시저를 가져오는 방법에 대 한 자세한 내용은 [방법: 저장된 프로시저 가져오기](https://msdn.microsoft.com/library/24e68bf4-bd6d-428d-bc35-92d7b8e3736d)합니다.</span><span class="sxs-lookup"><span data-stu-id="5f180-109">For information on how to import a stored procedure, see [How to: Import a Stored Procedure](https://msdn.microsoft.com/library/24e68bf4-bd6d-428d-bc35-92d7b8e3736d).</span></span>  
  
## <a name="example"></a><span data-ttu-id="5f180-110">예제</span><span class="sxs-lookup"><span data-stu-id="5f180-110">Example</span></span>  
 <span data-ttu-id="5f180-111">다음 코드에서는 `GetStudentGrades`가 필수 매개 변수인 `StudentId` 저장 프로시저를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5f180-111">The following code executes the `GetStudentGrades` stored procedure where `StudentId` is a required parameter.</span></span> <span data-ttu-id="5f180-112">그런 다음 <xref:System.Data.EntityClient.EntityDataReader>에서 결과를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="5f180-112">The results are then read by an <xref:System.Data.EntityClient.EntityDataReader>.</span></span>  
  
 [!code-csharp[DP EntityServices Concepts#StoredProcWithEntityCommand](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#storedprocwithentitycommand)]
 [!code-vb[DP EntityServices Concepts#StoredProcWithEntityCommand](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#storedprocwithentitycommand)]  
  
## <a name="see-also"></a><span data-ttu-id="5f180-113">참고자료</span><span class="sxs-lookup"><span data-stu-id="5f180-113">See also</span></span>
- [<span data-ttu-id="5f180-114">Entity Framework용 EntityClient 공급자</span><span class="sxs-lookup"><span data-stu-id="5f180-114">EntityClient Provider for the Entity Framework</span></span>](../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md)
