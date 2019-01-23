---
title: ICorProfilerInfo7 인터페이스
ms.date: 03/30/2017
ms.assetid: cf37c462-73c5-412a-a7f8-bb26ca746313
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c33e620b861f1065f95ba9f1f732911723c16f88
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54526277"
---
# <a name="icorprofilerinfo7-interface"></a><span data-ttu-id="63302-102">ICorProfilerInfo7 인터페이스</span><span class="sxs-lookup"><span data-stu-id="63302-102">ICorProfilerInfo7 Interface</span></span>
<span data-ttu-id="63302-103">[[!INCLUDE[net_v461](../../../../includes/net-v461-md.md)] 이상 버전에서 지원됨]</span><span class="sxs-lookup"><span data-stu-id="63302-103">[Supported in the [!INCLUDE[net_v461](../../../../includes/net-v461-md.md)] and later versions]</span></span>  
  
 <span data-ttu-id="63302-104">서브 클래스 [ICorProfilerInfo6](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo6-interface.md) 모듈에 정의 된 메타 데이터가 새로 적용 하는 메서드 및 메모리 내 기호 스트림에 대 한 액세스를 제공 하는 제공 하는 합니다.</span><span class="sxs-lookup"><span data-stu-id="63302-104">A subclass of [ICorProfilerInfo6](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo6-interface.md) that provides a method to apply newly defined metadata to a module and that provides access to an in-memory symbol stream.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="63302-105">메서드</span><span class="sxs-lookup"><span data-stu-id="63302-105">Methods</span></span>  
  
|<span data-ttu-id="63302-106">메서드</span><span class="sxs-lookup"><span data-stu-id="63302-106">Method</span></span>|<span data-ttu-id="63302-107">설명</span><span class="sxs-lookup"><span data-stu-id="63302-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="63302-108">ApplyMetaData 메서드</span><span class="sxs-lookup"><span data-stu-id="63302-108">ApplyMetaData Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-applymetadata-method.md)|<span data-ttu-id="63302-109">새로 정의한 메타 데이터를 적용 합니다 `IMetadataEmit::Define*` 지정된 된 모듈에는 메서드.</span><span class="sxs-lookup"><span data-stu-id="63302-109">Applies the metadata newly defined by the `IMetadataEmit::Define*` methods to a specified module.</span></span>|  
|[<span data-ttu-id="63302-110">GetInMemorySymbolsLength 메서드</span><span class="sxs-lookup"><span data-stu-id="63302-110">GetInMemorySymbolsLength Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-getinmemorysymbolslength-method.md)|<span data-ttu-id="63302-111">메모리 내 기호 스트림의 길이 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="63302-111">Returns the length of an in-memory symbol stream.</span></span>|  
|[<span data-ttu-id="63302-112">ReadInMemorySymbols</span><span class="sxs-lookup"><span data-stu-id="63302-112">ReadInMemorySymbols</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-readinmemorysymbols.md)|<span data-ttu-id="63302-113">메모리 내 기호 스트림에서 바이트를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="63302-113">Reads bytes from an in-memory symbol stream.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="63302-114">요구 사항</span><span class="sxs-lookup"><span data-stu-id="63302-114">Requirements</span></span>  
 <span data-ttu-id="63302-115">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="63302-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="63302-116">**헤더:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="63302-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="63302-117">**.NET Framework 버전:** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="63302-117">**.NET Framework Versions:** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="63302-118">참고자료</span><span class="sxs-lookup"><span data-stu-id="63302-118">See also</span></span>
- [<span data-ttu-id="63302-119">프로파일링 인터페이스</span><span class="sxs-lookup"><span data-stu-id="63302-119">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
