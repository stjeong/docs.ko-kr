---
title: AXL_AUTHENTICODE_SIGNER_INFO 구조
ms.date: 03/30/2017
ms.assetid: 81c0f8b4-ce35-4716-8651-b642d40648a2
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4b9f54c7c57d122ac1214b9f31cc4e1d1cddd71c
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43392181"
---
# <a name="axlauthenticodesignerinfo-structure"></a><span data-ttu-id="d6fed-102">AXL_AUTHENTICODE_SIGNER_INFO 구조</span><span class="sxs-lookup"><span data-stu-id="d6fed-102">AXL_AUTHENTICODE_SIGNER_INFO Structure</span></span>
<span data-ttu-id="d6fed-103">Authenticode 서명자 정보를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="d6fed-103">Defines the Authenticode signer information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d6fed-104">구문</span><span class="sxs-lookup"><span data-stu-id="d6fed-104">Syntax</span></span>  
  
```  
typedef struct _AXL_AUTHENTICODE_SIGNER_INFO {  
    DWORD cbSize;  
    HRESULT dwError;  
    ALG_ID algHash;  
    LPCWSTR pwszHash  
    LPCWSTR pwszDescription;  
    LPCWSTR pwszDescriptionUrl;  
    PCCERT_CHAIN_CONTEXT pChainContext  
} AXL_AUTHENTICODE_SIGNER_INFO, * PAXL_AUTHENTICODE_SIGNER_INFO;  
```  
  
## <a name="members"></a><span data-ttu-id="d6fed-105">멤버</span><span class="sxs-lookup"><span data-stu-id="d6fed-105">Members</span></span>  
  
|<span data-ttu-id="d6fed-106">멤버</span><span class="sxs-lookup"><span data-stu-id="d6fed-106">Member</span></span>|<span data-ttu-id="d6fed-107">설명</span><span class="sxs-lookup"><span data-stu-id="d6fed-107">Description</span></span>|  
|------------|-----------------|  
|`cbSize`|<span data-ttu-id="d6fed-108">이 구조체의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="d6fed-108">The size of this structure.</span></span>|  
|`dwError`|<span data-ttu-id="d6fed-109">오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="d6fed-109">The error code.</span></span>|  
|`algHash`|<span data-ttu-id="d6fed-110">해시 알고리즘입니다.</span><span class="sxs-lookup"><span data-stu-id="d6fed-110">The hash algorithm.</span></span>|  
|`pwszHash`|<span data-ttu-id="d6fed-111">해시입니다.</span><span class="sxs-lookup"><span data-stu-id="d6fed-111">The hash.</span></span>|  
|`pwszDescription`|<span data-ttu-id="d6fed-112">설명입니다.</span><span class="sxs-lookup"><span data-stu-id="d6fed-112">The description.</span></span>|  
|`pwszDescriptionUrl`|<span data-ttu-id="d6fed-113">설명의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="d6fed-113">The URL of the description.</span></span>|  
|`pChainContext`|<span data-ttu-id="d6fed-114">서명자의 체인 컨텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="d6fed-114">The chain context of the signer.</span></span> <span data-ttu-id="d6fed-115">참조 된 [CERT_CONTEXT](/windows/desktop/api/wincrypt/ns-wincrypt-_cert_context) 구조입니다.</span><span class="sxs-lookup"><span data-stu-id="d6fed-115">See the [CERT_CONTEXT](/windows/desktop/api/wincrypt/ns-wincrypt-_cert_context) structure.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d6fed-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d6fed-116">See Also</span></span>  
 [<span data-ttu-id="d6fed-117">Authenticode</span><span class="sxs-lookup"><span data-stu-id="d6fed-117">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
