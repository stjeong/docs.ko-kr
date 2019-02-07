---
title: ISOSDacInterface::GetMethodDescPtrFromIP 메서드
ms.date: 02/01/2019
api.name:
- ISOSDacInterface::GetMethodDescPtrFromIP Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- ISOSDacInterface::GetMethodDescPtrFromIP Method
helpviewer.keywords:
- ISOSDacInterface::GetMethodDescPtrFromIP Method [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: 74853733b1fb7f023d9f192d3e862dbf6875ecda
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55828658"
---
# <a name="isosdacinterfacegetmethoddescptrfromip-method"></a><span data-ttu-id="f089c-102">ISOSDacInterface::GetMethodDescPtrFromIP 메서드</span><span class="sxs-lookup"><span data-stu-id="f089c-102">ISOSDacInterface::GetMethodDescPtrFromIP Method</span></span>

<span data-ttu-id="f089c-103">특정된 네이티브 명령 주소를 포함 하는 메서드를 해당 MethodDesc의 포인터를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="f089c-103">Retrieves the pointer of the MethodDesc corresponding the method containing the given native instruction address.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="f089c-104">구문</span><span class="sxs-lookup"><span data-stu-id="f089c-104">Syntax</span></span>

```
HRESULT GetMethodDescPtrFromIP(
    CLRDATA_ADDRESS ip,
    CLRDATA_ADDRESS * ppMD
);
```

### <a name="parameters"></a><span data-ttu-id="f089c-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f089c-105">Parameters</span></span>

<span data-ttu-id="f089c-106">`ip` [in] 런타임 시 메서드 내에서 사용 되는 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="f089c-106">`ip` [in] An address within the method at runtime.</span></span>

<span data-ttu-id="f089c-107">`ppMD` [out] 주소는 `MethodDesc` 특정 메서드에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="f089c-107">`ppMD` [out] The address of the `MethodDesc` for the particular method.</span></span>

## <a name="remarks"></a><span data-ttu-id="f089c-108">설명</span><span class="sxs-lookup"><span data-stu-id="f089c-108">Remarks</span></span>

<span data-ttu-id="f089c-109">제공 된 메서드는의 일부를 [ `ISOSDacInterface` 인터페이스](isosdacinterface-interface.md) 가상 메서드 테이블의 21 슬롯에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="f089c-109">The provided method is part of the [`ISOSDacInterface` interface](isosdacinterface-interface.md) and corresponds to the 21st slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="f089c-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="f089c-110">Requirements</span></span>

<span data-ttu-id="f089c-111">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="f089c-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="f089c-112">**헤더:** 없음</span><span class="sxs-lookup"><span data-stu-id="f089c-112">**Header:** None</span></span>  
<span data-ttu-id="f089c-113">**라이브러리:** 없음</span><span class="sxs-lookup"><span data-stu-id="f089c-113">**Library:** None</span></span>  
<span data-ttu-id="f089c-114">**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="f089c-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="f089c-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="f089c-115">See also</span></span>

- [<span data-ttu-id="f089c-116">디버깅</span><span class="sxs-lookup"><span data-stu-id="f089c-116">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="f089c-117">ISOSDacInterface 인터페이스</span><span class="sxs-lookup"><span data-stu-id="f089c-117">ISOSDacInterface Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/isosdacinterface-interface.md)
