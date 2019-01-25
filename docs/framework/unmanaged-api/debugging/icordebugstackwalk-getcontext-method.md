---
title: ICorDebugStackWalk::GetContext 메서드
ms.date: 03/30/2017
api_name:
- ICorDebugStackWalk.GetContext Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStackWalk::GetContext
helpviewer_keywords:
- GetContext method, ICorDebugStackWalk interface [.NET Framework debugging]
- ICorDebugStackWalk::GetContext method [.NET Framework debugging]
ms.assetid: 081d1c95-152b-4797-8552-18453eb7b14b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 306eee3c0ce4689d1d6295aba1ef7584841dcc72
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54731051"
---
# <a name="icordebugstackwalkgetcontext-method"></a><span data-ttu-id="53904-102">ICorDebugStackWalk::GetContext 메서드</span><span class="sxs-lookup"><span data-stu-id="53904-102">ICorDebugStackWalk::GetContext Method</span></span>
<span data-ttu-id="53904-103">현재 프레임에 대 한 컨텍스트를 반환 합니다 [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="53904-103">Returns the context for the current frame in the [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="53904-104">구문</span><span class="sxs-lookup"><span data-stu-id="53904-104">Syntax</span></span>  
  
```  
HRESULT GetContext([in]  ULONG32 contextFlags,  
                   [in]  ULONG32 contextBufSize,  
                   [out] ULONG32* contextSize,  
                   [out, size_is(contextBufSize)] BYTE contextBuf[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="53904-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="53904-105">Parameters</span></span>  
 `contextFlags`  
 <span data-ttu-id="53904-106">[in] 상황에 맞는 버퍼 (WinNT.h에 정의 됨)의 요청 된 콘텐츠를 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="53904-106">[in] Flags that indicate the requested contents of the context buffer (defined in WinNT.h).</span></span>  
  
 `contextBufSize`  
 <span data-ttu-id="53904-107">[in] 상황에 맞는 버퍼의 할당 된 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="53904-107">[in] The allocated size of the context buffer.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="53904-108">[out] 컨텍스트의 실제 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="53904-108">[out] The actual size of the context.</span></span> <span data-ttu-id="53904-109">이 값은 컨텍스트 버퍼의 크기 보다 작거나 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53904-109">This value must be less than or equal to the size of the context buffer.</span></span>  
  
 `contextBuf`  
 <span data-ttu-id="53904-110">[out] 상황에 맞는 버퍼입니다.</span><span class="sxs-lookup"><span data-stu-id="53904-110">[out] The context buffer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="53904-111">반환 값</span><span class="sxs-lookup"><span data-stu-id="53904-111">Return Value</span></span>  
 <span data-ttu-id="53904-112">이 메서드는 다음과 같은 특정 HRESULT뿐만 아니라 메서드 오류를 나타내는 HRESULT 오류도 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="53904-112">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="53904-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="53904-113">HRESULT</span></span>|<span data-ttu-id="53904-114">설명</span><span class="sxs-lookup"><span data-stu-id="53904-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="53904-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="53904-115">S_OK</span></span>|<span data-ttu-id="53904-116">현재 프레임에 대 한 컨텍스트가 반환 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="53904-116">The context for the current frame was successfully returned.</span></span>|  
|<span data-ttu-id="53904-117">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="53904-117">E_FAIL</span></span>|<span data-ttu-id="53904-118">컨텍스트를 반환 하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="53904-118">The context could not be returned.</span></span>|  
|<span data-ttu-id="53904-119">HRESULT_FROM_WIN32(ERROR_INSUFFICIENT BUFFER)</span><span class="sxs-lookup"><span data-stu-id="53904-119">HRESULT_FROM_WIN32(ERROR_INSUFFICIENT BUFFER)</span></span>|<span data-ttu-id="53904-120">상황에 맞는 버퍼가 너무 작습니다.</span><span class="sxs-lookup"><span data-stu-id="53904-120">The context buffer is too small.</span></span>|  
|<span data-ttu-id="53904-121">CORDBG_E_PAST_END_OF_STACK</span><span class="sxs-lookup"><span data-stu-id="53904-121">CORDBG_E_PAST_END_OF_STACK</span></span>|<span data-ttu-id="53904-122">프레임 포인터 끝 스택;에 이미 따라서 추가 프레임 없음 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53904-122">The frame pointer is already at the end of the stack; therefore, no additional frames can be accessed.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="53904-123">예외</span><span class="sxs-lookup"><span data-stu-id="53904-123">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="53904-124">설명</span><span class="sxs-lookup"><span data-stu-id="53904-124">Remarks</span></span>  
 <span data-ttu-id="53904-125">비휘발성 레지스터와 같은 레지스터의 하위 집합만 복원 해제 때문에 컨텍스트 호출 시 레지스터 상태를 정확 하 게 일치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53904-125">Because unwinding restores only a subset of the registers, such as non-volatile registers, the context may not exactly match the register state at the time of the call.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="53904-126">요구 사항</span><span class="sxs-lookup"><span data-stu-id="53904-126">Requirements</span></span>  
 <span data-ttu-id="53904-127">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="53904-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="53904-128">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="53904-128">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="53904-129">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="53904-129">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="53904-130">**.NET Framework 버전:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="53904-130">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="53904-131">참고자료</span><span class="sxs-lookup"><span data-stu-id="53904-131">See also</span></span>
- [<span data-ttu-id="53904-132">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="53904-132">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="53904-133">디버깅</span><span class="sxs-lookup"><span data-stu-id="53904-133">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
