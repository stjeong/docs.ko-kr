---
title: AXL_AUTHENTICODE_TIMESTAMPER_INFO 구조
ms.date: 03/30/2017
ms.assetid: 89e41a81-0f41-45ad-8f20-a120e4ff24fb
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d7f4fff4f2c2b3dd04625f4cf50b8b19a0ef6f39
ms.sourcegitcommit: fe02afbc39e78afd78cc6050e4a9c12a75f579f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43254661"
---
# <a name="axlauthenticodetimestamperinfo-structure"></a><span data-ttu-id="e489d-102">AXL_AUTHENTICODE_TIMESTAMPER_INFO 구조</span><span class="sxs-lookup"><span data-stu-id="e489d-102">AXL_AUTHENTICODE_TIMESTAMPER_INFO Structure</span></span>
<span data-ttu-id="e489d-103">Authenticode 타임스탬퍼 정보를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="e489d-103">Defines the Authenticode time stamper information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e489d-104">구문</span><span class="sxs-lookup"><span data-stu-id="e489d-104">Syntax</span></span>  
  
```  
typedef struct _AXL_AUTHENTICODE_SIGNER_INFO {  
    DWORD cbSize;  
    HRESULT dwError;  
    ALG_ID algHash;  
    FILETIME ftTimestamp  
    PCCERT_CHAIN_CONTEXT pChainContext;  
} AXL_AUTHENTICODE_TIMESTAMPER_INFO, * PAXL_AUTHENTICODE_TIMESTAMPER_INFO;  
```  
  
## <a name="members"></a><span data-ttu-id="e489d-105">멤버</span><span class="sxs-lookup"><span data-stu-id="e489d-105">Members</span></span>  
  
|<span data-ttu-id="e489d-106">멤버</span><span class="sxs-lookup"><span data-stu-id="e489d-106">Member</span></span>|<span data-ttu-id="e489d-107">설명</span><span class="sxs-lookup"><span data-stu-id="e489d-107">Description</span></span>|  
|------------|-----------------|  
|`cbSize`|<span data-ttu-id="e489d-108">이 구조체의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="e489d-108">The size of this structure.</span></span>|  
|`dwError`|<span data-ttu-id="e489d-109">오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="e489d-109">The error code.</span></span>|  
|`algHash`|<span data-ttu-id="e489d-110">해시 알고리즘입니다.</span><span class="sxs-lookup"><span data-stu-id="e489d-110">The hash algorithm.</span></span>|  
|`ftTimestamp`|<span data-ttu-id="e489d-111">타임스탬프의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="e489d-111">The time of the time stamp.</span></span>|  
|`pChainContext`|<span data-ttu-id="e489d-112">타임스탬퍼의 체인 컨텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="e489d-112">The time stamper’s chain context.</span></span>  <span data-ttu-id="e489d-113">참조 된 [CERT_CONTEXT](/windows/desktop/api/wincrypt/ns-wincrypt-_cert_context) 구조입니다.</span><span class="sxs-lookup"><span data-stu-id="e489d-113">See the [CERT_CONTEXT](/windows/desktop/api/wincrypt/ns-wincrypt-_cert_context) structure.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e489d-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e489d-114">See Also</span></span>  
 [<span data-ttu-id="e489d-115">Authenticode</span><span class="sxs-lookup"><span data-stu-id="e489d-115">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
