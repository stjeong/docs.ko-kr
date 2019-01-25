---
title: ICorPublishAppDomainEnum 인터페이스
ms.date: 03/30/2017
api_name:
- ICorPublishAppDomainEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishAppDomainEnum
helpviewer_keywords:
- ICorPublishAppDomainEnum interface [.NET Framework debugging]
ms.assetid: bb798c56-042e-475d-a245-b6fac36d0c07
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e2be3406cd4330fb477e8a1c89945be1e9f777bb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54706607"
---
# <a name="icorpublishappdomainenum-interface"></a><span data-ttu-id="2681a-102">ICorPublishAppDomainEnum 인터페이스</span><span class="sxs-lookup"><span data-stu-id="2681a-102">ICorPublishAppDomainEnum Interface</span></span>
<span data-ttu-id="2681a-103">서브 클래스는 [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md) 의 컬렉션을 이동 하는 메서드를 제공 하는 인터페이스 [ICorPublishAppDomain](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md) 프로세스 내에서 현재 존재 하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2681a-103">A subclass of the [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md) interface that provides methods to traverse a collection of [ICorPublishAppDomain](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md) objects that currently exist within a process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="2681a-104">메서드</span><span class="sxs-lookup"><span data-stu-id="2681a-104">Methods</span></span>  
  
|<span data-ttu-id="2681a-105">메서드</span><span class="sxs-lookup"><span data-stu-id="2681a-105">Method</span></span>|<span data-ttu-id="2681a-106">설명</span><span class="sxs-lookup"><span data-stu-id="2681a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="2681a-107">Next 메서드</span><span class="sxs-lookup"><span data-stu-id="2681a-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomainenum-next-method.md)|<span data-ttu-id="2681a-108">지정 된 수를 가져옵니다 `ICorPublishAppDomain` 현재 위치부터 컬렉션의 인스턴스.</span><span class="sxs-lookup"><span data-stu-id="2681a-108">Gets the specified number of `ICorPublishAppDomain` instances from the collection, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2681a-109">설명</span><span class="sxs-lookup"><span data-stu-id="2681a-109">Remarks</span></span>  
 <span data-ttu-id="2681a-110">합니다 `ICorPublishAppDomainEnum` 추상 인터페이스의 메서드를 구현 하는 인터페이스 [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="2681a-110">The `ICorPublishAppDomainEnum` interface implements the methods of the abstract interface, [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2681a-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="2681a-111">Requirements</span></span>  
 <span data-ttu-id="2681a-112">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="2681a-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2681a-113">**헤더:** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="2681a-113">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="2681a-114">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2681a-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2681a-115">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2681a-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2681a-116">참고자료</span><span class="sxs-lookup"><span data-stu-id="2681a-116">See also</span></span>
- [<span data-ttu-id="2681a-117">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="2681a-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="2681a-118">CorpubPublish Coclass</span><span class="sxs-lookup"><span data-stu-id="2681a-118">CorpubPublish Coclass</span></span>](../../../../docs/framework/unmanaged-api/debugging/corpubpublish-coclass.md)
