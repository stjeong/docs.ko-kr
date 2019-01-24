---
title: '&#39;AddressOf&#39; 피연산자에 괄호 없이 메서드 이름 이어야 합니다.'
ms.date: 07/20/2015
f1_keywords:
- vbc30577
- bc30577
helpviewer_keywords:
- BC30577
ms.assetid: c2c55640-5c61-4e66-97a4-4322020c6001
ms.openlocfilehash: 6f9827d885996ffab8bdab91d0f774a57073e4a3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54565152"
---
# <a name="39addressof39-operand-must-be-the-name-of-a-method-without-parentheses"></a><span data-ttu-id="060ed-102">&#39;AddressOf&#39; 피연산자에 괄호 없이 메서드 이름 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="060ed-102">&#39;AddressOf&#39; operand must be the name of a method (without parentheses)</span></span>
<span data-ttu-id="060ed-103">`AddressOf` 연산자는 특정 프로시저를 참조하는 프로시저 대리자 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="060ed-103">The `AddressOf` operator creates a procedure delegate instance that references a specific procedure.</span></span> <span data-ttu-id="060ed-104">구문은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="060ed-104">The syntax is as follows.</span></span>  
  
 <span data-ttu-id="060ed-105">`AddressOf` `procedurename`</span><span class="sxs-lookup"><span data-stu-id="060ed-105">`AddressOf` `procedurename`</span></span>  
  
 <span data-ttu-id="060ed-106">인수 다음에 괄호를 삽입 `AddressOf`에 불필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="060ed-106">You inserted parentheses around the argument following `AddressOf`, where none are needed.</span></span>  
  
 <span data-ttu-id="060ed-107">**오류 ID:** BC30577</span><span class="sxs-lookup"><span data-stu-id="060ed-107">**Error ID:** BC30577</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="060ed-108">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="060ed-108">To correct this error</span></span>  
  
1.  <span data-ttu-id="060ed-109">인수 다음에 괄호를 제거 `AddressOf`합니다.</span><span class="sxs-lookup"><span data-stu-id="060ed-109">Remove the parentheses around the argument following `AddressOf`.</span></span>  
  
2.  <span data-ttu-id="060ed-110">인수는 메서드 이름 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="060ed-110">Make sure the argument is a method name.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="060ed-111">참고자료</span><span class="sxs-lookup"><span data-stu-id="060ed-111">See also</span></span>
- [<span data-ttu-id="060ed-112">AddressOf 연산자</span><span class="sxs-lookup"><span data-stu-id="060ed-112">AddressOf Operator</span></span>](../../../visual-basic/language-reference/operators/addressof-operator.md)
- [<span data-ttu-id="060ed-113">대리자</span><span class="sxs-lookup"><span data-stu-id="060ed-113">Delegates</span></span>](../../../visual-basic/programming-guide/language-features/delegates/index.md)
