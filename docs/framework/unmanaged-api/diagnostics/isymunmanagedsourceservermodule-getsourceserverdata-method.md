---
title: ISymUnmanagedSourceServerModule::GetSourceServerData 메서드
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSourceServerModule.GetSourceServerData
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSourceServerModule::GetSourceServerData
helpviewer_keywords:
- ISymUnmanagedSourceServerModule::GetSourceServerData method [.NET Framework debugging]
- GetSourceServerData method [.NET Framework debugging]
ms.assetid: 20bdf8ff-2d15-4c64-8950-6888f642d6c0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 71251af116fc8d634b822e1daa49d90e91fec6f1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54648825"
---
# <a name="isymunmanagedsourceservermodulegetsourceserverdata-method"></a><span data-ttu-id="5e4aa-102">ISymUnmanagedSourceServerModule::GetSourceServerData 메서드</span><span class="sxs-lookup"><span data-stu-id="5e4aa-102">ISymUnmanagedSourceServerModule::GetSourceServerData Method</span></span>
<span data-ttu-id="5e4aa-103">모듈에 대 한 원본 서버 데이터를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4aa-103">Returns the source server data for the module.</span></span> <span data-ttu-id="5e4aa-104">호출자에 게 사용 하 여 리소스를 해제 해야 `CoTaskMemFree`합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4aa-104">The caller must free resources by using `CoTaskMemFree`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5e4aa-105">구문</span><span class="sxs-lookup"><span data-stu-id="5e4aa-105">Syntax</span></span>  
  
```  
HRESULT GetSourceServerData(  
    [out] ULONG* pDataByteCount,   
    [out, size_is (, *pDataByteCount)] BYTE** ppData);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5e4aa-106">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5e4aa-106">Parameters</span></span>  
 `pDataByteCount`  
 <span data-ttu-id="5e4aa-107">[out] 에 대 한 포인터를 `ULONG32` 원본 서버 데이터를 바이트 단위로 크기를 받는 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e4aa-107">[out] A pointer to a `ULONG32` that receives the size, in bytes, of the source server data.</span></span>  
  
 `ppData`  
 <span data-ttu-id="5e4aa-108">[out] 반환 된 포인터 `pDataByteCount` 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5e4aa-108">[out] A pointer to the returned `pDataByteCount` value.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5e4aa-109">반환 값</span><span class="sxs-lookup"><span data-stu-id="5e4aa-109">Return Value</span></span>  
 <span data-ttu-id="5e4aa-110">메서드가 성공 하면 s_ok이 고 그렇지 않으면 E_FAIL 또는 일부 다른 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="5e4aa-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5e4aa-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="5e4aa-111">Requirements</span></span>  
 <span data-ttu-id="5e4aa-112">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="5e4aa-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e4aa-113">참고자료</span><span class="sxs-lookup"><span data-stu-id="5e4aa-113">See also</span></span>
- [<span data-ttu-id="5e4aa-114">ISymUnmanagedSourceServerModule 인터페이스</span><span class="sxs-lookup"><span data-stu-id="5e4aa-114">ISymUnmanagedSourceServerModule Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsourceservermodule-interface.md)
