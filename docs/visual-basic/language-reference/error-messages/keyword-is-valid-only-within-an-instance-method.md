---
title: "'<keyword>'은(는) 인스턴스 메서드 안에서만 사용할 수 있습니다."
ms.date: 07/20/2015
f1_keywords:
- bc30043
- vbc30043
helpviewer_keywords:
- BC30043
ms.assetid: 7973aa82-a681-440c-9bca-242627d7ba86
ms.openlocfilehash: af3bc95e2db88577c7c53e4b58fb60aed8a83453
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55267649"
---
# <a name="keyword-is-valid-only-within-an-instance-method"></a><span data-ttu-id="c8aad-102">'\<키워드 >'는 인스턴스 메서드 내 에서만 유효</span><span class="sxs-lookup"><span data-stu-id="c8aad-102">'\<keyword>' is valid only within an instance method</span></span>
<span data-ttu-id="c8aad-103">합니다 `Me`, `MyClass`, 및 `MyBase` 키워드 특정 클래스 인스턴스를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c8aad-103">The `Me`, `MyClass`, and `MyBase` keywords refer to specific class instances.</span></span> <span data-ttu-id="c8aad-104">공유 내에서 사용할 수 없습니다 `Function` 또는 `Sub` 프로시저입니다.</span><span class="sxs-lookup"><span data-stu-id="c8aad-104">You cannot use them inside a shared `Function` or `Sub` procedure.</span></span>  
  
 <span data-ttu-id="c8aad-105">**오류 ID:** BC30043</span><span class="sxs-lookup"><span data-stu-id="c8aad-105">**Error ID:** BC30043</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="c8aad-106">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="c8aad-106">To correct this error</span></span>  
  
-   <span data-ttu-id="c8aad-107">프로시저에서 키워드를 제거 하거나 제거 합니다 `Shared` 프로시저 선언에서 키워드입니다.</span><span class="sxs-lookup"><span data-stu-id="c8aad-107">Remove the keyword from the procedure, or remove the `Shared` keyword from the procedure declaration.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c8aad-108">참고자료</span><span class="sxs-lookup"><span data-stu-id="c8aad-108">See also</span></span>
- [<span data-ttu-id="c8aad-109">개체 변수 할당</span><span class="sxs-lookup"><span data-stu-id="c8aad-109">Object Variable Assignment</span></span>](../../../visual-basic/programming-guide/language-features/variables/object-variable-assignment.md)
- [<span data-ttu-id="c8aad-110">Me, My, MyBase 및 MyClass</span><span class="sxs-lookup"><span data-stu-id="c8aad-110">Me, My, MyBase, and MyClass</span></span>](../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
- [<span data-ttu-id="c8aad-111">상속 기본 사항</span><span class="sxs-lookup"><span data-stu-id="c8aad-111">Inheritance Basics</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
