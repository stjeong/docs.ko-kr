---
title: do 바인딩(F#)
description: "F # 'do' 바인딩에 사용법 함수 또는 값을 정의 하지 않고 코드를 실행할 수에 대해 알아봅니다."
ms.date: 05/16/2016
ms.openlocfilehash: 78dbf8da0fe40b5af566ad98693df1109eede7e4
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/13/2018
ms.locfileid: "45515849"
---
# <a name="do-bindings"></a><span data-ttu-id="d1ec1-103">do 바인딩</span><span class="sxs-lookup"><span data-stu-id="d1ec1-103">do Bindings</span></span>

<span data-ttu-id="d1ec1-104">`do` 함수 또는 값을 정의 하지 않고 코드를 실행 하려면 바인딩이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec1-104">A `do` binding is used to execute code without defining a function or value.</span></span> <span data-ttu-id="d1ec1-105">또한 수행 바인딩 수 있습니다 참조 클래스를 사용 [ `do` 클래스에 바인딩](../members/do-bindings-in-classes.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec1-105">Also, do bindings can be used in classes, see [`do` Bindings in Classes](../members/do-bindings-in-classes.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1ec1-106">구문</span><span class="sxs-lookup"><span data-stu-id="d1ec1-106">Syntax</span></span>

```fsharp
[ attributes ]
[ do ]expression
```

## <a name="remarks"></a><span data-ttu-id="d1ec1-107">설명</span><span class="sxs-lookup"><span data-stu-id="d1ec1-107">Remarks</span></span>

<span data-ttu-id="d1ec1-108">사용 된 `do` 함수 또는 값의 정의 의존 하지 않고 코드를 실행 하려는 경우 바인딩.</span><span class="sxs-lookup"><span data-stu-id="d1ec1-108">Use a `do` binding when you want to execute code independently of a function or value definition.</span></span> <span data-ttu-id="d1ec1-109">식에는 `do` 바인딩을 반환 해야 합니다 `unit`합니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec1-109">The expression in a `do` binding must return `unit`.</span></span> <span data-ttu-id="d1ec1-110">코드에서 최상위 `do` 바인딩 모듈 초기화 될 때 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec1-110">Code in a top-level `do` binding is executed when the module is initialized.</span></span> <span data-ttu-id="d1ec1-111">키워드 `do` 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec1-111">The keyword `do` is optional.</span></span>

<span data-ttu-id="d1ec1-112">최상위 수준에 특성을 적용할 수 있습니다 `do` 바인딩.</span><span class="sxs-lookup"><span data-stu-id="d1ec1-112">Attributes can be applied to a top-level `do` binding.</span></span> <span data-ttu-id="d1ec1-113">예를 들어, 프로그램 COM interop를 사용 하는 경우 적용할는 `STAThread` 프로그램 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="d1ec1-113">For example, if your program uses COM interop, you might want to apply the `STAThread` attribute to your program.</span></span> <span data-ttu-id="d1ec1-114">특성을 사용 하 여이 수행할 수는 `do` 다음 코드 에서처럼 바인딩.</span><span class="sxs-lookup"><span data-stu-id="d1ec1-114">You can do this by using an attribute on a `do` binding, as shown in the following code.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet201.fs)]

## <a name="see-also"></a><span data-ttu-id="d1ec1-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="d1ec1-115">See also</span></span>

- [<span data-ttu-id="d1ec1-116">F# 언어 참조</span><span class="sxs-lookup"><span data-stu-id="d1ec1-116">F# Language Reference</span></span>](../index.md)
- [<span data-ttu-id="d1ec1-117">함수</span><span class="sxs-lookup"><span data-stu-id="d1ec1-117">Functions</span></span>](index.md)
