---
title: IXCLRDataMethodDefinition::StartEnumInstances 메서드
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodDefinition::StartEnumInstances Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodDefinition::StartEnumInstances Method
helpviewer.keywords:
- IXCLRDataMethodDefinition::StartEnumInstances Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: c78af112e9239143c4854e34e9b6aa8e99344ec3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54623653"
---
# <a name="ixclrdatamethoddefinitionstartenuminstances-method"></a>IXCLRDataMethodDefinition::StartEnumInstances 메서드

에 대 한 메서드 인스턴스의 열거형에 대 한 핸들을 제공 된 지정 `IXCLRDataAppDomain`합니다.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>구문

```
HRESULT StartEnumInstances(
    [in] IXCLRDataAppDomain* appDomain,
    [out] CLRDATA_ENUM *handle
);
```

### <a name="parameters"></a>매개 변수

`appDomain` [in] 열거형에 대 한 AppDomain 합니다.

`handle` [out] 인스턴스를 열거 하는 것에 대 한 핸들입니다.

## <a name="remarks"></a>설명

제공 된 메서드는의 일부는 `IXCLRDataMethodDefinition` 인터페이스 및 가상 메서드 테이블의 세 번째 슬롯에 해당 합니다.

## <a name="requirements"></a>요구 사항

**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.  
**헤더:** 없음  
**라이브러리:** 없음  
**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>참고자료

- [CLRDataSourceType 열거형](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [디버깅](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [IXCLRDataMethodDefinition 인터페이스](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethoddefinition-interface.md)
