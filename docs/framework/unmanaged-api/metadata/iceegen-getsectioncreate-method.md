---
title: ICeeGen::GetSectionCreate 메서드
ms.date: 03/30/2017
api_name:
- ICeeGen.GetSectionCreate
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetSectionCreate
helpviewer_keywords:
- ICeeGen::GetSectionCreate method [.NET Framework metadata]
- GetSectionCreate method [.NET Framework metadata]
ms.assetid: 154b2460-59ce-4874-a9f2-1b3353486ac5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 93e96e7804a3b5ecc64e9e50ce700435be83b77a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54643366"
---
# <a name="iceegengetsectioncreate-method"></a><span data-ttu-id="cfac2-102">ICeeGen::GetSectionCreate 메서드</span><span class="sxs-lookup"><span data-stu-id="cfac2-102">ICeeGen::GetSectionCreate Method</span></span>
<span data-ttu-id="cfac2-103">생성 하 고 지정한 이름 및 플래그 값을 사용 하 여 코드 섹션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cfac2-103">Generates and gets a code section using the specified name and flag values.</span></span>  
  
 <span data-ttu-id="cfac2-104">이 메서드는 사용 되지 않습니다 및 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cfac2-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cfac2-105">구문</span><span class="sxs-lookup"><span data-stu-id="cfac2-105">Syntax</span></span>  
  
```  
HRESULT GetSectionCreate (  
    [in]  const char     *name,  
    [in]  DWORD          flags,  
    [out] HCEESECTION    *section  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cfac2-106">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cfac2-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="cfac2-107">[in] 만들 섹션의 이름을 지정 하는 문자열에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="cfac2-107">[in] A pointer to a string that specifies the name of the section to be created.</span></span>  
  
 `flags`  
 <span data-ttu-id="cfac2-108">[in] 옵션을 지정 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="cfac2-108">[in] Flags that specify options.</span></span>  
  
 `section`  
 <span data-ttu-id="cfac2-109">[out] 새로 생성된 된 코드 섹션에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="cfac2-109">[out] A pointer to the newly created code section.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cfac2-110">설명</span><span class="sxs-lookup"><span data-stu-id="cfac2-110">Remarks</span></span>  
 <span data-ttu-id="cfac2-111">호출 `GetSectionCreate` 다른 메서드에서 처리 되지 않는 특수 섹션 요구 사항이 있는 경우에 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfac2-111">Call `GetSectionCreate` only if you have special section requirements that are not handled by other methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cfac2-112">요구 사항</span><span class="sxs-lookup"><span data-stu-id="cfac2-112">Requirements</span></span>  
 <span data-ttu-id="cfac2-113">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="cfac2-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cfac2-114">**헤더:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="cfac2-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="cfac2-115">**라이브러리:** MsCorEE.dll에서 리소스로 사용</span><span class="sxs-lookup"><span data-stu-id="cfac2-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="cfac2-116">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cfac2-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cfac2-117">참고자료</span><span class="sxs-lookup"><span data-stu-id="cfac2-117">See also</span></span>
- [<span data-ttu-id="cfac2-118">ICeeGen 인터페이스</span><span class="sxs-lookup"><span data-stu-id="cfac2-118">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
