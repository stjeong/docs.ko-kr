---
title: ODBC 스키마 컬렉션
ms.date: 03/30/2017
ms.assetid: 1bb126a5-ceec-4649-a4bc-8aa19e801046
ms.openlocfilehash: bdedbb11960f02b99dcca6388abf663635238f74
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43479982"
---
# <a name="odbc-schema-collections"></a><span data-ttu-id="c620b-102">ODBC 스키마 컬렉션</span><span class="sxs-lookup"><span data-stu-id="c620b-102">ODBC Schema Collections</span></span>
<span data-ttu-id="c620b-103">이 단원에서는 Microsoft SQL Server, Oracle 및 Microsoft Jet용 ODBC 드라이버에서 지원하는 스키마 컬렉션에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="c620b-103">This section discusses schema collection support for the ODBC drivers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-odbc-driver"></a><span data-ttu-id="c620b-104">Microsoft SQL Server ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="c620b-104">Microsoft SQL Server ODBC Driver</span></span>  
 <span data-ttu-id="c620b-105">Microsoft SQL Server ODBC Driver에서는 공통 스키마 컬렉션 외에도 다음과 같은 특정 스키마 컬렉션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c620b-105">The Microsoft SQL Server ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="c620b-106">Tables</span><span class="sxs-lookup"><span data-stu-id="c620b-106">Tables</span></span>  
  
-   <span data-ttu-id="c620b-107">Indexes</span><span class="sxs-lookup"><span data-stu-id="c620b-107">Indexes</span></span>  
  
-   <span data-ttu-id="c620b-108">Columns</span><span class="sxs-lookup"><span data-stu-id="c620b-108">Columns</span></span>  
  
-   <span data-ttu-id="c620b-109">절차</span><span class="sxs-lookup"><span data-stu-id="c620b-109">Procedures</span></span>  
  
-   <span data-ttu-id="c620b-110">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="c620b-110">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="c620b-111">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="c620b-111">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="c620b-112">뷰</span><span class="sxs-lookup"><span data-stu-id="c620b-112">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="c620b-113">Tables 및 Views</span><span class="sxs-lookup"><span data-stu-id="c620b-113">Tables and Views</span></span>  
  
|<span data-ttu-id="c620b-114">열 이름</span><span class="sxs-lookup"><span data-stu-id="c620b-114">ColumnName</span></span>|<span data-ttu-id="c620b-115">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c620b-115">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c620b-116">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="c620b-116">TABLE_CAT</span></span>|<span data-ttu-id="c620b-117">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-117">String</span></span>|  
|<span data-ttu-id="c620b-118">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="c620b-118">TABLE_SCHEM</span></span>|<span data-ttu-id="c620b-119">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-119">String</span></span>|  
|<span data-ttu-id="c620b-120">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-120">TABLE_NAME</span></span>|<span data-ttu-id="c620b-121">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-121">String</span></span>|  
|<span data-ttu-id="c620b-122">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-122">TABLE_TYPE</span></span>|<span data-ttu-id="c620b-123">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-123">String</span></span>|  
|<span data-ttu-id="c620b-124">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c620b-124">REMARKS</span></span>|<span data-ttu-id="c620b-125">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-125">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="c620b-126">Indexes</span><span class="sxs-lookup"><span data-stu-id="c620b-126">Indexes</span></span>  
  
|<span data-ttu-id="c620b-127">열 이름</span><span class="sxs-lookup"><span data-stu-id="c620b-127">ColumnName</span></span>|<span data-ttu-id="c620b-128">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c620b-128">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c620b-129">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="c620b-129">TABLE_CAT</span></span>|<span data-ttu-id="c620b-130">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-130">String</span></span>|  
|<span data-ttu-id="c620b-131">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="c620b-131">TABLE_SCHEM</span></span>|<span data-ttu-id="c620b-132">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-132">String</span></span>|  
|<span data-ttu-id="c620b-133">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-133">TABLE_NAME</span></span>|<span data-ttu-id="c620b-134">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-134">String</span></span>|  
|<span data-ttu-id="c620b-135">NON_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="c620b-135">NON_UNIQUE</span></span>|<span data-ttu-id="c620b-136">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-136">Int16</span></span>|  
|<span data-ttu-id="c620b-137">INDEX_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="c620b-137">INDEX_QUALIFIER</span></span>|<span data-ttu-id="c620b-138">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-138">String</span></span>|  
|<span data-ttu-id="c620b-139">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-139">INDEX_NAME</span></span>|<span data-ttu-id="c620b-140">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-140">String</span></span>|  
|<span data-ttu-id="c620b-141">TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-141">TYPE</span></span>|<span data-ttu-id="c620b-142">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-142">Int16</span></span>|  
|<span data-ttu-id="c620b-143">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c620b-143">ORDINAL_POSITION</span></span>|<span data-ttu-id="c620b-144">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-144">Int16</span></span>|  
|<span data-ttu-id="c620b-145">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-145">COLUMN_NAME</span></span>|<span data-ttu-id="c620b-146">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-146">String</span></span>|  
|<span data-ttu-id="c620b-147">ASC_OR_DESC</span><span class="sxs-lookup"><span data-stu-id="c620b-147">ASC_OR_DESC</span></span>|<span data-ttu-id="c620b-148">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-148">String</span></span>|  
|<span data-ttu-id="c620b-149">CARDINATLITY</span><span class="sxs-lookup"><span data-stu-id="c620b-149">CARDINATLITY</span></span>|<span data-ttu-id="c620b-150">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-150">Int32</span></span>|  
|<span data-ttu-id="c620b-151">PAGES</span><span class="sxs-lookup"><span data-stu-id="c620b-151">PAGES</span></span>|<span data-ttu-id="c620b-152">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-152">Int32</span></span>|  
|<span data-ttu-id="c620b-153">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="c620b-153">FILTER_CONDITION</span></span>|<span data-ttu-id="c620b-154">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-154">String</span></span>|  
|<span data-ttu-id="c620b-155">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c620b-155">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="c620b-156">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-156">String</span></span>|  
|<span data-ttu-id="c620b-157">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-157">SS_DATA_TYPE</span></span>|<span data-ttu-id="c620b-158">Byte</span><span class="sxs-lookup"><span data-stu-id="c620b-158">Byte</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="c620b-159">Columns</span><span class="sxs-lookup"><span data-stu-id="c620b-159">Columns</span></span>  
  
|<span data-ttu-id="c620b-160">열 이름</span><span class="sxs-lookup"><span data-stu-id="c620b-160">ColumnName</span></span>|<span data-ttu-id="c620b-161">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c620b-161">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c620b-162">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="c620b-162">TABLE_CAT</span></span>|<span data-ttu-id="c620b-163">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-163">String</span></span>|  
|<span data-ttu-id="c620b-164">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="c620b-164">TABLE_SCHEM</span></span>|<span data-ttu-id="c620b-165">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-165">String</span></span>|  
|<span data-ttu-id="c620b-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-166">TABLE_NAME</span></span>|<span data-ttu-id="c620b-167">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-167">String</span></span>|  
|<span data-ttu-id="c620b-168">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-168">COLUMN_NAME</span></span>|<span data-ttu-id="c620b-169">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-169">String</span></span>|  
|<span data-ttu-id="c620b-170">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-170">DATA_TYPE</span></span>|<span data-ttu-id="c620b-171">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-171">Int16</span></span>|  
|<span data-ttu-id="c620b-172">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-172">TYPE_NAME</span></span>|<span data-ttu-id="c620b-173">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-173">String</span></span>|  
|<span data-ttu-id="c620b-174">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="c620b-174">COLUMN_SIZE</span></span>|<span data-ttu-id="c620b-175">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-175">Int32</span></span>|  
|<span data-ttu-id="c620b-176">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c620b-176">BUFFER_LENGTH</span></span>|<span data-ttu-id="c620b-177">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-177">Int32</span></span>|  
|<span data-ttu-id="c620b-178">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="c620b-178">DECIMAL_DIGITS</span></span>|<span data-ttu-id="c620b-179">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-179">Int16</span></span>|  
|<span data-ttu-id="c620b-180">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="c620b-180">NUM_PREC_RADIX</span></span>|<span data-ttu-id="c620b-181">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-181">Int16</span></span>|  
|<span data-ttu-id="c620b-182">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c620b-182">NULLABLE</span></span>|<span data-ttu-id="c620b-183">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-183">Int16</span></span>|  
|<span data-ttu-id="c620b-184">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c620b-184">REMARKS</span></span>|<span data-ttu-id="c620b-185">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-185">String</span></span>|  
|<span data-ttu-id="c620b-186">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="c620b-186">COLUMN_DEF</span></span>|<span data-ttu-id="c620b-187">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-187">String</span></span>|  
|<span data-ttu-id="c620b-188">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-188">SQL_DATA_TYPE</span></span>|<span data-ttu-id="c620b-189">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-189">Int16</span></span>|  
|<span data-ttu-id="c620b-190">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="c620b-190">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="c620b-191">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-191">Int16</span></span>|  
|<span data-ttu-id="c620b-192">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c620b-192">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="c620b-193">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-193">Int32</span></span>|  
|<span data-ttu-id="c620b-194">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c620b-194">ORDINAL_POSITION</span></span>|<span data-ttu-id="c620b-195">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-195">Int32</span></span>|  
|<span data-ttu-id="c620b-196">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c620b-196">IS_NULLABLE</span></span>|<span data-ttu-id="c620b-197">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-197">String</span></span>|  
|<span data-ttu-id="c620b-198">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c620b-198">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="c620b-199">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-199">String</span></span>|  
|<span data-ttu-id="c620b-200">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c620b-200">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="c620b-201">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-201">String</span></span>|  
|<span data-ttu-id="c620b-202">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-202">SS_DATA_TYPE</span></span>|<span data-ttu-id="c620b-203">Byte</span><span class="sxs-lookup"><span data-stu-id="c620b-203">Byte</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="c620b-204">절차</span><span class="sxs-lookup"><span data-stu-id="c620b-204">Procedures</span></span>  
  
|<span data-ttu-id="c620b-205">열 이름</span><span class="sxs-lookup"><span data-stu-id="c620b-205">ColumnName</span></span>|<span data-ttu-id="c620b-206">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c620b-206">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c620b-207">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="c620b-207">PROCEDURE_CAT</span></span>|<span data-ttu-id="c620b-208">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-208">String</span></span>|  
|<span data-ttu-id="c620b-209">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="c620b-209">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="c620b-210">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-210">String</span></span>|  
|<span data-ttu-id="c620b-211">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-211">PROCEDURE_NAME</span></span>|<span data-ttu-id="c620b-212">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-212">String</span></span>|  
|<span data-ttu-id="c620b-213">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="c620b-213">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="c620b-214">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-214">Int32</span></span>|  
|<span data-ttu-id="c620b-215">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="c620b-215">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="c620b-216">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-216">Int32</span></span>|  
|<span data-ttu-id="c620b-217">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="c620b-217">NUM_RESULT_SETS</span></span>|<span data-ttu-id="c620b-218">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-218">Int32</span></span>|  
|<span data-ttu-id="c620b-219">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c620b-219">REMARKS</span></span>|<span data-ttu-id="c620b-220">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-220">String</span></span>|  
|<span data-ttu-id="c620b-221">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-221">PROCEDURE_TYPE</span></span>|<span data-ttu-id="c620b-222">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-222">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="c620b-223">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="c620b-223">ProcedureColumns</span></span>  
  
|<span data-ttu-id="c620b-224">열 이름</span><span class="sxs-lookup"><span data-stu-id="c620b-224">ColumnName</span></span>|<span data-ttu-id="c620b-225">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c620b-225">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c620b-226">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="c620b-226">PROCEDURE_CAT</span></span>|<span data-ttu-id="c620b-227">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-227">String</span></span>|  
|<span data-ttu-id="c620b-228">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="c620b-228">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="c620b-229">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-229">String</span></span>|  
|<span data-ttu-id="c620b-230">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-230">PROCEDURE_NAME</span></span>|<span data-ttu-id="c620b-231">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-231">String</span></span>|  
|<span data-ttu-id="c620b-232">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-232">COLUMN_NAME</span></span>|<span data-ttu-id="c620b-233">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-233">String</span></span>|  
|<span data-ttu-id="c620b-234">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-234">COLUMN_TYPE</span></span>|<span data-ttu-id="c620b-235">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-235">Int16</span></span>|  
|<span data-ttu-id="c620b-236">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-236">DATA_TYPE</span></span>|<span data-ttu-id="c620b-237">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-237">Int16</span></span>|  
|<span data-ttu-id="c620b-238">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-238">TYPE_NAME</span></span>|<span data-ttu-id="c620b-239">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-239">String</span></span>|  
|<span data-ttu-id="c620b-240">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="c620b-240">COLUMN_SIZE</span></span>|<span data-ttu-id="c620b-241">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-241">Int32</span></span>|  
|<span data-ttu-id="c620b-242">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c620b-242">BUFFER_LENGTH</span></span>|<span data-ttu-id="c620b-243">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-243">Int32</span></span>|  
|<span data-ttu-id="c620b-244">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="c620b-244">DECIMAL_DIGITS</span></span>|<span data-ttu-id="c620b-245">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-245">Int16</span></span>|  
|<span data-ttu-id="c620b-246">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="c620b-246">NUM_PREC_RADIX</span></span>|<span data-ttu-id="c620b-247">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-247">Int16</span></span>|  
|<span data-ttu-id="c620b-248">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c620b-248">NULLABLE</span></span>|<span data-ttu-id="c620b-249">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-249">Int16</span></span>|  
|<span data-ttu-id="c620b-250">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c620b-250">REMARKS</span></span>|<span data-ttu-id="c620b-251">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-251">String</span></span>|  
|<span data-ttu-id="c620b-252">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="c620b-252">COLUMN_DEF</span></span>|<span data-ttu-id="c620b-253">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-253">String</span></span>|  
|<span data-ttu-id="c620b-254">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-254">SQL_DATA_TYPE</span></span>|<span data-ttu-id="c620b-255">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-255">Int16</span></span>|  
|<span data-ttu-id="c620b-256">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="c620b-256">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="c620b-257">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-257">Int16</span></span>|  
|<span data-ttu-id="c620b-258">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c620b-258">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="c620b-259">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-259">Int32</span></span>|  
|<span data-ttu-id="c620b-260">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c620b-260">ORDINAL_POSITION</span></span>|<span data-ttu-id="c620b-261">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-261">Int32</span></span>|  
|<span data-ttu-id="c620b-262">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c620b-262">IS_NULLABLE</span></span>|<span data-ttu-id="c620b-263">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-263">String</span></span>|  
|<span data-ttu-id="c620b-264">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c620b-264">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="c620b-265">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-265">String</span></span>|  
|<span data-ttu-id="c620b-266">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c620b-266">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="c620b-267">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-267">String</span></span>|  
|<span data-ttu-id="c620b-268">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-268">SS_DATA_TYPE</span></span>|<span data-ttu-id="c620b-269">Byte</span><span class="sxs-lookup"><span data-stu-id="c620b-269">Byte</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="c620b-270">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="c620b-270">ProcedureParameters</span></span>  
  
|<span data-ttu-id="c620b-271">열 이름</span><span class="sxs-lookup"><span data-stu-id="c620b-271">ColumnName</span></span>|<span data-ttu-id="c620b-272">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c620b-272">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c620b-273">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="c620b-273">PROCEDURE_CAT</span></span>|<span data-ttu-id="c620b-274">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-274">String</span></span>|  
|<span data-ttu-id="c620b-275">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="c620b-275">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="c620b-276">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-276">String</span></span>|  
|<span data-ttu-id="c620b-277">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-277">PROCEDURE_NAME</span></span>|<span data-ttu-id="c620b-278">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-278">String</span></span>|  
|<span data-ttu-id="c620b-279">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-279">COLUMN_NAME</span></span>|<span data-ttu-id="c620b-280">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-280">String</span></span>|  
|<span data-ttu-id="c620b-281">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-281">COLUMN_TYPE</span></span>|<span data-ttu-id="c620b-282">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-282">Int16</span></span>|  
|<span data-ttu-id="c620b-283">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-283">DATA_TYPE</span></span>|<span data-ttu-id="c620b-284">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-284">Int16</span></span>|  
|<span data-ttu-id="c620b-285">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-285">TYPE_NAME</span></span>|<span data-ttu-id="c620b-286">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-286">String</span></span>|  
|<span data-ttu-id="c620b-287">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="c620b-287">COLUMN_SIZE</span></span>|<span data-ttu-id="c620b-288">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-288">Int32</span></span>|  
|<span data-ttu-id="c620b-289">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c620b-289">BUFFER_LENGTH</span></span>|<span data-ttu-id="c620b-290">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-290">Int32</span></span>|  
|<span data-ttu-id="c620b-291">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="c620b-291">DECIMAL_DIGITS</span></span>|<span data-ttu-id="c620b-292">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-292">Int16</span></span>|  
|<span data-ttu-id="c620b-293">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="c620b-293">NUM_PREC_RADIX</span></span>|<span data-ttu-id="c620b-294">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-294">Int16</span></span>|  
|<span data-ttu-id="c620b-295">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c620b-295">NULLABLE</span></span>|<span data-ttu-id="c620b-296">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-296">Int16</span></span>|  
|<span data-ttu-id="c620b-297">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c620b-297">REMARKS</span></span>|<span data-ttu-id="c620b-298">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-298">String</span></span>|  
|<span data-ttu-id="c620b-299">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="c620b-299">COLUMN_DEF</span></span>|<span data-ttu-id="c620b-300">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-300">String</span></span>|  
|<span data-ttu-id="c620b-301">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-301">SQL_DATA_TYPE</span></span>|<span data-ttu-id="c620b-302">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-302">Int16</span></span>|  
|<span data-ttu-id="c620b-303">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="c620b-303">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="c620b-304">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-304">Int16</span></span>|  
|<span data-ttu-id="c620b-305">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c620b-305">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="c620b-306">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-306">Int32</span></span>|  
|<span data-ttu-id="c620b-307">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c620b-307">ORDINAL_POSITION</span></span>|<span data-ttu-id="c620b-308">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-308">Int32</span></span>|  
|<span data-ttu-id="c620b-309">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c620b-309">IS_NULLABLE</span></span>|<span data-ttu-id="c620b-310">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-310">String</span></span>|  
|<span data-ttu-id="c620b-311">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c620b-311">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="c620b-312">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-312">String</span></span>|  
|<span data-ttu-id="c620b-313">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c620b-313">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="c620b-314">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-314">String</span></span>|  
|<span data-ttu-id="c620b-315">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-315">SS_DATA_TYPE</span></span>|<span data-ttu-id="c620b-316">Byte</span><span class="sxs-lookup"><span data-stu-id="c620b-316">Byte</span></span>|  
  
## <a name="microsoft-oracle-odbc-driver"></a><span data-ttu-id="c620b-317">Microsoft Oracle ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="c620b-317">Microsoft Oracle ODBC Driver</span></span>  
 <span data-ttu-id="c620b-318">Microsoft SQL Server Oracle ODBC Driver에서는 공통 스키마 컬렉션 외에도 다음과 같은 특정 스키마 컬렉션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c620b-318">The Microsoft SQL Server Oracle ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="c620b-319">Tables</span><span class="sxs-lookup"><span data-stu-id="c620b-319">Tables</span></span>  
  
-   <span data-ttu-id="c620b-320">Columns</span><span class="sxs-lookup"><span data-stu-id="c620b-320">Columns</span></span>  
  
-   <span data-ttu-id="c620b-321">절차</span><span class="sxs-lookup"><span data-stu-id="c620b-321">Procedures</span></span>  
  
-   <span data-ttu-id="c620b-322">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="c620b-322">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="c620b-323">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="c620b-323">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="c620b-324">뷰</span><span class="sxs-lookup"><span data-stu-id="c620b-324">Views</span></span>  
  
-   <span data-ttu-id="c620b-325">Indexes</span><span class="sxs-lookup"><span data-stu-id="c620b-325">Indexes</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="c620b-326">Tables 및 Views</span><span class="sxs-lookup"><span data-stu-id="c620b-326">Tables and Views</span></span>  
  
|<span data-ttu-id="c620b-327">열 이름</span><span class="sxs-lookup"><span data-stu-id="c620b-327">ColumnName</span></span>|<span data-ttu-id="c620b-328">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c620b-328">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c620b-329">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="c620b-329">TABLE_QUALIFIER</span></span>|<span data-ttu-id="c620b-330">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-330">String</span></span>|  
|<span data-ttu-id="c620b-331">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="c620b-331">TABLE_OWNER</span></span>|<span data-ttu-id="c620b-332">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-332">String</span></span>|  
|<span data-ttu-id="c620b-333">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-333">TABLE_NAME</span></span>|<span data-ttu-id="c620b-334">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-334">String</span></span>|  
|<span data-ttu-id="c620b-335">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-335">TABLE_TYPE</span></span>|<span data-ttu-id="c620b-336">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-336">String</span></span>|  
|<span data-ttu-id="c620b-337">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c620b-337">REMARKS</span></span>|<span data-ttu-id="c620b-338">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-338">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="c620b-339">Columns</span><span class="sxs-lookup"><span data-stu-id="c620b-339">Columns</span></span>  
  
|<span data-ttu-id="c620b-340">열 이름</span><span class="sxs-lookup"><span data-stu-id="c620b-340">ColumnName</span></span>|<span data-ttu-id="c620b-341">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c620b-341">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c620b-342">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="c620b-342">TABLE_QUALIFIER</span></span>|<span data-ttu-id="c620b-343">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-343">String</span></span>|  
|<span data-ttu-id="c620b-344">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="c620b-344">TABLE_OWNER</span></span>|<span data-ttu-id="c620b-345">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-345">String</span></span>|  
|<span data-ttu-id="c620b-346">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-346">TABLE_NAME</span></span>|<span data-ttu-id="c620b-347">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-347">String</span></span>|  
|<span data-ttu-id="c620b-348">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-348">COLUMN_NAME</span></span>|<span data-ttu-id="c620b-349">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-349">String</span></span>|  
|<span data-ttu-id="c620b-350">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-350">DATA_TYPE</span></span>|<span data-ttu-id="c620b-351">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-351">Int16</span></span>|  
|<span data-ttu-id="c620b-352">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-352">TYPE_NAME</span></span>|<span data-ttu-id="c620b-353">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-353">String</span></span>|  
|<span data-ttu-id="c620b-354">PRECISION</span><span class="sxs-lookup"><span data-stu-id="c620b-354">PRECISION</span></span>|<span data-ttu-id="c620b-355">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-355">Int32</span></span>|  
|<span data-ttu-id="c620b-356">LENGTH</span><span class="sxs-lookup"><span data-stu-id="c620b-356">LENGTH</span></span>|<span data-ttu-id="c620b-357">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-357">Int32</span></span>|  
|<span data-ttu-id="c620b-358">SCALE</span><span class="sxs-lookup"><span data-stu-id="c620b-358">SCALE</span></span>|<span data-ttu-id="c620b-359">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-359">Int16</span></span>|  
|<span data-ttu-id="c620b-360">RADIX</span><span class="sxs-lookup"><span data-stu-id="c620b-360">RADIX</span></span>|<span data-ttu-id="c620b-361">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-361">Int16</span></span>|  
|<span data-ttu-id="c620b-362">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c620b-362">NULLABLE</span></span>|<span data-ttu-id="c620b-363">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-363">Int16</span></span>|  
|<span data-ttu-id="c620b-364">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c620b-364">REMARKS</span></span>|<span data-ttu-id="c620b-365">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-365">String</span></span>|  
|<span data-ttu-id="c620b-366">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c620b-366">ORDINAL_POSITION</span></span>|<span data-ttu-id="c620b-367">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-367">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="c620b-368">절차</span><span class="sxs-lookup"><span data-stu-id="c620b-368">Procedures</span></span>  
  
|<span data-ttu-id="c620b-369">열 이름</span><span class="sxs-lookup"><span data-stu-id="c620b-369">ColumnName</span></span>|<span data-ttu-id="c620b-370">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c620b-370">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c620b-371">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="c620b-371">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="c620b-372">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-372">String</span></span>|  
|<span data-ttu-id="c620b-373">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="c620b-373">PROCEDURE_OWNER</span></span>|<span data-ttu-id="c620b-374">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-374">String</span></span>|  
|<span data-ttu-id="c620b-375">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-375">PROCEDURE_NAME</span></span>|<span data-ttu-id="c620b-376">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-376">String</span></span>|  
|<span data-ttu-id="c620b-377">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="c620b-377">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="c620b-378">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-378">Int16</span></span>|  
|<span data-ttu-id="c620b-379">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="c620b-379">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="c620b-380">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-380">Int16</span></span>|  
|<span data-ttu-id="c620b-381">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="c620b-381">NUM_RESULT_SETS</span></span>|<span data-ttu-id="c620b-382">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-382">Int16</span></span>|  
|<span data-ttu-id="c620b-383">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c620b-383">REMARKS</span></span>|<span data-ttu-id="c620b-384">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-384">String</span></span>|  
|<span data-ttu-id="c620b-385">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-385">PROCEDURE_TYPE</span></span>|<span data-ttu-id="c620b-386">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-386">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="c620b-387">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="c620b-387">ProcedureColumns</span></span>  
  
|<span data-ttu-id="c620b-388">열 이름</span><span class="sxs-lookup"><span data-stu-id="c620b-388">ColumnName</span></span>|<span data-ttu-id="c620b-389">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c620b-389">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c620b-390">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="c620b-390">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="c620b-391">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-391">String</span></span>|  
|<span data-ttu-id="c620b-392">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="c620b-392">PROCEDURE_OWNER</span></span>|<span data-ttu-id="c620b-393">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-393">String</span></span>|  
|<span data-ttu-id="c620b-394">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-394">PROCEDURE_NAME</span></span>|<span data-ttu-id="c620b-395">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-395">String</span></span>|  
|<span data-ttu-id="c620b-396">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-396">COLUMN_NAME</span></span>|<span data-ttu-id="c620b-397">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-397">String</span></span>|  
|<span data-ttu-id="c620b-398">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-398">COLUMN_TYPE</span></span>|<span data-ttu-id="c620b-399">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-399">Int16</span></span>|  
|<span data-ttu-id="c620b-400">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-400">DATA_TYPE</span></span>|<span data-ttu-id="c620b-401">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-401">Int16</span></span>|  
|<span data-ttu-id="c620b-402">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-402">TYPE_NAME</span></span>|<span data-ttu-id="c620b-403">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-403">String</span></span>|  
|<span data-ttu-id="c620b-404">PRECISION</span><span class="sxs-lookup"><span data-stu-id="c620b-404">PRECISION</span></span>|<span data-ttu-id="c620b-405">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-405">Int32</span></span>|  
|<span data-ttu-id="c620b-406">LENGTH</span><span class="sxs-lookup"><span data-stu-id="c620b-406">LENGTH</span></span>|<span data-ttu-id="c620b-407">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-407">Int32</span></span>|  
|<span data-ttu-id="c620b-408">SCALE</span><span class="sxs-lookup"><span data-stu-id="c620b-408">SCALE</span></span>|<span data-ttu-id="c620b-409">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-409">Int16</span></span>|  
|<span data-ttu-id="c620b-410">RADIX</span><span class="sxs-lookup"><span data-stu-id="c620b-410">RADIX</span></span>|<span data-ttu-id="c620b-411">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-411">Int16</span></span>|  
|<span data-ttu-id="c620b-412">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c620b-412">NULLABLE</span></span>|<span data-ttu-id="c620b-413">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-413">Int16</span></span>|  
|<span data-ttu-id="c620b-414">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c620b-414">REMARKS</span></span>|<span data-ttu-id="c620b-415">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-415">String</span></span>|  
|<span data-ttu-id="c620b-416">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="c620b-416">OVERLOAD</span></span>|<span data-ttu-id="c620b-417">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-417">Int32</span></span>|  
|<span data-ttu-id="c620b-418">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c620b-418">ORDINAL_POSITION</span></span>|<span data-ttu-id="c620b-419">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-419">Int32</span></span>|  
  
## <a name="microsoft-jet-odbc-driver"></a><span data-ttu-id="c620b-420">Microsoft Jet ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="c620b-420">Microsoft Jet ODBC Driver</span></span>  
 <span data-ttu-id="c620b-421">Microsoft Jet ODBC Driver                                             .</span><span class="sxs-lookup"><span data-stu-id="c620b-421">The Microsoft Jet ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="c620b-422">Tables</span><span class="sxs-lookup"><span data-stu-id="c620b-422">Tables</span></span>  
  
-   <span data-ttu-id="c620b-423">Indexes</span><span class="sxs-lookup"><span data-stu-id="c620b-423">Indexes</span></span>  
  
-   <span data-ttu-id="c620b-424">Columns</span><span class="sxs-lookup"><span data-stu-id="c620b-424">Columns</span></span>  
  
-   <span data-ttu-id="c620b-425">절차</span><span class="sxs-lookup"><span data-stu-id="c620b-425">Procedures</span></span>  
  
-   <span data-ttu-id="c620b-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="c620b-426">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="c620b-427">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="c620b-427">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="c620b-428">뷰</span><span class="sxs-lookup"><span data-stu-id="c620b-428">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="c620b-429">Tables 및 Views</span><span class="sxs-lookup"><span data-stu-id="c620b-429">Tables and Views</span></span>  
  
|<span data-ttu-id="c620b-430">열 이름</span><span class="sxs-lookup"><span data-stu-id="c620b-430">ColumnName</span></span>|<span data-ttu-id="c620b-431">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c620b-431">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c620b-432">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="c620b-432">TABLE_QUALIFIER</span></span>|<span data-ttu-id="c620b-433">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-433">String</span></span>|  
|<span data-ttu-id="c620b-434">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="c620b-434">TABLE_OWNER</span></span>|<span data-ttu-id="c620b-435">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-435">String</span></span>|  
|<span data-ttu-id="c620b-436">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-436">TABLE_NAME</span></span>|<span data-ttu-id="c620b-437">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-437">String</span></span>|  
|<span data-ttu-id="c620b-438">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-438">TABLE_TYPE</span></span>|<span data-ttu-id="c620b-439">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-439">String</span></span>|  
|<span data-ttu-id="c620b-440">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c620b-440">REMARKS</span></span>|<span data-ttu-id="c620b-441">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-441">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="c620b-442">Columns</span><span class="sxs-lookup"><span data-stu-id="c620b-442">Columns</span></span>  
  
|<span data-ttu-id="c620b-443">열 이름</span><span class="sxs-lookup"><span data-stu-id="c620b-443">ColumnName</span></span>|<span data-ttu-id="c620b-444">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c620b-444">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c620b-445">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="c620b-445">TABLE_QUALIFIER</span></span>|<span data-ttu-id="c620b-446">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-446">String</span></span>|  
|<span data-ttu-id="c620b-447">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="c620b-447">TABLE_OWNER</span></span>|<span data-ttu-id="c620b-448">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-448">String</span></span>|  
|<span data-ttu-id="c620b-449">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-449">TABLE_NAME</span></span>|<span data-ttu-id="c620b-450">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-450">String</span></span>|  
|<span data-ttu-id="c620b-451">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-451">COLUMN_NAME</span></span>|<span data-ttu-id="c620b-452">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-452">String</span></span>|  
|<span data-ttu-id="c620b-453">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-453">DATA_TYPE</span></span>|<span data-ttu-id="c620b-454">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-454">Int16</span></span>|  
|<span data-ttu-id="c620b-455">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-455">TYPE_NAME</span></span>|<span data-ttu-id="c620b-456">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-456">String</span></span>|  
|<span data-ttu-id="c620b-457">PRECISION</span><span class="sxs-lookup"><span data-stu-id="c620b-457">PRECISION</span></span>|<span data-ttu-id="c620b-458">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-458">Int32</span></span>|  
|<span data-ttu-id="c620b-459">LENGTH</span><span class="sxs-lookup"><span data-stu-id="c620b-459">LENGTH</span></span>|<span data-ttu-id="c620b-460">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-460">Int32</span></span>|  
|<span data-ttu-id="c620b-461">SCALE</span><span class="sxs-lookup"><span data-stu-id="c620b-461">SCALE</span></span>|<span data-ttu-id="c620b-462">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-462">Int16</span></span>|  
|<span data-ttu-id="c620b-463">RADIX</span><span class="sxs-lookup"><span data-stu-id="c620b-463">RADIX</span></span>|<span data-ttu-id="c620b-464">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-464">Int16</span></span>|  
|<span data-ttu-id="c620b-465">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c620b-465">NULLABLE</span></span>|<span data-ttu-id="c620b-466">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-466">Int16</span></span>|  
|<span data-ttu-id="c620b-467">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c620b-467">REMARKS</span></span>|<span data-ttu-id="c620b-468">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-468">String</span></span>|  
|<span data-ttu-id="c620b-469">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c620b-469">ORDINAL_POSITION</span></span>|<span data-ttu-id="c620b-470">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-470">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="c620b-471">절차</span><span class="sxs-lookup"><span data-stu-id="c620b-471">Procedures</span></span>  
  
|<span data-ttu-id="c620b-472">열 이름</span><span class="sxs-lookup"><span data-stu-id="c620b-472">ColumnName</span></span>|<span data-ttu-id="c620b-473">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c620b-473">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c620b-474">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="c620b-474">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="c620b-475">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-475">String</span></span>|  
|<span data-ttu-id="c620b-476">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="c620b-476">PROCEDURE_OWNER</span></span>|<span data-ttu-id="c620b-477">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-477">String</span></span>|  
|<span data-ttu-id="c620b-478">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-478">PROCEDURE_NAME</span></span>|<span data-ttu-id="c620b-479">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-479">String</span></span>|  
|<span data-ttu-id="c620b-480">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="c620b-480">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="c620b-481">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-481">Int16</span></span>|  
|<span data-ttu-id="c620b-482">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="c620b-482">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="c620b-483">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-483">Int16</span></span>|  
|<span data-ttu-id="c620b-484">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="c620b-484">NUM_RESULT_SETS</span></span>|<span data-ttu-id="c620b-485">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-485">Int16</span></span>|  
|<span data-ttu-id="c620b-486">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c620b-486">REMARKS</span></span>|<span data-ttu-id="c620b-487">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-487">String</span></span>|  
|<span data-ttu-id="c620b-488">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-488">PROCEDURE_TYPE</span></span>|<span data-ttu-id="c620b-489">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-489">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="c620b-490">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="c620b-490">ProcedureColumns</span></span>  
  
|<span data-ttu-id="c620b-491">열 이름</span><span class="sxs-lookup"><span data-stu-id="c620b-491">ColumnName</span></span>|<span data-ttu-id="c620b-492">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c620b-492">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c620b-493">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="c620b-493">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="c620b-494">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-494">String</span></span>|  
|<span data-ttu-id="c620b-495">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="c620b-495">PROCEDURE_OWNER</span></span>|<span data-ttu-id="c620b-496">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-496">String</span></span>|  
|<span data-ttu-id="c620b-497">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-497">PROCEDURE_NAME</span></span>|<span data-ttu-id="c620b-498">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-498">String</span></span>|  
|<span data-ttu-id="c620b-499">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-499">COLUMN_NAME</span></span>|<span data-ttu-id="c620b-500">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-500">String</span></span>|  
|<span data-ttu-id="c620b-501">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-501">COLUMN_TYPE</span></span>|<span data-ttu-id="c620b-502">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-502">Int16</span></span>|  
|<span data-ttu-id="c620b-503">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-503">DATA_TYPE</span></span>|<span data-ttu-id="c620b-504">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-504">Int16</span></span>|  
|<span data-ttu-id="c620b-505">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-505">TYPE_NAME</span></span>|<span data-ttu-id="c620b-506">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-506">String</span></span>|  
|<span data-ttu-id="c620b-507">PRECISION</span><span class="sxs-lookup"><span data-stu-id="c620b-507">PRECISION</span></span>|<span data-ttu-id="c620b-508">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-508">Int32</span></span>|  
|<span data-ttu-id="c620b-509">LENGTH</span><span class="sxs-lookup"><span data-stu-id="c620b-509">LENGTH</span></span>|<span data-ttu-id="c620b-510">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-510">Int32</span></span>|  
|<span data-ttu-id="c620b-511">SCALE</span><span class="sxs-lookup"><span data-stu-id="c620b-511">SCALE</span></span>|<span data-ttu-id="c620b-512">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-512">Int16</span></span>|  
|<span data-ttu-id="c620b-513">RADIX</span><span class="sxs-lookup"><span data-stu-id="c620b-513">RADIX</span></span>|<span data-ttu-id="c620b-514">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-514">Int16</span></span>|  
|<span data-ttu-id="c620b-515">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c620b-515">NULLABLE</span></span>|<span data-ttu-id="c620b-516">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-516">Int16</span></span>|  
|<span data-ttu-id="c620b-517">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c620b-517">REMARKS</span></span>|<span data-ttu-id="c620b-518">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-518">String</span></span>|  
|<span data-ttu-id="c620b-519">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="c620b-519">OVERLOAD</span></span>|<span data-ttu-id="c620b-520">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-520">Int32</span></span>|  
|<span data-ttu-id="c620b-521">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c620b-521">ORDINAL_POSITION</span></span>|<span data-ttu-id="c620b-522">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-522">Int32</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="c620b-523">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="c620b-523">ProcedureParameters</span></span>  
  
|<span data-ttu-id="c620b-524">열 이름</span><span class="sxs-lookup"><span data-stu-id="c620b-524">ColumnName</span></span>|<span data-ttu-id="c620b-525">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c620b-525">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c620b-526">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="c620b-526">PROCEDURE_CAT</span></span>|<span data-ttu-id="c620b-527">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-527">String</span></span>|  
|<span data-ttu-id="c620b-528">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="c620b-528">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="c620b-529">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-529">String</span></span>|  
|<span data-ttu-id="c620b-530">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-530">PROCEDURE_NAME</span></span>|<span data-ttu-id="c620b-531">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-531">String</span></span>|  
|<span data-ttu-id="c620b-532">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-532">COLUMN_NAME</span></span>|<span data-ttu-id="c620b-533">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-533">String</span></span>|  
|<span data-ttu-id="c620b-534">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-534">COLUMN_TYPE</span></span>|<span data-ttu-id="c620b-535">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-535">Int16</span></span>|  
|<span data-ttu-id="c620b-536">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-536">DATA_TYPE</span></span>|<span data-ttu-id="c620b-537">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-537">Int16</span></span>|  
|<span data-ttu-id="c620b-538">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c620b-538">TYPE_NAME</span></span>|<span data-ttu-id="c620b-539">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-539">String</span></span>|  
|<span data-ttu-id="c620b-540">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="c620b-540">COLUMN_SIZE</span></span>|<span data-ttu-id="c620b-541">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-541">Int32</span></span>|  
|<span data-ttu-id="c620b-542">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c620b-542">BUFFER_LENGTH</span></span>|<span data-ttu-id="c620b-543">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-543">Int32</span></span>|  
|<span data-ttu-id="c620b-544">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="c620b-544">DECIMAL_DIGITS</span></span>|<span data-ttu-id="c620b-545">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-545">Int16</span></span>|  
|<span data-ttu-id="c620b-546">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="c620b-546">NUM_PREC_RADIX</span></span>|<span data-ttu-id="c620b-547">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-547">Int16</span></span>|  
|<span data-ttu-id="c620b-548">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c620b-548">NULLABLE</span></span>|<span data-ttu-id="c620b-549">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-549">Int16</span></span>|  
|<span data-ttu-id="c620b-550">REMARKS</span><span class="sxs-lookup"><span data-stu-id="c620b-550">REMARKS</span></span>|<span data-ttu-id="c620b-551">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-551">String</span></span>|  
|<span data-ttu-id="c620b-552">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="c620b-552">COLUMN_DEF</span></span>|<span data-ttu-id="c620b-553">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-553">String</span></span>|  
|<span data-ttu-id="c620b-554">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c620b-554">SQL_DATA_TYPE</span></span>|<span data-ttu-id="c620b-555">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-555">Int16</span></span>|  
|<span data-ttu-id="c620b-556">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="c620b-556">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="c620b-557">Int16</span><span class="sxs-lookup"><span data-stu-id="c620b-557">Int16</span></span>|  
|<span data-ttu-id="c620b-558">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c620b-558">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="c620b-559">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-559">Int32</span></span>|  
|<span data-ttu-id="c620b-560">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c620b-560">ORDINAL_POSITION</span></span>|<span data-ttu-id="c620b-561">Int32</span><span class="sxs-lookup"><span data-stu-id="c620b-561">Int32</span></span>|  
|<span data-ttu-id="c620b-562">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c620b-562">IS_NULLABLE</span></span>|<span data-ttu-id="c620b-563">문자열</span><span class="sxs-lookup"><span data-stu-id="c620b-563">String</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c620b-564">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c620b-564">See Also</span></span>  
 [<span data-ttu-id="c620b-565">ADO.NET 관리되는 공급자 및 데이터 집합 개발자 센터</span><span class="sxs-lookup"><span data-stu-id="c620b-565">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
