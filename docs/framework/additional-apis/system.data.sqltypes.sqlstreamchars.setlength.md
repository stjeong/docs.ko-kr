---
title: SqlStreamChars.SetLength(Int64) 메서드 (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/20/2018
ms.technology:
- dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.SetLength
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: c7199cbd08e62b1f0391437a0c1864cb9036fe1f
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54222703"
---
# <a name="sqlstreamcharssetlengthint64-method"></a><span data-ttu-id="378d3-102">SqlStreamChars.SetLength(Int64) 메서드</span><span class="sxs-lookup"><span data-stu-id="378d3-102">SqlStreamChars.SetLength(Int64) Method</span></span>

<span data-ttu-id="378d3-103">파생된 클래스에서 재정의 되 면 스트림을 사용 하는 리소스를 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d3-103">When overridden in a derived class, releases the resources used by the stream.</span></span> <span data-ttu-id="378d3-104">이 메서드를 포함 하는 어셈블리에는 SQLAccess.dll friend 관계를 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="378d3-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="378d3-105">SQL Server에서 사용할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="378d3-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="378d3-106">다른 데이터베이스에 대 한 해당 데이터베이스에서 제공 하는 호스팅 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d3-106">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public abstract void SetLength (long value);
```

## <a name="parameters"></a><span data-ttu-id="378d3-107">매개 변수</span><span class="sxs-lookup"><span data-stu-id="378d3-107">Parameters</span></span>

`value`\
<span data-ttu-id="378d3-108">원하는 현재 스트림의 길이(바이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="378d3-108">The desired length of the current stream in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="378d3-109">설명</span><span class="sxs-lookup"><span data-stu-id="378d3-109">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="378d3-110">`SqlStreamChars.SetLength` 메서드가 private 이며 코드에서 직접 사용할 하려고 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="378d3-110">The `SqlStreamChars.SetLength` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="378d3-111">Microsoft는 어떤 상황에서 프로덕션 응용 프로그램에서이 필드의 사용을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="378d3-111">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="378d3-112">요구 사항</span><span class="sxs-lookup"><span data-stu-id="378d3-112">Requirements</span></span>

<span data-ttu-id="378d3-113">**네임스페이스:** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="378d3-113">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="378d3-114">**어셈블리:** System.Data (System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="378d3-114">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="378d3-115">**.NET framework 버전:** 2.0부터 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="378d3-115">**.NET Framework versions:** Available since 2.0.</span></span>