---
title: Null 조건부 연산자 (Visual Basic)
ms.date: 10/19/2018
helpviewer_keywords:
- null-conditional operators [Visual Basic]
- ?. operator [Visual Basic]
- ?[] operator [C#]
- ?[] operator [Visual Basic]
ms.openlocfilehash: d30d452a7c140a0c56529386b14ef3a3512df490
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54722155"
---
# <a name="-and--null-conditional-operators-visual-basic"></a><span data-ttu-id="fb4ba-102">?.</span><span class="sxs-lookup"><span data-stu-id="fb4ba-102">?.</span></span> <span data-ttu-id="fb4ba-103">및? null 조건부 연산자 () (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fb4ba-103">and ?() null-conditional operators (Visual Basic)</span></span>

<span data-ttu-id="fb4ba-104">Null에 대 한 왼쪽 피연산자의 값을 테스트 (`Nothing`)는 멤버 액세스를 수행 하기 전에 (`?.`) 또는 인덱스 (`?()`) 작업; 반환 `Nothing` 왼쪽 피연산자가 `Nothing`입니다.</span><span class="sxs-lookup"><span data-stu-id="fb4ba-104">Tests the value of the left-hand operand for null (`Nothing`) before performing a member access (`?.`) or index (`?()`) operation; returns `Nothing` if the left-hand operand evaluates to `Nothing`.</span></span> <span data-ttu-id="fb4ba-105">일반적으로 값 형식을 반환 하는 식, null 조건부 연산자를 반환,는 <xref:System.Nullable%601>합니다.</span><span class="sxs-lookup"><span data-stu-id="fb4ba-105">Note that, in the expressions that would ordinarily return value types, the null-conditional operator returns a <xref:System.Nullable%601>.</span></span>

<span data-ttu-id="fb4ba-106">이러한 연산자는 데이터 구조에서 아래로 내려가는 경우에 특히 null 검사를 처리 하는 작은 코드를 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb4ba-106">These operators help you write less code to handle null checks, especially when descending into data structures.</span></span> <span data-ttu-id="fb4ba-107">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="fb4ba-107">For example:</span></span>

```vb
Dim length As Integer? = customers?.Length  ' Nothing if customers is Nothing  
Dim first As Customer = customers?(0)  ' Nothing if customers is Nothing  
Dim count As Integer? = customers?(0)?.Orders?.Count()  ' Nothing if customers, the first customer, or Orders is Nothing  
```

<span data-ttu-id="fb4ba-108">반면 null 조건부 연산자 없이 이러한 식의 첫 번째에 대 한 대체 코드는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fb4ba-108">For comparison, the alternative code for the first of these expressions without a null-conditional operator is:</span></span>

```vb
Dim length As Integer
If customers IsNot Nothing Then
   length = customers.Length
End If
```

<span data-ttu-id="fb4ba-109">Null 조건부 연산자는 단락 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="fb4ba-109">The null-conditional operators are short-circuiting.</span></span>  <span data-ttu-id="fb4ba-110">조건부 멤버 액세스 및 인덱스 작업의 체인에 하나의 작업 Nothing을 반환 하면 체인 실행의 나머지 부분을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb4ba-110">If one operation in a chain of conditional member access and index operations returns Nothing, the rest of the chain’s execution stops.</span></span>  <span data-ttu-id="fb4ba-111">하는 경우 다음 예제에서는 c (e) 평가 되지 않습니다 `A`, `B`, 또는 `C` Nothing으로 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb4ba-111">In the following example, C(E) isn't evaluated if `A`, `B`, or `C` evaluates to Nothing.</span></span>

```vb
A?.B?.C?(E);
```

<span data-ttu-id="fb4ba-112">Null 조건부 멤버 액세스에 대 한 또 다른 용도 훨씬 더 적은 코드를 사용 하 여 스레드로부터 안전한 방식으로 대리자를 호출 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fb4ba-112">Another use for null-conditional member access is to invoke delegates in a thread-safe way with much less code.</span></span>  <span data-ttu-id="fb4ba-113">이전 방식에서는 다음과 같은 코드가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="fb4ba-113">The old way requires code like the following:</span></span>  

```vb  
Dim handler = AddressOf(Me.PropertyChanged)  
If handler IsNot Nothing  
    Call handler(…)  
```

<span data-ttu-id="fb4ba-114">새로운 방식은 훨씬 더 간단합니다.</span><span class="sxs-lookup"><span data-stu-id="fb4ba-114">The new way is much simpler:</span></span>  

```vb
PropertyChanged?.Invoke(…)
```

<span data-ttu-id="fb4ba-115">새로운 방식은 컴파일러가 `PropertyChanged`를 한 번만 평가하는 코드를 생성하고 결과를 임시 변수에 유지하기 때문에 스레드로부터 안전합니다.</span><span class="sxs-lookup"><span data-stu-id="fb4ba-115">The new way is thread-safe because the compiler generates code to evaluate `PropertyChanged` one time only, keeping the result in a temporary variable.</span></span> <span data-ttu-id="fb4ba-116">null 조건부 대리자 호출 구문 `PropertyChanged?(e)`가 없기 때문에 `Invoke` 메서드를 명시적으로 호출해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb4ba-116">You need to explicitly call the `Invoke` method because there is no null-conditional delegate invocation syntax `PropertyChanged?(e)`.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fb4ba-117">참고자료</span><span class="sxs-lookup"><span data-stu-id="fb4ba-117">See also</span></span>

- [<span data-ttu-id="fb4ba-118">연산자 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fb4ba-118">Operators (Visual Basic)</span></span>](index.md)
- [<span data-ttu-id="fb4ba-119">Visual Basic 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="fb4ba-119">Visual Basic Programming Guide</span></span>](../../../visual-basic/programming-guide/index.md)
- [<span data-ttu-id="fb4ba-120">Visual Basic 언어 참조</span><span class="sxs-lookup"><span data-stu-id="fb4ba-120">Visual Basic Language Reference</span></span>](../../../visual-basic/language-reference/index.md)
