---
title: SetAssemblyFile 메서드
ms.date: 03/30/2017
api_name:
- IALink.SetAssemblyFile
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- SetAssemblyFile
helpviewer_keywords:
- SetAssemblyFile method
ms.assetid: 3a912787-f139-43ca-a841-8bbda3107ecf
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 006360203518f74adb964634af52505a71d51473
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54587101"
---
# <a name="setassemblyfile-method"></a><span data-ttu-id="f4f85-102">SetAssemblyFile 메서드</span><span class="sxs-lookup"><span data-stu-id="f4f85-102">SetAssemblyFile Method</span></span>
<span data-ttu-id="f4f85-103">만들려는 어셈블리의 이름을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f85-103">Assigns the name of the assembly to be built.</span></span> <span data-ttu-id="f4f85-104">바인딩되지 않은 모듈에 생성 때 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f4f85-104">Not for use when producing unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f4f85-105">구문</span><span class="sxs-lookup"><span data-stu-id="f4f85-105">Syntax</span></span>  
  
```  
HRESULT SetAssemblyFile(  
    LPCWSTR pszFilename,  
    IMetaDataEmit* pEmitter,  
    AssemblyFlags afFlags,  
    mdAssembly* pAssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f4f85-106">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f4f85-106">Parameters</span></span>  
 `pszFilename`  
 <span data-ttu-id="f4f85-107">매니페스트 파일의 정규화 된 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4f85-107">Fully qualified name of the manifest file.</span></span>  
  
 `pEmitter`  
 <span data-ttu-id="f4f85-108">에 대 한 포인터 [IMetaDataEmit 인터페이스](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md) 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="f4f85-108">Pointer to [IMetaDataEmit Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md) interface.</span></span>  
  
 `afFlags`  
 <span data-ttu-id="f4f85-109">에 정의 된 플래그 [AssemblyFlags 열거형](../../../../docs/framework/unmanaged-api/metadata/assemblyflags-enumeration.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f85-109">Flags as defined in [AssemblyFlags Enumeration](../../../../docs/framework/unmanaged-api/metadata/assemblyflags-enumeration.md).</span></span>  
  
 `pAssemblyID`  
 <span data-ttu-id="f4f85-110">결과 어셈블리의 ID에 대 한 포인터입니다.</span><span class="sxs-lookup"><span data-stu-id="f4f85-110">Pointer to ID of resulting assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f4f85-111">반환 값</span><span class="sxs-lookup"><span data-stu-id="f4f85-111">Return Value</span></span>  
 <span data-ttu-id="f4f85-112">메서드가 성공 하면 S_OK를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f85-112">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f4f85-113">요구 사항</span><span class="sxs-lookup"><span data-stu-id="f4f85-113">Requirements</span></span>  
 <span data-ttu-id="f4f85-114">Alink.h가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f85-114">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f4f85-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="f4f85-115">See also</span></span>
- [<span data-ttu-id="f4f85-116">IALink 인터페이스</span><span class="sxs-lookup"><span data-stu-id="f4f85-116">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="f4f85-117">IALink2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="f4f85-117">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="f4f85-118">ALink API</span><span class="sxs-lookup"><span data-stu-id="f4f85-118">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
