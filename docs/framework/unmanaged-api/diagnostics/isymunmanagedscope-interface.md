---
title: ISymUnmanagedScope 인터페이스
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope
helpviewer_keywords:
- ISymUnmanagedScope interface [.NET Framework debugging]
ms.assetid: 3db7a220-cfe9-4810-8ca8-a094bb8e0f5b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 965e8058d44ebb5dc87ade3b6025c6291a9c3bcd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54492129"
---
# <a name="isymunmanagedscope-interface"></a><span data-ttu-id="f5f6e-102">ISymUnmanagedScope 인터페이스</span><span class="sxs-lookup"><span data-stu-id="f5f6e-102">ISymUnmanagedScope Interface</span></span>
<span data-ttu-id="f5f6e-103">메서드 내에서 어휘 범위를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f5f6e-103">Represents a lexical scope within a method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f5f6e-104">메서드</span><span class="sxs-lookup"><span data-stu-id="f5f6e-104">Methods</span></span>  
  
|<span data-ttu-id="f5f6e-105">메서드</span><span class="sxs-lookup"><span data-stu-id="f5f6e-105">Method</span></span>|<span data-ttu-id="f5f6e-106">설명</span><span class="sxs-lookup"><span data-stu-id="f5f6e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f5f6e-107">GetChildren 메서드</span><span class="sxs-lookup"><span data-stu-id="f5f6e-107">GetChildren Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getchildren-method.md)|<span data-ttu-id="f5f6e-108">이 범위의 자식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5f6e-108">Gets the children of this scope.</span></span>|  
|[<span data-ttu-id="f5f6e-109">GetEndOffset 메서드</span><span class="sxs-lookup"><span data-stu-id="f5f6e-109">GetEndOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getendoffset-method.md)|<span data-ttu-id="f5f6e-110">이 범위의 끝 오프셋을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5f6e-110">Gets the end offset for this scope.</span></span>|  
|[<span data-ttu-id="f5f6e-111">GetLocalCount 메서드</span><span class="sxs-lookup"><span data-stu-id="f5f6e-111">GetLocalCount Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getlocalcount-method.md)|<span data-ttu-id="f5f6e-112">이 범위 내에 정의 된 로컬 변수 수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5f6e-112">Gets a count of the local variables defined within this scope.</span></span>|  
|[<span data-ttu-id="f5f6e-113">GetLocals 메서드</span><span class="sxs-lookup"><span data-stu-id="f5f6e-113">GetLocals Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getlocals-method.md)|<span data-ttu-id="f5f6e-114">이 범위 내에 정의 된 로컬 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5f6e-114">Gets the local variables defined within this scope.</span></span>|  
|[<span data-ttu-id="f5f6e-115">GetMethod 메서드</span><span class="sxs-lookup"><span data-stu-id="f5f6e-115">GetMethod Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getmethod-method.md)|<span data-ttu-id="f5f6e-116">이 범위를 포함 하는 메서드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5f6e-116">Gets the method that contains this scope.</span></span>|  
|[<span data-ttu-id="f5f6e-117">GetNamespaces 메서드</span><span class="sxs-lookup"><span data-stu-id="f5f6e-117">GetNamespaces Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getnamespaces-method.md)|<span data-ttu-id="f5f6e-118">이 범위 내에서 사용 되 고 있는 네임 스페이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5f6e-118">Gets the namespaces that are being used within this scope.</span></span>|  
|[<span data-ttu-id="f5f6e-119">GetParent 메서드</span><span class="sxs-lookup"><span data-stu-id="f5f6e-119">GetParent Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getparent-method.md)|<span data-ttu-id="f5f6e-120">이 범위의 상위 범위를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5f6e-120">Gets the parent scope of this scope.</span></span>|  
|[<span data-ttu-id="f5f6e-121">GetStartOffset 메서드</span><span class="sxs-lookup"><span data-stu-id="f5f6e-121">GetStartOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getstartoffset-method.md)|<span data-ttu-id="f5f6e-122">이 범위에 대 한 시작 오프셋을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5f6e-122">Gets the start offset for this scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f5f6e-123">요구 사항</span><span class="sxs-lookup"><span data-stu-id="f5f6e-123">Requirements</span></span>  
 <span data-ttu-id="f5f6e-124">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="f5f6e-124">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f5f6e-125">참고자료</span><span class="sxs-lookup"><span data-stu-id="f5f6e-125">See also</span></span>
- [<span data-ttu-id="f5f6e-126">진단 기호 저장소 인터페이스</span><span class="sxs-lookup"><span data-stu-id="f5f6e-126">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="f5f6e-127">ISymUnmanagedScope2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="f5f6e-127">ISymUnmanagedScope2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope2-interface.md)
