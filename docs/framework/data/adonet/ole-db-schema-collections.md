---
title: OLE DB 스키마 컬렉션
ms.date: 03/30/2017
ms.assetid: 6380c36b-658e-4d67-91e8-7131ef4a7c2c
ms.openlocfilehash: f753f35aab0a0200da5de463a73abb9813253d11
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54658457"
---
# <a name="ole-db-schema-collections"></a><span data-ttu-id="6307e-102">OLE DB 스키마 컬렉션</span><span class="sxs-lookup"><span data-stu-id="6307e-102">OLE DB Schema Collections</span></span>
<span data-ttu-id="6307e-103">이 단원에서는 Microsoft SQL Server, Oracle 및 Microsoft Jet용 OLE DB 공급자에서 지원하는 스키마 컬렉션에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="6307e-103">This section discusses schema collection support for the OLE DB providers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-ole-db-provider"></a><span data-ttu-id="6307e-104">Microsoft SQL Server OLE DB 공급자</span><span class="sxs-lookup"><span data-stu-id="6307e-104">Microsoft SQL Server OLE DB Provider</span></span>  
 <span data-ttu-id="6307e-105">Microsoft SQL Server OLE DB Driver에서는 공통 스키마 컬렉션 외에도 다음과 같은 특정 스키마 컬렉션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6307e-105">The Microsoft SQL Server OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="6307e-106">Tables</span><span class="sxs-lookup"><span data-stu-id="6307e-106">Tables</span></span>  
  
-   <span data-ttu-id="6307e-107">Columns</span><span class="sxs-lookup"><span data-stu-id="6307e-107">Columns</span></span>  
  
-   <span data-ttu-id="6307e-108">절차</span><span class="sxs-lookup"><span data-stu-id="6307e-108">Procedures</span></span>  
  
-   <span data-ttu-id="6307e-109">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="6307e-109">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="6307e-110">Catalog</span><span class="sxs-lookup"><span data-stu-id="6307e-110">Catalog</span></span>  
  
-   <span data-ttu-id="6307e-111">Indexes</span><span class="sxs-lookup"><span data-stu-id="6307e-111">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="6307e-112">Tables</span><span class="sxs-lookup"><span data-stu-id="6307e-112">Tables</span></span>  
  
|<span data-ttu-id="6307e-113">열 이름</span><span class="sxs-lookup"><span data-stu-id="6307e-113">ColumnName</span></span>|<span data-ttu-id="6307e-114">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6307e-114">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="6307e-115">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-115">TABLE_CATALOG</span></span>|<span data-ttu-id="6307e-116">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-116">String</span></span>|  
|<span data-ttu-id="6307e-117">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-117">TABLE_SCHEMA</span></span>|<span data-ttu-id="6307e-118">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-118">String</span></span>|  
|<span data-ttu-id="6307e-119">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-119">TABLE_NAME</span></span>|<span data-ttu-id="6307e-120">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-120">String</span></span>|  
|<span data-ttu-id="6307e-121">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="6307e-121">TABLE_TYPE</span></span>|<span data-ttu-id="6307e-122">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-122">String</span></span>|  
|<span data-ttu-id="6307e-123">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="6307e-123">TABLE_GUID</span></span>|<span data-ttu-id="6307e-124">Guid</span><span class="sxs-lookup"><span data-stu-id="6307e-124">Guid</span></span>|  
|<span data-ttu-id="6307e-125">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6307e-125">DESCRIPTION</span></span>|<span data-ttu-id="6307e-126">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-126">String</span></span>|  
|<span data-ttu-id="6307e-127">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="6307e-127">TABLE_PROPID</span></span>|<span data-ttu-id="6307e-128">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-128">Int64</span></span>|  
|<span data-ttu-id="6307e-129">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="6307e-129">DATE_CREATED</span></span>|<span data-ttu-id="6307e-130">DateTime</span><span class="sxs-lookup"><span data-stu-id="6307e-130">DateTime</span></span>|  
|<span data-ttu-id="6307e-131">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="6307e-131">DATE_MODIFIED</span></span>|<span data-ttu-id="6307e-132">DateTime</span><span class="sxs-lookup"><span data-stu-id="6307e-132">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="6307e-133">Columns</span><span class="sxs-lookup"><span data-stu-id="6307e-133">Columns</span></span>  
  
|<span data-ttu-id="6307e-134">열 이름</span><span class="sxs-lookup"><span data-stu-id="6307e-134">ColumnName</span></span>|<span data-ttu-id="6307e-135">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6307e-135">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="6307e-136">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-136">TABLE_CATALOG</span></span>|<span data-ttu-id="6307e-137">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-137">String</span></span>|  
|<span data-ttu-id="6307e-138">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-138">TABLE_SCHEMA</span></span>|<span data-ttu-id="6307e-139">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-139">String</span></span>|  
|<span data-ttu-id="6307e-140">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-140">TABLE_NAME</span></span>|<span data-ttu-id="6307e-141">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-141">String</span></span>|  
|<span data-ttu-id="6307e-142">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-142">COLUMN_NAME</span></span>|<span data-ttu-id="6307e-143">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-143">String</span></span>|  
|<span data-ttu-id="6307e-144">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="6307e-144">COLUMN_GUID</span></span>|<span data-ttu-id="6307e-145">Guid</span><span class="sxs-lookup"><span data-stu-id="6307e-145">Guid</span></span>|  
|<span data-ttu-id="6307e-146">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="6307e-146">COLUMN_PROPID</span></span>|<span data-ttu-id="6307e-147">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-147">Int64</span></span>|  
|<span data-ttu-id="6307e-148">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="6307e-148">ORDINAL_POSITION</span></span>|<span data-ttu-id="6307e-149">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-149">Int64</span></span>|  
|<span data-ttu-id="6307e-150">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="6307e-150">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="6307e-151">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-151">Boolean</span></span>|  
|<span data-ttu-id="6307e-152">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6307e-152">COLUMN_DEFAULT</span></span>|<span data-ttu-id="6307e-153">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-153">String</span></span>|  
|<span data-ttu-id="6307e-154">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="6307e-154">COLUMN_FLAGS</span></span>|<span data-ttu-id="6307e-155">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-155">Int64</span></span>|  
|<span data-ttu-id="6307e-156">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="6307e-156">IS_NULLABLE</span></span>|<span data-ttu-id="6307e-157">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-157">Boolean</span></span>|  
|<span data-ttu-id="6307e-158">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="6307e-158">DATA_TYPE</span></span>|<span data-ttu-id="6307e-159">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-159">Int32</span></span>|  
|<span data-ttu-id="6307e-160">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="6307e-160">TYPE_GUID</span></span>|<span data-ttu-id="6307e-161">Guid</span><span class="sxs-lookup"><span data-stu-id="6307e-161">Guid</span></span>|  
|<span data-ttu-id="6307e-162">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="6307e-162">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="6307e-163">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-163">Int64</span></span>|  
|<span data-ttu-id="6307e-164">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="6307e-164">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="6307e-165">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-165">Int64</span></span>|  
|<span data-ttu-id="6307e-166">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="6307e-166">NUMERIC_PRECISION</span></span>|<span data-ttu-id="6307e-167">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-167">Int32</span></span>|  
|<span data-ttu-id="6307e-168">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="6307e-168">NUMERIC_SCALE</span></span>|<span data-ttu-id="6307e-169">Int16</span><span class="sxs-lookup"><span data-stu-id="6307e-169">Int16</span></span>|  
|<span data-ttu-id="6307e-170">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="6307e-170">DATETIME_PRECISION</span></span>|<span data-ttu-id="6307e-171">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-171">Int64</span></span>|  
|<span data-ttu-id="6307e-172">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-172">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="6307e-173">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-173">String</span></span>|  
|<span data-ttu-id="6307e-174">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-174">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="6307e-175">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-175">String</span></span>|  
|<span data-ttu-id="6307e-176">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-176">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="6307e-177">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-177">String</span></span>|  
|<span data-ttu-id="6307e-178">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-178">COLLATION_CATALOG</span></span>|<span data-ttu-id="6307e-179">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-179">String</span></span>|  
|<span data-ttu-id="6307e-180">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-180">COLLATION_SCHEMA</span></span>|<span data-ttu-id="6307e-181">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-181">String</span></span>|  
|<span data-ttu-id="6307e-182">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-182">COLLATION_NAME</span></span>|<span data-ttu-id="6307e-183">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-183">String</span></span>|  
|<span data-ttu-id="6307e-184">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-184">DOMAIN_CATALOG</span></span>|<span data-ttu-id="6307e-185">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-185">String</span></span>|  
|<span data-ttu-id="6307e-186">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-186">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="6307e-187">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-187">String</span></span>|  
|<span data-ttu-id="6307e-188">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-188">DOMAIN_NAME</span></span>|<span data-ttu-id="6307e-189">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-189">String</span></span>|  
|<span data-ttu-id="6307e-190">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6307e-190">DESCRIPTION</span></span>|<span data-ttu-id="6307e-191">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-191">String</span></span>|  
|<span data-ttu-id="6307e-192">COLUMN_LCID</span><span class="sxs-lookup"><span data-stu-id="6307e-192">COLUMN_LCID</span></span>|<span data-ttu-id="6307e-193">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-193">Int32</span></span>|  
|<span data-ttu-id="6307e-194">COLUMN_COMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="6307e-194">COLUMN_COMPFLAGS</span></span>|<span data-ttu-id="6307e-195">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-195">Int32</span></span>|  
|<span data-ttu-id="6307e-196">COLUMN_SORTID</span><span class="sxs-lookup"><span data-stu-id="6307e-196">COLUMN_SORTID</span></span>|<span data-ttu-id="6307e-197">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-197">Int32</span></span>|  
|<span data-ttu-id="6307e-198">COLUMN_TDSCOLLATION</span><span class="sxs-lookup"><span data-stu-id="6307e-198">COLUMN_TDSCOLLATION</span></span>|<span data-ttu-id="6307e-199">Byte[]</span><span class="sxs-lookup"><span data-stu-id="6307e-199">Byte[]</span></span>|  
|<span data-ttu-id="6307e-200">IS_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="6307e-200">IS_COMPUTED</span></span>|<span data-ttu-id="6307e-201">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-201">Boolean</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="6307e-202">절차</span><span class="sxs-lookup"><span data-stu-id="6307e-202">Procedures</span></span>  
  
|<span data-ttu-id="6307e-203">열 이름</span><span class="sxs-lookup"><span data-stu-id="6307e-203">ColumnName</span></span>|<span data-ttu-id="6307e-204">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6307e-204">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="6307e-205">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-205">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="6307e-206">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-206">String</span></span>|  
|<span data-ttu-id="6307e-207">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-207">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="6307e-208">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-208">String</span></span>|  
|<span data-ttu-id="6307e-209">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-209">PROCEDURE_NAME</span></span>|<span data-ttu-id="6307e-210">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-210">String</span></span>|  
|<span data-ttu-id="6307e-211">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="6307e-211">PROCEDURE_TYPE</span></span>|<span data-ttu-id="6307e-212">Int16</span><span class="sxs-lookup"><span data-stu-id="6307e-212">Int16</span></span>|  
|<span data-ttu-id="6307e-213">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="6307e-213">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="6307e-214">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-214">String</span></span>|  
|<span data-ttu-id="6307e-215">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6307e-215">DESCRIPTION</span></span>|<span data-ttu-id="6307e-216">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-216">String</span></span>|  
|<span data-ttu-id="6307e-217">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="6307e-217">DATE_CREATED</span></span>|<span data-ttu-id="6307e-218">DateTime</span><span class="sxs-lookup"><span data-stu-id="6307e-218">DateTime</span></span>|  
|<span data-ttu-id="6307e-219">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="6307e-219">DATE_MODIFIED</span></span>|<span data-ttu-id="6307e-220">DateTime</span><span class="sxs-lookup"><span data-stu-id="6307e-220">DateTime</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="6307e-221">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="6307e-221">ProcedureParameters</span></span>  
  
|<span data-ttu-id="6307e-222">열 이름</span><span class="sxs-lookup"><span data-stu-id="6307e-222">ColumnName</span></span>|<span data-ttu-id="6307e-223">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6307e-223">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="6307e-224">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-224">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="6307e-225">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-225">String</span></span>|  
|<span data-ttu-id="6307e-226">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-226">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="6307e-227">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-227">String</span></span>|  
|<span data-ttu-id="6307e-228">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-228">PROCEDURE_NAME</span></span>|<span data-ttu-id="6307e-229">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-229">String</span></span>|  
|<span data-ttu-id="6307e-230">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-230">PARAMETER_NAME</span></span>|<span data-ttu-id="6307e-231">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-231">String</span></span>|  
|<span data-ttu-id="6307e-232">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="6307e-232">ORDINAL_POSITION</span></span>|<span data-ttu-id="6307e-233">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-233">Int32</span></span>|  
|<span data-ttu-id="6307e-234">PARAMETER_TYPE</span><span class="sxs-lookup"><span data-stu-id="6307e-234">PARAMETER_TYPE</span></span>|<span data-ttu-id="6307e-235">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-235">Int32</span></span>|  
|<span data-ttu-id="6307e-236">PARAMETER_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="6307e-236">PARAMETER_HASDEFAULT</span></span>|<span data-ttu-id="6307e-237">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-237">Boolean</span></span>|  
|<span data-ttu-id="6307e-238">PARAMETER_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6307e-238">PARAMETER_DEFAULT</span></span>|<span data-ttu-id="6307e-239">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-239">String</span></span>|  
|<span data-ttu-id="6307e-240">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="6307e-240">IS_NULLABLE</span></span>|<span data-ttu-id="6307e-241">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-241">Boolean</span></span>|  
|<span data-ttu-id="6307e-242">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="6307e-242">DATA_TYPE</span></span>|<span data-ttu-id="6307e-243">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-243">Int32</span></span>|  
|<span data-ttu-id="6307e-244">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="6307e-244">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="6307e-245">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-245">Int64</span></span>|  
|<span data-ttu-id="6307e-246">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="6307e-246">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="6307e-247">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-247">Int64</span></span>|  
|<span data-ttu-id="6307e-248">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="6307e-248">NUMERIC_PRECISION</span></span>|<span data-ttu-id="6307e-249">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-249">Int32</span></span>|  
|<span data-ttu-id="6307e-250">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="6307e-250">NUMERIC_SCALE</span></span>|<span data-ttu-id="6307e-251">Int16</span><span class="sxs-lookup"><span data-stu-id="6307e-251">Int16</span></span>|  
|<span data-ttu-id="6307e-252">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6307e-252">DESCRIPTION</span></span>|<span data-ttu-id="6307e-253">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-253">String</span></span>|  
|<span data-ttu-id="6307e-254">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-254">TYPE_NAME</span></span>|<span data-ttu-id="6307e-255">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-255">String</span></span>|  
|<span data-ttu-id="6307e-256">LOCAL_TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-256">LOCAL_TYPE_NAME</span></span>|<span data-ttu-id="6307e-257">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-257">String</span></span>|  
  
### <a name="catalog"></a><span data-ttu-id="6307e-258">Catalog</span><span class="sxs-lookup"><span data-stu-id="6307e-258">Catalog</span></span>  
  
|<span data-ttu-id="6307e-259">열 이름</span><span class="sxs-lookup"><span data-stu-id="6307e-259">ColumnName</span></span>|<span data-ttu-id="6307e-260">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6307e-260">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="6307e-261">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-261">CATALOG_NAME</span></span>|<span data-ttu-id="6307e-262">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-262">String</span></span>|  
|<span data-ttu-id="6307e-263">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6307e-263">DESCRIPTION</span></span>|<span data-ttu-id="6307e-264">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-264">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="6307e-265">Indexes</span><span class="sxs-lookup"><span data-stu-id="6307e-265">Indexes</span></span>  
  
|<span data-ttu-id="6307e-266">열 이름</span><span class="sxs-lookup"><span data-stu-id="6307e-266">ColumnName</span></span>|<span data-ttu-id="6307e-267">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6307e-267">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="6307e-268">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-268">TABLE_CATALOG</span></span>|<span data-ttu-id="6307e-269">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-269">String</span></span>|  
|<span data-ttu-id="6307e-270">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-270">TABLE_SCHEMA</span></span>|<span data-ttu-id="6307e-271">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-271">String</span></span>|  
|<span data-ttu-id="6307e-272">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-272">TABLE_NAME</span></span>|<span data-ttu-id="6307e-273">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-273">String</span></span>|  
|<span data-ttu-id="6307e-274">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-274">INDEX_CATALOG</span></span>|<span data-ttu-id="6307e-275">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-275">String</span></span>|  
|<span data-ttu-id="6307e-276">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-276">INDEX_SCHEMA</span></span>|<span data-ttu-id="6307e-277">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-277">String</span></span>|  
|<span data-ttu-id="6307e-278">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-278">INDEX_NAME</span></span>|<span data-ttu-id="6307e-279">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-279">String</span></span>|  
|<span data-ttu-id="6307e-280">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="6307e-280">PRIMARY_KEY</span></span>|<span data-ttu-id="6307e-281">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-281">Boolean</span></span>|  
|<span data-ttu-id="6307e-282">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="6307e-282">UNIQUE</span></span>|<span data-ttu-id="6307e-283">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-283">Boolean</span></span>|  
|<span data-ttu-id="6307e-284">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="6307e-284">CLUSTERED</span></span>|<span data-ttu-id="6307e-285">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-285">Boolean</span></span>|  
|<span data-ttu-id="6307e-286">TYPE</span><span class="sxs-lookup"><span data-stu-id="6307e-286">TYPE</span></span>|<span data-ttu-id="6307e-287">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-287">Int32</span></span>|  
|<span data-ttu-id="6307e-288">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="6307e-288">FILL_FACTOR</span></span>|<span data-ttu-id="6307e-289">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-289">Int32</span></span>|  
|<span data-ttu-id="6307e-290">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="6307e-290">INITIAL_SIZE</span></span>|<span data-ttu-id="6307e-291">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-291">Int32</span></span>|  
|<span data-ttu-id="6307e-292">NULLS</span><span class="sxs-lookup"><span data-stu-id="6307e-292">NULLS</span></span>|<span data-ttu-id="6307e-293">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-293">Int32</span></span>|  
|<span data-ttu-id="6307e-294">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="6307e-294">SORT_BOOKMARKS</span></span>|<span data-ttu-id="6307e-295">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-295">Boolean</span></span>|  
|<span data-ttu-id="6307e-296">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="6307e-296">AUTO_UPDATE</span></span>|<span data-ttu-id="6307e-297">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-297">Boolean</span></span>|  
|<span data-ttu-id="6307e-298">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="6307e-298">NULL_COLLATION</span></span>|<span data-ttu-id="6307e-299">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-299">Int32</span></span>|  
|<span data-ttu-id="6307e-300">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="6307e-300">ORDINAL_POSITION</span></span>|<span data-ttu-id="6307e-301">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-301">Int64</span></span>|  
|<span data-ttu-id="6307e-302">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-302">COLUMN_NAME</span></span>|<span data-ttu-id="6307e-303">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-303">String</span></span>|  
|<span data-ttu-id="6307e-304">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="6307e-304">COLUMN_GUID</span></span>|<span data-ttu-id="6307e-305">Guid</span><span class="sxs-lookup"><span data-stu-id="6307e-305">Guid</span></span>|  
|<span data-ttu-id="6307e-306">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="6307e-306">COLUMN_PROPID</span></span>|<span data-ttu-id="6307e-307">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-307">Int64</span></span>|  
|<span data-ttu-id="6307e-308">COLLATION</span><span class="sxs-lookup"><span data-stu-id="6307e-308">COLLATION</span></span>|<span data-ttu-id="6307e-309">Int16</span><span class="sxs-lookup"><span data-stu-id="6307e-309">Int16</span></span>|  
|<span data-ttu-id="6307e-310">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="6307e-310">CARDINALITY</span></span>|<span data-ttu-id="6307e-311">Decimal</span><span class="sxs-lookup"><span data-stu-id="6307e-311">Decimal</span></span>|  
|<span data-ttu-id="6307e-312">PAGES</span><span class="sxs-lookup"><span data-stu-id="6307e-312">PAGES</span></span>|<span data-ttu-id="6307e-313">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-313">Int32</span></span>|  
|<span data-ttu-id="6307e-314">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="6307e-314">FILTER_CONDITION</span></span>|<span data-ttu-id="6307e-315">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-315">String</span></span>|  
|<span data-ttu-id="6307e-316">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="6307e-316">INTEGRATED</span></span>|<span data-ttu-id="6307e-317">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-317">Boolean</span></span>|  
  
## <a name="microsoft-oracle-ole-db-provider"></a><span data-ttu-id="6307e-318">Microsoft Oracle OLE DB    </span><span class="sxs-lookup"><span data-stu-id="6307e-318">Microsoft Oracle OLE DB Provider</span></span>  
 <span data-ttu-id="6307e-319">Microsoft Oracle OLE DB Driver                                             .</span><span class="sxs-lookup"><span data-stu-id="6307e-319">The Microsoft Oracle OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="6307e-320">Tables</span><span class="sxs-lookup"><span data-stu-id="6307e-320">Tables</span></span>  
  
-   <span data-ttu-id="6307e-321">Columns</span><span class="sxs-lookup"><span data-stu-id="6307e-321">Columns</span></span>  
  
-   <span data-ttu-id="6307e-322">절차</span><span class="sxs-lookup"><span data-stu-id="6307e-322">Procedures</span></span>  
  
-   <span data-ttu-id="6307e-323">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="6307e-323">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="6307e-324">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="6307e-324">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="6307e-325">뷰</span><span class="sxs-lookup"><span data-stu-id="6307e-325">Views</span></span>  
  
-   <span data-ttu-id="6307e-326">Indexes</span><span class="sxs-lookup"><span data-stu-id="6307e-326">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="6307e-327">Tables</span><span class="sxs-lookup"><span data-stu-id="6307e-327">Tables</span></span>  
  
|<span data-ttu-id="6307e-328">열 이름</span><span class="sxs-lookup"><span data-stu-id="6307e-328">ColumnName</span></span>|<span data-ttu-id="6307e-329">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6307e-329">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="6307e-330">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-330">TABLE_CATALOG</span></span>|<span data-ttu-id="6307e-331">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-331">String</span></span>|  
|<span data-ttu-id="6307e-332">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-332">TABLE_SCHEMA</span></span>|<span data-ttu-id="6307e-333">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-333">String</span></span>|  
|<span data-ttu-id="6307e-334">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-334">TABLE_NAME</span></span>|<span data-ttu-id="6307e-335">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-335">String</span></span>|  
|<span data-ttu-id="6307e-336">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="6307e-336">TABLE_TYPE</span></span>|<span data-ttu-id="6307e-337">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-337">String</span></span>|  
|<span data-ttu-id="6307e-338">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="6307e-338">TABLE_GUID</span></span>|<span data-ttu-id="6307e-339">Guid</span><span class="sxs-lookup"><span data-stu-id="6307e-339">Guid</span></span>|  
|<span data-ttu-id="6307e-340">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6307e-340">DESCRIPTION</span></span>|<span data-ttu-id="6307e-341">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-341">String</span></span>|  
|<span data-ttu-id="6307e-342">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="6307e-342">TABLE_PROPID</span></span>|<span data-ttu-id="6307e-343">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-343">Int64</span></span>|  
|<span data-ttu-id="6307e-344">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="6307e-344">DATE_CREATED</span></span>|<span data-ttu-id="6307e-345">DateTime</span><span class="sxs-lookup"><span data-stu-id="6307e-345">DateTime</span></span>|  
|<span data-ttu-id="6307e-346">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="6307e-346">DATE_MODIFIED</span></span>|<span data-ttu-id="6307e-347">DateTime</span><span class="sxs-lookup"><span data-stu-id="6307e-347">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="6307e-348">Columns</span><span class="sxs-lookup"><span data-stu-id="6307e-348">Columns</span></span>  
  
|<span data-ttu-id="6307e-349">열 이름</span><span class="sxs-lookup"><span data-stu-id="6307e-349">ColumnName</span></span>|<span data-ttu-id="6307e-350">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6307e-350">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="6307e-351">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-351">TABLE_CATALOG</span></span>|<span data-ttu-id="6307e-352">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-352">String</span></span>|  
|<span data-ttu-id="6307e-353">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-353">TABLE_SCHEMA</span></span>|<span data-ttu-id="6307e-354">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-354">String</span></span>|  
|<span data-ttu-id="6307e-355">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-355">TABLE_NAME</span></span>|<span data-ttu-id="6307e-356">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-356">String</span></span>|  
|<span data-ttu-id="6307e-357">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-357">COLUMN_NAME</span></span>|<span data-ttu-id="6307e-358">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-358">String</span></span>|  
|<span data-ttu-id="6307e-359">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="6307e-359">COLUMN_GUID</span></span>|<span data-ttu-id="6307e-360">Guid</span><span class="sxs-lookup"><span data-stu-id="6307e-360">Guid</span></span>|  
|<span data-ttu-id="6307e-361">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="6307e-361">COLUMN_PROPID</span></span>|<span data-ttu-id="6307e-362">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-362">Int64</span></span>|  
|<span data-ttu-id="6307e-363">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="6307e-363">ORDINAL_POSITION</span></span>|<span data-ttu-id="6307e-364">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-364">Int64</span></span>|  
|<span data-ttu-id="6307e-365">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="6307e-365">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="6307e-366">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-366">Boolean</span></span>|  
|<span data-ttu-id="6307e-367">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6307e-367">COLUMN_DEFAULT</span></span>|<span data-ttu-id="6307e-368">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-368">String</span></span>|  
|<span data-ttu-id="6307e-369">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="6307e-369">COLUMN_FLAGS</span></span>|<span data-ttu-id="6307e-370">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-370">Int64</span></span>|  
|<span data-ttu-id="6307e-371">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="6307e-371">IS_NULLABLE</span></span>|<span data-ttu-id="6307e-372">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-372">Boolean</span></span>|  
|<span data-ttu-id="6307e-373">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="6307e-373">DATA_TYPE</span></span>|<span data-ttu-id="6307e-374">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-374">Int32</span></span>|  
|<span data-ttu-id="6307e-375">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="6307e-375">TYPE_GUID</span></span>|<span data-ttu-id="6307e-376">Guid</span><span class="sxs-lookup"><span data-stu-id="6307e-376">Guid</span></span>|  
|<span data-ttu-id="6307e-377">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="6307e-377">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="6307e-378">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-378">Int64</span></span>|  
|<span data-ttu-id="6307e-379">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="6307e-379">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="6307e-380">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-380">Int64</span></span>|  
|<span data-ttu-id="6307e-381">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="6307e-381">NUMERIC_PRECISION</span></span>|<span data-ttu-id="6307e-382">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-382">Int32</span></span>|  
|<span data-ttu-id="6307e-383">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="6307e-383">NUMERIC_SCALE</span></span>|<span data-ttu-id="6307e-384">Int16</span><span class="sxs-lookup"><span data-stu-id="6307e-384">Int16</span></span>|  
|<span data-ttu-id="6307e-385">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="6307e-385">DATETIME_PRECISION</span></span>|<span data-ttu-id="6307e-386">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-386">Int64</span></span>|  
|<span data-ttu-id="6307e-387">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-387">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="6307e-388">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-388">String</span></span>|  
|<span data-ttu-id="6307e-389">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-389">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="6307e-390">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-390">String</span></span>|  
|<span data-ttu-id="6307e-391">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-391">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="6307e-392">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-392">String</span></span>|  
|<span data-ttu-id="6307e-393">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-393">COLLATION_CATALOG</span></span>|<span data-ttu-id="6307e-394">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-394">String</span></span>|  
|<span data-ttu-id="6307e-395">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-395">COLLATION_SCHEMA</span></span>|<span data-ttu-id="6307e-396">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-396">String</span></span>|  
|<span data-ttu-id="6307e-397">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-397">COLLATION_NAME</span></span>|<span data-ttu-id="6307e-398">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-398">String</span></span>|  
|<span data-ttu-id="6307e-399">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-399">DOMAIN_CATALOG</span></span>|<span data-ttu-id="6307e-400">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-400">String</span></span>|  
|<span data-ttu-id="6307e-401">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-401">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="6307e-402">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-402">String</span></span>|  
|<span data-ttu-id="6307e-403">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-403">DOMAIN_NAME</span></span>|<span data-ttu-id="6307e-404">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-404">String</span></span>|  
|<span data-ttu-id="6307e-405">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6307e-405">DESCRIPTION</span></span>|<span data-ttu-id="6307e-406">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-406">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="6307e-407">절차</span><span class="sxs-lookup"><span data-stu-id="6307e-407">Procedures</span></span>  
  
|<span data-ttu-id="6307e-408">열 이름</span><span class="sxs-lookup"><span data-stu-id="6307e-408">ColumnName</span></span>|<span data-ttu-id="6307e-409">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6307e-409">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="6307e-410">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-410">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="6307e-411">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-411">String</span></span>|  
|<span data-ttu-id="6307e-412">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-412">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="6307e-413">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-413">String</span></span>|  
|<span data-ttu-id="6307e-414">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-414">PROCEDURE_NAME</span></span>|<span data-ttu-id="6307e-415">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-415">String</span></span>|  
|<span data-ttu-id="6307e-416">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="6307e-416">PROCEDURE_TYPE</span></span>|<span data-ttu-id="6307e-417">Int16</span><span class="sxs-lookup"><span data-stu-id="6307e-417">Int16</span></span>|  
|<span data-ttu-id="6307e-418">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="6307e-418">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="6307e-419">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-419">String</span></span>|  
|<span data-ttu-id="6307e-420">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6307e-420">DESCRIPTION</span></span>|<span data-ttu-id="6307e-421">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-421">String</span></span>|  
|<span data-ttu-id="6307e-422">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="6307e-422">DATE_CREATED</span></span>|<span data-ttu-id="6307e-423">DateTime</span><span class="sxs-lookup"><span data-stu-id="6307e-423">DateTime</span></span>|  
|<span data-ttu-id="6307e-424">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="6307e-424">DATE_MODIFIED</span></span>|<span data-ttu-id="6307e-425">DateTime</span><span class="sxs-lookup"><span data-stu-id="6307e-425">DateTime</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="6307e-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="6307e-426">ProcedureColumns</span></span>  
  
|<span data-ttu-id="6307e-427">열 이름</span><span class="sxs-lookup"><span data-stu-id="6307e-427">ColumnName</span></span>|<span data-ttu-id="6307e-428">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6307e-428">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="6307e-429">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-429">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="6307e-430">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-430">String</span></span>|  
|<span data-ttu-id="6307e-431">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-431">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="6307e-432">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-432">String</span></span>|  
|<span data-ttu-id="6307e-433">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-433">PROCEDURE_NAME</span></span>|<span data-ttu-id="6307e-434">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-434">String</span></span>|  
|<span data-ttu-id="6307e-435">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-435">COLUMN_NAME</span></span>|<span data-ttu-id="6307e-436">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-436">String</span></span>|  
|<span data-ttu-id="6307e-437">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="6307e-437">COLUMN_GUID</span></span>|<span data-ttu-id="6307e-438">Guid</span><span class="sxs-lookup"><span data-stu-id="6307e-438">Guid</span></span>|  
|<span data-ttu-id="6307e-439">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="6307e-439">COLUMN_PROPID</span></span>|<span data-ttu-id="6307e-440">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-440">Int64</span></span>|  
|<span data-ttu-id="6307e-441">ROWSET_NUMBER</span><span class="sxs-lookup"><span data-stu-id="6307e-441">ROWSET_NUMBER</span></span>|<span data-ttu-id="6307e-442">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-442">Int64</span></span>|  
|<span data-ttu-id="6307e-443">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="6307e-443">ORDINAL_POSITION</span></span>|<span data-ttu-id="6307e-444">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-444">Int64</span></span>|  
|<span data-ttu-id="6307e-445">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="6307e-445">IS_NULLABLE</span></span>|<span data-ttu-id="6307e-446">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-446">Boolean</span></span>|  
|<span data-ttu-id="6307e-447">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="6307e-447">DATA_TYPE</span></span>|<span data-ttu-id="6307e-448">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-448">Int32</span></span>|  
|<span data-ttu-id="6307e-449">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="6307e-449">TYPE_GUID</span></span>|<span data-ttu-id="6307e-450">Guid</span><span class="sxs-lookup"><span data-stu-id="6307e-450">Guid</span></span>|  
|<span data-ttu-id="6307e-451">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="6307e-451">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="6307e-452">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-452">Int64</span></span>|  
|<span data-ttu-id="6307e-453">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="6307e-453">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="6307e-454">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-454">Int64</span></span>|  
|<span data-ttu-id="6307e-455">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="6307e-455">NUMERIC_PRECISION</span></span>|<span data-ttu-id="6307e-456">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-456">Int32</span></span>|  
|<span data-ttu-id="6307e-457">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="6307e-457">NUMERIC_SCALE</span></span>|<span data-ttu-id="6307e-458">Int16</span><span class="sxs-lookup"><span data-stu-id="6307e-458">Int16</span></span>|  
|<span data-ttu-id="6307e-459">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6307e-459">DESCRIPTION</span></span>|<span data-ttu-id="6307e-460">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-460">String</span></span>|  
|<span data-ttu-id="6307e-461">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="6307e-461">OVERLOAD</span></span>|<span data-ttu-id="6307e-462">Int16</span><span class="sxs-lookup"><span data-stu-id="6307e-462">Int16</span></span>|  
  
### <a name="views"></a><span data-ttu-id="6307e-463">뷰</span><span class="sxs-lookup"><span data-stu-id="6307e-463">Views</span></span>  
  
|<span data-ttu-id="6307e-464">열 이름</span><span class="sxs-lookup"><span data-stu-id="6307e-464">ColumnName</span></span>|<span data-ttu-id="6307e-465">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6307e-465">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="6307e-466">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-466">TABLE_CATALOG</span></span>|<span data-ttu-id="6307e-467">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-467">String</span></span>|  
|<span data-ttu-id="6307e-468">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-468">TABLE_SCHEMA</span></span>|<span data-ttu-id="6307e-469">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-469">String</span></span>|  
|<span data-ttu-id="6307e-470">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-470">TABLE_NAME</span></span>|<span data-ttu-id="6307e-471">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-471">String</span></span>|  
|<span data-ttu-id="6307e-472">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="6307e-472">VIEW_DEFINITION</span></span>|<span data-ttu-id="6307e-473">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-473">String</span></span>|  
|<span data-ttu-id="6307e-474">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="6307e-474">CHECK_OPTION</span></span>|<span data-ttu-id="6307e-475">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-475">Boolean</span></span>|  
|<span data-ttu-id="6307e-476">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="6307e-476">IS_UPDATABLE</span></span>|<span data-ttu-id="6307e-477">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-477">Boolean</span></span>|  
|<span data-ttu-id="6307e-478">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6307e-478">DESCRIPTION</span></span>|<span data-ttu-id="6307e-479">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-479">String</span></span>|  
|<span data-ttu-id="6307e-480">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="6307e-480">DATE_CREATED</span></span>|<span data-ttu-id="6307e-481">DateTime</span><span class="sxs-lookup"><span data-stu-id="6307e-481">DateTime</span></span>|  
|<span data-ttu-id="6307e-482">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="6307e-482">DATE_MODIFIED</span></span>|<span data-ttu-id="6307e-483">DateTime</span><span class="sxs-lookup"><span data-stu-id="6307e-483">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="6307e-484">Indexes</span><span class="sxs-lookup"><span data-stu-id="6307e-484">Indexes</span></span>  
  
|<span data-ttu-id="6307e-485">열 이름</span><span class="sxs-lookup"><span data-stu-id="6307e-485">ColumnName</span></span>|<span data-ttu-id="6307e-486">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6307e-486">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="6307e-487">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-487">TABLE_CATALOG</span></span>|<span data-ttu-id="6307e-488">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-488">String</span></span>|  
|<span data-ttu-id="6307e-489">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-489">TABLE_SCHEMA</span></span>|<span data-ttu-id="6307e-490">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-490">String</span></span>|  
|<span data-ttu-id="6307e-491">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-491">TABLE_NAME</span></span>|<span data-ttu-id="6307e-492">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-492">String</span></span>|  
|<span data-ttu-id="6307e-493">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-493">INDEX_CATALOG</span></span>|<span data-ttu-id="6307e-494">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-494">String</span></span>|  
|<span data-ttu-id="6307e-495">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-495">INDEX_SCHEMA</span></span>|<span data-ttu-id="6307e-496">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-496">String</span></span>|  
|<span data-ttu-id="6307e-497">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-497">INDEX_NAME</span></span>|<span data-ttu-id="6307e-498">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-498">String</span></span>|  
|<span data-ttu-id="6307e-499">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="6307e-499">PRIMARY_KEY</span></span>|<span data-ttu-id="6307e-500">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-500">Boolean</span></span>|  
|<span data-ttu-id="6307e-501">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="6307e-501">UNIQUE</span></span>|<span data-ttu-id="6307e-502">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-502">Boolean</span></span>|  
|<span data-ttu-id="6307e-503">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="6307e-503">CLUSTERED</span></span>|<span data-ttu-id="6307e-504">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-504">Boolean</span></span>|  
|<span data-ttu-id="6307e-505">TYPE</span><span class="sxs-lookup"><span data-stu-id="6307e-505">TYPE</span></span>|<span data-ttu-id="6307e-506">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-506">Int32</span></span>|  
|<span data-ttu-id="6307e-507">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="6307e-507">FILL_FACTOR</span></span>|<span data-ttu-id="6307e-508">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-508">Int32</span></span>|  
|<span data-ttu-id="6307e-509">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="6307e-509">INITIAL_SIZE</span></span>|<span data-ttu-id="6307e-510">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-510">Int32</span></span>|  
|<span data-ttu-id="6307e-511">NULLS</span><span class="sxs-lookup"><span data-stu-id="6307e-511">NULLS</span></span>|<span data-ttu-id="6307e-512">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-512">Int32</span></span>|  
|<span data-ttu-id="6307e-513">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="6307e-513">SORT_BOOKMARKS</span></span>|<span data-ttu-id="6307e-514">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-514">Boolean</span></span>|  
|<span data-ttu-id="6307e-515">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="6307e-515">AUTO_UPDATE</span></span>|<span data-ttu-id="6307e-516">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-516">Boolean</span></span>|  
|<span data-ttu-id="6307e-517">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="6307e-517">NULL_COLLATION</span></span>|<span data-ttu-id="6307e-518">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-518">Int32</span></span>|  
|<span data-ttu-id="6307e-519">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="6307e-519">ORDINAL_POSITION</span></span>|<span data-ttu-id="6307e-520">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-520">Int64</span></span>|  
|<span data-ttu-id="6307e-521">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-521">COLUMN_NAME</span></span>|<span data-ttu-id="6307e-522">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-522">String</span></span>|  
|<span data-ttu-id="6307e-523">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="6307e-523">COLUMN_GUID</span></span>|<span data-ttu-id="6307e-524">Guid</span><span class="sxs-lookup"><span data-stu-id="6307e-524">Guid</span></span>|  
|<span data-ttu-id="6307e-525">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="6307e-525">COLUMN_PROPID</span></span>|<span data-ttu-id="6307e-526">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-526">Int64</span></span>|  
|<span data-ttu-id="6307e-527">COLLATION</span><span class="sxs-lookup"><span data-stu-id="6307e-527">COLLATION</span></span>|<span data-ttu-id="6307e-528">Int16</span><span class="sxs-lookup"><span data-stu-id="6307e-528">Int16</span></span>|  
|<span data-ttu-id="6307e-529">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="6307e-529">CARDINALITY</span></span>|<span data-ttu-id="6307e-530">Decimal</span><span class="sxs-lookup"><span data-stu-id="6307e-530">Decimal</span></span>|  
|<span data-ttu-id="6307e-531">PAGES</span><span class="sxs-lookup"><span data-stu-id="6307e-531">PAGES</span></span>|<span data-ttu-id="6307e-532">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-532">Int32</span></span>|  
|<span data-ttu-id="6307e-533">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="6307e-533">FILTER_CONDITION</span></span>|<span data-ttu-id="6307e-534">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-534">String</span></span>|  
|<span data-ttu-id="6307e-535">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="6307e-535">INTEGRATED</span></span>|<span data-ttu-id="6307e-536">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-536">Boolean</span></span>|  
  
## <a name="microsoft-jet-ole-db-provider"></a><span data-ttu-id="6307e-537">Microsoft Jet OLE DB    </span><span class="sxs-lookup"><span data-stu-id="6307e-537">Microsoft Jet OLE DB Provider</span></span>  
 <span data-ttu-id="6307e-538">Microsoft Jet OLE DB Driver                                             .</span><span class="sxs-lookup"><span data-stu-id="6307e-538">The Microsoft Jet OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="6307e-539">Tables</span><span class="sxs-lookup"><span data-stu-id="6307e-539">Tables</span></span>  
  
-   <span data-ttu-id="6307e-540">Columns</span><span class="sxs-lookup"><span data-stu-id="6307e-540">Columns</span></span>  
  
-   <span data-ttu-id="6307e-541">절차</span><span class="sxs-lookup"><span data-stu-id="6307e-541">Procedures</span></span>  
  
-   <span data-ttu-id="6307e-542">뷰</span><span class="sxs-lookup"><span data-stu-id="6307e-542">Views</span></span>  
  
-   <span data-ttu-id="6307e-543">Indexes</span><span class="sxs-lookup"><span data-stu-id="6307e-543">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="6307e-544">Tables</span><span class="sxs-lookup"><span data-stu-id="6307e-544">Tables</span></span>  
  
|<span data-ttu-id="6307e-545">열 이름</span><span class="sxs-lookup"><span data-stu-id="6307e-545">ColumnName</span></span>|<span data-ttu-id="6307e-546">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6307e-546">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="6307e-547">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-547">TABLE_CATALOG</span></span>|<span data-ttu-id="6307e-548">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-548">String</span></span>|  
|<span data-ttu-id="6307e-549">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-549">TABLE_SCHEMA</span></span>|<span data-ttu-id="6307e-550">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-550">String</span></span>|  
|<span data-ttu-id="6307e-551">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-551">TABLE_NAME</span></span>|<span data-ttu-id="6307e-552">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-552">String</span></span>|  
|<span data-ttu-id="6307e-553">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="6307e-553">TABLE_TYPE</span></span>|<span data-ttu-id="6307e-554">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-554">String</span></span>|  
|<span data-ttu-id="6307e-555">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="6307e-555">TABLE_GUID</span></span>|<span data-ttu-id="6307e-556">Guid</span><span class="sxs-lookup"><span data-stu-id="6307e-556">Guid</span></span>|  
|<span data-ttu-id="6307e-557">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6307e-557">DESCRIPTION</span></span>|<span data-ttu-id="6307e-558">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-558">String</span></span>|  
|<span data-ttu-id="6307e-559">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="6307e-559">TABLE_PROPID</span></span>|<span data-ttu-id="6307e-560">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-560">Int64</span></span>|  
|<span data-ttu-id="6307e-561">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="6307e-561">DATE_CREATED</span></span>|<span data-ttu-id="6307e-562">DateTime</span><span class="sxs-lookup"><span data-stu-id="6307e-562">DateTime</span></span>|  
|<span data-ttu-id="6307e-563">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="6307e-563">DATE_MODIFIED</span></span>|<span data-ttu-id="6307e-564">DateTime</span><span class="sxs-lookup"><span data-stu-id="6307e-564">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="6307e-565">Columns</span><span class="sxs-lookup"><span data-stu-id="6307e-565">Columns</span></span>  
  
|<span data-ttu-id="6307e-566">열 이름</span><span class="sxs-lookup"><span data-stu-id="6307e-566">ColumnName</span></span>|<span data-ttu-id="6307e-567">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6307e-567">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="6307e-568">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-568">TABLE_CATALOG</span></span>|<span data-ttu-id="6307e-569">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-569">String</span></span>|  
|<span data-ttu-id="6307e-570">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-570">TABLE_SCHEMA</span></span>|<span data-ttu-id="6307e-571">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-571">String</span></span>|  
|<span data-ttu-id="6307e-572">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-572">TABLE_NAME</span></span>|<span data-ttu-id="6307e-573">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-573">String</span></span>|  
|<span data-ttu-id="6307e-574">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-574">COLUMN_NAME</span></span>|<span data-ttu-id="6307e-575">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-575">String</span></span>|  
|<span data-ttu-id="6307e-576">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="6307e-576">COLUMN_GUID</span></span>|<span data-ttu-id="6307e-577">Guid</span><span class="sxs-lookup"><span data-stu-id="6307e-577">Guid</span></span>|  
|<span data-ttu-id="6307e-578">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="6307e-578">COLUMN_PROPID</span></span>|<span data-ttu-id="6307e-579">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-579">Int64</span></span>|  
|<span data-ttu-id="6307e-580">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="6307e-580">ORDINAL_POSITION</span></span>|<span data-ttu-id="6307e-581">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-581">Int64</span></span>|  
|<span data-ttu-id="6307e-582">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="6307e-582">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="6307e-583">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-583">Boolean</span></span>|  
|<span data-ttu-id="6307e-584">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6307e-584">COLUMN_DEFAULT</span></span>|<span data-ttu-id="6307e-585">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-585">String</span></span>|  
|<span data-ttu-id="6307e-586">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="6307e-586">COLUMN_FLAGS</span></span>|<span data-ttu-id="6307e-587">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-587">Int64</span></span>|  
|<span data-ttu-id="6307e-588">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="6307e-588">IS_NULLABLE</span></span>|<span data-ttu-id="6307e-589">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-589">Boolean</span></span>|  
|<span data-ttu-id="6307e-590">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="6307e-590">DATA_TYPE</span></span>|<span data-ttu-id="6307e-591">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-591">Int32</span></span>|  
|<span data-ttu-id="6307e-592">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="6307e-592">TYPE_GUID</span></span>|<span data-ttu-id="6307e-593">Guid</span><span class="sxs-lookup"><span data-stu-id="6307e-593">Guid</span></span>|  
|<span data-ttu-id="6307e-594">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="6307e-594">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="6307e-595">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-595">Int64</span></span>|  
|<span data-ttu-id="6307e-596">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="6307e-596">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="6307e-597">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-597">Int64</span></span>|  
|<span data-ttu-id="6307e-598">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="6307e-598">NUMERIC_PRECISION</span></span>|<span data-ttu-id="6307e-599">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-599">Int32</span></span>|  
|<span data-ttu-id="6307e-600">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="6307e-600">NUMERIC_SCALE</span></span>|<span data-ttu-id="6307e-601">Int16</span><span class="sxs-lookup"><span data-stu-id="6307e-601">Int16</span></span>|  
|<span data-ttu-id="6307e-602">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="6307e-602">DATETIME_PRECISION</span></span>|<span data-ttu-id="6307e-603">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-603">Int64</span></span>|  
|<span data-ttu-id="6307e-604">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-604">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="6307e-605">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-605">String</span></span>|  
|<span data-ttu-id="6307e-606">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-606">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="6307e-607">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-607">String</span></span>|  
|<span data-ttu-id="6307e-608">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-608">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="6307e-609">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-609">String</span></span>|  
|<span data-ttu-id="6307e-610">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-610">COLLATION_CATALOG</span></span>|<span data-ttu-id="6307e-611">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-611">String</span></span>|  
|<span data-ttu-id="6307e-612">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-612">COLLATION_SCHEMA</span></span>|<span data-ttu-id="6307e-613">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-613">String</span></span>|  
|<span data-ttu-id="6307e-614">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-614">COLLATION_NAME</span></span>|<span data-ttu-id="6307e-615">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-615">String</span></span>|  
|<span data-ttu-id="6307e-616">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-616">DOMAIN_CATALOG</span></span>|<span data-ttu-id="6307e-617">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-617">String</span></span>|  
|<span data-ttu-id="6307e-618">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-618">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="6307e-619">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-619">String</span></span>|  
|<span data-ttu-id="6307e-620">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-620">DOMAIN_NAME</span></span>|<span data-ttu-id="6307e-621">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-621">String</span></span>|  
|<span data-ttu-id="6307e-622">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6307e-622">DESCRIPTION</span></span>|<span data-ttu-id="6307e-623">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-623">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="6307e-624">절차</span><span class="sxs-lookup"><span data-stu-id="6307e-624">Procedures</span></span>  
  
|<span data-ttu-id="6307e-625">열 이름</span><span class="sxs-lookup"><span data-stu-id="6307e-625">ColumnName</span></span>|<span data-ttu-id="6307e-626">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6307e-626">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="6307e-627">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-627">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="6307e-628">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-628">String</span></span>|  
|<span data-ttu-id="6307e-629">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-629">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="6307e-630">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-630">String</span></span>|  
|<span data-ttu-id="6307e-631">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-631">PROCEDURE_NAME</span></span>|<span data-ttu-id="6307e-632">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-632">String</span></span>|  
|<span data-ttu-id="6307e-633">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="6307e-633">PROCEDURE_TYPE</span></span>|<span data-ttu-id="6307e-634">Int16</span><span class="sxs-lookup"><span data-stu-id="6307e-634">Int16</span></span>|  
|<span data-ttu-id="6307e-635">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="6307e-635">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="6307e-636">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-636">String</span></span>|  
|<span data-ttu-id="6307e-637">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6307e-637">DESCRIPTION</span></span>|<span data-ttu-id="6307e-638">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-638">String</span></span>|  
|<span data-ttu-id="6307e-639">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="6307e-639">DATE_CREATED</span></span>|<span data-ttu-id="6307e-640">DateTime</span><span class="sxs-lookup"><span data-stu-id="6307e-640">DateTime</span></span>|  
|<span data-ttu-id="6307e-641">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="6307e-641">DATE_MODIFIED</span></span>|<span data-ttu-id="6307e-642">DateTime</span><span class="sxs-lookup"><span data-stu-id="6307e-642">DateTime</span></span>|  
  
### <a name="views"></a><span data-ttu-id="6307e-643">뷰</span><span class="sxs-lookup"><span data-stu-id="6307e-643">Views</span></span>  
  
|<span data-ttu-id="6307e-644">열 이름</span><span class="sxs-lookup"><span data-stu-id="6307e-644">ColumnName</span></span>|<span data-ttu-id="6307e-645">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6307e-645">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="6307e-646">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-646">TABLE_CATALOG</span></span>|<span data-ttu-id="6307e-647">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-647">String</span></span>|  
|<span data-ttu-id="6307e-648">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-648">TABLE_SCHEMA</span></span>|<span data-ttu-id="6307e-649">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-649">String</span></span>|  
|<span data-ttu-id="6307e-650">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-650">TABLE_NAME</span></span>|<span data-ttu-id="6307e-651">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-651">String</span></span>|  
|<span data-ttu-id="6307e-652">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="6307e-652">VIEW_DEFINITION</span></span>|<span data-ttu-id="6307e-653">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-653">String</span></span>|  
|<span data-ttu-id="6307e-654">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="6307e-654">CHECK_OPTION</span></span>|<span data-ttu-id="6307e-655">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-655">Boolean</span></span>|  
|<span data-ttu-id="6307e-656">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="6307e-656">IS_UPDATABLE</span></span>|<span data-ttu-id="6307e-657">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-657">Boolean</span></span>|  
|<span data-ttu-id="6307e-658">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6307e-658">DESCRIPTION</span></span>|<span data-ttu-id="6307e-659">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-659">String</span></span>|  
|<span data-ttu-id="6307e-660">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="6307e-660">DATE_CREATED</span></span>|<span data-ttu-id="6307e-661">DateTime</span><span class="sxs-lookup"><span data-stu-id="6307e-661">DateTime</span></span>|  
|<span data-ttu-id="6307e-662">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="6307e-662">DATE_MODIFIED</span></span>|<span data-ttu-id="6307e-663">DateTime</span><span class="sxs-lookup"><span data-stu-id="6307e-663">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="6307e-664">Indexes</span><span class="sxs-lookup"><span data-stu-id="6307e-664">Indexes</span></span>  
  
|<span data-ttu-id="6307e-665">열 이름</span><span class="sxs-lookup"><span data-stu-id="6307e-665">ColumnName</span></span>|<span data-ttu-id="6307e-666">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6307e-666">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="6307e-667">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-667">TABLE_CATALOG</span></span>|<span data-ttu-id="6307e-668">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-668">String</span></span>|  
|<span data-ttu-id="6307e-669">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-669">TABLE_SCHEMA</span></span>|<span data-ttu-id="6307e-670">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-670">String</span></span>|  
|<span data-ttu-id="6307e-671">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-671">TABLE_NAME</span></span>|<span data-ttu-id="6307e-672">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-672">String</span></span>|  
|<span data-ttu-id="6307e-673">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6307e-673">INDEX_CATALOG</span></span>|<span data-ttu-id="6307e-674">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-674">String</span></span>|  
|<span data-ttu-id="6307e-675">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6307e-675">INDEX_SCHEMA</span></span>|<span data-ttu-id="6307e-676">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-676">String</span></span>|  
|<span data-ttu-id="6307e-677">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-677">INDEX_NAME</span></span>|<span data-ttu-id="6307e-678">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-678">String</span></span>|  
|<span data-ttu-id="6307e-679">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="6307e-679">PRIMARY_KEY</span></span>|<span data-ttu-id="6307e-680">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-680">Boolean</span></span>|  
|<span data-ttu-id="6307e-681">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="6307e-681">UNIQUE</span></span>|<span data-ttu-id="6307e-682">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-682">Boolean</span></span>|  
|<span data-ttu-id="6307e-683">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="6307e-683">CLUSTERED</span></span>|<span data-ttu-id="6307e-684">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-684">Boolean</span></span>|  
|<span data-ttu-id="6307e-685">TYPE</span><span class="sxs-lookup"><span data-stu-id="6307e-685">TYPE</span></span>|<span data-ttu-id="6307e-686">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-686">Int32</span></span>|  
|<span data-ttu-id="6307e-687">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="6307e-687">FILL_FACTOR</span></span>|<span data-ttu-id="6307e-688">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-688">Int32</span></span>|  
|<span data-ttu-id="6307e-689">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="6307e-689">INITIAL_SIZE</span></span>|<span data-ttu-id="6307e-690">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-690">Int32</span></span>|  
|<span data-ttu-id="6307e-691">NULLS</span><span class="sxs-lookup"><span data-stu-id="6307e-691">NULLS</span></span>|<span data-ttu-id="6307e-692">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-692">Int32</span></span>|  
|<span data-ttu-id="6307e-693">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="6307e-693">SORT_BOOKMARKS</span></span>|<span data-ttu-id="6307e-694">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-694">Boolean</span></span>|  
|<span data-ttu-id="6307e-695">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="6307e-695">AUTO_UPDATE</span></span>|<span data-ttu-id="6307e-696">Boolean</span><span class="sxs-lookup"><span data-stu-id="6307e-696">Boolean</span></span>|  
|<span data-ttu-id="6307e-697">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="6307e-697">NULL_COLLATION</span></span>|<span data-ttu-id="6307e-698">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-698">Int32</span></span>|  
|<span data-ttu-id="6307e-699">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="6307e-699">ORDINAL_POSITION</span></span>|<span data-ttu-id="6307e-700">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-700">Int64</span></span>|  
|<span data-ttu-id="6307e-701">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="6307e-701">COLUMN_NAME</span></span>|<span data-ttu-id="6307e-702">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-702">String</span></span>|  
|<span data-ttu-id="6307e-703">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="6307e-703">COLUMN_GUID</span></span>|<span data-ttu-id="6307e-704">Guid</span><span class="sxs-lookup"><span data-stu-id="6307e-704">Guid</span></span>|  
|<span data-ttu-id="6307e-705">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="6307e-705">COLUMN_PROPID</span></span>|<span data-ttu-id="6307e-706">Int64</span><span class="sxs-lookup"><span data-stu-id="6307e-706">Int64</span></span>|  
|<span data-ttu-id="6307e-707">COLLATION</span><span class="sxs-lookup"><span data-stu-id="6307e-707">COLLATION</span></span>|<span data-ttu-id="6307e-708">Int16</span><span class="sxs-lookup"><span data-stu-id="6307e-708">Int16</span></span>|  
|<span data-ttu-id="6307e-709">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="6307e-709">CARDINALITY</span></span>|<span data-ttu-id="6307e-710">Decimal</span><span class="sxs-lookup"><span data-stu-id="6307e-710">Decimal</span></span>|  
|<span data-ttu-id="6307e-711">PAGES</span><span class="sxs-lookup"><span data-stu-id="6307e-711">PAGES</span></span>|<span data-ttu-id="6307e-712">Int32</span><span class="sxs-lookup"><span data-stu-id="6307e-712">Int32</span></span>|  
|<span data-ttu-id="6307e-713">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="6307e-713">FILTER_CONDITION</span></span>|<span data-ttu-id="6307e-714">문자열</span><span class="sxs-lookup"><span data-stu-id="6307e-714">String</span></span>|  
|<span data-ttu-id="6307e-715">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="6307e-715">INTEGRATED</span></span>|<span data-ttu-id="6307e-716">부울</span><span class="sxs-lookup"><span data-stu-id="6307e-716">Boolean</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6307e-717">참고자료</span><span class="sxs-lookup"><span data-stu-id="6307e-717">See also</span></span>
- [<span data-ttu-id="6307e-718">ADO.NET 관리되는 공급자 및 데이터 집합 개발자 센터</span><span class="sxs-lookup"><span data-stu-id="6307e-718">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
