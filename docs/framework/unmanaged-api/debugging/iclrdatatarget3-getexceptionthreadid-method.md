---
title: ICLRDataTarget3::GetExceptionThreadID 메서드
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICLRDataTarget3.GetExceptionThreadID
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 307d6ac7-4a86-45f3-999d-6b47004a68f2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d59bd3b8c427996fe5e44e95aeff51deb1da984a
ms.sourcegitcommit: d9a0071d0fd490ae006c816f78a563b9946e269a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55066378"
---
# <a name="iclrdatatarget3getexceptionthreadid-method"></a><span data-ttu-id="a2b37-102">ICLRDataTarget3::GetExceptionThreadID 메서드</span><span class="sxs-lookup"><span data-stu-id="a2b37-102">ICLRDataTarget3::GetExceptionThreadID Method</span></span>
<span data-ttu-id="a2b37-103">CLR(공용 언어 런타임) 데이터 액세스 서비스에 의해 호출되어 예외를 throw한 스레드의 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a2b37-103">Called by the common language runtime (CLR) data access services to get the ID of the thread that threw the exception.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a2b37-104">구문</span><span class="sxs-lookup"><span data-stu-id="a2b37-104">Syntax</span></span>  
  
```cpp  
HRESULT GetExceptionThreadID(  
    [out] ULONG32* threadID  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a2b37-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a2b37-105">Parameters</span></span>  
 `threadID`  
 <span data-ttu-id="a2b37-106">[out] 예외를 throw한 스레드의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a2b37-106">[out] The ID of the thread that threw the exception.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a2b37-107">반환 값</span><span class="sxs-lookup"><span data-stu-id="a2b37-107">Return Value</span></span>  
 <span data-ttu-id="a2b37-108">반환 값은 성공 시 `S_OK`이고 실패 시에는 오류 `HRESULT` 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="a2b37-108">The return value is `S_OK` on success, or a failure `HRESULT` code on failure.</span></span> <span data-ttu-id="a2b37-109">`HRESULT` 코드는 다음을 비롯한 여러 항목을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2b37-109">The `HRESULT` codes can include but are not limited to the following:</span></span>  
  
|<span data-ttu-id="a2b37-110">반환 코드</span><span class="sxs-lookup"><span data-stu-id="a2b37-110">Return code</span></span>|<span data-ttu-id="a2b37-111">설명</span><span class="sxs-lookup"><span data-stu-id="a2b37-111">Description</span></span>|  
|-----------------|-----------------|  
|`S_OK`|<span data-ttu-id="a2b37-112">메서드가 정상적으로 실행되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a2b37-112">Method succeeded.</span></span>|  
|`HRESULT_FROM_WIN32(ERROR_NOT_FOUND)`|<span data-ttu-id="a2b37-113">예외의 유효한 스레드 ID를 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a2b37-113">Could not find a valid thread ID for the exception.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a2b37-114">설명</span><span class="sxs-lookup"><span data-stu-id="a2b37-114">Remarks</span></span>  
 <span data-ttu-id="a2b37-115">이 메서드는 디버깅 응용 프로그램의 작성자가 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="a2b37-115">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a2b37-116">요구 사항</span><span class="sxs-lookup"><span data-stu-id="a2b37-116">Requirements</span></span>  
 <span data-ttu-id="a2b37-117">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="a2b37-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a2b37-118">**헤더:** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="a2b37-118">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="a2b37-119">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a2b37-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a2b37-120">**.NET Framework 버전:** [!INCLUDE[v451_update](../../../../includes/net-current-v451-nov-plus.md)]</span><span class="sxs-lookup"><span data-stu-id="a2b37-120">**.NET Framework Versions:** [!INCLUDE[v451_update](../../../../includes/net-current-v451-nov-plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a2b37-121">참고자료</span><span class="sxs-lookup"><span data-stu-id="a2b37-121">See also</span></span>
- [<span data-ttu-id="a2b37-122">ICLRDataTarget3 인터페이스</span><span class="sxs-lookup"><span data-stu-id="a2b37-122">ICLRDataTarget3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-interface.md)
- [<span data-ttu-id="a2b37-123">GetExceptionContextRecord 메서드</span><span class="sxs-lookup"><span data-stu-id="a2b37-123">GetExceptionContextRecord Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-getexceptioncontextrecord-method.md)
- [<span data-ttu-id="a2b37-124">GetExceptionRecord 메서드</span><span class="sxs-lookup"><span data-stu-id="a2b37-124">GetExceptionRecord Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-getexceptionrecord-method.md)
