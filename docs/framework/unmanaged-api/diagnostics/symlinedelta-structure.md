---
title: SYMLINEDELTA 구조체
ms.date: 03/30/2017
api_name:
- SYMLINEDELTA
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- SYMLINEDELTA
helpviewer_keywords:
- SYMLINEDELTA structure [.NET Framework debugging]
ms.assetid: 9634e995-d46d-4397-ab66-cc5781d11e4e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2d534ae381e0dc105731cf0a537f81afe80d87e0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54732741"
---
# <a name="symlinedelta-structure"></a><span data-ttu-id="d5447-102">SYMLINEDELTA 구조체</span><span class="sxs-lookup"><span data-stu-id="d5447-102">SYMLINEDELTA Structure</span></span>
<span data-ttu-id="d5447-103">편집 결과로 이동 된 메서드에 대 한 기호 처리기에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5447-103">Provides information to the symbol handler about methods that were moved as a result of edits.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d5447-104">구문</span><span class="sxs-lookup"><span data-stu-id="d5447-104">Syntax</span></span>  
  
```  
typedef struct _SYMLINEDELTA  
    {  
        mdMethodDef  mdMethod;  
        INT32        delta;  
    } SYMLINEDELTA;  
```  
  
## <a name="members"></a><span data-ttu-id="d5447-105">멤버</span><span class="sxs-lookup"><span data-stu-id="d5447-105">Members</span></span>  
  
|<span data-ttu-id="d5447-106">멤버</span><span class="sxs-lookup"><span data-stu-id="d5447-106">Member</span></span>|<span data-ttu-id="d5447-107">설명</span><span class="sxs-lookup"><span data-stu-id="d5447-107">Description</span></span>|  
|------------|-----------------|  
|`mdMethod`|<span data-ttu-id="d5447-108">메서드의 메타 데이터 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="d5447-108">The method's metadata token.</span></span>|  
|`delta`|<span data-ttu-id="d5447-109">메서드가 이동 된 줄의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d5447-109">The number of lines the method was moved.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d5447-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="d5447-110">Requirements</span></span>  
 <span data-ttu-id="d5447-111">**헤더:** CorSym.idl</span><span class="sxs-lookup"><span data-stu-id="d5447-111">**Header:** CorSym.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d5447-112">참고자료</span><span class="sxs-lookup"><span data-stu-id="d5447-112">See also</span></span>
- [<span data-ttu-id="d5447-113">진단 기호 저장소 구조체</span><span class="sxs-lookup"><span data-stu-id="d5447-113">Diagnostics Symbol Store Structures</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-structures.md)
