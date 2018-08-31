---
title: params(C# 참조)
ms.date: 07/20/2015
f1_keywords:
- params_CSharpKeyword
- params
helpviewer_keywords:
- parameters [C#], params
- params keyword [C#]
ms.assetid: 1690815e-b52b-4967-8380-5780aff08012
ms.openlocfilehash: 692c2f61ae99f1c1c8e04a5a1bcad08814d286fe
ms.sourcegitcommit: a1e35d4e94edab384a63406c0a5438306873031b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "42752187"
---
# <a name="params-c-reference"></a><span data-ttu-id="61a93-102">params(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="61a93-102">params (C# Reference)</span></span>
<span data-ttu-id="61a93-103">`params` 키워드를 사용하면 가변 개수의 인수를 사용하는 [메서드 매개 변수](../../../csharp/language-reference/keywords/method-parameters.md)를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61a93-103">By using the `params` keyword, you can specify a [method parameter](../../../csharp/language-reference/keywords/method-parameters.md) that takes a variable number of arguments.</span></span>  
  
 <span data-ttu-id="61a93-104">매개 변수 선언이나 지정된 형식의 인수 배열에 지정된 형식의 쉼표로 구분된 인수 목록을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61a93-104">You can send a comma-separated list of arguments of the type specified in the parameter declaration or an array of arguments of the specified type.</span></span> <span data-ttu-id="61a93-105">인수를 보내지 않을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61a93-105">You also can send no arguments.</span></span> <span data-ttu-id="61a93-106">인수를 보내지 않는 경우 `params` 목록의 길이는 0입니다.</span><span class="sxs-lookup"><span data-stu-id="61a93-106">If you send no arguments, the length of the `params` list is zero.</span></span>  
  
 <span data-ttu-id="61a93-107">메서드 선언에서 `params` 키워드 뒤에는 추가 매개 변수가 허용되지 않으며, `params` 키워드 하나만 메서드 선언에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61a93-107">No additional parameters are permitted after the `params` keyword in a method declaration, and only one `params` keyword is permitted in a method declaration.</span></span>  
 
 <span data-ttu-id="61a93-108">`params` 매개 변수의 선언된 형식은 다음 예제와 같이 1차원 배열이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a93-108">The declared type of the `params` parameter must be a single-dimensional array, as the following example shows.</span></span> <span data-ttu-id="61a93-109">그렇지 않으면 컴파일러 오류 [CS0225](../../../csharp/misc/cs0225.md)가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="61a93-109">Otherwise, a compiler error [CS0225](../../../csharp/misc/cs0225.md) occurs.</span></span>
  
## <a name="example"></a><span data-ttu-id="61a93-110">예</span><span class="sxs-lookup"><span data-stu-id="61a93-110">Example</span></span>  
 <span data-ttu-id="61a93-111">다음 예제에서는 `params` 매개 변수에 인수를 보낼 수 있는 다양한 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="61a93-111">The following example demonstrates various ways in which arguments can be sent to a `params` parameter.</span></span>  
  
 [!code-csharp[csrefKeywordsMethodParams#5](../../../csharp/language-reference/keywords/codesnippet/CSharp/params_1.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="61a93-112">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="61a93-112">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="61a93-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="61a93-113">See Also</span></span>  
 [<span data-ttu-id="61a93-114">C# 참조</span><span class="sxs-lookup"><span data-stu-id="61a93-114">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="61a93-115">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="61a93-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="61a93-116">C# 키워드</span><span class="sxs-lookup"><span data-stu-id="61a93-116">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="61a93-117">메서드 매개 변수</span><span class="sxs-lookup"><span data-stu-id="61a93-117">Method Parameters</span></span>](../../../csharp/language-reference/keywords/method-parameters.md)
