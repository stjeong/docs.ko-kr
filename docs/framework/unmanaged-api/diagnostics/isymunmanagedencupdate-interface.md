---
title: ISymUnmanagedENCUpdate 인터페이스
ms.date: 03/30/2017
api_name:
- ISymUnmanagedENCUpdate
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedENCUpdate
helpviewer_keywords:
- ISymUnmanagedENCUpdate interface [.NET Framework debugging]
ms.assetid: 63a9ef45-01a6-46da-b958-5c6dc2dc232c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 634716b36a0e5826cd7667a9ae948e8172724a1e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54630868"
---
# <a name="isymunmanagedencupdate-interface"></a><span data-ttu-id="8ce34-102">ISymUnmanagedENCUpdate 인터페이스</span><span class="sxs-lookup"><span data-stu-id="8ce34-102">ISymUnmanagedENCUpdate Interface</span></span>
<span data-ttu-id="8ce34-103">편집 하며 계속 하기 기능에 대 한 함수를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="8ce34-103">Provides functions for the Edit and Continue feature.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8ce34-104">메서드</span><span class="sxs-lookup"><span data-stu-id="8ce34-104">Methods</span></span>  
  
|<span data-ttu-id="8ce34-105">메서드</span><span class="sxs-lookup"><span data-stu-id="8ce34-105">Method</span></span>|<span data-ttu-id="8ce34-106">설명</span><span class="sxs-lookup"><span data-stu-id="8ce34-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8ce34-107">GetLocalVariableCount 메서드</span><span class="sxs-lookup"><span data-stu-id="8ce34-107">GetLocalVariableCount Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-getlocalvariablecount-method.md)|<span data-ttu-id="8ce34-108">지역 변수의 수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ce34-108">Gets the number of local variables.</span></span>|  
|[<span data-ttu-id="8ce34-109">GetLocalVariables 메서드</span><span class="sxs-lookup"><span data-stu-id="8ce34-109">GetLocalVariables Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-getlocalvariables-method.md)|<span data-ttu-id="8ce34-110">지역 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ce34-110">Gets the local variables.</span></span>|  
|[<span data-ttu-id="8ce34-111">InitializeForEnc 메서드</span><span class="sxs-lookup"><span data-stu-id="8ce34-111">InitializeForEnc Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-initializeforenc-method.md)|<span data-ttu-id="8ce34-112">첫 번째 호출 하기 전에 계산 메서드 경계를 허용 합니다 [ISymUnmanagedENCUpdate::UpdateSymbolStore2](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-updatesymbolstore2-method.md) 메서드.</span><span class="sxs-lookup"><span data-stu-id="8ce34-112">Allows method boundaries to be computed before the first call to the [ISymUnmanagedENCUpdate::UpdateSymbolStore2](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-updatesymbolstore2-method.md) method.</span></span>|  
|[<span data-ttu-id="8ce34-113">UpdateMethodLines 메서드</span><span class="sxs-lookup"><span data-stu-id="8ce34-113">UpdateMethodLines Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-updatemethodlines-method.md)|<span data-ttu-id="8ce34-114">컴파일되지 않은, 하지만 해당 줄 독립적으로 이동 하는 방법에 대 한 줄 정보를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ce34-114">Allows updating the line information for a method that has not been recompiled, but whose lines have moved independently.</span></span> <span data-ttu-id="8ce34-115">각 문에 대 한 델타 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ce34-115">A delta for each statement is allowed.</span></span>|  
|[<span data-ttu-id="8ce34-116">UpdateSymbolStore2 메서드</span><span class="sxs-lookup"><span data-stu-id="8ce34-116">UpdateSymbolStore2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-updatesymbolstore2-method.md)|<span data-ttu-id="8ce34-117">컴파일러를 줄 정보를 요구 사항을 충족 된 프로그램 데이터베이스 (PDB) 스트림, 수정 되지 않은 함수를 생략할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ce34-117">Allows a compiler to omit functions that have not been modified from the program database (PDB) stream, provided that the line information meets the requirements.</span></span> <span data-ttu-id="8ce34-118">이전 PDB 줄 정보를 및 모든 줄은 함수에 대 한 델타를 사용 하 여 올바른 줄 정보를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ce34-118">The correct line information can be determined with the old PDB line information and one delta for all lines in the function.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="8ce34-119">요구 사항</span><span class="sxs-lookup"><span data-stu-id="8ce34-119">Requirements</span></span>  
 <span data-ttu-id="8ce34-120">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="8ce34-120">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8ce34-121">참고자료</span><span class="sxs-lookup"><span data-stu-id="8ce34-121">See also</span></span>
- [<span data-ttu-id="8ce34-122">진단 기호 저장소 인터페이스</span><span class="sxs-lookup"><span data-stu-id="8ce34-122">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
