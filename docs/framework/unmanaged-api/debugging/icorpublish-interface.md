---
title: ICorPublish 인터페이스
ms.date: 03/30/2017
api_name:
- ICorPublish
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublish
helpviewer_keywords:
- ICorPublish interface [.NET Framework debugging]
ms.assetid: 87c4fcb2-7703-4a2e-afb6-42973381b960
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e1dea8cc54c68db333c409e3bd7b3e4211bd52ac
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54713969"
---
# <a name="icorpublish-interface"></a><span data-ttu-id="def30-102">ICorPublish 인터페이스</span><span class="sxs-lookup"><span data-stu-id="def30-102">ICorPublish Interface</span></span>
<span data-ttu-id="def30-103">해당 프로세스의 프로세스에 대 한 정보 및 응용 프로그램 도메인에 대 한 정보를 게시 하는 것에 대 한 일반적인 인터페이스로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="def30-103">Serves as the general interface for publishing information about processes and information about the application domains in those processes.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="def30-104">메서드</span><span class="sxs-lookup"><span data-stu-id="def30-104">Methods</span></span>  
  
|<span data-ttu-id="def30-105">메서드</span><span class="sxs-lookup"><span data-stu-id="def30-105">Method</span></span>|<span data-ttu-id="def30-106">설명</span><span class="sxs-lookup"><span data-stu-id="def30-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="def30-107">EnumProcesses 메서드</span><span class="sxs-lookup"><span data-stu-id="def30-107">EnumProcesses Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublish-enumprocesses-method.md)|<span data-ttu-id="def30-108">가져옵니다는 [ICorPublishProcessEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocessenum-interface.md) 이 컴퓨터에서 실행 되는 관리 되는 프로세스를 포함 하는 인스턴스.</span><span class="sxs-lookup"><span data-stu-id="def30-108">Gets an [ICorPublishProcessEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocessenum-interface.md) instance that contains the managed processes running on this computer.</span></span>|  
|[<span data-ttu-id="def30-109">GetProcess 메서드</span><span class="sxs-lookup"><span data-stu-id="def30-109">GetProcess Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublish-getprocess-method.md)|<span data-ttu-id="def30-110">가져옵니다는 [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) 지정된 된 식별자를 사용 하 여 프로세스를 나타내는 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="def30-110">Gets an [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) instance that represents the process with the specified identifier.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="def30-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="def30-111">Requirements</span></span>  
 <span data-ttu-id="def30-112">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="def30-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="def30-113">**헤더:** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="def30-113">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="def30-114">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="def30-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="def30-115">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="def30-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="def30-116">참고자료</span><span class="sxs-lookup"><span data-stu-id="def30-116">See also</span></span>
- [<span data-ttu-id="def30-117">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="def30-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="def30-118">CorpubPublish Coclass</span><span class="sxs-lookup"><span data-stu-id="def30-118">CorpubPublish Coclass</span></span>](../../../../docs/framework/unmanaged-api/debugging/corpubpublish-coclass.md)
