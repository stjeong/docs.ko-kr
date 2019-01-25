---
title: IEnumReferenceIdentity 인터페이스
ms.date: 03/30/2017
api_name:
- IEnumReferenceIdentity
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IEnumReferenceIdentity
helpviewer_keywords:
- IEnumReferenceIdentity interface [.NET Framework fusion]
ms.assetid: a17b3155-7216-4e16-8c9f-abce21f549e7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1f2ea9d0e20cb67cc36d0b5883e483ce98941b2f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54743220"
---
# <a name="ienumreferenceidentity-interface"></a><span data-ttu-id="5893e-102">IEnumReferenceIdentity 인터페이스</span><span class="sxs-lookup"><span data-stu-id="5893e-102">IEnumReferenceIdentity Interface</span></span>
<span data-ttu-id="5893e-103">컬렉션의 열거자 역할을 `IReferenceIdentity` 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5893e-103">Serves as an enumerator for a collection of `IReferenceIdentity` objects.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5893e-104">메서드</span><span class="sxs-lookup"><span data-stu-id="5893e-104">Methods</span></span>  
  
|<span data-ttu-id="5893e-105">메서드</span><span class="sxs-lookup"><span data-stu-id="5893e-105">Method</span></span>|<span data-ttu-id="5893e-106">설명</span><span class="sxs-lookup"><span data-stu-id="5893e-106">Description</span></span>|  
|------------|-----------------|  
|`IEnumReferenceIdentity::Clone`|<span data-ttu-id="5893e-107">새 인터페이스 포인터를 가져옵니다 `IEnumReferenceIdentity` 이 동일한 멤버를 포함 하는 `IEnumReferenceIdentity`합니다.</span><span class="sxs-lookup"><span data-stu-id="5893e-107">Gets an interface pointer to a new `IEnumReferenceIdentity` that contains the same members as this `IEnumReferenceIdentity`.</span></span>|  
|`IEnumReferenceIdentity::Next`|<span data-ttu-id="5893e-108">지정 된 수를 가져옵니다 `IReferenceIdentity` 개체를 현재 위치에서 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5893e-108">Gets the specified number of `IReferenceIdentity` objects, starting at the current position.</span></span>|  
|`IEnumReferenceIdentity::Reset`|<span data-ttu-id="5893e-109">이 부분에 명령 포인터를 이동 `IEnumReferenceIdentity`합니다.</span><span class="sxs-lookup"><span data-stu-id="5893e-109">Moves the instruction pointer to the beginning of this `IEnumReferenceIdentity`.</span></span>|  
|`IEnumReferenceIdentity::Skip`|<span data-ttu-id="5893e-110">요소를 현재 위치부터 지정한 수 만큼 앞으로 명령 포인터를 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="5893e-110">Moves the instruction pointer forward by the specified number of elements, starting at the current position.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5893e-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="5893e-111">Requirements</span></span>  
 <span data-ttu-id="5893e-112">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="5893e-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5893e-113">**헤더:** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="5893e-113">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="5893e-114">**.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5893e-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5893e-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="5893e-115">See also</span></span>
- [<span data-ttu-id="5893e-116">Fusion 인터페이스</span><span class="sxs-lookup"><span data-stu-id="5893e-116">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [<span data-ttu-id="5893e-117">IReferenceIdentity 인터페이스</span><span class="sxs-lookup"><span data-stu-id="5893e-117">IReferenceIdentity Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/ireferenceidentity-interface.md)
