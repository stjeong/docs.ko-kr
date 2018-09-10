---
title: 형식(C# 참조)
ms.date: 07/20/2015
helpviewer_keywords:
- types [C#]
- data types [C#], type system
ms.assetid: 16b984df-f417-4e02-b1e6-4589d4a614ea
ms.openlocfilehash: c5c29f5d9a1a4e25e2d5f8816a0df31fa9a91fb1
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43506323"
---
# <a name="types-c-reference"></a><span data-ttu-id="954eb-102">형식(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="954eb-102">Types (C# Reference)</span></span>
<span data-ttu-id="954eb-103">C# 형식화 시스템에는 다음 범주가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="954eb-103">The C# typing system contains the following categories:</span></span>  
  
-   [<span data-ttu-id="954eb-104">값 형식</span><span class="sxs-lookup"><span data-stu-id="954eb-104">Value types</span></span>](../../../csharp/language-reference/keywords/value-types.md)  
  
-   [<span data-ttu-id="954eb-105">참조 형식</span><span class="sxs-lookup"><span data-stu-id="954eb-105">Reference types</span></span>](../../../csharp/language-reference/keywords/reference-types.md)  
  
-   [<span data-ttu-id="954eb-106">포인터 형식</span><span class="sxs-lookup"><span data-stu-id="954eb-106">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)  
  
 <span data-ttu-id="954eb-107">값 형식인 변수는 데이터를 저장하고, 참조 형식인 변수는 실제 데이터에 대한 참조를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="954eb-107">Variables that are value types store data, and those that are reference types store references to the actual data.</span></span> <span data-ttu-id="954eb-108">참조 형식을 개체라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="954eb-108">Reference types are also referred to as objects.</span></span> <span data-ttu-id="954eb-109">포인터 형식은 [안전하지 않은](../../../csharp/language-reference/keywords/unsafe.md) 모드에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="954eb-109">Pointer types can be used only in [unsafe](../../../csharp/language-reference/keywords/unsafe.md) mode.</span></span>  
  
 <span data-ttu-id="954eb-110">[boxing 및 unboxing](../../../csharp/programming-guide/types/boxing-and-unboxing.md)을 사용하여 값 형식을 참조 형식으로 변환한 다음 값 형식으로 다시 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="954eb-110">It is possible to convert a value type to a reference type, and back again to a value type, by using [boxing and unboxing](../../../csharp/programming-guide/types/boxing-and-unboxing.md).</span></span> <span data-ttu-id="954eb-111">boxed 값 형식을 제외하고 참조 형식을 값 형식으로 변환할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="954eb-111">With the exception of a boxed value type, you cannot convert a reference type to a value type.</span></span>  
  
 <span data-ttu-id="954eb-112">이 섹션에서는 [void](../../../csharp/language-reference/keywords/void.md)도 소개합니다.</span><span class="sxs-lookup"><span data-stu-id="954eb-112">This section also introduces [void](../../../csharp/language-reference/keywords/void.md).</span></span>  
  
 <span data-ttu-id="954eb-113">값 형식은 nullable이기도 하므로, 값이 아닌 추가 상태를 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="954eb-113">Value types are also nullable, which means they can store an additional non-value state.</span></span> <span data-ttu-id="954eb-114">자세한 내용은 [Null 허용 형식](../../../csharp/programming-guide/nullable-types/index.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="954eb-114">For more information, see [Nullable Types](../../../csharp/programming-guide/nullable-types/index.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="954eb-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="954eb-115">See Also</span></span>

- [<span data-ttu-id="954eb-116">C# 참조</span><span class="sxs-lookup"><span data-stu-id="954eb-116">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="954eb-117">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="954eb-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="954eb-118">C# 키워드</span><span class="sxs-lookup"><span data-stu-id="954eb-118">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="954eb-119">형식 참조 테이블</span><span class="sxs-lookup"><span data-stu-id="954eb-119">Reference Tables for Types</span></span>](../../../csharp/language-reference/keywords/reference-tables-for-types.md)  
- [<span data-ttu-id="954eb-120">캐스팅 및 형식 변환</span><span class="sxs-lookup"><span data-stu-id="954eb-120">Casting and Type Conversions</span></span>](../../../csharp/programming-guide/types/casting-and-type-conversions.md)  
- [<span data-ttu-id="954eb-121">유형</span><span class="sxs-lookup"><span data-stu-id="954eb-121">Types</span></span>](../../../csharp/programming-guide/types/index.md)
