---
title: '방법: EdmGen.exe를 사용 하 여 모델 및 매핑 파일 유효성을 검사 하려면'
ms.date: 03/30/2017
ms.assetid: 2641906a-971a-4d0b-8aee-13fabc02a1cc
ms.openlocfilehash: 87150aee8eac6a594b18b77230889c1208003dde
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54566361"
---
# <a name="how-to-use-edmgenexe-to-validate-model-and-mapping-files"></a><span data-ttu-id="7d788-102">방법: EdmGen.exe를 사용 하 여 모델 및 매핑 파일 유효성을 검사 하려면</span><span class="sxs-lookup"><span data-stu-id="7d788-102">How to: Use EdmGen.exe to Validate Model and Mapping Files</span></span>
<span data-ttu-id="7d788-103">이 항목에서는 사용 하는 [EDM 생성기 (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md) 모델 및 매핑 파일 유효성을 검사 하는 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="7d788-103">This topic shows how to use the [EDM Generator (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md) tool to validate the model and mapping files.</span></span> <span data-ttu-id="7d788-104">자세한 내용은 [엔터티 데이터 모델](../../../../../docs/framework/data/adonet/entity-data-model.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="7d788-104">For more information, see [Entity Data Model](../../../../../docs/framework/data/adonet/entity-data-model.md).</span></span>  
  
### <a name="to-validate-the-school-model-using-edmgenexe"></a><span data-ttu-id="7d788-105">EdmGen.exe를 사용하여 School 모델의 유효성을 검사하려면</span><span class="sxs-lookup"><span data-stu-id="7d788-105">To validate the School model using EdmGen.exe</span></span>  
  
1.  <span data-ttu-id="7d788-106">School 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7d788-106">Create the School database.</span></span> <span data-ttu-id="7d788-107">자세한 내용은 [School 샘플 데이터베이스 만들기](https://msdn.microsoft.com/library/c1bec483-a0ea-4660-aa0b-7b0a8b68fed0)합니다.</span><span class="sxs-lookup"><span data-stu-id="7d788-107">For more information, see [Creating the School Sample Database](https://msdn.microsoft.com/library/c1bec483-a0ea-4660-aa0b-7b0a8b68fed0).</span></span>  
  
2.  <span data-ttu-id="7d788-108">School 모델을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7d788-108">Generate the School model.</span></span> <span data-ttu-id="7d788-109">자세한 내용은 [방법: EdmGen.exe를 사용 하 여 모델 및 매핑 파일 생성](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="7d788-109">For more information, see [How to: Use EdmGen.exe to Generate the Model and Mapping Files](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span></span>  
  
3.  <span data-ttu-id="7d788-110">명령 프롬프트에서 줄 바꿈 없이 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7d788-110">At the command prompt, execute the following command without line breaks:</span></span>  
  
    ```console
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:ValidateArtifacts /inssdl:.\School.ssdl /inmsl:.\School.msl /incsdl:.\School.csdl  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="7d788-111">참고자료</span><span class="sxs-lookup"><span data-stu-id="7d788-111">See also</span></span>
- [<span data-ttu-id="7d788-112">방법: Entity Framework 프로젝트 수동 구성</span><span class="sxs-lookup"><span data-stu-id="7d788-112">How to: Manually Configure an Entity Framework Project</span></span>](https://msdn.microsoft.com/library/73f6ae1d-b3b2-4577-aebd-ad5a75954e9e)
- [<span data-ttu-id="7d788-113">ADO.NET 엔터티 데이터 모델 도구</span><span class="sxs-lookup"><span data-stu-id="7d788-113">ADO.NET Entity Data Model  Tools</span></span>](https://msdn.microsoft.com/library/91076853-0881-421b-837a-f582f36be527)
- [<span data-ttu-id="7d788-114">방법: 쿼리 성능을 개선 하는 뷰를 미리 생성</span><span class="sxs-lookup"><span data-stu-id="7d788-114">How to: Pre-Generate Views to Improve Query Performance</span></span>](https://msdn.microsoft.com/library/b18a9d16-e10b-4043-ba91-b632f85a2579)
- [<span data-ttu-id="7d788-115">방법: EdmGen.exe를 사용 하 여 개체 계층 코드 생성</span><span class="sxs-lookup"><span data-stu-id="7d788-115">How to: Use EdmGen.exe to Generate Object-Layer Code</span></span>](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-object-layer-code.md)
