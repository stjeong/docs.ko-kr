---
title: ISOSDacInterface::GetMethodDescData 메서드
ms.date: 01/16/2019
api.name:
- ISOSDacInterface::GetMethodDescData Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- ISOSDacInterface::GetMethodDescData Method
helpviewer.keywords:
- ISOSDacInterface::GetMethodDescData Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: e56f837c4d3362ec6e71030e4fb475df42b9fba4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54639958"
---
# <a name="isosdacinterfacegetmethoddescdata-method"></a>ISOSDacInterface::GetMethodDescData 메서드

에 대 한 데이터를 가져옵니다는 주어진 [MethodDesc](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md)합니다.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>구문

```
HRESULT GetMethodDescData(
    CLRDATA_ADDRESS            methodDesc,
    CLRDATA_ADDRESS            ip,
    void                       *data,
    ULONG                      cRevertedRejitVersions,
    void                      *rgRevertedRejitData,
    void                      *pcNeededRevertedRejitData
);
```

### <a name="parameters"></a>매개 변수

`methodDesc` [in] 주소는 MethodDesc입니다.

`ip` [in] 메서드의 IP 주소입니다.

`data` [out] 내부 Api에서 반환 되는 MethodDesc와 연결 된 데이터입니다. 구조에는 168 바이트 이상 필요합니다.

`cRevertedRejitVersions` [out] 되돌린된 rejit 버전 수입니다.

`rgRevertedRejitData` [out] 내부 Api에서 반환 된 되돌린된 rejit 버전과 연결 된 데이터입니다. 구조에는 24 바이트 이상 필요합니다.

`pcNeededRevertedRejitData` [out] 되돌린된 ReJit 버전과 연결 된 데이터를 저장 하는 데 필요한 바이트 수입니다.

## <a name="remarks"></a>설명

제공 된 메서드는의 일부는 `ISOSDacInterface` 인터페이스 및 가상 메서드 테이블의 20 슬롯에 해당 합니다. 또한는 `CLRDATA_ADDRESS` 은 64 비트 부호 없는 정수입니다.

## <a name="requirements"></a>요구 사항

**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.  
**헤더:** 없음  
**라이브러리:** 없음  
**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>참고자료

- [디버깅](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [ISOSDacInterface 인터페이스](../../../../docs/framework/unmanaged-api/debugging/isosdacinterface-interface.md)
