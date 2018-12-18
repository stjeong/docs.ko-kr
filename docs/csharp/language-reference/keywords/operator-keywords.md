---
title: 연산자 키워드 - C# 참조
ms.custom: seodec18
ms.date: 12/10/2018
helpviewer_keywords:
- keywords [C#], operators
- operators [C#], keywords
ms.assetid: f745c81f-f8d8-4673-86a1-0f3a85cc63c3
ms.openlocfilehash: e03e1c930b452cf5e4f2c4bb1d06d5363f20c991
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243611"
---
# <a name="operator-keywords-c-reference"></a><span data-ttu-id="11f32-102">연산자 키워드(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="11f32-102">Operator Keywords (C# Reference)</span></span>

<span data-ttu-id="11f32-103">개체 생성, 개체의 런타임 형식 확인, 형식의 크기 가져오기 등의 기타 작업을 수행하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-103">Used to perform miscellaneous actions such as creating objects, checking the run-time type of an object, obtaining the size of a type, and other actions.</span></span> <span data-ttu-id="11f32-104">이 섹션에서는 다음과 같은 키워드를 소개합니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-104">This section introduces the following keywords:</span></span>

- <span data-ttu-id="11f32-105">[as](as.md) 개체를 호환되는 형식으로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-105">[as](as.md) Converts an object to a compatible type.</span></span>

- <span data-ttu-id="11f32-106">[await](await.md) 대기 작업이 완료될 때까지 [비동기](async.md) 메서드를 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-106">[await](await.md) Suspends an [async](async.md) method until an awaited task is completed.</span></span>

- <span data-ttu-id="11f32-107">[is](is.md) 개체의 런타임 형식을 확인하거나 (C# 7.0부터는) 패턴에 대해 식을 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-107">[is](is.md) Checks the run-time type of an object, or (starting with C# 7.0) tests an expression against a pattern.</span></span>

- [<span data-ttu-id="11f32-108">new</span><span class="sxs-lookup"><span data-stu-id="11f32-108">new</span></span>](new.md)

  - <span data-ttu-id="11f32-109">[new 연산자](new-operator.md) 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-109">[new Operator](new-operator.md) Creates objects.</span></span>

  - <span data-ttu-id="11f32-110">[new 한정자](new-modifier.md) 상속된 멤버를 숨깁니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-110">[new Modifier](new-modifier.md) Hides an inherited member.</span></span>

  - <span data-ttu-id="11f32-111">[new 제약 조건](new-constraint.md) 형식 매개 변수를 한정합니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-111">[new Constraint](new-constraint.md) Qualifies a type parameter.</span></span>

- <span data-ttu-id="11f32-112">[nameof](nameof.md) 변수, 형식 또는 멤버의 단순(정규화되지 않은) 문자열 이름을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-112">[nameof](nameof.md) Obtains the simple (unqualified) string name of a variable, type, or member.</span></span>

- <span data-ttu-id="11f32-113">[sizeof](sizeof.md) 관리되지 않는 형식의 크기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-113">[sizeof](sizeof.md) Obtains the size of an unmanaged type.</span></span>  

- <span data-ttu-id="11f32-114">[typeof](typeof.md) 형식에 대한 <xref:System.Type?displayProperty=nameWithType> 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-114">[typeof](typeof.md) Obtains the <xref:System.Type?displayProperty=nameWithType> object for a type.</span></span>  

- [<span data-ttu-id="11f32-115">true</span><span class="sxs-lookup"><span data-stu-id="11f32-115">true</span></span>](true.md)  

  - <span data-ttu-id="11f32-116">[true 연산자](true-false-operators.md) [부울](bool.md) 값을 반환하여 `true` 피연산자가 확실히 true임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-116">[true Operator](true-false-operators.md) Returns the [bool](bool.md) value `true` to indicate that the operand is definitely true.</span></span>

  - <span data-ttu-id="11f32-117">[true 리터럴](true-literal.md) [부울](bool.md) 값 `true`를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-117">[true Literal](true-literal.md) Represents the [bool](bool.md) value `true`.</span></span>

- [<span data-ttu-id="11f32-118">false</span><span class="sxs-lookup"><span data-stu-id="11f32-118">false</span></span>](false.md)  

  - <span data-ttu-id="11f32-119">[false 연산자](true-false-operators.md) [부울](bool.md) 값을 반환하여 `true` 피연산자가 확실히 false임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-119">[false Operator](true-false-operators.md) Returns the [bool](bool.md) value `true` to indicate that the operand is definitely false.</span></span>

  - <span data-ttu-id="11f32-120">[false 리터럴](false-literal.md) [부울](bool.md) 값 `false`를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-120">[false Literal](false-literal.md) Represents the [bool](bool.md) value `false`.</span></span>

- <span data-ttu-id="11f32-121">[stackalloc](stackalloc.md) 스택의 메모리 블록을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-121">[stackalloc](stackalloc.md) Allocates a block of memory on the stack.</span></span>  

<span data-ttu-id="11f32-122">연산자 및 문으로 사용할 수 있는 다음 키워드는 [문](statement-keywords.md) 섹션에서 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-122">The following keywords, which can be used as operators and as statements, are covered in the [Statements](statement-keywords.md) section:</span></span>

- <span data-ttu-id="11f32-123">[checked](checked.md) checked 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-123">[checked](checked.md) Specifies checked context.</span></span>  

- <span data-ttu-id="11f32-124">[unchecked](unchecked.md) unchecked 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11f32-124">[unchecked](unchecked.md) Specifies unchecked context.</span></span>  

## <a name="see-also"></a><span data-ttu-id="11f32-125">참고 항목</span><span class="sxs-lookup"><span data-stu-id="11f32-125">See also</span></span>

- [<span data-ttu-id="11f32-126">C# 참조</span><span class="sxs-lookup"><span data-stu-id="11f32-126">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="11f32-127">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="11f32-127">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="11f32-128">C# 키워드</span><span class="sxs-lookup"><span data-stu-id="11f32-128">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="11f32-129">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="11f32-129">C# Operators</span></span>](../operators/index.md)
