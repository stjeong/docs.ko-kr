---
title: _CorDllMain 함수
ms.date: 03/30/2017
api_name:
- _CorDllMain
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- _CorDllMain
helpviewer_keywords:
- _CorDllMain function [.NET Framework hosting]
ms.assetid: bc7b51cf-39d3-48ec-a5cb-2f179fbefff8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f62ad2c9ec6e1c9672ac5c78e838e926b02359f4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54512374"
---
# <a name="cordllmain-function"></a><span data-ttu-id="e5089-102">_CorDllMain 함수</span><span class="sxs-lookup"><span data-stu-id="e5089-102">_CorDllMain Function</span></span>
<span data-ttu-id="e5089-103">CLR (공용 언어 런타임)을 초기화 하 고 DLL 어셈블리의 CLR 헤더에서 관리 되는 진입점을 찾습니다 실행을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5089-103">Initializes the common language runtime (CLR), locates the managed entry point in the DLL assembly's CLR header, and begins execution.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e5089-104">구문</span><span class="sxs-lookup"><span data-stu-id="e5089-104">Syntax</span></span>  
  
```  
BOOL STDMETHODCALLTYPE _CorDllMain (  
   [in] HINSTANCE hInst,  
   [in] DWORD     dwReason,  
   [in] LPVOID    lpReserved  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e5089-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e5089-105">Parameters</span></span>  
 `hInst`  
 <span data-ttu-id="e5089-106">[in] 로드 된 모듈의 인스턴스 핸들입니다.</span><span class="sxs-lookup"><span data-stu-id="e5089-106">[in] The instance handle of the loaded module.</span></span>  
  
 `dwReason`  
 <span data-ttu-id="e5089-107">[in] DLL 진입점 함수가 호출 되는 이유를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e5089-107">[in]Indicates why the DLL entry-point function is being called.</span></span> <span data-ttu-id="e5089-108">이 매개 변수는 다음 값 중 하나일 수 있습니다. DLL_PROCESS_ATTACH, 활발, 활발, 또는 DLL_PROCESS_DETACH를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5089-108">This parameter can be one of the following values: DLL_PROCESS_ATTACH, DLL_THREAD_ATTACH, DLL_THREAD_ATTACH, or DLL_PROCESS_DETACH.</span></span> <span data-ttu-id="e5089-109">이러한 값의 설명을 보려면는 `DllMain` Platform SDK에 대 한 설명서입니다.</span><span class="sxs-lookup"><span data-stu-id="e5089-109">For descriptions of these values, see the `DllMain` documentation in the Platform SDK.</span></span>  
  
 `lpReserved`  
 <span data-ttu-id="e5089-110">[in] 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5089-110">[in] Unused.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e5089-111">반환 값</span><span class="sxs-lookup"><span data-stu-id="e5089-111">Return Value</span></span>  
 <span data-ttu-id="e5089-112">이 메서드는 반환 `true` 성공을 위한 및 `false` 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5089-112">This method returns `true` for success and `false` if an error occurs.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e5089-113">설명</span><span class="sxs-lookup"><span data-stu-id="e5089-113">Remarks</span></span>  
 <span data-ttu-id="e5089-114">이 함수는 DLL 어셈블리에 대 한 운영 체제 로더에 의해 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5089-114">This function is called by the operating system loader for DLL assemblies.</span></span> <span data-ttu-id="e5089-115">실행 가능 어셈블리 로더 호출을 [_CorExeMain](../../../../docs/framework/unmanaged-api/hosting/corexemain-function.md) 함수를 대신 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5089-115">For executable assemblies, the loader calls the [_CorExeMain](../../../../docs/framework/unmanaged-api/hosting/corexemain-function.md) function instead.</span></span>  
  
 <span data-ttu-id="e5089-116">운영 체제 로더는 DLL 파일에 지정 된 진입점에 관계 없이이 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5089-116">The operating system loader calls this method regardless of the entry point specified in the DLL file.</span></span>  
  
 <span data-ttu-id="e5089-117">Windows 98, Windows ME, Windows NT 및 Windows 2000에는 `_CorDllMain` 함수는 간접적으로 호출을 fixupin 통해 운영 체제 로더.</span><span class="sxs-lookup"><span data-stu-id="e5089-117">In Windows 98, Windows ME, Windows NT, and Windows 2000, the `_CorDllMain` function is called indirectly through a fixupin the operating system loader.</span></span> <span data-ttu-id="e5089-118">다른 모든 버전의 Windows에서는 운영 체제 로더에 의해 직접 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5089-118">In all other versions of Windows, it is called directly by the operating system loader.</span></span>  
  
 <span data-ttu-id="e5089-119">자세한 내용은 주의 섹션을 참조 합니다 [_CorValidateImage](../../../../docs/framework/unmanaged-api/hosting/corvalidateimage-function.md) 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="e5089-119">For additional information, see the Remarks section in the [_CorValidateImage](../../../../docs/framework/unmanaged-api/hosting/corvalidateimage-function.md) topic.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e5089-120">요구 사항</span><span class="sxs-lookup"><span data-stu-id="e5089-120">Requirements</span></span>  
 <span data-ttu-id="e5089-121">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="e5089-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e5089-122">**헤더:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="e5089-122">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e5089-123">**라이브러리:** MsCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="e5089-123">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e5089-124">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e5089-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5089-125">참고자료</span><span class="sxs-lookup"><span data-stu-id="e5089-125">See also</span></span>
- [<span data-ttu-id="e5089-126">메타데이터 전역 정적 함수</span><span class="sxs-lookup"><span data-stu-id="e5089-126">Metadata Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-global-static-functions.md)
