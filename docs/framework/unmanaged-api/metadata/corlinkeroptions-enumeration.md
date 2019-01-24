---
title: CorLinkerOptions 열거형
ms.date: 03/30/2017
api_name:
- CorLinkerOptions
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorLinkerOptions
helpviewer_keywords:
- CorLinkerOptions enumeration [.NET Framework metadata]
ms.assetid: a656aad6-cc7e-4994-8251-004a6a45e18f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0a072e124343641c9f75fb9f924a6409efc8e1d4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54719939"
---
# <a name="corlinkeroptions-enumeration"></a><span data-ttu-id="ebdce-102">CorLinkerOptions 열거형</span><span class="sxs-lookup"><span data-stu-id="ebdce-102">CorLinkerOptions Enumeration</span></span>
<span data-ttu-id="ebdce-103">메타데이터 링커 옵션을 선택하는 플래그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ebdce-103">Specifies flags to select options for the metadata linker.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ebdce-104">구문</span><span class="sxs-lookup"><span data-stu-id="ebdce-104">Syntax</span></span>  
  
```  
typedef enum CorLinkerOptions {  
    MDAssembly          = 0x00000000,  
    MDNetModule         = 0x00000001,  
} CorLinkerOptions;  
```  
  
## <a name="members"></a><span data-ttu-id="ebdce-105">멤버</span><span class="sxs-lookup"><span data-stu-id="ebdce-105">Members</span></span>  
  
|<span data-ttu-id="ebdce-106">멤버</span><span class="sxs-lookup"><span data-stu-id="ebdce-106">Member</span></span>|<span data-ttu-id="ebdce-107">설명</span><span class="sxs-lookup"><span data-stu-id="ebdce-107">Description</span></span>|  
|------------|-----------------|  
|`MDAssembly`|<span data-ttu-id="ebdce-108">전용 형식 및 전역 함수 유지 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ebdce-108">The private types and global functions are not preserved.</span></span>|  
|`MDNetModule`|<span data-ttu-id="ebdce-109">전용 형식 및 전역 함수 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebdce-109">The private types and global functions are preserved.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ebdce-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="ebdce-110">Requirements</span></span>  
 <span data-ttu-id="ebdce-111">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="ebdce-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ebdce-112">**헤더:** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="ebdce-112">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="ebdce-113">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ebdce-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ebdce-114">참고자료</span><span class="sxs-lookup"><span data-stu-id="ebdce-114">See also</span></span>
- [<span data-ttu-id="ebdce-115">메타데이터 열거형</span><span class="sxs-lookup"><span data-stu-id="ebdce-115">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
