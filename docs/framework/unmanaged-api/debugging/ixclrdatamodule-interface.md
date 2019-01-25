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
ms.openlocfilehash: c8d6e36687fd43bbc59304eee64dd42eb78101e3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54676525"
---
# <a name="ixclrdatamodule-interface"></a><span data-ttu-id="28fdf-102">IXCLRDataModule 인터페이스</span><span class="sxs-lookup"><span data-stu-id="28fdf-102">IXCLRDataModule Interface</span></span>

<span data-ttu-id="28fdf-103">로드 된 모듈에 대 한 정보를 쿼리 하기 위한 메서드를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="28fdf-103">Provides methods for querying information about a loaded module.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="28fdf-104">메서드</span><span class="sxs-lookup"><span data-stu-id="28fdf-104">Methods</span></span>

| <span data-ttu-id="28fdf-105">메서드</span><span class="sxs-lookup"><span data-stu-id="28fdf-105">Method</span></span>                                                                                                                                | <span data-ttu-id="28fdf-106">설명</span><span class="sxs-lookup"><span data-stu-id="28fdf-106">Description</span></span>                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="28fdf-107">GetMethodDefinitionByToken</span><span class="sxs-lookup"><span data-stu-id="28fdf-107">GetMethodDefinitionByToken</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-getmethoddefinitionbytoken-method.md) | <span data-ttu-id="28fdf-108">지정 된 메타 데이터 토큰에 해당 하는 메서드 정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28fdf-108">Gets the method definition corresponding to a given metadata token.</span></span> |
| [<span data-ttu-id="28fdf-109">요청</span><span class="sxs-lookup"><span data-stu-id="28fdf-109">Request</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-request-method.md)                                       | <span data-ttu-id="28fdf-110">모듈의 데이터를 사용 하 여 지정 된 버퍼를 채우는 데 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="28fdf-110">Requests to populate the buffer given with the module's data.</span></span>       |
| [<span data-ttu-id="28fdf-111">GetVersionId</span><span class="sxs-lookup"><span data-stu-id="28fdf-111">GetVersionId</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-getversionid-method.md)                             | <span data-ttu-id="28fdf-112">모듈의 버전 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28fdf-112">Gets the module's version ID.</span></span>                                       |

## <a name="remarks"></a><span data-ttu-id="28fdf-113">설명</span><span class="sxs-lookup"><span data-stu-id="28fdf-113">Remarks</span></span>

<span data-ttu-id="28fdf-114">이 인터페이스는 런타임 내에서 있으며 모든 헤더 또는 라이브러리 파일을 통해 노출 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28fdf-114">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="28fdf-115">그러나 COM 인터페이스에서 파생 되는 것 `IUnknown` GUID를 사용 하 여 `88E32849-0A0A-4cb0-9022-7CD2E9E139E2` 일반적인 COM 메커니즘을 통해 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28fdf-115">However, it's a COM interface that derives from `IUnknown` with GUID `88E32849-0A0A-4cb0-9022-7CD2E9E139E2` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="28fdf-116">요구 사항</span><span class="sxs-lookup"><span data-stu-id="28fdf-116">Requirements</span></span>

<span data-ttu-id="28fdf-117">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="28fdf-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="28fdf-118">**헤더:** 없음</span><span class="sxs-lookup"><span data-stu-id="28fdf-118">**Header:** None</span></span>  
<span data-ttu-id="28fdf-119">**라이브러리:** 없음</span><span class="sxs-lookup"><span data-stu-id="28fdf-119">**Library:** None</span></span>  
<span data-ttu-id="28fdf-120">**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="28fdf-120">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="28fdf-121">참고자료</span><span class="sxs-lookup"><span data-stu-id="28fdf-121">See also</span></span>

- [<span data-ttu-id="28fdf-122">디버깅</span><span class="sxs-lookup"><span data-stu-id="28fdf-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="28fdf-123">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="28fdf-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
