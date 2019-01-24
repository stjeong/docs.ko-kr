---
title: ODBC 스키마 컬렉션
ms.date: 03/30/2017
ms.assetid: 1bb126a5-ceec-4649-a4bc-8aa19e801046
ms.openlocfilehash: 072a9cd365031cd5660d1824bc229d459abc5af8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54525835"
---
# <a name="odbc-schema-collections"></a><span data-ttu-id="d2225-102">ODBC 스키마 컬렉션</span><span class="sxs-lookup"><span data-stu-id="d2225-102">ODBC Schema Collections</span></span>
<span data-ttu-id="d2225-103">이 단원에서는 Microsoft SQL Server, Oracle 및 Microsoft Jet용 ODBC 드라이버에서 지원하는 스키마 컬렉션에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="d2225-103">This section discusses schema collection support for the ODBC drivers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-odbc-driver"></a><span data-ttu-id="d2225-104">Microsoft SQL Server ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="d2225-104">Microsoft SQL Server ODBC Driver</span></span>  
 <span data-ttu-id="d2225-105">Microsoft SQL Server ODBC Driver에서는 공통 스키마 컬렉션 외에도 다음과 같은 특정 스키마 컬렉션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d2225-105">The Microsoft SQL Server ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="d2225-106">Tables</span><span class="sxs-lookup"><span data-stu-id="d2225-106">Tables</span></span>  
  
-   <span data-ttu-id="d2225-107">Indexes</span><span class="sxs-lookup"><span data-stu-id="d2225-107">Indexes</span></span>  
  
-   <span data-ttu-id="d2225-108">Columns</span><span class="sxs-lookup"><span data-stu-id="d2225-108">Columns</span></span>  
  
-   <span data-ttu-id="d2225-109">절차</span><span class="sxs-lookup"><span data-stu-id="d2225-109">Procedures</span></span>  
  
-   <span data-ttu-id="d2225-110">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="d2225-110">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="d2225-111">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="d2225-111">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="d2225-112">뷰</span><span class="sxs-lookup"><span data-stu-id="d2225-112">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="d2225-113">Tables 및 Views</span><span class="sxs-lookup"><span data-stu-id="d2225-113">Tables and Views</span></span>  
  
|<span data-ttu-id="d2225-114">열 이름</span><span class="sxs-lookup"><span data-stu-id="d2225-114">ColumnName</span></span>|<span data-ttu-id="d2225-115">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="d2225-115">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d2225-116">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="d2225-116">TABLE_CAT</span></span>|<span data-ttu-id="d2225-117">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-117">String</span></span>|  
|<span data-ttu-id="d2225-118">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="d2225-118">TABLE_SCHEM</span></span>|<span data-ttu-id="d2225-119">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-119">String</span></span>|  
|<span data-ttu-id="d2225-120">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-120">TABLE_NAME</span></span>|<span data-ttu-id="d2225-121">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-121">String</span></span>|  
|<span data-ttu-id="d2225-122">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-122">TABLE_TYPE</span></span>|<span data-ttu-id="d2225-123">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-123">String</span></span>|  
|<span data-ttu-id="d2225-124">REMARKS</span><span class="sxs-lookup"><span data-stu-id="d2225-124">REMARKS</span></span>|<span data-ttu-id="d2225-125">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-125">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="d2225-126">Indexes</span><span class="sxs-lookup"><span data-stu-id="d2225-126">Indexes</span></span>  
  
|<span data-ttu-id="d2225-127">열 이름</span><span class="sxs-lookup"><span data-stu-id="d2225-127">ColumnName</span></span>|<span data-ttu-id="d2225-128">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="d2225-128">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d2225-129">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="d2225-129">TABLE_CAT</span></span>|<span data-ttu-id="d2225-130">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-130">String</span></span>|  
|<span data-ttu-id="d2225-131">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="d2225-131">TABLE_SCHEM</span></span>|<span data-ttu-id="d2225-132">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-132">String</span></span>|  
|<span data-ttu-id="d2225-133">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-133">TABLE_NAME</span></span>|<span data-ttu-id="d2225-134">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-134">String</span></span>|  
|<span data-ttu-id="d2225-135">NON_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="d2225-135">NON_UNIQUE</span></span>|<span data-ttu-id="d2225-136">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-136">Int16</span></span>|  
|<span data-ttu-id="d2225-137">INDEX_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="d2225-137">INDEX_QUALIFIER</span></span>|<span data-ttu-id="d2225-138">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-138">String</span></span>|  
|<span data-ttu-id="d2225-139">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-139">INDEX_NAME</span></span>|<span data-ttu-id="d2225-140">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-140">String</span></span>|  
|<span data-ttu-id="d2225-141">TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-141">TYPE</span></span>|<span data-ttu-id="d2225-142">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-142">Int16</span></span>|  
|<span data-ttu-id="d2225-143">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="d2225-143">ORDINAL_POSITION</span></span>|<span data-ttu-id="d2225-144">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-144">Int16</span></span>|  
|<span data-ttu-id="d2225-145">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-145">COLUMN_NAME</span></span>|<span data-ttu-id="d2225-146">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-146">String</span></span>|  
|<span data-ttu-id="d2225-147">ASC_OR_DESC</span><span class="sxs-lookup"><span data-stu-id="d2225-147">ASC_OR_DESC</span></span>|<span data-ttu-id="d2225-148">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-148">String</span></span>|  
|<span data-ttu-id="d2225-149">CARDINATLITY</span><span class="sxs-lookup"><span data-stu-id="d2225-149">CARDINATLITY</span></span>|<span data-ttu-id="d2225-150">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-150">Int32</span></span>|  
|<span data-ttu-id="d2225-151">PAGES</span><span class="sxs-lookup"><span data-stu-id="d2225-151">PAGES</span></span>|<span data-ttu-id="d2225-152">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-152">Int32</span></span>|  
|<span data-ttu-id="d2225-153">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="d2225-153">FILTER_CONDITION</span></span>|<span data-ttu-id="d2225-154">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-154">String</span></span>|  
|<span data-ttu-id="d2225-155">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d2225-155">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="d2225-156">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-156">String</span></span>|  
|<span data-ttu-id="d2225-157">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-157">SS_DATA_TYPE</span></span>|<span data-ttu-id="d2225-158">Byte</span><span class="sxs-lookup"><span data-stu-id="d2225-158">Byte</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="d2225-159">Columns</span><span class="sxs-lookup"><span data-stu-id="d2225-159">Columns</span></span>  
  
|<span data-ttu-id="d2225-160">열 이름</span><span class="sxs-lookup"><span data-stu-id="d2225-160">ColumnName</span></span>|<span data-ttu-id="d2225-161">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="d2225-161">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d2225-162">TABLE_CAT</span><span class="sxs-lookup"><span data-stu-id="d2225-162">TABLE_CAT</span></span>|<span data-ttu-id="d2225-163">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-163">String</span></span>|  
|<span data-ttu-id="d2225-164">TABLE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="d2225-164">TABLE_SCHEM</span></span>|<span data-ttu-id="d2225-165">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-165">String</span></span>|  
|<span data-ttu-id="d2225-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-166">TABLE_NAME</span></span>|<span data-ttu-id="d2225-167">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-167">String</span></span>|  
|<span data-ttu-id="d2225-168">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-168">COLUMN_NAME</span></span>|<span data-ttu-id="d2225-169">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-169">String</span></span>|  
|<span data-ttu-id="d2225-170">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-170">DATA_TYPE</span></span>|<span data-ttu-id="d2225-171">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-171">Int16</span></span>|  
|<span data-ttu-id="d2225-172">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-172">TYPE_NAME</span></span>|<span data-ttu-id="d2225-173">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-173">String</span></span>|  
|<span data-ttu-id="d2225-174">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="d2225-174">COLUMN_SIZE</span></span>|<span data-ttu-id="d2225-175">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-175">Int32</span></span>|  
|<span data-ttu-id="d2225-176">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d2225-176">BUFFER_LENGTH</span></span>|<span data-ttu-id="d2225-177">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-177">Int32</span></span>|  
|<span data-ttu-id="d2225-178">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="d2225-178">DECIMAL_DIGITS</span></span>|<span data-ttu-id="d2225-179">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-179">Int16</span></span>|  
|<span data-ttu-id="d2225-180">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="d2225-180">NUM_PREC_RADIX</span></span>|<span data-ttu-id="d2225-181">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-181">Int16</span></span>|  
|<span data-ttu-id="d2225-182">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="d2225-182">NULLABLE</span></span>|<span data-ttu-id="d2225-183">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-183">Int16</span></span>|  
|<span data-ttu-id="d2225-184">REMARKS</span><span class="sxs-lookup"><span data-stu-id="d2225-184">REMARKS</span></span>|<span data-ttu-id="d2225-185">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-185">String</span></span>|  
|<span data-ttu-id="d2225-186">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="d2225-186">COLUMN_DEF</span></span>|<span data-ttu-id="d2225-187">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-187">String</span></span>|  
|<span data-ttu-id="d2225-188">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-188">SQL_DATA_TYPE</span></span>|<span data-ttu-id="d2225-189">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-189">Int16</span></span>|  
|<span data-ttu-id="d2225-190">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="d2225-190">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="d2225-191">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-191">Int16</span></span>|  
|<span data-ttu-id="d2225-192">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d2225-192">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="d2225-193">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-193">Int32</span></span>|  
|<span data-ttu-id="d2225-194">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="d2225-194">ORDINAL_POSITION</span></span>|<span data-ttu-id="d2225-195">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-195">Int32</span></span>|  
|<span data-ttu-id="d2225-196">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="d2225-196">IS_NULLABLE</span></span>|<span data-ttu-id="d2225-197">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-197">String</span></span>|  
|<span data-ttu-id="d2225-198">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d2225-198">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="d2225-199">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-199">String</span></span>|  
|<span data-ttu-id="d2225-200">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d2225-200">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="d2225-201">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-201">String</span></span>|  
|<span data-ttu-id="d2225-202">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-202">SS_DATA_TYPE</span></span>|<span data-ttu-id="d2225-203">Byte</span><span class="sxs-lookup"><span data-stu-id="d2225-203">Byte</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="d2225-204">절차</span><span class="sxs-lookup"><span data-stu-id="d2225-204">Procedures</span></span>  
  
|<span data-ttu-id="d2225-205">열 이름</span><span class="sxs-lookup"><span data-stu-id="d2225-205">ColumnName</span></span>|<span data-ttu-id="d2225-206">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="d2225-206">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d2225-207">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="d2225-207">PROCEDURE_CAT</span></span>|<span data-ttu-id="d2225-208">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-208">String</span></span>|  
|<span data-ttu-id="d2225-209">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="d2225-209">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="d2225-210">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-210">String</span></span>|  
|<span data-ttu-id="d2225-211">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-211">PROCEDURE_NAME</span></span>|<span data-ttu-id="d2225-212">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-212">String</span></span>|  
|<span data-ttu-id="d2225-213">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="d2225-213">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="d2225-214">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-214">Int32</span></span>|  
|<span data-ttu-id="d2225-215">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="d2225-215">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="d2225-216">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-216">Int32</span></span>|  
|<span data-ttu-id="d2225-217">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="d2225-217">NUM_RESULT_SETS</span></span>|<span data-ttu-id="d2225-218">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-218">Int32</span></span>|  
|<span data-ttu-id="d2225-219">REMARKS</span><span class="sxs-lookup"><span data-stu-id="d2225-219">REMARKS</span></span>|<span data-ttu-id="d2225-220">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-220">String</span></span>|  
|<span data-ttu-id="d2225-221">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-221">PROCEDURE_TYPE</span></span>|<span data-ttu-id="d2225-222">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-222">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="d2225-223">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="d2225-223">ProcedureColumns</span></span>  
  
|<span data-ttu-id="d2225-224">열 이름</span><span class="sxs-lookup"><span data-stu-id="d2225-224">ColumnName</span></span>|<span data-ttu-id="d2225-225">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="d2225-225">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d2225-226">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="d2225-226">PROCEDURE_CAT</span></span>|<span data-ttu-id="d2225-227">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-227">String</span></span>|  
|<span data-ttu-id="d2225-228">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="d2225-228">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="d2225-229">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-229">String</span></span>|  
|<span data-ttu-id="d2225-230">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-230">PROCEDURE_NAME</span></span>|<span data-ttu-id="d2225-231">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-231">String</span></span>|  
|<span data-ttu-id="d2225-232">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-232">COLUMN_NAME</span></span>|<span data-ttu-id="d2225-233">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-233">String</span></span>|  
|<span data-ttu-id="d2225-234">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-234">COLUMN_TYPE</span></span>|<span data-ttu-id="d2225-235">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-235">Int16</span></span>|  
|<span data-ttu-id="d2225-236">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-236">DATA_TYPE</span></span>|<span data-ttu-id="d2225-237">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-237">Int16</span></span>|  
|<span data-ttu-id="d2225-238">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-238">TYPE_NAME</span></span>|<span data-ttu-id="d2225-239">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-239">String</span></span>|  
|<span data-ttu-id="d2225-240">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="d2225-240">COLUMN_SIZE</span></span>|<span data-ttu-id="d2225-241">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-241">Int32</span></span>|  
|<span data-ttu-id="d2225-242">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d2225-242">BUFFER_LENGTH</span></span>|<span data-ttu-id="d2225-243">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-243">Int32</span></span>|  
|<span data-ttu-id="d2225-244">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="d2225-244">DECIMAL_DIGITS</span></span>|<span data-ttu-id="d2225-245">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-245">Int16</span></span>|  
|<span data-ttu-id="d2225-246">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="d2225-246">NUM_PREC_RADIX</span></span>|<span data-ttu-id="d2225-247">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-247">Int16</span></span>|  
|<span data-ttu-id="d2225-248">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="d2225-248">NULLABLE</span></span>|<span data-ttu-id="d2225-249">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-249">Int16</span></span>|  
|<span data-ttu-id="d2225-250">REMARKS</span><span class="sxs-lookup"><span data-stu-id="d2225-250">REMARKS</span></span>|<span data-ttu-id="d2225-251">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-251">String</span></span>|  
|<span data-ttu-id="d2225-252">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="d2225-252">COLUMN_DEF</span></span>|<span data-ttu-id="d2225-253">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-253">String</span></span>|  
|<span data-ttu-id="d2225-254">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-254">SQL_DATA_TYPE</span></span>|<span data-ttu-id="d2225-255">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-255">Int16</span></span>|  
|<span data-ttu-id="d2225-256">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="d2225-256">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="d2225-257">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-257">Int16</span></span>|  
|<span data-ttu-id="d2225-258">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d2225-258">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="d2225-259">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-259">Int32</span></span>|  
|<span data-ttu-id="d2225-260">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="d2225-260">ORDINAL_POSITION</span></span>|<span data-ttu-id="d2225-261">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-261">Int32</span></span>|  
|<span data-ttu-id="d2225-262">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="d2225-262">IS_NULLABLE</span></span>|<span data-ttu-id="d2225-263">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-263">String</span></span>|  
|<span data-ttu-id="d2225-264">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d2225-264">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="d2225-265">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-265">String</span></span>|  
|<span data-ttu-id="d2225-266">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d2225-266">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="d2225-267">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-267">String</span></span>|  
|<span data-ttu-id="d2225-268">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-268">SS_DATA_TYPE</span></span>|<span data-ttu-id="d2225-269">Byte</span><span class="sxs-lookup"><span data-stu-id="d2225-269">Byte</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="d2225-270">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="d2225-270">ProcedureParameters</span></span>  
  
|<span data-ttu-id="d2225-271">열 이름</span><span class="sxs-lookup"><span data-stu-id="d2225-271">ColumnName</span></span>|<span data-ttu-id="d2225-272">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="d2225-272">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d2225-273">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="d2225-273">PROCEDURE_CAT</span></span>|<span data-ttu-id="d2225-274">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-274">String</span></span>|  
|<span data-ttu-id="d2225-275">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="d2225-275">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="d2225-276">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-276">String</span></span>|  
|<span data-ttu-id="d2225-277">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-277">PROCEDURE_NAME</span></span>|<span data-ttu-id="d2225-278">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-278">String</span></span>|  
|<span data-ttu-id="d2225-279">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-279">COLUMN_NAME</span></span>|<span data-ttu-id="d2225-280">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-280">String</span></span>|  
|<span data-ttu-id="d2225-281">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-281">COLUMN_TYPE</span></span>|<span data-ttu-id="d2225-282">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-282">Int16</span></span>|  
|<span data-ttu-id="d2225-283">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-283">DATA_TYPE</span></span>|<span data-ttu-id="d2225-284">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-284">Int16</span></span>|  
|<span data-ttu-id="d2225-285">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-285">TYPE_NAME</span></span>|<span data-ttu-id="d2225-286">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-286">String</span></span>|  
|<span data-ttu-id="d2225-287">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="d2225-287">COLUMN_SIZE</span></span>|<span data-ttu-id="d2225-288">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-288">Int32</span></span>|  
|<span data-ttu-id="d2225-289">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d2225-289">BUFFER_LENGTH</span></span>|<span data-ttu-id="d2225-290">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-290">Int32</span></span>|  
|<span data-ttu-id="d2225-291">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="d2225-291">DECIMAL_DIGITS</span></span>|<span data-ttu-id="d2225-292">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-292">Int16</span></span>|  
|<span data-ttu-id="d2225-293">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="d2225-293">NUM_PREC_RADIX</span></span>|<span data-ttu-id="d2225-294">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-294">Int16</span></span>|  
|<span data-ttu-id="d2225-295">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="d2225-295">NULLABLE</span></span>|<span data-ttu-id="d2225-296">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-296">Int16</span></span>|  
|<span data-ttu-id="d2225-297">REMARKS</span><span class="sxs-lookup"><span data-stu-id="d2225-297">REMARKS</span></span>|<span data-ttu-id="d2225-298">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-298">String</span></span>|  
|<span data-ttu-id="d2225-299">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="d2225-299">COLUMN_DEF</span></span>|<span data-ttu-id="d2225-300">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-300">String</span></span>|  
|<span data-ttu-id="d2225-301">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-301">SQL_DATA_TYPE</span></span>|<span data-ttu-id="d2225-302">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-302">Int16</span></span>|  
|<span data-ttu-id="d2225-303">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="d2225-303">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="d2225-304">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-304">Int16</span></span>|  
|<span data-ttu-id="d2225-305">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d2225-305">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="d2225-306">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-306">Int32</span></span>|  
|<span data-ttu-id="d2225-307">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="d2225-307">ORDINAL_POSITION</span></span>|<span data-ttu-id="d2225-308">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-308">Int32</span></span>|  
|<span data-ttu-id="d2225-309">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="d2225-309">IS_NULLABLE</span></span>|<span data-ttu-id="d2225-310">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-310">String</span></span>|  
|<span data-ttu-id="d2225-311">SS_TYPE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d2225-311">SS_TYPE_CATALOG</span></span>|<span data-ttu-id="d2225-312">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-312">String</span></span>|  
|<span data-ttu-id="d2225-313">SS_TYPE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d2225-313">SS_TYPE_SCHEMA</span></span>|<span data-ttu-id="d2225-314">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-314">String</span></span>|  
|<span data-ttu-id="d2225-315">SS_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-315">SS_DATA_TYPE</span></span>|<span data-ttu-id="d2225-316">Byte</span><span class="sxs-lookup"><span data-stu-id="d2225-316">Byte</span></span>|  
  
## <a name="microsoft-oracle-odbc-driver"></a><span data-ttu-id="d2225-317">Microsoft Oracle ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="d2225-317">Microsoft Oracle ODBC Driver</span></span>  
 <span data-ttu-id="d2225-318">Microsoft SQL Server Oracle ODBC Driver에서는 공통 스키마 컬렉션 외에도 다음과 같은 특정 스키마 컬렉션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d2225-318">The Microsoft SQL Server Oracle ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="d2225-319">Tables</span><span class="sxs-lookup"><span data-stu-id="d2225-319">Tables</span></span>  
  
-   <span data-ttu-id="d2225-320">Columns</span><span class="sxs-lookup"><span data-stu-id="d2225-320">Columns</span></span>  
  
-   <span data-ttu-id="d2225-321">절차</span><span class="sxs-lookup"><span data-stu-id="d2225-321">Procedures</span></span>  
  
-   <span data-ttu-id="d2225-322">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="d2225-322">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="d2225-323">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="d2225-323">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="d2225-324">뷰</span><span class="sxs-lookup"><span data-stu-id="d2225-324">Views</span></span>  
  
-   <span data-ttu-id="d2225-325">Indexes</span><span class="sxs-lookup"><span data-stu-id="d2225-325">Indexes</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="d2225-326">Tables 및 Views</span><span class="sxs-lookup"><span data-stu-id="d2225-326">Tables and Views</span></span>  
  
|<span data-ttu-id="d2225-327">열 이름</span><span class="sxs-lookup"><span data-stu-id="d2225-327">ColumnName</span></span>|<span data-ttu-id="d2225-328">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="d2225-328">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d2225-329">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="d2225-329">TABLE_QUALIFIER</span></span>|<span data-ttu-id="d2225-330">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-330">String</span></span>|  
|<span data-ttu-id="d2225-331">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="d2225-331">TABLE_OWNER</span></span>|<span data-ttu-id="d2225-332">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-332">String</span></span>|  
|<span data-ttu-id="d2225-333">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-333">TABLE_NAME</span></span>|<span data-ttu-id="d2225-334">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-334">String</span></span>|  
|<span data-ttu-id="d2225-335">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-335">TABLE_TYPE</span></span>|<span data-ttu-id="d2225-336">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-336">String</span></span>|  
|<span data-ttu-id="d2225-337">REMARKS</span><span class="sxs-lookup"><span data-stu-id="d2225-337">REMARKS</span></span>|<span data-ttu-id="d2225-338">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-338">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="d2225-339">Columns</span><span class="sxs-lookup"><span data-stu-id="d2225-339">Columns</span></span>  
  
|<span data-ttu-id="d2225-340">열 이름</span><span class="sxs-lookup"><span data-stu-id="d2225-340">ColumnName</span></span>|<span data-ttu-id="d2225-341">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="d2225-341">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d2225-342">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="d2225-342">TABLE_QUALIFIER</span></span>|<span data-ttu-id="d2225-343">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-343">String</span></span>|  
|<span data-ttu-id="d2225-344">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="d2225-344">TABLE_OWNER</span></span>|<span data-ttu-id="d2225-345">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-345">String</span></span>|  
|<span data-ttu-id="d2225-346">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-346">TABLE_NAME</span></span>|<span data-ttu-id="d2225-347">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-347">String</span></span>|  
|<span data-ttu-id="d2225-348">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-348">COLUMN_NAME</span></span>|<span data-ttu-id="d2225-349">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-349">String</span></span>|  
|<span data-ttu-id="d2225-350">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-350">DATA_TYPE</span></span>|<span data-ttu-id="d2225-351">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-351">Int16</span></span>|  
|<span data-ttu-id="d2225-352">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-352">TYPE_NAME</span></span>|<span data-ttu-id="d2225-353">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-353">String</span></span>|  
|<span data-ttu-id="d2225-354">PRECISION</span><span class="sxs-lookup"><span data-stu-id="d2225-354">PRECISION</span></span>|<span data-ttu-id="d2225-355">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-355">Int32</span></span>|  
|<span data-ttu-id="d2225-356">LENGTH</span><span class="sxs-lookup"><span data-stu-id="d2225-356">LENGTH</span></span>|<span data-ttu-id="d2225-357">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-357">Int32</span></span>|  
|<span data-ttu-id="d2225-358">SCALE</span><span class="sxs-lookup"><span data-stu-id="d2225-358">SCALE</span></span>|<span data-ttu-id="d2225-359">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-359">Int16</span></span>|  
|<span data-ttu-id="d2225-360">RADIX</span><span class="sxs-lookup"><span data-stu-id="d2225-360">RADIX</span></span>|<span data-ttu-id="d2225-361">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-361">Int16</span></span>|  
|<span data-ttu-id="d2225-362">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="d2225-362">NULLABLE</span></span>|<span data-ttu-id="d2225-363">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-363">Int16</span></span>|  
|<span data-ttu-id="d2225-364">REMARKS</span><span class="sxs-lookup"><span data-stu-id="d2225-364">REMARKS</span></span>|<span data-ttu-id="d2225-365">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-365">String</span></span>|  
|<span data-ttu-id="d2225-366">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="d2225-366">ORDINAL_POSITION</span></span>|<span data-ttu-id="d2225-367">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-367">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="d2225-368">절차</span><span class="sxs-lookup"><span data-stu-id="d2225-368">Procedures</span></span>  
  
|<span data-ttu-id="d2225-369">열 이름</span><span class="sxs-lookup"><span data-stu-id="d2225-369">ColumnName</span></span>|<span data-ttu-id="d2225-370">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="d2225-370">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d2225-371">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="d2225-371">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="d2225-372">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-372">String</span></span>|  
|<span data-ttu-id="d2225-373">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="d2225-373">PROCEDURE_OWNER</span></span>|<span data-ttu-id="d2225-374">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-374">String</span></span>|  
|<span data-ttu-id="d2225-375">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-375">PROCEDURE_NAME</span></span>|<span data-ttu-id="d2225-376">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-376">String</span></span>|  
|<span data-ttu-id="d2225-377">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="d2225-377">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="d2225-378">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-378">Int16</span></span>|  
|<span data-ttu-id="d2225-379">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="d2225-379">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="d2225-380">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-380">Int16</span></span>|  
|<span data-ttu-id="d2225-381">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="d2225-381">NUM_RESULT_SETS</span></span>|<span data-ttu-id="d2225-382">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-382">Int16</span></span>|  
|<span data-ttu-id="d2225-383">REMARKS</span><span class="sxs-lookup"><span data-stu-id="d2225-383">REMARKS</span></span>|<span data-ttu-id="d2225-384">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-384">String</span></span>|  
|<span data-ttu-id="d2225-385">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-385">PROCEDURE_TYPE</span></span>|<span data-ttu-id="d2225-386">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-386">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="d2225-387">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="d2225-387">ProcedureColumns</span></span>  
  
|<span data-ttu-id="d2225-388">열 이름</span><span class="sxs-lookup"><span data-stu-id="d2225-388">ColumnName</span></span>|<span data-ttu-id="d2225-389">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="d2225-389">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d2225-390">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="d2225-390">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="d2225-391">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-391">String</span></span>|  
|<span data-ttu-id="d2225-392">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="d2225-392">PROCEDURE_OWNER</span></span>|<span data-ttu-id="d2225-393">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-393">String</span></span>|  
|<span data-ttu-id="d2225-394">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-394">PROCEDURE_NAME</span></span>|<span data-ttu-id="d2225-395">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-395">String</span></span>|  
|<span data-ttu-id="d2225-396">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-396">COLUMN_NAME</span></span>|<span data-ttu-id="d2225-397">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-397">String</span></span>|  
|<span data-ttu-id="d2225-398">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-398">COLUMN_TYPE</span></span>|<span data-ttu-id="d2225-399">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-399">Int16</span></span>|  
|<span data-ttu-id="d2225-400">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-400">DATA_TYPE</span></span>|<span data-ttu-id="d2225-401">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-401">Int16</span></span>|  
|<span data-ttu-id="d2225-402">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-402">TYPE_NAME</span></span>|<span data-ttu-id="d2225-403">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-403">String</span></span>|  
|<span data-ttu-id="d2225-404">PRECISION</span><span class="sxs-lookup"><span data-stu-id="d2225-404">PRECISION</span></span>|<span data-ttu-id="d2225-405">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-405">Int32</span></span>|  
|<span data-ttu-id="d2225-406">LENGTH</span><span class="sxs-lookup"><span data-stu-id="d2225-406">LENGTH</span></span>|<span data-ttu-id="d2225-407">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-407">Int32</span></span>|  
|<span data-ttu-id="d2225-408">SCALE</span><span class="sxs-lookup"><span data-stu-id="d2225-408">SCALE</span></span>|<span data-ttu-id="d2225-409">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-409">Int16</span></span>|  
|<span data-ttu-id="d2225-410">RADIX</span><span class="sxs-lookup"><span data-stu-id="d2225-410">RADIX</span></span>|<span data-ttu-id="d2225-411">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-411">Int16</span></span>|  
|<span data-ttu-id="d2225-412">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="d2225-412">NULLABLE</span></span>|<span data-ttu-id="d2225-413">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-413">Int16</span></span>|  
|<span data-ttu-id="d2225-414">REMARKS</span><span class="sxs-lookup"><span data-stu-id="d2225-414">REMARKS</span></span>|<span data-ttu-id="d2225-415">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-415">String</span></span>|  
|<span data-ttu-id="d2225-416">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="d2225-416">OVERLOAD</span></span>|<span data-ttu-id="d2225-417">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-417">Int32</span></span>|  
|<span data-ttu-id="d2225-418">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="d2225-418">ORDINAL_POSITION</span></span>|<span data-ttu-id="d2225-419">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-419">Int32</span></span>|  
  
## <a name="microsoft-jet-odbc-driver"></a><span data-ttu-id="d2225-420">Microsoft Jet ODBC Driver</span><span class="sxs-lookup"><span data-stu-id="d2225-420">Microsoft Jet ODBC Driver</span></span>  
 <span data-ttu-id="d2225-421">Microsoft Jet ODBC Driver                                             .</span><span class="sxs-lookup"><span data-stu-id="d2225-421">The Microsoft Jet ODBC Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="d2225-422">Tables</span><span class="sxs-lookup"><span data-stu-id="d2225-422">Tables</span></span>  
  
-   <span data-ttu-id="d2225-423">Indexes</span><span class="sxs-lookup"><span data-stu-id="d2225-423">Indexes</span></span>  
  
-   <span data-ttu-id="d2225-424">Columns</span><span class="sxs-lookup"><span data-stu-id="d2225-424">Columns</span></span>  
  
-   <span data-ttu-id="d2225-425">절차</span><span class="sxs-lookup"><span data-stu-id="d2225-425">Procedures</span></span>  
  
-   <span data-ttu-id="d2225-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="d2225-426">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="d2225-427">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="d2225-427">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="d2225-428">뷰</span><span class="sxs-lookup"><span data-stu-id="d2225-428">Views</span></span>  
  
### <a name="tables-and-views"></a><span data-ttu-id="d2225-429">Tables 및 Views</span><span class="sxs-lookup"><span data-stu-id="d2225-429">Tables and Views</span></span>  
  
|<span data-ttu-id="d2225-430">열 이름</span><span class="sxs-lookup"><span data-stu-id="d2225-430">ColumnName</span></span>|<span data-ttu-id="d2225-431">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="d2225-431">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d2225-432">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="d2225-432">TABLE_QUALIFIER</span></span>|<span data-ttu-id="d2225-433">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-433">String</span></span>|  
|<span data-ttu-id="d2225-434">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="d2225-434">TABLE_OWNER</span></span>|<span data-ttu-id="d2225-435">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-435">String</span></span>|  
|<span data-ttu-id="d2225-436">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-436">TABLE_NAME</span></span>|<span data-ttu-id="d2225-437">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-437">String</span></span>|  
|<span data-ttu-id="d2225-438">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-438">TABLE_TYPE</span></span>|<span data-ttu-id="d2225-439">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-439">String</span></span>|  
|<span data-ttu-id="d2225-440">REMARKS</span><span class="sxs-lookup"><span data-stu-id="d2225-440">REMARKS</span></span>|<span data-ttu-id="d2225-441">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-441">String</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="d2225-442">Columns</span><span class="sxs-lookup"><span data-stu-id="d2225-442">Columns</span></span>  
  
|<span data-ttu-id="d2225-443">열 이름</span><span class="sxs-lookup"><span data-stu-id="d2225-443">ColumnName</span></span>|<span data-ttu-id="d2225-444">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="d2225-444">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d2225-445">TABLE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="d2225-445">TABLE_QUALIFIER</span></span>|<span data-ttu-id="d2225-446">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-446">String</span></span>|  
|<span data-ttu-id="d2225-447">TABLE_OWNER</span><span class="sxs-lookup"><span data-stu-id="d2225-447">TABLE_OWNER</span></span>|<span data-ttu-id="d2225-448">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-448">String</span></span>|  
|<span data-ttu-id="d2225-449">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-449">TABLE_NAME</span></span>|<span data-ttu-id="d2225-450">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-450">String</span></span>|  
|<span data-ttu-id="d2225-451">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-451">COLUMN_NAME</span></span>|<span data-ttu-id="d2225-452">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-452">String</span></span>|  
|<span data-ttu-id="d2225-453">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-453">DATA_TYPE</span></span>|<span data-ttu-id="d2225-454">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-454">Int16</span></span>|  
|<span data-ttu-id="d2225-455">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-455">TYPE_NAME</span></span>|<span data-ttu-id="d2225-456">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-456">String</span></span>|  
|<span data-ttu-id="d2225-457">PRECISION</span><span class="sxs-lookup"><span data-stu-id="d2225-457">PRECISION</span></span>|<span data-ttu-id="d2225-458">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-458">Int32</span></span>|  
|<span data-ttu-id="d2225-459">LENGTH</span><span class="sxs-lookup"><span data-stu-id="d2225-459">LENGTH</span></span>|<span data-ttu-id="d2225-460">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-460">Int32</span></span>|  
|<span data-ttu-id="d2225-461">SCALE</span><span class="sxs-lookup"><span data-stu-id="d2225-461">SCALE</span></span>|<span data-ttu-id="d2225-462">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-462">Int16</span></span>|  
|<span data-ttu-id="d2225-463">RADIX</span><span class="sxs-lookup"><span data-stu-id="d2225-463">RADIX</span></span>|<span data-ttu-id="d2225-464">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-464">Int16</span></span>|  
|<span data-ttu-id="d2225-465">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="d2225-465">NULLABLE</span></span>|<span data-ttu-id="d2225-466">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-466">Int16</span></span>|  
|<span data-ttu-id="d2225-467">REMARKS</span><span class="sxs-lookup"><span data-stu-id="d2225-467">REMARKS</span></span>|<span data-ttu-id="d2225-468">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-468">String</span></span>|  
|<span data-ttu-id="d2225-469">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="d2225-469">ORDINAL_POSITION</span></span>|<span data-ttu-id="d2225-470">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-470">Int32</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="d2225-471">절차</span><span class="sxs-lookup"><span data-stu-id="d2225-471">Procedures</span></span>  
  
|<span data-ttu-id="d2225-472">열 이름</span><span class="sxs-lookup"><span data-stu-id="d2225-472">ColumnName</span></span>|<span data-ttu-id="d2225-473">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="d2225-473">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d2225-474">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="d2225-474">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="d2225-475">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-475">String</span></span>|  
|<span data-ttu-id="d2225-476">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="d2225-476">PROCEDURE_OWNER</span></span>|<span data-ttu-id="d2225-477">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-477">String</span></span>|  
|<span data-ttu-id="d2225-478">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-478">PROCEDURE_NAME</span></span>|<span data-ttu-id="d2225-479">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-479">String</span></span>|  
|<span data-ttu-id="d2225-480">NUM_INPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="d2225-480">NUM_INPUT_PARAMS</span></span>|<span data-ttu-id="d2225-481">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-481">Int16</span></span>|  
|<span data-ttu-id="d2225-482">NUM_OUTPUT_PARAMS</span><span class="sxs-lookup"><span data-stu-id="d2225-482">NUM_OUTPUT_PARAMS</span></span>|<span data-ttu-id="d2225-483">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-483">Int16</span></span>|  
|<span data-ttu-id="d2225-484">NUM_RESULT_SETS</span><span class="sxs-lookup"><span data-stu-id="d2225-484">NUM_RESULT_SETS</span></span>|<span data-ttu-id="d2225-485">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-485">Int16</span></span>|  
|<span data-ttu-id="d2225-486">REMARKS</span><span class="sxs-lookup"><span data-stu-id="d2225-486">REMARKS</span></span>|<span data-ttu-id="d2225-487">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-487">String</span></span>|  
|<span data-ttu-id="d2225-488">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-488">PROCEDURE_TYPE</span></span>|<span data-ttu-id="d2225-489">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-489">Int16</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="d2225-490">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="d2225-490">ProcedureColumns</span></span>  
  
|<span data-ttu-id="d2225-491">열 이름</span><span class="sxs-lookup"><span data-stu-id="d2225-491">ColumnName</span></span>|<span data-ttu-id="d2225-492">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="d2225-492">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d2225-493">PROCEDURE_QUALIFIER</span><span class="sxs-lookup"><span data-stu-id="d2225-493">PROCEDURE_QUALIFIER</span></span>|<span data-ttu-id="d2225-494">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-494">String</span></span>|  
|<span data-ttu-id="d2225-495">PROCEDURE_OWNER</span><span class="sxs-lookup"><span data-stu-id="d2225-495">PROCEDURE_OWNER</span></span>|<span data-ttu-id="d2225-496">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-496">String</span></span>|  
|<span data-ttu-id="d2225-497">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-497">PROCEDURE_NAME</span></span>|<span data-ttu-id="d2225-498">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-498">String</span></span>|  
|<span data-ttu-id="d2225-499">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-499">COLUMN_NAME</span></span>|<span data-ttu-id="d2225-500">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-500">String</span></span>|  
|<span data-ttu-id="d2225-501">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-501">COLUMN_TYPE</span></span>|<span data-ttu-id="d2225-502">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-502">Int16</span></span>|  
|<span data-ttu-id="d2225-503">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-503">DATA_TYPE</span></span>|<span data-ttu-id="d2225-504">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-504">Int16</span></span>|  
|<span data-ttu-id="d2225-505">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-505">TYPE_NAME</span></span>|<span data-ttu-id="d2225-506">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-506">String</span></span>|  
|<span data-ttu-id="d2225-507">PRECISION</span><span class="sxs-lookup"><span data-stu-id="d2225-507">PRECISION</span></span>|<span data-ttu-id="d2225-508">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-508">Int32</span></span>|  
|<span data-ttu-id="d2225-509">LENGTH</span><span class="sxs-lookup"><span data-stu-id="d2225-509">LENGTH</span></span>|<span data-ttu-id="d2225-510">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-510">Int32</span></span>|  
|<span data-ttu-id="d2225-511">SCALE</span><span class="sxs-lookup"><span data-stu-id="d2225-511">SCALE</span></span>|<span data-ttu-id="d2225-512">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-512">Int16</span></span>|  
|<span data-ttu-id="d2225-513">RADIX</span><span class="sxs-lookup"><span data-stu-id="d2225-513">RADIX</span></span>|<span data-ttu-id="d2225-514">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-514">Int16</span></span>|  
|<span data-ttu-id="d2225-515">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="d2225-515">NULLABLE</span></span>|<span data-ttu-id="d2225-516">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-516">Int16</span></span>|  
|<span data-ttu-id="d2225-517">REMARKS</span><span class="sxs-lookup"><span data-stu-id="d2225-517">REMARKS</span></span>|<span data-ttu-id="d2225-518">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-518">String</span></span>|  
|<span data-ttu-id="d2225-519">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="d2225-519">OVERLOAD</span></span>|<span data-ttu-id="d2225-520">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-520">Int32</span></span>|  
|<span data-ttu-id="d2225-521">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="d2225-521">ORDINAL_POSITION</span></span>|<span data-ttu-id="d2225-522">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-522">Int32</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="d2225-523">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="d2225-523">ProcedureParameters</span></span>  
  
|<span data-ttu-id="d2225-524">열 이름</span><span class="sxs-lookup"><span data-stu-id="d2225-524">ColumnName</span></span>|<span data-ttu-id="d2225-525">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="d2225-525">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="d2225-526">PROCEDURE_CAT</span><span class="sxs-lookup"><span data-stu-id="d2225-526">PROCEDURE_CAT</span></span>|<span data-ttu-id="d2225-527">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-527">String</span></span>|  
|<span data-ttu-id="d2225-528">PROCEDURE_SCHEM</span><span class="sxs-lookup"><span data-stu-id="d2225-528">PROCEDURE_SCHEM</span></span>|<span data-ttu-id="d2225-529">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-529">String</span></span>|  
|<span data-ttu-id="d2225-530">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-530">PROCEDURE_NAME</span></span>|<span data-ttu-id="d2225-531">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-531">String</span></span>|  
|<span data-ttu-id="d2225-532">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-532">COLUMN_NAME</span></span>|<span data-ttu-id="d2225-533">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-533">String</span></span>|  
|<span data-ttu-id="d2225-534">COLUMN_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-534">COLUMN_TYPE</span></span>|<span data-ttu-id="d2225-535">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-535">Int16</span></span>|  
|<span data-ttu-id="d2225-536">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-536">DATA_TYPE</span></span>|<span data-ttu-id="d2225-537">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-537">Int16</span></span>|  
|<span data-ttu-id="d2225-538">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="d2225-538">TYPE_NAME</span></span>|<span data-ttu-id="d2225-539">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-539">String</span></span>|  
|<span data-ttu-id="d2225-540">COLUMN_SIZE</span><span class="sxs-lookup"><span data-stu-id="d2225-540">COLUMN_SIZE</span></span>|<span data-ttu-id="d2225-541">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-541">Int32</span></span>|  
|<span data-ttu-id="d2225-542">BUFFER_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d2225-542">BUFFER_LENGTH</span></span>|<span data-ttu-id="d2225-543">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-543">Int32</span></span>|  
|<span data-ttu-id="d2225-544">DECIMAL_DIGITS</span><span class="sxs-lookup"><span data-stu-id="d2225-544">DECIMAL_DIGITS</span></span>|<span data-ttu-id="d2225-545">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-545">Int16</span></span>|  
|<span data-ttu-id="d2225-546">NUM_PREC_RADIX</span><span class="sxs-lookup"><span data-stu-id="d2225-546">NUM_PREC_RADIX</span></span>|<span data-ttu-id="d2225-547">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-547">Int16</span></span>|  
|<span data-ttu-id="d2225-548">NULLABLE</span><span class="sxs-lookup"><span data-stu-id="d2225-548">NULLABLE</span></span>|<span data-ttu-id="d2225-549">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-549">Int16</span></span>|  
|<span data-ttu-id="d2225-550">REMARKS</span><span class="sxs-lookup"><span data-stu-id="d2225-550">REMARKS</span></span>|<span data-ttu-id="d2225-551">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-551">String</span></span>|  
|<span data-ttu-id="d2225-552">COLUMN_DEF</span><span class="sxs-lookup"><span data-stu-id="d2225-552">COLUMN_DEF</span></span>|<span data-ttu-id="d2225-553">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-553">String</span></span>|  
|<span data-ttu-id="d2225-554">SQL_DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2225-554">SQL_DATA_TYPE</span></span>|<span data-ttu-id="d2225-555">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-555">Int16</span></span>|  
|<span data-ttu-id="d2225-556">SQL_DATETIME_SUB</span><span class="sxs-lookup"><span data-stu-id="d2225-556">SQL_DATETIME_SUB</span></span>|<span data-ttu-id="d2225-557">Int16</span><span class="sxs-lookup"><span data-stu-id="d2225-557">Int16</span></span>|  
|<span data-ttu-id="d2225-558">CHAR_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="d2225-558">CHAR_OCTET_LENGTH</span></span>|<span data-ttu-id="d2225-559">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-559">Int32</span></span>|  
|<span data-ttu-id="d2225-560">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="d2225-560">ORDINAL_POSITION</span></span>|<span data-ttu-id="d2225-561">Int32</span><span class="sxs-lookup"><span data-stu-id="d2225-561">Int32</span></span>|  
|<span data-ttu-id="d2225-562">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="d2225-562">IS_NULLABLE</span></span>|<span data-ttu-id="d2225-563">문자열</span><span class="sxs-lookup"><span data-stu-id="d2225-563">String</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d2225-564">참고자료</span><span class="sxs-lookup"><span data-stu-id="d2225-564">See also</span></span>
- [<span data-ttu-id="d2225-565">ADO.NET 관리되는 공급자 및 데이터 집합 개발자 센터</span><span class="sxs-lookup"><span data-stu-id="d2225-565">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
