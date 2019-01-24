---
title: ICLRDataTarget 인터페이스
ms.date: 03/30/2017
api_name:
- ICLRDataTarget
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget
helpviewer_keywords:
- ICLRDataTarget interface [.NET Framework debugging]
ms.assetid: e2f05155-9bef-4e11-b703-7f05890665ca
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 11eb49347caacbfa92493e9ac20f1c8cb5c706e6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54745027"
---
# <a name="iclrdatatarget-interface"></a><span data-ttu-id="528b1-102">ICLRDataTarget 인터페이스</span><span class="sxs-lookup"><span data-stu-id="528b1-102">ICLRDataTarget Interface</span></span>
<span data-ttu-id="528b1-103">CLR (공용 언어 런타임)의 대상 항목과 상호 작용 하기 위한 메서드를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="528b1-103">Provides methods for interaction with a target item of the common language runtime (CLR).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="528b1-104">메서드</span><span class="sxs-lookup"><span data-stu-id="528b1-104">Methods</span></span>  
  
|<span data-ttu-id="528b1-105">메서드</span><span class="sxs-lookup"><span data-stu-id="528b1-105">Method</span></span>|<span data-ttu-id="528b1-106">설명</span><span class="sxs-lookup"><span data-stu-id="528b1-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="528b1-107">GetCurrentThreadID 메서드</span><span class="sxs-lookup"><span data-stu-id="528b1-107">GetCurrentThreadID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-getcurrentthreadid-method.md)|<span data-ttu-id="528b1-108">현재 스레드에 대 한 운영 체제 식별자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="528b1-108">Gets the operating system identifier for the current thread.</span></span>|  
|[<span data-ttu-id="528b1-109">GetImageBase 메서드</span><span class="sxs-lookup"><span data-stu-id="528b1-109">GetImageBase Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-getimagebase-method.md)|<span data-ttu-id="528b1-110">지정된 된 이미지에 대 한 기본 메모리 주소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="528b1-110">Gets the base memory address for the specified image.</span></span>|  
|[<span data-ttu-id="528b1-111">GetMachineType 메서드</span><span class="sxs-lookup"><span data-stu-id="528b1-111">GetMachineType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-getmachinetype-method.md)|<span data-ttu-id="528b1-112">대상 프로세스에서 사용 되는 명령 집합의 종류에 대 한 식별자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="528b1-112">Gets an identifier for the kind of instruction set that the target process is using.</span></span>|  
|[<span data-ttu-id="528b1-113">GetPointerSize 메서드</span><span class="sxs-lookup"><span data-stu-id="528b1-113">GetPointerSize Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-getpointersize-method.md)|<span data-ttu-id="528b1-114">현재 대상에 대 한 포인터를 바이트 단위로 크기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="528b1-114">Gets the size, in bytes, of a pointer to the current target.</span></span>|  
|[<span data-ttu-id="528b1-115">GetThreadContext 메서드</span><span class="sxs-lookup"><span data-stu-id="528b1-115">GetThreadContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-getthreadcontext-method.md)|<span data-ttu-id="528b1-116">지정된 된 식별자를 사용 하 여 스레드의 컨텍스트에 대 한 포인터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="528b1-116">Gets a pointer to the context of the thread with the specified identifier.</span></span>|  
|[<span data-ttu-id="528b1-117">GetTLSValue 메서드</span><span class="sxs-lookup"><span data-stu-id="528b1-117">GetTLSValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-gettlsvalue-method.md)|<span data-ttu-id="528b1-118">스레드 로컬 저장소 (TLS)에 지정 된 스레드에 대 한 지정 된 인덱스 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="528b1-118">Gets a value in thread local storage (TLS) at the specified index for the specified thread.</span></span>|  
|[<span data-ttu-id="528b1-119">ReadVirtual 메서드</span><span class="sxs-lookup"><span data-stu-id="528b1-119">ReadVirtual Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-readvirtual-method.md)|<span data-ttu-id="528b1-120">지정된 된 버퍼에 지정 된 가상 메모리 주소에서 데이터를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="528b1-120">Reads data from the specified virtual memory address into the specified buffer.</span></span>|  
|[<span data-ttu-id="528b1-121">Request 메서드</span><span class="sxs-lookup"><span data-stu-id="528b1-121">Request Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-request-method.md)|<span data-ttu-id="528b1-122">구현에 의해 정의 된 대로 작업을 요청 하는 공용 언어 런타임 (CLR) 데이터 액세스 서비스에서 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="528b1-122">Called by the common language runtime (CLR) data access services to request an operation, as defined by the implementation.</span></span>|  
|[<span data-ttu-id="528b1-123">SetThreadContext 메서드</span><span class="sxs-lookup"><span data-stu-id="528b1-123">SetThreadContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-setthreadcontext-method.md)|<span data-ttu-id="528b1-124">대상 프로세스에서 지정 된 스레드의 현재 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="528b1-124">Sets the current context of the specified thread in the target process.</span></span>|  
|[<span data-ttu-id="528b1-125">SetTLSValue 메서드</span><span class="sxs-lookup"><span data-stu-id="528b1-125">SetTLSValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-settlsvalue-method.md)|<span data-ttu-id="528b1-126">대상 프로세스에서 지정 된 스레드의 스레드 로컬 저장소 (TLS)에서 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="528b1-126">Sets a value in the thread local storage (TLS) of the specified thread in the target process.</span></span>|  
|[<span data-ttu-id="528b1-127">WriteVirtual 메서드</span><span class="sxs-lookup"><span data-stu-id="528b1-127">WriteVirtual Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-writevirtual-method.md)|<span data-ttu-id="528b1-128">지정 된 가상 메모리 주소를 지정된 된 버퍼에서 데이터를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="528b1-128">Writes data from the specified buffer to the specified virtual memory address.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="528b1-129">설명</span><span class="sxs-lookup"><span data-stu-id="528b1-129">Remarks</span></span>  
 <span data-ttu-id="528b1-130">API 클라이언트 (즉, 디버거)는 특정 대상 항목에 대 한 적절 하 게이 인터페이스를 구현 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="528b1-130">The API client (that is, the debugger) must implement this interface as appropriate for the particular target item.</span></span> <span data-ttu-id="528b1-131">예를 들어 활성 프로세스의 구현은 메모리 덤프의 구현과는 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="528b1-131">For example, a live process would have an implementation different from that of a memory dump.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="528b1-132">요구 사항</span><span class="sxs-lookup"><span data-stu-id="528b1-132">Requirements</span></span>  
 <span data-ttu-id="528b1-133">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="528b1-133">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="528b1-134">**헤더:** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="528b1-134">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="528b1-135">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="528b1-135">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="528b1-136">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="528b1-136">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="528b1-137">참고자료</span><span class="sxs-lookup"><span data-stu-id="528b1-137">See also</span></span>
- [<span data-ttu-id="528b1-138">ICLRDataTarget2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="528b1-138">ICLRDataTarget2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md)
- [<span data-ttu-id="528b1-139">디버깅 인터페이스</span><span class="sxs-lookup"><span data-stu-id="528b1-139">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
