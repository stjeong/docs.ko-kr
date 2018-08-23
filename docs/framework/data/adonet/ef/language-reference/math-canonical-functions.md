---
title: 수학 정식 함수
ms.date: 03/30/2017
ms.assetid: 6f6cddc6-b561-4ebe-84b6-841ef5b4113b
ms.openlocfilehash: 0fc9f4942c3f76f139ab7e4400005f0bfe80204e
ms.sourcegitcommit: a1e35d4e94edab384a63406c0a5438306873031b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "42754489"
---
# <a name="math-canonical-functions"></a><span data-ttu-id="26af5-102">수학 정식 함수</span><span class="sxs-lookup"><span data-stu-id="26af5-102">Math Canonical Functions</span></span>

<span data-ttu-id="26af5-103">Entity SQL 수학 정식 함수를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-103">Entity SQL includes the following math canonical functions:</span></span>
  
## <a name="absvalue"></a><span data-ttu-id="26af5-104">Abs(value)</span><span class="sxs-lookup"><span data-stu-id="26af5-104">Abs(value)</span></span>

<span data-ttu-id="26af5-105">`value`의 절대값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-105">Returns the absolute value of `value`.</span></span>

<span data-ttu-id="26af5-106">**인수**</span><span class="sxs-lookup"><span data-stu-id="26af5-106">**Arguments**</span></span>

<span data-ttu-id="26af5-107">`Int16`, `Int32`를 `Int64`, `Byte`를 `Single`를 `Double`, 및 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-107">An `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="26af5-108">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="26af5-108">**Return Value**</span></span>

<span data-ttu-id="26af5-109">`value`의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-109">The type of `value`.</span></span>

<span data-ttu-id="26af5-110">**예제**</span><span class="sxs-lookup"><span data-stu-id="26af5-110">**Example**</span></span>

`Abs(-2)`

## <a name="ceilingvalue"></a><span data-ttu-id="26af5-111">Ceiling(value)</span><span class="sxs-lookup"><span data-stu-id="26af5-111">Ceiling(value)</span></span>

<span data-ttu-id="26af5-112">`value`보다 작지 않은 가장 작은 정수를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-112">Returns the smallest integer that is not less than `value`.</span></span>

<span data-ttu-id="26af5-113">**인수**</span><span class="sxs-lookup"><span data-stu-id="26af5-113">**Arguments**</span></span>

<span data-ttu-id="26af5-114">A `Single`, `Double`, 및 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-114">A `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="26af5-115">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="26af5-115">**Return Value**</span></span>

<span data-ttu-id="26af5-116">`value`의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-116">The type of `value`.</span></span>

<span data-ttu-id="26af5-117">**예제**</span><span class="sxs-lookup"><span data-stu-id="26af5-117">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_CEILING](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_ceiling)]
[!code-sql[DP EntityServices Concepts#EDM_CEILING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_ceiling)]

## <a name="floorvalue"></a><span data-ttu-id="26af5-118">Floor(value)</span><span class="sxs-lookup"><span data-stu-id="26af5-118">Floor(value)</span></span>

<span data-ttu-id="26af5-119">`value`보다 크지 않은 가장 큰 정수를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-119">Returns the largest integer that is not greater than `value`.</span></span>

<span data-ttu-id="26af5-120">**인수**</span><span class="sxs-lookup"><span data-stu-id="26af5-120">**Arguments**</span></span>

<span data-ttu-id="26af5-121">A `Single`, `Double`, 및 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-121">A `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="26af5-122">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="26af5-122">**Return Value**</span></span>

<span data-ttu-id="26af5-123">`value`의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-123">The type of `value`.</span></span>

<span data-ttu-id="26af5-124">**예제**</span><span class="sxs-lookup"><span data-stu-id="26af5-124">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_FLOOR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_floor)]
[!code-sql[DP EntityServices Concepts#EDM_FLOOR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_floor)]

## <a name="powervalue-exponent"></a><span data-ttu-id="26af5-125">Power(value, exponent)</span><span class="sxs-lookup"><span data-stu-id="26af5-125">Power(value, exponent)</span></span>

<span data-ttu-id="26af5-126">지정된 `value`에 대해 지정된 `exponent`의 결과를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-126">Returns the result of the specified `value` to the specified `exponent`.</span></span>

<span data-ttu-id="26af5-127">**인수**</span><span class="sxs-lookup"><span data-stu-id="26af5-127">**Arguments**</span></span>

|  |  |
|--|--|
|`value` | <span data-ttu-id="26af5-128">`Int32, Int64, Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-128">An `Int32, Int64, Double`, or `Decimal`.</span></span> |
|`exponent` | <span data-ttu-id="26af5-129">`Int64`하십시오 `Double`, 또는 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-129">An `Int64`, `Double`, or `Decimal`.</span></span> |

<span data-ttu-id="26af5-130">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="26af5-130">**Return Value**</span></span>

<span data-ttu-id="26af5-131">`value`의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-131">The type of `value`.</span></span>

<span data-ttu-id="26af5-132">**예제**</span><span class="sxs-lookup"><span data-stu-id="26af5-132">**Example**</span></span>

`Power(748.58,2)`

## <a name="roundvalue"></a><span data-ttu-id="26af5-133">Round(value)</span><span class="sxs-lookup"><span data-stu-id="26af5-133">Round(value)</span></span>

<span data-ttu-id="26af5-134">`value`의 정수 부분을 가장 가까운 정수로 반올림하여 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-134">Returns the integer portion of `value`, rounded to the nearest integer.</span></span>

<span data-ttu-id="26af5-135">**인수**</span><span class="sxs-lookup"><span data-stu-id="26af5-135">**Arguments**</span></span>

<span data-ttu-id="26af5-136">A `Single`, `Double`, 및 `Decimal`합니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-136">A `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="26af5-137">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="26af5-137">**Return Value**</span></span>

<span data-ttu-id="26af5-138">`value`의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-138">The type of `value`.</span></span>

<span data-ttu-id="26af5-139">**예제**</span><span class="sxs-lookup"><span data-stu-id="26af5-139">**Example**</span></span>

`Round(748.58)`

## <a name="roundvalue-digits"></a><span data-ttu-id="26af5-140">Round(value, digits)</span><span class="sxs-lookup"><span data-stu-id="26af5-140">Round(value, digits)</span></span>

<span data-ttu-id="26af5-141">`value`를 지정된 `digits` 중 가장 가까운 숫자로 반올림하여 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-141">Returns the `value`, rounded to the nearest specified `digits`.</span></span>

<span data-ttu-id="26af5-142">**인수**</span><span class="sxs-lookup"><span data-stu-id="26af5-142">**Arguments**</span></span>

|  |  |
|--|--|
|`value`|<span data-ttu-id="26af5-143">`Double` 또는 `Decimal`</span><span class="sxs-lookup"><span data-stu-id="26af5-143">`Double` or `Decimal`.</span></span>|
|`digits`|<span data-ttu-id="26af5-144">`Int16` 또는 `Int32`</span><span class="sxs-lookup"><span data-stu-id="26af5-144">`Int16` or `Int32`.</span></span>|

<span data-ttu-id="26af5-145">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="26af5-145">**Return Value**</span></span>

<span data-ttu-id="26af5-146">`value`의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-146">The type of `value`.</span></span>

<span data-ttu-id="26af5-147">**예제**</span><span class="sxs-lookup"><span data-stu-id="26af5-147">**Example**</span></span>

`Round(748.58,1)`

## <a name="truncatevalue-digits"></a><span data-ttu-id="26af5-148">Truncate(value, digits)</span><span class="sxs-lookup"><span data-stu-id="26af5-148">Truncate(value, digits)</span></span>

<span data-ttu-id="26af5-149">`value`를 지정된 `digits` 중 가장 가까운 숫자로 잘라 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-149">Returns the `value`, truncated to the nearest specified `digits`.</span></span>

<span data-ttu-id="26af5-150">**인수**</span><span class="sxs-lookup"><span data-stu-id="26af5-150">**Arguments**</span></span>

|  |  |
|--|--|
|`value`|<span data-ttu-id="26af5-151">`Double` 또는 `Decimal`</span><span class="sxs-lookup"><span data-stu-id="26af5-151">`Double` or `Decimal`.</span></span>|
|`digits`|<span data-ttu-id="26af5-152">`Int16` 또는 `Int32`</span><span class="sxs-lookup"><span data-stu-id="26af5-152">`Int16` or `Int32`.</span></span>|

<span data-ttu-id="26af5-153">**반환 값**</span><span class="sxs-lookup"><span data-stu-id="26af5-153">**Return Value**</span></span>

<span data-ttu-id="26af5-154">`value`의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-154">The type of `value`.</span></span>

<span data-ttu-id="26af5-155">**예제**</span><span class="sxs-lookup"><span data-stu-id="26af5-155">**Example**</span></span>

`Truncate(748.58,1)`  
  
 <span data-ttu-id="26af5-156">이러한 함수는 `null`이 입력되면 `null`을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-156">These functions will return `null` if given `null` input.</span></span>  
  
 <span data-ttu-id="26af5-157">동일한 기능을 Microsoft SQL 클라이언트 관리 공급자에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-157">Equivalent functionality is available in the Microsoft SQL Client Managed Provider.</span></span> <span data-ttu-id="26af5-158">자세한 내용은 [Entity Framework 함수에 대 한 SqlClient](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="26af5-158">For more information, see [SqlClient for Entity Framework Functions](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26af5-159">참고 항목</span><span class="sxs-lookup"><span data-stu-id="26af5-159">See Also</span></span>  
 [<span data-ttu-id="26af5-160">정식 함수</span><span class="sxs-lookup"><span data-stu-id="26af5-160">Canonical Functions</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md)
