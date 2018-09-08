---
title: 지연 계산(F#)
description: 'F # 지연 계산 앱 및 라이브러리의 성능을 향상 시킬 수 있습니다 하는 방법에 대해 알아봅니다.'
ms.date: 05/16/2016
ms.openlocfilehash: 8afe815f26978de96291a52973d54a9dbcc5eaf2
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44201632"
---
# <a name="lazy-computations"></a><span data-ttu-id="affdb-103">지연 계산</span><span class="sxs-lookup"><span data-stu-id="affdb-103">Lazy Computations</span></span>

<span data-ttu-id="affdb-104">*지연 계산* 즉시 평가 되지 않습니다 하지만 결과가 필요한 경우 대신 평가 되는 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="affdb-104">*Lazy computations* are computations that are not evaluated immediately, but are instead evaluated when the result is needed.</span></span> <span data-ttu-id="affdb-105">이 코드의 성능을 향상 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="affdb-105">This can help to improve the performance of your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="affdb-106">구문</span><span class="sxs-lookup"><span data-stu-id="affdb-106">Syntax</span></span>

```fsharp
let identifier = lazy ( expression )
```

## <a name="remarks"></a><span data-ttu-id="affdb-107">설명</span><span class="sxs-lookup"><span data-stu-id="affdb-107">Remarks</span></span>

<span data-ttu-id="affdb-108">이전 구문에서 *식* 결과가 필요한 경우에 평가 되는 코드 및 *식별자* 결과 저장 하는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="affdb-108">In the previous syntax, *expression* is code that is evaluated only when a result is required, and *identifier* is a value that stores the result.</span></span> <span data-ttu-id="affdb-109">형식의 값이 [ `Lazy<'T>` ](https://msdn.microsoft.com/library/b29d0af5-6efb-4a55-a278-2662a4ecc489)여기서는 실제 형식은는 `'T` 식의 결과에서 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="affdb-109">The value is of type [`Lazy<'T>`](https://msdn.microsoft.com/library/b29d0af5-6efb-4a55-a278-2662a4ecc489), where the actual type that is used for `'T` is determined from the result of the expression.</span></span>

<span data-ttu-id="affdb-110">지연 계산을 사용 하면 결과가 필요할 때 해당 상황에만에 계산의 실행을 제한 하 여 성능을 향상 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="affdb-110">Lazy computations enable you to improve performance by restricting the execution of a computation to only those situations in which a result is needed.</span></span>

<span data-ttu-id="affdb-111">메서드를 호출 하면 수행할 계산을 적용할 `Force`합니다.</span><span class="sxs-lookup"><span data-stu-id="affdb-111">To force the computation to be performed, you call the method `Force`.</span></span> <span data-ttu-id="affdb-112">`Force` 한 번만 수행 하 고 실행을 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="affdb-112">`Force` causes the execution to be performed only one time.</span></span> <span data-ttu-id="affdb-113">에 대 한 후속 호출 `Force` 동일한 결과 실행 하지는 않습니다 모든 코드를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="affdb-113">Subsequent calls to `Force` return the same result, but do not execute any code.</span></span>

<span data-ttu-id="affdb-114">다음 코드에서는 지연 계산 사용 및 사용 `Force`합니다.</span><span class="sxs-lookup"><span data-stu-id="affdb-114">The following code illustrates the use of lazy computation and the use of `Force`.</span></span> <span data-ttu-id="affdb-115">이 코드에서 형식의 `result` 됩니다 `Lazy<int>`, 및 `Force` 메서드가 반환 되는 `int`.</span><span class="sxs-lookup"><span data-stu-id="affdb-115">In this code, the type of `result` is `Lazy<int>`, and the `Force` method returns an `int`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet73011.fs)]

<span data-ttu-id="affdb-116">지연 계산 하지 않고는 `Lazy` 입력, 시퀀스에도 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="affdb-116">Lazy evaluation, but not the `Lazy` type, is also used for sequences.</span></span> <span data-ttu-id="affdb-117">자세한 내용은 [시퀀스](sequences.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="affdb-117">For more information, see [Sequences](sequences.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="affdb-118">참고자료</span><span class="sxs-lookup"><span data-stu-id="affdb-118">See also</span></span>

- [<span data-ttu-id="affdb-119">F# 언어 참조</span><span class="sxs-lookup"><span data-stu-id="affdb-119">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="affdb-120">LazyExtensions 모듈</span><span class="sxs-lookup"><span data-stu-id="affdb-120">LazyExtensions module</span></span>](https://msdn.microsoft.com/library/86671f40-84a0-402a-867d-ae596218d948)
