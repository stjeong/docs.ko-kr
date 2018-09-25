---
title: 배열(C# 프로그래밍 가이드)
ms.date: 07/20/2015
helpviewer_keywords:
- arrays [C#]
- C# language, arrays
ms.assetid: bb79bdde-e570-4c30-adb0-1dd5759ae041
ms.openlocfilehash: e0ed2d678363a29bb870a496846fc6f054769a4b
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47111115"
---
# <a name="arrays-c-programming-guide"></a><span data-ttu-id="1a30f-102">배열(C# 프로그래밍 가이드)</span><span class="sxs-lookup"><span data-stu-id="1a30f-102">Arrays (C# Programming Guide)</span></span>

<span data-ttu-id="1a30f-103">배열 데이터 구조에 형식이 동일한 변수를 여러 개 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a30f-103">You can store multiple variables of the same type in an array data structure.</span></span> <span data-ttu-id="1a30f-104">요소의 형식을 지정하여 배열을 선언합니다.</span><span class="sxs-lookup"><span data-stu-id="1a30f-104">You declare an array by specifying the type of its elements.</span></span>  
  
 `type[] arrayName;`  
  
 <span data-ttu-id="1a30f-105">다음 예제에서는 단일 차원, 다차원 및 가변 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1a30f-105">The following examples create single-dimensional, multidimensional, and jagged arrays:</span></span>  
  
 [!code-csharp[csProgGuideArrays#1](../../../csharp/programming-guide/arrays/codesnippet/CSharp/index_1.cs)]  
  
## <a name="array-overview"></a><span data-ttu-id="1a30f-106">배열 개요</span><span class="sxs-lookup"><span data-stu-id="1a30f-106">Array Overview</span></span>

 <span data-ttu-id="1a30f-107">배열에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a30f-107">An array has the following properties:</span></span>  
  
-   <span data-ttu-id="1a30f-108">배열은 [단일 차원](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md), [다차원](../../../csharp/programming-guide/arrays/multidimensional-arrays.md) 또는 [가변](../../../csharp/programming-guide/arrays/jagged-arrays.md)일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a30f-108">An array can be [Single-Dimensional](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md), [Multidimensional](../../../csharp/programming-guide/arrays/multidimensional-arrays.md) or [Jagged](../../../csharp/programming-guide/arrays/jagged-arrays.md).</span></span>  
  
-   <span data-ttu-id="1a30f-109">차원 수와 각 차원의 길이는 배열 인스턴스를 만들 때 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a30f-109">The number of dimensions and the length of each dimension are established when the array instance is created.</span></span> <span data-ttu-id="1a30f-110">이러한 값은 인스턴스의 수명 동안 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1a30f-110">These values can't be changed during the lifetime of the instance.</span></span>  
  
-   <span data-ttu-id="1a30f-111">숫자 배열 요소의 기본값은 0으로 설정되고, 참조 요소는 null로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a30f-111">The default values of numeric array elements are set to zero, and reference elements are set to null.</span></span>  
  
-   <span data-ttu-id="1a30f-112">가변 배열은 여러 배열로 구성되어 있기 때문에 해당 요소가 참조 형식이며, `null`로 초기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a30f-112">A jagged array is an array of arrays, and therefore its elements are reference types and are initialized to `null`.</span></span>  
  
-   <span data-ttu-id="1a30f-113">배열은 0으로 인덱싱됩니다. `n` 요소는 `0`부터 `n-1`로 인덱싱됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a30f-113">Arrays are zero indexed: an array with `n` elements is indexed from `0` to `n-1`.</span></span>  
  
-   <span data-ttu-id="1a30f-114">배열 요소 형식은 배열 형식을 비롯한 어떤 형식도 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a30f-114">Array elements can be of any type, including an array type.</span></span>  
  
-   <span data-ttu-id="1a30f-115">배열 형식은 <xref:System.Array> 추상 기본 형식에서 파생된 [참조 형식](../../../csharp/language-reference/keywords/reference-types.md)입니다.</span><span class="sxs-lookup"><span data-stu-id="1a30f-115">Array types are [reference types](../../../csharp/language-reference/keywords/reference-types.md) derived from the abstract base type <xref:System.Array>.</span></span> <span data-ttu-id="1a30f-116">이 형식은 <xref:System.Collections.IEnumerable> 및 <xref:System.Collections.Generic.IEnumerable%601>을 구현하므로 C#의 모든 배열에서 [foreach](../../../csharp/language-reference/keywords/foreach-in.md) 반복을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a30f-116">Since this type implements <xref:System.Collections.IEnumerable> and <xref:System.Collections.Generic.IEnumerable%601>, you can use [foreach](../../../csharp/language-reference/keywords/foreach-in.md) iteration on all arrays in C#.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="1a30f-117">관련 단원</span><span class="sxs-lookup"><span data-stu-id="1a30f-117">Related Sections</span></span>  
  
-   [<span data-ttu-id="1a30f-118">개체로 사용되는 배열</span><span class="sxs-lookup"><span data-stu-id="1a30f-118">Arrays as Objects</span></span>](../../../csharp/programming-guide/arrays/arrays-as-objects.md)  
  
-   [<span data-ttu-id="1a30f-119">배열에 foreach 사용</span><span class="sxs-lookup"><span data-stu-id="1a30f-119">Using foreach with Arrays</span></span>](../../../csharp/programming-guide/arrays/using-foreach-with-arrays.md)  
  
-   [<span data-ttu-id="1a30f-120">인수로 배열 전달</span><span class="sxs-lookup"><span data-stu-id="1a30f-120">Passing Arrays as Arguments</span></span>](../../../csharp/programming-guide/arrays/passing-arrays-as-arguments.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="1a30f-121">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="1a30f-121">C# Language Specification</span></span>

 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="1a30f-122">참고 항목</span><span class="sxs-lookup"><span data-stu-id="1a30f-122">See Also</span></span>

- [<span data-ttu-id="1a30f-123">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="1a30f-123">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="1a30f-124">컬렉션</span><span class="sxs-lookup"><span data-stu-id="1a30f-124">Collections</span></span>](../../../csharp/programming-guide/concepts/collections.md)  
- [<span data-ttu-id="1a30f-125">배열 컬렉션 유형</span><span class="sxs-lookup"><span data-stu-id="1a30f-125">Array Collection Type</span></span>](https://msdn.microsoft.com/library/8a9964de-8941-47b1-a3cf-a01bc88db9e8)
