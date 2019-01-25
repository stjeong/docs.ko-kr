---
title: 대리자 클래스 &#39; &lt;classname&gt; &#39; Invoke 메서드가 있으므로이 형식의 식은 메서드 호출의 대상일 수 없습니다
ms.date: 07/20/2015
f1_keywords:
- vbc30220
- bc30220
helpviewer_keywords:
- BC30220
ms.assetid: 6be0d61c-f2f9-4f9b-ab90-8871a0d7206d
ms.openlocfilehash: d5421ea05968a221bbbf8f52a575550d1bca3cb2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54653160"
---
# <a name="delegate-class-39ltclassnamegt39-has-no-invoke-method-so-an-expression-of-this-type-cannot-be-the-target-of-a-method-call"></a><span data-ttu-id="446ff-102">대리자 클래스 &#39; &lt;classname&gt; &#39; Invoke 메서드가 있으므로이 형식의 식은 메서드 호출의 대상일 수 없습니다</span><span class="sxs-lookup"><span data-stu-id="446ff-102">Delegate class &#39;&lt;classname&gt;&#39; has no Invoke method, so an expression of this type cannot be the target of a method call</span></span>
<span data-ttu-id="446ff-103">에 대 한 호출 `Invoke` 때문에 실패 했습니다 대리자를 통해 `Invoke` 대리자 클래스에서 구현 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="446ff-103">A call to `Invoke` through a delegate has failed because `Invoke` is not implemented on the delegate class.</span></span>  
  
 <span data-ttu-id="446ff-104">**오류 ID:** BC30220</span><span class="sxs-lookup"><span data-stu-id="446ff-104">**Error ID:** BC30220</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="446ff-105">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="446ff-105">To correct this error</span></span>  
  
1.  <span data-ttu-id="446ff-106">대리자 클래스의 인스턴스를 사용 하 여 만들어졌는지 확인 한 `Dim` 문과 프로시저를 사용 하 여 대리자 인스턴스를 할당할지를 `AddressOf` 연산자.</span><span class="sxs-lookup"><span data-stu-id="446ff-106">Ensure that an instance of the delegate class has been created with a `Dim` statement and that a procedure has been assigned to the delegate instance with the `AddressOf` operator.</span></span>  
  
2.  <span data-ttu-id="446ff-107">대리자 클래스를 구현 하는 코드를 찾아를 구현 합니다는 `Invoke` 프로시저입니다.</span><span class="sxs-lookup"><span data-stu-id="446ff-107">Locate the code that implements the delegate class and make sure it implements the `Invoke` procedure.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="446ff-108">참고자료</span><span class="sxs-lookup"><span data-stu-id="446ff-108">See also</span></span>
- [<span data-ttu-id="446ff-109">대리자</span><span class="sxs-lookup"><span data-stu-id="446ff-109">Delegates</span></span>](../../../visual-basic/programming-guide/language-features/delegates/index.md)
- [<span data-ttu-id="446ff-110">Delegate 문</span><span class="sxs-lookup"><span data-stu-id="446ff-110">Delegate Statement</span></span>](../../../visual-basic/language-reference/statements/delegate-statement.md)
- [<span data-ttu-id="446ff-111">AddressOf 연산자</span><span class="sxs-lookup"><span data-stu-id="446ff-111">AddressOf Operator</span></span>](../../../visual-basic/language-reference/operators/addressof-operator.md)
- [<span data-ttu-id="446ff-112">Dim 문</span><span class="sxs-lookup"><span data-stu-id="446ff-112">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)
