---
title: ISOSDacInterface::GetMethodDescData 메서드
ms.date: 01/16/2019
api.name:
- ISOSDacInterface::GetMethodDescData Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- ISOSDacInterface::GetMethodDescData Method
helpviewer.keywords:
- ISOSDacInterface::GetMethodDescData Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 3f22752446413c622a20340541b0ac328f63c77b
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416733"
---
# <a name="isosdacinterfacegetmethoddescdata-method"></a><span data-ttu-id="820a1-102">ISOSDacInterface::GetMethodDescData 메서드</span><span class="sxs-lookup"><span data-stu-id="820a1-102">ISOSDacInterface::GetMethodDescData Method</span></span>

<span data-ttu-id="820a1-103">에 대 한 데이터를 가져옵니다는 주어진 [MethodDesc](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="820a1-103">Gets the data for the given [MethodDesc](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md).</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="820a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="820a1-104">Syntax</span></span>

```
HRESULT GetMethodDescData(
    CLRDATA_ADDRESS            methodDesc,
    CLRDATA_ADDRESS            ip,
    void                       *data,
    ULONG                      cRevertedRejitVersions,
    void                      *rgRevertedRejitData,
    void                      *pcNeededRevertedRejitData
);
```

### <a name="parameters"></a><span data-ttu-id="820a1-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="820a1-105">Parameters</span></span>

<span data-ttu-id="820a1-106">`methodDesc` [in] 주소는 MethodDesc입니다.</span><span class="sxs-lookup"><span data-stu-id="820a1-106">`methodDesc` [in] The address of the MethodDesc.</span></span>

<span data-ttu-id="820a1-107">`ip` [in] 메서드의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="820a1-107">`ip` [in] The IP address of the method.</span></span>

<span data-ttu-id="820a1-108">`data` [out] 내부 Api에서 반환 되는 MethodDesc와 연결 된 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="820a1-108">`data` [out] The data associated with the MethodDesc as returned from the internal APIs.</span></span> <span data-ttu-id="820a1-109">구조에는 168 바이트 이상 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="820a1-109">The structure needs at least 168 bytes.</span></span>

<span data-ttu-id="820a1-110">`cRevertedRejitVersions` [out] 되돌린된 rejit 버전 수입니다.</span><span class="sxs-lookup"><span data-stu-id="820a1-110">`cRevertedRejitVersions` [out] The number of reverted rejit versions.</span></span>

<span data-ttu-id="820a1-111">`rgRevertedRejitData` [out] 내부 Api에서 반환 된 되돌린된 rejit 버전과 연결 된 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="820a1-111">`rgRevertedRejitData` [out] The data associated with the reverted rejit versions as returned from the internal APIs.</span></span> <span data-ttu-id="820a1-112">구조에는 24 바이트 이상 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="820a1-112">The structure needs at least 24 bytes.</span></span>

<span data-ttu-id="820a1-113">`pcNeededRevertedRejitData` [out] 되돌린된 ReJit 버전과 연결 된 데이터를 저장 하는 데 필요한 바이트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="820a1-113">`pcNeededRevertedRejitData` [out] The number of bytes required to store the data associated with the reverted ReJit versions.</span></span>

## <a name="remarks"></a><span data-ttu-id="820a1-114">설명</span><span class="sxs-lookup"><span data-stu-id="820a1-114">Remarks</span></span>

<span data-ttu-id="820a1-115">제공 된 메서드는의 일부는 `ISOSDacInterface` 인터페이스 및 가상 메서드 테이블의 20 슬롯에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="820a1-115">The provided method is part of the `ISOSDacInterface` interface and corresponds to the 20th slot of the virtual method table.</span></span> <span data-ttu-id="820a1-116">또한는 `CLRDATA_ADDRESS` 은 64 비트 부호 없는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="820a1-116">Also the `CLRDATA_ADDRESS` are 64-bit unsigned integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="820a1-117">요구 사항</span><span class="sxs-lookup"><span data-stu-id="820a1-117">Requirements</span></span>

<span data-ttu-id="820a1-118">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="820a1-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="820a1-119">**헤더:** 없음</span><span class="sxs-lookup"><span data-stu-id="820a1-119">**Header:** None</span></span>  
<span data-ttu-id="820a1-120">**라이브러리:** 없음</span><span class="sxs-lookup"><span data-stu-id="820a1-120">**Library:** None</span></span>  
<span data-ttu-id="820a1-121">**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="820a1-121">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="820a1-122">참고 항목</span><span class="sxs-lookup"><span data-stu-id="820a1-122">See Also</span></span>

- [<span data-ttu-id="820a1-123">디버깅</span><span class="sxs-lookup"><span data-stu-id="820a1-123">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="820a1-124">ISOSDacInterface 인터페이스</span><span class="sxs-lookup"><span data-stu-id="820a1-124">ISOSDacInterface Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/isosdacinterface-interface.md)
