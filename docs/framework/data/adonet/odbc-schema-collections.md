---
title: ODBC 스키마 컬렉션
ms.date: 03/30/2017
ms.assetid: 1bb126a5-ceec-4649-a4bc-8aa19e801046
ms.openlocfilehash: bdedbb11960f02b99dcca6388abf663635238f74
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43877533"
---
# <a name="odbc-schema-collections"></a><span data-ttu-id="0eed4-102">ODBC 스키마 컬렉션</span><span class="sxs-lookup"><span data-stu-id="0eed4-102">ODBC Schema Collections</span></span>
<span data-ttu-id="0eed4-103">이 단원에서는 Microsoft SQL Server, Oracle 및 Microsoft Jet용 ODBC 드라이버에서 지원하는 스키마 컬렉션에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="0eed4-103">This section discusses schema collection support for the ODBC drivers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-odbc-driver"></a><span data-ttu-id="0eed4-104">Microsoft SQL Server ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="0eed4-104">Microsoft SQL Server ODBC Driver</span></span>  
 <span data-ttu-id="0eed4-105">Microsoft SQL Server ODBC Driver에서는 공통 스키마 컬렉션 외에도 다음과 같은 특정 스키마 컬렉션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0eed4-105">The Microsoft SQL Server ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="0eed4-106">Tables</span><span class="sxs-lookup"><span data-stu-id="0eed4-106">Tables</span></span>  
  
-   <span data-ttu-id="0eed4-107">Indexes</span><span class="sxs-lookup"><span data-stu-id="0eed4-107">Indexes</span></span>  
  
-   <span data-ttu-id="0eed4-108">Columns</span><span class="sxs-lookup"><span data-stu-id="0eed4-108">Columns</span></span>  
  
-   <span data-ttu-id="0eed4-109">절차</span><span class="sxs-lookup"><span data-stu-id="0eed4-109">Procedures</span></span>  
  
-   <span data-ttu-id="0eed4-110">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="0eed4-110">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="0eed4-111">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="0eed4-111">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="0eed4-112">뷰</span><span class="sxs-lookup"><span data-stu-id="0eed4-112">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="0eed4-113">Tables 및 Views</span><span class="sxs-lookup"><span data-stu-id="0eed4-113">Tables and Views</span></span>  
  
|<span data-ttu-id="0eed4-114">열 이름</span><span class="sxs-lookup"><span data-stu-id="0eed4-114">ColumnName</span></span>|<span data-ttu-id="0eed4-115">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="0eed4-115">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0eed4-116">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="0eed4-116">TABLE_CAT</span></span>|<span data-ttu-id="0eed4-117">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-117">String</span></span>|  
|<span data-ttu-id="0eed4-118">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="0eed4-118">TABLE_SCHEM</span></span>|<span data-ttu-id="0eed4-119">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-119">String</span></span>|  
|<span data-ttu-id="0eed4-120">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-120">TABLE_NAME</span></span>|<span data-ttu-id="0eed4-121">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-121">String</span></span>|  
|<span data-ttu-id="0eed4-122">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-122">TABLE_TYPE</span></span>|<span data-ttu-id="0eed4-123">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-123">String</span></span>|  
|<span data-ttu-id="0eed4-124">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0eed4-124">REMARKS</span></span>|<span data-ttu-id="0eed4-125">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-125">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="0eed4-126">Indexes</span><span class="sxs-lookup"><span data-stu-id="0eed4-126">Indexes</span></span>  
  
|<span data-ttu-id="0eed4-127">열 이름</span><span class="sxs-lookup"><span data-stu-id="0eed4-127">ColumnName</span></span>|<span data-ttu-id="0eed4-128">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="0eed4-128">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0eed4-129">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="0eed4-129">TABLE_CAT</span></span>|<span data-ttu-id="0eed4-130">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-130">String</span></span>|  
|<span data-ttu-id="0eed4-131">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="0eed4-131">TABLE_SCHEM</span></span>|<span data-ttu-id="0eed4-132">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-132">String</span></span>|  
|<span data-ttu-id="0eed4-133">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-133">TABLE_NAME</span></span>|<span data-ttu-id="0eed4-134">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-134">String</span></span>|  
|<span data-ttu-id="0eed4-135">NON_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="0eed4-135">NON_UNIQUE</span></span>|<span data-ttu-id="0eed4-136">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-136">Int16</span></span>|  
|<span data-ttu-id="0eed4-137">INDEX_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="0eed4-137">INDEX_QUALIFIER</span></span>|<span data-ttu-id="0eed4-138">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-138">String</span></span>|  
|<span data-ttu-id="0eed4-139">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-139">INDEX_NAME</span></span>|<span data-ttu-id="0eed4-140">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-140">String</span></span>|  
|<span data-ttu-id="0eed4-141">TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-141">TYPE</span></span>|<span data-ttu-id="0eed4-142">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-142">Int16</span></span>|  
|<span data-ttu-id="0eed4-143">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0eed4-143">ORDINAL_POSITION</span></span>|<span data-ttu-id="0eed4-144">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-144">Int16</span></span>|  
|<span data-ttu-id="0eed4-145">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-145">COLUMN_NAME</span></span>|<span data-ttu-id="0eed4-146">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-146">String</span></span>|  
|<span data-ttu-id="0eed4-147">ASC_OR_DESC</span><span class="sxs-lookup"><span data-stu-id="0eed4-147">ASC_OR_DESC</span></span>|<span data-ttu-id="0eed4-148">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-148">String</span></span>|  
|<span data-ttu-id="0eed4-149">CARDINATLITY</span><span class="sxs-lookup"><span data-stu-id="0eed4-149">CARDINATLITY</span></span>|<span data-ttu-id="0eed4-150">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-150">Int32</span></span>|  
|<span data-ttu-id="0eed4-151">PAGES</span><span class="sxs-lookup"><span data-stu-id="0eed4-151">PAGES</span></span>|<span data-ttu-id="0eed4-152">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-152">Int32</span></span>|  
|<span data-ttu-id="0eed4-153">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="0eed4-153">FILTER_CONDITION</span></span>|<span data-ttu-id="0eed4-154">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-154">String</span></span>|  
|<span data-ttu-id="0eed4-155">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0eed4-155">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="0eed4-156">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-156">String</span></span>|  
|<span data-ttu-id="0eed4-157">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-157">SS_DATA_TYPE</span></span>|<span data-ttu-id="0eed4-158">Byte</span><span class="sxs-lookup"><span data-stu-id="0eed4-158">Byte</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="0eed4-159">Columns</span><span class="sxs-lookup"><span data-stu-id="0eed4-159">Columns</span></span>  
  
|<span data-ttu-id="0eed4-160">열 이름</span><span class="sxs-lookup"><span data-stu-id="0eed4-160">ColumnName</span></span>|<span data-ttu-id="0eed4-161">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="0eed4-161">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0eed4-162">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="0eed4-162">TABLE_CAT</span></span>|<span data-ttu-id="0eed4-163">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-163">String</span></span>|  
|<span data-ttu-id="0eed4-164">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="0eed4-164">TABLE_SCHEM</span></span>|<span data-ttu-id="0eed4-165">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-165">String</span></span>|  
|<span data-ttu-id="0eed4-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-166">TABLE_NAME</span></span>|<span data-ttu-id="0eed4-167">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-167">String</span></span>|  
|<span data-ttu-id="0eed4-168">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-168">COLUMN_NAME</span></span>|<span data-ttu-id="0eed4-169">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-169">String</span></span>|  
|<span data-ttu-id="0eed4-170">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-170">DATA_TYPE</span></span>|<span data-ttu-id="0eed4-171">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-171">Int16</span></span>|  
|<span data-ttu-id="0eed4-172">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-172">TYPE_NAME</span></span>|<span data-ttu-id="0eed4-173">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-173">String</span></span>|  
|<span data-ttu-id="0eed4-174">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="0eed4-174">COLUMN_SIZE</span></span>|<span data-ttu-id="0eed4-175">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-175">Int32</span></span>|  
|<span data-ttu-id="0eed4-176">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0eed4-176">BUFFER_LENGTH</span></span>|<span data-ttu-id="0eed4-177">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-177">Int32</span></span>|  
|<span data-ttu-id="0eed4-178">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="0eed4-178">DECIMAL_DIGITS</span></span>|<span data-ttu-id="0eed4-179">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-179">Int16</span></span>|  
|<span data-ttu-id="0eed4-180">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="0eed4-180">NUM_PREC_RADIX</span></span>|<span data-ttu-id="0eed4-181">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-181">Int16</span></span>|  
|<span data-ttu-id="0eed4-182">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0eed4-182">NULLABLE</span></span>|<span data-ttu-id="0eed4-183">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-183">Int16</span></span>|  
|<span data-ttu-id="0eed4-184">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0eed4-184">REMARKS</span></span>|<span data-ttu-id="0eed4-185">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-185">String</span></span>|  
|<span data-ttu-id="0eed4-186">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="0eed4-186">COLUMN_DEF</span></span>|<span data-ttu-id="0eed4-187">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-187">String</span></span>|  
|<span data-ttu-id="0eed4-188">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-188">SQL_DATA_TYPE</span></span>|<span data-ttu-id="0eed4-189">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-189">Int16</span></span>|  
|<span data-ttu-id="0eed4-190">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="0eed4-190">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="0eed4-191">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-191">Int16</span></span>|  
|<span data-ttu-id="0eed4-192">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0eed4-192">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="0eed4-193">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-193">Int32</span></span>|  
|<span data-ttu-id="0eed4-194">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0eed4-194">ORDINAL_POSITION</span></span>|<span data-ttu-id="0eed4-195">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-195">Int32</span></span>|  
|<span data-ttu-id="0eed4-196">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0eed4-196">IS_NULLABLE</span></span>|<span data-ttu-id="0eed4-197">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-197">String</span></span>|  
|<span data-ttu-id="0eed4-198">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0eed4-198">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="0eed4-199">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-199">String</span></span>|  
|<span data-ttu-id="0eed4-200">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0eed4-200">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="0eed4-201">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-201">String</span></span>|  
|<span data-ttu-id="0eed4-202">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-202">SS_DATA_TYPE</span></span>|<span data-ttu-id="0eed4-203">Byte</span><span class="sxs-lookup"><span data-stu-id="0eed4-203">Byte</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="0eed4-204">절차</span><span class="sxs-lookup"><span data-stu-id="0eed4-204">Procedures</span></span>  
  
|<span data-ttu-id="0eed4-205">열 이름</span><span class="sxs-lookup"><span data-stu-id="0eed4-205">ColumnName</span></span>|<span data-ttu-id="0eed4-206">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="0eed4-206">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0eed4-207">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="0eed4-207">PROCEDURE_CAT</span></span>|<span data-ttu-id="0eed4-208">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-208">String</span></span>|  
|<span data-ttu-id="0eed4-209">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="0eed4-209">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="0eed4-210">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-210">String</span></span>|  
|<span data-ttu-id="0eed4-211">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-211">PROCEDURE_NAME</span></span>|<span data-ttu-id="0eed4-212">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-212">String</span></span>|  
|<span data-ttu-id="0eed4-213">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="0eed4-213">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="0eed4-214">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-214">Int32</span></span>|  
|<span data-ttu-id="0eed4-215">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="0eed4-215">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="0eed4-216">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-216">Int32</span></span>|  
|<span data-ttu-id="0eed4-217">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="0eed4-217">NUM_RESULT_SETS</span></span>|<span data-ttu-id="0eed4-218">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-218">Int32</span></span>|  
|<span data-ttu-id="0eed4-219">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0eed4-219">REMARKS</span></span>|<span data-ttu-id="0eed4-220">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-220">String</span></span>|  
|<span data-ttu-id="0eed4-221">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-221">PROCEDURE_TYPE</span></span>|<span data-ttu-id="0eed4-222">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-222">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="0eed4-223">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="0eed4-223">ProcedureColumns</span></span>  
  
|<span data-ttu-id="0eed4-224">열 이름</span><span class="sxs-lookup"><span data-stu-id="0eed4-224">ColumnName</span></span>|<span data-ttu-id="0eed4-225">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="0eed4-225">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0eed4-226">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="0eed4-226">PROCEDURE_CAT</span></span>|<span data-ttu-id="0eed4-227">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-227">String</span></span>|  
|<span data-ttu-id="0eed4-228">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="0eed4-228">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="0eed4-229">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-229">String</span></span>|  
|<span data-ttu-id="0eed4-230">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-230">PROCEDURE_NAME</span></span>|<span data-ttu-id="0eed4-231">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-231">String</span></span>|  
|<span data-ttu-id="0eed4-232">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-232">COLUMN_NAME</span></span>|<span data-ttu-id="0eed4-233">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-233">String</span></span>|  
|<span data-ttu-id="0eed4-234">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-234">COLUMN_TYPE</span></span>|<span data-ttu-id="0eed4-235">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-235">Int16</span></span>|  
|<span data-ttu-id="0eed4-236">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-236">DATA_TYPE</span></span>|<span data-ttu-id="0eed4-237">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-237">Int16</span></span>|  
|<span data-ttu-id="0eed4-238">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-238">TYPE_NAME</span></span>|<span data-ttu-id="0eed4-239">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-239">String</span></span>|  
|<span data-ttu-id="0eed4-240">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="0eed4-240">COLUMN_SIZE</span></span>|<span data-ttu-id="0eed4-241">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-241">Int32</span></span>|  
|<span data-ttu-id="0eed4-242">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0eed4-242">BUFFER_LENGTH</span></span>|<span data-ttu-id="0eed4-243">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-243">Int32</span></span>|  
|<span data-ttu-id="0eed4-244">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="0eed4-244">DECIMAL_DIGITS</span></span>|<span data-ttu-id="0eed4-245">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-245">Int16</span></span>|  
|<span data-ttu-id="0eed4-246">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="0eed4-246">NUM_PREC_RADIX</span></span>|<span data-ttu-id="0eed4-247">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-247">Int16</span></span>|  
|<span data-ttu-id="0eed4-248">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0eed4-248">NULLABLE</span></span>|<span data-ttu-id="0eed4-249">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-249">Int16</span></span>|  
|<span data-ttu-id="0eed4-250">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0eed4-250">REMARKS</span></span>|<span data-ttu-id="0eed4-251">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-251">String</span></span>|  
|<span data-ttu-id="0eed4-252">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="0eed4-252">COLUMN_DEF</span></span>|<span data-ttu-id="0eed4-253">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-253">String</span></span>|  
|<span data-ttu-id="0eed4-254">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-254">SQL_DATA_TYPE</span></span>|<span data-ttu-id="0eed4-255">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-255">Int16</span></span>|  
|<span data-ttu-id="0eed4-256">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="0eed4-256">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="0eed4-257">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-257">Int16</span></span>|  
|<span data-ttu-id="0eed4-258">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0eed4-258">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="0eed4-259">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-259">Int32</span></span>|  
|<span data-ttu-id="0eed4-260">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0eed4-260">ORDINAL_POSITION</span></span>|<span data-ttu-id="0eed4-261">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-261">Int32</span></span>|  
|<span data-ttu-id="0eed4-262">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0eed4-262">IS_NULLABLE</span></span>|<span data-ttu-id="0eed4-263">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-263">String</span></span>|  
|<span data-ttu-id="0eed4-264">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0eed4-264">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="0eed4-265">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-265">String</span></span>|  
|<span data-ttu-id="0eed4-266">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0eed4-266">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="0eed4-267">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-267">String</span></span>|  
|<span data-ttu-id="0eed4-268">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-268">SS_DATA_TYPE</span></span>|<span data-ttu-id="0eed4-269">Byte</span><span class="sxs-lookup"><span data-stu-id="0eed4-269">Byte</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="0eed4-270">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="0eed4-270">ProcedureParameters</span></span>  
  
|<span data-ttu-id="0eed4-271">열 이름</span><span class="sxs-lookup"><span data-stu-id="0eed4-271">ColumnName</span></span>|<span data-ttu-id="0eed4-272">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="0eed4-272">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0eed4-273">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="0eed4-273">PROCEDURE_CAT</span></span>|<span data-ttu-id="0eed4-274">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-274">String</span></span>|  
|<span data-ttu-id="0eed4-275">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="0eed4-275">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="0eed4-276">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-276">String</span></span>|  
|<span data-ttu-id="0eed4-277">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-277">PROCEDURE_NAME</span></span>|<span data-ttu-id="0eed4-278">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-278">String</span></span>|  
|<span data-ttu-id="0eed4-279">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-279">COLUMN_NAME</span></span>|<span data-ttu-id="0eed4-280">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-280">String</span></span>|  
|<span data-ttu-id="0eed4-281">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-281">COLUMN_TYPE</span></span>|<span data-ttu-id="0eed4-282">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-282">Int16</span></span>|  
|<span data-ttu-id="0eed4-283">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-283">DATA_TYPE</span></span>|<span data-ttu-id="0eed4-284">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-284">Int16</span></span>|  
|<span data-ttu-id="0eed4-285">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-285">TYPE_NAME</span></span>|<span data-ttu-id="0eed4-286">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-286">String</span></span>|  
|<span data-ttu-id="0eed4-287">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="0eed4-287">COLUMN_SIZE</span></span>|<span data-ttu-id="0eed4-288">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-288">Int32</span></span>|  
|<span data-ttu-id="0eed4-289">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0eed4-289">BUFFER_LENGTH</span></span>|<span data-ttu-id="0eed4-290">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-290">Int32</span></span>|  
|<span data-ttu-id="0eed4-291">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="0eed4-291">DECIMAL_DIGITS</span></span>|<span data-ttu-id="0eed4-292">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-292">Int16</span></span>|  
|<span data-ttu-id="0eed4-293">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="0eed4-293">NUM_PREC_RADIX</span></span>|<span data-ttu-id="0eed4-294">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-294">Int16</span></span>|  
|<span data-ttu-id="0eed4-295">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0eed4-295">NULLABLE</span></span>|<span data-ttu-id="0eed4-296">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-296">Int16</span></span>|  
|<span data-ttu-id="0eed4-297">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0eed4-297">REMARKS</span></span>|<span data-ttu-id="0eed4-298">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-298">String</span></span>|  
|<span data-ttu-id="0eed4-299">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="0eed4-299">COLUMN_DEF</span></span>|<span data-ttu-id="0eed4-300">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-300">String</span></span>|  
|<span data-ttu-id="0eed4-301">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-301">SQL_DATA_TYPE</span></span>|<span data-ttu-id="0eed4-302">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-302">Int16</span></span>|  
|<span data-ttu-id="0eed4-303">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="0eed4-303">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="0eed4-304">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-304">Int16</span></span>|  
|<span data-ttu-id="0eed4-305">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0eed4-305">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="0eed4-306">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-306">Int32</span></span>|  
|<span data-ttu-id="0eed4-307">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0eed4-307">ORDINAL_POSITION</span></span>|<span data-ttu-id="0eed4-308">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-308">Int32</span></span>|  
|<span data-ttu-id="0eed4-309">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0eed4-309">IS_NULLABLE</span></span>|<span data-ttu-id="0eed4-310">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-310">String</span></span>|  
|<span data-ttu-id="0eed4-311">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="0eed4-311">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="0eed4-312">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-312">String</span></span>|  
|<span data-ttu-id="0eed4-313">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0eed4-313">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="0eed4-314">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-314">String</span></span>|  
|<span data-ttu-id="0eed4-315">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-315">SS_DATA_TYPE</span></span>|<span data-ttu-id="0eed4-316">Byte</span><span class="sxs-lookup"><span data-stu-id="0eed4-316">Byte</span></span>|  
  
## <a name="microsoft-oracle-odbc-driver"></a><span data-ttu-id="0eed4-317">Microsoft Oracle ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="0eed4-317">Microsoft Oracle ODBC Driver</span></span>  
 <span data-ttu-id="0eed4-318">Microsoft SQL Server Oracle ODBC Driver에서는 공통 스키마 컬렉션 외에도 다음과 같은 특정 스키마 컬렉션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0eed4-318">The Microsoft SQL Server Oracle ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="0eed4-319">Tables</span><span class="sxs-lookup"><span data-stu-id="0eed4-319">Tables</span></span>  
  
-   <span data-ttu-id="0eed4-320">Columns</span><span class="sxs-lookup"><span data-stu-id="0eed4-320">Columns</span></span>  
  
-   <span data-ttu-id="0eed4-321">절차</span><span class="sxs-lookup"><span data-stu-id="0eed4-321">Procedures</span></span>  
  
-   <span data-ttu-id="0eed4-322">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="0eed4-322">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="0eed4-323">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="0eed4-323">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="0eed4-324">뷰</span><span class="sxs-lookup"><span data-stu-id="0eed4-324">Views</span></span>  
  
-   <span data-ttu-id="0eed4-325">Indexes</span><span class="sxs-lookup"><span data-stu-id="0eed4-325">Indexes</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="0eed4-326">Tables 및 Views</span><span class="sxs-lookup"><span data-stu-id="0eed4-326">Tables and Views</span></span>  
  
|<span data-ttu-id="0eed4-327">열 이름</span><span class="sxs-lookup"><span data-stu-id="0eed4-327">ColumnName</span></span>|<span data-ttu-id="0eed4-328">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="0eed4-328">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0eed4-329">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="0eed4-329">TABLE_QUALIFIER</span></span>|<span data-ttu-id="0eed4-330">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-330">String</span></span>|  
|<span data-ttu-id="0eed4-331">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="0eed4-331">TABLE_OWNER</span></span>|<span data-ttu-id="0eed4-332">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-332">String</span></span>|  
|<span data-ttu-id="0eed4-333">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-333">TABLE_NAME</span></span>|<span data-ttu-id="0eed4-334">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-334">String</span></span>|  
|<span data-ttu-id="0eed4-335">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-335">TABLE_TYPE</span></span>|<span data-ttu-id="0eed4-336">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-336">String</span></span>|  
|<span data-ttu-id="0eed4-337">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0eed4-337">REMARKS</span></span>|<span data-ttu-id="0eed4-338">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-338">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="0eed4-339">Columns</span><span class="sxs-lookup"><span data-stu-id="0eed4-339">Columns</span></span>  
  
|<span data-ttu-id="0eed4-340">열 이름</span><span class="sxs-lookup"><span data-stu-id="0eed4-340">ColumnName</span></span>|<span data-ttu-id="0eed4-341">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="0eed4-341">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0eed4-342">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="0eed4-342">TABLE_QUALIFIER</span></span>|<span data-ttu-id="0eed4-343">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-343">String</span></span>|  
|<span data-ttu-id="0eed4-344">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="0eed4-344">TABLE_OWNER</span></span>|<span data-ttu-id="0eed4-345">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-345">String</span></span>|  
|<span data-ttu-id="0eed4-346">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-346">TABLE_NAME</span></span>|<span data-ttu-id="0eed4-347">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-347">String</span></span>|  
|<span data-ttu-id="0eed4-348">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-348">COLUMN_NAME</span></span>|<span data-ttu-id="0eed4-349">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-349">String</span></span>|  
|<span data-ttu-id="0eed4-350">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-350">DATA_TYPE</span></span>|<span data-ttu-id="0eed4-351">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-351">Int16</span></span>|  
|<span data-ttu-id="0eed4-352">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-352">TYPE_NAME</span></span>|<span data-ttu-id="0eed4-353">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-353">String</span></span>|  
|<span data-ttu-id="0eed4-354">PRECISION</span><span class="sxs-lookup"><span data-stu-id="0eed4-354">PRECISION</span></span>|<span data-ttu-id="0eed4-355">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-355">Int32</span></span>|  
|<span data-ttu-id="0eed4-356">LENGTH</span><span class="sxs-lookup"><span data-stu-id="0eed4-356">LENGTH</span></span>|<span data-ttu-id="0eed4-357">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-357">Int32</span></span>|  
|<span data-ttu-id="0eed4-358">SCALE</span><span class="sxs-lookup"><span data-stu-id="0eed4-358">SCALE</span></span>|<span data-ttu-id="0eed4-359">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-359">Int16</span></span>|  
|<span data-ttu-id="0eed4-360">RADIX</span><span class="sxs-lookup"><span data-stu-id="0eed4-360">RADIX</span></span>|<span data-ttu-id="0eed4-361">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-361">Int16</span></span>|  
|<span data-ttu-id="0eed4-362">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0eed4-362">NULLABLE</span></span>|<span data-ttu-id="0eed4-363">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-363">Int16</span></span>|  
|<span data-ttu-id="0eed4-364">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0eed4-364">REMARKS</span></span>|<span data-ttu-id="0eed4-365">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-365">String</span></span>|  
|<span data-ttu-id="0eed4-366">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0eed4-366">ORDINAL_POSITION</span></span>|<span data-ttu-id="0eed4-367">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-367">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="0eed4-368">절차</span><span class="sxs-lookup"><span data-stu-id="0eed4-368">Procedures</span></span>  
  
|<span data-ttu-id="0eed4-369">열 이름</span><span class="sxs-lookup"><span data-stu-id="0eed4-369">ColumnName</span></span>|<span data-ttu-id="0eed4-370">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="0eed4-370">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0eed4-371">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="0eed4-371">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="0eed4-372">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-372">String</span></span>|  
|<span data-ttu-id="0eed4-373">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="0eed4-373">PROCEDURE_OWNER</span></span>|<span data-ttu-id="0eed4-374">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-374">String</span></span>|  
|<span data-ttu-id="0eed4-375">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-375">PROCEDURE_NAME</span></span>|<span data-ttu-id="0eed4-376">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-376">String</span></span>|  
|<span data-ttu-id="0eed4-377">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="0eed4-377">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="0eed4-378">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-378">Int16</span></span>|  
|<span data-ttu-id="0eed4-379">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="0eed4-379">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="0eed4-380">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-380">Int16</span></span>|  
|<span data-ttu-id="0eed4-381">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="0eed4-381">NUM_RESULT_SETS</span></span>|<span data-ttu-id="0eed4-382">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-382">Int16</span></span>|  
|<span data-ttu-id="0eed4-383">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0eed4-383">REMARKS</span></span>|<span data-ttu-id="0eed4-384">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-384">String</span></span>|  
|<span data-ttu-id="0eed4-385">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-385">PROCEDURE_TYPE</span></span>|<span data-ttu-id="0eed4-386">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-386">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="0eed4-387">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="0eed4-387">ProcedureColumns</span></span>  
  
|<span data-ttu-id="0eed4-388">열 이름</span><span class="sxs-lookup"><span data-stu-id="0eed4-388">ColumnName</span></span>|<span data-ttu-id="0eed4-389">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="0eed4-389">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0eed4-390">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="0eed4-390">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="0eed4-391">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-391">String</span></span>|  
|<span data-ttu-id="0eed4-392">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="0eed4-392">PROCEDURE_OWNER</span></span>|<span data-ttu-id="0eed4-393">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-393">String</span></span>|  
|<span data-ttu-id="0eed4-394">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-394">PROCEDURE_NAME</span></span>|<span data-ttu-id="0eed4-395">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-395">String</span></span>|  
|<span data-ttu-id="0eed4-396">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-396">COLUMN_NAME</span></span>|<span data-ttu-id="0eed4-397">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-397">String</span></span>|  
|<span data-ttu-id="0eed4-398">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-398">COLUMN_TYPE</span></span>|<span data-ttu-id="0eed4-399">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-399">Int16</span></span>|  
|<span data-ttu-id="0eed4-400">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-400">DATA_TYPE</span></span>|<span data-ttu-id="0eed4-401">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-401">Int16</span></span>|  
|<span data-ttu-id="0eed4-402">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-402">TYPE_NAME</span></span>|<span data-ttu-id="0eed4-403">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-403">String</span></span>|  
|<span data-ttu-id="0eed4-404">PRECISION</span><span class="sxs-lookup"><span data-stu-id="0eed4-404">PRECISION</span></span>|<span data-ttu-id="0eed4-405">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-405">Int32</span></span>|  
|<span data-ttu-id="0eed4-406">LENGTH</span><span class="sxs-lookup"><span data-stu-id="0eed4-406">LENGTH</span></span>|<span data-ttu-id="0eed4-407">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-407">Int32</span></span>|  
|<span data-ttu-id="0eed4-408">SCALE</span><span class="sxs-lookup"><span data-stu-id="0eed4-408">SCALE</span></span>|<span data-ttu-id="0eed4-409">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-409">Int16</span></span>|  
|<span data-ttu-id="0eed4-410">RADIX</span><span class="sxs-lookup"><span data-stu-id="0eed4-410">RADIX</span></span>|<span data-ttu-id="0eed4-411">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-411">Int16</span></span>|  
|<span data-ttu-id="0eed4-412">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0eed4-412">NULLABLE</span></span>|<span data-ttu-id="0eed4-413">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-413">Int16</span></span>|  
|<span data-ttu-id="0eed4-414">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0eed4-414">REMARKS</span></span>|<span data-ttu-id="0eed4-415">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-415">String</span></span>|  
|<span data-ttu-id="0eed4-416">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="0eed4-416">OVERLOAD</span></span>|<span data-ttu-id="0eed4-417">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-417">Int32</span></span>|  
|<span data-ttu-id="0eed4-418">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0eed4-418">ORDINAL_POSITION</span></span>|<span data-ttu-id="0eed4-419">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-419">Int32</span></span>|  
  
## <a name="microsoft-jet-odbc-driver"></a><span data-ttu-id="0eed4-420">Microsoft Jet ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="0eed4-420">Microsoft Jet ODBC Driver</span></span>  
 <span data-ttu-id="0eed4-421">Microsoft Jet ODBC Driver                                             .</span><span class="sxs-lookup"><span data-stu-id="0eed4-421">The Microsoft Jet ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="0eed4-422">Tables</span><span class="sxs-lookup"><span data-stu-id="0eed4-422">Tables</span></span>  
  
-   <span data-ttu-id="0eed4-423">Indexes</span><span class="sxs-lookup"><span data-stu-id="0eed4-423">Indexes</span></span>  
  
-   <span data-ttu-id="0eed4-424">Columns</span><span class="sxs-lookup"><span data-stu-id="0eed4-424">Columns</span></span>  
  
-   <span data-ttu-id="0eed4-425">절차</span><span class="sxs-lookup"><span data-stu-id="0eed4-425">Procedures</span></span>  
  
-   <span data-ttu-id="0eed4-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="0eed4-426">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="0eed4-427">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="0eed4-427">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="0eed4-428">뷰</span><span class="sxs-lookup"><span data-stu-id="0eed4-428">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="0eed4-429">Tables 및 Views</span><span class="sxs-lookup"><span data-stu-id="0eed4-429">Tables and Views</span></span>  
  
|<span data-ttu-id="0eed4-430">열 이름</span><span class="sxs-lookup"><span data-stu-id="0eed4-430">ColumnName</span></span>|<span data-ttu-id="0eed4-431">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="0eed4-431">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0eed4-432">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="0eed4-432">TABLE_QUALIFIER</span></span>|<span data-ttu-id="0eed4-433">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-433">String</span></span>|  
|<span data-ttu-id="0eed4-434">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="0eed4-434">TABLE_OWNER</span></span>|<span data-ttu-id="0eed4-435">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-435">String</span></span>|  
|<span data-ttu-id="0eed4-436">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-436">TABLE_NAME</span></span>|<span data-ttu-id="0eed4-437">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-437">String</span></span>|  
|<span data-ttu-id="0eed4-438">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-438">TABLE_TYPE</span></span>|<span data-ttu-id="0eed4-439">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-439">String</span></span>|  
|<span data-ttu-id="0eed4-440">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0eed4-440">REMARKS</span></span>|<span data-ttu-id="0eed4-441">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-441">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="0eed4-442">Columns</span><span class="sxs-lookup"><span data-stu-id="0eed4-442">Columns</span></span>  
  
|<span data-ttu-id="0eed4-443">열 이름</span><span class="sxs-lookup"><span data-stu-id="0eed4-443">ColumnName</span></span>|<span data-ttu-id="0eed4-444">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="0eed4-444">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0eed4-445">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="0eed4-445">TABLE_QUALIFIER</span></span>|<span data-ttu-id="0eed4-446">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-446">String</span></span>|  
|<span data-ttu-id="0eed4-447">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="0eed4-447">TABLE_OWNER</span></span>|<span data-ttu-id="0eed4-448">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-448">String</span></span>|  
|<span data-ttu-id="0eed4-449">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-449">TABLE_NAME</span></span>|<span data-ttu-id="0eed4-450">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-450">String</span></span>|  
|<span data-ttu-id="0eed4-451">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-451">COLUMN_NAME</span></span>|<span data-ttu-id="0eed4-452">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-452">String</span></span>|  
|<span data-ttu-id="0eed4-453">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-453">DATA_TYPE</span></span>|<span data-ttu-id="0eed4-454">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-454">Int16</span></span>|  
|<span data-ttu-id="0eed4-455">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-455">TYPE_NAME</span></span>|<span data-ttu-id="0eed4-456">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-456">String</span></span>|  
|<span data-ttu-id="0eed4-457">PRECISION</span><span class="sxs-lookup"><span data-stu-id="0eed4-457">PRECISION</span></span>|<span data-ttu-id="0eed4-458">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-458">Int32</span></span>|  
|<span data-ttu-id="0eed4-459">LENGTH</span><span class="sxs-lookup"><span data-stu-id="0eed4-459">LENGTH</span></span>|<span data-ttu-id="0eed4-460">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-460">Int32</span></span>|  
|<span data-ttu-id="0eed4-461">SCALE</span><span class="sxs-lookup"><span data-stu-id="0eed4-461">SCALE</span></span>|<span data-ttu-id="0eed4-462">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-462">Int16</span></span>|  
|<span data-ttu-id="0eed4-463">RADIX</span><span class="sxs-lookup"><span data-stu-id="0eed4-463">RADIX</span></span>|<span data-ttu-id="0eed4-464">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-464">Int16</span></span>|  
|<span data-ttu-id="0eed4-465">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0eed4-465">NULLABLE</span></span>|<span data-ttu-id="0eed4-466">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-466">Int16</span></span>|  
|<span data-ttu-id="0eed4-467">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0eed4-467">REMARKS</span></span>|<span data-ttu-id="0eed4-468">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-468">String</span></span>|  
|<span data-ttu-id="0eed4-469">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0eed4-469">ORDINAL_POSITION</span></span>|<span data-ttu-id="0eed4-470">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-470">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="0eed4-471">절차</span><span class="sxs-lookup"><span data-stu-id="0eed4-471">Procedures</span></span>  
  
|<span data-ttu-id="0eed4-472">열 이름</span><span class="sxs-lookup"><span data-stu-id="0eed4-472">ColumnName</span></span>|<span data-ttu-id="0eed4-473">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="0eed4-473">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0eed4-474">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="0eed4-474">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="0eed4-475">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-475">String</span></span>|  
|<span data-ttu-id="0eed4-476">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="0eed4-476">PROCEDURE_OWNER</span></span>|<span data-ttu-id="0eed4-477">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-477">String</span></span>|  
|<span data-ttu-id="0eed4-478">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-478">PROCEDURE_NAME</span></span>|<span data-ttu-id="0eed4-479">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-479">String</span></span>|  
|<span data-ttu-id="0eed4-480">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="0eed4-480">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="0eed4-481">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-481">Int16</span></span>|  
|<span data-ttu-id="0eed4-482">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="0eed4-482">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="0eed4-483">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-483">Int16</span></span>|  
|<span data-ttu-id="0eed4-484">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="0eed4-484">NUM_RESULT_SETS</span></span>|<span data-ttu-id="0eed4-485">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-485">Int16</span></span>|  
|<span data-ttu-id="0eed4-486">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0eed4-486">REMARKS</span></span>|<span data-ttu-id="0eed4-487">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-487">String</span></span>|  
|<span data-ttu-id="0eed4-488">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-488">PROCEDURE_TYPE</span></span>|<span data-ttu-id="0eed4-489">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-489">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="0eed4-490">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="0eed4-490">ProcedureColumns</span></span>  
  
|<span data-ttu-id="0eed4-491">열 이름</span><span class="sxs-lookup"><span data-stu-id="0eed4-491">ColumnName</span></span>|<span data-ttu-id="0eed4-492">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="0eed4-492">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0eed4-493">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="0eed4-493">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="0eed4-494">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-494">String</span></span>|  
|<span data-ttu-id="0eed4-495">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="0eed4-495">PROCEDURE_OWNER</span></span>|<span data-ttu-id="0eed4-496">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-496">String</span></span>|  
|<span data-ttu-id="0eed4-497">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-497">PROCEDURE_NAME</span></span>|<span data-ttu-id="0eed4-498">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-498">String</span></span>|  
|<span data-ttu-id="0eed4-499">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-499">COLUMN_NAME</span></span>|<span data-ttu-id="0eed4-500">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-500">String</span></span>|  
|<span data-ttu-id="0eed4-501">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-501">COLUMN_TYPE</span></span>|<span data-ttu-id="0eed4-502">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-502">Int16</span></span>|  
|<span data-ttu-id="0eed4-503">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-503">DATA_TYPE</span></span>|<span data-ttu-id="0eed4-504">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-504">Int16</span></span>|  
|<span data-ttu-id="0eed4-505">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-505">TYPE_NAME</span></span>|<span data-ttu-id="0eed4-506">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-506">String</span></span>|  
|<span data-ttu-id="0eed4-507">PRECISION</span><span class="sxs-lookup"><span data-stu-id="0eed4-507">PRECISION</span></span>|<span data-ttu-id="0eed4-508">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-508">Int32</span></span>|  
|<span data-ttu-id="0eed4-509">LENGTH</span><span class="sxs-lookup"><span data-stu-id="0eed4-509">LENGTH</span></span>|<span data-ttu-id="0eed4-510">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-510">Int32</span></span>|  
|<span data-ttu-id="0eed4-511">SCALE</span><span class="sxs-lookup"><span data-stu-id="0eed4-511">SCALE</span></span>|<span data-ttu-id="0eed4-512">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-512">Int16</span></span>|  
|<span data-ttu-id="0eed4-513">RADIX</span><span class="sxs-lookup"><span data-stu-id="0eed4-513">RADIX</span></span>|<span data-ttu-id="0eed4-514">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-514">Int16</span></span>|  
|<span data-ttu-id="0eed4-515">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0eed4-515">NULLABLE</span></span>|<span data-ttu-id="0eed4-516">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-516">Int16</span></span>|  
|<span data-ttu-id="0eed4-517">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0eed4-517">REMARKS</span></span>|<span data-ttu-id="0eed4-518">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-518">String</span></span>|  
|<span data-ttu-id="0eed4-519">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="0eed4-519">OVERLOAD</span></span>|<span data-ttu-id="0eed4-520">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-520">Int32</span></span>|  
|<span data-ttu-id="0eed4-521">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0eed4-521">ORDINAL_POSITION</span></span>|<span data-ttu-id="0eed4-522">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-522">Int32</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="0eed4-523">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="0eed4-523">ProcedureParameters</span></span>  
  
|<span data-ttu-id="0eed4-524">열 이름</span><span class="sxs-lookup"><span data-stu-id="0eed4-524">ColumnName</span></span>|<span data-ttu-id="0eed4-525">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="0eed4-525">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="0eed4-526">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="0eed4-526">PROCEDURE_CAT</span></span>|<span data-ttu-id="0eed4-527">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-527">String</span></span>|  
|<span data-ttu-id="0eed4-528">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="0eed4-528">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="0eed4-529">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-529">String</span></span>|  
|<span data-ttu-id="0eed4-530">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-530">PROCEDURE_NAME</span></span>|<span data-ttu-id="0eed4-531">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-531">String</span></span>|  
|<span data-ttu-id="0eed4-532">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-532">COLUMN_NAME</span></span>|<span data-ttu-id="0eed4-533">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-533">String</span></span>|  
|<span data-ttu-id="0eed4-534">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-534">COLUMN_TYPE</span></span>|<span data-ttu-id="0eed4-535">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-535">Int16</span></span>|  
|<span data-ttu-id="0eed4-536">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-536">DATA_TYPE</span></span>|<span data-ttu-id="0eed4-537">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-537">Int16</span></span>|  
|<span data-ttu-id="0eed4-538">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="0eed4-538">TYPE_NAME</span></span>|<span data-ttu-id="0eed4-539">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-539">String</span></span>|  
|<span data-ttu-id="0eed4-540">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="0eed4-540">COLUMN_SIZE</span></span>|<span data-ttu-id="0eed4-541">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-541">Int32</span></span>|  
|<span data-ttu-id="0eed4-542">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0eed4-542">BUFFER_LENGTH</span></span>|<span data-ttu-id="0eed4-543">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-543">Int32</span></span>|  
|<span data-ttu-id="0eed4-544">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="0eed4-544">DECIMAL_DIGITS</span></span>|<span data-ttu-id="0eed4-545">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-545">Int16</span></span>|  
|<span data-ttu-id="0eed4-546">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="0eed4-546">NUM_PREC_RADIX</span></span>|<span data-ttu-id="0eed4-547">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-547">Int16</span></span>|  
|<span data-ttu-id="0eed4-548">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0eed4-548">NULLABLE</span></span>|<span data-ttu-id="0eed4-549">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-549">Int16</span></span>|  
|<span data-ttu-id="0eed4-550">REMARKS</span><span class="sxs-lookup"><span data-stu-id="0eed4-550">REMARKS</span></span>|<span data-ttu-id="0eed4-551">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-551">String</span></span>|  
|<span data-ttu-id="0eed4-552">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="0eed4-552">COLUMN_DEF</span></span>|<span data-ttu-id="0eed4-553">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-553">String</span></span>|  
|<span data-ttu-id="0eed4-554">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="0eed4-554">SQL_DATA_TYPE</span></span>|<span data-ttu-id="0eed4-555">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-555">Int16</span></span>|  
|<span data-ttu-id="0eed4-556">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="0eed4-556">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="0eed4-557">Int16</span><span class="sxs-lookup"><span data-stu-id="0eed4-557">Int16</span></span>|  
|<span data-ttu-id="0eed4-558">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="0eed4-558">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="0eed4-559">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-559">Int32</span></span>|  
|<span data-ttu-id="0eed4-560">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="0eed4-560">ORDINAL_POSITION</span></span>|<span data-ttu-id="0eed4-561">Int32</span><span class="sxs-lookup"><span data-stu-id="0eed4-561">Int32</span></span>|  
|<span data-ttu-id="0eed4-562">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="0eed4-562">IS_NULLABLE</span></span>|<span data-ttu-id="0eed4-563">문자열</span><span class="sxs-lookup"><span data-stu-id="0eed4-563">String</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0eed4-564">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0eed4-564">See Also</span></span>  
 [<span data-ttu-id="0eed4-565">ADO.NET 관리되는 공급자 및 데이터 집합 개발자 센터</span><span class="sxs-lookup"><span data-stu-id="0eed4-565">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
