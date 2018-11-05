---
title: as(C# 참조)
ms.date: 10/11/2018
f1_keywords:
- as_CSharpKeyword
- as
helpviewer_keywords:
- type conversion [C#], as keyword
- as keyword [C#]
ms.assetid: a9be126b-cbf4-4990-a70d-d0e1983cad0e
ms.openlocfilehash: ce3163f7d957df96a5c0304adc0b3083d8e20104
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49122727"
---
# <a name="as-c-reference"></a><span data-ttu-id="3658e-102">as(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="3658e-102">as (C# Reference)</span></span>
<span data-ttu-id="3658e-103">`as` 연산자를 사용하여 호환되는 참조 형식 또는 [nullable 형식](../../../csharp/programming-guide/nullable-types/index.md) 간에 특정 형식의 변환을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3658e-103">You can use the `as` operator to perform certain types of conversions between compatible reference types or [nullable types](../../../csharp/programming-guide/nullable-types/index.md).</span></span> <span data-ttu-id="3658e-104">다음 코드는 예제를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3658e-104">The following code shows an example.</span></span>  
  
[!code-csharp[csrefKeywordsOperator#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#1)]

<span data-ttu-id="3658e-105">예제에 나와 있는 대로 `as` 식의 결과를 `null`과 비교하여 변환에 성공했는지 확인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3658e-105">As the example shows, you need to compare the result of the `as` expression with `null` to check if a conversion is successful.</span></span> <span data-ttu-id="3658e-106">C# 7.0부터는 [is](is.md) 식을 사용하여 변환에 성공했는지 테스트하고 변환 성공 시 조건부로 변수를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3658e-106">Beginning with C# 7.0, you can use the [is](is.md) expression both to test that a conversion succeeds and conditionally assign a variable when the conversion succeeds.</span></span> <span data-ttu-id="3658e-107">대부분 시나리오에서는 `as` 연산자를 사용하는 것보다 더 적합합니다.</span><span class="sxs-lookup"><span data-stu-id="3658e-107">In many scenarios, it's more concise than using the `as` operator.</span></span> <span data-ttu-id="3658e-108">자세한 내용은 [`is` 연산자](is.md) 문서의 [형식 패턴](is.md#type) 섹션을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3658e-108">For more information, see the [Type pattern](is.md#type) section of the [`is` operator](is.md) article.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3658e-109">설명</span><span class="sxs-lookup"><span data-stu-id="3658e-109">Remarks</span></span>  
 <span data-ttu-id="3658e-110">`as` 연산자는 캐스트 작업과 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="3658e-110">The `as` operator is like a cast operation.</span></span> <span data-ttu-id="3658e-111">하지만 변환할 수 없는 경우 `as`는 예외를 발생시키지 않고 `null`을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3658e-111">However, if the conversion isn't possible, `as` returns `null` instead of raising an exception.</span></span> <span data-ttu-id="3658e-112">다음 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3658e-112">Consider the following example:</span></span>  
  
```csharp  
expression as type  
```  
  
 <span data-ttu-id="3658e-113">`expression` 변수가 한 번만 계산된다는 점을 제외하고 코드는 다음 식과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3658e-113">The code is equivalent to the following expression except that the `expression` variable is evaluated only one time.</span></span>  
  
```csharp  
expression is type ? (type)expression : (type)null  
```  
  
 <span data-ttu-id="3658e-114">`as` 연산자는 참조 변환, nullable 변환 및 boxing 변환만 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="3658e-114">Note that the `as` operator performs only reference conversions, nullable conversions, and boxing conversions.</span></span> <span data-ttu-id="3658e-115">`as` 연산자는 캐스트 식을 사용하여 수행해야 하는 사용자 정의 변환 등의 기타 변환을 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3658e-115">The `as` operator can't perform other conversions, such as user-defined conversions, which should instead be performed by using cast expressions.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3658e-116">예</span><span class="sxs-lookup"><span data-stu-id="3658e-116">Example</span></span>  

[!code-csharp[csrefKeywordsOperator#2](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#2)]
  
## <a name="c-language-specification"></a><span data-ttu-id="3658e-117">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="3658e-117">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="3658e-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3658e-118">See Also</span></span>  
- [<span data-ttu-id="3658e-119">C# 참조</span><span class="sxs-lookup"><span data-stu-id="3658e-119">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="3658e-120">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="3658e-120">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="3658e-121">C# 키워드</span><span class="sxs-lookup"><span data-stu-id="3658e-121">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="3658e-122">is</span><span class="sxs-lookup"><span data-stu-id="3658e-122">is</span></span>](../../../csharp/language-reference/keywords/is.md)  
- [<span data-ttu-id="3658e-123">?: 연산자</span><span class="sxs-lookup"><span data-stu-id="3658e-123">?: Operator</span></span>](../../../csharp/language-reference/operators/conditional-operator.md)  
- [<span data-ttu-id="3658e-124">연산자 키워드</span><span class="sxs-lookup"><span data-stu-id="3658e-124">Operator Keywords</span></span>](../../../csharp/language-reference/keywords/operator-keywords.md)
