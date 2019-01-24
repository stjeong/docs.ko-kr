---
title: ICorProfilerCallback::RemotingServerInvocationReturned 메서드
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingServerInvocationReturned
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingServerInvocationReturned
helpviewer_keywords:
- ICorProfilerCallback::RemotingServerInvocationReturned method [.NET Framework profiling]
- RemotingServerInvocationReturned method [.NET Framework profiling]
ms.assetid: a4de6805-e159-4280-99e5-3390c86166d0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3a64941c35630e76e05ac982725c9eb3f5583d12
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54495996"
---
# <a name="icorprofilercallbackremotingserverinvocationreturned-method"></a><span data-ttu-id="9b781-102">ICorProfilerCallback::RemotingServerInvocationReturned 메서드</span><span class="sxs-lookup"><span data-stu-id="9b781-102">ICorProfilerCallback::RemotingServerInvocationReturned Method</span></span>
<span data-ttu-id="9b781-103">프로세스에서 원격 메서드 호출 요청에 대 한 응답에서 메서드를 호출 되었음을 프로파일러에 알립니다.</span><span class="sxs-lookup"><span data-stu-id="9b781-103">Notifies the profiler that the process has finished invoking a method in response to a remote method invocation request.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9b781-104">구문</span><span class="sxs-lookup"><span data-stu-id="9b781-104">Syntax</span></span>  
  
```  
HRESULT RemotingServerInvocationReturned();  
```  
  
## <a name="requirements"></a><span data-ttu-id="9b781-105">요구 사항</span><span class="sxs-lookup"><span data-stu-id="9b781-105">Requirements</span></span>  
 <span data-ttu-id="9b781-106">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="9b781-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9b781-107">**헤더:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="9b781-107">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="9b781-108">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9b781-108">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9b781-109">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9b781-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9b781-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="9b781-110">See also</span></span>
- [<span data-ttu-id="9b781-111">ICorProfilerCallback 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9b781-111">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
