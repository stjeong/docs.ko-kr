---
title: ICLRStrongName::StrongNameTokenFromAssembly 메서드
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameTokenFromAssembly
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameTokenFromAssembly
helpviewer_keywords:
- ICLRStrongName::StrongNameTokenFromAssembly method [.NET Framework hosting]
- StrongNameTokenFromAssembly method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: fc725afb-b66b-4015-aa44-1c0d1304197f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3dd083193fa8fed2abc8a1a498325f7edd89bc96
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43658002"
---
# <a name="iclrstrongnamestrongnametokenfromassembly-method"></a><span data-ttu-id="b75f2-102">ICLRStrongName::StrongNameTokenFromAssembly 메서드</span><span class="sxs-lookup"><span data-stu-id="b75f2-102">ICLRStrongName::StrongNameTokenFromAssembly Method</span></span>
<span data-ttu-id="b75f2-103">지정된 어셈블리 파일에서 강력한 이름 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b75f2-103">Creates a strong name token from the specified assembly file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b75f2-104">구문</span><span class="sxs-lookup"><span data-stu-id="b75f2-104">Syntax</span></span>  
  
```  
HRESULT StrongNameTokenFromAssembly (  
    [in]  LPCWSTR   wszFilePath,  
    [out] BYTE      **ppbStrongNameToken,  
    [out] ULONG     *pcbStrongNameToken  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b75f2-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b75f2-105">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="b75f2-106">[in] 어셈블리의 pe (이식 가능) 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b75f2-106">[in] The path to the portable executable (PE) file for the assembly.</span></span>  
  
 `ppbStrongNameToken`  
 <span data-ttu-id="b75f2-107">[out] 반환 된 강력한 이름 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="b75f2-107">[out] The returned strong name token.</span></span>  
  
 `pcbStrongNameToken`  
 <span data-ttu-id="b75f2-108">[out] 강력한 이름 토큰의 바이트 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="b75f2-108">[out] The size, in bytes, of the strong name token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b75f2-109">반환 값</span><span class="sxs-lookup"><span data-stu-id="b75f2-109">Return Value</span></span>  
 <span data-ttu-id="b75f2-110">`S_OK` 메서드가 성공적으로 완료 하는 경우 그렇지 않으면 실패를 나타내는 HRESULT 값을 (참조 [일반적인 HRESULT 값](https://go.microsoft.com/fwlink/?LinkId=213878) 목록에 대 한).</span><span class="sxs-lookup"><span data-stu-id="b75f2-110">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b75f2-111">설명</span><span class="sxs-lookup"><span data-stu-id="b75f2-111">Remarks</span></span>  
 <span data-ttu-id="b75f2-112">강력한 이름 토큰은 공개 키의 축약 형태입니다.</span><span class="sxs-lookup"><span data-stu-id="b75f2-112">A strong name token is the shortened form of a public key.</span></span> <span data-ttu-id="b75f2-113">토큰은 어셈블리 서명에 사용 된 공개 키에서 생성 되는 64 비트 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="b75f2-113">The token is a 64-bit hash that is created from the public key used to sign the assembly.</span></span> <span data-ttu-id="b75f2-114">토큰에는 어셈블리에 대 한 강력한 이름의 일부인 되며 어셈블리 메타 데이터에서 읽을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b75f2-114">The token is a part of the strong name for the assembly, and can be read from the assembly metadata.</span></span>  
  
 <span data-ttu-id="b75f2-115">토큰을 만든 후 호출 해야 합니다 [iclrstrongname:: Strongnamefreebuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) 할당 된 메모리를 해제 하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="b75f2-115">After the token is created, you should call the [ICLRStrongName::StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) method to release the allocated memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b75f2-116">요구 사항</span><span class="sxs-lookup"><span data-stu-id="b75f2-116">Requirements</span></span>  
 <span data-ttu-id="b75f2-117">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b75f2-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b75f2-118">**헤더:** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="b75f2-118">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="b75f2-119">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="b75f2-119">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b75f2-120">**.NET Framework 버전:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b75f2-120">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b75f2-121">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b75f2-121">See Also</span></span>  
 [<span data-ttu-id="b75f2-122">StrongNameTokenFromAssemblyEx 메서드</span><span class="sxs-lookup"><span data-stu-id="b75f2-122">StrongNameTokenFromAssemblyEx Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfromassemblyex-method.md)  
 [<span data-ttu-id="b75f2-123">ICLRStrongName 인터페이스</span><span class="sxs-lookup"><span data-stu-id="b75f2-123">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
