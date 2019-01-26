---
title: ICLRDataTarget3 인터페이스
ms.date: 03/30/2017
api_name:
- ICLRDataTarget3
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: d2711bdf-64b3-404c-a0c3-01ba4907f703
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 74e106e17c0f0e5702927c4599fb143fb3554ce3
ms.sourcegitcommit: d9a0071d0fd490ae006c816f78a563b9946e269a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55065949"
---
# <a name="iclrdatatarget3-interface"></a><span data-ttu-id="6cae7-102">ICLRDataTarget3 인터페이스</span><span class="sxs-lookup"><span data-stu-id="6cae7-102">ICLRDataTarget3 Interface</span></span>
<span data-ttu-id="6cae7-103">서브 클래스 [ICLRDataTarget2](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md) 예외 정보에 대 한 액세스를 제공 하는 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cae7-103">A subclass of [ICLRDataTarget2](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md) that provides access to exception information.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="6cae7-104">메서드</span><span class="sxs-lookup"><span data-stu-id="6cae7-104">Methods</span></span>  
  
|<span data-ttu-id="6cae7-105">메서드</span><span class="sxs-lookup"><span data-stu-id="6cae7-105">Method</span></span>|<span data-ttu-id="6cae7-106">설명</span><span class="sxs-lookup"><span data-stu-id="6cae7-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="6cae7-107">GetExceptionRecord 메서드</span><span class="sxs-lookup"><span data-stu-id="6cae7-107">GetExceptionRecord Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-getexceptionrecord-method.md)|<span data-ttu-id="6cae7-108">공용 언어 런타임(CLR)에 의해 호출되는 데이터 액세스는 대상 프로세스와 연관된 예외 레코드 검색을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6cae7-108">Called by the common language runtime (CLR) data access services to retrieve the exception record associated with the target process.</span></span>|  
|[<span data-ttu-id="6cae7-109">GetExceptionContextRecord 메서드</span><span class="sxs-lookup"><span data-stu-id="6cae7-109">GetExceptionContextRecord Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-getexceptioncontextrecord-method.md)|<span data-ttu-id="6cae7-110">CLR에 의해 호출되는 데이터 액세스는 대상 프로세스와 연관된 컨텍스트 레코드 검색을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6cae7-110">Called by the CLR data access services to retrieve the context record associated with the target process.</span></span>|  
|[<span data-ttu-id="6cae7-111">GetExceptionThreadID 메서드</span><span class="sxs-lookup"><span data-stu-id="6cae7-111">GetExceptionThreadID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-getexceptionthreadid-method.md)|<span data-ttu-id="6cae7-112">CLR 데이터 액세스 서비스에 의해 호출되어 예외를 throw한 스레드의 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6cae7-112">Called by the CLR data access services to get the ID of the thread that threw the exception.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6cae7-113">설명</span><span class="sxs-lookup"><span data-stu-id="6cae7-113">Remarks</span></span>  
 <span data-ttu-id="6cae7-114">API 클라이언트(즉, 디버거)에서는 이 인터페이스를 특정 대상 프로세스에 적절하게 구현해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cae7-114">The API client (that is, the debugger) must implement this interface as appropriate for the particular target process.</span></span> <span data-ttu-id="6cae7-115">예를 들어 활성 프로세스의 구현은 메모리 덤프의 구현과는 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="6cae7-115">For example, a live process would have an implementation different from that of a memory dump.</span></span> <span data-ttu-id="6cae7-116">대상에서 메모리 영역의 수정을 지원하지 않을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6cae7-116">The target may not support modification of its memory regions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6cae7-117">요구 사항</span><span class="sxs-lookup"><span data-stu-id="6cae7-117">Requirements</span></span>  
 <span data-ttu-id="6cae7-118">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="6cae7-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6cae7-119">**헤더:** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="6cae7-119">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="6cae7-120">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6cae7-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6cae7-121">**.NET Framework 버전:** [!INCLUDE[v451_update](../../../../includes/net-current-v451-nov-plus.md)]</span><span class="sxs-lookup"><span data-stu-id="6cae7-121">**.NET Framework Versions:** [!INCLUDE[v451_update](../../../../includes/net-current-v451-nov-plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6cae7-122">참고자료</span><span class="sxs-lookup"><span data-stu-id="6cae7-122">See also</span></span>
- [<span data-ttu-id="6cae7-123">ICLRDataTarget 인터페이스</span><span class="sxs-lookup"><span data-stu-id="6cae7-123">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
- [<span data-ttu-id="6cae7-124">ICLRDataTarget2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="6cae7-124">ICLRDataTarget2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md)
- [<span data-ttu-id="6cae7-125">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="6cae7-125">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
