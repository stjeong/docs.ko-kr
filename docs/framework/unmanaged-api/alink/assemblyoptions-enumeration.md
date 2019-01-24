---
title: AssemblyOptions 열거형
ms.date: 03/30/2017
api_name:
- AssemblyOptions
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- AssemblyOptions
helpviewer_keywords:
- Alink API, AssemblyOptions enumeration
- AssemblyOptions enumeration
ms.assetid: 84f83921-64cb-49e3-ac8b-22a0b77b18a8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 939e815f4d3adc5f6e1c8b8fc85c9f4b89372501
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54571485"
---
# <a name="assemblyoptions-enumeration"></a><span data-ttu-id="9de86-102">AssemblyOptions 열거형</span><span class="sxs-lookup"><span data-stu-id="9de86-102">AssemblyOptions Enumeration</span></span>
<span data-ttu-id="9de86-103">어셈블리 옵션을 열거합니다.</span><span class="sxs-lookup"><span data-stu-id="9de86-103">Enumerates the assembly options.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9de86-104">구문</span><span class="sxs-lookup"><span data-stu-id="9de86-104">Syntax</span></span>  
  
```  
typedef enum _AssemblyOptions {  
    optAssemTitle = 0,  
    optAssemDescription,  
    optAssemConfig,  
    optAssemOS,  
    optAssemProcessor,  
    optAssemLocale,  
    optAssemVersion,  
    optAssemCompany,  
    optAssemProduct,  
    optAssemProductVersion,  
    optAssemCopyright,  
    optAssemTrademark,  
    optAssemKeyFile,  
    optAssemKeyName,  
    optAssemAlgID,  
    optAssemFlags,  
    optAssemHalfSign,  
    optAssemFileVersion,  
    optAssemSatelliteVer,  
    optLastAssemOption  
}   AssemblyOptions;  
```  
  
## <a name="fields"></a><span data-ttu-id="9de86-105">필드</span><span class="sxs-lookup"><span data-stu-id="9de86-105">Fields</span></span>  
  
|<span data-ttu-id="9de86-106">필드</span><span class="sxs-lookup"><span data-stu-id="9de86-106">Field</span></span>|<span data-ttu-id="9de86-107">설명</span><span class="sxs-lookup"><span data-stu-id="9de86-107">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="9de86-108">optAssemTitle</span><span class="sxs-lookup"><span data-stu-id="9de86-108">optAssemTitle</span></span>|<span data-ttu-id="9de86-109">문자열-어셈블리 제목을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9de86-109">String - Represents the assembly title.</span></span>|  
|<span data-ttu-id="9de86-110">optAssemDescription</span><span class="sxs-lookup"><span data-stu-id="9de86-110">optAssemDescription</span></span>|<span data-ttu-id="9de86-111">문자열-어셈블리 파일에 대 한 설명을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de86-111">String - Contains the assembly description.</span></span>|  
|<span data-ttu-id="9de86-112">optAssemConfig</span><span class="sxs-lookup"><span data-stu-id="9de86-112">optAssemConfig</span></span>|<span data-ttu-id="9de86-113">문자열-어셈블리 구성을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de86-113">String - Contains the assembly configuration.</span></span>|  
|<span data-ttu-id="9de86-114">optAssemOS</span><span class="sxs-lookup"><span data-stu-id="9de86-114">optAssemOS</span></span>|<span data-ttu-id="9de86-115">로 인코드된 문자열: "dwOSPlatformId.dwOSMajorVersion.dwOSMinorVersion"입니다.</span><span class="sxs-lookup"><span data-stu-id="9de86-115">String - Encoded as: "dwOSPlatformId.dwOSMajorVersion.dwOSMinorVersion".</span></span>|  
|<span data-ttu-id="9de86-116">optAssemProcessor</span><span class="sxs-lookup"><span data-stu-id="9de86-116">optAssemProcessor</span></span>|<span data-ttu-id="9de86-117">ULONG</span><span class="sxs-lookup"><span data-stu-id="9de86-117">ULONG</span></span>|  
|<span data-ttu-id="9de86-118">optAssemLocale</span><span class="sxs-lookup"><span data-stu-id="9de86-118">optAssemLocale</span></span>|<span data-ttu-id="9de86-119">문자열-어셈블리 로캘을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de86-119">String - Contains the assembly locale.</span></span>|  
|<span data-ttu-id="9de86-120">optAssemVersion</span><span class="sxs-lookup"><span data-stu-id="9de86-120">optAssemVersion</span></span>|<span data-ttu-id="9de86-121">문자열-로 인코딩됩니다. "Major.Minor.Build.Revision".</span><span class="sxs-lookup"><span data-stu-id="9de86-121">String - Encoded as: "Major.Minor.Build.Revision".</span></span>|  
|<span data-ttu-id="9de86-122">optAssemCompany</span><span class="sxs-lookup"><span data-stu-id="9de86-122">optAssemCompany</span></span>|<span data-ttu-id="9de86-123">문자열-회사 이름을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de86-123">String - Contains the company.</span></span>|  
|<span data-ttu-id="9de86-124">optAssemProduct</span><span class="sxs-lookup"><span data-stu-id="9de86-124">optAssemProduct</span></span>|<span data-ttu-id="9de86-125">문자열-제품 이름을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de86-125">String - Contains the product name.</span></span>|  
|<span data-ttu-id="9de86-126">optAssemProductVersion</span><span class="sxs-lookup"><span data-stu-id="9de86-126">optAssemProductVersion</span></span>|<span data-ttu-id="9de86-127">문자열 (InformationalVersion이 라고도 함)입니다.</span><span class="sxs-lookup"><span data-stu-id="9de86-127">String (also known as InformationalVersion).</span></span>|  
|<span data-ttu-id="9de86-128">optAssemCopyright</span><span class="sxs-lookup"><span data-stu-id="9de86-128">optAssemCopyright</span></span>|<span data-ttu-id="9de86-129">문자열-저작권 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de86-129">String - Contains the copyright information.</span></span>|  
|<span data-ttu-id="9de86-130">optAssemTrademark</span><span class="sxs-lookup"><span data-stu-id="9de86-130">optAssemTrademark</span></span>|<span data-ttu-id="9de86-131">문자열-상표 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de86-131">String - Contains the trademark information.</span></span>|  
|<span data-ttu-id="9de86-132">optAssemKeyFile</span><span class="sxs-lookup"><span data-stu-id="9de86-132">optAssemKeyFile</span></span>|<span data-ttu-id="9de86-133">String (파일 이름)입니다.</span><span class="sxs-lookup"><span data-stu-id="9de86-133">String (file name).</span></span>|  
|<span data-ttu-id="9de86-134">optAssemKeyName</span><span class="sxs-lookup"><span data-stu-id="9de86-134">optAssemKeyName</span></span>|<span data-ttu-id="9de86-135">문자열 (키 이름)입니다.</span><span class="sxs-lookup"><span data-stu-id="9de86-135">String (The key name).</span></span>|  
|<span data-ttu-id="9de86-136">optAssemAlgID</span><span class="sxs-lookup"><span data-stu-id="9de86-136">optAssemAlgID</span></span>|<span data-ttu-id="9de86-137">ULONG</span><span class="sxs-lookup"><span data-stu-id="9de86-137">ULONG</span></span>|  
|<span data-ttu-id="9de86-138">optAssemFlags</span><span class="sxs-lookup"><span data-stu-id="9de86-138">optAssemFlags</span></span>|<span data-ttu-id="9de86-139">ULONG</span><span class="sxs-lookup"><span data-stu-id="9de86-139">ULONG</span></span>|  
|<span data-ttu-id="9de86-140">optAssemHalfSign</span><span class="sxs-lookup"><span data-stu-id="9de86-140">optAssemHalfSign</span></span>|<span data-ttu-id="9de86-141">Bool (DelaySign 라고도 함)입니다.</span><span class="sxs-lookup"><span data-stu-id="9de86-141">Bool (Also known as DelaySign).</span></span>|  
|<span data-ttu-id="9de86-142">optAssemFileVersion</span><span class="sxs-lookup"><span data-stu-id="9de86-142">optAssemFileVersion</span></span>|<span data-ttu-id="9de86-143">String - Encoded as "Major.Minor.Build.Revision"--same as ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="9de86-143">String - Encoded as "Major.Minor.Build.Revision"--same as ProductVersion.</span></span>|  
|<span data-ttu-id="9de86-144">optAssemSatelliteVer</span><span class="sxs-lookup"><span data-stu-id="9de86-144">optAssemSatelliteVer</span></span>|<span data-ttu-id="9de86-145">문자열-"Major.Minor.Build.Revision"로 인코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="9de86-145">String - Encoded as "Major.Minor.Build.Revision".</span></span>|  
|<span data-ttu-id="9de86-146">optLastAssemOption</span><span class="sxs-lookup"><span data-stu-id="9de86-146">optLastAssemOption</span></span>|<span data-ttu-id="9de86-147">요소 수가 카운터입니다.</span><span class="sxs-lookup"><span data-stu-id="9de86-147">A counter of the number of elements.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9de86-148">요구 사항</span><span class="sxs-lookup"><span data-stu-id="9de86-148">Requirements</span></span>  
 <span data-ttu-id="9de86-149">**헤더:** alink.h</span><span class="sxs-lookup"><span data-stu-id="9de86-149">**Header:** alink.h</span></span>  
  
 <span data-ttu-id="9de86-150">**라이브러리**: alink.dll</span><span class="sxs-lookup"><span data-stu-id="9de86-150">**Library**: alink.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9de86-151">참고자료</span><span class="sxs-lookup"><span data-stu-id="9de86-151">See also</span></span>
- [<span data-ttu-id="9de86-152">Al.exe(어셈블리 링커)</span><span class="sxs-lookup"><span data-stu-id="9de86-152">Al.exe (Assembly Linker)</span></span>](../../../../docs/framework/tools/al-exe-assembly-linker.md)
