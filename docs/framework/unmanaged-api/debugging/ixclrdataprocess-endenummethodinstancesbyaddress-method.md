---
title: IXCLRDataProcess::EndEnumMethodInstancesByAddress 메서드
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EndEnumMethodInstancesByAddress Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EndEnumMethodInstancesByAddress Method
helpviewer.keywords:
- IXCLRDataProcess::EndEnumMethodInstancesByAddress Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 67978e49a8c23c4b25234ecbb3639c696c7232f4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54655649"
---
# <a name="ixclrdataprocessendenummethodinstancesbyaddress-method"></a><span data-ttu-id="8ee2a-102">IXCLRDataProcess::EndEnumMethodInstancesByAddress 메서드</span><span class="sxs-lookup"><span data-stu-id="8ee2a-102">IXCLRDataProcess::EndEnumMethodInstancesByAddress Method</span></span>

<span data-ttu-id="8ee2a-103">인스턴스 열거 하는 동안 사용 되는 내부 반복기 사용 하는 리소스를 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ee2a-103">Releases the resources used by internal iterators used during instance enumeration.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="8ee2a-104">구문</span><span class="sxs-lookup"><span data-stu-id="8ee2a-104">Syntax</span></span>

```
HRESULT EndEnumMethodInstancesByAddress(
    [in] CLRDATA_ENUM handle
);
```

### <a name="parameters"></a><span data-ttu-id="8ee2a-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8ee2a-105">Parameters</span></span>

<span data-ttu-id="8ee2a-106">`handle` [out] 메서드 인스턴스를 열거 하는 것에 대 한 핸들입니다.</span><span class="sxs-lookup"><span data-stu-id="8ee2a-106">`handle` [out] A handle for enumerating the method instances.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ee2a-107">설명</span><span class="sxs-lookup"><span data-stu-id="8ee2a-107">Remarks</span></span>

<span data-ttu-id="8ee2a-108">제공 된 메서드는의 일부는 `IXCLRDataProcess` 인터페이스 및 가상 메서드 테이블의 29 슬롯에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ee2a-108">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 29th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ee2a-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="8ee2a-109">Requirements</span></span>

<span data-ttu-id="8ee2a-110">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="8ee2a-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="8ee2a-111">**헤더:** 없음</span><span class="sxs-lookup"><span data-stu-id="8ee2a-111">**Header:** None</span></span>  
<span data-ttu-id="8ee2a-112">**라이브러리:** 없음</span><span class="sxs-lookup"><span data-stu-id="8ee2a-112">**Library:** None</span></span>  
<span data-ttu-id="8ee2a-113">**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="8ee2a-113">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="8ee2a-114">참고자료</span><span class="sxs-lookup"><span data-stu-id="8ee2a-114">See also</span></span>

- [<span data-ttu-id="8ee2a-115">CLRDataSourceType 열거형</span><span class="sxs-lookup"><span data-stu-id="8ee2a-115">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="8ee2a-116">디버깅</span><span class="sxs-lookup"><span data-stu-id="8ee2a-116">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="8ee2a-117">IXCLRDataProcess 인터페이스</span><span class="sxs-lookup"><span data-stu-id="8ee2a-117">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
