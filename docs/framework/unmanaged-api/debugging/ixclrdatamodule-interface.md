---
title: IXCLRDataModule 인터페이스
ms.date: 01/16/2019
api.name:
- IXCLRDataModule Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataModule Interface
helpviewer.keywords:
- IXCLRDataModule Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: e306834166051ae48fd283d51f18d9458091578f
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416663"
---
# <a name="ixclrdatamodule-interface"></a><span data-ttu-id="c7e84-102">IXCLRDataModule 인터페이스</span><span class="sxs-lookup"><span data-stu-id="c7e84-102">IXCLRDataModule Interface</span></span>

<span data-ttu-id="c7e84-103">로드 된 모듈에 대 한 정보를 쿼리 하기 위한 메서드를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7e84-103">Provides methods for querying information about a loaded module.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="c7e84-104">메서드</span><span class="sxs-lookup"><span data-stu-id="c7e84-104">Methods</span></span>

| <span data-ttu-id="c7e84-105">메서드</span><span class="sxs-lookup"><span data-stu-id="c7e84-105">Method</span></span>                                                                                                                                | <span data-ttu-id="c7e84-106">설명</span><span class="sxs-lookup"><span data-stu-id="c7e84-106">Description</span></span>                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="c7e84-107">GetMethodDefinitionByToken</span><span class="sxs-lookup"><span data-stu-id="c7e84-107">GetMethodDefinitionByToken</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-getmethoddefinitionbytoken-method.md) | <span data-ttu-id="c7e84-108">지정 된 메타 데이터 토큰에 해당 하는 메서드 정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c7e84-108">Gets the method definition corresponding to a given metadata token.</span></span> |
| [<span data-ttu-id="c7e84-109">요청</span><span class="sxs-lookup"><span data-stu-id="c7e84-109">Request</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-request-method.md)                                       | <span data-ttu-id="c7e84-110">모듈의 데이터를 사용 하 여 지정 된 버퍼를 채우는 데 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7e84-110">Requests to populate the buffer given with the module's data.</span></span>       |
| [<span data-ttu-id="c7e84-111">GetVersionId</span><span class="sxs-lookup"><span data-stu-id="c7e84-111">GetVersionId</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-getversionid-method.md)                             | <span data-ttu-id="c7e84-112">모듈의 버전 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c7e84-112">Gets the module's version ID.</span></span>                                       |

## <a name="remarks"></a><span data-ttu-id="c7e84-113">설명</span><span class="sxs-lookup"><span data-stu-id="c7e84-113">Remarks</span></span>

<span data-ttu-id="c7e84-114">이 인터페이스는 런타임 내에서 있으며 모든 헤더 또는 라이브러리 파일을 통해 노출 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7e84-114">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="c7e84-115">그러나 COM 인터페이스에서 파생 되는 것 `IUnknown` GUID를 사용 하 여 `88E32849-0A0A-4cb0-9022-7CD2E9E139E2` 일반적인 COM 메커니즘을 통해 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7e84-115">However, it's a COM interface that derives from `IUnknown` with GUID `88E32849-0A0A-4cb0-9022-7CD2E9E139E2` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7e84-116">요구 사항</span><span class="sxs-lookup"><span data-stu-id="c7e84-116">Requirements</span></span>

<span data-ttu-id="c7e84-117">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="c7e84-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="c7e84-118">**헤더:** 없음</span><span class="sxs-lookup"><span data-stu-id="c7e84-118">**Header:** None</span></span>  
<span data-ttu-id="c7e84-119">**라이브러리:** 없음</span><span class="sxs-lookup"><span data-stu-id="c7e84-119">**Library:** None</span></span>  
<span data-ttu-id="c7e84-120">**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="c7e84-120">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="c7e84-121">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c7e84-121">See Also</span></span>

- [<span data-ttu-id="c7e84-122">디버깅</span><span class="sxs-lookup"><span data-stu-id="c7e84-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="c7e84-123">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="c7e84-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
