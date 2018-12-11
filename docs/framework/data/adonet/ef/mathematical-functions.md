---
title: 수학 함수
ms.date: 03/30/2017
ms.assetid: b040c7cb-156d-40f2-9152-61065b18148c
ms.openlocfilehash: 63f83532c399f77e268913da3198327345b9c2ee
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53143677"
---
# <a name="mathematical-functions"></a><span data-ttu-id="5f531-102">수학 함수</span><span class="sxs-lookup"><span data-stu-id="5f531-102">Mathematical Functions</span></span>

<span data-ttu-id="5f531-103">.NET Framework Data Provider for SQL Server(SqlClient)에서는 인수로 제공된 입력 값에 대해 계산을 수행한 다음 숫자 값으로 된 결과를 반환하는 수치 연산 함수를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-103">The .NET Framework Data Provider for SQL Server (SqlClient) provides math functions that perform calculations on input values that are provided as arguments, and return a numeric value result.</span></span> <span data-ttu-id="5f531-104">이 함수는 SqlClient를 사용할 때 사용 가능한 SqlServer 네임스페이스에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-104">These functions are in the SqlServer namespace, which is available when you use SqlClient.</span></span> <span data-ttu-id="5f531-105">공급자의 네임스페이스 속성이 있으면 특정 구문(예: 형식 및 함수)에 대해 이 공급자가 사용하는 접두사를 Entity Framework에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-105">A provider's namespace property allows the Entity Framework to discover which prefix is used by this provider for specific constructs, such as types and functions.</span></span> <span data-ttu-id="5f531-106">다음 표에서 SqlClient 수치 함수를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-106">The following table describes the SqlClient math functions.</span></span>  
  
## <a name="absexpression"></a><span data-ttu-id="5f531-107">ABS(expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-107">ABS(expression)</span></span>

<span data-ttu-id="5f531-108">절대 값 함수를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-108">Performs the absolute value function.</span></span>

<span data-ttu-id="5f531-109">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-109">**Arguments**</span></span>

<span data-ttu-id="5f531-110">`expression`: `Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-110">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="5f531-111">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-111">**Return Value**</span></span>

<span data-ttu-id="5f531-112">지정한 식의 절대 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-112">The absolute value of the specified expression.</span></span>

<span data-ttu-id="5f531-113">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-113">**Example**</span></span>

`SqlServer.ABS(-2)`

## <a name="acosexpression"></a><span data-ttu-id="5f531-114">ACOS(expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-114">ACOS(expression)</span></span>

<span data-ttu-id="5f531-115">지정한 식의 아크코사인 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-115">Returns the arccosine value of the specified expression.</span></span>

<span data-ttu-id="5f531-116">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-116">**Arguments**</span></span>

<span data-ttu-id="5f531-117">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-117">`expression`: A `Double`.</span></span>

<span data-ttu-id="5f531-118">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-118">**Return Value**</span></span>

<span data-ttu-id="5f531-119">`Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-119">A `Double`.</span></span>

<span data-ttu-id="5f531-120">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-120">**Example**</span></span>

`SqlServer.ACOS(.9)`

## <a name="asinexpression"></a><span data-ttu-id="5f531-121">ASIN(expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-121">ASIN(expression)</span></span>

<span data-ttu-id="5f531-122">지정한 식의 아크사인 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-122">Returns the arcsine value of the specified expression.</span></span>

<span data-ttu-id="5f531-123">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-123">**Arguments**</span></span>

<span data-ttu-id="5f531-124">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-124">`expression`: A `Double`.</span></span>

<span data-ttu-id="5f531-125">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-125">**Return Value**</span></span>

<span data-ttu-id="5f531-126">`Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-126">A `Double`.</span></span>

<span data-ttu-id="5f531-127">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-127">**Example**</span></span>

`SqlServer.ASIN(.9)`

## <a name="atanexpression"></a><span data-ttu-id="5f531-128">ATAN(expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-128">ATAN(expression)</span></span>

<span data-ttu-id="5f531-129">지정한 숫자 식의 아크탄젠트 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-129">Returns the arctangent value of the specified numeric expression.</span></span>

<span data-ttu-id="5f531-130">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-130">**Arguments**</span></span>

<span data-ttu-id="5f531-131">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-131">`expression`: A `Double`.</span></span>

<span data-ttu-id="5f531-132">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-132">**Return Value**</span></span>

<span data-ttu-id="5f531-133">`Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-133">A `Double`.</span></span>

<span data-ttu-id="5f531-134">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-134">**Example**</span></span>

`SqlServer.ATAN(9)`

## <a name="atn2expression-expression"></a><span data-ttu-id="5f531-135">ATN2(expression, expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-135">ATN2(expression, expression)</span></span>

<span data-ttu-id="5f531-136">탄젠트 값이 지정한 두 숫자 식 사이에 속하는 각도를 라디안으로 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-136">Returns the angle, in radians, whose tangent is between the two specified numeric expressions.</span></span>

<span data-ttu-id="5f531-137">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-137">**Arguments**</span></span>

<span data-ttu-id="5f531-138">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-138">`expression`: A `Double`.</span></span>

<span data-ttu-id="5f531-139">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-139">**Return Value**</span></span>

<span data-ttu-id="5f531-140">`Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-140">A `Double`.</span></span>

<span data-ttu-id="5f531-141">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-141">**Example**</span></span>

`SqlServer.ATN2(9, 8)`
 
## <a name="ceilingexpression"></a><span data-ttu-id="5f531-142">CEILING(expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-142">CEILING(expression)</span></span>

<span data-ttu-id="5f531-143">지정한 식을 해당 식보다 크거나 같은 가장 작은 정수로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-143">Converts the specified expression to the smallest integer that is greater than or equal to it.</span></span>

<span data-ttu-id="5f531-144">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-144">**Arguments**</span></span>

<span data-ttu-id="5f531-145">`expression`: `Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-145">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="5f531-146">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-146">**Return Value**</span></span>

<span data-ttu-id="5f531-147">`Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-147">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="5f531-148">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-148">**Example**</span></span> 

[!code-csharp[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_ceiling)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_ceiling)]

## <a name="cosexpression"></a><span data-ttu-id="5f531-149">COS(expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-149">COS(expression)</span></span>

<span data-ttu-id="5f531-150">라디안으로 지정된 각도의 삼각 코사인을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-150">Calculates the trigonometric cosine of the specified angle in radians.</span></span> 

<span data-ttu-id="5f531-151">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-151">**Arguments**</span></span> 

<span data-ttu-id="5f531-152">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-152">`expression`: A `Double`.</span></span> 

<span data-ttu-id="5f531-153">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-153">**Return Value**</span></span> 

<span data-ttu-id="5f531-154">`Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-154">A `Double`.</span></span> 

<span data-ttu-id="5f531-155">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-155">**Example**</span></span> 

`SqlServer.COS(45)`

## <a name="cotexpression"></a><span data-ttu-id="5f531-156">COT(expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-156">COT(expression)</span></span>

<span data-ttu-id="5f531-157">지정된 각도의 삼각 코탄젠트를 라디안으로 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-157">Calculates the trigonometric cotangent of the specified angle in radians.</span></span> 

<span data-ttu-id="5f531-158">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-158">**Arguments**</span></span> 

<span data-ttu-id="5f531-159">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-159">`expression`: A `Double`.</span></span> 

<span data-ttu-id="5f531-160">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-160">**Return Value**</span></span> 

<span data-ttu-id="5f531-161">`Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-161">A `Double`.</span></span> 

<span data-ttu-id="5f531-162">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-162">**Example**</span></span> 

`SqlServer.COT(60)`
  
## <a name="degreesradians"></a><span data-ttu-id="5f531-163">DEGREES(radians)</span><span class="sxs-lookup"><span data-stu-id="5f531-163">DEGREES(radians)</span></span>

<span data-ttu-id="5f531-164">해당 각도를 도 단위로 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-164">Returns the corresponding angle in degrees.</span></span> 

<span data-ttu-id="5f531-165">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-165">**Arguments**</span></span> 

<span data-ttu-id="5f531-166">`expression`: `Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-166">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="5f531-167">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-167">**Return Value**</span></span> 

<span data-ttu-id="5f531-168">`Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-168">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="5f531-169">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-169">**Example**</span></span> 

`SqlServer.DEGREES(3.1)`

## <a name="expexpression"></a><span data-ttu-id="5f531-170">EXP(expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-170">EXP(expression)</span></span>

<span data-ttu-id="5f531-171">지정한 숫자 식의 지수 값을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-171">Calculates the exponential value of a specified numeric expression.</span></span> 

<span data-ttu-id="5f531-172">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-172">**Arguments**</span></span> 

<span data-ttu-id="5f531-173">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-173">`expression`: A `Double`.</span></span> 

<span data-ttu-id="5f531-174">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-174">**Return Value**</span></span> 

<span data-ttu-id="5f531-175">`Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-175">A `Double`.</span></span> 

<span data-ttu-id="5f531-176">**예제** `SqlServer.EXP(1)`</span><span class="sxs-lookup"><span data-stu-id="5f531-176">**Example** `SqlServer.EXP(1)`</span></span>

## <a name="floorexpression"></a><span data-ttu-id="5f531-177">FLOOR(expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-177">FLOOR(expression)</span></span>

<span data-ttu-id="5f531-178">지정한 식을 해당 식보다 작거나 같은 가장 큰 정수로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-178">Converts the specified expression to the largest integer less than or equal to it.</span></span> 

<span data-ttu-id="5f531-179">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-179">**Arguments**</span></span> 

<span data-ttu-id="5f531-180">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-180">`expression`: A `Double`.</span></span> 

<span data-ttu-id="5f531-181">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-181">**Return Value**</span></span> 

<span data-ttu-id="5f531-182">`Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-182">A `Double`.</span></span> 

<span data-ttu-id="5f531-183">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-183">**Example**</span></span> 

[!code-csharp[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_floor)] 
[!code-sql[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_floor)]

## <a name="logexpression"></a><span data-ttu-id="5f531-184">LOG(expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-184">LOG(expression)</span></span>

<span data-ttu-id="5f531-185">지정한 `float` 식의 자연 로그를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-185">Calculates the natural logarithm of the specified `float` expression.</span></span> 

<span data-ttu-id="5f531-186">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-186">**Arguments**</span></span> 

<span data-ttu-id="5f531-187">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-187">`expression`: A `Double`.</span></span> 

<span data-ttu-id="5f531-188">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-188">**Return Value**</span></span> 

<span data-ttu-id="5f531-189">`Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-189">A `Double`.</span></span> 

<span data-ttu-id="5f531-190">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-190">**Example**</span></span> 

`SqlServer.LOG(100)`

## <a name="log10expression"></a><span data-ttu-id="5f531-191">LOG10(expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-191">LOG10(expression)</span></span>

<span data-ttu-id="5f531-192">지정한 `Double` 식의 상용 로그를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-192">Returns the base-10 logarithm of the specified `Double` expression.</span></span> 

<span data-ttu-id="5f531-193">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-193">**Arguments**</span></span> 

<span data-ttu-id="5f531-194">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-194">`expression`: A `Double`.</span></span> 

<span data-ttu-id="5f531-195">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-195">**Return Value**</span></span> 

<span data-ttu-id="5f531-196">`Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-196">A `Double`.</span></span> 

<span data-ttu-id="5f531-197">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-197">**Example**</span></span> 

`SqlServer.LOG10(100)`

## <a name="pi"></a><span data-ttu-id="5f531-198">PI)</span><span class="sxs-lookup"><span data-stu-id="5f531-198">PI()</span></span>

<span data-ttu-id="5f531-199">파이의 상수 값을 `Double`로 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-199">Returns the constant value of pi as a `Double`.</span></span> 

<span data-ttu-id="5f531-200">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-200">**Return Value**</span></span> 

<span data-ttu-id="5f531-201">`Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-201">A `Double`.</span></span> 

<span data-ttu-id="5f531-202">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-202">**Example**</span></span> 

`SqlServer.PI()`

## <a name="powernumericexpression-powerexpression"></a><span data-ttu-id="5f531-203">POWER (numeric_expression, power_expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-203">POWER(numeric_expression, power_expression)</span></span>

<span data-ttu-id="5f531-204">지정한 숫자 식의 지정된 거듭제곱 값을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-204">Calculates the value of a specified expression to a specified power.</span></span>

<span data-ttu-id="5f531-205">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-205">**Arguments**</span></span> 

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="5f531-206">`Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-206">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>|
|`power_expression`| <span data-ttu-id="5f531-207">`Double`에 대해 계산할 거듭제곱을 나타내는 `numeric_expression`입니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-207">A `Double` that represents the power to which to raise the `numeric_expression`.</span></span>| 

<span data-ttu-id="5f531-208">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-208">**Return Value**</span></span> 

<span data-ttu-id="5f531-209">지정한 `numeric_expression`에 지정한 `power_expression`을 거듭제곱한 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-209">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span> 

<span data-ttu-id="5f531-210">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-210">**Example**</span></span> 

`SqlServer.POWER(2,7)`

## <a name="radiansexpression"></a><span data-ttu-id="5f531-211">RADIANS(expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-211">RADIANS(expression)</span></span>

<span data-ttu-id="5f531-212">각도를 라디안으로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-212">Converts degrees to radians.</span></span> 

<span data-ttu-id="5f531-213">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-213">**Arguments**</span></span> 

<span data-ttu-id="5f531-214">`expression`: `Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-214">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="5f531-215">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-215">**Return Value**</span></span> 

<span data-ttu-id="5f531-216">`Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-216">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="5f531-217">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-217">**Example**</span></span> 

`SqlServer.RADIANS(360.0)`

## <a name="randseed"></a><span data-ttu-id="5f531-218">RAND([seed])</span><span class="sxs-lookup"><span data-stu-id="5f531-218">RAND([seed])</span></span>

<span data-ttu-id="5f531-219">0에서 1 사이의 임의 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-219">Returns a random value from 0 through 1.</span></span> 

<span data-ttu-id="5f531-220">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-220">**Arguments**</span></span> 

<span data-ttu-id="5f531-221">시드 값으로는 `Int32`합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-221">The seed value as an `Int32`.</span></span> <span data-ttu-id="5f531-222">시드를 지정하지 않으면 SQL Server 데이터베이스 엔진에서 시드 값을 임의로 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-222">If the seed is not specified, the SQL Server Database Engine assigns a seed value at random.</span></span> <span data-ttu-id="5f531-223">지정된 특정 시드 값에 대해 반환되는 결과는 항상 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-223">For a specified seed value, the result returned is always the same.</span></span>

<span data-ttu-id="5f531-224">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-224">**Return Value**</span></span> 

<span data-ttu-id="5f531-225">0에서 1 사이의 임의 `Double` 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-225">A random `Double` value from 0 through 1.</span></span> 

<span data-ttu-id="5f531-226">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-226">**Example**</span></span> 

`SqlServer.RAND()`
  
## <a name="roundnumericexpression-lengthfunction"></a><span data-ttu-id="5f531-227">ROUND(numeric_expression, length[,function])</span><span class="sxs-lookup"><span data-stu-id="5f531-227">ROUND(numeric_expression, length[,function])</span></span>

<span data-ttu-id="5f531-228">숫자 식을 지정한 길이나 전체 자릿수로 반올림하여 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-228">Returns a numeric expression, rounded to the specified length or precision.</span></span> 

<span data-ttu-id="5f531-229">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-229">**Arguments**</span></span> 

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="5f531-230">`Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-230">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 
|`length`| <span data-ttu-id="5f531-231">`Int32`을 반올림할 전체 자릿수를 나타내는 `numeric_expression`입니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-231">An `Int32` that represents the precision to which `numeric_expression` is to be rounded.</span></span> <span data-ttu-id="5f531-232">`length`가 양수일 경우 `numeric_expression`은 `length`에서 지정한 소수 자릿수로 반올림됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-232">When `length` is a positive number, `numeric_expression` is rounded to the number of decimal positions specified by `length`.</span></span> <span data-ttu-id="5f531-233">`length`가 음수일 경우 `numeric_expression`은 `length`에서 지정한 대로 소수점의 왼쪽에서 반올림됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-233">When `length` is a negative number, `numeric_expression` is rounded on the left side of the decimal point, as specified by `length`.</span></span>|
|`function` | <span data-ttu-id="5f531-234">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-234">Optional.</span></span> <span data-ttu-id="5f531-235">`Int32` 수행할 연산 형식을 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-235">An `Int32` that represents the type of operation to perform.</span></span> <span data-ttu-id="5f531-236">함수를 생략 하거나 값이 0 (기본값) 일 때 `numeric_expression` 반올림 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-236">When function is omitted or has a value of 0 (default), `numeric_expression` is rounded.</span></span> <span data-ttu-id="5f531-237">이외의 값 0을 지정 하면 `numeric_expression` 잘립니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-237">When a value other than 0 is specified, `numeric_expression` is truncated.</span></span> |

<span data-ttu-id="5f531-238">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-238">**Return Value**</span></span> 

<span data-ttu-id="5f531-239">지정한 `numeric_expression`에 지정한 `power_expression`을 거듭제곱한 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-239">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span>

<span data-ttu-id="5f531-240">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-240">**Example**</span></span> 

`SqlServer.ROUND(748.58, -3)`

## <a name="signexpression"></a><span data-ttu-id="5f531-241">SIGN(expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-241">SIGN(expression)</span></span> 

<span data-ttu-id="5f531-242">지정한 식의 양수(+1), 0 또는 음수(-1) 부호를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-242">Returns the positive (+1), zero (0), or negative (-1) sign of the specified expression.</span></span> 

<span data-ttu-id="5f531-243">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-243">**Arguments**</span></span> 

<span data-ttu-id="5f531-244">`expression`: `Int32`, `Int64`, `Double` 또는 `Decimal`</span><span class="sxs-lookup"><span data-stu-id="5f531-244">`expression`: `Int32`, `Int64`, `Double`, or `Decimal`</span></span> 

<span data-ttu-id="5f531-245">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-245">**Return Value**</span></span> 

<span data-ttu-id="5f531-246">`Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-246">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="5f531-247">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-247">**Example**</span></span> 

`SqlServer.SIGN(-10)`

## <a name="sinexpression"></a><span data-ttu-id="5f531-248">SIN(expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-248">SIN(expression)</span></span>

<span data-ttu-id="5f531-249">라디안으로 지정한 각도의 삼각 사인을 계산하여 `Double` 식을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-249">Calculates the trigonometric sine of the specified angle in radians, and returns a `Double` expression.</span></span> 

<span data-ttu-id="5f531-250">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-250">**Arguments**</span></span> 

<span data-ttu-id="5f531-251">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-251">`expression`: A `Double`.</span></span> 

<span data-ttu-id="5f531-252">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-252">**Return Value**</span></span> 

<span data-ttu-id="5f531-253">`Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-253">A `Double`.</span></span> 

<span data-ttu-id="5f531-254">**예제** `SqlServer.SIN(20)`</span><span class="sxs-lookup"><span data-stu-id="5f531-254">**Example** `SqlServer.SIN(20)`</span></span>

## <a name="sqrtexpression"></a><span data-ttu-id="5f531-255">SQRT(expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-255">SQRT(expression)</span></span>

<span data-ttu-id="5f531-256">지정한 식의 제곱근을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-256">Returns the square root of the specified expression.</span></span> 

<span data-ttu-id="5f531-257">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-257">**Arguments**</span></span> 

<span data-ttu-id="5f531-258">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-258">`expression`: A `Double`.</span></span> 

<span data-ttu-id="5f531-259">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-259">**Return Value**</span></span> 

<span data-ttu-id="5f531-260">`Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-260">A `Double`.</span></span> 

<span data-ttu-id="5f531-261">**예제** `SqlServer.SQRT(3600)`</span><span class="sxs-lookup"><span data-stu-id="5f531-261">**Example** `SqlServer.SQRT(3600)`</span></span>

## <a name="squareexpression"></a><span data-ttu-id="5f531-262">SQUARE(expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-262">SQUARE(expression)</span></span>

<span data-ttu-id="5f531-263">지정한 식의 제곱을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-263">Returns the square of the specified expression.</span></span> 

<span data-ttu-id="5f531-264">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-264">**Arguments**</span></span> 

<span data-ttu-id="5f531-265">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-265">`expression`: A `Double`.</span></span> 

<span data-ttu-id="5f531-266">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-266">**Return Value**</span></span> 

<span data-ttu-id="5f531-267">`Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-267">A `Double`.</span></span> 

<span data-ttu-id="5f531-268">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-268">**Example**</span></span> 

`SqlServer.SQUARE(25)`

## <a name="tanexpression"></a><span data-ttu-id="5f531-269">TAN(expression)</span><span class="sxs-lookup"><span data-stu-id="5f531-269">TAN(expression)</span></span>

<span data-ttu-id="5f531-270">지정한 식의 탄젠트를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="5f531-270">Calculates the tangent of a specified expression.</span></span>

<span data-ttu-id="5f531-271">**인수**</span><span class="sxs-lookup"><span data-stu-id="5f531-271">**Arguments**</span></span> 

<span data-ttu-id="5f531-272">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="5f531-272">`expression`: `Double`</span></span> 

<span data-ttu-id="5f531-273">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="5f531-273">**Return Value**</span></span> 

`Double` 

<span data-ttu-id="5f531-274">**예제**</span><span class="sxs-lookup"><span data-stu-id="5f531-274">**Example**</span></span> 

`SqlServer.TAN(45.0)`
  
## <a name="see-also"></a><span data-ttu-id="5f531-275">참고 항목</span><span class="sxs-lookup"><span data-stu-id="5f531-275">See also</span></span>

<span data-ttu-id="5f531-276">SqlClient에서 지원하는 수치 함수에 대한 자세한 내용은 SqlClient 공급자 매니페스트에 지정한 SQL Server 버전의 설명서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5f531-276">For more information about the mathematical functions that SqlClient supports, see the documentation for the SQL Server version that you specified in the SqlClient provider manifest:</span></span>  
  
<span data-ttu-id="5f531-277">**SQL Server 2005:** [수치 연산 함수 (TRANSACT-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms177516(v=sql.90))</span><span class="sxs-lookup"><span data-stu-id="5f531-277">**SQL Server 2005:** [Mathematical Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms177516(v=sql.90))</span></span>  
<span data-ttu-id="5f531-278">**SQL Server 2008:** [수치 연산 함수 (TRANSACT-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2008/ms177516(v=sql.100))</span><span class="sxs-lookup"><span data-stu-id="5f531-278">**SQL Server 2008:** [Mathematical Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2008/ms177516(v=sql.100))</span></span>  
<span data-ttu-id="5f531-279">**SQL Server 2012 이상:** [수치 연산 함수 (TRANSACT-SQL)](/sql/t-sql/functions/mathematical-functions-transact-sql?view=sql-server-2017)</span><span class="sxs-lookup"><span data-stu-id="5f531-279">**SQL Server 2012 and later:** [Mathematical Functions (Transact-SQL)](/sql/t-sql/functions/mathematical-functions-transact-sql?view=sql-server-2017)</span></span>   

 [<span data-ttu-id="5f531-280">Entity Framework용 SqlClient 기능</span><span class="sxs-lookup"><span data-stu-id="5f531-280">SqlClient for Entity Framework Functions</span></span>](sqlclient-for-ef-functions.md)
