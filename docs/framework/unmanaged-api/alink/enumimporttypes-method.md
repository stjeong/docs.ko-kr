---
title: EnumImportTypes 메서드
ms.date: 03/30/2017
api_name:
- EnumImportTypes
- IALink.EnumImportTypes
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EnumImportTypes
helpviewer_keywords:
- EnumImportTypes method
ms.assetid: 83a0e4e7-ec06-40cb-9b63-700b9695bb04
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4e437868138d7ae31d233853ecc0f709de3ee39d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54512725"
---
# <a name="enumimporttypes-method"></a><span data-ttu-id="56556-102">EnumImportTypes 메서드</span><span class="sxs-lookup"><span data-stu-id="56556-102">EnumImportTypes Method</span></span>
<span data-ttu-id="56556-103">각 범위에서 각 종류를 열거합니다.</span><span class="sxs-lookup"><span data-stu-id="56556-103">Enumerates each type in each scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="56556-104">구문</span><span class="sxs-lookup"><span data-stu-id="56556-104">Syntax</span></span>  
  
```  
HRESULT EnumImportTypes(  
    HALINKENUM   hEnum,  
    DWORD        dwMax,  
    mdTypeDef    aTypeDefs[],  
    DWORD*       pdwCount  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="56556-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="56556-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="56556-106">열거자에 대 한 핸들입니다.</span><span class="sxs-lookup"><span data-stu-id="56556-106">Handle for enumerator.</span></span>  
  
 `dwMax`  
 <span data-ttu-id="56556-107">최대 검색 하는 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="56556-107">Maximum number of types to retrieve.</span></span>  
  
 `aTypeDefs`  
 <span data-ttu-id="56556-108">형식 토큰을 넘지 받습니다 `dwMax`합니다.</span><span class="sxs-lookup"><span data-stu-id="56556-108">Recieves type tokens, not to exceed `dwMax`.</span></span>  
  
 `pdwCount`  
 <span data-ttu-id="56556-109">실제 수를 입력 받는 `aTypeDefs`합니다.</span><span class="sxs-lookup"><span data-stu-id="56556-109">Receives actual number of type in `aTypeDefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="56556-110">반환 값</span><span class="sxs-lookup"><span data-stu-id="56556-110">Return Value</span></span>  
 <span data-ttu-id="56556-111">메서드가 성공 하면 S_OK를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="56556-111">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="56556-112">요구 사항</span><span class="sxs-lookup"><span data-stu-id="56556-112">Requirements</span></span>  
 <span data-ttu-id="56556-113">Alink.h 필요</span><span class="sxs-lookup"><span data-stu-id="56556-113">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="56556-114">참고자료</span><span class="sxs-lookup"><span data-stu-id="56556-114">See also</span></span>
- [<span data-ttu-id="56556-115">IALink 인터페이스</span><span class="sxs-lookup"><span data-stu-id="56556-115">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="56556-116">IALink2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="56556-116">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="56556-117">ALink API</span><span class="sxs-lookup"><span data-stu-id="56556-117">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
