---
title: '방법: Visual Basic에서 배열 변수 초기화'
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], initializing
- arrays [Visual Basic], variables
- arrays [Visual Basic], initializing
- arrays [Visual Basic], declaring
ms.assetid: aadd7a60-7ca4-4608-b986-091f19e7fc10
ms.openlocfilehash: 4ce2e061c5f523fae3020b08034875422a0062a7
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50202005"
---
# <a name="how-to-initialize-an-array-variable-in-visual-basic"></a><span data-ttu-id="e9910-102">방법: Visual Basic에서 배열 변수 초기화</span><span class="sxs-lookup"><span data-stu-id="e9910-102">How to: Initialize an Array Variable in Visual Basic</span></span>
<span data-ttu-id="e9910-103">에 배열 리터럴 포함 하 여 배열 변수 초기화는 `New` 절 및 배열의 초기 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-103">You initialize an array variable by including an array literal in a `New` clause and specifying the initial values of the array.</span></span> <span data-ttu-id="e9910-104">형식을 지정 하거나 배열 리터럴의 값에서 유추 하도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-104">You can either specify the type or allow it to be inferred from the values in the array literal.</span></span> <span data-ttu-id="e9910-105">형식 유추는 방법에 대 한 자세한 내용은 "채우기는 배열에 초기 값"를 참조 하세요 [배열](../../../../visual-basic/programming-guide/language-features/arrays/index.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-105">For more information about how the type is inferred, see "Populating an Array with Initial Values" in [Arrays](../../../../visual-basic/programming-guide/language-features/arrays/index.md).</span></span>  
  
### <a name="to-initialize-an-array-variable-by-using-an-array-literal"></a><span data-ttu-id="e9910-106">배열 리터럴을 사용 하 여 배열 변수를 초기화 하려면</span><span class="sxs-lookup"><span data-stu-id="e9910-106">To initialize an array variable by using an array literal</span></span>  
  
-   <span data-ttu-id="e9910-107">에 `New` 절을 배열 값에 할당할 때 중괄호 안에 요소 값을 제공 하거나 (`{}`).</span><span class="sxs-lookup"><span data-stu-id="e9910-107">Either in the `New` clause, or when you assign the array value, supply the element values inside braces (`{}`).</span></span> <span data-ttu-id="e9910-108">다음 예제에서는 선언, 생성 및 형식의 요소가 있는 배열을 포함 하는 변수를 초기화 하는 여러 방법을 `Char`합니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-108">The following example shows several ways to declare, create, and initialize a variable to contain an array that has elements of type `Char`.</span></span>  
  
     [!code-vb[VbVbalrArrays#16](../../../../visual-basic/programming-guide/language-features/arrays/codesnippet/VisualBasic/how-to-initialize-an-array-variable_1.vb)]  
  
     <span data-ttu-id="e9910-109">각 문을 실행 한 후 만들어지는 배열의 길이는 2 초기 값이 포함 된 인덱스를 인덱스 0에 있는 요소를 사용 하 여 3에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-109">After each statement executes, the array that's created has a length of 3, with elements at index 0 through index 2 containing the initial values.</span></span> <span data-ttu-id="e9910-110">상한 값과 값이 모두를 제공 하는 경우 인덱스 0부터 상한 까지의 모든 요소에 대 한 값을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-110">If you supply both the upper bound and the values, you must include a value for every element from index 0 through the upper bound.</span></span>  
  
     <span data-ttu-id="e9910-111">배열 리터럴에 요소 값을 제공 하는 경우 인덱스 상한을 지정할 필요가 없습니다를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-111">Notice that you do not have to specify the index upper bound if you supply element values in an array literal.</span></span> <span data-ttu-id="e9910-112">상한은 없으며 지정 된 경우 배열의 크기 배열 리터럴의 값의 수를 기준으로 유추 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-112">If no upper bound is specified, the size of the array is inferred based on the number of values in the array literal.</span></span>  
  
### <a name="to-initialize-a-multidimensional-array-variable-by-using-array-literals"></a><span data-ttu-id="e9910-113">배열 리터럴을 사용 하 여 다차원 배열 변수를 초기화 하려면</span><span class="sxs-lookup"><span data-stu-id="e9910-113">To initialize a multidimensional array variable by using array literals</span></span>  
  
-   <span data-ttu-id="e9910-114">중괄호 안에 값을 중첩 (`{}`) 중괄호 안에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-114">Nest values inside braces (`{}`) within braces.</span></span> <span data-ttu-id="e9910-115">중첩 된 배열 리터럴은 모두 동일한 형식과 길이의 배열로 유추 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-115">Ensure that the nested array literals all infer as arrays of the same type and length.</span></span> <span data-ttu-id="e9910-116">다음 코드 예제에서는 다차원 배열 초기화의 몇 가지 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-116">The following code example shows several examples of multidimensional array initialization.</span></span>  
  
     [!code-vb[VbVbalrArrays#17](../../../../visual-basic/programming-guide/language-features/arrays/codesnippet/VisualBasic/how-to-initialize-an-array-variable_2.vb)]  
  
-   <span data-ttu-id="e9910-117">명시적으로 배열 범위를 지정 하거나 그대로 컴파일러에서 배열 리터럴의 값을 기반으로 배열 범위를 유추 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-117">You can explicitly specify the array bounds, or leave them out and have the compiler infer the array bounds based on the values in the array literal.</span></span> <span data-ttu-id="e9910-118">상한 및 값을 제공 하는 경우 모든 차원의 인덱스 0부터 상한 까지의 모든 요소에 대 한 값을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-118">If you supply both the upper bounds and the values, you must include a value for every element from index 0 through the upper bound in every dimension.</span></span> <span data-ttu-id="e9910-119">다음 예제에서는 여러 가지 방법으로 선언 하 고, 만들고, 형식의 요소가 있는 2 차원 배열을 포함 하는 변수를 초기화 합니다. `Short`</span><span class="sxs-lookup"><span data-stu-id="e9910-119">The following example shows several ways to declare, create, and initialize a variable to contain a two-dimensional array that has elements of type `Short`</span></span>  
  
     [!code-vb[VbVbalrArrays#18](../../../../visual-basic/programming-guide/language-features/arrays/codesnippet/VisualBasic/how-to-initialize-an-array-variable_3.vb)]  
  
     <span data-ttu-id="e9910-120">만들어진된 배열 인덱스가 있는 6 개의 초기화 된 요소가 포함 각 문을 실행 한 후 `(0,0)`, `(0,1)`, `(0,2)`, `(1,0)`를 `(1,1)`, 및 `(1,2)`합니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-120">After each statement executes, the created array contains six initialized elements that have indexes `(0,0)`, `(0,1)`, `(0,2)`, `(1,0)`, `(1,1)`, and `(1,2)`.</span></span> <span data-ttu-id="e9910-121">값을 포함 하는 각 배열 위치 `10`합니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-121">Each array location contains the value `10`.</span></span>  
  
-   <span data-ttu-id="e9910-122">다음 예제에서는 다차원 배열을 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-122">The following example iterates through a multidimensional array.</span></span> <span data-ttu-id="e9910-123">Visual Basic에서 작성 된 Windows 콘솔 응용 프로그램에서 내부 코드를 붙여 넣습니다.는 `Sub Main()` 메서드.</span><span class="sxs-lookup"><span data-stu-id="e9910-123">In a Windows console application that is written in Visual Basic, paste the code inside the `Sub Main()` method.</span></span> <span data-ttu-id="e9910-124">마지막 주석은 출력을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-124">The last comments show the output.</span></span>  
  
     [!code-vb[VbVbalrArrays#31](../../../../visual-basic/programming-guide/language-features/arrays/codesnippet/VisualBasic/how-to-initialize-an-array-variable_4.vb)]  
  
### <a name="to-initialize-a-jagged-array-variable-by-using-array-literals"></a><span data-ttu-id="e9910-125">배열 리터럴을 사용 하 여 가변된 배열 변수를 초기화 하려면</span><span class="sxs-lookup"><span data-stu-id="e9910-125">To initialize a jagged array variable by using array literals</span></span>  
  
-   <span data-ttu-id="e9910-126">중괄호 안에 개체 값을 중첩 (`{}`).</span><span class="sxs-lookup"><span data-stu-id="e9910-126">Nest object values inside braces (`{}`).</span></span> <span data-ttu-id="e9910-127">가변된 배열의 경우 서로 다른 길이의 배열을 지정 하는 배열 리터럴을 중첩할 수도 있습니다 하지만 중첩 된 배열 리터럴을 괄호로 묶인 있는지 확인 (`()`).</span><span class="sxs-lookup"><span data-stu-id="e9910-127">Although you can also nest array literals that specify arrays of different lengths, in the case of a jagged array, make sure that the nested array literals are enclosed in parentheses (`()`).</span></span> <span data-ttu-id="e9910-128">괄호의 중첩 된 배열 리터럴 평가 하 고, 결과 배열이 가변 배열의 초기 값으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-128">The parentheses force the evaluation of the nested array literals, and the resulting arrays are used as the initial values of the jagged array.</span></span> <span data-ttu-id="e9910-129">다음 코드 예제에서는 가변된 배열 초기화 하는 두 가지 예제를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-129">The following code example shows two examples of jagged array initialization.</span></span>  
  
     [!code-vb[VbVbalrArrays#19](../../../../visual-basic/programming-guide/language-features/arrays/codesnippet/VisualBasic/how-to-initialize-an-array-variable_5.vb)]  
  
-   <span data-ttu-id="e9910-130">다음 예제에서는 가변된 배열을 반복합니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-130">The following example iterates through a jagged array.</span></span> <span data-ttu-id="e9910-131">Visual Basic에서 작성 된 Windows 콘솔 응용 프로그램에서 내부 코드를 붙여 넣습니다.는 `Sub Main()` 메서드.</span><span class="sxs-lookup"><span data-stu-id="e9910-131">In a Windows console application that is written in Visual Basic, paste the code inside the `Sub Main()` method.</span></span>  <span data-ttu-id="e9910-132">코드의 마지막 주석은 출력을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e9910-132">The last comments in the code show the output.</span></span>  
  
     [!code-vb[VbVbalrArrays#32](../../../../visual-basic/programming-guide/language-features/arrays/codesnippet/VisualBasic/how-to-initialize-an-array-variable_6.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="e9910-133">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e9910-133">See Also</span></span>  
 [<span data-ttu-id="e9910-134">배열</span><span class="sxs-lookup"><span data-stu-id="e9910-134">Arrays</span></span>](../../../../visual-basic/programming-guide/language-features/arrays/index.md)  
 [<span data-ttu-id="e9910-135">배열 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e9910-135">Troubleshooting Arrays</span></span>](../../../../visual-basic/programming-guide/language-features/arrays/troubleshooting-arrays.md)
