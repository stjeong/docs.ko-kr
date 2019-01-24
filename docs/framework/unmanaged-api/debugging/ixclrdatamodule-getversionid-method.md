---
title: IXCLRDataModule::GetVersionId 메서드
ms.date: 01/16/2019
api.name:
- IXCLRDataModule::GetVersionId Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataModule::GetVersionId Method
helpviewer.keywords:
- IXCLRDataModule::GetVersionId Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 5184db00b10b53011f24c5096b470608e84546b6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54567427"
---
# <a name="ixclrdatamodulegetversionid-method"></a><span data-ttu-id="91b95-102">IXCLRDataModule::GetVersionId 메서드</span><span class="sxs-lookup"><span data-stu-id="91b95-102">IXCLRDataModule::GetVersionId Method</span></span>

<span data-ttu-id="91b95-103">모듈의 버전 식별자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91b95-103">Gets the module's version identifier.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="91b95-104">구문</span><span class="sxs-lookup"><span data-stu-id="91b95-104">Syntax</span></span>

```
HRESULT GetVersionId(
    [out] GUID* vid
);
```

### <a name="parameters"></a><span data-ttu-id="91b95-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="91b95-105">Parameters</span></span>

<span data-ttu-id="91b95-106">`vid` [out] 모듈의 버전 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="91b95-106">`vid` [out] The module's version identifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="91b95-107">설명</span><span class="sxs-lookup"><span data-stu-id="91b95-107">Remarks</span></span>

<span data-ttu-id="91b95-108">제공 된 메서드는의 일부는 `IXCLRDataModule` 인터페이스 및 가상 메서드 테이블의 40 슬롯에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="91b95-108">The provided method is part of the `IXCLRDataModule` interface and corresponds to the 40th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="91b95-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="91b95-109">Requirements</span></span>

<span data-ttu-id="91b95-110">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="91b95-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="91b95-111">**헤더:** 없음</span><span class="sxs-lookup"><span data-stu-id="91b95-111">**Header:** None</span></span>  
<span data-ttu-id="91b95-112">**라이브러리:** 없음</span><span class="sxs-lookup"><span data-stu-id="91b95-112">**Library:** None</span></span>  
<span data-ttu-id="91b95-113">**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="91b95-113">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="91b95-114">참고자료</span><span class="sxs-lookup"><span data-stu-id="91b95-114">See also</span></span>

- [<span data-ttu-id="91b95-115">디버깅</span><span class="sxs-lookup"><span data-stu-id="91b95-115">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="91b95-116">IXCLRDataModule 인터페이스</span><span class="sxs-lookup"><span data-stu-id="91b95-116">IXCLRDataModule Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-interface.md)
