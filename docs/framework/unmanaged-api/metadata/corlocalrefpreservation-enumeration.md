---
title: CorLocalRefPreservation 열거형
ms.date: 03/30/2017
api_name:
- CorLocalRefPreservation
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorLocalRefPreservation
helpviewer_keywords:
- CorLocalRefPreservation enumeration [.NET Framework metadata]
ms.assetid: 44757163-1228-4213-a4c4-d4de503cc75d
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e9ed3cdac726fbdbf9ee2b33f42565d8594bc36e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54669681"
---
# <a name="corlocalrefpreservation-enumeration"></a><span data-ttu-id="d6776-102">CorLocalRefPreservation 열거형</span><span class="sxs-lookup"><span data-stu-id="d6776-102">CorLocalRefPreservation Enumeration</span></span>
<span data-ttu-id="d6776-103">로컬 참조의 처리에 대한 플래그 값을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="d6776-103">Contains flag values for the treatment of local references.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d6776-104">구문</span><span class="sxs-lookup"><span data-stu-id="d6776-104">Syntax</span></span>  
  
```  
typedef enum CorLocalRefPreservation  
{  
    MDPreserveLocalRefsNone     =   0x00000000,  
    MDPreserveLocalTypeRef      =   0x00000001,  
    MDPreserveLocalMemberRef    =   0x00000002  
} CorLocalRefPreservation;  
```  
  
## <a name="members"></a><span data-ttu-id="d6776-105">멤버</span><span class="sxs-lookup"><span data-stu-id="d6776-105">Members</span></span>  
  
|<span data-ttu-id="d6776-106">멤버</span><span class="sxs-lookup"><span data-stu-id="d6776-106">Member</span></span>|<span data-ttu-id="d6776-107">설명</span><span class="sxs-lookup"><span data-stu-id="d6776-107">Description</span></span>|  
|------------|-----------------|  
|`MDPreserveLocalRefsNone`|<span data-ttu-id="d6776-108">없는 로컬 참조를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6776-108">Preserve no local references.</span></span>|  
|`MDPreserveLocalTypeRef`|<span data-ttu-id="d6776-109">로컬 형식 참조를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6776-109">Preserve local type references.</span></span>|  
|`MDPreserveLocalMemberRef`|<span data-ttu-id="d6776-110">로컬 멤버 참조를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6776-110">Preserve local member references.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d6776-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="d6776-111">Requirements</span></span>  
 <span data-ttu-id="d6776-112">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="d6776-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d6776-113">**헤더:** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="d6776-113">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="d6776-114">**.NET Framework 버전:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d6776-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d6776-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="d6776-115">See also</span></span>
- [<span data-ttu-id="d6776-116">메타데이터 열거형</span><span class="sxs-lookup"><span data-stu-id="d6776-116">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
