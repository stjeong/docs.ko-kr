---
title: IXCLRDataMethodDefinition::EndEnumInstances 메서드
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodDefinition::EndEnumInstances Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodDefinition::EndEnumInstances Method
helpviewer.keywords:
- IXCLRDataMethodDefinition::EndEnumInstances Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 7901ba3ac95052e265df619d06996b4c9ce8baa6
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416553"
---
# <a name="ixclrdatamethoddefinitionendenuminstances-method"></a><span data-ttu-id="667a0-102">IXCLRDataMethodDefinition::EndEnumInstances 메서드</span><span class="sxs-lookup"><span data-stu-id="667a0-102">IXCLRDataMethodDefinition::EndEnumInstances Method</span></span>

<span data-ttu-id="667a0-103">인스턴스 열거 하는 동안 사용 되는 내부 반복기 사용 하는 리소스를 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="667a0-103">Releases the resources used by internal iterators used during instance enumeration.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="667a0-104">구문</span><span class="sxs-lookup"><span data-stu-id="667a0-104">Syntax</span></span>

```
HRESULT EndEnumInstances(
    [in] CLRDATA_ENUM handle
);
```

### <a name="parameters"></a><span data-ttu-id="667a0-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="667a0-105">Parameters</span></span>

<span data-ttu-id="667a0-106">`handle` [out] 인스턴스를 열거 하는 것에 대 한 핸들입니다.</span><span class="sxs-lookup"><span data-stu-id="667a0-106">`handle` [out] A handle for enumerating the instances.</span></span>

## <a name="remarks"></a><span data-ttu-id="667a0-107">설명</span><span class="sxs-lookup"><span data-stu-id="667a0-107">Remarks</span></span>

<span data-ttu-id="667a0-108">제공 된 메서드는의 일부는 `IXCLRDataMethodDefinition` 인터페이스 및 가상 메서드 테이블의 다섯 번째 슬롯에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="667a0-108">The provided method is part of the `IXCLRDataMethodDefinition` interface and corresponds to the fifth slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="667a0-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="667a0-109">Requirements</span></span>

<span data-ttu-id="667a0-110">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="667a0-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="667a0-111">**헤더:** 없음</span><span class="sxs-lookup"><span data-stu-id="667a0-111">**Header:** None</span></span>  
<span data-ttu-id="667a0-112">**라이브러리:** 없음</span><span class="sxs-lookup"><span data-stu-id="667a0-112">**Library:** None</span></span>  
<span data-ttu-id="667a0-113">**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="667a0-113">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="667a0-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="667a0-114">See Also</span></span>

- [<span data-ttu-id="667a0-115">디버깅</span><span class="sxs-lookup"><span data-stu-id="667a0-115">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="667a0-116">IXCLRDataMethodDefinition 인터페이스</span><span class="sxs-lookup"><span data-stu-id="667a0-116">IXCLRDataMethodDefinition Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethoddefinition-interface.md)
