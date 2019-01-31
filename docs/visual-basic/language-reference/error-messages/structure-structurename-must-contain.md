---
title: "'<structurename>' 구조체에는 'Custom'으로 표시되지 않은 적어도 하나의 인스턴스 멤버 변수 또는 이벤트 선언이 있어야 합니다."
ms.date: 07/20/2015
f1_keywords:
- bc30941
- vbc30941
helpviewer_keywords:
- BC30941
ms.assetid: 7054cc1e-bac3-4c3d-82f3-35772bd8dd3b
ms.openlocfilehash: a8a85f4f089de9be6f2ecadac05256b30d3014b0
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55267458"
---
# <a name="structure-structurename-must-contain-at-least-one-instance-member-variable-or-at-least-one-instance-event-declaration-not-marked-custom"></a><span data-ttu-id="ab932-102">구조 '\<structurename >' 하나 이상의 인스턴스 멤버 변수 또는 'Custom' 표시 되지 않은 인스턴스를 하나 이상 이벤트 선언이 있어야</span><span class="sxs-lookup"><span data-stu-id="ab932-102">Structure '\<structurename>' must contain at least one instance member variable or at least one instance event declaration not marked 'Custom'</span></span>
<span data-ttu-id="ab932-103">구조체 정의 비공유 변수 또는 비공유 비 사용자 정의 이벤트 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab932-103">A structure definition does not include any nonshared variables or nonshared noncustom events.</span></span>  
  
 <span data-ttu-id="ab932-104">모든 구조체는 변수 또는 모든 인스턴스에 (비공유) 대신 특정 인스턴스의 전체적으로 적용 되는 이벤트 해야 합니다. ([공유](../../../visual-basic/language-reference/modifiers/shared.md)).</span><span class="sxs-lookup"><span data-stu-id="ab932-104">Every structure must have either a variable or an event that applies to each specific instance (nonshared) instead of to all instances collectively ([Shared](../../../visual-basic/language-reference/modifiers/shared.md)).</span></span> <span data-ttu-id="ab932-105">비공유 상수, 속성 및 절차가 요구이 사항을 충족 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab932-105">Nonshared constants, properties, and procedures do not satisfy this requirement.</span></span> <span data-ttu-id="ab932-106">또한 비공유 변수가 없고 하나의 비공유 이벤트가 없으면 이벤트 일 수 없습니다는 `Custom` 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="ab932-106">In addition, if there are no nonshared variables and only one nonshared event, that event cannot be a `Custom` event.</span></span>  
  
 <span data-ttu-id="ab932-107">**오류 ID:** BC30941</span><span class="sxs-lookup"><span data-stu-id="ab932-107">**Error ID:** BC30941</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="ab932-108">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="ab932-108">To correct this error</span></span>  
  
-   <span data-ttu-id="ab932-109">하나 이상의 변수 또는 없는 이벤트를 정의 `Shared`합니다.</span><span class="sxs-lookup"><span data-stu-id="ab932-109">Define at least one variable or event that is not `Shared`.</span></span> <span data-ttu-id="ab932-110">하나의 이벤트를 정의 하는 경우 사용자와 공유 되지 않는 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab932-110">If you define only one event, it must be noncustom as well as nonshared.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab932-111">참고자료</span><span class="sxs-lookup"><span data-stu-id="ab932-111">See also</span></span>
- [<span data-ttu-id="ab932-112">구조체</span><span class="sxs-lookup"><span data-stu-id="ab932-112">Structures</span></span>](../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="ab932-113">방법: 구조 선언</span><span class="sxs-lookup"><span data-stu-id="ab932-113">How to: Declare a Structure</span></span>](../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
- [<span data-ttu-id="ab932-114">Structure 문</span><span class="sxs-lookup"><span data-stu-id="ab932-114">Structure Statement</span></span>](../../../visual-basic/language-reference/statements/structure-statement.md)
