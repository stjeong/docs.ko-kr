---
title: ICorDebugClass::GetToken 메서드
ms.date: 03/30/2017
api_name:
- ICorDebugClass.GetToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugClass::GetToken
helpviewer_keywords:
- GetToken method, ICorDebugClass interface [.NET Framework debugging]
- ICorDebugClass::GetToken method [.NET Framework debugging]
ms.assetid: ee5c848a-eac4-4462-b07a-07ccd76a75df
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d6dc245a53c9ec7cbe56e20313abc4269e33f45c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54582320"
---
# <a name="icordebugclassgettoken-method"></a><span data-ttu-id="a1cb8-102">ICorDebugClass::GetToken 메서드</span><span class="sxs-lookup"><span data-stu-id="a1cb8-102">ICorDebugClass::GetToken Method</span></span>
<span data-ttu-id="a1cb8-103">가져옵니다는 `TypeDef` 이 클래스의 정의 참조 하는 메타 데이터 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="a1cb8-103">Gets the `TypeDef` metadata token that references the definition of this class.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a1cb8-104">구문</span><span class="sxs-lookup"><span data-stu-id="a1cb8-104">Syntax</span></span>  
  
```  
HRESULT GetToken (  
    [out] mdTypeDef          *pTypeDef  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a1cb8-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a1cb8-105">Parameters</span></span>  
 `pTypeDef`  
 <span data-ttu-id="a1cb8-106">[out] 에 대 한 포인터는 `mdTypeDef` 이 클래스의 정의 참조 하는 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="a1cb8-106">[out] A pointer to an `mdTypeDef` token that references the definition of this class.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a1cb8-107">요구 사항</span><span class="sxs-lookup"><span data-stu-id="a1cb8-107">Requirements</span></span>  
 <span data-ttu-id="a1cb8-108">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="a1cb8-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a1cb8-109">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a1cb8-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a1cb8-110">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a1cb8-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a1cb8-111">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a1cb8-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1cb8-112">참고자료</span><span class="sxs-lookup"><span data-stu-id="a1cb8-112">See also</span></span>
- [<span data-ttu-id="a1cb8-113">메타데이터 인터페이스</span><span class="sxs-lookup"><span data-stu-id="a1cb8-113">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
