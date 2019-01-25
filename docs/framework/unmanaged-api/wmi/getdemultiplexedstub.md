---
title: GetDemultiplexedStub 함수 (관리 되지 않는 API 참조)
description: GetDemultiplexedStub 함수에는 Windows 관리에서 비동기 호출을 수신할 클라이언트를 지원 하기 위해 개체 전달자 싱크를 만듭니다.
ms.date: 11/06/2017
api_name:
- GetDemultiplexedStub
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetDemultiplexedStub
helpviewer_keywords:
- GetDemultiplexedStub function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: db41a11a3fb6c772a3e6fbb164435daa9e032ea5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54516943"
---
# <a name="getdemultiplexedstub-function"></a>GetDemultiplexedStub 함수
클라이언트가 Windows 관리에서 비동기 호출을 수신하는 데 도움이 되는 개체 전달자 싱크를 만듭니다.
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a>구문  
  
```  
HRESULT GetDemultiplexedStub (
   [in] IUnknown*    pObject, 
   [in] boolean      isLocal, 
   [out] IUnknown**  ppObject
); 
```  

## <a name="parameters"></a>매개 변수

`pObject`  
[in] 클라이언트의 in process 구현에 대 한 포인터 [IWbemObjectSink](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectsink)합니다.

`isLocal`  
[in] 이벤트를 로컬 인지 여부를 나타내는 플래그입니다 (`true`)이 고, 그렇지 않으면 `false`합니다.

`ppObject`  
[out] Windows 관리에서 비동기 호출을 수신할 클라이언트를 지원 하기 위해 개체 전달자 싱크.

## <a name="return-value"></a>반환 값

함수가 성공할 경우 반환 값은 `S_OK` (0).

함수가 실패 한 경우 반환 값은 0이 아닌 오류 코드입니다. 오류 정보를 호출 합니다 [GetErrorInfo](geterrorinfo.md) 함수입니다.
    
## <a name="requirements"></a>요구 사항  
 **플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.  
  
 **헤더:** WMINet_Utils.idl  
  
 **.NET Framework 버전:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>참고자료
- [WMI 및 성능 카운터 (관리 되지 않는 API 참조)](index.md)
