---
title: IMethodMalloc::Alloc 메서드
ms.date: 03/30/2017
api_name:
- IMethodMalloc.Alloc
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- IMethodMalloc::Alloc
helpviewer_keywords:
- IMethodMalloc::Alloc method [.NET Framework profiling]
- Alloc method, IMethodMalloc interface [.NET Framework profiling]
ms.assetid: 8653bd4c-2290-43d2-a3e1-cbbd50033f4f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 54c38f9a9abc9a02ba4d84c9a41b2ef6b1f7cb69
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54528565"
---
# <a name="imethodmallocalloc-method"></a>IMethodMalloc::Alloc 메서드
새 Microsoft MSIL (intermediate language) 함수 본문에 대 한 지정된 된 양의 메모리를 할당 하려고 시도 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
PVOID Alloc (  
    [in] ULONG   cb  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `cb`  
 [in] 메서드 본문에 대해 할당할 바이트 수입니다.  
  
## <a name="remarks"></a>설명  
 할당 된 메모리가이 할당자와 연결 된 모듈의 기본 주소 보다 큰 주소에서 시작 됩니다. 즉, 각 할당자는 특정 모듈의 경우 생성 되 고 해당 기본 주소에서 양수 오프셋에서 메모리를 할당 하려고 합니다. 경우 `Alloc` 모듈의 기준 주소 보다 큰 주소에서 바이트 수가 요청 된 할당에 실패 e_outofmemory가 실제 양 사용 가능한 메모리 공간에 관계 없이 반환 합니다.  
  
 합니다 `Alloc` 함께에서 메서드를 사용 해야 합니다 [icorprofilerinfo:: Setilfunctionbody](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setilfunctionbody-method.md) 메서드.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** WindSee [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.  
  
 **헤더:** CorProf.idl, CorProf.h  
  
 **라이브러리:** CorGuids.lib  
  
 **.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>참고자료
- [IMethodMalloc 인터페이스](../../../../docs/framework/unmanaged-api/profiling/imethodmalloc-interface.md)
