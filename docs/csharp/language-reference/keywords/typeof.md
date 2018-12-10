---
title: typeof(C# 참조)
ms.date: 07/20/2015
f1_keywords:
- typeof
- typeof_CSharpKeyword
helpviewer_keywords:
- typeof keyword [C#]
ms.assetid: 0c08d880-515e-46bb-8cd2-48b8dd62c08d
ms.openlocfilehash: 039294d17d25d1d8775e7f92f46f5f57f2ac3212
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53146682"
---
# <a name="typeof-c-reference"></a><span data-ttu-id="5a60f-102">typeof(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="5a60f-102">typeof (C# Reference)</span></span>

<span data-ttu-id="5a60f-103">형식의 `System.Type` 개체를 가져오는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a60f-103">Used to obtain the `System.Type` object for a type.</span></span> <span data-ttu-id="5a60f-104">`typeof` 식의 형식은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5a60f-104">A `typeof` expression takes the following form:</span></span>

```csharp
System.Type type = typeof(int);
```

## <a name="remarks"></a><span data-ttu-id="5a60f-105">설명</span><span class="sxs-lookup"><span data-stu-id="5a60f-105">Remarks</span></span>

<span data-ttu-id="5a60f-106">식의 런타임 형식을 가져오려면 다음 예제와 같이 .NET Framework 메서드 <xref:System.Object.GetType%2A>을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a60f-106">To obtain the run-time type of an expression, you can use the .NET Framework method <xref:System.Object.GetType%2A>, as in the following example:</span></span>

```csharp
int i = 0;
System.Type type = i.GetType();
```

<span data-ttu-id="5a60f-107">`typeof` 연산자를 오버로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5a60f-107">The `typeof` operator cannot be overloaded.</span></span>

<span data-ttu-id="5a60f-108">열린 제네릭 형식에서 `typeof` 연산자를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a60f-108">The `typeof` operator can also be used on open generic types.</span></span> <span data-ttu-id="5a60f-109">둘 이상의 형식 매개 변수가 있는 형식의 사양에 적절한 개수의 쉼표가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a60f-109">Types with more than one type parameter must have the appropriate number of commas in the specification.</span></span> <span data-ttu-id="5a60f-110">다음 예제에서는 메서드의 반환 형식이 제네릭 <xref:System.Collections.Generic.IEnumerable%601>인지 여부를 확인하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5a60f-110">The following example shows how to determine whether the return type of a method is a generic <xref:System.Collections.Generic.IEnumerable%601>.</span></span> <span data-ttu-id="5a60f-111">반환 형식이 <xref:System.Collections.Generic.IEnumerable%601> 제네릭 형식이 아닌 경우 <xref:System.Type.GetInterface%2A?displayProperty=nameWithType>은 `null`을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5a60f-111"><xref:System.Type.GetInterface%2A?displayProperty=nameWithType> will return `null` if the return type is not an <xref:System.Collections.Generic.IEnumerable%601> generic type.</span></span>

[!code-csharp[typeof_3.cs](~/samples/snippets/csharp/keywords/typeof/typeof_3.cs)]

## <a name="example"></a><span data-ttu-id="5a60f-112">예제</span><span class="sxs-lookup"><span data-stu-id="5a60f-112">Example</span></span>

[!code-csharp[csrefKeywordsOperator#12](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#12)] 

## <a name="example"></a><span data-ttu-id="5a60f-113">예제</span><span class="sxs-lookup"><span data-stu-id="5a60f-113">Example</span></span>

<span data-ttu-id="5a60f-114">이 샘플에서는 <xref:System.Object.GetType%2A> 메서드를 사용하여 숫자 계산의 결과를 포함하는 데 사용되는 형식을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a60f-114">This sample uses the <xref:System.Object.GetType%2A> method to determine the type that is used to contain the result of a numeric calculation.</span></span> <span data-ttu-id="5a60f-115">이 형식은 결과 숫자의 저장소 요구 사항에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="5a60f-115">This depends on the storage requirements of the resulting number.</span></span>

[!code-csharp[csrefKeywordsOperator#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#13)]

## <a name="c-language-specification"></a><span data-ttu-id="5a60f-116">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="5a60f-116">C# language specification</span></span>

<span data-ttu-id="5a60f-117">자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [typeof 연산자](~/_csharplang/spec/expressions.md#the-typeof-operator)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5a60f-117">For more information, see [The typeof operator](~/_csharplang/spec/expressions.md#the-typeof-operator) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="5a60f-118">C# 언어 사양은 C# 구문 및 사용법에 대한 신뢰할 수 있는 소스입니다.</span><span class="sxs-lookup"><span data-stu-id="5a60f-118">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a60f-119">참고 항목</span><span class="sxs-lookup"><span data-stu-id="5a60f-119">See also</span></span>

- <xref:System.Type?displayProperty=nameWithType>
- [<span data-ttu-id="5a60f-120">C# 참조</span><span class="sxs-lookup"><span data-stu-id="5a60f-120">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="5a60f-121">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="5a60f-121">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="5a60f-122">C# 키워드</span><span class="sxs-lookup"><span data-stu-id="5a60f-122">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)
- [<span data-ttu-id="5a60f-123">is</span><span class="sxs-lookup"><span data-stu-id="5a60f-123">is</span></span>](../../../csharp/language-reference/keywords/is.md)
- [<span data-ttu-id="5a60f-124">연산자 키워드</span><span class="sxs-lookup"><span data-stu-id="5a60f-124">Operator Keywords</span></span>](../../../csharp/language-reference/keywords/operator-keywords.md)