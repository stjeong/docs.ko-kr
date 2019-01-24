---
title: IXCLRDataProcess::StartEnumMethodInstancesByAddress 메서드
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::StartEnumMethodInstancesByAddress Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::StartEnumMethodInstancesByAddress Method
helpviewer.keywords:
- IXCLRDataProcess::StartEnumMethodInstancesByAddress Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 9afbf0665b114169661a74b60c744203d160fed3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54662623"
---
# <a name="ixclrdataprocessstartenummethodinstancesbyaddress-method"></a><span data-ttu-id="8fa5e-102">IXCLRDataProcess::StartEnumMethodInstancesByAddress 메서드</span><span class="sxs-lookup"><span data-stu-id="8fa5e-102">IXCLRDataProcess::StartEnumMethodInstancesByAddress Method</span></span>

<span data-ttu-id="8fa5e-103">메서드 인스턴스를 열거 핸들을 제공 `AppDomain` 지정된 된 주소에서 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-103">Provides a handle to enumerate the method instances of `AppDomain` starting at a given address.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="8fa5e-104">구문</span><span class="sxs-lookup"><span data-stu-id="8fa5e-104">Syntax</span></span>

```
HRESULT StartEnumMethodInstancesByAddress(
    [in] CLRDATA_ADDRESS     address,
    [in] IXCLRDataAppDomain *appDomain,
    [out] CLRDATA_ENUM      *handle
);
```

### <a name="parameters"></a><span data-ttu-id="8fa5e-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8fa5e-105">Parameters</span></span>

<span data-ttu-id="8fa5e-106">`address` [in] 첫 번째 메서드 인스턴스의 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-106">`address` [in] The address of the first method instance.</span></span>

<span data-ttu-id="8fa5e-107">`appDomain` [in] 메서드 인스턴스의 AppDomain 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-107">`appDomain` [in] The AppDomain of the method instances.</span></span>

<span data-ttu-id="8fa5e-108">`handle` [out] 메서드 인스턴스를 열거 하는 것에 대 한 핸들입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-108">`handle` [out] A handle for enumerating the method instances.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fa5e-109">설명</span><span class="sxs-lookup"><span data-stu-id="8fa5e-109">Remarks</span></span>

<span data-ttu-id="8fa5e-110">제공 된 메서드는의 일부는 `IXCLRDataProcess` 인터페이스 및 가상 메서드 테이블의 27 슬롯에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-110">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 27th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fa5e-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="8fa5e-111">Requirements</span></span>

<span data-ttu-id="8fa5e-112">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="8fa5e-113">**헤더:** 없음</span><span class="sxs-lookup"><span data-stu-id="8fa5e-113">**Header:** None</span></span>  
<span data-ttu-id="8fa5e-114">**라이브러리:** 없음</span><span class="sxs-lookup"><span data-stu-id="8fa5e-114">**Library:** None</span></span>  
<span data-ttu-id="8fa5e-115">**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="8fa5e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="8fa5e-116">참고자료</span><span class="sxs-lookup"><span data-stu-id="8fa5e-116">See also</span></span>

- [<span data-ttu-id="8fa5e-117">CLRDataSourceType 열거형</span><span class="sxs-lookup"><span data-stu-id="8fa5e-117">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="8fa5e-118">디버깅</span><span class="sxs-lookup"><span data-stu-id="8fa5e-118">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="8fa5e-119">IXCLRDataProcess 인터페이스</span><span class="sxs-lookup"><span data-stu-id="8fa5e-119">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
