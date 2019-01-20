---
title: IXCLRDataMethodInstance::GetILAddressMap 메서드
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodInstance::GetILAddressMap Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodInstance::GetILAddressMap Method
helpviewer.keywords:
- IXCLRDataMethodInstance::GetILAddressMap Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 26c86af2c739532c96ce36c36561f8b8f089dd92
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416748"
---
# <a name="ixclrdatamethodinstancegetiladdressmap-method"></a>IXCLRDataMethodInstance::GetILAddressMap 메서드

IL을 주소 매핑 정보를 가져옵니다.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>구문

```
HRESULT GetILAddressMap(
    [in] ULONG32                                   mapLen,
    [out] ULONG32                                 *mapNeeded,
    [out, size_is(mapLen)] CLRDATA_IL_ADDRESS_MAP  maps[]
);
```

### <a name="parameters"></a>매개 변수

`mapLen` [in] 제공 된 맵 배열의 길이입니다.

`mapNeeded` [out] 메서드는 맵 항목의 수입니다.

`maps` [out, size_is(mapLen)] 맵 항목을 저장 하기 위한 배열입니다.

## <a name="remarks"></a>설명

제공 된 메서드는의 일부는 `IXCLRDataMethodInstance` 인터페이스 및 가상 메서드 테이블의 14 슬롯에 해당 합니다.

## <a name="requirements"></a>요구 사항

**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.  
**헤더:** 없음  
**라이브러리:** 없음  
**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>참고 항목

- [디버깅](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [IXCLRDataMethodInstance 인터페이스](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethodinstance-interface.md)
