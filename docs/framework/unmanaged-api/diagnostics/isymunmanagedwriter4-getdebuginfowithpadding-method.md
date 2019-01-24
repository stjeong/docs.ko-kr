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
# <a name="isymunmanagedwriter4getdebuginfowithpadding-method"></a><span data-ttu-id="7bcf3-102">ISymUnmanagedWriter4::GetDebugInfoWithPadding 메서드</span><span class="sxs-lookup"><span data-stu-id="7bcf3-102">ISymUnmanagedWriter4::GetDebugInfoWithPadding Method</span></span>
<span data-ttu-id="7bcf3-103">동일 하 게 작동 [GetDebugInfo 메서드](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-getdebuginfo-method.md) 제외 하 고 경로 문자열을 문자열 데이터의 크기가 고정 되어 있도록 null 종결 문자 뒤에 오는 0이 채워집니다 `MAX_PATH`합니다.</span><span class="sxs-lookup"><span data-stu-id="7bcf3-103">Functions the same as [GetDebugInfo Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-getdebuginfo-method.md) except that the path string is padded with zeros following the terminating null character to make the string data a fixed size of `MAX_PATH`.</span></span> <span data-ttu-id="7bcf3-104">자체 경로 문자열 길이가 안쪽 여백을 지정 되어 보다 작은 `MAX_PATH`합니다.</span><span class="sxs-lookup"><span data-stu-id="7bcf3-104">Padding is only given if the path string length itself is less than `MAX_PATH`.</span></span>  
  
 <span data-ttu-id="7bcf3-105">따라서 쉽게 도구는 차이 PE 파일을 쓸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bcf3-105">This makes it easier to write tools that difference PE files.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7bcf3-106">구문</span><span class="sxs-lookup"><span data-stu-id="7bcf3-106">Syntax</span></span>  
  
```idl  
HRESULT GetDebugInfoWithPadding(    [in, out] IMAGE_DEBUG_DIRECTORY *pIDD,    [in] DWORD cData,    [out] DWORD *pcData,    [out, size_is(cData), length_is(*pcData)] BYTE data[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7bcf3-107">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7bcf3-107">Parameters</span></span>  
  
|<span data-ttu-id="7bcf3-108">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7bcf3-108">Parameter</span></span>|<span data-ttu-id="7bcf3-109">설명</span><span class="sxs-lookup"><span data-stu-id="7bcf3-109">Description</span></span>|  
|---------------|-----------------|  
|`pIDD`||  
|`cData`||  
|`pcData`||  
|`data`||  
  
## <a name="return-value"></a><span data-ttu-id="7bcf3-110">반환 값</span><span class="sxs-lookup"><span data-stu-id="7bcf3-110">Return Value</span></span>  
 <span data-ttu-id="7bcf3-111">`HRESULT`을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7bcf3-111">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7bcf3-112">요구 사항</span><span class="sxs-lookup"><span data-stu-id="7bcf3-112">Requirements</span></span>  
 <span data-ttu-id="7bcf3-113">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="7bcf3-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7bcf3-114">참고자료</span><span class="sxs-lookup"><span data-stu-id="7bcf3-114">See also</span></span>
- [<span data-ttu-id="7bcf3-115">ISymUnmanagedWriter4 인터페이스</span><span class="sxs-lookup"><span data-stu-id="7bcf3-115">ISymUnmanagedWriter4 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter4-interface.md)
