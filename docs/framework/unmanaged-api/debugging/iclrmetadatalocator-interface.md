---
title: ICLRMetadataLocator 인터페이스
ms.date: 03/30/2017
api_name:
- ICLRMetadataLocator
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRMetadataLocator
helpviewer_keywords:
- ICLRMetadataLocator interface [.NET Framework debugging]
ms.assetid: 43c944f4-406a-4df6-981e-0eabb33dd5d0
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5d1d767de88b239c96cb98130b6ff006e3f75b09
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54495034"
---
# <a name="iclrmetadatalocator-interface"></a><span data-ttu-id="cd567-102">ICLRMetadataLocator 인터페이스</span><span class="sxs-lookup"><span data-stu-id="cd567-102">ICLRMetadataLocator Interface</span></span>
<span data-ttu-id="cd567-103">대상 프로세스에서 어셈블리의 메타 데이터를 찾을 데이터 액세스 서비스 계층을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd567-103">Used by the data access services layer to locate metadata of assemblies in a target process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="cd567-104">메서드</span><span class="sxs-lookup"><span data-stu-id="cd567-104">Methods</span></span>  
  
|<span data-ttu-id="cd567-105">메서드</span><span class="sxs-lookup"><span data-stu-id="cd567-105">Method</span></span>|<span data-ttu-id="cd567-106">설명</span><span class="sxs-lookup"><span data-stu-id="cd567-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="cd567-107">GetMetadata 메서드</span><span class="sxs-lookup"><span data-stu-id="cd567-107">GetMetadata Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrmetadatalocator-getmetadata-method.md)|<span data-ttu-id="cd567-108">대상 프로세스에서 이미지의 메타 데이터를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="cd567-108">Retrieves the metadata of an image from the target process.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cd567-109">설명</span><span class="sxs-lookup"><span data-stu-id="cd567-109">Remarks</span></span>  
 <span data-ttu-id="cd567-110">API 클라이언트(즉, 디버거)에서는 이 인터페이스를 특정 대상 프로세스에 적절하게 구현해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd567-110">The API client (that is, the debugger) must implement this interface as appropriate for the particular target process.</span></span> <span data-ttu-id="cd567-111">예를 들어 활성 프로세스에 대 한 구현은 메모리 덤프와 다른 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cd567-111">For example, the implementation for a live process would be different from that of a memory dump.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cd567-112">요구 사항</span><span class="sxs-lookup"><span data-stu-id="cd567-112">Requirements</span></span>  
 <span data-ttu-id="cd567-113">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="cd567-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cd567-114">**헤더:** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="cd567-114">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="cd567-115">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cd567-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cd567-116">**.**</span><span class="sxs-lookup"><span data-stu-id="cd567-116">**.**</span></span> <span data-ttu-id="cd567-117">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cd567-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cd567-118">참고자료</span><span class="sxs-lookup"><span data-stu-id="cd567-118">See also</span></span>
- [<span data-ttu-id="cd567-119">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="cd567-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
