---
title: Ansi(Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Ansi
helpviewer_keywords:
- Declare statement [Visual Basic], marshaling strings [Visual Basic]
- ANSI, Visual Basic
- ANSI
ms.assetid: 4f1fa6ff-5557-41ab-b6da-90baf4c15917
ms.openlocfilehash: e474bd686cc753a0265df1fc2914a73d1b62f1b5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54737324"
---
# <a name="ansi-visual-basic"></a><span data-ttu-id="5575b-102">Ansi(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="5575b-102">Ansi (Visual Basic)</span></span>
<span data-ttu-id="5575b-103">Visual Basic 선언 되는 외부 프로시저의 이름에 관계 없이 ANSI American National Standards Institute () 값으로 모든 문자열을 마샬링하고 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5575b-103">Specifies that Visual Basic should marshal all strings to American National Standards Institute (ANSI) values regardless of the name of the external procedure being declared.</span></span>  
  
 <span data-ttu-id="5575b-104">프로젝트 외부에서 정의 된 프로시저를 호출할 때 Visual Basic 컴파일러 절차를 올바르게 호출 해야 하는 정보에 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5575b-104">When you call a procedure defined outside your project, the Visual Basic compiler does not have access to the information it needs to call the procedure correctly.</span></span> <span data-ttu-id="5575b-105">문자열 문자 집합 사용 및 프로시저 위치한, 식별 하는 방법이, 호출 시퀀스가 및 반환 형식으로이 정보 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5575b-105">This information includes where the procedure is located, how it is identified, its calling sequence and return type, and the string character set it uses.</span></span> <span data-ttu-id="5575b-106">합니다 [Declare Statement](../../../visual-basic/language-reference/statements/declare-statement.md) 외부 프로시저에 대 한 참조를 만들고이 필요한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5575b-106">The [Declare Statement](../../../visual-basic/language-reference/statements/declare-statement.md) creates a reference to an external procedure and supplies this necessary information.</span></span>  
  
 <span data-ttu-id="5575b-107">`charsetmodifier` 부분을 `Declare` 문은 외부 프로시저를 호출 하는 동안 문자열을 마샬링 한 문자 집합 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5575b-107">The `charsetmodifier` part in the `Declare` statement supplies the character set information for marshaling strings during a call to the external procedure.</span></span> <span data-ttu-id="5575b-108">또한 Visual Basic에서 외부 프로시저 이름에 대 한 외부 파일을 검색 하는 방식을 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5575b-108">It also affects how Visual Basic searches the external file for the external procedure name.</span></span> <span data-ttu-id="5575b-109">`Ansi` 한정자는 Visual Basic에서 모든 문자열을 ANSI 값으로 마샬링하고 검색 하는 동안 이름을 수정 하지 않고 프로시저를 조회 해야 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5575b-109">The `Ansi` modifier specifies that Visual Basic should marshal all strings to ANSI values and should look up the procedure without modifying its name during the search.</span></span>  
  
 <span data-ttu-id="5575b-110">문자 집합 자가 지정 된 경우 `Ansi` 가 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="5575b-110">If no character set modifier is specified, `Ansi` is the default.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5575b-111">설명</span><span class="sxs-lookup"><span data-stu-id="5575b-111">Remarks</span></span>  
 <span data-ttu-id="5575b-112">`Ansi` 한정자는이 컨텍스트에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5575b-112">The `Ansi` modifier can be used in this context:</span></span>  
  
 [<span data-ttu-id="5575b-113">Declare 문</span><span class="sxs-lookup"><span data-stu-id="5575b-113">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
## <a name="smart-device-developer-notes"></a><span data-ttu-id="5575b-114">스마트 디바이스 개발자 노트</span><span class="sxs-lookup"><span data-stu-id="5575b-114">Smart Device Developer Notes</span></span>  
 <span data-ttu-id="5575b-115">이 키워드는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5575b-115">This keyword is not supported.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5575b-116">참고자료</span><span class="sxs-lookup"><span data-stu-id="5575b-116">See also</span></span>
- [<span data-ttu-id="5575b-117">자동</span><span class="sxs-lookup"><span data-stu-id="5575b-117">Auto</span></span>](../../../visual-basic/language-reference/modifiers/auto.md)
- [<span data-ttu-id="5575b-118">유니코드</span><span class="sxs-lookup"><span data-stu-id="5575b-118">Unicode</span></span>](../../../visual-basic/language-reference/modifiers/unicode.md)
- [<span data-ttu-id="5575b-119">키워드</span><span class="sxs-lookup"><span data-stu-id="5575b-119">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
