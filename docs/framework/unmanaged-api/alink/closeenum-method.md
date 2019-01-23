---
title: CloseEnum 메서드
ms.date: 03/30/2017
api_name:
- CloseEnum
- IALink.CloseEnum
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- CloseEnum
helpviewer_keywords:
- CloseEnum method
ms.assetid: aa4a091e-13fe-4264-91de-e12f1c767c87
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 009f7d20dfd6efc279b3187af8f5c95132ae51e7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54525237"
---
# <a name="closeenum-method"></a><span data-ttu-id="09835-102">CloseEnum 메서드</span><span class="sxs-lookup"><span data-stu-id="09835-102">CloseEnum Method</span></span>
<span data-ttu-id="09835-103">표시 된 열거형을 닫고 연결 된 리소스를 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="09835-103">Closes the indicated enumeration and frees associated resources.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="09835-104">구문</span><span class="sxs-lookup"><span data-stu-id="09835-104">Syntax</span></span>  
  
```  
HRESULT CloseEnum(  
    HALINKENUM hEnum  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="09835-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="09835-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="09835-106">핸들을 닫아야 하는 열거형입니다.</span><span class="sxs-lookup"><span data-stu-id="09835-106">Handle of enumeration to be closed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="09835-107">반환 값</span><span class="sxs-lookup"><span data-stu-id="09835-107">Return Value</span></span>  
 <span data-ttu-id="09835-108">메서드가 성공 하면 S_OK를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="09835-108">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="09835-109">요구 사항</span><span class="sxs-lookup"><span data-stu-id="09835-109">Requirements</span></span>  
 <span data-ttu-id="09835-110">Alink.h 필요</span><span class="sxs-lookup"><span data-stu-id="09835-110">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09835-111">참고자료</span><span class="sxs-lookup"><span data-stu-id="09835-111">See also</span></span>
- [<span data-ttu-id="09835-112">IALink 인터페이스</span><span class="sxs-lookup"><span data-stu-id="09835-112">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="09835-113">IALink2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="09835-113">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="09835-114">ALink API</span><span class="sxs-lookup"><span data-stu-id="09835-114">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
