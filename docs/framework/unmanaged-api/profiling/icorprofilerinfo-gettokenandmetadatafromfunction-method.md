---
title: ICorProfilerInfo::GetTokenAndMetadataFromFunction 메서드
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetTokenAndMetadataFromFunction
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetTokenAndMetadataFromFunction
helpviewer_keywords:
- ICorProfilerInfo::GetTokenAndMetadataFromFunction method [.NET Framework profiling]
- GetTokenAndMetadataFromFunction method [.NET Framework profiling]
ms.assetid: e525aa16-c923-4b16-833b-36f1f0dd70fc
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0561f76c70da603d50b96ce5b5162efac4eff2de
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54492979"
---
# <a name="icorprofilerinfogettokenandmetadatafromfunction-method"></a><span data-ttu-id="72e74-102">ICorProfilerInfo::GetTokenAndMetadataFromFunction 메서드</span><span class="sxs-lookup"><span data-stu-id="72e74-102">ICorProfilerInfo::GetTokenAndMetadataFromFunction Method</span></span>
<span data-ttu-id="72e74-103">메타 데이터 토큰 및 지정된 된 함수에 대 한 토큰을 기준으로 사용할 수 있는 메타 데이터 인터페이스 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="72e74-103">Gets the metadata token and a metadata interface instance that can be used against the token for the specified function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="72e74-104">구문</span><span class="sxs-lookup"><span data-stu-id="72e74-104">Syntax</span></span>  
  
```  
HRESULT GetTokenAndMetaDataFromFunction(  
    [in]  FunctionID functionId,  
    [in]  REFIID     riid,  
    [out] IUnknown   **ppImport,  
    [out] mdToken    *pToken);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="72e74-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="72e74-105">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="72e74-106">[in] 메타 데이터 토큰 및 메타 데이터 인터페이스를 가져올 함수의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="72e74-106">[in] The ID of the function for which to get the metadata token and metadata interface.</span></span>  
  
 `riid`  
 <span data-ttu-id="72e74-107">[in] 인스턴스를 가져올 메타 데이터 인터페이스의 참조 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="72e74-107">[in] The reference ID of the metadata interface to get the instance of.</span></span>  
  
 `ppImport`  
 <span data-ttu-id="72e74-108">[out] 지정된 된 함수에 대 한 토큰을 기준으로 사용할 수 있는 메타 데이터 인터페이스 인스턴스 주소에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="72e74-108">[out] A pointer to the address of the metadata interface instance that can be used against the token for the specified function.</span></span>  
  
 `pToken`  
 <span data-ttu-id="72e74-109">[out] 지정된 된 함수에 대 한 메타 데이터 토큰에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="72e74-109">[out] A pointer to the metadata token for the specified function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="72e74-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="72e74-110">Requirements</span></span>  
 <span data-ttu-id="72e74-111">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="72e74-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="72e74-112">**헤더:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="72e74-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="72e74-113">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="72e74-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="72e74-114">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="72e74-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="72e74-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="72e74-115">See also</span></span>
- [<span data-ttu-id="72e74-116">ICorProfilerInfo 인터페이스</span><span class="sxs-lookup"><span data-stu-id="72e74-116">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
