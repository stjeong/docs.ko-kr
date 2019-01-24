---
title: CloseAssembly 메서드
ms.date: 03/30/2017
api_name:
- IALink.CloseAssembly
- CloseAssembly
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- CloseAssembly
helpviewer_keywords:
- CloseAssembly method
ms.assetid: f66a43bc-a5c5-4190-acbe-63fd27640634
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: aa415926f4a818f697812f1a3c5531cb0ab7081b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54510171"
---
# <a name="closeassembly-method"></a><span data-ttu-id="c721e-102">CloseAssembly 메서드</span><span class="sxs-lookup"><span data-stu-id="c721e-102">CloseAssembly Method</span></span>
<span data-ttu-id="c721e-103">어셈블리 작업을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="c721e-103">Finalizes assembly operations.</span></span> <span data-ttu-id="c721e-104">새 어셈블리 또는 바인딩되지 않은 모듈을 시작 하기 전에이 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="c721e-104">Call this method before beginning a new assembly or unbound module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c721e-105">구문</span><span class="sxs-lookup"><span data-stu-id="c721e-105">Syntax</span></span>  
  
```  
HRESULT CloseAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c721e-106">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c721e-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="c721e-107">어셈블리의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c721e-107">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c721e-108">반환 값</span><span class="sxs-lookup"><span data-stu-id="c721e-108">Return Value</span></span>  
 <span data-ttu-id="c721e-109">메서드가 성공 하면 S_OK를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c721e-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c721e-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="c721e-110">Requirements</span></span>  
 <span data-ttu-id="c721e-111">Alink.h가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="c721e-111">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c721e-112">참고자료</span><span class="sxs-lookup"><span data-stu-id="c721e-112">See also</span></span>
- [<span data-ttu-id="c721e-113">IALink 인터페이스</span><span class="sxs-lookup"><span data-stu-id="c721e-113">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="c721e-114">IALink2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="c721e-114">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="c721e-115">ALink API</span><span class="sxs-lookup"><span data-stu-id="c721e-115">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
