---
title: 비트 연산자(F#)
description: 'F # 프로그래밍 언어에서 사용할 수 있는 비트 연산자에 알아봅니다.'
ms.date: 07/20/2018
ms.openlocfilehash: abd2778eba422b3ce2a3472efd458446854b3d2f
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43559558"
---
# <a name="bitwise-operators"></a><span data-ttu-id="7bc1f-103">비트 연산자</span><span class="sxs-lookup"><span data-stu-id="7bc1f-103">Bitwise Operators</span></span>

<span data-ttu-id="7bc1f-104">이 항목에서는 F # 언어에서 사용할 수 있는 비트 연산자를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-104">This topic describes bitwise operators that are available in the F# language.</span></span>

## <a name="summary-of-bitwise-operators"></a><span data-ttu-id="7bc1f-105">비트 연산자 요약</span><span class="sxs-lookup"><span data-stu-id="7bc1f-105">Summary of Bitwise Operators</span></span>
<span data-ttu-id="7bc1f-106">다음 표에서 F # 언어에서 unboxed 정수 계열 형식에 대 한 지원 되는 비트 연산자를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-106">The following table describes the bitwise operators that are supported for unboxed integral types in the F# language.</span></span>

|<span data-ttu-id="7bc1f-107">연산자</span><span class="sxs-lookup"><span data-stu-id="7bc1f-107">Operator</span></span>|<span data-ttu-id="7bc1f-108">노트</span><span class="sxs-lookup"><span data-stu-id="7bc1f-108">Notes</span></span>|
|--------|-----|
|`&&&`|<span data-ttu-id="7bc1f-109">비트 AND 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-109">Bitwise AND operator.</span></span> <span data-ttu-id="7bc1f-110">결과 비트는 모두 소스 피연산자의 해당 비트가 1 하는 경우에 1 값을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-110">Bits in the result have the value 1 if and only if the corresponding bits in both source operands are 1.</span></span>|
|<code>&#124;&#124;&#124;</code>|<span data-ttu-id="7bc1f-111">비트 OR 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-111">Bitwise OR operator.</span></span> <span data-ttu-id="7bc1f-112">결과 비트의에서 경우 값 1을 가질 원본의 해당 비트의 두 피연산자가 1입니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-112">Bits in the result have the value 1 if either of the corresponding bits in the source operands are 1.</span></span>|
|`^^^`|<span data-ttu-id="7bc1f-113">비트 배타적 OR 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-113">Bitwise exclusive OR operator.</span></span> <span data-ttu-id="7bc1f-114">결과 비트는 소스 피연산자의 비트 같지 않은 값이 있는 경우에 값 1을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-114">Bits in the result have the value 1 if and only if bits in the source operands have unequal values.</span></span>|
|`~~~`|<span data-ttu-id="7bc1f-115">비트 부정 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-115">Bitwise negation operator.</span></span> <span data-ttu-id="7bc1f-116">단항 연산자 이며는 소스 피연산자의 0 비트가 모두 1 비트 변환 되 고 1 비트가 모두 0 비트로 변환할 결과 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-116">This is a unary operator and produces a result in which all 0 bits in the source operand are converted to 1 bits and all 1 bits are converted to 0 bits.</span></span>|
|`<<<`|<span data-ttu-id="7bc1f-117">비트 왼쪽 시프트 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-117">Bitwise left-shift operator.</span></span> <span data-ttu-id="7bc1f-118">Bits 사용 하 여 첫 번째 피연산자는 두 번째 피연산자의 비트 수 만큼 왼쪽 이동 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-118">The result is the first operand with bits shifted left by the number of bits in the second operand.</span></span> <span data-ttu-id="7bc1f-119">가장 중요 하지 않은 위치에 가장 중요 한 위치에서 벗어나 이동한 비트 회전 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-119">Bits shifted off the most significant position are not rotated into the least significant position.</span></span> <span data-ttu-id="7bc1f-120">최하위 비트는 0으로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-120">The least significant bits are padded with zeros.</span></span> <span data-ttu-id="7bc1f-121">두 번째 인수의 형식이 `int32`합니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-121">The type of the second argument is `int32`.</span></span>|
|`>>>`|<span data-ttu-id="7bc1f-122">비트 오른쪽 시프트 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-122">Bitwise right-shift operator.</span></span> <span data-ttu-id="7bc1f-123">결과 두 번째 피연산자의 비트 수 만큼 오른쪽으로 이동 하는 비트를 사용 하 여 첫 번째 피연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-123">The result is the first operand with bits shifted right by the number of bits in the second operand.</span></span> <span data-ttu-id="7bc1f-124">가장 중요 한 위치에 가장 중요 하지 않은 위치에서 벗어나 이동한 비트 회전 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-124">Bits shifted off the least significant position are not rotated into the most significant position.</span></span> <span data-ttu-id="7bc1f-125">부호 없는 형식에 대 한 최상위 비트는 0으로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-125">For unsigned types, the most significant bits are padded with zeros.</span></span> <span data-ttu-id="7bc1f-126">음수 값 부호 있는 형식에 대 한 최상위 비트는 1로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-126">For signed types with negative values, the most significant bits are padded with ones.</span></span> <span data-ttu-id="7bc1f-127">두 번째 인수의 형식이 `int32`합니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-127">The type of the second argument is `int32`.</span></span>|

<span data-ttu-id="7bc1f-128">형식은 비트 연산자를 사용 하 여 사용할 수: `byte`, `sbyte`, `int16`, `uint16`, `int32 (int)`를 `uint32`, `int64`를 `uint64`, `nativeint`, 및 `unativeint`합니다.</span><span class="sxs-lookup"><span data-stu-id="7bc1f-128">The following types can be used with bitwise operators: `byte`, `sbyte`, `int16`, `uint16`, `int32 (int)`, `uint32`, `int64`, `uint64`, `nativeint`, and `unativeint`.</span></span>

## <a name="see-also"></a><span data-ttu-id="7bc1f-129">참고 항목</span><span class="sxs-lookup"><span data-stu-id="7bc1f-129">See Also</span></span>
[<span data-ttu-id="7bc1f-130">기호 및 연산자 참조</span><span class="sxs-lookup"><span data-stu-id="7bc1f-130">Symbol and Operator Reference</span></span>](index.md)

[<span data-ttu-id="7bc1f-131">산술 연산자</span><span class="sxs-lookup"><span data-stu-id="7bc1f-131">Arithmetic Operators</span></span>](arithmetic-operators.md)

[<span data-ttu-id="7bc1f-132">부울 연산자</span><span class="sxs-lookup"><span data-stu-id="7bc1f-132">Boolean Operators</span></span>](boolean-operators.md)

