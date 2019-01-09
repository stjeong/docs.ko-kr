---
title: SqlStreamChars.Write (Char, Int32, Int32) 메서드 (System.Data.SqlTypes)
author: douglaslMS
ms.author: douglasl
ms.date: 12/20/2018
ms.technology:
- dotnet-data
api_name:
- System.Data.SqlTypes.SqlStreamChars.Write
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: e8c8ee7ab7a744c1a1d18212f1c7f9788c91ea0d
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152576"
---
# <a name="sqlstreamcharswritechar-int32-int32-method"></a><span data-ttu-id="fccb2-102">(Char, Int32, Int32) SqlStreamChars.Write 메서드</span><span class="sxs-lookup"><span data-stu-id="fccb2-102">SqlStreamChars.Write(Char[], Int32, Int32) Method</span></span>

<span data-ttu-id="fccb2-103">파생된 클래스에서 재정의 문자의 시퀀스를 현재 스트림에 쓰고 쓴 문자 수 만큼이 스트림 내의 현재 위치를 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="fccb2-103">When overridden in a derived class, writes a sequence of characters to the current stream and advances the current position within this stream by the number of characters written.</span></span> <span data-ttu-id="fccb2-104">이 메서드를 포함 하는 어셈블리에는 SQLAccess.dll friend 관계를 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="fccb2-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="fccb2-105">SQL Server에서 사용할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fccb2-105">It's intended for use by SQL Server.</span></span> <span data-ttu-id="fccb2-106">다른 데이터베이스에 대 한 해당 데이터베이스에서 제공 하는 호스팅 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fccb2-106">For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public abstract void Write (char[] buffer, int offset, int count);
```

## <a name="parameters"></a><span data-ttu-id="fccb2-107">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fccb2-107">Parameters</span></span>

`buffer`  
<span data-ttu-id="fccb2-108">쓸 문자 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="fccb2-108">A char array to write.</span></span>

`offset`  
<span data-ttu-id="fccb2-109">원점 기준으로 하는 오프셋입니다.</span><span class="sxs-lookup"><span data-stu-id="fccb2-109">An offset relative to origin.</span></span>

`count`  
<span data-ttu-id="fccb2-110">현재 스트림에 쓸 문자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fccb2-110">The number of characters to be written to the current stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="fccb2-111">설명</span><span class="sxs-lookup"><span data-stu-id="fccb2-111">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="fccb2-112">`SqlStreamChars.Write` 메서드가 private 이며 코드에서 직접 사용할 하려고 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fccb2-112">The `SqlStreamChars.Write` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="fccb2-113">Microsoft는 어떤 상황에서 프로덕션 응용 프로그램에서이 필드의 사용을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fccb2-113">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="fccb2-114">요구 사항</span><span class="sxs-lookup"><span data-stu-id="fccb2-114">Requirements</span></span>

<span data-ttu-id="fccb2-115">**네임스페이스:** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="fccb2-115">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="fccb2-116">**어셈블리:** System.Data (System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="fccb2-116">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="fccb2-117">**.NET framework 버전:** 2.0부터 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fccb2-117">**.NET Framework versions:** Available since 2.0.</span></span>