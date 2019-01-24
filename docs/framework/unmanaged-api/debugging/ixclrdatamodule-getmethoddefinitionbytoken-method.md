---
title: IXCLRDataModule::GetMethodDefinitionByToken 메서드
ms.date: 01/16/2019
api.name:
- IXCLRDataModule::GetMethodDefinitionByToken Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataModule::GetMethodDefinitionByToken Method
helpviewer.keywords:
- IXCLRDataModule::GetMethodDefinitionByToken Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 1371b86f30324908a639b3b1bbae0ae007ba590a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54708092"
---
# <a name="ixclrdatamodulegetmethoddefinitionbytoken-method"></a><span data-ttu-id="7f976-102">IXCLRDataModule::GetMethodDefinitionByToken 메서드</span><span class="sxs-lookup"><span data-stu-id="7f976-102">IXCLRDataModule::GetMethodDefinitionByToken Method</span></span>

<span data-ttu-id="7f976-103">지정 된 메타 데이터 토큰에 해당 하는 메서드 정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f976-103">Gets the method definition corresponding to a given metadata token.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="7f976-104">구문</span><span class="sxs-lookup"><span data-stu-id="7f976-104">Syntax</span></span>

```
HRESULT GetMethodDefinitionByToken(
    [in] mdMethodDef token,
    [out] IXCLRDataMethodDefinition** methodDefinition
);
```

### <a name="parameters"></a><span data-ttu-id="7f976-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7f976-105">Parameters</span></span>

<span data-ttu-id="7f976-106">`token` [in] 메서드 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="7f976-106">`token` [in] The method token.</span></span>

<span data-ttu-id="7f976-107">`methodDefinition` [out] 메서드 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="7f976-107">`methodDefinition` [out] The method definition.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f976-108">설명</span><span class="sxs-lookup"><span data-stu-id="7f976-108">Remarks</span></span>

<span data-ttu-id="7f976-109">제공 된 메서드는의 일부는 `IXCLRDataModule` 인터페이스 및 가상 메서드 테이블의 25 슬롯에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f976-109">The provided method is part of the `IXCLRDataModule` interface and corresponds to the 25th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f976-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="7f976-110">Requirements</span></span>

<span data-ttu-id="7f976-111">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="7f976-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="7f976-112">**헤더:** 없음</span><span class="sxs-lookup"><span data-stu-id="7f976-112">**Header:** None</span></span>  
<span data-ttu-id="7f976-113">**라이브러리:** 없음</span><span class="sxs-lookup"><span data-stu-id="7f976-113">**Library:** None</span></span>  
<span data-ttu-id="7f976-114">**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="7f976-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  
 
## <a name="see-also"></a><span data-ttu-id="7f976-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="7f976-115">See also</span></span>

- [<span data-ttu-id="7f976-116">디버깅</span><span class="sxs-lookup"><span data-stu-id="7f976-116">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="7f976-117">IXCLRDataModule 인터페이스</span><span class="sxs-lookup"><span data-stu-id="7f976-117">IXCLRDataModule Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-interface.md)
