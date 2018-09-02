---
title: ICLRStrongName::StrongNameKeyDelete 메서드
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameKeyDelete
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameKeyDelete
helpviewer_keywords:
- StrongNameKeyDelete method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::StrongNameKeyDelete method [.NET Framework hosting]
ms.assetid: 0163412f-f617-4428-89e0-03992fec31e8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2515eb0e33a033e78843d68754d3175e91165dff
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43388789"
---
# <a name="iclrstrongnamestrongnamekeydelete-method"></a><span data-ttu-id="efa49-102">ICLRStrongName::StrongNameKeyDelete 메서드</span><span class="sxs-lookup"><span data-stu-id="efa49-102">ICLRStrongName::StrongNameKeyDelete Method</span></span>
<span data-ttu-id="efa49-103">지정된 된 키 컨테이너를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="efa49-103">Deletes the specified key container.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="efa49-104">구문</span><span class="sxs-lookup"><span data-stu-id="efa49-104">Syntax</span></span>  
  
```  
HRESULT StrongNameKeyDelete (  
    [in]  LPCWSTR   wszKeyContainer  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="efa49-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="efa49-105">Parameters</span></span>  
 `wszKeyContainer`  
 <span data-ttu-id="efa49-106">[in] 삭제할 키 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efa49-106">[in] The name of the key container to delete.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="efa49-107">반환 값</span><span class="sxs-lookup"><span data-stu-id="efa49-107">Return Value</span></span>  
 <span data-ttu-id="efa49-108">`S_OK` 메서드가 성공적으로 완료 하는 경우 그렇지 않으면 실패를 나타내는 HRESULT 값을 (참조 [일반적인 HRESULT 값](https://go.microsoft.com/fwlink/?LinkId=213878) 목록에 대 한).</span><span class="sxs-lookup"><span data-stu-id="efa49-108">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="efa49-109">설명</span><span class="sxs-lookup"><span data-stu-id="efa49-109">Remarks</span></span>  
 <span data-ttu-id="efa49-110">사용 된 [iclrstrongname:: Strongnamekeyinstall](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeyinstall-method.md) 컨테이너로 공개/개인 키 쌍을 가져오는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="efa49-110">Use the [ICLRStrongName::StrongNameKeyInstall](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeyinstall-method.md) method to import a public/private key pair into a container.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="efa49-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="efa49-111">Requirements</span></span>  
 <span data-ttu-id="efa49-112">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="efa49-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="efa49-113">**헤더:** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="efa49-113">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="efa49-114">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="efa49-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="efa49-115">**.NET Framework 버전:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="efa49-115">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="efa49-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="efa49-116">See Also</span></span>  
 [<span data-ttu-id="efa49-117">StrongNameKeyInstall 메서드</span><span class="sxs-lookup"><span data-stu-id="efa49-117">StrongNameKeyInstall Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeyinstall-method.md)  
 [<span data-ttu-id="efa49-118">ICLRStrongName 인터페이스</span><span class="sxs-lookup"><span data-stu-id="efa49-118">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
