---
title: ISOSDacInterface 인터페이스
ms.date: 01/16/2019
api.name:
- ISOSDacInterface Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- ISOSDacInterface Interface
helpviewer.keywords:
- ISOSDacInterface Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 745ecfbffaad841e1ceb9216802644ba9dd5b94e
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416513"
---
# <a name="isosdacinterface-interface"></a><span data-ttu-id="9d08c-102">ISOSDacInterface 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9d08c-102">ISOSDacInterface Interface</span></span>

<span data-ttu-id="9d08c-103">데이터에 액세스할 도우미 메서드를 제공 `SOS`합니다.</span><span class="sxs-lookup"><span data-stu-id="9d08c-103">Provides helper methods to access data from `SOS`.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="9d08c-104">메서드</span><span class="sxs-lookup"><span data-stu-id="9d08c-104">Methods</span></span>

| <span data-ttu-id="9d08c-105">메서드</span><span class="sxs-lookup"><span data-stu-id="9d08c-105">Method</span></span>                                                                                                               | <span data-ttu-id="9d08c-106">설명</span><span class="sxs-lookup"><span data-stu-id="9d08c-106">Description</span></span>                                                                                                                   |
| -------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| [<span data-ttu-id="9d08c-107">GetMethodDescData</span><span class="sxs-lookup"><span data-stu-id="9d08c-107">GetMethodDescData</span></span>](../../../../docs/framework/unmanaged-api/debugging/isosdacinterface-getmethoddescdata-method.md) | <span data-ttu-id="9d08c-108">에 대 한 데이터를 가져옵니다는 주어진 [MethodDesc](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="9d08c-108">Gets the data for the given [MethodDesc](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md).</span></span> |

## <a name="remarks"></a><span data-ttu-id="9d08c-109">설명</span><span class="sxs-lookup"><span data-stu-id="9d08c-109">Remarks</span></span>

<span data-ttu-id="9d08c-110">이 인터페이스는 런타임 내에서 있으며 모든 헤더 또는 라이브러리 파일을 통해 노출 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9d08c-110">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="9d08c-111">그러나 COM 인터페이스에서 파생 되는 것 `IUnknown` GUID를 사용 하 여 `436f00f2-b42a-4b9f-870c-e73db66ae930` 일반적인 COM 메커니즘을 통해 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9d08c-111">However, it's a COM interface that derives from `IUnknown` with GUID `436f00f2-b42a-4b9f-870c-e73db66ae930` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d08c-112">요구 사항</span><span class="sxs-lookup"><span data-stu-id="9d08c-112">Requirements</span></span>

<span data-ttu-id="9d08c-113">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="9d08c-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="9d08c-114">**헤더:** 없음</span><span class="sxs-lookup"><span data-stu-id="9d08c-114">**Header:** None</span></span>  
<span data-ttu-id="9d08c-115">**라이브러리:** 없음</span><span class="sxs-lookup"><span data-stu-id="9d08c-115">**Library:** None</span></span>  
<span data-ttu-id="9d08c-116">**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="9d08c-116">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="9d08c-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="9d08c-117">See Also</span></span>

- [<span data-ttu-id="9d08c-118">디버깅</span><span class="sxs-lookup"><span data-stu-id="9d08c-118">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="9d08c-119">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9d08c-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
