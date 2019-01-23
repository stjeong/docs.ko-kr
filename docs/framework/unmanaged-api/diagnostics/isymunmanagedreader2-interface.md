---
title: ISymUnmanagedReader2 인터페이스
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader2
helpviewer_keywords:
- ISymUnmanagedReader2 interface [.NET Framework debugging]
ms.assetid: a01a881b-82a3-4b3e-a3a9-9dc305c2e5f7
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a08695c4e5df6aaa63bedecf68b741302e5ddd8e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54524945"
---
# <a name="isymunmanagedreader2-interface"></a><span data-ttu-id="9f41b-102">ISymUnmanagedReader2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9f41b-102">ISymUnmanagedReader2 Interface</span></span>
<span data-ttu-id="9f41b-103">문서, 메서드 및 기호 저장소 내의 변수에 대 한 액세스를 제공 하는 기호 판독기를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9f41b-103">Represents a symbol reader that provides access to documents, methods, and variables within a symbol store.</span></span> <span data-ttu-id="9f41b-104">이 인터페이스를 확장 합니다 [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="9f41b-104">This interface extends the [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="9f41b-105">메서드</span><span class="sxs-lookup"><span data-stu-id="9f41b-105">Methods</span></span>  
  
|<span data-ttu-id="9f41b-106">메서드</span><span class="sxs-lookup"><span data-stu-id="9f41b-106">Method</span></span>|<span data-ttu-id="9f41b-107">설명</span><span class="sxs-lookup"><span data-stu-id="9f41b-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="9f41b-108">GetMethodByVersionPreRemap 메서드</span><span class="sxs-lookup"><span data-stu-id="9f41b-108">GetMethodByVersionPreRemap Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-getmethodbyversionpreremap-method.md)|<span data-ttu-id="9f41b-109">지정 된 메서드 토큰 및 편집 하며 계속 하기 버전 번호를 기호 판독기 메서드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9f41b-109">Get a symbol reader method, given a method token and an edit-and-continue version number.</span></span>|  
|[<span data-ttu-id="9f41b-110">GetMethodsInDocument 메서드</span><span class="sxs-lookup"><span data-stu-id="9f41b-110">GetMethodsInDocument Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-getmethodsindocument-method.md)|<span data-ttu-id="9f41b-111">제공 된 문서의 줄 정보가 있는 모든 메서드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9f41b-111">Gets every method that has line information in the provided document.</span></span>|  
|[<span data-ttu-id="9f41b-112">GetSymAttributePreRemap 메서드</span><span class="sxs-lookup"><span data-stu-id="9f41b-112">GetSymAttributePreRemap Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-getsymattributepreremap-method.md)|<span data-ttu-id="9f41b-113">해당 이름을 기준으로 사용자 지정 특성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9f41b-113">Gets a custom attribute based upon its name.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9f41b-114">요구 사항</span><span class="sxs-lookup"><span data-stu-id="9f41b-114">Requirements</span></span>  
 <span data-ttu-id="9f41b-115">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="9f41b-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f41b-116">참고자료</span><span class="sxs-lookup"><span data-stu-id="9f41b-116">See also</span></span>
- [<span data-ttu-id="9f41b-117">진단 기호 저장소 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9f41b-117">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="9f41b-118">ISymUnmanagedReader 인터페이스</span><span class="sxs-lookup"><span data-stu-id="9f41b-118">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
