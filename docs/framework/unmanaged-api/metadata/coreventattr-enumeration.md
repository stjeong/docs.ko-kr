---
title: CorEventAttr 열거형
ms.date: 03/30/2017
api_name:
- CorEventAttr
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorEventAttr
helpviewer_keywords:
- CorEventAttr enumeration [.NET Framework metadata]
ms.assetid: dc2b3281-3820-487e-930d-350b66dc6417
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d34aa954126cc26519aaea963f99299e5557d2c8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54743054"
---
# <a name="coreventattr-enumeration"></a><span data-ttu-id="2a29e-102">CorEventAttr 열거형</span><span class="sxs-lookup"><span data-stu-id="2a29e-102">CorEventAttr Enumeration</span></span>
<span data-ttu-id="2a29e-103">이벤트의 메타데이터를 설명하는 값을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="2a29e-103">Contains values that describe the metadata of an event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2a29e-104">구문</span><span class="sxs-lookup"><span data-stu-id="2a29e-104">Syntax</span></span>  
  
```  
typedef enum CorEventAttr {  
  
    evSpecialName           =   0x0200,  
  
    evReservedMask          =   0x0400,  
    evRTSpecialName         =   0x0400,  
  
} CorEventAttr;  
```  
  
## <a name="members"></a><span data-ttu-id="2a29e-105">멤버</span><span class="sxs-lookup"><span data-stu-id="2a29e-105">Members</span></span>  
  
|<span data-ttu-id="2a29e-106">멤버</span><span class="sxs-lookup"><span data-stu-id="2a29e-106">Member</span></span>|<span data-ttu-id="2a29e-107">설명</span><span class="sxs-lookup"><span data-stu-id="2a29e-107">Description</span></span>|  
|------------|-----------------|  
|`evSpecialName`|<span data-ttu-id="2a29e-108">이벤트는 특별 하 고 이름과 설명 하는지 지정 하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="2a29e-108">Specifies that the event is special, and that its name describes how.</span></span>|  
|`evReservedMask`|<span data-ttu-id="2a29e-109">공용 언어 런타임에서 내부 용도로 예약 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a29e-109">Reserved for internal use by the common language runtime.</span></span>|  
|`evRTSpecialName`|<span data-ttu-id="2a29e-110">공용 언어 런타임 이벤트 이름 인코딩을 확인 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a29e-110">Specifies that the common language runtime should check the encoding of the event name.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="2a29e-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="2a29e-111">Requirements</span></span>  
 <span data-ttu-id="2a29e-112">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="2a29e-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2a29e-113">**헤더:** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="2a29e-113">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="2a29e-114">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2a29e-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2a29e-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="2a29e-115">See also</span></span>
- [<span data-ttu-id="2a29e-116">메타데이터 열거형</span><span class="sxs-lookup"><span data-stu-id="2a29e-116">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
