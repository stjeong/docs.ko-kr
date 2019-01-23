---
title: ICLRIoCompletionManager 인터페이스
ms.date: 03/30/2017
api_name:
- ICLRIoCompletionManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRIoCompletionManager
helpviewer_keywords:
- ICLRIoCompletionManager interface [.NET Framework hosting]
ms.assetid: c6c3ace6-e5e7-4450-8cc5-a9a48208c493
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b71c177c7c0cb029fb7cfa734f54c87abf20b348
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54557840"
---
# <a name="iclriocompletionmanager-interface"></a><span data-ttu-id="a5240-102">ICLRIoCompletionManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="a5240-102">ICLRIoCompletionManager Interface</span></span>
<span data-ttu-id="a5240-103">지정 된 I/O의 상태는 CLR (공용 언어 런타임)에 알리기 위해 호스트를 허용 하는 콜백 메서드 요청를 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5240-103">Implements a callback method that allows the host to notify the common language runtime (CLR) of the status of specified I/O requests.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a5240-104">메서드</span><span class="sxs-lookup"><span data-stu-id="a5240-104">Methods</span></span>  
  
|<span data-ttu-id="a5240-105">메서드</span><span class="sxs-lookup"><span data-stu-id="a5240-105">Method</span></span>|<span data-ttu-id="a5240-106">설명</span><span class="sxs-lookup"><span data-stu-id="a5240-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a5240-107">OnComplete 메서드</span><span class="sxs-lookup"><span data-stu-id="a5240-107">OnComplete Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-oncomplete-method.md)|<span data-ttu-id="a5240-108">CLR에 대 한 호출을 사용 하 여 수행 된 I/O 요청의 상태를에 알립니다 합니다 [ihostiocompletionmanager:: Bind](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-bind-method.md) 메서드.</span><span class="sxs-lookup"><span data-stu-id="a5240-108">Notifies the CLR of the status of an I/O request that was made by using a call to the [IHostIoCompletionManager::Bind](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-bind-method.md) method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a5240-109">설명</span><span class="sxs-lookup"><span data-stu-id="a5240-109">Remarks</span></span>  
 <span data-ttu-id="a5240-110">호스트를 사용 하 여 I/O 완료 추상화를 구현 합니다 [IHostIoCompletionManager](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md) 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="a5240-110">The host implements the I/O completion abstraction by using the [IHostIoCompletionManager](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md) interface.</span></span> <span data-ttu-id="a5240-111">CLR이이 인터페이스를 통해 I/O 요청은 및 호스트를 사용 하 여 이러한 요청의 결과 런타임에 알립니다는 `ICLRIoCompletionManager` 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="a5240-111">The CLR makes I/O requests through this interface, and the host notifies the runtime of the outcome of such requests by using the `ICLRIoCompletionManager` interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a5240-112">요구 사항</span><span class="sxs-lookup"><span data-stu-id="a5240-112">Requirements</span></span>  
 <span data-ttu-id="a5240-113">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="a5240-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a5240-114">**헤더:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a5240-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a5240-115">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="a5240-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a5240-116">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a5240-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a5240-117">참고자료</span><span class="sxs-lookup"><span data-stu-id="a5240-117">See also</span></span>
- [<span data-ttu-id="a5240-118">IHostIoCompletionManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="a5240-118">IHostIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md)
- [<span data-ttu-id="a5240-119">IHostThreadPoolManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="a5240-119">IHostThreadPoolManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-interface.md)
- [<span data-ttu-id="a5240-120">호스팅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="a5240-120">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
