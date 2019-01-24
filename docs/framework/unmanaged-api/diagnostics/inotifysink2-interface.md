---
title: INotifySink2 인터페이스
ms.date: 03/30/2017
api_name:
- INotifySink2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- INotifySink2
helpviewer_keywords:
- INotifySink2 interface [.NET Framework debugging]
ms.assetid: c1018789-4206-455d-aacc-2d876fc0d0bb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fc5d09ac12919b8c68b9fe4bf9f7dc0009b2d4b0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54705471"
---
# <a name="inotifysink2-interface"></a><span data-ttu-id="4214e-102">INotifySink2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="4214e-102">INotifySink2 Interface</span></span>
<span data-ttu-id="4214e-103">싱크 알림 위한 메서드를 선언합니다.</span><span class="sxs-lookup"><span data-stu-id="4214e-103">Declares methods for sink notification.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4214e-104">메서드</span><span class="sxs-lookup"><span data-stu-id="4214e-104">Methods</span></span>  
  
|<span data-ttu-id="4214e-105">메서드</span><span class="sxs-lookup"><span data-stu-id="4214e-105">Method</span></span>|<span data-ttu-id="4214e-106">설명</span><span class="sxs-lookup"><span data-stu-id="4214e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4214e-107">OnSyncCallEnter 메서드</span><span class="sxs-lookup"><span data-stu-id="4214e-107">OnSyncCallEnter Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallenter-method.md)|<span data-ttu-id="4214e-108">호출을 시작 하면 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4214e-108">Gets invoked when entering a call.</span></span>|  
|[<span data-ttu-id="4214e-109">OnSyncCallExit 메서드</span><span class="sxs-lookup"><span data-stu-id="4214e-109">OnSyncCallExit Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallexit-method.md)|<span data-ttu-id="4214e-110">호출을 종료할 때 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4214e-110">Gets invoked when exiting a call.</span></span>|  
|[<span data-ttu-id="4214e-111">OnSyncCallOut 메서드</span><span class="sxs-lookup"><span data-stu-id="4214e-111">OnSyncCallOut Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallout-method.md)|<span data-ttu-id="4214e-112">이 호출 하는 경우 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4214e-112">Gets invoked when a call is out.</span></span>|  
|[<span data-ttu-id="4214e-113">OnSyncCallReturn 메서드</span><span class="sxs-lookup"><span data-stu-id="4214e-113">OnSyncCallReturn Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallreturn-method.md)|<span data-ttu-id="4214e-114">호출 반환 될 때 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4214e-114">Gets invoked when a call returns.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="4214e-115">요구 사항</span><span class="sxs-lookup"><span data-stu-id="4214e-115">Requirements</span></span>  
 <span data-ttu-id="4214e-116">**헤더:** ProtocolNotify2.idl</span><span class="sxs-lookup"><span data-stu-id="4214e-116">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4214e-117">참고자료</span><span class="sxs-lookup"><span data-stu-id="4214e-117">See also</span></span>
- [<span data-ttu-id="4214e-118">INotifyConnection2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="4214e-118">INotifyConnection2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifyconnection2-interface.md)
- [<span data-ttu-id="4214e-119">INotifySource2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="4214e-119">INotifySource2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-interface.md)
- [<span data-ttu-id="4214e-120">진단 기호 저장소 인터페이스</span><span class="sxs-lookup"><span data-stu-id="4214e-120">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
