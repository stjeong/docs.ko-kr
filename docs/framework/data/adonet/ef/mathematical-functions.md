---
title: 수학 함수
ms.date: 03/30/2017
ms.assetid: b040c7cb-156d-40f2-9152-61065b18148c
ms.openlocfilehash: e6c58d781d7138f8295f2d0a2f0db110ad4b1dd6
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44268976"
---
# <a name="mathematical-functions"></a><span data-ttu-id="6d47d-102">수학 함수</span><span class="sxs-lookup"><span data-stu-id="6d47d-102">Mathematical Functions</span></span>

<span data-ttu-id="6d47d-103">.NET Framework Data Provider for SQL Server(SqlClient)에서는 인수로 제공된 입력 값에 대해 계산을 수행한 다음 숫자 값으로 된 결과를 반환하는 수치 연산 함수를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-103">The .NET Framework Data Provider for SQL Server (SqlClient) provides math functions that perform calculations on input values that are provided as arguments, and return a numeric value result.</span></span> <span data-ttu-id="6d47d-104">이 함수는 SqlClient를 사용할 때 사용 가능한 SqlServer 네임스페이스에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-104">These functions are in the SqlServer namespace, which is available when you use SqlClient.</span></span> <span data-ttu-id="6d47d-105">공급자의 네임스페이스 속성이 있으면 특정 구문(예: 형식 및 함수)에 대해 이 공급자가 사용하는 접두사를 Entity Framework에서 찾을 수 있습니다. 다음 표에서는 SqlClient 수치 함수에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-105">A provider's namespace property allows the Entity Framework to discover which prefix is used by this provider for specific constructs, such as types and functions.The following table describes the SqlClient math functions.</span></span>  
  
## <a name="absexpression"></a><span data-ttu-id="6d47d-106">ABS(expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-106">ABS(expression)</span></span>

<span data-ttu-id="6d47d-107">절대 값 함수를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-107">Performs the absolute value function.</span></span>

<span data-ttu-id="6d47d-108">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-108">**Arguments**</span></span>

<span data-ttu-id="6d47d-109">`expression`: `Int32`, `Int64`, `Double` 또는 `Decimal`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-109">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="6d47d-110">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-110">**Return Value**</span></span>

<span data-ttu-id="6d47d-111">지정한 식의 절대 값입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-111">The absolute value of the specified expression.</span></span>

<span data-ttu-id="6d47d-112">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-112">**Example**</span></span>

`SqlServer.ABS(-2)`

## <a name="acosexpression"></a><span data-ttu-id="6d47d-113">ACOS(expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-113">ACOS(expression)</span></span>

<span data-ttu-id="6d47d-114">지정한 식의 아크코사인 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-114">Returns the arccosine value of the specified expression.</span></span>

<span data-ttu-id="6d47d-115">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-115">**Arguments**</span></span>

<span data-ttu-id="6d47d-116">`expression`: `Double`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-116">`expression`: A `Double`.</span></span>

<span data-ttu-id="6d47d-117">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-117">**Return Value**</span></span>

<span data-ttu-id="6d47d-118">`Double`</span><span class="sxs-lookup"><span data-stu-id="6d47d-118">A `Double`.</span></span>

<span data-ttu-id="6d47d-119">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-119">**Example**</span></span>

`SqlServer.ACOS(.9)`

## <a name="asinexpression"></a><span data-ttu-id="6d47d-120">ASIN(expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-120">ASIN(expression)</span></span>

<span data-ttu-id="6d47d-121">지정한 식의 아크사인 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-121">Returns the arcsine value of the specified expression.</span></span>

<span data-ttu-id="6d47d-122">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-122">**Arguments**</span></span>

<span data-ttu-id="6d47d-123">`expression`: `Double`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-123">`expression`: A `Double`.</span></span>

<span data-ttu-id="6d47d-124">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-124">**Return Value**</span></span>

<span data-ttu-id="6d47d-125">`Double`</span><span class="sxs-lookup"><span data-stu-id="6d47d-125">A `Double`.</span></span>

<span data-ttu-id="6d47d-126">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-126">**Example**</span></span>

`SqlServer.ASIN(.9)`

## <a name="atanexpression"></a><span data-ttu-id="6d47d-127">ATAN(expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-127">ATAN(expression)</span></span>

<span data-ttu-id="6d47d-128">지정한 숫자 식의 아크탄젠트 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-128">Returns the arctangent value of the specified numeric expression.</span></span>

<span data-ttu-id="6d47d-129">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-129">**Arguments**</span></span>

<span data-ttu-id="6d47d-130">`expression`: `Double`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-130">`expression`: A `Double`.</span></span>

<span data-ttu-id="6d47d-131">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-131">**Return Value**</span></span>

<span data-ttu-id="6d47d-132">`Double`</span><span class="sxs-lookup"><span data-stu-id="6d47d-132">A `Double`.</span></span>

<span data-ttu-id="6d47d-133">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-133">**Example**</span></span>

`SqlServer.ATAN(9)`

## <a name="atn2expression-expression"></a><span data-ttu-id="6d47d-134">ATN2(expression, expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-134">ATN2(expression, expression)</span></span>

<span data-ttu-id="6d47d-135">탄젠트 값이 지정한 두 숫자 식 사이에 속하는 각도를 라디안으로 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-135">Returns the angle, in radians, whose tangent is between the two specified numeric expressions.</span></span>

<span data-ttu-id="6d47d-136">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-136">**Arguments**</span></span>

<span data-ttu-id="6d47d-137">`expression`: `Double`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-137">`expression`: A `Double`.</span></span>

<span data-ttu-id="6d47d-138">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-138">**Return Value**</span></span>

<span data-ttu-id="6d47d-139">`Double`</span><span class="sxs-lookup"><span data-stu-id="6d47d-139">A `Double`.</span></span>

<span data-ttu-id="6d47d-140">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-140">**Example**</span></span>

`SqlServer.ATN2(9, 8)`
 
## <a name="ceilingexpression"></a><span data-ttu-id="6d47d-141">CEILING(expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-141">CEILING(expression)</span></span>

<span data-ttu-id="6d47d-142">지정한 식을 해당 식보다 크거나 같은 가장 작은 정수로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-142">Converts the specified expression to the smallest integer that is greater than or equal to it.</span></span>

<span data-ttu-id="6d47d-143">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-143">**Arguments**</span></span>

<span data-ttu-id="6d47d-144">`expression`: `Int32`, `Int64`, `Double` 또는 `Decimal`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-144">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="6d47d-145">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-145">**Return Value**</span></span>

<span data-ttu-id="6d47d-146">`Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-146">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="6d47d-147">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-147">**Example**</span></span> 

[!code-csharp[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_ceiling)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_ceiling)]

## <a name="cosexpression"></a><span data-ttu-id="6d47d-148">COS(expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-148">COS(expression)</span></span>

<span data-ttu-id="6d47d-149">라디안으로 지정된 각도의 삼각 코사인을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-149">Calculates the trigonometric cosine of the specified angle in radians.</span></span> 

<span data-ttu-id="6d47d-150">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-150">**Arguments**</span></span> 

<span data-ttu-id="6d47d-151">`expression`: `Double`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-151">`expression`: A `Double`.</span></span> 

<span data-ttu-id="6d47d-152">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-152">**Return Value**</span></span> 

<span data-ttu-id="6d47d-153">`Double`</span><span class="sxs-lookup"><span data-stu-id="6d47d-153">A `Double`.</span></span> 

<span data-ttu-id="6d47d-154">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-154">**Example**</span></span> 

`SqlServer.COS(45)`

## <a name="cotexpression"></a><span data-ttu-id="6d47d-155">COT(expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-155">COT(expression)</span></span>

<span data-ttu-id="6d47d-156">지정된 각도의 삼각 코탄젠트를 라디안으로 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-156">Calculates the trigonometric cotangent of the specified angle in radians.</span></span> 

<span data-ttu-id="6d47d-157">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-157">**Arguments**</span></span> 

<span data-ttu-id="6d47d-158">`expression`: `Double`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-158">`expression`: A `Double`.</span></span> 

<span data-ttu-id="6d47d-159">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-159">**Return Value**</span></span> 

<span data-ttu-id="6d47d-160">`Double`</span><span class="sxs-lookup"><span data-stu-id="6d47d-160">A `Double`.</span></span> 

<span data-ttu-id="6d47d-161">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-161">**Example**</span></span> 

`SqlServer.COT(60)`
  
## <a name="degreesradians"></a><span data-ttu-id="6d47d-162">DEGREES(radians)</span><span class="sxs-lookup"><span data-stu-id="6d47d-162">DEGREES(radians)</span></span>

<span data-ttu-id="6d47d-163">해당 각도를 도 단위로 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-163">Returns the corresponding angle in degrees.</span></span> 

<span data-ttu-id="6d47d-164">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-164">**Arguments**</span></span> 

<span data-ttu-id="6d47d-165">`expression`: `Int32`, `Int64`, `Double` 또는 `Decimal`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-165">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="6d47d-166">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-166">**Return Value**</span></span> 

<span data-ttu-id="6d47d-167">`Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-167">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="6d47d-168">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-168">**Example**</span></span> 

`SqlServer.DEGREES(3.1)`

## <a name="expexpression"></a><span data-ttu-id="6d47d-169">EXP(expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-169">EXP(expression)</span></span>

<span data-ttu-id="6d47d-170">지정한 숫자 식의 지수 값을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-170">Calculates the exponential value of a specified numeric expression.</span></span> 

<span data-ttu-id="6d47d-171">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-171">**Arguments**</span></span> 

<span data-ttu-id="6d47d-172">`expression`: `Double`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-172">`expression`: A `Double`.</span></span> 

<span data-ttu-id="6d47d-173">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-173">**Return Value**</span></span> 

<span data-ttu-id="6d47d-174">`Double`</span><span class="sxs-lookup"><span data-stu-id="6d47d-174">A `Double`.</span></span> 

<span data-ttu-id="6d47d-175">**예제** `SqlServer.EXP(1)`</span><span class="sxs-lookup"><span data-stu-id="6d47d-175">**Example** `SqlServer.EXP(1)`</span></span>

## <a name="floorexpression"></a><span data-ttu-id="6d47d-176">FLOOR(expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-176">FLOOR(expression)</span></span>

<span data-ttu-id="6d47d-177">지정한 식을 해당 식보다 작거나 같은 가장 큰 정수로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-177">Converts the specified expression to the largest integer less than or equal to it.</span></span> 

<span data-ttu-id="6d47d-178">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-178">**Arguments**</span></span> 

<span data-ttu-id="6d47d-179">`expression`: `Double`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-179">`expression`: A `Double`.</span></span> 

<span data-ttu-id="6d47d-180">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-180">**Return Value**</span></span> 

<span data-ttu-id="6d47d-181">`Double`</span><span class="sxs-lookup"><span data-stu-id="6d47d-181">A `Double`.</span></span> 

<span data-ttu-id="6d47d-182">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-182">**Example**</span></span> 

[!code-csharp[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_floor)] 
[!code-sql[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_floor)]

## <a name="logexpression"></a><span data-ttu-id="6d47d-183">LOG(expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-183">LOG(expression)</span></span>

<span data-ttu-id="6d47d-184">지정한 `float` 식의 자연 로그를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-184">Calculates the natural logarithm of the specified `float` expression.</span></span> 

<span data-ttu-id="6d47d-185">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-185">**Arguments**</span></span> 

<span data-ttu-id="6d47d-186">`expression`: `Double`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-186">`expression`: A `Double`.</span></span> 

<span data-ttu-id="6d47d-187">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-187">**Return Value**</span></span> 

<span data-ttu-id="6d47d-188">`Double`</span><span class="sxs-lookup"><span data-stu-id="6d47d-188">A `Double`.</span></span> 

<span data-ttu-id="6d47d-189">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-189">**Example**</span></span> 

`SqlServer.LOG(100)`

## <a name="log10expression"></a><span data-ttu-id="6d47d-190">LOG10(expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-190">LOG10(expression)</span></span>

<span data-ttu-id="6d47d-191">지정한 `Double` 식의 상용 로그를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-191">Returns the base-10 logarithm of the specified `Double` expression.</span></span> 

<span data-ttu-id="6d47d-192">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-192">**Arguments**</span></span> 

<span data-ttu-id="6d47d-193">`expression`: `Double`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-193">`expression`: A `Double`.</span></span> 

<span data-ttu-id="6d47d-194">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-194">**Return Value**</span></span> 

<span data-ttu-id="6d47d-195">`Double`</span><span class="sxs-lookup"><span data-stu-id="6d47d-195">A `Double`.</span></span> 

<span data-ttu-id="6d47d-196">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-196">**Example**</span></span> 

`SqlServer.LOG10(100)`

## <a name="pi"></a><span data-ttu-id="6d47d-197">PI)</span><span class="sxs-lookup"><span data-stu-id="6d47d-197">PI()</span></span>

<span data-ttu-id="6d47d-198">파이의 상수 값을 `Double`로 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-198">Returns the constant value of pi as a `Double`.</span></span> 

<span data-ttu-id="6d47d-199">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-199">**Return Value**</span></span> 

<span data-ttu-id="6d47d-200">`Double`</span><span class="sxs-lookup"><span data-stu-id="6d47d-200">A `Double`.</span></span> 

<span data-ttu-id="6d47d-201">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-201">**Example**</span></span> 

`SqlServer.PI()`

## <a name="powernumericexpression-powerexpression"></a><span data-ttu-id="6d47d-202">POWER (numeric_expression, power_expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-202">POWER(numeric_expression, power_expression)</span></span>

<span data-ttu-id="6d47d-203">지정한 숫자 식의 지정된 거듭제곱 값을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-203">Calculates the value of a specified expression to a specified power.</span></span>

<span data-ttu-id="6d47d-204">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-204">**Arguments**</span></span> 

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="6d47d-205">`Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-205">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>|
|`power_expression`| <span data-ttu-id="6d47d-206">`Double`에 대해 계산할 거듭제곱을 나타내는 `numeric_expression`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-206">A `Double` that represents the power to which to raise the `numeric_expression`.</span></span>| 

<span data-ttu-id="6d47d-207">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-207">**Return Value**</span></span> 

<span data-ttu-id="6d47d-208">지정한 `numeric_expression`에 지정한 `power_expression`을 거듭제곱한 값입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-208">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span> 

<span data-ttu-id="6d47d-209">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-209">**Example**</span></span> 

`SqlServer.POWER(2,7)`

## <a name="radiansexpression"></a><span data-ttu-id="6d47d-210">RADIANS(expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-210">RADIANS(expression)</span></span>

<span data-ttu-id="6d47d-211">각도를 라디안으로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-211">Converts degrees to radians.</span></span> 

<span data-ttu-id="6d47d-212">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-212">**Arguments**</span></span> 

<span data-ttu-id="6d47d-213">`expression`: `Int32`, `Int64`, `Double` 또는 `Decimal`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-213">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="6d47d-214">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-214">**Return Value**</span></span> 

<span data-ttu-id="6d47d-215">`Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-215">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="6d47d-216">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-216">**Example**</span></span> 

`SqlServer.RADIANS(360.0)`

## <a name="randseed"></a><span data-ttu-id="6d47d-217">RAND([seed])</span><span class="sxs-lookup"><span data-stu-id="6d47d-217">RAND([seed])</span></span>

<span data-ttu-id="6d47d-218">0에서 1 사이의 임의 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-218">Returns a random value from 0 through 1.</span></span> 

<span data-ttu-id="6d47d-219">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-219">**Arguments**</span></span> 

<span data-ttu-id="6d47d-220">시드 값으로는 `Int32`합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-220">The seed value as an `Int32`.</span></span> <span data-ttu-id="6d47d-221">시드를 지정하지 않으면 SQL Server 데이터베이스 엔진에서 시드 값을 임의로 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-221">If the seed is not specified, the SQL Server Database Engine assigns a seed value at random.</span></span> <span data-ttu-id="6d47d-222">지정된 특정 시드 값에 대해 반환되는 결과는 항상 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-222">For a specified seed value, the result returned is always the same.</span></span>

<span data-ttu-id="6d47d-223">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-223">**Return Value**</span></span> 

<span data-ttu-id="6d47d-224">0에서 1 사이의 임의 `Double` 값입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-224">A random `Double` value from 0 through 1.</span></span> 

<span data-ttu-id="6d47d-225">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-225">**Example**</span></span> 

`SqlServer.RAND()`
  
## <a name="roundnumericexpression-lengthfunction"></a><span data-ttu-id="6d47d-226">ROUND(numeric_expression, length[,function])</span><span class="sxs-lookup"><span data-stu-id="6d47d-226">ROUND(numeric_expression, length[,function])</span></span>

<span data-ttu-id="6d47d-227">숫자 식을 지정한 길이나 전체 자릿수로 반올림하여 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-227">Returns a numeric expression, rounded to the specified length or precision.</span></span> 

<span data-ttu-id="6d47d-228">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-228">**Arguments**</span></span> 

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="6d47d-229">`Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-229">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 
|`length`| <span data-ttu-id="6d47d-230">`Int32`을 반올림할 전체 자릿수를 나타내는 `numeric_expression`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-230">An `Int32` that represents the precision to which `numeric_expression` is to be rounded.</span></span> <span data-ttu-id="6d47d-231">`length`가 양수일 경우 `numeric_expression`은 `length`에서 지정한 소수 자릿수로 반올림됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-231">When `length` is a positive number, `numeric_expression` is rounded to the number of decimal positions specified by `length`.</span></span> <span data-ttu-id="6d47d-232">`length`가 음수일 경우 `numeric_expression`은 `length`에서 지정한 대로 소수점의 왼쪽에서 반올림됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-232">When `length` is a negative number, `numeric_expression` is rounded on the left side of the decimal point, as specified by `length`.</span></span>|
|`function` | <span data-ttu-id="6d47d-233">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-233">Optional.</span></span> <span data-ttu-id="6d47d-234">`Int32` 수행할 연산 형식을 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-234">An `Int32` that represents the type of operation to perform.</span></span> <span data-ttu-id="6d47d-235">함수를 생략 하거나 값이 0 (기본값) 일 때 `numeric_expression` 반올림 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-235">When function is omitted or has a value of 0 (default), `numeric_expression` is rounded.</span></span> <span data-ttu-id="6d47d-236">이외의 값 0을 지정 하면 `numeric_expression` 잘립니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-236">When a value other than 0 is specified, `numeric_expression` is truncated.</span></span> |

<span data-ttu-id="6d47d-237">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-237">**Return Value**</span></span> 

<span data-ttu-id="6d47d-238">지정한 `numeric_expression`에 지정한 `power_expression`을 거듭제곱한 값입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-238">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span>

<span data-ttu-id="6d47d-239">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-239">**Example**</span></span> 

`SqlServer.ROUND(748.58, -3)`

## <a name="signexpression"></a><span data-ttu-id="6d47d-240">SIGN(expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-240">SIGN(expression)</span></span> 

<span data-ttu-id="6d47d-241">지정한 식의 양수(+1), 0 또는 음수(-1) 부호를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-241">Returns the positive (+1), zero (0), or negative (-1) sign of the specified expression.</span></span> 

<span data-ttu-id="6d47d-242">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-242">**Arguments**</span></span> 

<span data-ttu-id="6d47d-243">`expression`: `Int32`, `Int64`, `Double` 또는 `Decimal`</span><span class="sxs-lookup"><span data-stu-id="6d47d-243">`expression`: `Int32`, `Int64`, `Double`, or `Decimal`</span></span> 

<span data-ttu-id="6d47d-244">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-244">**Return Value**</span></span> 

<span data-ttu-id="6d47d-245">`Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-245">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="6d47d-246">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-246">**Example**</span></span> 

`SqlServer.SIGN(-10)`

## <a name="sinexpression"></a><span data-ttu-id="6d47d-247">SIN(expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-247">SIN(expression)</span></span>

<span data-ttu-id="6d47d-248">라디안으로 지정한 각도의 삼각 사인을 계산하여 `Double` 식을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-248">Calculates the trigonometric sine of the specified angle in radians, and returns a `Double` expression.</span></span> 

<span data-ttu-id="6d47d-249">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-249">**Arguments**</span></span> 

<span data-ttu-id="6d47d-250">`expression`: `Double`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-250">`expression`: A `Double`.</span></span> 

<span data-ttu-id="6d47d-251">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-251">**Return Value**</span></span> 

<span data-ttu-id="6d47d-252">`Double`</span><span class="sxs-lookup"><span data-stu-id="6d47d-252">A `Double`.</span></span> 

<span data-ttu-id="6d47d-253">**예제** `SqlServer.SIN(20)`</span><span class="sxs-lookup"><span data-stu-id="6d47d-253">**Example** `SqlServer.SIN(20)`</span></span>

## <a name="sqrtexpression"></a><span data-ttu-id="6d47d-254">SQRT(expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-254">SQRT(expression)</span></span>

<span data-ttu-id="6d47d-255">지정한 식의 제곱근을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-255">Returns the square root of the specified expression.</span></span> 

<span data-ttu-id="6d47d-256">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-256">**Arguments**</span></span> 

<span data-ttu-id="6d47d-257">`expression`: `Double`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-257">`expression`: A `Double`.</span></span> 

<span data-ttu-id="6d47d-258">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-258">**Return Value**</span></span> 

<span data-ttu-id="6d47d-259">`Double`</span><span class="sxs-lookup"><span data-stu-id="6d47d-259">A `Double`.</span></span> 

<span data-ttu-id="6d47d-260">**예제** `SqlServer.SQRT(3600)`</span><span class="sxs-lookup"><span data-stu-id="6d47d-260">**Example** `SqlServer.SQRT(3600)`</span></span>

## <a name="squareexpression"></a><span data-ttu-id="6d47d-261">SQUARE(expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-261">SQUARE(expression)</span></span>

<span data-ttu-id="6d47d-262">지정한 식의 제곱을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-262">Returns the square of the specified expression.</span></span> 

<span data-ttu-id="6d47d-263">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-263">**Arguments**</span></span> 

<span data-ttu-id="6d47d-264">`expression`: `Double`입니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-264">`expression`: A `Double`.</span></span> 

<span data-ttu-id="6d47d-265">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-265">**Return Value**</span></span> 

<span data-ttu-id="6d47d-266">`Double`</span><span class="sxs-lookup"><span data-stu-id="6d47d-266">A `Double`.</span></span> 

<span data-ttu-id="6d47d-267">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-267">**Example**</span></span> 

`SqlServer.SQUARE(25)`

## <a name="tanexpression"></a><span data-ttu-id="6d47d-268">TAN(expression)</span><span class="sxs-lookup"><span data-stu-id="6d47d-268">TAN(expression)</span></span>

<span data-ttu-id="6d47d-269">지정한 식의 탄젠트를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="6d47d-269">Calculates the tangent of a specified expression.</span></span>

<span data-ttu-id="6d47d-270">**인수**</span><span class="sxs-lookup"><span data-stu-id="6d47d-270">**Arguments**</span></span> 

<span data-ttu-id="6d47d-271">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="6d47d-271">`expression`: `Double`</span></span> 

<span data-ttu-id="6d47d-272">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="6d47d-272">**Return Value**</span></span> 

`Double` 

<span data-ttu-id="6d47d-273">**예제**</span><span class="sxs-lookup"><span data-stu-id="6d47d-273">**Example**</span></span> 

`SqlServer.TAN(45.0)`
  
## <a name="see-also"></a><span data-ttu-id="6d47d-274">참고자료</span><span class="sxs-lookup"><span data-stu-id="6d47d-274">See also</span></span>

<span data-ttu-id="6d47d-275">SqlClient에서 지원하는 수치 함수에 대한 자세한 내용은 SqlClient 공급자 매니페스트에 지정한 SQL Server 버전의 설명서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6d47d-275">For more information about the mathematical functions that SqlClient supports, see the documentation for the SQL Server version that you specified in the SqlClient provider manifest:</span></span>  
  
<span data-ttu-id="6d47d-276">**SQL Server 2005:** [수치 연산 함수 (TRANSACT-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms177516(v=sql.90))</span><span class="sxs-lookup"><span data-stu-id="6d47d-276">**SQL Server 2005:** [Mathematical Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms177516(v=sql.90))</span></span>  
<span data-ttu-id="6d47d-277">**SQL Server 2008:** [수치 연산 함수 (TRANSACT-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2008/ms177516(v=sql.100))</span><span class="sxs-lookup"><span data-stu-id="6d47d-277">**SQL Server 2008:** [Mathematical Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2008/ms177516(v=sql.100))</span></span>  
<span data-ttu-id="6d47d-278">**SQL Server 2012 이상:** [수치 연산 함수 (TRANSACT-SQL)](/sql/t-sql/functions/mathematical-functions-transact-sql?view=sql-server-2017)</span><span class="sxs-lookup"><span data-stu-id="6d47d-278">**SQL Server 2012 and later:** [Mathematical Functions (Transact-SQL)](/sql/t-sql/functions/mathematical-functions-transact-sql?view=sql-server-2017)</span></span>   

 [<span data-ttu-id="6d47d-279">Entity Framework용 SqlClient 기능</span><span class="sxs-lookup"><span data-stu-id="6d47d-279">SqlClient for Entity Framework Functions</span></span>](sqlclient-for-ef-functions.md)
