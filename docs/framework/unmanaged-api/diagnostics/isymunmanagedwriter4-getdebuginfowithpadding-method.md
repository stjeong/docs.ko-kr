---
title: ISymUnmanagedWriter4::GetDebugInfoWithPadding 메서드
ms.date: 03/30/2017
ms.assetid: 881e20ca-8131-4bd0-ba41-c2d6391b0fe2
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1d669ae15c01a560f2cefb6e361ca32411652fbc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54732975"
---
# <a name="isymunmanagedwriter4getdebuginfowithpadding-method"></a>ISymUnmanagedWriter4::GetDebugInfoWithPadding 메서드
동일 하 게 작동 [GetDebugInfo 메서드](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-getdebuginfo-method.md) 제외 하 고 경로 문자열을 문자열 데이터의 크기가 고정 되어 있도록 null 종결 문자 뒤에 오는 0이 채워집니다 `MAX_PATH`합니다. 자체 경로 문자열 길이가 안쪽 여백을 지정 되어 보다 작은 `MAX_PATH`합니다.  
  
 따라서 쉽게 도구는 차이 PE 파일을 쓸 수 있습니다.  
  
## <a name="syntax"></a>구문  
  
```idl  
HRESULT GetDebugInfoWithPadding(    [in, out] IMAGE_DEBUG_DIRECTORY *pIDD,    [in] DWORD cData,    [out] DWORD *pcData,    [out, size_is(cData), length_is(*pcData)] BYTE data[]);  
```  
  
#### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|`pIDD`||  
|`cData`||  
|`pcData`||  
|`data`||  
  
## <a name="return-value"></a>반환 값  
 `HRESULT`을 반환합니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>참고자료
- [ISymUnmanagedWriter4 인터페이스](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter4-interface.md)
