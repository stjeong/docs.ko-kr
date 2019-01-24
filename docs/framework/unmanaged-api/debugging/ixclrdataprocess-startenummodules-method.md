---
title: IXCLRDataProcess::StartEnumModules 메서드
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::StartEnumModules Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::StartEnumModules Method
helpviewer.keywords:
- IXCLRDataProcess::StartEnumModules Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 4a086157b27b7426cb6d5f17f13426c0f26d2b2d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54658223"
---
# <a name="ixclrdataprocessstartenummodules-method"></a><span data-ttu-id="7c2b3-102">IXCLRDataProcess::StartEnumModules 메서드</span><span class="sxs-lookup"><span data-stu-id="7c2b3-102">IXCLRDataProcess::StartEnumModules Method</span></span>

<span data-ttu-id="7c2b3-103">프로세스의 모듈을 열거에 대 한 핸들을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-103">Provides a handle to enumerate the modules of a process.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="7c2b3-104">구문</span><span class="sxs-lookup"><span data-stu-id="7c2b3-104">Syntax</span></span>

```
HRESULT StartEnumModules(
    [out] CLRDATA_ENUM *handle
);
```

### <a name="parameters"></a><span data-ttu-id="7c2b3-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7c2b3-105">Parameters</span></span>

<span data-ttu-id="7c2b3-106">`handle` [out] 모듈을 열거 하는 것에 대 한 핸들입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-106">`handle` [out] A handle for enumerating the modules.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c2b3-107">설명</span><span class="sxs-lookup"><span data-stu-id="7c2b3-107">Remarks</span></span>

<span data-ttu-id="7c2b3-108">제공 된 메서드는의 일부는 `IXCLRDataProcess` 인터페이스 및 가상 메서드 테이블의 24 슬롯에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-108">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 24th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c2b3-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="7c2b3-109">Requirements</span></span>

<span data-ttu-id="7c2b3-110">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="7c2b3-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="7c2b3-111">**헤더:** 없음</span><span class="sxs-lookup"><span data-stu-id="7c2b3-111">**Header:** None</span></span>  
<span data-ttu-id="7c2b3-112">**라이브러리:** 없음</span><span class="sxs-lookup"><span data-stu-id="7c2b3-112">**Library:** None</span></span>  
<span data-ttu-id="7c2b3-113">**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="7c2b3-113">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="7c2b3-114">참고자료</span><span class="sxs-lookup"><span data-stu-id="7c2b3-114">See also</span></span>

- [<span data-ttu-id="7c2b3-115">CLRDataSourceType 열거형</span><span class="sxs-lookup"><span data-stu-id="7c2b3-115">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="7c2b3-116">디버깅</span><span class="sxs-lookup"><span data-stu-id="7c2b3-116">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="7c2b3-117">IXCLRDataProcess 인터페이스</span><span class="sxs-lookup"><span data-stu-id="7c2b3-117">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
