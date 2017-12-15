---
title: "ICorProfilerInfo::GetThreadInfo 메서드"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo.GetThreadInfo
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo::GetThreadInfo
helpviewer_keywords:
- ICorProfilerInfo::GetThreadInfo method [.NET Framework profiling]
- GetThreadInfo method [.NET Framework profiling]
ms.assetid: fc994fef-65c9-432a-84cb-66c8141147e7
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 4c4657279e145dbb923c339ed0114723620e7aa7
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/18/2017
---
# <a name="icorprofilerinfogetthreadinfo-method"></a><span data-ttu-id="3dcf0-102">ICorProfilerInfo::GetThreadInfo 메서드</span><span class="sxs-lookup"><span data-stu-id="3dcf0-102">ICorProfilerInfo::GetThreadInfo Method</span></span>
<span data-ttu-id="3dcf0-103">지정 된 스레드에 대 한 현재 Win32 스레드 id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3dcf0-103">Gets the current Win32 thread identity for the specified thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3dcf0-104">구문</span><span class="sxs-lookup"><span data-stu-id="3dcf0-104">Syntax</span></span>  
  
```  
HRESULT GetThreadInfo(  
    [in]  ThreadID threadId,  
    [out] DWORD    *pdwWin32ThreadId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3dcf0-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3dcf0-105">Parameters</span></span>  
 `threadId`  
 <span data-ttu-id="3dcf0-106">[in] id입니다. 현재 Win32 가져올 스레드의 ID</span><span class="sxs-lookup"><span data-stu-id="3dcf0-106">[in] The ID of the thread for which to get the current Win32 ID.</span></span>  
  
 `pdwWin32ThreadId`  
 <span data-ttu-id="3dcf0-107">[out] 지정한 스레드의 현재 Win32 스레드에 대 한 포인터의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="3dcf0-107">[out] A pointer to the specified thread's current Win32 thread ID.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3dcf0-108">요구 사항</span><span class="sxs-lookup"><span data-stu-id="3dcf0-108">Requirements</span></span>  
 <span data-ttu-id="3dcf0-109">**플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="3dcf0-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3dcf0-110">**헤더:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="3dcf0-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="3dcf0-111">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3dcf0-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3dcf0-112">**.NET framework 버전:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3dcf0-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3dcf0-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3dcf0-113">See Also</span></span>  
 [<span data-ttu-id="3dcf0-114">ICorProfilerInfo 인터페이스</span><span class="sxs-lookup"><span data-stu-id="3dcf0-114">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)