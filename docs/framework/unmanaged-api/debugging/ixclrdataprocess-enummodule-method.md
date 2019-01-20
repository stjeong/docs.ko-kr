---
title: IXCLRDataProcess::EnumModule 메서드
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EnumModule Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EnumModule Method
helpviewer.keywords:
- IXCLRDataProcess::EnumModule Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: fa1e41985444324627c6b66a109b4619d85fc57f
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416678"
---
# <a name="ixclrdataprocessenummodule-method"></a><span data-ttu-id="f5d7b-102">IXCLRDataProcess::EnumModule 메서드</span><span class="sxs-lookup"><span data-stu-id="f5d7b-102">IXCLRDataProcess::EnumModule Method</span></span>

<span data-ttu-id="f5d7b-103">이 프로세스의 모듈을 열거합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-103">Enumerates the modules of this process.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="f5d7b-104">구문</span><span class="sxs-lookup"><span data-stu-id="f5d7b-104">Syntax</span></span>

```
HRESULT EnumModule(
    [in, out] CLRDATA_ENUM  *handle,
    [out] IXCLRDataModule  **mod
);
```

### <a name="parameters"></a><span data-ttu-id="f5d7b-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f5d7b-105">Parameters</span></span>

<span data-ttu-id="f5d7b-106">`handle` [out에서] 모듈을 열거 하는 것에 대 한 핸들입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-106">`handle` [in, out] A handle for enumerating the modules.</span></span>

<span data-ttu-id="f5d7b-107">`mod` [out] 열거 된 모듈입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-107">`mod` [out] The enumerated module.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5d7b-108">설명</span><span class="sxs-lookup"><span data-stu-id="f5d7b-108">Remarks</span></span>

<span data-ttu-id="f5d7b-109">제공 된 메서드는의 일부는 `IXCLRDataProcess` 인터페이스 및 가상 메서드 테이블의 25 슬롯에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 25th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5d7b-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="f5d7b-110">Requirements</span></span>

<span data-ttu-id="f5d7b-111">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="f5d7b-112">**헤더:** 없음</span><span class="sxs-lookup"><span data-stu-id="f5d7b-112">**Header:** None</span></span>  
<span data-ttu-id="f5d7b-113">**라이브러리:** 없음</span><span class="sxs-lookup"><span data-stu-id="f5d7b-113">**Library:** None</span></span>  
<span data-ttu-id="f5d7b-114">**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="f5d7b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="f5d7b-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f5d7b-115">See Also</span></span>

- [<span data-ttu-id="f5d7b-116">CLRDataSourceType 열거형</span><span class="sxs-lookup"><span data-stu-id="f5d7b-116">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="f5d7b-117">디버깅</span><span class="sxs-lookup"><span data-stu-id="f5d7b-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="f5d7b-118">IXCLRDataModule 인터페이스</span><span class="sxs-lookup"><span data-stu-id="f5d7b-118">IXCLRDataModule Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-interface.md)
- [<span data-ttu-id="f5d7b-119">IXCLRDataProcess 인터페이스</span><span class="sxs-lookup"><span data-stu-id="f5d7b-119">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
