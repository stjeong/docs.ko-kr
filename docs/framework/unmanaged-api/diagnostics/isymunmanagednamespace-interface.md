---
title: ISymUnmanagedNamespace 인터페이스
ms.date: 03/30/2017
api_name:
- ISymUnmanagedNamespace
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedNamespace
helpviewer_keywords:
- ISymUnmanagedNamespace interface [.NET Framework debugging]
ms.assetid: d42bea4e-5848-4e43-a883-69af7a313ce9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bb5a833f7d6ed8f681f1f8d7ae79ac6113b8f2bf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54744377"
---
# <a name="isymunmanagednamespace-interface"></a><span data-ttu-id="f1b39-102">ISymUnmanagedNamespace 인터페이스</span><span class="sxs-lookup"><span data-stu-id="f1b39-102">ISymUnmanagedNamespace Interface</span></span>
<span data-ttu-id="f1b39-103">네임스페이스를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f1b39-103">Represents a namespace.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f1b39-104">메서드</span><span class="sxs-lookup"><span data-stu-id="f1b39-104">Methods</span></span>  
  
|<span data-ttu-id="f1b39-105">메서드</span><span class="sxs-lookup"><span data-stu-id="f1b39-105">Method</span></span>|<span data-ttu-id="f1b39-106">설명</span><span class="sxs-lookup"><span data-stu-id="f1b39-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f1b39-107">GetName 메서드</span><span class="sxs-lookup"><span data-stu-id="f1b39-107">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagednamespace-getname-method.md)|<span data-ttu-id="f1b39-108">이 네임 스페이스의 이름을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1b39-108">Gets the name of this namespace.</span></span>|  
|[<span data-ttu-id="f1b39-109">GetNamespaces 메서드</span><span class="sxs-lookup"><span data-stu-id="f1b39-109">GetNamespaces Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagednamespace-getnamespaces-method.md)|<span data-ttu-id="f1b39-110">이 네임 스페이스의 자식을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1b39-110">Gets the children of this namespace.</span></span>|  
|[<span data-ttu-id="f1b39-111">GetVariables 메서드</span><span class="sxs-lookup"><span data-stu-id="f1b39-111">GetVariables Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagednamespace-getvariables-method.md)|<span data-ttu-id="f1b39-112">이 네임 스페이스 내에서 전역 범위에서 정의 된 모든 변수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1b39-112">Returns all variables defined at global scope within this namespace.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f1b39-113">요구 사항</span><span class="sxs-lookup"><span data-stu-id="f1b39-113">Requirements</span></span>  
 <span data-ttu-id="f1b39-114">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="f1b39-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f1b39-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="f1b39-115">See also</span></span>
- [<span data-ttu-id="f1b39-116">진단 기호 저장소 인터페이스</span><span class="sxs-lookup"><span data-stu-id="f1b39-116">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
