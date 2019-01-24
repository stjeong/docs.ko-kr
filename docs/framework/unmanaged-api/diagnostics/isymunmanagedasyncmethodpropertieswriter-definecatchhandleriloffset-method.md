---
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset 메서드
ms.date: 03/30/2017
ms.assetid: 92af7896-2201-408d-8b1b-23e28001eeac
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 55d35db387d6184f68ff31a74253d3d1610c806f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54741253"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefinecatchhandleriloffset-method"></a>ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset 메서드
비동기 메서드를 래핑하는 컴파일러에서 생성 된 catch 처리기에 대 한 오프셋 IL을 설정 합니다.  
  
 생성 된 catch의 IL 오프셋 사용자 코드 메서드에서 발생할 수 있습니다 하는 경우에 사용자 코드가 아닌 것 처럼 catch를 처리 하도록 디버거에 의해 사용 됩니다. 특히 대 한 응답으로 사용 되는 **CatchHandlerFound** 예외 이벤트입니다.  
  
## <a name="syntax"></a>구문  
  
```idl  
HRESULT DefineCatchHandlerILOffset(    [in] ULONG32 catchHandlerOffset);  
```  
  
#### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|`catchHandlerOffset`||  
  
## <a name="return-value"></a>반환 값  
 `HRESULT`을 반환합니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>참고자료
- [ISymUnmanagedAsyncMethodPropertiesWriter 인터페이스](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)
