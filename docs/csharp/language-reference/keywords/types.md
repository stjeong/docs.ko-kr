---
title: 형식(C# 참조)
ms.date: 07/20/2015
helpviewer_keywords:
- types [C#]
- data types [C#], type system
ms.assetid: 16b984df-f417-4e02-b1e6-4589d4a614ea
ms.openlocfilehash: f5a3ad9fef108c1eec2ba63d68bc5015d2f6c430
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53142959"
---
# <a name="types-c-reference"></a><span data-ttu-id="a5fb8-102">형식(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="a5fb8-102">Types (C# Reference)</span></span>

<span data-ttu-id="a5fb8-103">C# 형식화 시스템에는 다음 범주가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5fb8-103">The C# typing system contains the following categories:</span></span>

- [<span data-ttu-id="a5fb8-104">값 형식</span><span class="sxs-lookup"><span data-stu-id="a5fb8-104">Value types</span></span>](value-types.md)

- [<span data-ttu-id="a5fb8-105">참조 형식</span><span class="sxs-lookup"><span data-stu-id="a5fb8-105">Reference types</span></span>](reference-types.md)

- [<span data-ttu-id="a5fb8-106">포인터 형식</span><span class="sxs-lookup"><span data-stu-id="a5fb8-106">Pointer types</span></span>](../../programming-guide/unsafe-code-pointers/pointer-types.md)

 <span data-ttu-id="a5fb8-107">값 형식인 변수는 데이터를 저장하고, 참조 형식인 변수는 실제 데이터에 대한 참조를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fb8-107">Variables that are value types store data, and those that are reference types store references to the actual data.</span></span> <span data-ttu-id="a5fb8-108">참조 형식 인스턴스를 개체라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fb8-108">Instances of reference types are also referred to as objects.</span></span> <span data-ttu-id="a5fb8-109">포인터 형식은 [안전하지 않은](unsafe.md) 모드에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fb8-109">Pointer types can be used only in [unsafe](unsafe.md) mode.</span></span>

 <span data-ttu-id="a5fb8-110">[boxing 및 unboxing](../../../csharp/programming-guide/types/boxing-and-unboxing.md)을 사용하여 값 형식을 참조 형식으로 변환한 다음, 값 형식으로 다시 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fb8-110">It's possible to convert a value type to a reference type, and back again to a value type, by using [boxing and unboxing](../../../csharp/programming-guide/types/boxing-and-unboxing.md).</span></span> <span data-ttu-id="a5fb8-111">boxed 값 형식을 제외하고 참조 형식을 값 형식으로 변환할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fb8-111">With the exception of a boxed value type, you cannot convert a reference type to a value type.</span></span>

 <span data-ttu-id="a5fb8-112">이 섹션에서는 [void](void.md)도 소개합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fb8-112">This section also introduces [void](void.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a5fb8-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a5fb8-113">See also</span></span>

- [<span data-ttu-id="a5fb8-114">C# 참조</span><span class="sxs-lookup"><span data-stu-id="a5fb8-114">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="a5fb8-115">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="a5fb8-115">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="a5fb8-116">C# 키워드</span><span class="sxs-lookup"><span data-stu-id="a5fb8-116">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="a5fb8-117">형식 참조 테이블</span><span class="sxs-lookup"><span data-stu-id="a5fb8-117">Reference Tables for Types</span></span>](reference-tables-for-types.md)
- [<span data-ttu-id="a5fb8-118">캐스팅 및 형식 변환</span><span class="sxs-lookup"><span data-stu-id="a5fb8-118">Casting and Type Conversions</span></span>](../../programming-guide/types/casting-and-type-conversions.md)
- [<span data-ttu-id="a5fb8-119">유형</span><span class="sxs-lookup"><span data-stu-id="a5fb8-119">Types</span></span>](../../programming-guide/types/index.md)
