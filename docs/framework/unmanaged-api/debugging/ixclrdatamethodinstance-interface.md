---
title: IXCLRDataMethodInstance 인터페이스
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodInstance Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodInstance Interface
helpviewer.keywords:
- IXCLRDataMethodInstance Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 0eef69cea9f59911b5076f56579b0192be357431
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54659113"
---
# <a name="ixclrdatamethodinstance-interface"></a><span data-ttu-id="d5574-102">IXCLRDataMethodInstance 인터페이스</span><span class="sxs-lookup"><span data-stu-id="d5574-102">IXCLRDataMethodInstance Interface</span></span>

<span data-ttu-id="d5574-103">메서드 인스턴스에 대 한 정보를 쿼리 하기 위한 메서드를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5574-103">Provides methods for querying information about a method instance.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="d5574-104">메서드</span><span class="sxs-lookup"><span data-stu-id="d5574-104">Methods</span></span>

| <span data-ttu-id="d5574-105">메서드</span><span class="sxs-lookup"><span data-stu-id="d5574-105">Method</span></span>                                                                                                                  | <span data-ttu-id="d5574-106">설명</span><span class="sxs-lookup"><span data-stu-id="d5574-106">Description</span></span>                                 |
| ----------------------------------------------------------------------------------------------------------------------- | ------------------------------------------- |
| [<span data-ttu-id="d5574-107">GetILAddressMap</span><span class="sxs-lookup"><span data-stu-id="d5574-107">GetILAddressMap</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethodinstance-getiladdressmap-method.md) | <span data-ttu-id="d5574-108">IL을 주소 매핑 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d5574-108">Gets the IL to address mapping information.</span></span> |

## <a name="remarks"></a><span data-ttu-id="d5574-109">설명</span><span class="sxs-lookup"><span data-stu-id="d5574-109">Remarks</span></span>

<span data-ttu-id="d5574-110">이 인터페이스는 런타임 내에서 있으며 모든 헤더 또는 라이브러리 파일을 통해 노출 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5574-110">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="d5574-111">그러나 COM 인터페이스에서 파생 되는 것 `IUnknown` GUID를 사용 하 여 `ECD73800-22CA-4b0d-AB55-E9BA7E6318A5` 일반적인 COM 메커니즘을 통해 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5574-111">However, it's a COM interface that derives from `IUnknown` with GUID `ECD73800-22CA-4b0d-AB55-E9BA7E6318A5` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5574-112">요구 사항</span><span class="sxs-lookup"><span data-stu-id="d5574-112">Requirements</span></span>

<span data-ttu-id="d5574-113">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="d5574-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="d5574-114">**헤더:** 없음</span><span class="sxs-lookup"><span data-stu-id="d5574-114">**Header:** None</span></span>  
<span data-ttu-id="d5574-115">**라이브러리:** 없음</span><span class="sxs-lookup"><span data-stu-id="d5574-115">**Library:** None</span></span>  
<span data-ttu-id="d5574-116">**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="d5574-116">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="d5574-117">참고자료</span><span class="sxs-lookup"><span data-stu-id="d5574-117">See also</span></span>

- [<span data-ttu-id="d5574-118">디버깅</span><span class="sxs-lookup"><span data-stu-id="d5574-118">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="d5574-119">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="d5574-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
