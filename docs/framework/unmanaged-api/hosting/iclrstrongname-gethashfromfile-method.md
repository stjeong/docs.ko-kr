---
title: ICLRStrongName::GetHashFromFile 메서드
ms.date: 03/30/2017
api_name:
- ICLRStrongName.GetHashFromFile
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::GetHashFromFile
helpviewer_keywords:
- ICLRStrongName::GetHashFromFile method [.NET Framework hosting]
- GetHashFromFile method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 9e50480a-8ada-4044-b2a5-97bb14ed3525
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 33aab5ee23a1f0d30d1f9f3079856ca30d46d2ec
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44192322"
---
# <a name="iclrstrongnamegethashfromfile-method"></a><span data-ttu-id="cf443-102">ICLRStrongName::GetHashFromFile 메서드</span><span class="sxs-lookup"><span data-stu-id="cf443-102">ICLRStrongName::GetHashFromFile Method</span></span>
<span data-ttu-id="cf443-103">지정된 파일 내용에 대해 해시를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-103">Generates a hash over the contents of the specified file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cf443-104">구문</span><span class="sxs-lookup"><span data-stu-id="cf443-104">Syntax</span></span>  
  
```  
HRESULT GetHashFromFile (  
    [in]  LPCSTR   szFilePath,  
    [in, out] unsigned int   *piHashAlg,   
    [out] BYTE     *pbHash,      
    [in]  DWORD    cchHash,      
    [out] DWORD    *pchHash  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cf443-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cf443-105">Parameters</span></span>  
 `szFilePath`  
 <span data-ttu-id="cf443-106">[in] 해시 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-106">[in] The name of the file to hash.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="cf443-107">[out에서] 해시를 생성할 때 사용할 알고리즘입니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-107">[in, out] The algorithm to use when generating the hash.</span></span> <span data-ttu-id="cf443-108">유효한 알고리즘은 Win32 CryptoAPI에 의해 정의 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-108">Valid algorithms are those defined by the Win32 CryptoAPI.</span></span> <span data-ttu-id="cf443-109">경우 `piHashAlg` CALG_SHA-1은 사용 하는 기본 알고리즘 0으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-109">If `piHashAlg` is set to 0, the default algorithm CALG_SHA-1 is used.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="cf443-110">[out] 생성된 된 해시를 포함 하는 바이트 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-110">[out] A byte array containing the generated hash.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="cf443-111">[in] 버퍼의 최대 크기는 `pbHash` 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-111">[in] The maximum size of the buffer that `pbHash` points to.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="cf443-112">[out] 반환 된 바이트의 크기, `pbHash`합니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-112">[out] The size, in bytes, of the returned `pbHash`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cf443-113">반환 값</span><span class="sxs-lookup"><span data-stu-id="cf443-113">Return Value</span></span>  
 <span data-ttu-id="cf443-114">`S_OK` 메서드가 성공적으로 완료 하는 경우 그렇지 않으면 실패를 나타내는 HRESULT 값을 (참조 [일반적인 HRESULT 값](https://go.microsoft.com/fwlink/?LinkId=213878) 목록에 대 한).</span><span class="sxs-lookup"><span data-stu-id="cf443-114">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cf443-115">설명</span><span class="sxs-lookup"><span data-stu-id="cf443-115">Remarks</span></span>  
 <span data-ttu-id="cf443-116">이 메서드는 동일 합니다 [iclrstrongname:: Gethashfromfilew](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfilew-method.md) 메서드를 제외 하 고 파일 이름을 지정은 유니코드가 아닌 ANSI 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf443-116">This method is the same as the [ICLRStrongName::GetHashFromFileW](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfilew-method.md) method, except that the file name specification is ANSI instead of Unicode.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cf443-117">요구 사항</span><span class="sxs-lookup"><span data-stu-id="cf443-117">Requirements</span></span>  
 <span data-ttu-id="cf443-118">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cf443-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cf443-119">**헤더:** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="cf443-119">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="cf443-120">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="cf443-120">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cf443-121">**.NET Framework 버전:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cf443-121">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cf443-122">참고 항목</span><span class="sxs-lookup"><span data-stu-id="cf443-122">See Also</span></span>  
 [<span data-ttu-id="cf443-123">GetHashFromFileW 메서드</span><span class="sxs-lookup"><span data-stu-id="cf443-123">GetHashFromFileW Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfilew-method.md)  
 [<span data-ttu-id="cf443-124">ICLRStrongName 인터페이스</span><span class="sxs-lookup"><span data-stu-id="cf443-124">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
