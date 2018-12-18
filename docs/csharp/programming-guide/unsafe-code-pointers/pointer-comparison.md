---
title: 포인터 비교 - C# 프로그래밍 가이드
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], comparison
ms.assetid: fcafd514-7405-4deb-8490-cc58efda5495
ms.openlocfilehash: 72d9017064959c801bd2702ff585ee16b1592da6
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236793"
---
# <a name="pointer-comparison-c-programming-guide"></a><span data-ttu-id="598e3-102">포인터 비교(C# 프로그래밍 가이드)</span><span class="sxs-lookup"><span data-stu-id="598e3-102">Pointer Comparison (C# Programming Guide)</span></span>
<span data-ttu-id="598e3-103">다음 연산자를 적용하여 임의 형식의 포인터를 비교할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="598e3-103">You can apply the following operators to compare pointers of any type:</span></span>  
  
 <span data-ttu-id="598e3-104">**==   !=   \<   >   \<=   >=**</span><span class="sxs-lookup"><span data-stu-id="598e3-104">**==   !=   \<   >   \<=   >=**</span></span>  
  
 <span data-ttu-id="598e3-105">비교 연산자는 부호 없는 정수처럼 두 피연산자의 주소를 비교합니다.</span><span class="sxs-lookup"><span data-stu-id="598e3-105">The comparison operators compare the addresses of the two operands as if they are unsigned integers.</span></span>  
  
## <a name="example"></a><span data-ttu-id="598e3-106">예제</span><span class="sxs-lookup"><span data-stu-id="598e3-106">Example</span></span>  
 [!code-csharp[csProgGuidePointers#16](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/pointer-comparison_1.cs)]  
  
 [!code-csharp[csProgGuidePointers#17](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/pointer-comparison_2.cs)]  
  
## <a name="sample-output"></a><span data-ttu-id="598e3-107">샘플 출력</span><span class="sxs-lookup"><span data-stu-id="598e3-107">Sample Output</span></span>  
 `True`  
  
 `False`  
  
## <a name="see-also"></a><span data-ttu-id="598e3-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="598e3-108">See Also</span></span>

- [<span data-ttu-id="598e3-109">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="598e3-109">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="598e3-110">포인터 식</span><span class="sxs-lookup"><span data-stu-id="598e3-110">Pointer Expressions</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)  
- [<span data-ttu-id="598e3-111">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="598e3-111">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
- [<span data-ttu-id="598e3-112">포인터 조작</span><span class="sxs-lookup"><span data-stu-id="598e3-112">Manipulating Pointers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/manipulating-pointers.md)  
- [<span data-ttu-id="598e3-113">포인터 형식</span><span class="sxs-lookup"><span data-stu-id="598e3-113">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)  
- [<span data-ttu-id="598e3-114">유형</span><span class="sxs-lookup"><span data-stu-id="598e3-114">Types</span></span>](../../../csharp/language-reference/keywords/types.md)  
- [<span data-ttu-id="598e3-115">unsafe</span><span class="sxs-lookup"><span data-stu-id="598e3-115">unsafe</span></span>](../../../csharp/language-reference/keywords/unsafe.md)  
- [<span data-ttu-id="598e3-116">fixed 문</span><span class="sxs-lookup"><span data-stu-id="598e3-116">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)  
- [<span data-ttu-id="598e3-117">stackalloc</span><span class="sxs-lookup"><span data-stu-id="598e3-117">stackalloc</span></span>](../../../csharp/language-reference/keywords/stackalloc.md)
