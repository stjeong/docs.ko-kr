---
title: SqlStreamChars.IsNull 속성 (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/19/2018
ms.technology:
- dotnet-data
api_name:
- System.Data.SqlTypes.SqlStreamChars.IsNull
- System.Data.SqlTypes.SqlStreamChars.get_IsNull
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 79ebb9ec54185a94cb95dfd0fb2929e61cf513ef
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152626"
---
# <a name="sqlstreamcharsisnull-property"></a><span data-ttu-id="ff076-102">SqlStreamChars.IsNull 속성</span><span class="sxs-lookup"><span data-stu-id="ff076-102">SqlStreamChars.IsNull Property</span></span>

<span data-ttu-id="ff076-103">파생된 클래스에서 재정의 되 면 스트림 인지 여부를 나타내는 값을 가져옵니다 `null`합니다.</span><span class="sxs-lookup"><span data-stu-id="ff076-103">When overridden in a derived class, gets a value that indicates whether the stream is `null`.</span></span> <span data-ttu-id="ff076-104">이 속성을 포함 하는 어셈블리에는 SQLAccess.dll friend 관계를 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="ff076-104">The assembly that contains this property has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="ff076-105">SQL Server에서 사용할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ff076-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="ff076-106">다른 데이터베이스에 대 한 해당 데이터베이스에서 제공 하는 호스팅 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff076-106">For other databases, use the hosting mechanism provided by that database.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff076-107">구문</span><span class="sxs-lookup"><span data-stu-id="ff076-107">Syntax</span></span>

```csharp
public abstract bool IsNull { get; }
```

## <a name="property-value"></a><span data-ttu-id="ff076-108">속성 값</span><span class="sxs-lookup"><span data-stu-id="ff076-108">Property value</span></span>

<xref:System.Boolean>\
<span data-ttu-id="ff076-109">`true` 스트림이 `null`이 고, 그렇지 않으면 `false`합니다.</span><span class="sxs-lookup"><span data-stu-id="ff076-109">`true` if the stream is `null`; otherwise, `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff076-110">설명</span><span class="sxs-lookup"><span data-stu-id="ff076-110">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="ff076-111">`SqlStreamChars.IsNull` 속성은 전용 이며 코드에서 직접 사용할 하려고 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff076-111">The `SqlStreamChars.IsNull` property is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="ff076-112">Microsoft는 어떤 상황에서 프로덕션 응용 프로그램에서이 필드의 사용을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff076-112">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff076-113">요구 사항</span><span class="sxs-lookup"><span data-stu-id="ff076-113">Requirements</span></span>

<span data-ttu-id="ff076-114">**네임스페이스:** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="ff076-114">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="ff076-115">**어셈블리:** System.Data (System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="ff076-115">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="ff076-116">**.NET framework 버전:** 2.0부터 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ff076-116">**.NET Framework versions:** Available since 2.0.</span></span>