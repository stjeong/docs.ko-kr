---
title: _AxlGetIssuerPublicKeyHash 함수
ms.date: 03/30/2017
api_name:
- _AxlGetIssuerPublicKeyHash
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: fb626b41-b888-4625-84c3-2c02b5e3866f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 408b71bf38427d12418e05f8b509fe841bc95ef1
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43395236"
---
# <a name="axlgetissuerpublickeyhash-function"></a><span data-ttu-id="cb068-102">_AxlGetIssuerPublicKeyHash 함수</span><span class="sxs-lookup"><span data-stu-id="cb068-102">_AxlGetIssuerPublicKeyHash Function</span></span>
<span data-ttu-id="cb068-103">지정한 인증서에 서명하는 데 사용되는 개인 키에 연결된 공개 키의 SHA-1 해시를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="cb068-103">Retrieves the SHA-1 hash of the public key associated with the private key that is used to sign the specified certificate.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cb068-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb068-104">Syntax</span></span>  
  
```  
HRESULT _AxlGetIssuerPublicKeyHash (  
    [in]  IN PCRYPT_DATA_BLOB   pChainContext,  
    [out] LPWSTR                *ppwszPublicKeyHash  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cb068-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cb068-105">Parameters</span></span>  
 `pChainContext`  
 <span data-ttu-id="cb068-106">[in] CSP 공개 키 Blob입니다.</span><span class="sxs-lookup"><span data-stu-id="cb068-106">[in] The CSP public key blob.</span></span> <span data-ttu-id="cb068-107">참조 된 [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) 구조입니다.</span><span class="sxs-lookup"><span data-stu-id="cb068-107">See the [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) structure.</span></span>  
  
 `ppwszPublicKeyHash`  
 <span data-ttu-id="cb068-108">[out] 16진수로 인코딩된 공개 키 토큰을 받는 WCHAR \*에 대한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="cb068-108">[out] A pointer to WCHAR \* to receive the hex-encoded public key token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cb068-109">반환 값</span><span class="sxs-lookup"><span data-stu-id="cb068-109">Return Value</span></span>  
 <span data-ttu-id="cb068-110">함수가 정상적으로 실행되는 경우 `S_OK`이고 그러지 않으면 `S_FALSE`입니다.</span><span class="sxs-lookup"><span data-stu-id="cb068-110">`S_OK` if the function succeeds; otherwise `S_FALSE`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cb068-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="cb068-111">See Also</span></span>  
 [<span data-ttu-id="cb068-112">Authenticode</span><span class="sxs-lookup"><span data-stu-id="cb068-112">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
