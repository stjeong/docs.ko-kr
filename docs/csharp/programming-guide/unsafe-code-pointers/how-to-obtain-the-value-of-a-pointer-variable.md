---
title: '방법: 포인터 변수의 값 가져오기(C# 프로그래밍 가이드)'
ms.date: 07/20/2015
helpviewer_keywords:
- pointer expressions [C#], indirection
- pointers [C#], indirection
- variables [C#], pointers
- pointers [C#], * operator
ms.assetid: 460a813a-4995-44c1-9de2-213b91dc7668
ms.openlocfilehash: 66f341e193a0f018adb76a40617f85266519e602
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44267219"
---
# <a name="how-to-obtain-the-value-of-a-pointer-variable-c-programming-guide"></a><span data-ttu-id="21ce6-102">방법: 포인터 변수의 값 가져오기(C# 프로그래밍 가이드)</span><span class="sxs-lookup"><span data-stu-id="21ce6-102">How to: Obtain the Value of a Pointer Variable (C# Programming Guide)</span></span>
<span data-ttu-id="21ce6-103">포인터 간접 참조 연산자를 사용하여 포인터가 가리키는 위치에 있는 변수를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21ce6-103">Use the pointer indirection operator to obtain the variable at the location pointed to by a pointer.</span></span> <span data-ttu-id="21ce6-104">식의 형식은 다음과 같습니다. 여기서 `p`는 포인터 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="21ce6-104">The expression takes the following form, where `p` is a pointer type:</span></span>  
  
```  
*p;  
```  
  
 <span data-ttu-id="21ce6-105">포인터 형식이 아닌 식에서는 단항 간접 참조 연산자를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="21ce6-105">You cannot use the unary indirection operator on an expression of any type other than the pointer type.</span></span> <span data-ttu-id="21ce6-106">또한 [void](../../../csharp/language-reference/keywords/void.md) 포인터에는 적용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="21ce6-106">Also, you cannot apply it to a [void](../../../csharp/language-reference/keywords/void.md) pointer.</span></span>  
  
 <span data-ttu-id="21ce6-107">[null](../../../csharp/language-reference/keywords/null.md) 포인터에 간접 참조 연산자를 적용할 때의 결과는 구현에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="21ce6-107">When you apply the indirection operator to a [null](../../../csharp/language-reference/keywords/null.md) pointer, the result depends on the implementation.</span></span>  
  
## <a name="example"></a><span data-ttu-id="21ce6-108">예</span><span class="sxs-lookup"><span data-stu-id="21ce6-108">Example</span></span>  
 <span data-ttu-id="21ce6-109">다음 예제에서는 다양한 형식의 포인터를 사용하여 `char` 형식의 변수에 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="21ce6-109">In the following example, a variable of the type `char` is accessed by using pointers of different types.</span></span> <span data-ttu-id="21ce6-110">변수에 할당되는 물리적 주소가 변경될 수 있으므로 `theChar`의 주소는 실행할 때마다 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="21ce6-110">Note that the address of `theChar` will vary from run to run, because the physical address allocated to a variable can change.</span></span>  
  
 [!code-csharp[csProgGuidePointers#5](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-obtain-the-value-of-a-pointer-variable_1.cs)]  
  
 [!code-csharp[csProgGuidePointers#6](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-obtain-the-value-of-a-pointer-variable_2.cs)]  
  
<span data-ttu-id="21ce6-111">**theChar 값 = Z**
**theChar 주소 = 12F718**
**pChar 값 = Z**
**pInt 값 = 90**</span><span class="sxs-lookup"><span data-stu-id="21ce6-111">**Value of theChar = Z**
**Address of theChar = 12F718**
**Value of pChar = Z**
**Value of pInt = 90**</span></span>

## <a name="see-also"></a><span data-ttu-id="21ce6-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="21ce6-112">See Also</span></span>

- [<span data-ttu-id="21ce6-113">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="21ce6-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="21ce6-114">포인터 식</span><span class="sxs-lookup"><span data-stu-id="21ce6-114">Pointer Expressions</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)  
- [<span data-ttu-id="21ce6-115">포인터 형식</span><span class="sxs-lookup"><span data-stu-id="21ce6-115">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)  
- [<span data-ttu-id="21ce6-116">유형</span><span class="sxs-lookup"><span data-stu-id="21ce6-116">Types</span></span>](../../../csharp/language-reference/keywords/types.md)  
- [<span data-ttu-id="21ce6-117">unsafe</span><span class="sxs-lookup"><span data-stu-id="21ce6-117">unsafe</span></span>](../../../csharp/language-reference/keywords/unsafe.md)  
- [<span data-ttu-id="21ce6-118">fixed 문</span><span class="sxs-lookup"><span data-stu-id="21ce6-118">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)  
- [<span data-ttu-id="21ce6-119">stackalloc</span><span class="sxs-lookup"><span data-stu-id="21ce6-119">stackalloc</span></span>](../../../csharp/language-reference/keywords/stackalloc.md)
