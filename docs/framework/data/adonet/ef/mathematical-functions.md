---
title: 수학 함수
ms.date: 03/30/2017
ms.assetid: b040c7cb-156d-40f2-9152-61065b18148c
ms.openlocfilehash: b6f248382f069df59a55e85e9a764b0df700fb26
ms.sourcegitcommit: 01ea420eaa4bf76d5fc47673294c8881379b3369
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/06/2019
ms.locfileid: "55759381"
---
# <a name="mathematical-functions"></a><span data-ttu-id="81d99-102">수학 함수</span><span class="sxs-lookup"><span data-stu-id="81d99-102">Mathematical Functions</span></span>

<span data-ttu-id="81d99-103">.NET Framework Data Provider for SQL Server(SqlClient)에서는 인수로 제공된 입력 값에 대해 계산을 수행한 다음 숫자 값으로 된 결과를 반환하는 수치 연산 함수를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-103">The .NET Framework Data Provider for SQL Server (SqlClient) provides math functions that perform calculations on input values that are provided as arguments, and return a numeric value result.</span></span> <span data-ttu-id="81d99-104">이 함수는 SqlClient를 사용할 때 사용 가능한 SqlServer 네임스페이스에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-104">These functions are in the SqlServer namespace, which is available when you use SqlClient.</span></span> <span data-ttu-id="81d99-105">공급자의 네임스페이스 속성이 있으면 특정 구문(예: 형식 및 함수)에 대해 이 공급자가 사용하는 접두사를 Entity Framework에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-105">A provider's namespace property allows the Entity Framework to discover which prefix is used by this provider for specific constructs, such as types and functions.</span></span> <span data-ttu-id="81d99-106">다음 표에서 SqlClient 수치 함수를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-106">The following table describes the SqlClient math functions.</span></span>  
  
## <a name="absexpression"></a><span data-ttu-id="81d99-107">ABS(expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-107">ABS(expression)</span></span>

<span data-ttu-id="81d99-108">절대 값 함수를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-108">Performs the absolute value function.</span></span>

<span data-ttu-id="81d99-109">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-109">**Arguments**</span></span>

<span data-ttu-id="81d99-110">`expression`: `Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-110">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="81d99-111">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-111">**Return Value**</span></span>

<span data-ttu-id="81d99-112">지정한 식의 절대 값입니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-112">The absolute value of the specified expression.</span></span>

<span data-ttu-id="81d99-113">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-113">**Example**</span></span>

`SqlServer.ABS(-2)`

## <a name="acosexpression"></a><span data-ttu-id="81d99-114">ACOS(expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-114">ACOS(expression)</span></span>

<span data-ttu-id="81d99-115">지정한 식의 아크코사인 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-115">Returns the arccosine value of the specified expression.</span></span>

<span data-ttu-id="81d99-116">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-116">**Arguments**</span></span>

<span data-ttu-id="81d99-117">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-117">`expression`: A `Double`.</span></span>

<span data-ttu-id="81d99-118">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-118">**Return Value**</span></span>

<span data-ttu-id="81d99-119">`Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-119">A `Double`.</span></span>

<span data-ttu-id="81d99-120">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-120">**Example**</span></span>

`SqlServer.ACOS(.9)`

## <a name="asinexpression"></a><span data-ttu-id="81d99-121">ASIN(expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-121">ASIN(expression)</span></span>

<span data-ttu-id="81d99-122">지정한 식의 아크사인 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-122">Returns the arcsine value of the specified expression.</span></span>

<span data-ttu-id="81d99-123">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-123">**Arguments**</span></span>

<span data-ttu-id="81d99-124">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-124">`expression`: A `Double`.</span></span>

<span data-ttu-id="81d99-125">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-125">**Return Value**</span></span>

<span data-ttu-id="81d99-126">`Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-126">A `Double`.</span></span>

<span data-ttu-id="81d99-127">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-127">**Example**</span></span>

`SqlServer.ASIN(.9)`

## <a name="atanexpression"></a><span data-ttu-id="81d99-128">ATAN(expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-128">ATAN(expression)</span></span>

<span data-ttu-id="81d99-129">지정한 숫자 식의 아크탄젠트 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-129">Returns the arctangent value of the specified numeric expression.</span></span>

<span data-ttu-id="81d99-130">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-130">**Arguments**</span></span>

<span data-ttu-id="81d99-131">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-131">`expression`: A `Double`.</span></span>

<span data-ttu-id="81d99-132">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-132">**Return Value**</span></span>

<span data-ttu-id="81d99-133">`Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-133">A `Double`.</span></span>

<span data-ttu-id="81d99-134">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-134">**Example**</span></span>

`SqlServer.ATAN(9)`

## <a name="atn2expression-expression"></a><span data-ttu-id="81d99-135">ATN2(expression, expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-135">ATN2(expression, expression)</span></span>

<span data-ttu-id="81d99-136">탄젠트 값이 지정한 두 숫자 식 사이에 속하는 각도를 라디안으로 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-136">Returns the angle, in radians, whose tangent is between the two specified numeric expressions.</span></span>

<span data-ttu-id="81d99-137">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-137">**Arguments**</span></span>

<span data-ttu-id="81d99-138">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-138">`expression`: A `Double`.</span></span>

<span data-ttu-id="81d99-139">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-139">**Return Value**</span></span>

<span data-ttu-id="81d99-140">`Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-140">A `Double`.</span></span>

<span data-ttu-id="81d99-141">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-141">**Example**</span></span>

`SqlServer.ATN2(9, 8)`
 
## <a name="ceilingexpression"></a><span data-ttu-id="81d99-142">CEILING(expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-142">CEILING(expression)</span></span>

<span data-ttu-id="81d99-143">지정한 식을 해당 식보다 크거나 같은 가장 작은 정수로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-143">Converts the specified expression to the smallest integer that is greater than or equal to it.</span></span>

<span data-ttu-id="81d99-144">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-144">**Arguments**</span></span>

<span data-ttu-id="81d99-145">`expression`: `Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-145">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="81d99-146">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-146">**Return Value**</span></span>

<span data-ttu-id="81d99-147">`Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-147">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="81d99-148">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-148">**Example**</span></span> 

[!code-csharp[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_ceiling)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_ceiling)]

## <a name="cosexpression"></a><span data-ttu-id="81d99-149">COS(expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-149">COS(expression)</span></span>

<span data-ttu-id="81d99-150">라디안으로 지정된 각도의 삼각 코사인을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-150">Calculates the trigonometric cosine of the specified angle in radians.</span></span> 

<span data-ttu-id="81d99-151">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-151">**Arguments**</span></span> 

<span data-ttu-id="81d99-152">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-152">`expression`: A `Double`.</span></span> 

<span data-ttu-id="81d99-153">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-153">**Return Value**</span></span> 

<span data-ttu-id="81d99-154">`Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-154">A `Double`.</span></span> 

<span data-ttu-id="81d99-155">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-155">**Example**</span></span> 

`SqlServer.COS(45)`

## <a name="cotexpression"></a><span data-ttu-id="81d99-156">COT(expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-156">COT(expression)</span></span>

<span data-ttu-id="81d99-157">지정된 각도의 삼각 코탄젠트를 라디안으로 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-157">Calculates the trigonometric cotangent of the specified angle in radians.</span></span> 

<span data-ttu-id="81d99-158">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-158">**Arguments**</span></span> 

<span data-ttu-id="81d99-159">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-159">`expression`: A `Double`.</span></span> 

<span data-ttu-id="81d99-160">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-160">**Return Value**</span></span> 

<span data-ttu-id="81d99-161">`Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-161">A `Double`.</span></span> 

<span data-ttu-id="81d99-162">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-162">**Example**</span></span> 

`SqlServer.COT(60)`
  
## <a name="degreesradians"></a><span data-ttu-id="81d99-163">DEGREES(radians)</span><span class="sxs-lookup"><span data-stu-id="81d99-163">DEGREES(radians)</span></span>

<span data-ttu-id="81d99-164">해당 각도를 도 단위로 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-164">Returns the corresponding angle in degrees.</span></span> 

<span data-ttu-id="81d99-165">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-165">**Arguments**</span></span> 

<span data-ttu-id="81d99-166">`expression`: `Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-166">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="81d99-167">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-167">**Return Value**</span></span> 

<span data-ttu-id="81d99-168">`Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-168">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="81d99-169">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-169">**Example**</span></span> 

`SqlServer.DEGREES(3.1)`

## <a name="expexpression"></a><span data-ttu-id="81d99-170">EXP(expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-170">EXP(expression)</span></span>

<span data-ttu-id="81d99-171">지정한 숫자 식의 지수 값을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-171">Calculates the exponential value of a specified numeric expression.</span></span> 

<span data-ttu-id="81d99-172">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-172">**Arguments**</span></span> 

<span data-ttu-id="81d99-173">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-173">`expression`: A `Double`.</span></span> 

<span data-ttu-id="81d99-174">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-174">**Return Value**</span></span> 

<span data-ttu-id="81d99-175">`Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-175">A `Double`.</span></span> 

<span data-ttu-id="81d99-176">**예제** `SqlServer.EXP(1)`</span><span class="sxs-lookup"><span data-stu-id="81d99-176">**Example** `SqlServer.EXP(1)`</span></span>

## <a name="floorexpression"></a><span data-ttu-id="81d99-177">FLOOR(expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-177">FLOOR(expression)</span></span>

<span data-ttu-id="81d99-178">지정한 식을 해당 식보다 작거나 같은 가장 큰 정수로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-178">Converts the specified expression to the largest integer less than or equal to it.</span></span> 

<span data-ttu-id="81d99-179">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-179">**Arguments**</span></span> 

<span data-ttu-id="81d99-180">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-180">`expression`: A `Double`.</span></span> 

<span data-ttu-id="81d99-181">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-181">**Return Value**</span></span> 

<span data-ttu-id="81d99-182">`Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-182">A `Double`.</span></span> 

<span data-ttu-id="81d99-183">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-183">**Example**</span></span> 

[!code-csharp[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_floor)] 
[!code-sql[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_floor)]

## <a name="logexpression"></a><span data-ttu-id="81d99-184">LOG(expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-184">LOG(expression)</span></span>

<span data-ttu-id="81d99-185">지정한 `float` 식의 자연 로그를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-185">Calculates the natural logarithm of the specified `float` expression.</span></span> 

<span data-ttu-id="81d99-186">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-186">**Arguments**</span></span> 

<span data-ttu-id="81d99-187">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-187">`expression`: A `Double`.</span></span> 

<span data-ttu-id="81d99-188">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-188">**Return Value**</span></span> 

<span data-ttu-id="81d99-189">`Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-189">A `Double`.</span></span> 

<span data-ttu-id="81d99-190">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-190">**Example**</span></span> 

`SqlServer.LOG(100)`

## <a name="log10expression"></a><span data-ttu-id="81d99-191">LOG10(expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-191">LOG10(expression)</span></span>

<span data-ttu-id="81d99-192">지정한 `Double` 식의 상용 로그를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-192">Returns the base-10 logarithm of the specified `Double` expression.</span></span> 

<span data-ttu-id="81d99-193">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-193">**Arguments**</span></span> 

<span data-ttu-id="81d99-194">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-194">`expression`: A `Double`.</span></span> 

<span data-ttu-id="81d99-195">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-195">**Return Value**</span></span> 

<span data-ttu-id="81d99-196">`Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-196">A `Double`.</span></span> 

<span data-ttu-id="81d99-197">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-197">**Example**</span></span> 

`SqlServer.LOG10(100)`

## <a name="pi"></a><span data-ttu-id="81d99-198">PI()</span><span class="sxs-lookup"><span data-stu-id="81d99-198">PI()</span></span>

<span data-ttu-id="81d99-199">파이의 상수 값을 `Double`로 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-199">Returns the constant value of pi as a `Double`.</span></span> 

<span data-ttu-id="81d99-200">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-200">**Return Value**</span></span> 

<span data-ttu-id="81d99-201">`Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-201">A `Double`.</span></span> 

<span data-ttu-id="81d99-202">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-202">**Example**</span></span> 

`SqlServer.PI()`

## <a name="powernumericexpression-powerexpression"></a><span data-ttu-id="81d99-203">POWER (numeric_expression, power_expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-203">POWER(numeric_expression, power_expression)</span></span>

<span data-ttu-id="81d99-204">지정한 숫자 식의 지정된 거듭제곱 값을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-204">Calculates the value of a specified expression to a specified power.</span></span>

<span data-ttu-id="81d99-205">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-205">**Arguments**</span></span> 

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="81d99-206">`Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-206">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>|
|`power_expression`| <span data-ttu-id="81d99-207">`Double`에 대해 계산할 거듭제곱을 나타내는 `numeric_expression`입니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-207">A `Double` that represents the power to which to raise the `numeric_expression`.</span></span>| 

<span data-ttu-id="81d99-208">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-208">**Return Value**</span></span> 

<span data-ttu-id="81d99-209">지정한 `numeric_expression`에 지정한 `power_expression`을 거듭제곱한 값입니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-209">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span> 

<span data-ttu-id="81d99-210">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-210">**Example**</span></span> 

`SqlServer.POWER(2,7)`

## <a name="radiansexpression"></a><span data-ttu-id="81d99-211">RADIANS(expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-211">RADIANS(expression)</span></span>

<span data-ttu-id="81d99-212">각도를 라디안으로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-212">Converts degrees to radians.</span></span> 

<span data-ttu-id="81d99-213">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-213">**Arguments**</span></span> 

<span data-ttu-id="81d99-214">`expression`: `Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-214">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="81d99-215">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-215">**Return Value**</span></span> 

<span data-ttu-id="81d99-216">`Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-216">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="81d99-217">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-217">**Example**</span></span> 

`SqlServer.RADIANS(360.0)`

## <a name="randseed"></a><span data-ttu-id="81d99-218">RAND([seed])</span><span class="sxs-lookup"><span data-stu-id="81d99-218">RAND([seed])</span></span>

<span data-ttu-id="81d99-219">0에서 1 사이의 임의 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-219">Returns a random value from 0 through 1.</span></span> 

<span data-ttu-id="81d99-220">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-220">**Arguments**</span></span> 

<span data-ttu-id="81d99-221">시드 값으로는 `Int32`합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-221">The seed value as an `Int32`.</span></span> <span data-ttu-id="81d99-222">시드를 지정하지 않으면 SQL Server 데이터베이스 엔진에서 시드 값을 임의로 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-222">If the seed is not specified, the SQL Server Database Engine assigns a seed value at random.</span></span> <span data-ttu-id="81d99-223">지정된 특정 시드 값에 대해 반환되는 결과는 항상 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-223">For a specified seed value, the result returned is always the same.</span></span>

<span data-ttu-id="81d99-224">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-224">**Return Value**</span></span> 

<span data-ttu-id="81d99-225">0에서 1 사이의 임의 `Double` 값입니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-225">A random `Double` value from 0 through 1.</span></span> 

<span data-ttu-id="81d99-226">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-226">**Example**</span></span> 

`SqlServer.RAND()`
  
## <a name="roundnumericexpression-lengthfunction"></a><span data-ttu-id="81d99-227">ROUND(numeric_expression, length[,function])</span><span class="sxs-lookup"><span data-stu-id="81d99-227">ROUND(numeric_expression, length[,function])</span></span>

<span data-ttu-id="81d99-228">숫자 식을 지정한 길이나 전체 자릿수로 반올림하여 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-228">Returns a numeric expression, rounded to the specified length or precision.</span></span> 

<span data-ttu-id="81d99-229">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-229">**Arguments**</span></span> 

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="81d99-230">`Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-230">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 
|`length`| <span data-ttu-id="81d99-231">`Int32`을 반올림할 전체 자릿수를 나타내는 `numeric_expression`입니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-231">An `Int32` that represents the precision to which `numeric_expression` is to be rounded.</span></span> <span data-ttu-id="81d99-232">`length`가 양수일 경우 `numeric_expression`은 `length`에서 지정한 소수 자릿수로 반올림됩니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-232">When `length` is a positive number, `numeric_expression` is rounded to the number of decimal positions specified by `length`.</span></span> <span data-ttu-id="81d99-233">`length`가 음수일 경우 `numeric_expression`은 `length`에서 지정한 대로 소수점의 왼쪽에서 반올림됩니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-233">When `length` is a negative number, `numeric_expression` is rounded on the left side of the decimal point, as specified by `length`.</span></span>|
|`function` | <span data-ttu-id="81d99-234">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-234">Optional.</span></span> <span data-ttu-id="81d99-235">`Int32` 수행할 연산 형식을 나타내는입니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-235">An `Int32` that represents the type of operation to perform.</span></span> <span data-ttu-id="81d99-236">함수를 생략 하거나 값이 0 (기본값) 일 때 `numeric_expression` 반올림 됩니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-236">When function is omitted or has a value of 0 (default), `numeric_expression` is rounded.</span></span> <span data-ttu-id="81d99-237">이외의 값 0을 지정 하면 `numeric_expression` 잘립니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-237">When a value other than 0 is specified, `numeric_expression` is truncated.</span></span> |

<span data-ttu-id="81d99-238">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-238">**Return Value**</span></span> 

<span data-ttu-id="81d99-239">지정한 `numeric_expression`에 지정한 `power_expression`을 거듭제곱한 값입니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-239">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span>

<span data-ttu-id="81d99-240">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-240">**Example**</span></span> 

`SqlServer.ROUND(748.58, -3)`

## <a name="signexpression"></a><span data-ttu-id="81d99-241">SIGN(expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-241">SIGN(expression)</span></span> 

<span data-ttu-id="81d99-242">지정한 식의 양수(+1), 0 또는 음수(-1) 부호를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-242">Returns the positive (+1), zero (0), or negative (-1) sign of the specified expression.</span></span> 

<span data-ttu-id="81d99-243">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-243">**Arguments**</span></span> 

<span data-ttu-id="81d99-244">`expression`: `Int32`, `Int64`, `Double` 또는 `Decimal`</span><span class="sxs-lookup"><span data-stu-id="81d99-244">`expression`: `Int32`, `Int64`, `Double`, or `Decimal`</span></span> 

<span data-ttu-id="81d99-245">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-245">**Return Value**</span></span> 

<span data-ttu-id="81d99-246">`Int32`, `Int64`를 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-246">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="81d99-247">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-247">**Example**</span></span> 

`SqlServer.SIGN(-10)`

## <a name="sinexpression"></a><span data-ttu-id="81d99-248">SIN(expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-248">SIN(expression)</span></span>

<span data-ttu-id="81d99-249">라디안으로 지정한 각도의 삼각 사인을 계산하여 `Double` 식을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-249">Calculates the trigonometric sine of the specified angle in radians, and returns a `Double` expression.</span></span> 

<span data-ttu-id="81d99-250">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-250">**Arguments**</span></span> 

<span data-ttu-id="81d99-251">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-251">`expression`: A `Double`.</span></span> 

<span data-ttu-id="81d99-252">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-252">**Return Value**</span></span> 

<span data-ttu-id="81d99-253">`Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-253">A `Double`.</span></span> 

<span data-ttu-id="81d99-254">**예제** `SqlServer.SIN(20)`</span><span class="sxs-lookup"><span data-stu-id="81d99-254">**Example** `SqlServer.SIN(20)`</span></span>

## <a name="sqrtexpression"></a><span data-ttu-id="81d99-255">SQRT(expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-255">SQRT(expression)</span></span>

<span data-ttu-id="81d99-256">지정한 식의 제곱근을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-256">Returns the square root of the specified expression.</span></span> 

<span data-ttu-id="81d99-257">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-257">**Arguments**</span></span> 

<span data-ttu-id="81d99-258">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-258">`expression`: A `Double`.</span></span> 

<span data-ttu-id="81d99-259">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-259">**Return Value**</span></span> 

<span data-ttu-id="81d99-260">`Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-260">A `Double`.</span></span> 

<span data-ttu-id="81d99-261">**예제** `SqlServer.SQRT(3600)`</span><span class="sxs-lookup"><span data-stu-id="81d99-261">**Example** `SqlServer.SQRT(3600)`</span></span>

## <a name="squareexpression"></a><span data-ttu-id="81d99-262">SQUARE(expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-262">SQUARE(expression)</span></span>

<span data-ttu-id="81d99-263">지정한 식의 제곱을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-263">Returns the square of the specified expression.</span></span> 

<span data-ttu-id="81d99-264">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-264">**Arguments**</span></span> 

<span data-ttu-id="81d99-265">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-265">`expression`: A `Double`.</span></span> 

<span data-ttu-id="81d99-266">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-266">**Return Value**</span></span> 

<span data-ttu-id="81d99-267">`Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-267">A `Double`.</span></span> 

<span data-ttu-id="81d99-268">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-268">**Example**</span></span> 

`SqlServer.SQUARE(25)`

## <a name="tanexpression"></a><span data-ttu-id="81d99-269">TAN(expression)</span><span class="sxs-lookup"><span data-stu-id="81d99-269">TAN(expression)</span></span>

<span data-ttu-id="81d99-270">지정한 식의 탄젠트를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="81d99-270">Calculates the tangent of a specified expression.</span></span>

<span data-ttu-id="81d99-271">**인수**</span><span class="sxs-lookup"><span data-stu-id="81d99-271">**Arguments**</span></span> 

<span data-ttu-id="81d99-272">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="81d99-272">`expression`: `Double`</span></span> 

<span data-ttu-id="81d99-273">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="81d99-273">**Return Value**</span></span> 

`Double` 

<span data-ttu-id="81d99-274">**예제**</span><span class="sxs-lookup"><span data-stu-id="81d99-274">**Example**</span></span> 

`SqlServer.TAN(45.0)`
  
## <a name="see-also"></a><span data-ttu-id="81d99-275">참고자료</span><span class="sxs-lookup"><span data-stu-id="81d99-275">See also</span></span>

<span data-ttu-id="81d99-276">SqlClient에서 지원하는 수치 함수에 대한 자세한 내용은 SqlClient 공급자 매니페스트에 지정한 SQL Server 버전의 설명서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="81d99-276">For more information about the mathematical functions that SqlClient supports, see the documentation for the SQL Server version that you specified in the SqlClient provider manifest:</span></span>

- <span data-ttu-id="81d99-277">**SQL Server 2005:** [수치 연산 함수 (TRANSACT-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms177516(v=sql.90))</span><span class="sxs-lookup"><span data-stu-id="81d99-277">**SQL Server 2005:** [Mathematical Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms177516(v=sql.90))</span></span>
- <span data-ttu-id="81d99-278">**SQL Server 2008:** [수치 연산 함수 (TRANSACT-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2008/ms177516(v=sql.100))</span><span class="sxs-lookup"><span data-stu-id="81d99-278">**SQL Server 2008:** [Mathematical Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2008/ms177516(v=sql.100))</span></span>
- <span data-ttu-id="81d99-279">**SQL Server 2012 이상:** [수치 연산 함수 (TRANSACT-SQL)](/sql/t-sql/functions/mathematical-functions-transact-sql?view=sql-server-2017)</span><span class="sxs-lookup"><span data-stu-id="81d99-279">**SQL Server 2012 and later:** [Mathematical Functions (Transact-SQL)](/sql/t-sql/functions/mathematical-functions-transact-sql?view=sql-server-2017)</span></span>

- [<span data-ttu-id="81d99-280">Entity Framework용 SqlClient 기능</span><span class="sxs-lookup"><span data-stu-id="81d99-280">SqlClient for Entity Framework Functions</span></span>](sqlclient-for-ef-functions.md)
