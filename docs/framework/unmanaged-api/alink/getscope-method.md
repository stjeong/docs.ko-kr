---
title: GetScope Method1
ms.date: 03/30/2017
api_name:
- IALink.GetScope
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetScope
helpviewer_keywords:
- GetScope method
ms.assetid: e1555328-2c71-4ece-b357-9eb6d3a8efc4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 782697536f5e01fa29830a64e47d960a47fe4eae
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54663143"
---
# <a name="getscope-method1"></a><span data-ttu-id="a0c96-102">GetScope Method1</span><span class="sxs-lookup"><span data-stu-id="a0c96-102">GetScope Method1</span></span>
<span data-ttu-id="a0c96-103">가져오기 범위를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0c96-103">Gets an import scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a0c96-104">구문</span><span class="sxs-lookup"><span data-stu-id="a0c96-104">Syntax</span></span>  
  
```  
HRESULT GetScope(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwScope,  
    IMetaDataImport** ppImportScope  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a0c96-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a0c96-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="a0c96-106">가져올 어셈블리의 고유 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a0c96-106">Unique ID of assembly to import to.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="a0c96-107">가져올 파일의 고유 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a0c96-107">Unique ID of the file to import from.</span></span>  
  
 `dwScope`  
 <span data-ttu-id="a0c96-108">가져오려는 0부터 시작 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="a0c96-108">Zero-based scope to import.</span></span>  
  
 `ppImportScope`  
 <span data-ttu-id="a0c96-109">수신 [IMetaDataImport 인터페이스](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) 범위에 대 한 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="a0c96-109">Receives [IMetaDataImport Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) interface for the scope.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a0c96-110">반환 값</span><span class="sxs-lookup"><span data-stu-id="a0c96-110">Return Value</span></span>  
 <span data-ttu-id="a0c96-111">메서드가 성공 하면 S_OK를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c96-111">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a0c96-112">요구 사항</span><span class="sxs-lookup"><span data-stu-id="a0c96-112">Requirements</span></span>  
 <span data-ttu-id="a0c96-113">Alink.h 필요</span><span class="sxs-lookup"><span data-stu-id="a0c96-113">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0c96-114">참고자료</span><span class="sxs-lookup"><span data-stu-id="a0c96-114">See also</span></span>
- [<span data-ttu-id="a0c96-115">IALink 인터페이스</span><span class="sxs-lookup"><span data-stu-id="a0c96-115">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="a0c96-116">IALink2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="a0c96-116">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="a0c96-117">ALink API</span><span class="sxs-lookup"><span data-stu-id="a0c96-117">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
