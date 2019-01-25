---
title: IXCLRDataMethodDefinition::EnumInstance 메서드
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodDefinition::EnumInstance Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodDefinition::EnumInstance Method
helpviewer.keywords:
- IXCLRDataMethodDefinition::EnumInstance Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 0fbb246f8c4bf791dd705aedf8eab6ef8bfeae56
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54680268"
---
# <a name="ixclrdatamethoddefinitionenuminstance-method"></a><span data-ttu-id="04ab6-102">IXCLRDataMethodDefinition::EnumInstance 메서드</span><span class="sxs-lookup"><span data-stu-id="04ab6-102">IXCLRDataMethodDefinition::EnumInstance Method</span></span>

<span data-ttu-id="04ab6-103">이 메서드 정의의 인스턴스를 열거 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ab6-103">Enumerates the instances of this method definition.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="04ab6-104">구문</span><span class="sxs-lookup"><span data-stu-id="04ab6-104">Syntax</span></span>

```
HRESULT EnumInstance(
    [in, out] CLRDATA_ENUM         *handle,
    [out] IXCLRDataMethodInstance **instance
);
```

### <a name="parameters"></a><span data-ttu-id="04ab6-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="04ab6-105">Parameters</span></span>

<span data-ttu-id="04ab6-106">`handle` [out에서] 인스턴스를 열거 하는 것에 대 한 핸들입니다.</span><span class="sxs-lookup"><span data-stu-id="04ab6-106">`handle` [in, out] A handle for enumerating the instances.</span></span>

<span data-ttu-id="04ab6-107">`instance` [out] 열거 된 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="04ab6-107">`instance` [out] The enumerated instance.</span></span>

## <a name="remarks"></a><span data-ttu-id="04ab6-108">설명</span><span class="sxs-lookup"><span data-stu-id="04ab6-108">Remarks</span></span>

<span data-ttu-id="04ab6-109">제공 된 메서드는의 일부는 `IXCLRDataMethodDefinition` 인터페이스 및 가상 메서드 테이블의 네 번째 슬롯에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ab6-109">The provided method is part of the `IXCLRDataMethodDefinition` interface and corresponds to the fourth slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="04ab6-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="04ab6-110">Requirements</span></span>

<span data-ttu-id="04ab6-111">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="04ab6-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="04ab6-112">**헤더:** 없음</span><span class="sxs-lookup"><span data-stu-id="04ab6-112">**Header:** None</span></span>  
<span data-ttu-id="04ab6-113">**라이브러리:** 없음</span><span class="sxs-lookup"><span data-stu-id="04ab6-113">**Library:** None</span></span>  
<span data-ttu-id="04ab6-114">**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="04ab6-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="04ab6-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="04ab6-115">See also</span></span>

- [<span data-ttu-id="04ab6-116">CLRDataSourceType 열거형</span><span class="sxs-lookup"><span data-stu-id="04ab6-116">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="04ab6-117">디버깅</span><span class="sxs-lookup"><span data-stu-id="04ab6-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="04ab6-118">IXCLRDataMethodDefinition 인터페이스</span><span class="sxs-lookup"><span data-stu-id="04ab6-118">IXCLRDataMethodDefinition Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethoddefinition-interface.md)
- [<span data-ttu-id="04ab6-119">IXCLRDataMethodInstance 인터페이스</span><span class="sxs-lookup"><span data-stu-id="04ab6-119">IXCLRDataMethodInstance Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethodinstance-interface.md)
