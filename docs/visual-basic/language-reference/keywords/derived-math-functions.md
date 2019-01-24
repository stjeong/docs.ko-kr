---
title: 파생된 수학 함수(Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- arithmetic operations, derived math functions
- cosecant function
- arcsecant function
- arccotangent function
- functions [Visual Basic], derived math functions
- inverse functions
- math functions, derived
- derived math functions
- cotangent function
- angles
- secant function
- trigonometric functions
- logarithms
- arccosecant function
- hyperbolic functions
- arcsine function
- degrees
- arccosine function
ms.assetid: 63e449d8-9444-44fb-8db1-6d9cf346e2aa
ms.openlocfilehash: 1273871faf65afdd1a894c03f13a2c93507c1b13
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54505863"
---
# <a name="derived-math-functions-visual-basic"></a><span data-ttu-id="15285-102">파생된 수학 함수(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="15285-102">Derived Math Functions (Visual Basic)</span></span>
<span data-ttu-id="15285-103">다음 표에서 기본 수학 함수의에서 파생 될 수 있는 비 내장 수치 연산 함수는 <xref:System.Math?displayProperty=nameWithType> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="15285-103">The following table shows non-intrinsic math functions that can be derived from the intrinsic math functions of the <xref:System.Math?displayProperty=nameWithType> object.</span></span> <span data-ttu-id="15285-104">기본 수학 함수를 추가 하 여 액세스할 수 있습니다 `Imports System.Math` 을 파일이 나 프로젝트입니다.</span><span class="sxs-lookup"><span data-stu-id="15285-104">You can access the intrinsic math functions by adding `Imports System.Math` to your file or project.</span></span>  
  
|<span data-ttu-id="15285-105">기능</span><span class="sxs-lookup"><span data-stu-id="15285-105">Function</span></span>|<span data-ttu-id="15285-106">해당 파생된 항목</span><span class="sxs-lookup"><span data-stu-id="15285-106">Derived equivalents</span></span>|  
|--------------|-------------------------|  
|<span data-ttu-id="15285-107">시 컨 트 (Sec(x))</span><span class="sxs-lookup"><span data-stu-id="15285-107">Secant (Sec(x))</span></span>|<span data-ttu-id="15285-108">1 / Cos(x)</span><span class="sxs-lookup"><span data-stu-id="15285-108">1 / Cos(x)</span></span>|  
|<span data-ttu-id="15285-109">코시 컨 트 (Csc(x))</span><span class="sxs-lookup"><span data-stu-id="15285-109">Cosecant (Csc(x))</span></span>|<span data-ttu-id="15285-110">1 / Sin(x)</span><span class="sxs-lookup"><span data-stu-id="15285-110">1 / Sin(x)</span></span>|  
|<span data-ttu-id="15285-111">코탄젠트 (Ctan(x))</span><span class="sxs-lookup"><span data-stu-id="15285-111">Cotangent (Ctan(x))</span></span>|<span data-ttu-id="15285-112">1 / Tan(x)</span><span class="sxs-lookup"><span data-stu-id="15285-112">1 / Tan(x)</span></span>|  
|<span data-ttu-id="15285-113">역 사인 (Asin(x))</span><span class="sxs-lookup"><span data-stu-id="15285-113">Inverse sine (Asin(x))</span></span>|<span data-ttu-id="15285-114">Atan(x / Sqrt(-x \* x + 1))</span><span class="sxs-lookup"><span data-stu-id="15285-114">Atan(x / Sqrt(-x \* x + 1))</span></span>|  
|<span data-ttu-id="15285-115">역 코사인 (Acos(x))</span><span class="sxs-lookup"><span data-stu-id="15285-115">Inverse cosine (Acos(x))</span></span>|<span data-ttu-id="15285-116">Atan(-x / Sqrt(-x \* x + 1)) + 2 \* Atan(1)</span><span class="sxs-lookup"><span data-stu-id="15285-116">Atan(-x / Sqrt(-x \* x + 1)) + 2 \* Atan(1)</span></span>|  
|<span data-ttu-id="15285-117">역 시 컨 트 (Asec(x))</span><span class="sxs-lookup"><span data-stu-id="15285-117">Inverse secant (Asec(x))</span></span>|<span data-ttu-id="15285-118">2 \* Atan(1) – Atan(Sign(x) / Sqrt(x \* x – 1))</span><span class="sxs-lookup"><span data-stu-id="15285-118">2 \* Atan(1) – Atan(Sign(x) / Sqrt(x \* x – 1))</span></span>|  
|<span data-ttu-id="15285-119">역 코시 컨 트 (Acsc(x))</span><span class="sxs-lookup"><span data-stu-id="15285-119">Inverse cosecant (Acsc(x))</span></span>|<span data-ttu-id="15285-120">Atan(Sign(x) / Sqrt(x \* x – 1))</span><span class="sxs-lookup"><span data-stu-id="15285-120">Atan(Sign(x) / Sqrt(x \* x – 1))</span></span>|  
|<span data-ttu-id="15285-121">역 코탄젠트 (Acot(x))</span><span class="sxs-lookup"><span data-stu-id="15285-121">Inverse cotangent (Acot(x))</span></span>|<span data-ttu-id="15285-122">2 \* Atan(1) - Atan(x)</span><span class="sxs-lookup"><span data-stu-id="15285-122">2 \* Atan(1) - Atan(x)</span></span>|  
|<span data-ttu-id="15285-123">쌍 곡 사인 (Sinh(x))</span><span class="sxs-lookup"><span data-stu-id="15285-123">Hyperbolic sine (Sinh(x))</span></span>|<span data-ttu-id="15285-124">(Exp(x) – Exp(-x)) / 2</span><span class="sxs-lookup"><span data-stu-id="15285-124">(Exp(x) – Exp(-x)) / 2</span></span>|  
|<span data-ttu-id="15285-125">쌍 곡 코사인 (Cosh(x))</span><span class="sxs-lookup"><span data-stu-id="15285-125">Hyperbolic cosine (Cosh(x))</span></span>|<span data-ttu-id="15285-126">(Exp(x) + Exp(-x)) / 2</span><span class="sxs-lookup"><span data-stu-id="15285-126">(Exp(x) + Exp(-x)) / 2</span></span>|  
|<span data-ttu-id="15285-127">Hyperbolic tangent (Tanh(x))</span><span class="sxs-lookup"><span data-stu-id="15285-127">Hyperbolic tangent (Tanh(x))</span></span>|<span data-ttu-id="15285-128">(Exp(x) – Exp(-x)) / (Exp(x) + Exp(-x))</span><span class="sxs-lookup"><span data-stu-id="15285-128">(Exp(x) – Exp(-x)) / (Exp(x) + Exp(-x))</span></span>|  
|<span data-ttu-id="15285-129">쌍 곡 시 컨 트 (Sech(x))</span><span class="sxs-lookup"><span data-stu-id="15285-129">Hyperbolic secant (Sech(x))</span></span>|<span data-ttu-id="15285-130">2 / (Exp(x) + Exp(-x))</span><span class="sxs-lookup"><span data-stu-id="15285-130">2 / (Exp(x) + Exp(-x))</span></span>|  
|<span data-ttu-id="15285-131">Hyperbolic cosecant (Csch(x))</span><span class="sxs-lookup"><span data-stu-id="15285-131">Hyperbolic cosecant (Csch(x))</span></span>|<span data-ttu-id="15285-132">2 / (Exp(x) – Exp(-x))</span><span class="sxs-lookup"><span data-stu-id="15285-132">2 / (Exp(x) – Exp(-x))</span></span>|  
|<span data-ttu-id="15285-133">Hyperbolic cotangent (Coth(x))</span><span class="sxs-lookup"><span data-stu-id="15285-133">Hyperbolic cotangent (Coth(x))</span></span>|<span data-ttu-id="15285-134">(Exp(x) + Exp(-x)) / (Exp(x) – Exp(-x))</span><span class="sxs-lookup"><span data-stu-id="15285-134">(Exp(x) + Exp(-x)) / (Exp(x) – Exp(-x))</span></span>|  
|<span data-ttu-id="15285-135">역 쌍 곡 사인 (Asinh(x))</span><span class="sxs-lookup"><span data-stu-id="15285-135">Inverse hyperbolic sine (Asinh(x))</span></span>|<span data-ttu-id="15285-136">Log(x + Sqrt(x \* x + 1))</span><span class="sxs-lookup"><span data-stu-id="15285-136">Log(x + Sqrt(x \* x + 1))</span></span>|  
|<span data-ttu-id="15285-137">역 쌍 곡 코사인 (Acosh(x))</span><span class="sxs-lookup"><span data-stu-id="15285-137">Inverse hyperbolic cosine (Acosh(x))</span></span>|<span data-ttu-id="15285-138">Log(x + Sqrt(x \* x – 1))</span><span class="sxs-lookup"><span data-stu-id="15285-138">Log(x + Sqrt(x \* x – 1))</span></span>|  
|<span data-ttu-id="15285-139">역 쌍 곡 탄젠트 (Atanh(x))</span><span class="sxs-lookup"><span data-stu-id="15285-139">Inverse hyperbolic tangent (Atanh(x))</span></span>|<span data-ttu-id="15285-140">Log((1 + x) / (1 – x)) / 2</span><span class="sxs-lookup"><span data-stu-id="15285-140">Log((1 + x) / (1 – x)) / 2</span></span>|  
|<span data-ttu-id="15285-141">역 쌍 곡 시 컨 트 (AsecH(x))</span><span class="sxs-lookup"><span data-stu-id="15285-141">Inverse hyperbolic secant (AsecH(x))</span></span>|<span data-ttu-id="15285-142">Log((Sqrt(-x \* x + 1) + 1) / x)</span><span class="sxs-lookup"><span data-stu-id="15285-142">Log((Sqrt(-x \* x + 1) + 1) / x)</span></span>|  
|<span data-ttu-id="15285-143">역 쌍 곡 코시 컨 트 (Acsch(x))</span><span class="sxs-lookup"><span data-stu-id="15285-143">Inverse hyperbolic cosecant (Acsch(x))</span></span>|<span data-ttu-id="15285-144">Log((Sign(x) \* Sqrt(x \* x + 1) + 1) / x)</span><span class="sxs-lookup"><span data-stu-id="15285-144">Log((Sign(x) \* Sqrt(x \* x + 1) + 1) / x)</span></span>|  
|<span data-ttu-id="15285-145">역 쌍 곡 코탄젠트 (Acoth(x))</span><span class="sxs-lookup"><span data-stu-id="15285-145">Inverse hyperbolic cotangent (Acoth(x))</span></span>|<span data-ttu-id="15285-146">로그 ((x + 1) / (x-1)) / 2</span><span class="sxs-lookup"><span data-stu-id="15285-146">Log((x + 1) / (x – 1)) / 2</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="15285-147">참고자료</span><span class="sxs-lookup"><span data-stu-id="15285-147">See also</span></span>
- [<span data-ttu-id="15285-148">수학 함수</span><span class="sxs-lookup"><span data-stu-id="15285-148">Math Functions</span></span>](../../../visual-basic/language-reference/functions/math-functions.md)
