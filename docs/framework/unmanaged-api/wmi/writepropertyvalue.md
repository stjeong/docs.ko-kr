---
title: WritePropertyValue 함수 (관리 되지 않는 API 참조)
description: WritePropertyValue 함수 속성에 바이트를 씁니다.
ms.date: 11/06/2017
api_name:
- WritePropertyValue
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- WritePropertyValue
helpviewer_keywords:
- WritePropertyValue function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f2a4eb444967390492be33b25866de8a93a1698c
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43393909"
---
# <a name="writepropertyvalue-function"></a><span data-ttu-id="48faf-103">WritePropertyValue 함수</span><span class="sxs-lookup"><span data-stu-id="48faf-103">WritePropertyValue function</span></span>
<span data-ttu-id="48faf-104">속성 핸들에 의해 식별 된 속성에 지정 된 바이트 수를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="48faf-104">Writes a specified number of bytes to a property identified by a property handle.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a><span data-ttu-id="48faf-105">구문</span><span class="sxs-lookup"><span data-stu-id="48faf-105">Syntax</span></span>  
  
```  
HRESULT WritePropertyValue (
   [in] int                  vFunc, 
   [in] IWbemObjectAccess*   ptr, 
   [in] long                 lHandle,
   [in] long                 lNumBytes,
   [in] byte*                aData
); 
```  

## <a name="parameters"></a><span data-ttu-id="48faf-106">매개 변수</span><span class="sxs-lookup"><span data-stu-id="48faf-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="48faf-107">[in] 이 매개 변수 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="48faf-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="48faf-108">[in] 에 대 한 포인터를 [IWbemObjectAccess](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess) 인스턴스.</span><span class="sxs-lookup"><span data-stu-id="48faf-108">[in] A pointer to an [IWbemObjectAccess](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess) instance.</span></span>

`lHandle`  
<span data-ttu-id="48faf-109">[in] 이 속성을 식별 하는 핸들을 포함 하는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="48faf-109">[in] An integer that contains the handle that identifies this property.</span></span> <span data-ttu-id="48faf-110">핸들을 호출 하 여 검색할 수는 [GetPropertyHandle](getpropertyhandle.md) 함수입니다.</span><span class="sxs-lookup"><span data-stu-id="48faf-110">The handle can be retrieved by calling the [GetPropertyHandle](getpropertyhandle.md) function.</span></span>   

`lNumBytes`  
<span data-ttu-id="48faf-111">[in] 속성에 쓸 바이트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="48faf-111">[in] The number of bytes being written to the property.</span></span> <span data-ttu-id="48faf-112">참조 된 [주의](#remarks) 자세한 내용은 섹션입니다.</span><span class="sxs-lookup"><span data-stu-id="48faf-112">See the [Remarks](#remarks) section for more information.</span></span>

`pHandle`   
<span data-ttu-id="48faf-113">[out] 데이터를 포함 하는 바이트 배열에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="48faf-113">[out] A pointer to the byte array that contains the data.</span></span>

## <a name="return-value"></a><span data-ttu-id="48faf-114">반환 값</span><span class="sxs-lookup"><span data-stu-id="48faf-114">Return value</span></span>

<span data-ttu-id="48faf-115">이 함수에 의해 반환 되는 다음 값에 정의 된 합니다 *WbemCli.h* 헤더 파일에서 정의할 수 상수로 코드:</span><span class="sxs-lookup"><span data-stu-id="48faf-115">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="48faf-116">상수</span><span class="sxs-lookup"><span data-stu-id="48faf-116">Constant</span></span>  |<span data-ttu-id="48faf-117">값</span><span class="sxs-lookup"><span data-stu-id="48faf-117">Value</span></span>  |<span data-ttu-id="48faf-118">설명</span><span class="sxs-lookup"><span data-stu-id="48faf-118">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="48faf-119">'(0x80041008</span><span class="sxs-lookup"><span data-stu-id="48faf-119">0x80041008</span></span> | <span data-ttu-id="48faf-120">매개 변수가 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="48faf-120">A parameter is not valid.</span></span> |
|`WBEM_E_TYPE_MISMATCH` | <span data-ttu-id="48faf-121">0x80041005가 나타나는 경우</span><span class="sxs-lookup"><span data-stu-id="48faf-121">0x80041005</span></span> | <span data-ttu-id="48faf-122">형식 불일치가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="48faf-122">A type mismatch occurred.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="48faf-123">0</span><span class="sxs-lookup"><span data-stu-id="48faf-123">0</span></span> | <span data-ttu-id="48faf-124">함수 호출이 성공 했습니다.</span><span class="sxs-lookup"><span data-stu-id="48faf-124">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="48faf-125">설명</span><span class="sxs-lookup"><span data-stu-id="48faf-125">Remarks</span></span>

<span data-ttu-id="48faf-126">이 함수에 대 한 호출을 래핑하는 [IWbemClassObject::WritePropertyValue](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-writepropertyvalue) 메서드.</span><span class="sxs-lookup"><span data-stu-id="48faf-126">This function wraps a call to the [IWbemClassObject::WritePropertyValue](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-writepropertyvalue) method.</span></span>

<span data-ttu-id="48faf-127">이 함수를 사용 하 여 문자열 및 모든 다른 비-설정할`DWORD` 또는 비-`QWORD` 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="48faf-127">Use this function to set string and all other non-`DWORD` or non-`QWORD` data.</span></span>

<span data-ttu-id="48faf-128">문자열이 아닌 속성 값에 대 한 `lNumBytes` 지정 된 속성 형식의 올바른 데이터 크기 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="48faf-128">For nonstring property values, `lNumBytes` must be the correct data size of the property type specified.</span></span> <span data-ttu-id="48faf-129">문자열 속성 값에 대 한 `lNumBytes` 길이 여야 합니다 (바이트) 지정된 된 문자열 및 문자열을도 길이 (바이트) 이어야 합니다 자체 및이 null 종결 문자를 사용 하 여 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="48faf-129">For string property values, `lNumBytes` must be the length of the specified string in bytes, and the string itself must be of an even length in bytes and be followed with a null-termination character.</span></span>

## <a name="requirements"></a><span data-ttu-id="48faf-130">요구 사항</span><span class="sxs-lookup"><span data-stu-id="48faf-130">Requirements</span></span>  
<span data-ttu-id="48faf-131">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="48faf-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="48faf-132">**헤더:** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="48faf-132">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="48faf-133">**.NET Framework 버전:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="48faf-133">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="48faf-134">참고자료</span><span class="sxs-lookup"><span data-stu-id="48faf-134">See also</span></span>  
[<span data-ttu-id="48faf-135">WMI 및 성능 카운터 (관리 되지 않는 API 참조)</span><span class="sxs-lookup"><span data-stu-id="48faf-135">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
