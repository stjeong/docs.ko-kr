---
title: '?: 연산자(C# 참조)'
ms.date: 07/20/2015
f1_keywords:
- ?:_CSharpKeyword
- ?_CSharpKeyword
- :_CSharpKeyword
helpviewer_keywords:
- '?: operator [C#]'
- conditional operator (?:) [C#]
ms.assetid: e83a17f1-7500-48ba-8bee-2fbc4c847af4
ms.openlocfilehash: 3e45ff6eaaefa5829c3ed9415abe1a12b7a1d069
ms.sourcegitcommit: 4bca8f7e172fd019ef437a4803bf5895c6bc4781
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/03/2018
ms.locfileid: "50980624"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="d5191-102">?: 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="d5191-102">?: Operator (C# Reference)</span></span>

<span data-ttu-id="d5191-103">일반적으로 3개로 구성된 조건 연산자로 알려진 조건 연산자(`?:`)는 부울 식의 값에 따라 두 값 중 하나를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-103">The conditional operator (`?:`), commonly known as the ternary conditional operator, returns one of two values depending on the value of a Boolean expression.</span></span> <span data-ttu-id="d5191-104">다음은 조건 연산자의 구문입니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-104">Following is the syntax for the conditional operator.</span></span>  

```csharp
condition ? first_expression : second_expression;  
```

<span data-ttu-id="d5191-105">C# 7.2부터 `first_expression` 및 `second_expression`은 내 [`ref`식](https://github.com/dotnet/csharplang/blob/master/proposals/csharp-7.2/conditional-ref.md)이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-105">Beginning with C# 7.2, the `first_expression` and `second_expression` my be [`ref` expressions](https://github.com/dotnet/csharplang/blob/master/proposals/csharp-7.2/conditional-ref.md):</span></span>

```csharp
ref condition ? ref first_expression : ref second_expression;  
```

<span data-ttu-id="d5191-106">결과는 `ref` 또는 `ref readonly` 변수나 모두 한정자가 없는 변수에 할당될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-106">The result may be assigned to a `ref` or `ref readonly` variable, or to a variable with neither modifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5191-107">설명</span><span class="sxs-lookup"><span data-stu-id="d5191-107">Remarks</span></span>

<span data-ttu-id="d5191-108">`condition`은 `true` 또는 `false`이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-108">The `condition` must evaluate to `true` or `false`.</span></span> <span data-ttu-id="d5191-109">`condition`이 `true`인 경우 `first_expression`이 평가되고 결과가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-109">If `condition` is `true`, `first_expression` is evaluated and becomes the result.</span></span> <span data-ttu-id="d5191-110">`condition`이 `false`인 경우 `second_expression`이 평가되고 결과가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-110">If `condition` is `false`, `second_expression` is evaluated and becomes the result.</span></span> <span data-ttu-id="d5191-111">두 식 중 하나만 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-111">Only one of the two expressions is evaluated.</span></span> <span data-ttu-id="d5191-112">다음 항목은 유효하므로 결과가 `ref`인 식에 특히 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-112">This is particularly important for expressions where the result is a `ref`, as the following is valid:</span></span>

```csharp
ref (storage != null) ? ref storage[3] : ref defaultValue;
```

<span data-ttu-id="d5191-113">`storage`가 null일 때 `storage`에 대한 참조가 평가되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-113">The reference to `storage` is not evaluated when `storage` is null.</span></span>

<span data-ttu-id="d5191-114">결과가 값이면 `first_expression` 및 `second_expression`의 형식이 동일해야 하거나 한 형식에서 다른 형식으로 암시적으로 변환이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-114">When the result is a value, the type of `first_expression` and `second_expression` must be the same, or there must be an implicit conversion from one type to the other.</span></span> <span data-ttu-id="d5191-115">결과가 `ref`이면 `first_expression` 및 `second_expression`의 형식이 동일해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-115">When the result is a `ref`, the type of `first_expression` and `second_expression` must be the same.</span></span>

<span data-ttu-id="d5191-116">조건 연산자를 사용하면 `if-else` 구성이 필요할 수 있는 계산을 더 간결하게 표현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-116">You can express calculations that might otherwise require an `if-else` construction more concisely by using the conditional operator.</span></span> <span data-ttu-id="d5191-117">예를 들어, 다음 코드는 처음에 `if` 문을 사용한 다음 조건부 연산자를 사용하여 정수를 양 또는 음으로 분류합니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-117">For example, the following code uses first an `if` statement and then a conditional operator to classify an integer as positive or negative.</span></span>

```csharp
int input = Convert.ToInt32(Console.ReadLine());  
string classify;  
  
// if-else construction.  
if (input > 0)  
    classify = "positive";  
else  
    classify = "negative";  
  
// ?: conditional operator.  
classify = (input > 0) ? "positive" : "negative";  
```

<span data-ttu-id="d5191-118">조건 연산자에는 오른쪽 결합성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-118">The conditional operator is right-associative.</span></span> <span data-ttu-id="d5191-119">`a ? b : c ? d : e` 식은 `a ? b : (c ? d : e)`가 아닌 `(a ? b : c) ? d : e`로 평가됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-119">The expression `a ? b : c ? d : e` is evaluated as `a ? b : (c ? d : e)`, not as `(a ? b : c) ? d : e`.</span></span>  
  
<span data-ttu-id="d5191-120">조건 연산자는 오버로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-120">The conditional operator cannot be overloaded.</span></span>
  
## <a name="example"></a><span data-ttu-id="d5191-121">예</span><span class="sxs-lookup"><span data-stu-id="d5191-121">Example</span></span>

<span data-ttu-id="d5191-122">다음 예제에서는 해당 결과가 값인 조건 연산자를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-122">The following example shows the conditional operator whose result is a value:</span></span>

[!code-csharp[csRefOperators?:](~/samples/snippets/csharp/language-reference/operators/ConditionalExamples.cs#ConditionalValue)]

<span data-ttu-id="d5191-123">다음 대안은 결과가 참조인 조건 연산자를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d5191-123">The following alternative shows the conditional operator where the result is a reference:</span></span>

[!code-csharp[csRefOperatorsRef?:](~/samples/snippets/csharp/language-reference/operators/ConditionalExamples.cs#ConditionalRef)]

## <a name="see-also"></a><span data-ttu-id="d5191-124">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d5191-124">See Also</span></span>

- [<span data-ttu-id="d5191-125">C# 참조</span><span class="sxs-lookup"><span data-stu-id="d5191-125">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="d5191-126">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="d5191-126">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="d5191-127">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="d5191-127">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
- [<span data-ttu-id="d5191-128">if-else</span><span class="sxs-lookup"><span data-stu-id="d5191-128">if-else</span></span>](../../../csharp/language-reference/keywords/if-else.md)  
- <span data-ttu-id="d5191-129">[?. 및 ?[] 연산자](../../../csharp/language-reference/operators/null-conditional-operators.md)</span><span class="sxs-lookup"><span data-stu-id="d5191-129">[?. and ?[] Operators](../../../csharp/language-reference/operators/null-conditional-operators.md)</span></span>  
- [<span data-ttu-id="d5191-130">?? 연산자</span><span class="sxs-lookup"><span data-stu-id="d5191-130">?? Operator</span></span>](../../../csharp/language-reference/operators/null-coalescing-operator.md)
