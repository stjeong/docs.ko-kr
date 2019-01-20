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
ms.openlocfilehash: ac4111abdf6a471aca1eca72a86e33698debbff6
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416558"
---
# <a name="ixclrdatamodulegetversionid-method"></a><span data-ttu-id="ebd8d-102">IXCLRDataModule::GetVersionId 메서드</span><span class="sxs-lookup"><span data-stu-id="ebd8d-102">IXCLRDataModule::GetVersionId Method</span></span>

<span data-ttu-id="ebd8d-103">모듈의 버전 식별자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ebd8d-103">Gets the module's version identifier.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="ebd8d-104">구문</span><span class="sxs-lookup"><span data-stu-id="ebd8d-104">Syntax</span></span>

```
HRESULT GetVersionId(
    [out] GUID* vid
);
```

### <a name="parameters"></a><span data-ttu-id="ebd8d-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ebd8d-105">Parameters</span></span>

<span data-ttu-id="ebd8d-106">`vid` [out] 모듈의 버전 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ebd8d-106">`vid` [out] The module's version identifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebd8d-107">설명</span><span class="sxs-lookup"><span data-stu-id="ebd8d-107">Remarks</span></span>

<span data-ttu-id="ebd8d-108">제공 된 메서드는의 일부는 `IXCLRDataModule` 인터페이스 및 가상 메서드 테이블의 40 슬롯에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebd8d-108">The provided method is part of the `IXCLRDataModule` interface and corresponds to the 40th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd8d-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="ebd8d-109">Requirements</span></span>

<span data-ttu-id="ebd8d-110">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="ebd8d-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="ebd8d-111">**헤더:** 없음</span><span class="sxs-lookup"><span data-stu-id="ebd8d-111">**Header:** None</span></span>  
<span data-ttu-id="ebd8d-112">**라이브러리:** 없음</span><span class="sxs-lookup"><span data-stu-id="ebd8d-112">**Library:** None</span></span>  
<span data-ttu-id="ebd8d-113">**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="ebd8d-113">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="ebd8d-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ebd8d-114">See Also</span></span>

- [<span data-ttu-id="ebd8d-115">디버깅</span><span class="sxs-lookup"><span data-stu-id="ebd8d-115">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="ebd8d-116">IXCLRDataModule 인터페이스</span><span class="sxs-lookup"><span data-stu-id="ebd8d-116">IXCLRDataModule Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-interface.md)
