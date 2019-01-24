---
title: CreateICeeFileGen 함수
ms.date: 03/30/2017
api_name:
- CreateICeeFileGen
api_location:
- mscoree.dll
- mscorpehost.dll
- mscorpe.dll
api_type:
- COM
f1_keywords:
- CreateICeeFileGen
helpviewer_keywords:
- CreateICeeFileGen function [.NET Framework hosting]
ms.assetid: e36e1fd8-8456-4359-bdc3-3ec1765f041f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0e367ab3c966cea2d875b1de5b4244db5c4b813e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54702225"
---
# <a name="createiceefilegen-function"></a><span data-ttu-id="94b7c-102">CreateICeeFileGen 함수</span><span class="sxs-lookup"><span data-stu-id="94b7c-102">CreateICeeFileGen Function</span></span>
<span data-ttu-id="94b7c-103">만듭니다는 [ICeeFileGen](../../../../docs/framework/unmanaged-api/hosting/iceefilegen-class.md) 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-103">Creates an [ICeeFileGen](../../../../docs/framework/unmanaged-api/hosting/iceefilegen-class.md) object.</span></span>  
  
 <span data-ttu-id="94b7c-104">이 함수에서 사용 중단에 [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)]합니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="94b7c-105">구문</span><span class="sxs-lookup"><span data-stu-id="94b7c-105">Syntax</span></span>  
  
```  
HRESULT CreateICeeFileGen (  
    [out] ICeeFileGen  **ceeFileGen  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="94b7c-106">매개 변수</span><span class="sxs-lookup"><span data-stu-id="94b7c-106">Parameters</span></span>  
 `ceeFileGen`  
 <span data-ttu-id="94b7c-107">[out] 새 주소에 대 한 포인터 `ICeeFileGen` 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-107">[out] A pointer to the address of a new `ICeeFileGen` object.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="94b7c-108">반환 값</span><span class="sxs-lookup"><span data-stu-id="94b7c-108">Return Value</span></span>  
 <span data-ttu-id="94b7c-109">이 메서드는 표준 COM 오류 코드를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-109">This method returns standard COM error codes.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="94b7c-110">설명</span><span class="sxs-lookup"><span data-stu-id="94b7c-110">Remarks</span></span>  
 <span data-ttu-id="94b7c-111">`ICeeFileGen` 개체가 공용 언어 런타임 (CLR) pe (이식 가능) 파일을 만드는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-111">The `ICeeFileGen` object is used to create common language runtime (CLR) portable executable (PE) files.</span></span>  
  
 <span data-ttu-id="94b7c-112">호출 된 [DestroyICeeFileGen](../../../../docs/framework/unmanaged-api/hosting/destroyiceefilegen-function.md) 제거할 함수는 `ICeeFileGen` 완료 되 면 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-112">Call the [DestroyICeeFileGen](../../../../docs/framework/unmanaged-api/hosting/destroyiceefilegen-function.md) function to destroy the `ICeeFileGen` object when finished.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="94b7c-113">요구 사항</span><span class="sxs-lookup"><span data-stu-id="94b7c-113">Requirements</span></span>  
 <span data-ttu-id="94b7c-114">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="94b7c-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="94b7c-115">**헤더:** ICeeFileGen.h</span><span class="sxs-lookup"><span data-stu-id="94b7c-115">**Header:** ICeeFileGen.h</span></span>  
  
 <span data-ttu-id="94b7c-116">**라이브러리:** MSCorPE.dll</span><span class="sxs-lookup"><span data-stu-id="94b7c-116">**Library:** MSCorPE.dll</span></span>  
  
 <span data-ttu-id="94b7c-117">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="94b7c-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="94b7c-118">참고자료</span><span class="sxs-lookup"><span data-stu-id="94b7c-118">See also</span></span>
- [<span data-ttu-id="94b7c-119">사용되지 않는 CLR 호스팅 함수</span><span class="sxs-lookup"><span data-stu-id="94b7c-119">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
