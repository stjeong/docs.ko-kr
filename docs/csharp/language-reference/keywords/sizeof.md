---
title: sizeof(C# 참조)
ms.date: 07/20/2015
f1_keywords:
- sizeof_CSharpKeyword
- sizeof
helpviewer_keywords:
- sizeof keyword [C#]
ms.assetid: c548592c-677c-4f40-a4ce-e613f7529141
ms.openlocfilehash: f2507dd8528e2e66016524873ada890227a74ed8
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43517040"
---
# <a name="sizeof-c-reference"></a><span data-ttu-id="fc14d-102">sizeof(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="fc14d-102">sizeof (C# Reference)</span></span>
<span data-ttu-id="fc14d-103">관리되지 않는 형식의 크기(바이트)를 가져오는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc14d-103">Used to obtain the size in bytes for an unmanaged type.</span></span>

<span data-ttu-id="fc14d-104">관리되지 않는 형식은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fc14d-104">Unmanaged types include:</span></span>

-   <span data-ttu-id="fc14d-105">다음 표에서는 간단한 형식을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fc14d-105">The simple types that are listed in the following table:</span></span>
  
   |<span data-ttu-id="fc14d-106">식</span><span class="sxs-lookup"><span data-stu-id="fc14d-106">Expression</span></span>|<span data-ttu-id="fc14d-107">상수 값</span><span class="sxs-lookup"><span data-stu-id="fc14d-107">Constant value</span></span>|  
   |----------------|--------------------|  
   |`sizeof(sbyte)`|<span data-ttu-id="fc14d-108">1</span><span class="sxs-lookup"><span data-stu-id="fc14d-108">1</span></span>|  
   |`sizeof(byte)`|<span data-ttu-id="fc14d-109">1</span><span class="sxs-lookup"><span data-stu-id="fc14d-109">1</span></span>|  
   |`sizeof(short)`|<span data-ttu-id="fc14d-110">2</span><span class="sxs-lookup"><span data-stu-id="fc14d-110">2</span></span>|  
   |`sizeof(ushort)`|<span data-ttu-id="fc14d-111">2</span><span class="sxs-lookup"><span data-stu-id="fc14d-111">2</span></span>|  
   |`sizeof(int)`|<span data-ttu-id="fc14d-112">4</span><span class="sxs-lookup"><span data-stu-id="fc14d-112">4</span></span>|  
   |`sizeof(uint)`|<span data-ttu-id="fc14d-113">4</span><span class="sxs-lookup"><span data-stu-id="fc14d-113">4</span></span>|  
   |`sizeof(long)`|<span data-ttu-id="fc14d-114">8</span><span class="sxs-lookup"><span data-stu-id="fc14d-114">8</span></span>|  
   |`sizeof(ulong)`|<span data-ttu-id="fc14d-115">8</span><span class="sxs-lookup"><span data-stu-id="fc14d-115">8</span></span>|  
   |`sizeof(char)`|<span data-ttu-id="fc14d-116">2(유니코드)</span><span class="sxs-lookup"><span data-stu-id="fc14d-116">2 (Unicode)</span></span>|  
   |`sizeof(float)`|<span data-ttu-id="fc14d-117">4</span><span class="sxs-lookup"><span data-stu-id="fc14d-117">4</span></span>|  
   |`sizeof(double)`|<span data-ttu-id="fc14d-118">8</span><span class="sxs-lookup"><span data-stu-id="fc14d-118">8</span></span>|  
   |`sizeof(decimal)`|<span data-ttu-id="fc14d-119">16</span><span class="sxs-lookup"><span data-stu-id="fc14d-119">16</span></span>|  
   |`sizeof(bool)`|<span data-ttu-id="fc14d-120">1</span><span class="sxs-lookup"><span data-stu-id="fc14d-120">1</span></span>| 
  
-   <span data-ttu-id="fc14d-121">열거형 형식.</span><span class="sxs-lookup"><span data-stu-id="fc14d-121">Enum types.</span></span>
  
-   <span data-ttu-id="fc14d-122">포인터 형식.</span><span class="sxs-lookup"><span data-stu-id="fc14d-122">Pointer types.</span></span>
  
-   <span data-ttu-id="fc14d-123">참조 형식 또는 구성된 형식인 모든 인스턴스 필드 또는 자동 구현 인스턴스 속성을 포함하지 않는 사용자 정의 구조체입니다.</span><span class="sxs-lookup"><span data-stu-id="fc14d-123">User-defined structs that do not contain any instance fields or auto-implemented instance properties that are reference types or constructed types.</span></span>
  
 <span data-ttu-id="fc14d-124">다음 예제에서는 `int`의 크기를 검색하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fc14d-124">The following example shows how to retrieve the size of an `int`:</span></span>  
  
```csharp  
// Constant value 4:  
int intSize = sizeof(int);   
```  
  
## <a name="remarks"></a><span data-ttu-id="fc14d-125">설명</span><span class="sxs-lookup"><span data-stu-id="fc14d-125">Remarks</span></span>  
 <span data-ttu-id="fc14d-126">C# 버전 2.0부터 단순 형식 또는 열거형 형식에 `sizeof`를 적용하면 [안전하지 않은](unsafe.md) 컨텍스트에서 코드를 더 이상 컴파일할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fc14d-126">Starting with version 2.0 of C#, applying `sizeof` to simple or enum types no longer requires that code be compiled in an [unsafe](unsafe.md) context.</span></span>
  
 <span data-ttu-id="fc14d-127">`sizeof` 연산자를 오버로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fc14d-127">The `sizeof` operator cannot be overloaded.</span></span> <span data-ttu-id="fc14d-128">`sizeof` 연산자에서 반환되는 값은 `int` 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="fc14d-128">The values returned by the `sizeof` operator are of type `int`.</span></span> <span data-ttu-id="fc14d-129">이전 표에서는 특정 단순 형식이 피연산자로 포함된 `sizeof` 식을 대체하는 상수 값을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fc14d-129">The previous table shows the constant values that are substituted for `sizeof` expressions that have certain simple types as operands.</span></span>  
    
 <span data-ttu-id="fc14d-130">구조체를 비롯한 다른 모든 형식의 경우 `sizeof` 연산자는 안전하지 않은 코드 블록에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc14d-130">For all other types, including structs, the `sizeof` operator can be used only in unsafe code blocks.</span></span> <span data-ttu-id="fc14d-131"><xref:System.Runtime.InteropServices.Marshal.SizeOf%2A?displayProperty=nameWithType> 메서드를 사용할 수 있지만 이 메서드에서 반환된 값이 `sizeof`에서 반환된 값과 항상 같지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc14d-131">Although you can use the <xref:System.Runtime.InteropServices.Marshal.SizeOf%2A?displayProperty=nameWithType> method, the value returned by this method is not always the same as the value returned by `sizeof`.</span></span> <span data-ttu-id="fc14d-132"><xref:System.Runtime.InteropServices.Marshal.SizeOf%2A?displayProperty=nameWithType>는 형식이 마샬링된 후의 크기를 반환하는 반면, `sizeof`는 안쪽 여백을 포함하여 공용 언어 런타임에 의해 할당된 크기를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fc14d-132"><xref:System.Runtime.InteropServices.Marshal.SizeOf%2A?displayProperty=nameWithType> returns the size after the type has been marshaled, whereas `sizeof` returns the size as it has been allocated by the common language runtime, including any padding.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fc14d-133">예</span><span class="sxs-lookup"><span data-stu-id="fc14d-133">Example</span></span>  
 [!code-csharp[csrefKeywordsOperator#11](../../../csharp/language-reference/keywords/codesnippet/CSharp/sizeof_1.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="fc14d-134">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="fc14d-134">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="fc14d-135">참고 항목</span><span class="sxs-lookup"><span data-stu-id="fc14d-135">See Also</span></span>

- [<span data-ttu-id="fc14d-136">C# 참조</span><span class="sxs-lookup"><span data-stu-id="fc14d-136">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="fc14d-137">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="fc14d-137">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="fc14d-138">C# 키워드</span><span class="sxs-lookup"><span data-stu-id="fc14d-138">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="fc14d-139">연산자 키워드</span><span class="sxs-lookup"><span data-stu-id="fc14d-139">Operator Keywords</span></span>](../../../csharp/language-reference/keywords/operator-keywords.md)  
- [<span data-ttu-id="fc14d-140">enum</span><span class="sxs-lookup"><span data-stu-id="fc14d-140">enum</span></span>](../../../csharp/language-reference/keywords/enum.md)  
- [<span data-ttu-id="fc14d-141">안전하지 않은 코드 및 포인터</span><span class="sxs-lookup"><span data-stu-id="fc14d-141">Unsafe Code and Pointers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/index.md)  
- [<span data-ttu-id="fc14d-142">구조체</span><span class="sxs-lookup"><span data-stu-id="fc14d-142">Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/structs.md)  
- [<span data-ttu-id="fc14d-143">상수</span><span class="sxs-lookup"><span data-stu-id="fc14d-143">Constants</span></span>](../../../csharp/programming-guide/classes-and-structs/constants.md)
