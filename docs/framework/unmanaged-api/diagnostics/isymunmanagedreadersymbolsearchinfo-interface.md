---
title: ISymUnmanagedReaderSymbolSearchInfo 인터페이스
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReaderSymbolSearchInfo
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReaderSymbolSearchInfo
helpviewer_keywords:
- ISymUnmanagedReaderSymbolSearchInfo interface [.NET Framework debugging]
ms.assetid: fde7e21d-1169-4bed-a34d-792e69652bf9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4a6eb99de44c2d3f1afe6dda2d6ec895ec57c617
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54635005"
---
# <a name="isymunmanagedreadersymbolsearchinfo-interface"></a><span data-ttu-id="fa254-102">ISymUnmanagedReaderSymbolSearchInfo 인터페이스</span><span class="sxs-lookup"><span data-stu-id="fa254-102">ISymUnmanagedReaderSymbolSearchInfo Interface</span></span>
<span data-ttu-id="fa254-103">기호 검색 정보를 가져오는 메서드를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa254-103">Provides methods that get symbol search information.</span></span> <span data-ttu-id="fa254-104">호출 하 여이 인터페이스를 가져올 `QueryInterface` 구현 하는 개체에는 [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="fa254-104">Obtain this interface by calling `QueryInterface` on an object that implements the [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="fa254-105">메서드</span><span class="sxs-lookup"><span data-stu-id="fa254-105">Methods</span></span>  
  
|<span data-ttu-id="fa254-106">메서드</span><span class="sxs-lookup"><span data-stu-id="fa254-106">Method</span></span>|<span data-ttu-id="fa254-107">설명</span><span class="sxs-lookup"><span data-stu-id="fa254-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="fa254-108">GetSymbolSearchInfo 메서드</span><span class="sxs-lookup"><span data-stu-id="fa254-108">GetSymbolSearchInfo Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreadersymbolsearchinfo-getsymbolsearchinfo-method.md)|<span data-ttu-id="fa254-109">기호 검색 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fa254-109">Gets symbol search information.</span></span>|  
|[<span data-ttu-id="fa254-110">GetSymbolSearchInfoCount 메서드</span><span class="sxs-lookup"><span data-stu-id="fa254-110">GetSymbolSearchInfoCount Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreadersymbolsearchinfo-getsymbolsearchinfocount-method.md)|<span data-ttu-id="fa254-111">정보를 검색 하는 기호 수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fa254-111">Gets a count of symbol search information.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="fa254-112">요구 사항</span><span class="sxs-lookup"><span data-stu-id="fa254-112">Requirements</span></span>  
 <span data-ttu-id="fa254-113">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="fa254-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa254-114">참고자료</span><span class="sxs-lookup"><span data-stu-id="fa254-114">See also</span></span>
- [<span data-ttu-id="fa254-115">진단 기호 저장소 인터페이스</span><span class="sxs-lookup"><span data-stu-id="fa254-115">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
