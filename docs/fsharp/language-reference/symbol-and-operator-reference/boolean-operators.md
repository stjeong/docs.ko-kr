---
title: 부울 연산자
description: 사용할 수 있는 부울 연산자에 알아봅니다는 F# 프로그래밍 언어입니다.
ms.date: 05/16/2016
ms.openlocfilehash: 5353b6ec6a0bd610f3446761a1d28f01f0403302
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53612740"
---
# <a name="boolean-operators"></a><span data-ttu-id="5b7f9-103">부울 연산자</span><span class="sxs-lookup"><span data-stu-id="5b7f9-103">Boolean Operators</span></span>

<span data-ttu-id="5b7f9-104">부울 연산자에 대 한 지원에 설명 합니다 F# 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="5b7f9-104">This topic describes the support for Boolean operators in the F# language.</span></span>

## <a name="summary-of-boolean-operators"></a><span data-ttu-id="5b7f9-105">부울 연산자 요약</span><span class="sxs-lookup"><span data-stu-id="5b7f9-105">Summary of Boolean Operators</span></span>

<span data-ttu-id="5b7f9-106">다음 표에서 사용할 수 있는 부울 연산자는 F# 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="5b7f9-106">The following table summarizes the Boolean operators that are available in the F# language.</span></span> <span data-ttu-id="5b7f9-107">이러한 연산자에서 지 원하는 유일한 형식이 `bool` 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5b7f9-107">The only type supported by these operators is the `bool` type.</span></span>

|<span data-ttu-id="5b7f9-108">연산자</span><span class="sxs-lookup"><span data-stu-id="5b7f9-108">Operator</span></span>|<span data-ttu-id="5b7f9-109">설명</span><span class="sxs-lookup"><span data-stu-id="5b7f9-109">Description</span></span>|
|--------|-----------|
|`not`|<span data-ttu-id="5b7f9-110">부정 부울</span><span class="sxs-lookup"><span data-stu-id="5b7f9-110">Boolean negation</span></span>|
|<code>&#124;&#124;</code>|<span data-ttu-id="5b7f9-111">부울 OR</span><span class="sxs-lookup"><span data-stu-id="5b7f9-111">Boolean OR</span></span>|
|`&&`|<span data-ttu-id="5b7f9-112">부울 AND</span><span class="sxs-lookup"><span data-stu-id="5b7f9-112">Boolean AND</span></span>|

<span data-ttu-id="5b7f9-113">부울 AND 및 OR 연산자를 수행 *평가 단락 (short-circuit)*, 식의 전체 결과 확인 하는 데 필요한 경우에 연산자의 오른쪽에 있는 식 평가, 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7f9-113">The Boolean AND and OR operators perform *short-circuit evaluation*, that is, they evaluate the expression on the right of the operator only when it is necessary to determine the overall result of the expression.</span></span> <span data-ttu-id="5b7f9-114">두 번째 식의 `&&` 연산자는 첫 번째 식이 계산 되는 경우에 계산 됩니다 `true`;의 두 번째 식의 `||` 연산자는 첫 번째 식이 계산 되는 경우에 계산 됩니다 `false`합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7f9-114">The second expression of the `&&` operator is evaluated only if the first expression evaluates to `true`; the second expression of the `||` operator is evaluated only if the first expression evaluates to `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="5b7f9-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="5b7f9-115">See also</span></span>

- [<span data-ttu-id="5b7f9-116">비트 연산자</span><span class="sxs-lookup"><span data-stu-id="5b7f9-116">Bitwise Operators</span></span>](bitwise-operators.md)
- [<span data-ttu-id="5b7f9-117">산술 연산자</span><span class="sxs-lookup"><span data-stu-id="5b7f9-117">Arithmetic Operators</span></span>](arithmetic-operators.md)
- [<span data-ttu-id="5b7f9-118">기호 및 연산자 참조</span><span class="sxs-lookup"><span data-stu-id="5b7f9-118">Symbol and Operator Reference</span></span>](index.md)