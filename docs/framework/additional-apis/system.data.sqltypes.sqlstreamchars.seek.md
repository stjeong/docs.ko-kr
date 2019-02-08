---
title: SqlStreamChars.Seek (Int64, SeekOrigin) 메서드 (System.Data.SqlTypes)
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology:
- dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Seek
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: d52a1cd4dd70c29fc1af3fcf50c4f9b0c90125df
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55827385"
---
# <a name="sqlstreamcharsseekint64-seekorigin-method"></a><span data-ttu-id="565ea-102">(Int64, SeekOrigin) SqlStreamChars.Seek 메서드</span><span class="sxs-lookup"><span data-stu-id="565ea-102">SqlStreamChars.Seek(Int64, SeekOrigin) Method</span></span>

<span data-ttu-id="565ea-103">파생 클래스를 재정의될 때 현재 스트림 내의 위치를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="565ea-103">When overridden in a derived class, sets the position within the current stream.</span></span> <span data-ttu-id="565ea-104">이 메서드를 포함 하는 어셈블리에는 SQLAccess.dll friend 관계를 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="565ea-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="565ea-105">SQL Server에서 사용할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="565ea-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="565ea-106">다른 데이터베이스에 대 한 해당 데이터베이스에서 제공 하는 호스팅 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="565ea-106">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public abstract long Seek (long offset, System.IO.SeekOrigin origin);
```

## <a name="parameters"></a><span data-ttu-id="565ea-107">매개 변수</span><span class="sxs-lookup"><span data-stu-id="565ea-107">Parameters</span></span>

`offset`\
<span data-ttu-id="565ea-108">`origin`에 상대적인 바이트 오프셋입니다.</span><span class="sxs-lookup"><span data-stu-id="565ea-108">A byte offset relative to `origin`.</span></span>

`origin`\
<span data-ttu-id="565ea-109">새 위치를 가져올 참조 위치를 나타내는 열거형 값 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="565ea-109">One of the enumeration values that indicates the reference point from which to obtain the new position.</span></span>

## <a name="returns"></a><span data-ttu-id="565ea-110">반환 값</span><span class="sxs-lookup"><span data-stu-id="565ea-110">Returns</span></span>

<xref:System.Int32>\
<span data-ttu-id="565ea-111">현재 스트림 내의 새 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="565ea-111">The new position within the current stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="565ea-112">설명</span><span class="sxs-lookup"><span data-stu-id="565ea-112">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="565ea-113">`SqlStreamChars.Seek` 메서드가 private 이며 코드에서 직접 사용할 하려고 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="565ea-113">The `SqlStreamChars.Seek` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="565ea-114">Microsoft는 어떤 상황에서 프로덕션 응용 프로그램에서이 필드의 사용을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="565ea-114">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="565ea-115">요구 사항</span><span class="sxs-lookup"><span data-stu-id="565ea-115">Requirements</span></span>

<span data-ttu-id="565ea-116">**네임스페이스:** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="565ea-116">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="565ea-117">**어셈블리:** System.Data (System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="565ea-117">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="565ea-118">**.NET framework 버전:** 2.0부터 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="565ea-118">**.NET Framework versions:** Available since 2.0.</span></span>