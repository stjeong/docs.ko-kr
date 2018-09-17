---
title: lock 문(C# 참조)
description: C# lock 문을 사용하여 공유 리소스에 대한 스레드 액세스 동기화
ms.date: 08/28/2018
f1_keywords:
- lock_CSharpKeyword
- lock
helpviewer_keywords:
- lock keyword [C#]
ms.assetid: 656da1a4-707e-4ef6-9c6e-6d13b646af42
ms.openlocfilehash: 2b6fbfb2f81d7745c4effb9ea0087f34cc872a6c
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43858358"
---
# <a name="lock-statement-c-reference"></a><span data-ttu-id="0acde-103">lock 문(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="0acde-103">lock statement (C# Reference)</span></span>

<span data-ttu-id="0acde-104">`lock` 문은 지정된 개체에 대한 상호 배제 잠금을 가져와서 명령문 블록을 실행한 다음, 잠금을 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="0acde-104">The `lock` statement obtains the mutual-exclusion lock for a given object, executes a statement block, and then releases the lock.</span></span> <span data-ttu-id="0acde-105">잠금이 유지되는 동안 잠금을 보유하는 스레드는 잠금을 다시 가져오고 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0acde-105">While a lock is held, the thread that holds the lock can again obtain and release the lock.</span></span> <span data-ttu-id="0acde-106">다른 스레드는 잠금을 가져올 수 없도록 차단되며 잠금이 해제될 때까지 대기합니다.</span><span class="sxs-lookup"><span data-stu-id="0acde-106">Any other thread is blocked from obtaining the lock and waits until the lock is released.</span></span>

<span data-ttu-id="0acde-107">`lock` 문이 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="0acde-107">The `lock` statement is of the form</span></span>

```csharp
lock (x)
{
    // Your code...
}
```

<span data-ttu-id="0acde-108">여기서 `x`는 [참조 형식](reference-types.md)의 식입니다.</span><span class="sxs-lookup"><span data-stu-id="0acde-108">where `x` is an expression of a [reference type](reference-types.md).</span></span> <span data-ttu-id="0acde-109">정확히 다음과 같은 경우</span><span class="sxs-lookup"><span data-stu-id="0acde-109">It's precisely equivalent to</span></span>

```csharp
object __lockObj = x;
bool __lockWasTaken = false;
try
{
    System.Threading.Monitor.Enter(__lockObj, ref __lockWasTaken);
    // Your code...
}
finally
{
    if (__lockWasTaken) System.Threading.Monitor.Exit(__lockObj);
}
```

<span data-ttu-id="0acde-110">코드에서 [try...finally](try-finally.md) 블록을 사용하므로 `lock` 문의 본문 내에서 예외가 throw되더라도 잠금이 해제됩니다.</span><span class="sxs-lookup"><span data-stu-id="0acde-110">Since the code uses a [try...finally](try-finally.md) block, the lock is released even if an exception is thrown within the body of a `lock` statement.</span></span>

<span data-ttu-id="0acde-111">`lock` 문의 본문에서 [await](await.md) 키워드를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0acde-111">You can't use the [await](await.md) keyword in the body of a `lock` statement.</span></span>

## <a name="remarks"></a><span data-ttu-id="0acde-112">설명</span><span class="sxs-lookup"><span data-stu-id="0acde-112">Remarks</span></span>

<span data-ttu-id="0acde-113">공유 리소스에스 레드 엑세스를 동기화하는 경우 전용 개체 인스턴스(예: `private readonly object balanceLock = new object();`) 또는 코드의 관련 없는 부분에서 잠금 개체로 사용되지 않을 가능성이 있는 다른 인스턴스에서 잠급니다.</span><span class="sxs-lookup"><span data-stu-id="0acde-113">When you synchronize thread access to shared resource, lock on a dedicated object instance (for example, `private readonly object balanceLock = new object();`) or another instance that is unlikely to be used as a lock object by unrelated parts of the code.</span></span> <span data-ttu-id="0acde-114">교착 상태 또는 잠금 경합이 발생할 수 있으므로 다른 공유 리소스에 대해 동일한 잠금 개체 인스턴스를 사용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="0acde-114">Avoid using the same lock object instance for different shared resources, as it might result in deadlock or lock contention.</span></span> <span data-ttu-id="0acde-115">특히,</span><span class="sxs-lookup"><span data-stu-id="0acde-115">In particular, avoid using</span></span>

- <span data-ttu-id="0acde-116">`this`(호출자가 잠금으로 사용할 수 있음),</span><span class="sxs-lookup"><span data-stu-id="0acde-116">`this` (might be used by the callers as a lock),</span></span>
- <span data-ttu-id="0acde-117"><xref:System.Type> 인스턴스([typeof](typeof.md) 연산자 또는 리플렉션에서 가져올 수 있음),</span><span class="sxs-lookup"><span data-stu-id="0acde-117"><xref:System.Type> instances (might be obtained by the [typeof](typeof.md) operator or reflection),</span></span>
- <span data-ttu-id="0acde-118">문자열 인스턴스(문자열 리터럴 포함)의 경우,</span><span class="sxs-lookup"><span data-stu-id="0acde-118">string instances, including string literals,</span></span>

<span data-ttu-id="0acde-119">잠금 개체로 사용하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="0acde-119">as lock objects.</span></span>

## <a name="example"></a><span data-ttu-id="0acde-120">예</span><span class="sxs-lookup"><span data-stu-id="0acde-120">Example</span></span>

<span data-ttu-id="0acde-121">다음 예제에서는 전용 `balanceLock` 인스턴스에 잠금을 설정하여 해당 개인 `balance` 필드에 대한 액세스를 동기화하는 `Account` 클래스를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="0acde-121">The following example defines an `Account` class that synchronizes access to its private `balance` field by locking on a dedicated `balanceLock` instance.</span></span> <span data-ttu-id="0acde-122">동일한 인스턴스를 잠금에 사용하면 `Debit` 또는 `Credit` 메서드를 동시에 호출하려는 두 스레드에 의해 `balance` 필드가 동시에 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0acde-122">Using the same instance for locking ensures that the `balance` field cannot be updated simultaneously by two threads attempting to call the `Debit` or `Credit` methods simultaneously.</span></span>

[!code-csharp[lock-statement-example](~/samples/snippets/csharp/keywords/LockStatementExample.cs)]

## <a name="c-language-specification"></a><span data-ttu-id="0acde-123">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="0acde-123">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="0acde-124">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0acde-124">See also</span></span>

- <xref:System.Threading.Monitor?displayProperty=nameWithType>
- <xref:System.Threading.SpinLock?displayProperty=nameWithType>
- <xref:System.Threading.Interlocked?displayProperty=nameWithType>
- [<span data-ttu-id="0acde-125">C# 참조</span><span class="sxs-lookup"><span data-stu-id="0acde-125">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="0acde-126">C# 키워드</span><span class="sxs-lookup"><span data-stu-id="0acde-126">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="0acde-127">문 키워드</span><span class="sxs-lookup"><span data-stu-id="0acde-127">Statement Keywords</span></span>](statement-keywords.md)
- [<span data-ttu-id="0acde-128">연동 작업</span><span class="sxs-lookup"><span data-stu-id="0acde-128">Interlocked operations</span></span>](../../../standard/threading/interlocked-operations.md)
- [<span data-ttu-id="0acde-129">동기화 기본 형식 개요</span><span class="sxs-lookup"><span data-stu-id="0acde-129">Overview of synchronization primitives</span></span>](../../../standard/threading/overview-of-synchronization-primitives.md)