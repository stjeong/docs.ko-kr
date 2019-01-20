---
title: CLRDATA_ADDRESS_RANGE 구조
ms.date: 01/16/2019
api.name:
- CLRDATA_ADDRESS_RANGE Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- CLRDATA_ADDRESS_RANGE Structure
helpviewer.keywords:
- CLRDATA_ADDRESS_RANGE Structure [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 3a8832a0eb173da00715bd0441b7efd337eae932
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416543"
---
# <a name="clrdataaddressrange-structure"></a><span data-ttu-id="1b413-102">CLRDATA_ADDRESS_RANGE 구조</span><span class="sxs-lookup"><span data-stu-id="1b413-102">CLRDATA_ADDRESS_RANGE Structure</span></span>

<span data-ttu-id="1b413-103">주소 범위를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="1b413-103">Defines an address range.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="1b413-104">구문</span><span class="sxs-lookup"><span data-stu-id="1b413-104">Syntax</span></span>

```
typedef struct
{
    CLRDATA_ADDRESS startAddress;
    CLRDATA_ADDRESS endAddress;
} CLRDATA_ADDRESS_RANGE;
```

## <a name="members"></a><span data-ttu-id="1b413-105">멤버</span><span class="sxs-lookup"><span data-stu-id="1b413-105">Members</span></span>

| <span data-ttu-id="1b413-106">멤버</span><span class="sxs-lookup"><span data-stu-id="1b413-106">Member</span></span>         | <span data-ttu-id="1b413-107">설명</span><span class="sxs-lookup"><span data-stu-id="1b413-107">Description</span></span>                     |
| -------------- | ------------------------------- |
| `startAddress` | <span data-ttu-id="1b413-108">범위의 시작 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="1b413-108">The start address of the range.</span></span> |
| `endAddress`   | <span data-ttu-id="1b413-109">범위의 끝 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="1b413-109">The end address of the range.</span></span>   |

## <a name="remarks"></a><span data-ttu-id="1b413-110">설명</span><span class="sxs-lookup"><span data-stu-id="1b413-110">Remarks</span></span>

<span data-ttu-id="1b413-111">이 구조는 런타임 내에서 있으며 모든 헤더 또는 라이브러리 파일을 통해 노출 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b413-111">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="1b413-112">를 사용 하려면 구조를 정의 위에 지정 된 대로 위치 `CLRDATA_ADDRESS` 는 64 비트 부호 없는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="1b413-112">To use it, define the structure as specified above, where `CLRDATA_ADDRESS` is a 64-bit unsigned integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b413-113">요구 사항</span><span class="sxs-lookup"><span data-stu-id="1b413-113">Requirements</span></span>

<span data-ttu-id="1b413-114">**플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="1b413-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="1b413-115">**헤더:** 없음</span><span class="sxs-lookup"><span data-stu-id="1b413-115">**Header:** None</span></span>  
<span data-ttu-id="1b413-116">**라이브러리:** 없음</span><span class="sxs-lookup"><span data-stu-id="1b413-116">**Library:** None</span></span>  
<span data-ttu-id="1b413-117">**.NET Framework 버전:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="1b413-117">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="1b413-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1b413-118">See Also</span></span>

- [<span data-ttu-id="1b413-119">디버깅</span><span class="sxs-lookup"><span data-stu-id="1b413-119">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="1b413-120">디버깅 구조체</span><span class="sxs-lookup"><span data-stu-id="1b413-120">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
