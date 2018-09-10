---
title: 배열을 인수로 전달(C# 프로그래밍 가이드)
ms.date: 07/05/2018
helpviewer_keywords:
- arrays [C#], passing as arguments
ms.assetid: f3a0971e-c87c-4a1f-8262-bc0a3b712772
ms.openlocfilehash: b2e6c0134af3b5814e9c9321e1486820311aa5c6
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "44042428"
---
# <a name="passing-arrays-as-arguments-c-programming-guide"></a><span data-ttu-id="2e58b-102">배열을 인수로 전달(C# 프로그래밍 가이드)</span><span class="sxs-lookup"><span data-stu-id="2e58b-102">Passing arrays as arguments (C# Programming Guide)</span></span>

<span data-ttu-id="2e58b-103">배열을 메서드 매개 변수에 인수로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e58b-103">Arrays can be passed as arguments to method parameters.</span></span> <span data-ttu-id="2e58b-104">배열은 참조 형식이므로 메서드를 통해 요소 값을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e58b-104">Because arrays are reference types, the method can change the value of the elements.</span></span>

## <a name="passing-single-dimensional-arrays-as-arguments"></a><span data-ttu-id="2e58b-105">1차원 배열을 인수로 전달</span><span class="sxs-lookup"><span data-stu-id="2e58b-105">Passing single-dimensional arrays as arguments</span></span>

<span data-ttu-id="2e58b-106">초기화된 1차원 배열을 메서드에 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e58b-106">You can pass an initialized single-dimensional array to a method.</span></span> <span data-ttu-id="2e58b-107">예를 들어 다음 문은 인쇄 메서드에 배열을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="2e58b-107">For example, the following statement sends an array to a print method.</span></span>

[!code-csharp[csProgGuideArrays#34](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideArrays/CS/Arrays.cs#34)]

<span data-ttu-id="2e58b-108">다음 코드는 인쇄 메서드의 부분 구현을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2e58b-108">The following code shows a partial implementation of the print method.</span></span>

[!code-csharp[csProgGuideArrays#33](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideArrays/CS/Arrays.cs#33)]

<span data-ttu-id="2e58b-109">다음 예제와 같이 한 단계로 새 배열을 초기화하고 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e58b-109">You can initialize and pass a new array in one step, as is shown in the following example.</span></span>

[!code-csharp[CsProgGuideArrays#35](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideArrays/CS/Arrays.cs#35)]

### <a name="example"></a><span data-ttu-id="2e58b-110">예</span><span class="sxs-lookup"><span data-stu-id="2e58b-110">Example</span></span>

<span data-ttu-id="2e58b-111">다음 예제에서는 문자열 배열이 초기화되고 문자열에 대한 `DisplayArray` 메서드에 인수로 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e58b-111">In the following example, an array of strings is initialized and passed as an argument to a `DisplayArray` method for strings.</span></span> <span data-ttu-id="2e58b-112">메서드가 배열 요소를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="2e58b-112">The method displays the elements of the array.</span></span> <span data-ttu-id="2e58b-113">다음으로 `ChangeArray` 메서드는 배열 요소를 반대로 전환한 다음, `ChangeArrayElements` 메서드는 배열의 처음 세 요소를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e58b-113">Next, the `ChangeArray` method reverses the array elements, and then the `ChangeArrayElements` method modifies the first three elements of the array.</span></span> <span data-ttu-id="2e58b-114">각 메서드가 반환된 후 `DisplayArray` 메서드는 배열을 값으로 전달해도 배열 요소가 변경되지 않는다는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2e58b-114">After each method returns, the `DisplayArray` method shows that passing an array by value doesn't prevent changes to the array elements.</span></span>

[!code-csharp[csProgGuideArrays#30](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideArrays/CS/ArrayExample.cs)]

## <a name="passing-multidimensional-arrays-as-arguments"></a><span data-ttu-id="2e58b-115">다차원 배열을 인수로 전달</span><span class="sxs-lookup"><span data-stu-id="2e58b-115">Passing multidimensional arrays as arguments</span></span>

<span data-ttu-id="2e58b-116">초기화된 다차원 배열을 1차원 배열 전달과 동일한 방식으로 메서드에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="2e58b-116">You pass an initialized multidimensional array to a method in the same way that you pass a one-dimensional array.</span></span>

[!code-csharp[csProgGuideArrays#41](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideArrays/CS/Arrays.cs#41)]

<span data-ttu-id="2e58b-117">다음 코드는 2차원 배열을 해당 인수로 허용하는 인쇄 메서드의 부분 선언을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2e58b-117">The following code shows a partial declaration of a print method that accepts a two-dimensional array as its argument.</span></span>

[!code-csharp[csProgGuideArrays#36](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideArrays/CS/Arrays.cs#36)]

<span data-ttu-id="2e58b-118">다음 예제와 같이 한 단계로 새 배열을 초기화하고 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e58b-118">You can initialize and pass a new array in one step, as is shown in the following example:</span></span>

[!code-csharp[csProgGuideArrays#32](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideArrays/CS/Arrays.cs#32)]

### <a name="example"></a><span data-ttu-id="2e58b-119">예</span><span class="sxs-lookup"><span data-stu-id="2e58b-119">Example</span></span>

<span data-ttu-id="2e58b-120">다음 예제에서는 정수의 2차원 배열이 초기화되고 `Print2DArray` 메서드에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e58b-120">In the following example, a two-dimensional array of integers is initialized and passed to the `Print2DArray` method.</span></span> <span data-ttu-id="2e58b-121">메서드가 배열 요소를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="2e58b-121">The method displays the elements of the array.</span></span>

[!code-csharp[csProgGuideArrays#31](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideArrays/CS/Arrays.cs#31)]

## <a name="see-also"></a><span data-ttu-id="2e58b-122">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2e58b-122">See also</span></span>

- [<span data-ttu-id="2e58b-123">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="2e58b-123">C# Programming Guide</span></span>](../index.md)  
- [<span data-ttu-id="2e58b-124">배열</span><span class="sxs-lookup"><span data-stu-id="2e58b-124">Arrays</span></span>](index.md)  
- [<span data-ttu-id="2e58b-125">1차원 배열</span><span class="sxs-lookup"><span data-stu-id="2e58b-125">Single-Dimensional Arrays</span></span>](single-dimensional-arrays.md)  
- [<span data-ttu-id="2e58b-126">다차원 배열</span><span class="sxs-lookup"><span data-stu-id="2e58b-126">Multidimensional Arrays</span></span>](multidimensional-arrays.md)  
- [<span data-ttu-id="2e58b-127">가변 배열</span><span class="sxs-lookup"><span data-stu-id="2e58b-127">Jagged Arrays</span></span>](jagged-arrays.md)  