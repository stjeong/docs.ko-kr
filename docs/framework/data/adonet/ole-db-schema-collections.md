---
title: OLE DB 스키마 컬렉션
ms.date: 03/30/2017
ms.assetid: 6380c36b-658e-4d67-91e8-7131ef4a7c2c
ms.openlocfilehash: 1ab6426875b73b400a59b7e4cf155615d7472d05
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43514491"
---
# <a name="ole-db-schema-collections"></a><span data-ttu-id="c3e48-102">OLE DB 스키마 컬렉션</span><span class="sxs-lookup"><span data-stu-id="c3e48-102">OLE DB Schema Collections</span></span>
<span data-ttu-id="c3e48-103">이 단원에서는 Microsoft SQL Server, Oracle 및 Microsoft Jet용 OLE DB 공급자에서 지원하는 스키마 컬렉션에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e48-103">This section discusses schema collection support for the OLE DB providers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-ole-db-provider"></a><span data-ttu-id="c3e48-104">Microsoft SQL Server OLE DB 공급자</span><span class="sxs-lookup"><span data-stu-id="c3e48-104">Microsoft SQL Server OLE DB Provider</span></span>  
 <span data-ttu-id="c3e48-105">Microsoft SQL Server OLE DB Driver에서는 공통 스키마 컬렉션 외에도 다음과 같은 특정 스키마 컬렉션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e48-105">The Microsoft SQL Server OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="c3e48-106">Tables</span><span class="sxs-lookup"><span data-stu-id="c3e48-106">Tables</span></span>  
  
-   <span data-ttu-id="c3e48-107">Columns</span><span class="sxs-lookup"><span data-stu-id="c3e48-107">Columns</span></span>  
  
-   <span data-ttu-id="c3e48-108">절차</span><span class="sxs-lookup"><span data-stu-id="c3e48-108">Procedures</span></span>  
  
-   <span data-ttu-id="c3e48-109">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="c3e48-109">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="c3e48-110">Catalog</span><span class="sxs-lookup"><span data-stu-id="c3e48-110">Catalog</span></span>  
  
-   <span data-ttu-id="c3e48-111">Indexes</span><span class="sxs-lookup"><span data-stu-id="c3e48-111">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="c3e48-112">Tables</span><span class="sxs-lookup"><span data-stu-id="c3e48-112">Tables</span></span>  
  
|<span data-ttu-id="c3e48-113">열 이름</span><span class="sxs-lookup"><span data-stu-id="c3e48-113">ColumnName</span></span>|<span data-ttu-id="c3e48-114">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c3e48-114">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c3e48-115">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-115">TABLE_CATALOG</span></span>|<span data-ttu-id="c3e48-116">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-116">String</span></span>|  
|<span data-ttu-id="c3e48-117">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-117">TABLE_SCHEMA</span></span>|<span data-ttu-id="c3e48-118">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-118">String</span></span>|  
|<span data-ttu-id="c3e48-119">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-119">TABLE_NAME</span></span>|<span data-ttu-id="c3e48-120">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-120">String</span></span>|  
|<span data-ttu-id="c3e48-121">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c3e48-121">TABLE_TYPE</span></span>|<span data-ttu-id="c3e48-122">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-122">String</span></span>|  
|<span data-ttu-id="c3e48-123">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="c3e48-123">TABLE_GUID</span></span>|<span data-ttu-id="c3e48-124">Guid</span><span class="sxs-lookup"><span data-stu-id="c3e48-124">Guid</span></span>|  
|<span data-ttu-id="c3e48-125">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c3e48-125">DESCRIPTION</span></span>|<span data-ttu-id="c3e48-126">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-126">String</span></span>|  
|<span data-ttu-id="c3e48-127">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="c3e48-127">TABLE_PROPID</span></span>|<span data-ttu-id="c3e48-128">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-128">Int64</span></span>|  
|<span data-ttu-id="c3e48-129">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="c3e48-129">DATE_CREATED</span></span>|<span data-ttu-id="c3e48-130">DateTime</span><span class="sxs-lookup"><span data-stu-id="c3e48-130">DateTime</span></span>|  
|<span data-ttu-id="c3e48-131">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="c3e48-131">DATE_MODIFIED</span></span>|<span data-ttu-id="c3e48-132">DateTime</span><span class="sxs-lookup"><span data-stu-id="c3e48-132">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="c3e48-133">Columns</span><span class="sxs-lookup"><span data-stu-id="c3e48-133">Columns</span></span>  
  
|<span data-ttu-id="c3e48-134">열 이름</span><span class="sxs-lookup"><span data-stu-id="c3e48-134">ColumnName</span></span>|<span data-ttu-id="c3e48-135">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c3e48-135">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c3e48-136">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-136">TABLE_CATALOG</span></span>|<span data-ttu-id="c3e48-137">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-137">String</span></span>|  
|<span data-ttu-id="c3e48-138">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-138">TABLE_SCHEMA</span></span>|<span data-ttu-id="c3e48-139">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-139">String</span></span>|  
|<span data-ttu-id="c3e48-140">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-140">TABLE_NAME</span></span>|<span data-ttu-id="c3e48-141">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-141">String</span></span>|  
|<span data-ttu-id="c3e48-142">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-142">COLUMN_NAME</span></span>|<span data-ttu-id="c3e48-143">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-143">String</span></span>|  
|<span data-ttu-id="c3e48-144">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="c3e48-144">COLUMN_GUID</span></span>|<span data-ttu-id="c3e48-145">Guid</span><span class="sxs-lookup"><span data-stu-id="c3e48-145">Guid</span></span>|  
|<span data-ttu-id="c3e48-146">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="c3e48-146">COLUMN_PROPID</span></span>|<span data-ttu-id="c3e48-147">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-147">Int64</span></span>|  
|<span data-ttu-id="c3e48-148">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c3e48-148">ORDINAL_POSITION</span></span>|<span data-ttu-id="c3e48-149">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-149">Int64</span></span>|  
|<span data-ttu-id="c3e48-150">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3e48-150">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="c3e48-151">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-151">Boolean</span></span>|  
|<span data-ttu-id="c3e48-152">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3e48-152">COLUMN_DEFAULT</span></span>|<span data-ttu-id="c3e48-153">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-153">String</span></span>|  
|<span data-ttu-id="c3e48-154">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="c3e48-154">COLUMN_FLAGS</span></span>|<span data-ttu-id="c3e48-155">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-155">Int64</span></span>|  
|<span data-ttu-id="c3e48-156">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c3e48-156">IS_NULLABLE</span></span>|<span data-ttu-id="c3e48-157">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-157">Boolean</span></span>|  
|<span data-ttu-id="c3e48-158">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c3e48-158">DATA_TYPE</span></span>|<span data-ttu-id="c3e48-159">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-159">Int32</span></span>|  
|<span data-ttu-id="c3e48-160">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="c3e48-160">TYPE_GUID</span></span>|<span data-ttu-id="c3e48-161">Guid</span><span class="sxs-lookup"><span data-stu-id="c3e48-161">Guid</span></span>|  
|<span data-ttu-id="c3e48-162">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c3e48-162">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="c3e48-163">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-163">Int64</span></span>|  
|<span data-ttu-id="c3e48-164">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c3e48-164">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="c3e48-165">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-165">Int64</span></span>|  
|<span data-ttu-id="c3e48-166">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="c3e48-166">NUMERIC_PRECISION</span></span>|<span data-ttu-id="c3e48-167">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-167">Int32</span></span>|  
|<span data-ttu-id="c3e48-168">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="c3e48-168">NUMERIC_SCALE</span></span>|<span data-ttu-id="c3e48-169">Int16</span><span class="sxs-lookup"><span data-stu-id="c3e48-169">Int16</span></span>|  
|<span data-ttu-id="c3e48-170">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="c3e48-170">DATETIME_PRECISION</span></span>|<span data-ttu-id="c3e48-171">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-171">Int64</span></span>|  
|<span data-ttu-id="c3e48-172">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-172">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="c3e48-173">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-173">String</span></span>|  
|<span data-ttu-id="c3e48-174">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-174">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="c3e48-175">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-175">String</span></span>|  
|<span data-ttu-id="c3e48-176">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-176">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="c3e48-177">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-177">String</span></span>|  
|<span data-ttu-id="c3e48-178">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-178">COLLATION_CATALOG</span></span>|<span data-ttu-id="c3e48-179">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-179">String</span></span>|  
|<span data-ttu-id="c3e48-180">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-180">COLLATION_SCHEMA</span></span>|<span data-ttu-id="c3e48-181">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-181">String</span></span>|  
|<span data-ttu-id="c3e48-182">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-182">COLLATION_NAME</span></span>|<span data-ttu-id="c3e48-183">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-183">String</span></span>|  
|<span data-ttu-id="c3e48-184">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-184">DOMAIN_CATALOG</span></span>|<span data-ttu-id="c3e48-185">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-185">String</span></span>|  
|<span data-ttu-id="c3e48-186">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-186">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="c3e48-187">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-187">String</span></span>|  
|<span data-ttu-id="c3e48-188">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-188">DOMAIN_NAME</span></span>|<span data-ttu-id="c3e48-189">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-189">String</span></span>|  
|<span data-ttu-id="c3e48-190">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c3e48-190">DESCRIPTION</span></span>|<span data-ttu-id="c3e48-191">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-191">String</span></span>|  
|<span data-ttu-id="c3e48-192">COLUMN_LCID</span><span class="sxs-lookup"><span data-stu-id="c3e48-192">COLUMN_LCID</span></span>|<span data-ttu-id="c3e48-193">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-193">Int32</span></span>|  
|<span data-ttu-id="c3e48-194">COLUMN_COMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="c3e48-194">COLUMN_COMPFLAGS</span></span>|<span data-ttu-id="c3e48-195">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-195">Int32</span></span>|  
|<span data-ttu-id="c3e48-196">COLUMN_SORTID</span><span class="sxs-lookup"><span data-stu-id="c3e48-196">COLUMN_SORTID</span></span>|<span data-ttu-id="c3e48-197">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-197">Int32</span></span>|  
|<span data-ttu-id="c3e48-198">COLUMN_TDSCOLLATION</span><span class="sxs-lookup"><span data-stu-id="c3e48-198">COLUMN_TDSCOLLATION</span></span>|<span data-ttu-id="c3e48-199">Byte[]</span><span class="sxs-lookup"><span data-stu-id="c3e48-199">Byte[]</span></span>|  
|<span data-ttu-id="c3e48-200">IS_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="c3e48-200">IS_COMPUTED</span></span>|<span data-ttu-id="c3e48-201">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-201">Boolean</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="c3e48-202">절차</span><span class="sxs-lookup"><span data-stu-id="c3e48-202">Procedures</span></span>  
  
|<span data-ttu-id="c3e48-203">열 이름</span><span class="sxs-lookup"><span data-stu-id="c3e48-203">ColumnName</span></span>|<span data-ttu-id="c3e48-204">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c3e48-204">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c3e48-205">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-205">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="c3e48-206">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-206">String</span></span>|  
|<span data-ttu-id="c3e48-207">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-207">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="c3e48-208">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-208">String</span></span>|  
|<span data-ttu-id="c3e48-209">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-209">PROCEDURE_NAME</span></span>|<span data-ttu-id="c3e48-210">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-210">String</span></span>|  
|<span data-ttu-id="c3e48-211">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c3e48-211">PROCEDURE_TYPE</span></span>|<span data-ttu-id="c3e48-212">Int16</span><span class="sxs-lookup"><span data-stu-id="c3e48-212">Int16</span></span>|  
|<span data-ttu-id="c3e48-213">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="c3e48-213">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="c3e48-214">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-214">String</span></span>|  
|<span data-ttu-id="c3e48-215">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c3e48-215">DESCRIPTION</span></span>|<span data-ttu-id="c3e48-216">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-216">String</span></span>|  
|<span data-ttu-id="c3e48-217">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="c3e48-217">DATE_CREATED</span></span>|<span data-ttu-id="c3e48-218">DateTime</span><span class="sxs-lookup"><span data-stu-id="c3e48-218">DateTime</span></span>|  
|<span data-ttu-id="c3e48-219">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="c3e48-219">DATE_MODIFIED</span></span>|<span data-ttu-id="c3e48-220">DateTime</span><span class="sxs-lookup"><span data-stu-id="c3e48-220">DateTime</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="c3e48-221">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="c3e48-221">ProcedureParameters</span></span>  
  
|<span data-ttu-id="c3e48-222">열 이름</span><span class="sxs-lookup"><span data-stu-id="c3e48-222">ColumnName</span></span>|<span data-ttu-id="c3e48-223">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c3e48-223">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c3e48-224">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-224">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="c3e48-225">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-225">String</span></span>|  
|<span data-ttu-id="c3e48-226">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-226">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="c3e48-227">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-227">String</span></span>|  
|<span data-ttu-id="c3e48-228">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-228">PROCEDURE_NAME</span></span>|<span data-ttu-id="c3e48-229">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-229">String</span></span>|  
|<span data-ttu-id="c3e48-230">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-230">PARAMETER_NAME</span></span>|<span data-ttu-id="c3e48-231">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-231">String</span></span>|  
|<span data-ttu-id="c3e48-232">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c3e48-232">ORDINAL_POSITION</span></span>|<span data-ttu-id="c3e48-233">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-233">Int32</span></span>|  
|<span data-ttu-id="c3e48-234">PARAMETER_TYPE</span><span class="sxs-lookup"><span data-stu-id="c3e48-234">PARAMETER_TYPE</span></span>|<span data-ttu-id="c3e48-235">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-235">Int32</span></span>|  
|<span data-ttu-id="c3e48-236">PARAMETER_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3e48-236">PARAMETER_HASDEFAULT</span></span>|<span data-ttu-id="c3e48-237">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-237">Boolean</span></span>|  
|<span data-ttu-id="c3e48-238">PARAMETER_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3e48-238">PARAMETER_DEFAULT</span></span>|<span data-ttu-id="c3e48-239">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-239">String</span></span>|  
|<span data-ttu-id="c3e48-240">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c3e48-240">IS_NULLABLE</span></span>|<span data-ttu-id="c3e48-241">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-241">Boolean</span></span>|  
|<span data-ttu-id="c3e48-242">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c3e48-242">DATA_TYPE</span></span>|<span data-ttu-id="c3e48-243">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-243">Int32</span></span>|  
|<span data-ttu-id="c3e48-244">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c3e48-244">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="c3e48-245">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-245">Int64</span></span>|  
|<span data-ttu-id="c3e48-246">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c3e48-246">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="c3e48-247">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-247">Int64</span></span>|  
|<span data-ttu-id="c3e48-248">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="c3e48-248">NUMERIC_PRECISION</span></span>|<span data-ttu-id="c3e48-249">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-249">Int32</span></span>|  
|<span data-ttu-id="c3e48-250">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="c3e48-250">NUMERIC_SCALE</span></span>|<span data-ttu-id="c3e48-251">Int16</span><span class="sxs-lookup"><span data-stu-id="c3e48-251">Int16</span></span>|  
|<span data-ttu-id="c3e48-252">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c3e48-252">DESCRIPTION</span></span>|<span data-ttu-id="c3e48-253">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-253">String</span></span>|  
|<span data-ttu-id="c3e48-254">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-254">TYPE_NAME</span></span>|<span data-ttu-id="c3e48-255">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-255">String</span></span>|  
|<span data-ttu-id="c3e48-256">LOCAL_TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-256">LOCAL_TYPE_NAME</span></span>|<span data-ttu-id="c3e48-257">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-257">String</span></span>|  
  
### <a name="catalog"></a><span data-ttu-id="c3e48-258">Catalog</span><span class="sxs-lookup"><span data-stu-id="c3e48-258">Catalog</span></span>  
  
|<span data-ttu-id="c3e48-259">열 이름</span><span class="sxs-lookup"><span data-stu-id="c3e48-259">ColumnName</span></span>|<span data-ttu-id="c3e48-260">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c3e48-260">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c3e48-261">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-261">CATALOG_NAME</span></span>|<span data-ttu-id="c3e48-262">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-262">String</span></span>|  
|<span data-ttu-id="c3e48-263">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c3e48-263">DESCRIPTION</span></span>|<span data-ttu-id="c3e48-264">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-264">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="c3e48-265">Indexes</span><span class="sxs-lookup"><span data-stu-id="c3e48-265">Indexes</span></span>  
  
|<span data-ttu-id="c3e48-266">열 이름</span><span class="sxs-lookup"><span data-stu-id="c3e48-266">ColumnName</span></span>|<span data-ttu-id="c3e48-267">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c3e48-267">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c3e48-268">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-268">TABLE_CATALOG</span></span>|<span data-ttu-id="c3e48-269">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-269">String</span></span>|  
|<span data-ttu-id="c3e48-270">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-270">TABLE_SCHEMA</span></span>|<span data-ttu-id="c3e48-271">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-271">String</span></span>|  
|<span data-ttu-id="c3e48-272">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-272">TABLE_NAME</span></span>|<span data-ttu-id="c3e48-273">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-273">String</span></span>|  
|<span data-ttu-id="c3e48-274">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-274">INDEX_CATALOG</span></span>|<span data-ttu-id="c3e48-275">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-275">String</span></span>|  
|<span data-ttu-id="c3e48-276">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-276">INDEX_SCHEMA</span></span>|<span data-ttu-id="c3e48-277">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-277">String</span></span>|  
|<span data-ttu-id="c3e48-278">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-278">INDEX_NAME</span></span>|<span data-ttu-id="c3e48-279">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-279">String</span></span>|  
|<span data-ttu-id="c3e48-280">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="c3e48-280">PRIMARY_KEY</span></span>|<span data-ttu-id="c3e48-281">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-281">Boolean</span></span>|  
|<span data-ttu-id="c3e48-282">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="c3e48-282">UNIQUE</span></span>|<span data-ttu-id="c3e48-283">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-283">Boolean</span></span>|  
|<span data-ttu-id="c3e48-284">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="c3e48-284">CLUSTERED</span></span>|<span data-ttu-id="c3e48-285">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-285">Boolean</span></span>|  
|<span data-ttu-id="c3e48-286">TYPE</span><span class="sxs-lookup"><span data-stu-id="c3e48-286">TYPE</span></span>|<span data-ttu-id="c3e48-287">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-287">Int32</span></span>|  
|<span data-ttu-id="c3e48-288">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="c3e48-288">FILL_FACTOR</span></span>|<span data-ttu-id="c3e48-289">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-289">Int32</span></span>|  
|<span data-ttu-id="c3e48-290">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="c3e48-290">INITIAL_SIZE</span></span>|<span data-ttu-id="c3e48-291">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-291">Int32</span></span>|  
|<span data-ttu-id="c3e48-292">NULLS</span><span class="sxs-lookup"><span data-stu-id="c3e48-292">NULLS</span></span>|<span data-ttu-id="c3e48-293">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-293">Int32</span></span>|  
|<span data-ttu-id="c3e48-294">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c3e48-294">SORT_BOOKMARKS</span></span>|<span data-ttu-id="c3e48-295">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-295">Boolean</span></span>|  
|<span data-ttu-id="c3e48-296">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="c3e48-296">AUTO_UPDATE</span></span>|<span data-ttu-id="c3e48-297">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-297">Boolean</span></span>|  
|<span data-ttu-id="c3e48-298">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="c3e48-298">NULL_COLLATION</span></span>|<span data-ttu-id="c3e48-299">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-299">Int32</span></span>|  
|<span data-ttu-id="c3e48-300">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c3e48-300">ORDINAL_POSITION</span></span>|<span data-ttu-id="c3e48-301">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-301">Int64</span></span>|  
|<span data-ttu-id="c3e48-302">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-302">COLUMN_NAME</span></span>|<span data-ttu-id="c3e48-303">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-303">String</span></span>|  
|<span data-ttu-id="c3e48-304">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="c3e48-304">COLUMN_GUID</span></span>|<span data-ttu-id="c3e48-305">Guid</span><span class="sxs-lookup"><span data-stu-id="c3e48-305">Guid</span></span>|  
|<span data-ttu-id="c3e48-306">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="c3e48-306">COLUMN_PROPID</span></span>|<span data-ttu-id="c3e48-307">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-307">Int64</span></span>|  
|<span data-ttu-id="c3e48-308">COLLATION</span><span class="sxs-lookup"><span data-stu-id="c3e48-308">COLLATION</span></span>|<span data-ttu-id="c3e48-309">Int16</span><span class="sxs-lookup"><span data-stu-id="c3e48-309">Int16</span></span>|  
|<span data-ttu-id="c3e48-310">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="c3e48-310">CARDINALITY</span></span>|<span data-ttu-id="c3e48-311">Decimal</span><span class="sxs-lookup"><span data-stu-id="c3e48-311">Decimal</span></span>|  
|<span data-ttu-id="c3e48-312">PAGES</span><span class="sxs-lookup"><span data-stu-id="c3e48-312">PAGES</span></span>|<span data-ttu-id="c3e48-313">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-313">Int32</span></span>|  
|<span data-ttu-id="c3e48-314">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="c3e48-314">FILTER_CONDITION</span></span>|<span data-ttu-id="c3e48-315">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-315">String</span></span>|  
|<span data-ttu-id="c3e48-316">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="c3e48-316">INTEGRATED</span></span>|<span data-ttu-id="c3e48-317">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-317">Boolean</span></span>|  
  
## <a name="microsoft-oracle-ole-db-provider"></a><span data-ttu-id="c3e48-318">Microsoft Oracle OLE DB    </span><span class="sxs-lookup"><span data-stu-id="c3e48-318">Microsoft Oracle OLE DB Provider</span></span>  
 <span data-ttu-id="c3e48-319">Microsoft Oracle OLE DB Driver                                             .</span><span class="sxs-lookup"><span data-stu-id="c3e48-319">The Microsoft Oracle OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="c3e48-320">Tables</span><span class="sxs-lookup"><span data-stu-id="c3e48-320">Tables</span></span>  
  
-   <span data-ttu-id="c3e48-321">Columns</span><span class="sxs-lookup"><span data-stu-id="c3e48-321">Columns</span></span>  
  
-   <span data-ttu-id="c3e48-322">절차</span><span class="sxs-lookup"><span data-stu-id="c3e48-322">Procedures</span></span>  
  
-   <span data-ttu-id="c3e48-323">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="c3e48-323">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="c3e48-324">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="c3e48-324">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="c3e48-325">뷰</span><span class="sxs-lookup"><span data-stu-id="c3e48-325">Views</span></span>  
  
-   <span data-ttu-id="c3e48-326">Indexes</span><span class="sxs-lookup"><span data-stu-id="c3e48-326">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="c3e48-327">Tables</span><span class="sxs-lookup"><span data-stu-id="c3e48-327">Tables</span></span>  
  
|<span data-ttu-id="c3e48-328">열 이름</span><span class="sxs-lookup"><span data-stu-id="c3e48-328">ColumnName</span></span>|<span data-ttu-id="c3e48-329">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c3e48-329">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c3e48-330">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-330">TABLE_CATALOG</span></span>|<span data-ttu-id="c3e48-331">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-331">String</span></span>|  
|<span data-ttu-id="c3e48-332">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-332">TABLE_SCHEMA</span></span>|<span data-ttu-id="c3e48-333">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-333">String</span></span>|  
|<span data-ttu-id="c3e48-334">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-334">TABLE_NAME</span></span>|<span data-ttu-id="c3e48-335">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-335">String</span></span>|  
|<span data-ttu-id="c3e48-336">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c3e48-336">TABLE_TYPE</span></span>|<span data-ttu-id="c3e48-337">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-337">String</span></span>|  
|<span data-ttu-id="c3e48-338">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="c3e48-338">TABLE_GUID</span></span>|<span data-ttu-id="c3e48-339">Guid</span><span class="sxs-lookup"><span data-stu-id="c3e48-339">Guid</span></span>|  
|<span data-ttu-id="c3e48-340">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c3e48-340">DESCRIPTION</span></span>|<span data-ttu-id="c3e48-341">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-341">String</span></span>|  
|<span data-ttu-id="c3e48-342">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="c3e48-342">TABLE_PROPID</span></span>|<span data-ttu-id="c3e48-343">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-343">Int64</span></span>|  
|<span data-ttu-id="c3e48-344">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="c3e48-344">DATE_CREATED</span></span>|<span data-ttu-id="c3e48-345">DateTime</span><span class="sxs-lookup"><span data-stu-id="c3e48-345">DateTime</span></span>|  
|<span data-ttu-id="c3e48-346">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="c3e48-346">DATE_MODIFIED</span></span>|<span data-ttu-id="c3e48-347">DateTime</span><span class="sxs-lookup"><span data-stu-id="c3e48-347">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="c3e48-348">Columns</span><span class="sxs-lookup"><span data-stu-id="c3e48-348">Columns</span></span>  
  
|<span data-ttu-id="c3e48-349">열 이름</span><span class="sxs-lookup"><span data-stu-id="c3e48-349">ColumnName</span></span>|<span data-ttu-id="c3e48-350">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c3e48-350">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c3e48-351">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-351">TABLE_CATALOG</span></span>|<span data-ttu-id="c3e48-352">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-352">String</span></span>|  
|<span data-ttu-id="c3e48-353">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-353">TABLE_SCHEMA</span></span>|<span data-ttu-id="c3e48-354">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-354">String</span></span>|  
|<span data-ttu-id="c3e48-355">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-355">TABLE_NAME</span></span>|<span data-ttu-id="c3e48-356">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-356">String</span></span>|  
|<span data-ttu-id="c3e48-357">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-357">COLUMN_NAME</span></span>|<span data-ttu-id="c3e48-358">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-358">String</span></span>|  
|<span data-ttu-id="c3e48-359">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="c3e48-359">COLUMN_GUID</span></span>|<span data-ttu-id="c3e48-360">Guid</span><span class="sxs-lookup"><span data-stu-id="c3e48-360">Guid</span></span>|  
|<span data-ttu-id="c3e48-361">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="c3e48-361">COLUMN_PROPID</span></span>|<span data-ttu-id="c3e48-362">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-362">Int64</span></span>|  
|<span data-ttu-id="c3e48-363">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c3e48-363">ORDINAL_POSITION</span></span>|<span data-ttu-id="c3e48-364">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-364">Int64</span></span>|  
|<span data-ttu-id="c3e48-365">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3e48-365">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="c3e48-366">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-366">Boolean</span></span>|  
|<span data-ttu-id="c3e48-367">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3e48-367">COLUMN_DEFAULT</span></span>|<span data-ttu-id="c3e48-368">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-368">String</span></span>|  
|<span data-ttu-id="c3e48-369">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="c3e48-369">COLUMN_FLAGS</span></span>|<span data-ttu-id="c3e48-370">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-370">Int64</span></span>|  
|<span data-ttu-id="c3e48-371">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c3e48-371">IS_NULLABLE</span></span>|<span data-ttu-id="c3e48-372">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-372">Boolean</span></span>|  
|<span data-ttu-id="c3e48-373">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c3e48-373">DATA_TYPE</span></span>|<span data-ttu-id="c3e48-374">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-374">Int32</span></span>|  
|<span data-ttu-id="c3e48-375">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="c3e48-375">TYPE_GUID</span></span>|<span data-ttu-id="c3e48-376">Guid</span><span class="sxs-lookup"><span data-stu-id="c3e48-376">Guid</span></span>|  
|<span data-ttu-id="c3e48-377">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c3e48-377">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="c3e48-378">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-378">Int64</span></span>|  
|<span data-ttu-id="c3e48-379">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c3e48-379">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="c3e48-380">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-380">Int64</span></span>|  
|<span data-ttu-id="c3e48-381">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="c3e48-381">NUMERIC_PRECISION</span></span>|<span data-ttu-id="c3e48-382">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-382">Int32</span></span>|  
|<span data-ttu-id="c3e48-383">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="c3e48-383">NUMERIC_SCALE</span></span>|<span data-ttu-id="c3e48-384">Int16</span><span class="sxs-lookup"><span data-stu-id="c3e48-384">Int16</span></span>|  
|<span data-ttu-id="c3e48-385">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="c3e48-385">DATETIME_PRECISION</span></span>|<span data-ttu-id="c3e48-386">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-386">Int64</span></span>|  
|<span data-ttu-id="c3e48-387">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-387">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="c3e48-388">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-388">String</span></span>|  
|<span data-ttu-id="c3e48-389">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-389">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="c3e48-390">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-390">String</span></span>|  
|<span data-ttu-id="c3e48-391">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-391">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="c3e48-392">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-392">String</span></span>|  
|<span data-ttu-id="c3e48-393">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-393">COLLATION_CATALOG</span></span>|<span data-ttu-id="c3e48-394">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-394">String</span></span>|  
|<span data-ttu-id="c3e48-395">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-395">COLLATION_SCHEMA</span></span>|<span data-ttu-id="c3e48-396">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-396">String</span></span>|  
|<span data-ttu-id="c3e48-397">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-397">COLLATION_NAME</span></span>|<span data-ttu-id="c3e48-398">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-398">String</span></span>|  
|<span data-ttu-id="c3e48-399">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-399">DOMAIN_CATALOG</span></span>|<span data-ttu-id="c3e48-400">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-400">String</span></span>|  
|<span data-ttu-id="c3e48-401">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-401">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="c3e48-402">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-402">String</span></span>|  
|<span data-ttu-id="c3e48-403">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-403">DOMAIN_NAME</span></span>|<span data-ttu-id="c3e48-404">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-404">String</span></span>|  
|<span data-ttu-id="c3e48-405">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c3e48-405">DESCRIPTION</span></span>|<span data-ttu-id="c3e48-406">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-406">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="c3e48-407">절차</span><span class="sxs-lookup"><span data-stu-id="c3e48-407">Procedures</span></span>  
  
|<span data-ttu-id="c3e48-408">열 이름</span><span class="sxs-lookup"><span data-stu-id="c3e48-408">ColumnName</span></span>|<span data-ttu-id="c3e48-409">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c3e48-409">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c3e48-410">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-410">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="c3e48-411">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-411">String</span></span>|  
|<span data-ttu-id="c3e48-412">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-412">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="c3e48-413">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-413">String</span></span>|  
|<span data-ttu-id="c3e48-414">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-414">PROCEDURE_NAME</span></span>|<span data-ttu-id="c3e48-415">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-415">String</span></span>|  
|<span data-ttu-id="c3e48-416">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c3e48-416">PROCEDURE_TYPE</span></span>|<span data-ttu-id="c3e48-417">Int16</span><span class="sxs-lookup"><span data-stu-id="c3e48-417">Int16</span></span>|  
|<span data-ttu-id="c3e48-418">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="c3e48-418">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="c3e48-419">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-419">String</span></span>|  
|<span data-ttu-id="c3e48-420">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c3e48-420">DESCRIPTION</span></span>|<span data-ttu-id="c3e48-421">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-421">String</span></span>|  
|<span data-ttu-id="c3e48-422">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="c3e48-422">DATE_CREATED</span></span>|<span data-ttu-id="c3e48-423">DateTime</span><span class="sxs-lookup"><span data-stu-id="c3e48-423">DateTime</span></span>|  
|<span data-ttu-id="c3e48-424">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="c3e48-424">DATE_MODIFIED</span></span>|<span data-ttu-id="c3e48-425">DateTime</span><span class="sxs-lookup"><span data-stu-id="c3e48-425">DateTime</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="c3e48-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="c3e48-426">ProcedureColumns</span></span>  
  
|<span data-ttu-id="c3e48-427">열 이름</span><span class="sxs-lookup"><span data-stu-id="c3e48-427">ColumnName</span></span>|<span data-ttu-id="c3e48-428">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c3e48-428">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c3e48-429">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-429">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="c3e48-430">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-430">String</span></span>|  
|<span data-ttu-id="c3e48-431">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-431">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="c3e48-432">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-432">String</span></span>|  
|<span data-ttu-id="c3e48-433">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-433">PROCEDURE_NAME</span></span>|<span data-ttu-id="c3e48-434">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-434">String</span></span>|  
|<span data-ttu-id="c3e48-435">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-435">COLUMN_NAME</span></span>|<span data-ttu-id="c3e48-436">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-436">String</span></span>|  
|<span data-ttu-id="c3e48-437">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="c3e48-437">COLUMN_GUID</span></span>|<span data-ttu-id="c3e48-438">Guid</span><span class="sxs-lookup"><span data-stu-id="c3e48-438">Guid</span></span>|  
|<span data-ttu-id="c3e48-439">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="c3e48-439">COLUMN_PROPID</span></span>|<span data-ttu-id="c3e48-440">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-440">Int64</span></span>|  
|<span data-ttu-id="c3e48-441">ROWSET_NUMBER</span><span class="sxs-lookup"><span data-stu-id="c3e48-441">ROWSET_NUMBER</span></span>|<span data-ttu-id="c3e48-442">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-442">Int64</span></span>|  
|<span data-ttu-id="c3e48-443">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c3e48-443">ORDINAL_POSITION</span></span>|<span data-ttu-id="c3e48-444">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-444">Int64</span></span>|  
|<span data-ttu-id="c3e48-445">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c3e48-445">IS_NULLABLE</span></span>|<span data-ttu-id="c3e48-446">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-446">Boolean</span></span>|  
|<span data-ttu-id="c3e48-447">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c3e48-447">DATA_TYPE</span></span>|<span data-ttu-id="c3e48-448">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-448">Int32</span></span>|  
|<span data-ttu-id="c3e48-449">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="c3e48-449">TYPE_GUID</span></span>|<span data-ttu-id="c3e48-450">Guid</span><span class="sxs-lookup"><span data-stu-id="c3e48-450">Guid</span></span>|  
|<span data-ttu-id="c3e48-451">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c3e48-451">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="c3e48-452">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-452">Int64</span></span>|  
|<span data-ttu-id="c3e48-453">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c3e48-453">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="c3e48-454">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-454">Int64</span></span>|  
|<span data-ttu-id="c3e48-455">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="c3e48-455">NUMERIC_PRECISION</span></span>|<span data-ttu-id="c3e48-456">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-456">Int32</span></span>|  
|<span data-ttu-id="c3e48-457">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="c3e48-457">NUMERIC_SCALE</span></span>|<span data-ttu-id="c3e48-458">Int16</span><span class="sxs-lookup"><span data-stu-id="c3e48-458">Int16</span></span>|  
|<span data-ttu-id="c3e48-459">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c3e48-459">DESCRIPTION</span></span>|<span data-ttu-id="c3e48-460">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-460">String</span></span>|  
|<span data-ttu-id="c3e48-461">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="c3e48-461">OVERLOAD</span></span>|<span data-ttu-id="c3e48-462">Int16</span><span class="sxs-lookup"><span data-stu-id="c3e48-462">Int16</span></span>|  
  
### <a name="views"></a><span data-ttu-id="c3e48-463">뷰</span><span class="sxs-lookup"><span data-stu-id="c3e48-463">Views</span></span>  
  
|<span data-ttu-id="c3e48-464">열 이름</span><span class="sxs-lookup"><span data-stu-id="c3e48-464">ColumnName</span></span>|<span data-ttu-id="c3e48-465">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c3e48-465">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c3e48-466">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-466">TABLE_CATALOG</span></span>|<span data-ttu-id="c3e48-467">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-467">String</span></span>|  
|<span data-ttu-id="c3e48-468">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-468">TABLE_SCHEMA</span></span>|<span data-ttu-id="c3e48-469">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-469">String</span></span>|  
|<span data-ttu-id="c3e48-470">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-470">TABLE_NAME</span></span>|<span data-ttu-id="c3e48-471">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-471">String</span></span>|  
|<span data-ttu-id="c3e48-472">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="c3e48-472">VIEW_DEFINITION</span></span>|<span data-ttu-id="c3e48-473">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-473">String</span></span>|  
|<span data-ttu-id="c3e48-474">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="c3e48-474">CHECK_OPTION</span></span>|<span data-ttu-id="c3e48-475">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-475">Boolean</span></span>|  
|<span data-ttu-id="c3e48-476">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="c3e48-476">IS_UPDATABLE</span></span>|<span data-ttu-id="c3e48-477">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-477">Boolean</span></span>|  
|<span data-ttu-id="c3e48-478">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c3e48-478">DESCRIPTION</span></span>|<span data-ttu-id="c3e48-479">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-479">String</span></span>|  
|<span data-ttu-id="c3e48-480">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="c3e48-480">DATE_CREATED</span></span>|<span data-ttu-id="c3e48-481">DateTime</span><span class="sxs-lookup"><span data-stu-id="c3e48-481">DateTime</span></span>|  
|<span data-ttu-id="c3e48-482">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="c3e48-482">DATE_MODIFIED</span></span>|<span data-ttu-id="c3e48-483">DateTime</span><span class="sxs-lookup"><span data-stu-id="c3e48-483">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="c3e48-484">Indexes</span><span class="sxs-lookup"><span data-stu-id="c3e48-484">Indexes</span></span>  
  
|<span data-ttu-id="c3e48-485">열 이름</span><span class="sxs-lookup"><span data-stu-id="c3e48-485">ColumnName</span></span>|<span data-ttu-id="c3e48-486">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c3e48-486">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c3e48-487">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-487">TABLE_CATALOG</span></span>|<span data-ttu-id="c3e48-488">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-488">String</span></span>|  
|<span data-ttu-id="c3e48-489">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-489">TABLE_SCHEMA</span></span>|<span data-ttu-id="c3e48-490">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-490">String</span></span>|  
|<span data-ttu-id="c3e48-491">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-491">TABLE_NAME</span></span>|<span data-ttu-id="c3e48-492">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-492">String</span></span>|  
|<span data-ttu-id="c3e48-493">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-493">INDEX_CATALOG</span></span>|<span data-ttu-id="c3e48-494">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-494">String</span></span>|  
|<span data-ttu-id="c3e48-495">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-495">INDEX_SCHEMA</span></span>|<span data-ttu-id="c3e48-496">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-496">String</span></span>|  
|<span data-ttu-id="c3e48-497">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-497">INDEX_NAME</span></span>|<span data-ttu-id="c3e48-498">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-498">String</span></span>|  
|<span data-ttu-id="c3e48-499">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="c3e48-499">PRIMARY_KEY</span></span>|<span data-ttu-id="c3e48-500">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-500">Boolean</span></span>|  
|<span data-ttu-id="c3e48-501">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="c3e48-501">UNIQUE</span></span>|<span data-ttu-id="c3e48-502">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-502">Boolean</span></span>|  
|<span data-ttu-id="c3e48-503">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="c3e48-503">CLUSTERED</span></span>|<span data-ttu-id="c3e48-504">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-504">Boolean</span></span>|  
|<span data-ttu-id="c3e48-505">TYPE</span><span class="sxs-lookup"><span data-stu-id="c3e48-505">TYPE</span></span>|<span data-ttu-id="c3e48-506">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-506">Int32</span></span>|  
|<span data-ttu-id="c3e48-507">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="c3e48-507">FILL_FACTOR</span></span>|<span data-ttu-id="c3e48-508">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-508">Int32</span></span>|  
|<span data-ttu-id="c3e48-509">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="c3e48-509">INITIAL_SIZE</span></span>|<span data-ttu-id="c3e48-510">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-510">Int32</span></span>|  
|<span data-ttu-id="c3e48-511">NULLS</span><span class="sxs-lookup"><span data-stu-id="c3e48-511">NULLS</span></span>|<span data-ttu-id="c3e48-512">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-512">Int32</span></span>|  
|<span data-ttu-id="c3e48-513">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c3e48-513">SORT_BOOKMARKS</span></span>|<span data-ttu-id="c3e48-514">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-514">Boolean</span></span>|  
|<span data-ttu-id="c3e48-515">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="c3e48-515">AUTO_UPDATE</span></span>|<span data-ttu-id="c3e48-516">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-516">Boolean</span></span>|  
|<span data-ttu-id="c3e48-517">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="c3e48-517">NULL_COLLATION</span></span>|<span data-ttu-id="c3e48-518">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-518">Int32</span></span>|  
|<span data-ttu-id="c3e48-519">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c3e48-519">ORDINAL_POSITION</span></span>|<span data-ttu-id="c3e48-520">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-520">Int64</span></span>|  
|<span data-ttu-id="c3e48-521">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-521">COLUMN_NAME</span></span>|<span data-ttu-id="c3e48-522">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-522">String</span></span>|  
|<span data-ttu-id="c3e48-523">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="c3e48-523">COLUMN_GUID</span></span>|<span data-ttu-id="c3e48-524">Guid</span><span class="sxs-lookup"><span data-stu-id="c3e48-524">Guid</span></span>|  
|<span data-ttu-id="c3e48-525">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="c3e48-525">COLUMN_PROPID</span></span>|<span data-ttu-id="c3e48-526">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-526">Int64</span></span>|  
|<span data-ttu-id="c3e48-527">COLLATION</span><span class="sxs-lookup"><span data-stu-id="c3e48-527">COLLATION</span></span>|<span data-ttu-id="c3e48-528">Int16</span><span class="sxs-lookup"><span data-stu-id="c3e48-528">Int16</span></span>|  
|<span data-ttu-id="c3e48-529">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="c3e48-529">CARDINALITY</span></span>|<span data-ttu-id="c3e48-530">Decimal</span><span class="sxs-lookup"><span data-stu-id="c3e48-530">Decimal</span></span>|  
|<span data-ttu-id="c3e48-531">PAGES</span><span class="sxs-lookup"><span data-stu-id="c3e48-531">PAGES</span></span>|<span data-ttu-id="c3e48-532">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-532">Int32</span></span>|  
|<span data-ttu-id="c3e48-533">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="c3e48-533">FILTER_CONDITION</span></span>|<span data-ttu-id="c3e48-534">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-534">String</span></span>|  
|<span data-ttu-id="c3e48-535">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="c3e48-535">INTEGRATED</span></span>|<span data-ttu-id="c3e48-536">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-536">Boolean</span></span>|  
  
## <a name="microsoft-jet-ole-db-provider"></a><span data-ttu-id="c3e48-537">Microsoft Jet OLE DB    </span><span class="sxs-lookup"><span data-stu-id="c3e48-537">Microsoft Jet OLE DB Provider</span></span>  
 <span data-ttu-id="c3e48-538">Microsoft Jet OLE DB Driver                                             .</span><span class="sxs-lookup"><span data-stu-id="c3e48-538">The Microsoft Jet OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="c3e48-539">Tables</span><span class="sxs-lookup"><span data-stu-id="c3e48-539">Tables</span></span>  
  
-   <span data-ttu-id="c3e48-540">Columns</span><span class="sxs-lookup"><span data-stu-id="c3e48-540">Columns</span></span>  
  
-   <span data-ttu-id="c3e48-541">절차</span><span class="sxs-lookup"><span data-stu-id="c3e48-541">Procedures</span></span>  
  
-   <span data-ttu-id="c3e48-542">뷰</span><span class="sxs-lookup"><span data-stu-id="c3e48-542">Views</span></span>  
  
-   <span data-ttu-id="c3e48-543">Indexes</span><span class="sxs-lookup"><span data-stu-id="c3e48-543">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="c3e48-544">Tables</span><span class="sxs-lookup"><span data-stu-id="c3e48-544">Tables</span></span>  
  
|<span data-ttu-id="c3e48-545">열 이름</span><span class="sxs-lookup"><span data-stu-id="c3e48-545">ColumnName</span></span>|<span data-ttu-id="c3e48-546">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c3e48-546">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c3e48-547">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-547">TABLE_CATALOG</span></span>|<span data-ttu-id="c3e48-548">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-548">String</span></span>|  
|<span data-ttu-id="c3e48-549">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-549">TABLE_SCHEMA</span></span>|<span data-ttu-id="c3e48-550">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-550">String</span></span>|  
|<span data-ttu-id="c3e48-551">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-551">TABLE_NAME</span></span>|<span data-ttu-id="c3e48-552">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-552">String</span></span>|  
|<span data-ttu-id="c3e48-553">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c3e48-553">TABLE_TYPE</span></span>|<span data-ttu-id="c3e48-554">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-554">String</span></span>|  
|<span data-ttu-id="c3e48-555">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="c3e48-555">TABLE_GUID</span></span>|<span data-ttu-id="c3e48-556">Guid</span><span class="sxs-lookup"><span data-stu-id="c3e48-556">Guid</span></span>|  
|<span data-ttu-id="c3e48-557">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c3e48-557">DESCRIPTION</span></span>|<span data-ttu-id="c3e48-558">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-558">String</span></span>|  
|<span data-ttu-id="c3e48-559">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="c3e48-559">TABLE_PROPID</span></span>|<span data-ttu-id="c3e48-560">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-560">Int64</span></span>|  
|<span data-ttu-id="c3e48-561">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="c3e48-561">DATE_CREATED</span></span>|<span data-ttu-id="c3e48-562">DateTime</span><span class="sxs-lookup"><span data-stu-id="c3e48-562">DateTime</span></span>|  
|<span data-ttu-id="c3e48-563">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="c3e48-563">DATE_MODIFIED</span></span>|<span data-ttu-id="c3e48-564">DateTime</span><span class="sxs-lookup"><span data-stu-id="c3e48-564">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="c3e48-565">Columns</span><span class="sxs-lookup"><span data-stu-id="c3e48-565">Columns</span></span>  
  
|<span data-ttu-id="c3e48-566">열 이름</span><span class="sxs-lookup"><span data-stu-id="c3e48-566">ColumnName</span></span>|<span data-ttu-id="c3e48-567">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c3e48-567">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c3e48-568">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-568">TABLE_CATALOG</span></span>|<span data-ttu-id="c3e48-569">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-569">String</span></span>|  
|<span data-ttu-id="c3e48-570">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-570">TABLE_SCHEMA</span></span>|<span data-ttu-id="c3e48-571">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-571">String</span></span>|  
|<span data-ttu-id="c3e48-572">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-572">TABLE_NAME</span></span>|<span data-ttu-id="c3e48-573">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-573">String</span></span>|  
|<span data-ttu-id="c3e48-574">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-574">COLUMN_NAME</span></span>|<span data-ttu-id="c3e48-575">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-575">String</span></span>|  
|<span data-ttu-id="c3e48-576">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="c3e48-576">COLUMN_GUID</span></span>|<span data-ttu-id="c3e48-577">Guid</span><span class="sxs-lookup"><span data-stu-id="c3e48-577">Guid</span></span>|  
|<span data-ttu-id="c3e48-578">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="c3e48-578">COLUMN_PROPID</span></span>|<span data-ttu-id="c3e48-579">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-579">Int64</span></span>|  
|<span data-ttu-id="c3e48-580">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c3e48-580">ORDINAL_POSITION</span></span>|<span data-ttu-id="c3e48-581">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-581">Int64</span></span>|  
|<span data-ttu-id="c3e48-582">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3e48-582">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="c3e48-583">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-583">Boolean</span></span>|  
|<span data-ttu-id="c3e48-584">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c3e48-584">COLUMN_DEFAULT</span></span>|<span data-ttu-id="c3e48-585">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-585">String</span></span>|  
|<span data-ttu-id="c3e48-586">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="c3e48-586">COLUMN_FLAGS</span></span>|<span data-ttu-id="c3e48-587">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-587">Int64</span></span>|  
|<span data-ttu-id="c3e48-588">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="c3e48-588">IS_NULLABLE</span></span>|<span data-ttu-id="c3e48-589">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-589">Boolean</span></span>|  
|<span data-ttu-id="c3e48-590">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="c3e48-590">DATA_TYPE</span></span>|<span data-ttu-id="c3e48-591">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-591">Int32</span></span>|  
|<span data-ttu-id="c3e48-592">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="c3e48-592">TYPE_GUID</span></span>|<span data-ttu-id="c3e48-593">Guid</span><span class="sxs-lookup"><span data-stu-id="c3e48-593">Guid</span></span>|  
|<span data-ttu-id="c3e48-594">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c3e48-594">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="c3e48-595">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-595">Int64</span></span>|  
|<span data-ttu-id="c3e48-596">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="c3e48-596">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="c3e48-597">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-597">Int64</span></span>|  
|<span data-ttu-id="c3e48-598">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="c3e48-598">NUMERIC_PRECISION</span></span>|<span data-ttu-id="c3e48-599">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-599">Int32</span></span>|  
|<span data-ttu-id="c3e48-600">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="c3e48-600">NUMERIC_SCALE</span></span>|<span data-ttu-id="c3e48-601">Int16</span><span class="sxs-lookup"><span data-stu-id="c3e48-601">Int16</span></span>|  
|<span data-ttu-id="c3e48-602">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="c3e48-602">DATETIME_PRECISION</span></span>|<span data-ttu-id="c3e48-603">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-603">Int64</span></span>|  
|<span data-ttu-id="c3e48-604">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-604">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="c3e48-605">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-605">String</span></span>|  
|<span data-ttu-id="c3e48-606">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-606">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="c3e48-607">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-607">String</span></span>|  
|<span data-ttu-id="c3e48-608">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-608">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="c3e48-609">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-609">String</span></span>|  
|<span data-ttu-id="c3e48-610">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-610">COLLATION_CATALOG</span></span>|<span data-ttu-id="c3e48-611">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-611">String</span></span>|  
|<span data-ttu-id="c3e48-612">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-612">COLLATION_SCHEMA</span></span>|<span data-ttu-id="c3e48-613">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-613">String</span></span>|  
|<span data-ttu-id="c3e48-614">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-614">COLLATION_NAME</span></span>|<span data-ttu-id="c3e48-615">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-615">String</span></span>|  
|<span data-ttu-id="c3e48-616">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-616">DOMAIN_CATALOG</span></span>|<span data-ttu-id="c3e48-617">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-617">String</span></span>|  
|<span data-ttu-id="c3e48-618">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-618">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="c3e48-619">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-619">String</span></span>|  
|<span data-ttu-id="c3e48-620">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-620">DOMAIN_NAME</span></span>|<span data-ttu-id="c3e48-621">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-621">String</span></span>|  
|<span data-ttu-id="c3e48-622">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c3e48-622">DESCRIPTION</span></span>|<span data-ttu-id="c3e48-623">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-623">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="c3e48-624">절차</span><span class="sxs-lookup"><span data-stu-id="c3e48-624">Procedures</span></span>  
  
|<span data-ttu-id="c3e48-625">열 이름</span><span class="sxs-lookup"><span data-stu-id="c3e48-625">ColumnName</span></span>|<span data-ttu-id="c3e48-626">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c3e48-626">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c3e48-627">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-627">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="c3e48-628">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-628">String</span></span>|  
|<span data-ttu-id="c3e48-629">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-629">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="c3e48-630">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-630">String</span></span>|  
|<span data-ttu-id="c3e48-631">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-631">PROCEDURE_NAME</span></span>|<span data-ttu-id="c3e48-632">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-632">String</span></span>|  
|<span data-ttu-id="c3e48-633">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="c3e48-633">PROCEDURE_TYPE</span></span>|<span data-ttu-id="c3e48-634">Int16</span><span class="sxs-lookup"><span data-stu-id="c3e48-634">Int16</span></span>|  
|<span data-ttu-id="c3e48-635">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="c3e48-635">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="c3e48-636">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-636">String</span></span>|  
|<span data-ttu-id="c3e48-637">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c3e48-637">DESCRIPTION</span></span>|<span data-ttu-id="c3e48-638">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-638">String</span></span>|  
|<span data-ttu-id="c3e48-639">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="c3e48-639">DATE_CREATED</span></span>|<span data-ttu-id="c3e48-640">DateTime</span><span class="sxs-lookup"><span data-stu-id="c3e48-640">DateTime</span></span>|  
|<span data-ttu-id="c3e48-641">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="c3e48-641">DATE_MODIFIED</span></span>|<span data-ttu-id="c3e48-642">DateTime</span><span class="sxs-lookup"><span data-stu-id="c3e48-642">DateTime</span></span>|  
  
### <a name="views"></a><span data-ttu-id="c3e48-643">뷰</span><span class="sxs-lookup"><span data-stu-id="c3e48-643">Views</span></span>  
  
|<span data-ttu-id="c3e48-644">열 이름</span><span class="sxs-lookup"><span data-stu-id="c3e48-644">ColumnName</span></span>|<span data-ttu-id="c3e48-645">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c3e48-645">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c3e48-646">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-646">TABLE_CATALOG</span></span>|<span data-ttu-id="c3e48-647">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-647">String</span></span>|  
|<span data-ttu-id="c3e48-648">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-648">TABLE_SCHEMA</span></span>|<span data-ttu-id="c3e48-649">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-649">String</span></span>|  
|<span data-ttu-id="c3e48-650">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-650">TABLE_NAME</span></span>|<span data-ttu-id="c3e48-651">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-651">String</span></span>|  
|<span data-ttu-id="c3e48-652">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="c3e48-652">VIEW_DEFINITION</span></span>|<span data-ttu-id="c3e48-653">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-653">String</span></span>|  
|<span data-ttu-id="c3e48-654">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="c3e48-654">CHECK_OPTION</span></span>|<span data-ttu-id="c3e48-655">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-655">Boolean</span></span>|  
|<span data-ttu-id="c3e48-656">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="c3e48-656">IS_UPDATABLE</span></span>|<span data-ttu-id="c3e48-657">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-657">Boolean</span></span>|  
|<span data-ttu-id="c3e48-658">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c3e48-658">DESCRIPTION</span></span>|<span data-ttu-id="c3e48-659">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-659">String</span></span>|  
|<span data-ttu-id="c3e48-660">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="c3e48-660">DATE_CREATED</span></span>|<span data-ttu-id="c3e48-661">DateTime</span><span class="sxs-lookup"><span data-stu-id="c3e48-661">DateTime</span></span>|  
|<span data-ttu-id="c3e48-662">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="c3e48-662">DATE_MODIFIED</span></span>|<span data-ttu-id="c3e48-663">DateTime</span><span class="sxs-lookup"><span data-stu-id="c3e48-663">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="c3e48-664">Indexes</span><span class="sxs-lookup"><span data-stu-id="c3e48-664">Indexes</span></span>  
  
|<span data-ttu-id="c3e48-665">열 이름</span><span class="sxs-lookup"><span data-stu-id="c3e48-665">ColumnName</span></span>|<span data-ttu-id="c3e48-666">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="c3e48-666">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="c3e48-667">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-667">TABLE_CATALOG</span></span>|<span data-ttu-id="c3e48-668">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-668">String</span></span>|  
|<span data-ttu-id="c3e48-669">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-669">TABLE_SCHEMA</span></span>|<span data-ttu-id="c3e48-670">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-670">String</span></span>|  
|<span data-ttu-id="c3e48-671">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-671">TABLE_NAME</span></span>|<span data-ttu-id="c3e48-672">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-672">String</span></span>|  
|<span data-ttu-id="c3e48-673">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="c3e48-673">INDEX_CATALOG</span></span>|<span data-ttu-id="c3e48-674">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-674">String</span></span>|  
|<span data-ttu-id="c3e48-675">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="c3e48-675">INDEX_SCHEMA</span></span>|<span data-ttu-id="c3e48-676">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-676">String</span></span>|  
|<span data-ttu-id="c3e48-677">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-677">INDEX_NAME</span></span>|<span data-ttu-id="c3e48-678">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-678">String</span></span>|  
|<span data-ttu-id="c3e48-679">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="c3e48-679">PRIMARY_KEY</span></span>|<span data-ttu-id="c3e48-680">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-680">Boolean</span></span>|  
|<span data-ttu-id="c3e48-681">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="c3e48-681">UNIQUE</span></span>|<span data-ttu-id="c3e48-682">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-682">Boolean</span></span>|  
|<span data-ttu-id="c3e48-683">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="c3e48-683">CLUSTERED</span></span>|<span data-ttu-id="c3e48-684">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-684">Boolean</span></span>|  
|<span data-ttu-id="c3e48-685">TYPE</span><span class="sxs-lookup"><span data-stu-id="c3e48-685">TYPE</span></span>|<span data-ttu-id="c3e48-686">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-686">Int32</span></span>|  
|<span data-ttu-id="c3e48-687">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="c3e48-687">FILL_FACTOR</span></span>|<span data-ttu-id="c3e48-688">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-688">Int32</span></span>|  
|<span data-ttu-id="c3e48-689">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="c3e48-689">INITIAL_SIZE</span></span>|<span data-ttu-id="c3e48-690">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-690">Int32</span></span>|  
|<span data-ttu-id="c3e48-691">NULLS</span><span class="sxs-lookup"><span data-stu-id="c3e48-691">NULLS</span></span>|<span data-ttu-id="c3e48-692">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-692">Int32</span></span>|  
|<span data-ttu-id="c3e48-693">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="c3e48-693">SORT_BOOKMARKS</span></span>|<span data-ttu-id="c3e48-694">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-694">Boolean</span></span>|  
|<span data-ttu-id="c3e48-695">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="c3e48-695">AUTO_UPDATE</span></span>|<span data-ttu-id="c3e48-696">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e48-696">Boolean</span></span>|  
|<span data-ttu-id="c3e48-697">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="c3e48-697">NULL_COLLATION</span></span>|<span data-ttu-id="c3e48-698">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-698">Int32</span></span>|  
|<span data-ttu-id="c3e48-699">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="c3e48-699">ORDINAL_POSITION</span></span>|<span data-ttu-id="c3e48-700">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-700">Int64</span></span>|  
|<span data-ttu-id="c3e48-701">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="c3e48-701">COLUMN_NAME</span></span>|<span data-ttu-id="c3e48-702">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-702">String</span></span>|  
|<span data-ttu-id="c3e48-703">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="c3e48-703">COLUMN_GUID</span></span>|<span data-ttu-id="c3e48-704">Guid</span><span class="sxs-lookup"><span data-stu-id="c3e48-704">Guid</span></span>|  
|<span data-ttu-id="c3e48-705">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="c3e48-705">COLUMN_PROPID</span></span>|<span data-ttu-id="c3e48-706">Int64</span><span class="sxs-lookup"><span data-stu-id="c3e48-706">Int64</span></span>|  
|<span data-ttu-id="c3e48-707">COLLATION</span><span class="sxs-lookup"><span data-stu-id="c3e48-707">COLLATION</span></span>|<span data-ttu-id="c3e48-708">Int16</span><span class="sxs-lookup"><span data-stu-id="c3e48-708">Int16</span></span>|  
|<span data-ttu-id="c3e48-709">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="c3e48-709">CARDINALITY</span></span>|<span data-ttu-id="c3e48-710">Decimal</span><span class="sxs-lookup"><span data-stu-id="c3e48-710">Decimal</span></span>|  
|<span data-ttu-id="c3e48-711">PAGES</span><span class="sxs-lookup"><span data-stu-id="c3e48-711">PAGES</span></span>|<span data-ttu-id="c3e48-712">Int32</span><span class="sxs-lookup"><span data-stu-id="c3e48-712">Int32</span></span>|  
|<span data-ttu-id="c3e48-713">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="c3e48-713">FILTER_CONDITION</span></span>|<span data-ttu-id="c3e48-714">문자열</span><span class="sxs-lookup"><span data-stu-id="c3e48-714">String</span></span>|  
|<span data-ttu-id="c3e48-715">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="c3e48-715">INTEGRATED</span></span>|<span data-ttu-id="c3e48-716">부울</span><span class="sxs-lookup"><span data-stu-id="c3e48-716">Boolean</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c3e48-717">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c3e48-717">See Also</span></span>  
 [<span data-ttu-id="c3e48-718">ADO.NET 관리되는 공급자 및 데이터 집합 개발자 센터</span><span class="sxs-lookup"><span data-stu-id="c3e48-718">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
