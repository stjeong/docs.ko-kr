---
title: CorImportOptions 열거형
ms.date: 03/30/2017
api_name:
- CorImportOptions
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorImportOptions
helpviewer_keywords:
- CorImportOptions enumeration [.NET Framework metadata]
ms.assetid: 4e5d03cb-97c9-4ff4-8dbd-17d94ee374d3
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8a4cc17bdcaea5099d0d2b0195ae4fa28e3d4744
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54744607"
---
# <a name="corimportoptions-enumeration"></a><span data-ttu-id="1b500-102">CorImportOptions 열거형</span><span class="sxs-lookup"><span data-stu-id="1b500-102">CorImportOptions Enumeration</span></span>
<span data-ttu-id="1b500-103">현재 범위를 벗어난 어셈블리를 가져오는 중의 동작을 제어하는 플래그 값을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="1b500-103">Contains flag values that control the behavior during importation of an assembly outside the current scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1b500-104">구문</span><span class="sxs-lookup"><span data-stu-id="1b500-104">Syntax</span></span>  
  
```  
typedef enum CorImportOptions {  
  
    MDImportOptionDefault                = 0x00000000,  
    MDImportOptionAll                    = 0xFFFFFFFF,  
    MDImportOptionAllTypeDefs            = 0x00000001,  
    MDImportOptionAllMethodDefs          = 0x00000002,  
    MDImportOptionAllFieldDefs           = 0x00000004,  
    MDImportOptionAllProperties          = 0x00000008,  
    MDImportOptionAllEvents              = 0x00000010,  
    MDImportOptionAllCustomAttributes    = 0x00000020,  
    MDImportOptionAllExportedTypes       = 0x00000040  
  
} CorImportOptions;  
```  
  
## <a name="members"></a><span data-ttu-id="1b500-105">멤버</span><span class="sxs-lookup"><span data-stu-id="1b500-105">Members</span></span>  
  
|<span data-ttu-id="1b500-106">멤버</span><span class="sxs-lookup"><span data-stu-id="1b500-106">Member</span></span>|<span data-ttu-id="1b500-107">설명</span><span class="sxs-lookup"><span data-stu-id="1b500-107">Description</span></span>|  
|------------|-----------------|  
|`MDImportOptionDefault`|<span data-ttu-id="1b500-108">삭제 된 레코드를 건너뛸 하는 기본 동작을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1b500-108">Indicates the default behavior, which is to skip deleted records.</span></span>|  
|`MDImportOptionAll`|<span data-ttu-id="1b500-109">모든 메타 데이터를 열거 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1b500-109">Indicates that all metadata should be enumerated.</span></span>|  
|`MDImportOptionAllTypeDefs`|<span data-ttu-id="1b500-110">삭제 된 항목을 포함 하는 모든 형식 정의 열거 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1b500-110">Indicates that all TypeDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllMethodDefs`|<span data-ttu-id="1b500-111">삭제 된 항목을 포함 하는 모든 MethodDefs 열거 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1b500-111">Indicates that all MethodDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllFieldDefs`|<span data-ttu-id="1b500-112">삭제 된 항목을 포함 하 여 모든 Fielddef 열거 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1b500-112">Indicates that all FieldDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllProperties`|<span data-ttu-id="1b500-113">삭제 된 항목을 포함 하는 모든 PropertyDefs 열거 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1b500-113">Indicates that all PropertyDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllEvents`|<span data-ttu-id="1b500-114">삭제 된 항목을 포함 하 여 모든 Eventdef 열거 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1b500-114">Indicates that all EventDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllCustomAttributes`|<span data-ttu-id="1b500-115">삭제 된 항목을 포함 하 여 모든 사용자 지정 특성을 열거 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1b500-115">Indicates that all custom attributes, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllExportedTypes`|<span data-ttu-id="1b500-116">삭제 된 항목을 비롯 한 모든 내보낸된 형식이 열거 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1b500-116">Indicates that all exported types, including deleted ones, should be enumerated.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1b500-117">요구 사항</span><span class="sxs-lookup"><span data-stu-id="1b500-117">Requirements</span></span>  
 <span data-ttu-id="1b500-118">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="1b500-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1b500-119">**헤더:** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="1b500-119">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="1b500-120">**.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1b500-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1b500-121">참고자료</span><span class="sxs-lookup"><span data-stu-id="1b500-121">See also</span></span>
- [<span data-ttu-id="1b500-122">메타데이터 열거형</span><span class="sxs-lookup"><span data-stu-id="1b500-122">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
