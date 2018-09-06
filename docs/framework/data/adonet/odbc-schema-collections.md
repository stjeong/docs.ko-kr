---
title: ODBC 스키마 컬렉션
ms.date: 03/30/2017
ms.assetid: 1bb126a5-ceec-4649-a4bc-8aa19e801046
ms.openlocfilehash: bdedbb11960f02b99dcca6388abf663635238f74
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43750011"
---
# <a name="odbc-schema-collections"></a><span data-ttu-id="c20cc-102">ODBC 스키마 컬렉션</span><span class="sxs-lookup"><span data-stu-id="c20cc-102">ODBC Schema Collections</span></span>
<span data-ttu-id="c20cc-103">이 단원에서는 Microsoft SQL Server, Oracle 및 Microsoft Jet용 ODBC 드라이버에서 지원하는 스키마 컬렉션에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="c20cc-103">This section discusses schema collection support for the ODBC drivers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-odbc-driver"></a><span data-ttu-id="c20cc-104">Microsoft SQL Server ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="c20cc-104">Microsoft SQL Server ODBC Driver</span></span>  
 <span data-ttu-id="c20cc-105">Microsoft SQL Server ODBC Driver에서는 공통 스키마 컬렉션 외에도 다음과 같은 특정 스키마 컬렉션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c20cc-105">The Microsoft SQL Server ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="c20cc-106">Tables</span><span class="sxs-lookup"><span data-stu-id="c20cc-106">Tables</span></span>  
  
-   <span data-ttu-id="c20cc-107">Indexes</span><span class="sxs-lookup"><span data-stu-id="c20cc-107">Indexes</span></span>  
  
-   <span data-ttu-id="c20cc-108">Columns</span><span class="sxs-lookup"><span data-stu-id="c20cc-108">Columns</span></span>  
  
-   <span data-ttu-id="c20cc-109">절차</span><span class="sxs-lookup"><span data-stu-id="c20cc-109">Procedures</span></span>  
  
-   <span data-ttu-id="c20cc-110">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="c20cc-110">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="c20cc-111">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="c20cc-111">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="c20cc-112">뷰</span><span class="sxs-lookup"><span data-stu-id="c20cc-112">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="c20cc-113">Tables 및 Views</span><span class="sxs-lookup"><span data-stu-id="c20cc-113">Tables and Views</span></span>  
  
|<span data-ttu-id="c20cc-114">열 이름</span><span class="sxs-lookup"><span data-stu-id="c20cc-114">ColumnName</span></span>|<span data-ttu-id="c20cc-115">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c20cc-115">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c20cc-116">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="c20cc-116">TABLE_CAT</span></span>|<span data-ttu-id="c20cc-117">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-117">String</span></span>|  
|<span data-ttu-id="c20cc-118">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="c20cc-118">TABLE_SCHEM</span></span>|<span data-ttu-id="c20cc-119">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-119">String</span></span>|  
|<span data-ttu-id="c20cc-120">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-120">TABLE_NAME</span></span>|<span data-ttu-id="c20cc-121">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-121">String</span></span>|  
|<span data-ttu-id="c20cc-122">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-122">TABLE_TYPE</span></span>|<span data-ttu-id="c20cc-123">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-123">String</span></span>|  
|<span data-ttu-id="c20cc-124">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c20cc-124">REMARKS</span></span>|<span data-ttu-id="c20cc-125">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-125">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="c20cc-126">Indexes</span><span class="sxs-lookup"><span data-stu-id="c20cc-126">Indexes</span></span>  
  
|<span data-ttu-id="c20cc-127">열 이름</span><span class="sxs-lookup"><span data-stu-id="c20cc-127">ColumnName</span></span>|<span data-ttu-id="c20cc-128">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c20cc-128">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c20cc-129">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="c20cc-129">TABLE_CAT</span></span>|<span data-ttu-id="c20cc-130">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-130">String</span></span>|  
|<span data-ttu-id="c20cc-131">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="c20cc-131">TABLE_SCHEM</span></span>|<span data-ttu-id="c20cc-132">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-132">String</span></span>|  
|<span data-ttu-id="c20cc-133">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-133">TABLE_NAME</span></span>|<span data-ttu-id="c20cc-134">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-134">String</span></span>|  
|<span data-ttu-id="c20cc-135">NON_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="c20cc-135">NON_UNIQUE</span></span>|<span data-ttu-id="c20cc-136">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-136">Int16</span></span>|  
|<span data-ttu-id="c20cc-137">INDEX_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="c20cc-137">INDEX_QUALIFIER</span></span>|<span data-ttu-id="c20cc-138">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-138">String</span></span>|  
|<span data-ttu-id="c20cc-139">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-139">INDEX_NAME</span></span>|<span data-ttu-id="c20cc-140">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-140">String</span></span>|  
|<span data-ttu-id="c20cc-141">TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-141">TYPE</span></span>|<span data-ttu-id="c20cc-142">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-142">Int16</span></span>|  
|<span data-ttu-id="c20cc-143">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c20cc-143">ORDINAL_POSITION</span></span>|<span data-ttu-id="c20cc-144">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-144">Int16</span></span>|  
|<span data-ttu-id="c20cc-145">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-145">COLUMN_NAME</span></span>|<span data-ttu-id="c20cc-146">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-146">String</span></span>|  
|<span data-ttu-id="c20cc-147">ASC_OR_DESC</span><span class="sxs-lookup"><span data-stu-id="c20cc-147">ASC_OR_DESC</span></span>|<span data-ttu-id="c20cc-148">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-148">String</span></span>|  
|<span data-ttu-id="c20cc-149">CARDINATLITY</span><span class="sxs-lookup"><span data-stu-id="c20cc-149">CARDINATLITY</span></span>|<span data-ttu-id="c20cc-150">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-150">Int32</span></span>|  
|<span data-ttu-id="c20cc-151">PAGES</span><span class="sxs-lookup"><span data-stu-id="c20cc-151">PAGES</span></span>|<span data-ttu-id="c20cc-152">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-152">Int32</span></span>|  
|<span data-ttu-id="c20cc-153">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="c20cc-153">FILTER_CONDITION</span></span>|<span data-ttu-id="c20cc-154">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-154">String</span></span>|  
|<span data-ttu-id="c20cc-155">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c20cc-155">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="c20cc-156">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-156">String</span></span>|  
|<span data-ttu-id="c20cc-157">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-157">SS_DATA_TYPE</span></span>|<span data-ttu-id="c20cc-158">Byte</span><span class="sxs-lookup"><span data-stu-id="c20cc-158">Byte</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="c20cc-159">Columns</span><span class="sxs-lookup"><span data-stu-id="c20cc-159">Columns</span></span>  
  
|<span data-ttu-id="c20cc-160">열 이름</span><span class="sxs-lookup"><span data-stu-id="c20cc-160">ColumnName</span></span>|<span data-ttu-id="c20cc-161">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c20cc-161">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c20cc-162">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="c20cc-162">TABLE_CAT</span></span>|<span data-ttu-id="c20cc-163">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-163">String</span></span>|  
|<span data-ttu-id="c20cc-164">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="c20cc-164">TABLE_SCHEM</span></span>|<span data-ttu-id="c20cc-165">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-165">String</span></span>|  
|<span data-ttu-id="c20cc-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-166">TABLE_NAME</span></span>|<span data-ttu-id="c20cc-167">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-167">String</span></span>|  
|<span data-ttu-id="c20cc-168">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-168">COLUMN_NAME</span></span>|<span data-ttu-id="c20cc-169">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-169">String</span></span>|  
|<span data-ttu-id="c20cc-170">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-170">DATA_TYPE</span></span>|<span data-ttu-id="c20cc-171">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-171">Int16</span></span>|  
|<span data-ttu-id="c20cc-172">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-172">TYPE_NAME</span></span>|<span data-ttu-id="c20cc-173">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-173">String</span></span>|  
|<span data-ttu-id="c20cc-174">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="c20cc-174">COLUMN_SIZE</span></span>|<span data-ttu-id="c20cc-175">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-175">Int32</span></span>|  
|<span data-ttu-id="c20cc-176">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c20cc-176">BUFFER_LENGTH</span></span>|<span data-ttu-id="c20cc-177">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-177">Int32</span></span>|  
|<span data-ttu-id="c20cc-178">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="c20cc-178">DECIMAL_DIGITS</span></span>|<span data-ttu-id="c20cc-179">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-179">Int16</span></span>|  
|<span data-ttu-id="c20cc-180">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="c20cc-180">NUM_PREC_RADIX</span></span>|<span data-ttu-id="c20cc-181">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-181">Int16</span></span>|  
|<span data-ttu-id="c20cc-182">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c20cc-182">NULLABLE</span></span>|<span data-ttu-id="c20cc-183">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-183">Int16</span></span>|  
|<span data-ttu-id="c20cc-184">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c20cc-184">REMARKS</span></span>|<span data-ttu-id="c20cc-185">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-185">String</span></span>|  
|<span data-ttu-id="c20cc-186">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="c20cc-186">COLUMN_DEF</span></span>|<span data-ttu-id="c20cc-187">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-187">String</span></span>|  
|<span data-ttu-id="c20cc-188">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-188">SQL_DATA_TYPE</span></span>|<span data-ttu-id="c20cc-189">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-189">Int16</span></span>|  
|<span data-ttu-id="c20cc-190">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="c20cc-190">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="c20cc-191">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-191">Int16</span></span>|  
|<span data-ttu-id="c20cc-192">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c20cc-192">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="c20cc-193">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-193">Int32</span></span>|  
|<span data-ttu-id="c20cc-194">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c20cc-194">ORDINAL_POSITION</span></span>|<span data-ttu-id="c20cc-195">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-195">Int32</span></span>|  
|<span data-ttu-id="c20cc-196">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c20cc-196">IS_NULLABLE</span></span>|<span data-ttu-id="c20cc-197">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-197">String</span></span>|  
|<span data-ttu-id="c20cc-198">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c20cc-198">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="c20cc-199">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-199">String</span></span>|  
|<span data-ttu-id="c20cc-200">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c20cc-200">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="c20cc-201">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-201">String</span></span>|  
|<span data-ttu-id="c20cc-202">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-202">SS_DATA_TYPE</span></span>|<span data-ttu-id="c20cc-203">Byte</span><span class="sxs-lookup"><span data-stu-id="c20cc-203">Byte</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="c20cc-204">절차</span><span class="sxs-lookup"><span data-stu-id="c20cc-204">Procedures</span></span>  
  
|<span data-ttu-id="c20cc-205">열 이름</span><span class="sxs-lookup"><span data-stu-id="c20cc-205">ColumnName</span></span>|<span data-ttu-id="c20cc-206">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c20cc-206">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c20cc-207">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="c20cc-207">PROCEDURE_CAT</span></span>|<span data-ttu-id="c20cc-208">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-208">String</span></span>|  
|<span data-ttu-id="c20cc-209">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="c20cc-209">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="c20cc-210">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-210">String</span></span>|  
|<span data-ttu-id="c20cc-211">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-211">PROCEDURE_NAME</span></span>|<span data-ttu-id="c20cc-212">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-212">String</span></span>|  
|<span data-ttu-id="c20cc-213">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="c20cc-213">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="c20cc-214">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-214">Int32</span></span>|  
|<span data-ttu-id="c20cc-215">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="c20cc-215">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="c20cc-216">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-216">Int32</span></span>|  
|<span data-ttu-id="c20cc-217">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="c20cc-217">NUM_RESULT_SETS</span></span>|<span data-ttu-id="c20cc-218">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-218">Int32</span></span>|  
|<span data-ttu-id="c20cc-219">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c20cc-219">REMARKS</span></span>|<span data-ttu-id="c20cc-220">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-220">String</span></span>|  
|<span data-ttu-id="c20cc-221">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-221">PROCEDURE_TYPE</span></span>|<span data-ttu-id="c20cc-222">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-222">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="c20cc-223">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="c20cc-223">ProcedureColumns</span></span>  
  
|<span data-ttu-id="c20cc-224">열 이름</span><span class="sxs-lookup"><span data-stu-id="c20cc-224">ColumnName</span></span>|<span data-ttu-id="c20cc-225">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c20cc-225">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c20cc-226">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="c20cc-226">PROCEDURE_CAT</span></span>|<span data-ttu-id="c20cc-227">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-227">String</span></span>|  
|<span data-ttu-id="c20cc-228">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="c20cc-228">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="c20cc-229">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-229">String</span></span>|  
|<span data-ttu-id="c20cc-230">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-230">PROCEDURE_NAME</span></span>|<span data-ttu-id="c20cc-231">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-231">String</span></span>|  
|<span data-ttu-id="c20cc-232">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-232">COLUMN_NAME</span></span>|<span data-ttu-id="c20cc-233">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-233">String</span></span>|  
|<span data-ttu-id="c20cc-234">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-234">COLUMN_TYPE</span></span>|<span data-ttu-id="c20cc-235">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-235">Int16</span></span>|  
|<span data-ttu-id="c20cc-236">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-236">DATA_TYPE</span></span>|<span data-ttu-id="c20cc-237">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-237">Int16</span></span>|  
|<span data-ttu-id="c20cc-238">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-238">TYPE_NAME</span></span>|<span data-ttu-id="c20cc-239">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-239">String</span></span>|  
|<span data-ttu-id="c20cc-240">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="c20cc-240">COLUMN_SIZE</span></span>|<span data-ttu-id="c20cc-241">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-241">Int32</span></span>|  
|<span data-ttu-id="c20cc-242">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c20cc-242">BUFFER_LENGTH</span></span>|<span data-ttu-id="c20cc-243">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-243">Int32</span></span>|  
|<span data-ttu-id="c20cc-244">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="c20cc-244">DECIMAL_DIGITS</span></span>|<span data-ttu-id="c20cc-245">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-245">Int16</span></span>|  
|<span data-ttu-id="c20cc-246">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="c20cc-246">NUM_PREC_RADIX</span></span>|<span data-ttu-id="c20cc-247">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-247">Int16</span></span>|  
|<span data-ttu-id="c20cc-248">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c20cc-248">NULLABLE</span></span>|<span data-ttu-id="c20cc-249">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-249">Int16</span></span>|  
|<span data-ttu-id="c20cc-250">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c20cc-250">REMARKS</span></span>|<span data-ttu-id="c20cc-251">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-251">String</span></span>|  
|<span data-ttu-id="c20cc-252">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="c20cc-252">COLUMN_DEF</span></span>|<span data-ttu-id="c20cc-253">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-253">String</span></span>|  
|<span data-ttu-id="c20cc-254">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-254">SQL_DATA_TYPE</span></span>|<span data-ttu-id="c20cc-255">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-255">Int16</span></span>|  
|<span data-ttu-id="c20cc-256">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="c20cc-256">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="c20cc-257">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-257">Int16</span></span>|  
|<span data-ttu-id="c20cc-258">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c20cc-258">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="c20cc-259">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-259">Int32</span></span>|  
|<span data-ttu-id="c20cc-260">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c20cc-260">ORDINAL_POSITION</span></span>|<span data-ttu-id="c20cc-261">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-261">Int32</span></span>|  
|<span data-ttu-id="c20cc-262">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c20cc-262">IS_NULLABLE</span></span>|<span data-ttu-id="c20cc-263">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-263">String</span></span>|  
|<span data-ttu-id="c20cc-264">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c20cc-264">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="c20cc-265">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-265">String</span></span>|  
|<span data-ttu-id="c20cc-266">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c20cc-266">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="c20cc-267">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-267">String</span></span>|  
|<span data-ttu-id="c20cc-268">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-268">SS_DATA_TYPE</span></span>|<span data-ttu-id="c20cc-269">Byte</span><span class="sxs-lookup"><span data-stu-id="c20cc-269">Byte</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="c20cc-270">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="c20cc-270">ProcedureParameters</span></span>  
  
|<span data-ttu-id="c20cc-271">열 이름</span><span class="sxs-lookup"><span data-stu-id="c20cc-271">ColumnName</span></span>|<span data-ttu-id="c20cc-272">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c20cc-272">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c20cc-273">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="c20cc-273">PROCEDURE_CAT</span></span>|<span data-ttu-id="c20cc-274">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-274">String</span></span>|  
|<span data-ttu-id="c20cc-275">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="c20cc-275">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="c20cc-276">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-276">String</span></span>|  
|<span data-ttu-id="c20cc-277">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-277">PROCEDURE_NAME</span></span>|<span data-ttu-id="c20cc-278">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-278">String</span></span>|  
|<span data-ttu-id="c20cc-279">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-279">COLUMN_NAME</span></span>|<span data-ttu-id="c20cc-280">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-280">String</span></span>|  
|<span data-ttu-id="c20cc-281">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-281">COLUMN_TYPE</span></span>|<span data-ttu-id="c20cc-282">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-282">Int16</span></span>|  
|<span data-ttu-id="c20cc-283">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-283">DATA_TYPE</span></span>|<span data-ttu-id="c20cc-284">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-284">Int16</span></span>|  
|<span data-ttu-id="c20cc-285">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-285">TYPE_NAME</span></span>|<span data-ttu-id="c20cc-286">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-286">String</span></span>|  
|<span data-ttu-id="c20cc-287">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="c20cc-287">COLUMN_SIZE</span></span>|<span data-ttu-id="c20cc-288">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-288">Int32</span></span>|  
|<span data-ttu-id="c20cc-289">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c20cc-289">BUFFER_LENGTH</span></span>|<span data-ttu-id="c20cc-290">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-290">Int32</span></span>|  
|<span data-ttu-id="c20cc-291">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="c20cc-291">DECIMAL_DIGITS</span></span>|<span data-ttu-id="c20cc-292">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-292">Int16</span></span>|  
|<span data-ttu-id="c20cc-293">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="c20cc-293">NUM_PREC_RADIX</span></span>|<span data-ttu-id="c20cc-294">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-294">Int16</span></span>|  
|<span data-ttu-id="c20cc-295">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c20cc-295">NULLABLE</span></span>|<span data-ttu-id="c20cc-296">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-296">Int16</span></span>|  
|<span data-ttu-id="c20cc-297">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c20cc-297">REMARKS</span></span>|<span data-ttu-id="c20cc-298">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-298">String</span></span>|  
|<span data-ttu-id="c20cc-299">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="c20cc-299">COLUMN_DEF</span></span>|<span data-ttu-id="c20cc-300">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-300">String</span></span>|  
|<span data-ttu-id="c20cc-301">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-301">SQL_DATA_TYPE</span></span>|<span data-ttu-id="c20cc-302">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-302">Int16</span></span>|  
|<span data-ttu-id="c20cc-303">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="c20cc-303">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="c20cc-304">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-304">Int16</span></span>|  
|<span data-ttu-id="c20cc-305">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c20cc-305">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="c20cc-306">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-306">Int32</span></span>|  
|<span data-ttu-id="c20cc-307">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c20cc-307">ORDINAL_POSITION</span></span>|<span data-ttu-id="c20cc-308">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-308">Int32</span></span>|  
|<span data-ttu-id="c20cc-309">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c20cc-309">IS_NULLABLE</span></span>|<span data-ttu-id="c20cc-310">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-310">String</span></span>|  
|<span data-ttu-id="c20cc-311">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c20cc-311">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="c20cc-312">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-312">String</span></span>|  
|<span data-ttu-id="c20cc-313">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c20cc-313">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="c20cc-314">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-314">String</span></span>|  
|<span data-ttu-id="c20cc-315">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-315">SS_DATA_TYPE</span></span>|<span data-ttu-id="c20cc-316">Byte</span><span class="sxs-lookup"><span data-stu-id="c20cc-316">Byte</span></span>|  
  
## <a name="microsoft-oracle-odbc-driver"></a><span data-ttu-id="c20cc-317">Microsoft Oracle ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="c20cc-317">Microsoft Oracle ODBC Driver</span></span>  
 <span data-ttu-id="c20cc-318">Microsoft SQL Server Oracle ODBC Driver에서는 공통 스키마 컬렉션 외에도 다음과 같은 특정 스키마 컬렉션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c20cc-318">The Microsoft SQL Server Oracle ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="c20cc-319">Tables</span><span class="sxs-lookup"><span data-stu-id="c20cc-319">Tables</span></span>  
  
-   <span data-ttu-id="c20cc-320">Columns</span><span class="sxs-lookup"><span data-stu-id="c20cc-320">Columns</span></span>  
  
-   <span data-ttu-id="c20cc-321">절차</span><span class="sxs-lookup"><span data-stu-id="c20cc-321">Procedures</span></span>  
  
-   <span data-ttu-id="c20cc-322">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="c20cc-322">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="c20cc-323">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="c20cc-323">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="c20cc-324">뷰</span><span class="sxs-lookup"><span data-stu-id="c20cc-324">Views</span></span>  
  
-   <span data-ttu-id="c20cc-325">Indexes</span><span class="sxs-lookup"><span data-stu-id="c20cc-325">Indexes</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="c20cc-326">Tables 및 Views</span><span class="sxs-lookup"><span data-stu-id="c20cc-326">Tables and Views</span></span>  
  
|<span data-ttu-id="c20cc-327">열 이름</span><span class="sxs-lookup"><span data-stu-id="c20cc-327">ColumnName</span></span>|<span data-ttu-id="c20cc-328">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c20cc-328">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c20cc-329">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="c20cc-329">TABLE_QUALIFIER</span></span>|<span data-ttu-id="c20cc-330">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-330">String</span></span>|  
|<span data-ttu-id="c20cc-331">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="c20cc-331">TABLE_OWNER</span></span>|<span data-ttu-id="c20cc-332">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-332">String</span></span>|  
|<span data-ttu-id="c20cc-333">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-333">TABLE_NAME</span></span>|<span data-ttu-id="c20cc-334">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-334">String</span></span>|  
|<span data-ttu-id="c20cc-335">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-335">TABLE_TYPE</span></span>|<span data-ttu-id="c20cc-336">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-336">String</span></span>|  
|<span data-ttu-id="c20cc-337">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c20cc-337">REMARKS</span></span>|<span data-ttu-id="c20cc-338">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-338">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="c20cc-339">Columns</span><span class="sxs-lookup"><span data-stu-id="c20cc-339">Columns</span></span>  
  
|<span data-ttu-id="c20cc-340">열 이름</span><span class="sxs-lookup"><span data-stu-id="c20cc-340">ColumnName</span></span>|<span data-ttu-id="c20cc-341">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c20cc-341">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c20cc-342">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="c20cc-342">TABLE_QUALIFIER</span></span>|<span data-ttu-id="c20cc-343">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-343">String</span></span>|  
|<span data-ttu-id="c20cc-344">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="c20cc-344">TABLE_OWNER</span></span>|<span data-ttu-id="c20cc-345">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-345">String</span></span>|  
|<span data-ttu-id="c20cc-346">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-346">TABLE_NAME</span></span>|<span data-ttu-id="c20cc-347">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-347">String</span></span>|  
|<span data-ttu-id="c20cc-348">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-348">COLUMN_NAME</span></span>|<span data-ttu-id="c20cc-349">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-349">String</span></span>|  
|<span data-ttu-id="c20cc-350">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-350">DATA_TYPE</span></span>|<span data-ttu-id="c20cc-351">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-351">Int16</span></span>|  
|<span data-ttu-id="c20cc-352">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-352">TYPE_NAME</span></span>|<span data-ttu-id="c20cc-353">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-353">String</span></span>|  
|<span data-ttu-id="c20cc-354">PRECISION</span><span class="sxs-lookup"><span data-stu-id="c20cc-354">PRECISION</span></span>|<span data-ttu-id="c20cc-355">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-355">Int32</span></span>|  
|<span data-ttu-id="c20cc-356">LENGTH</span><span class="sxs-lookup"><span data-stu-id="c20cc-356">LENGTH</span></span>|<span data-ttu-id="c20cc-357">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-357">Int32</span></span>|  
|<span data-ttu-id="c20cc-358">SCALE</span><span class="sxs-lookup"><span data-stu-id="c20cc-358">SCALE</span></span>|<span data-ttu-id="c20cc-359">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-359">Int16</span></span>|  
|<span data-ttu-id="c20cc-360">RADIX</span><span class="sxs-lookup"><span data-stu-id="c20cc-360">RADIX</span></span>|<span data-ttu-id="c20cc-361">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-361">Int16</span></span>|  
|<span data-ttu-id="c20cc-362">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c20cc-362">NULLABLE</span></span>|<span data-ttu-id="c20cc-363">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-363">Int16</span></span>|  
|<span data-ttu-id="c20cc-364">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c20cc-364">REMARKS</span></span>|<span data-ttu-id="c20cc-365">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-365">String</span></span>|  
|<span data-ttu-id="c20cc-366">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c20cc-366">ORDINAL_POSITION</span></span>|<span data-ttu-id="c20cc-367">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-367">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="c20cc-368">절차</span><span class="sxs-lookup"><span data-stu-id="c20cc-368">Procedures</span></span>  
  
|<span data-ttu-id="c20cc-369">열 이름</span><span class="sxs-lookup"><span data-stu-id="c20cc-369">ColumnName</span></span>|<span data-ttu-id="c20cc-370">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c20cc-370">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c20cc-371">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="c20cc-371">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="c20cc-372">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-372">String</span></span>|  
|<span data-ttu-id="c20cc-373">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="c20cc-373">PROCEDURE_OWNER</span></span>|<span data-ttu-id="c20cc-374">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-374">String</span></span>|  
|<span data-ttu-id="c20cc-375">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-375">PROCEDURE_NAME</span></span>|<span data-ttu-id="c20cc-376">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-376">String</span></span>|  
|<span data-ttu-id="c20cc-377">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="c20cc-377">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="c20cc-378">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-378">Int16</span></span>|  
|<span data-ttu-id="c20cc-379">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="c20cc-379">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="c20cc-380">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-380">Int16</span></span>|  
|<span data-ttu-id="c20cc-381">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="c20cc-381">NUM_RESULT_SETS</span></span>|<span data-ttu-id="c20cc-382">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-382">Int16</span></span>|  
|<span data-ttu-id="c20cc-383">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c20cc-383">REMARKS</span></span>|<span data-ttu-id="c20cc-384">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-384">String</span></span>|  
|<span data-ttu-id="c20cc-385">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-385">PROCEDURE_TYPE</span></span>|<span data-ttu-id="c20cc-386">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-386">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="c20cc-387">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="c20cc-387">ProcedureColumns</span></span>  
  
|<span data-ttu-id="c20cc-388">열 이름</span><span class="sxs-lookup"><span data-stu-id="c20cc-388">ColumnName</span></span>|<span data-ttu-id="c20cc-389">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c20cc-389">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c20cc-390">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="c20cc-390">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="c20cc-391">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-391">String</span></span>|  
|<span data-ttu-id="c20cc-392">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="c20cc-392">PROCEDURE_OWNER</span></span>|<span data-ttu-id="c20cc-393">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-393">String</span></span>|  
|<span data-ttu-id="c20cc-394">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-394">PROCEDURE_NAME</span></span>|<span data-ttu-id="c20cc-395">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-395">String</span></span>|  
|<span data-ttu-id="c20cc-396">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-396">COLUMN_NAME</span></span>|<span data-ttu-id="c20cc-397">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-397">String</span></span>|  
|<span data-ttu-id="c20cc-398">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-398">COLUMN_TYPE</span></span>|<span data-ttu-id="c20cc-399">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-399">Int16</span></span>|  
|<span data-ttu-id="c20cc-400">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-400">DATA_TYPE</span></span>|<span data-ttu-id="c20cc-401">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-401">Int16</span></span>|  
|<span data-ttu-id="c20cc-402">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-402">TYPE_NAME</span></span>|<span data-ttu-id="c20cc-403">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-403">String</span></span>|  
|<span data-ttu-id="c20cc-404">PRECISION</span><span class="sxs-lookup"><span data-stu-id="c20cc-404">PRECISION</span></span>|<span data-ttu-id="c20cc-405">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-405">Int32</span></span>|  
|<span data-ttu-id="c20cc-406">LENGTH</span><span class="sxs-lookup"><span data-stu-id="c20cc-406">LENGTH</span></span>|<span data-ttu-id="c20cc-407">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-407">Int32</span></span>|  
|<span data-ttu-id="c20cc-408">SCALE</span><span class="sxs-lookup"><span data-stu-id="c20cc-408">SCALE</span></span>|<span data-ttu-id="c20cc-409">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-409">Int16</span></span>|  
|<span data-ttu-id="c20cc-410">RADIX</span><span class="sxs-lookup"><span data-stu-id="c20cc-410">RADIX</span></span>|<span data-ttu-id="c20cc-411">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-411">Int16</span></span>|  
|<span data-ttu-id="c20cc-412">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c20cc-412">NULLABLE</span></span>|<span data-ttu-id="c20cc-413">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-413">Int16</span></span>|  
|<span data-ttu-id="c20cc-414">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c20cc-414">REMARKS</span></span>|<span data-ttu-id="c20cc-415">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-415">String</span></span>|  
|<span data-ttu-id="c20cc-416">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="c20cc-416">OVERLOAD</span></span>|<span data-ttu-id="c20cc-417">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-417">Int32</span></span>|  
|<span data-ttu-id="c20cc-418">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c20cc-418">ORDINAL_POSITION</span></span>|<span data-ttu-id="c20cc-419">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-419">Int32</span></span>|  
  
## <a name="microsoft-jet-odbc-driver"></a><span data-ttu-id="c20cc-420">Microsoft Jet ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="c20cc-420">Microsoft Jet ODBC Driver</span></span>  
 <span data-ttu-id="c20cc-421">Microsoft Jet ODBC Driver                                             .</span><span class="sxs-lookup"><span data-stu-id="c20cc-421">The Microsoft Jet ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="c20cc-422">Tables</span><span class="sxs-lookup"><span data-stu-id="c20cc-422">Tables</span></span>  
  
-   <span data-ttu-id="c20cc-423">Indexes</span><span class="sxs-lookup"><span data-stu-id="c20cc-423">Indexes</span></span>  
  
-   <span data-ttu-id="c20cc-424">Columns</span><span class="sxs-lookup"><span data-stu-id="c20cc-424">Columns</span></span>  
  
-   <span data-ttu-id="c20cc-425">절차</span><span class="sxs-lookup"><span data-stu-id="c20cc-425">Procedures</span></span>  
  
-   <span data-ttu-id="c20cc-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="c20cc-426">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="c20cc-427">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="c20cc-427">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="c20cc-428">뷰</span><span class="sxs-lookup"><span data-stu-id="c20cc-428">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="c20cc-429">Tables 및 Views</span><span class="sxs-lookup"><span data-stu-id="c20cc-429">Tables and Views</span></span>  
  
|<span data-ttu-id="c20cc-430">열 이름</span><span class="sxs-lookup"><span data-stu-id="c20cc-430">ColumnName</span></span>|<span data-ttu-id="c20cc-431">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c20cc-431">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c20cc-432">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="c20cc-432">TABLE_QUALIFIER</span></span>|<span data-ttu-id="c20cc-433">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-433">String</span></span>|  
|<span data-ttu-id="c20cc-434">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="c20cc-434">TABLE_OWNER</span></span>|<span data-ttu-id="c20cc-435">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-435">String</span></span>|  
|<span data-ttu-id="c20cc-436">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-436">TABLE_NAME</span></span>|<span data-ttu-id="c20cc-437">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-437">String</span></span>|  
|<span data-ttu-id="c20cc-438">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-438">TABLE_TYPE</span></span>|<span data-ttu-id="c20cc-439">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-439">String</span></span>|  
|<span data-ttu-id="c20cc-440">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c20cc-440">REMARKS</span></span>|<span data-ttu-id="c20cc-441">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-441">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="c20cc-442">Columns</span><span class="sxs-lookup"><span data-stu-id="c20cc-442">Columns</span></span>  
  
|<span data-ttu-id="c20cc-443">열 이름</span><span class="sxs-lookup"><span data-stu-id="c20cc-443">ColumnName</span></span>|<span data-ttu-id="c20cc-444">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c20cc-444">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c20cc-445">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="c20cc-445">TABLE_QUALIFIER</span></span>|<span data-ttu-id="c20cc-446">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-446">String</span></span>|  
|<span data-ttu-id="c20cc-447">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="c20cc-447">TABLE_OWNER</span></span>|<span data-ttu-id="c20cc-448">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-448">String</span></span>|  
|<span data-ttu-id="c20cc-449">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-449">TABLE_NAME</span></span>|<span data-ttu-id="c20cc-450">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-450">String</span></span>|  
|<span data-ttu-id="c20cc-451">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-451">COLUMN_NAME</span></span>|<span data-ttu-id="c20cc-452">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-452">String</span></span>|  
|<span data-ttu-id="c20cc-453">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-453">DATA_TYPE</span></span>|<span data-ttu-id="c20cc-454">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-454">Int16</span></span>|  
|<span data-ttu-id="c20cc-455">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-455">TYPE_NAME</span></span>|<span data-ttu-id="c20cc-456">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-456">String</span></span>|  
|<span data-ttu-id="c20cc-457">PRECISION</span><span class="sxs-lookup"><span data-stu-id="c20cc-457">PRECISION</span></span>|<span data-ttu-id="c20cc-458">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-458">Int32</span></span>|  
|<span data-ttu-id="c20cc-459">LENGTH</span><span class="sxs-lookup"><span data-stu-id="c20cc-459">LENGTH</span></span>|<span data-ttu-id="c20cc-460">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-460">Int32</span></span>|  
|<span data-ttu-id="c20cc-461">SCALE</span><span class="sxs-lookup"><span data-stu-id="c20cc-461">SCALE</span></span>|<span data-ttu-id="c20cc-462">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-462">Int16</span></span>|  
|<span data-ttu-id="c20cc-463">RADIX</span><span class="sxs-lookup"><span data-stu-id="c20cc-463">RADIX</span></span>|<span data-ttu-id="c20cc-464">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-464">Int16</span></span>|  
|<span data-ttu-id="c20cc-465">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c20cc-465">NULLABLE</span></span>|<span data-ttu-id="c20cc-466">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-466">Int16</span></span>|  
|<span data-ttu-id="c20cc-467">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c20cc-467">REMARKS</span></span>|<span data-ttu-id="c20cc-468">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-468">String</span></span>|  
|<span data-ttu-id="c20cc-469">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c20cc-469">ORDINAL_POSITION</span></span>|<span data-ttu-id="c20cc-470">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-470">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="c20cc-471">절차</span><span class="sxs-lookup"><span data-stu-id="c20cc-471">Procedures</span></span>  
  
|<span data-ttu-id="c20cc-472">열 이름</span><span class="sxs-lookup"><span data-stu-id="c20cc-472">ColumnName</span></span>|<span data-ttu-id="c20cc-473">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c20cc-473">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c20cc-474">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="c20cc-474">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="c20cc-475">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-475">String</span></span>|  
|<span data-ttu-id="c20cc-476">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="c20cc-476">PROCEDURE_OWNER</span></span>|<span data-ttu-id="c20cc-477">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-477">String</span></span>|  
|<span data-ttu-id="c20cc-478">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-478">PROCEDURE_NAME</span></span>|<span data-ttu-id="c20cc-479">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-479">String</span></span>|  
|<span data-ttu-id="c20cc-480">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="c20cc-480">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="c20cc-481">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-481">Int16</span></span>|  
|<span data-ttu-id="c20cc-482">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="c20cc-482">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="c20cc-483">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-483">Int16</span></span>|  
|<span data-ttu-id="c20cc-484">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="c20cc-484">NUM_RESULT_SETS</span></span>|<span data-ttu-id="c20cc-485">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-485">Int16</span></span>|  
|<span data-ttu-id="c20cc-486">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c20cc-486">REMARKS</span></span>|<span data-ttu-id="c20cc-487">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-487">String</span></span>|  
|<span data-ttu-id="c20cc-488">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-488">PROCEDURE_TYPE</span></span>|<span data-ttu-id="c20cc-489">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-489">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="c20cc-490">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="c20cc-490">ProcedureColumns</span></span>  
  
|<span data-ttu-id="c20cc-491">열 이름</span><span class="sxs-lookup"><span data-stu-id="c20cc-491">ColumnName</span></span>|<span data-ttu-id="c20cc-492">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c20cc-492">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c20cc-493">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="c20cc-493">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="c20cc-494">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-494">String</span></span>|  
|<span data-ttu-id="c20cc-495">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="c20cc-495">PROCEDURE_OWNER</span></span>|<span data-ttu-id="c20cc-496">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-496">String</span></span>|  
|<span data-ttu-id="c20cc-497">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-497">PROCEDURE_NAME</span></span>|<span data-ttu-id="c20cc-498">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-498">String</span></span>|  
|<span data-ttu-id="c20cc-499">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-499">COLUMN_NAME</span></span>|<span data-ttu-id="c20cc-500">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-500">String</span></span>|  
|<span data-ttu-id="c20cc-501">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-501">COLUMN_TYPE</span></span>|<span data-ttu-id="c20cc-502">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-502">Int16</span></span>|  
|<span data-ttu-id="c20cc-503">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-503">DATA_TYPE</span></span>|<span data-ttu-id="c20cc-504">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-504">Int16</span></span>|  
|<span data-ttu-id="c20cc-505">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-505">TYPE_NAME</span></span>|<span data-ttu-id="c20cc-506">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-506">String</span></span>|  
|<span data-ttu-id="c20cc-507">PRECISION</span><span class="sxs-lookup"><span data-stu-id="c20cc-507">PRECISION</span></span>|<span data-ttu-id="c20cc-508">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-508">Int32</span></span>|  
|<span data-ttu-id="c20cc-509">LENGTH</span><span class="sxs-lookup"><span data-stu-id="c20cc-509">LENGTH</span></span>|<span data-ttu-id="c20cc-510">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-510">Int32</span></span>|  
|<span data-ttu-id="c20cc-511">SCALE</span><span class="sxs-lookup"><span data-stu-id="c20cc-511">SCALE</span></span>|<span data-ttu-id="c20cc-512">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-512">Int16</span></span>|  
|<span data-ttu-id="c20cc-513">RADIX</span><span class="sxs-lookup"><span data-stu-id="c20cc-513">RADIX</span></span>|<span data-ttu-id="c20cc-514">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-514">Int16</span></span>|  
|<span data-ttu-id="c20cc-515">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c20cc-515">NULLABLE</span></span>|<span data-ttu-id="c20cc-516">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-516">Int16</span></span>|  
|<span data-ttu-id="c20cc-517">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c20cc-517">REMARKS</span></span>|<span data-ttu-id="c20cc-518">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-518">String</span></span>|  
|<span data-ttu-id="c20cc-519">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="c20cc-519">OVERLOAD</span></span>|<span data-ttu-id="c20cc-520">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-520">Int32</span></span>|  
|<span data-ttu-id="c20cc-521">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c20cc-521">ORDINAL_POSITION</span></span>|<span data-ttu-id="c20cc-522">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-522">Int32</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="c20cc-523">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="c20cc-523">ProcedureParameters</span></span>  
  
|<span data-ttu-id="c20cc-524">열 이름</span><span class="sxs-lookup"><span data-stu-id="c20cc-524">ColumnName</span></span>|<span data-ttu-id="c20cc-525">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c20cc-525">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c20cc-526">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="c20cc-526">PROCEDURE_CAT</span></span>|<span data-ttu-id="c20cc-527">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-527">String</span></span>|  
|<span data-ttu-id="c20cc-528">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="c20cc-528">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="c20cc-529">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-529">String</span></span>|  
|<span data-ttu-id="c20cc-530">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-530">PROCEDURE_NAME</span></span>|<span data-ttu-id="c20cc-531">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-531">String</span></span>|  
|<span data-ttu-id="c20cc-532">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-532">COLUMN_NAME</span></span>|<span data-ttu-id="c20cc-533">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-533">String</span></span>|  
|<span data-ttu-id="c20cc-534">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-534">COLUMN_TYPE</span></span>|<span data-ttu-id="c20cc-535">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-535">Int16</span></span>|  
|<span data-ttu-id="c20cc-536">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-536">DATA_TYPE</span></span>|<span data-ttu-id="c20cc-537">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-537">Int16</span></span>|  
|<span data-ttu-id="c20cc-538">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c20cc-538">TYPE_NAME</span></span>|<span data-ttu-id="c20cc-539">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-539">String</span></span>|  
|<span data-ttu-id="c20cc-540">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="c20cc-540">COLUMN_SIZE</span></span>|<span data-ttu-id="c20cc-541">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-541">Int32</span></span>|  
|<span data-ttu-id="c20cc-542">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c20cc-542">BUFFER_LENGTH</span></span>|<span data-ttu-id="c20cc-543">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-543">Int32</span></span>|  
|<span data-ttu-id="c20cc-544">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="c20cc-544">DECIMAL_DIGITS</span></span>|<span data-ttu-id="c20cc-545">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-545">Int16</span></span>|  
|<span data-ttu-id="c20cc-546">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="c20cc-546">NUM_PREC_RADIX</span></span>|<span data-ttu-id="c20cc-547">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-547">Int16</span></span>|  
|<span data-ttu-id="c20cc-548">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c20cc-548">NULLABLE</span></span>|<span data-ttu-id="c20cc-549">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-549">Int16</span></span>|  
|<span data-ttu-id="c20cc-550">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c20cc-550">REMARKS</span></span>|<span data-ttu-id="c20cc-551">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-551">String</span></span>|  
|<span data-ttu-id="c20cc-552">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="c20cc-552">COLUMN_DEF</span></span>|<span data-ttu-id="c20cc-553">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-553">String</span></span>|  
|<span data-ttu-id="c20cc-554">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c20cc-554">SQL_DATA_TYPE</span></span>|<span data-ttu-id="c20cc-555">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-555">Int16</span></span>|  
|<span data-ttu-id="c20cc-556">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="c20cc-556">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="c20cc-557">Int16</span><span class="sxs-lookup"><span data-stu-id="c20cc-557">Int16</span></span>|  
|<span data-ttu-id="c20cc-558">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c20cc-558">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="c20cc-559">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-559">Int32</span></span>|  
|<span data-ttu-id="c20cc-560">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c20cc-560">ORDINAL_POSITION</span></span>|<span data-ttu-id="c20cc-561">Int32</span><span class="sxs-lookup"><span data-stu-id="c20cc-561">Int32</span></span>|  
|<span data-ttu-id="c20cc-562">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c20cc-562">IS_NULLABLE</span></span>|<span data-ttu-id="c20cc-563">문자열</span><span class="sxs-lookup"><span data-stu-id="c20cc-563">String</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c20cc-564">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c20cc-564">See Also</span></span>  
 [<span data-ttu-id="c20cc-565">ADO.NET 관리되는 공급자 및 데이터 집합 개발자 센터</span><span class="sxs-lookup"><span data-stu-id="c20cc-565">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
