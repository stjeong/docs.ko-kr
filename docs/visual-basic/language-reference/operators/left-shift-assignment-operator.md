---
title: << = 연산자 (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.<<=
helpviewer_keywords:
- operator <<=
- assignment statements [Visual Basic], compound
- <<= operator [Visual Basic]
- statements [Visual Basic], compound assignment
- operator<<=
- compound assignment statements [Visual Basic]
ms.assetid: 8ad26613-faff-4e2f-89ee-63feee33bfda
ms.openlocfilehash: b2a642b1187c9a08007ee1eddfa0764198fc0877
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56981649"
---
# <a name="-operator-visual-basic"></a><span data-ttu-id="020d5-102">\<\<= 연산자 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="020d5-102">\<\<= Operator (Visual Basic)</span></span>
<span data-ttu-id="020d5-103">변수 또는 속성의 값에 산술 왼쪽된 시프트를 수행 하 고 해당 변수 또는 속성으로 결과 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="020d5-103">Performs an arithmetic left shift on the value of a variable or property and assigns the result back to the variable or property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="020d5-104">구문</span><span class="sxs-lookup"><span data-stu-id="020d5-104">Syntax</span></span>  
  
```  
variableorproperty <<= amount  
```  
  
## <a name="parts"></a><span data-ttu-id="020d5-105">요소</span><span class="sxs-lookup"><span data-stu-id="020d5-105">Parts</span></span>  
 `variableorproperty`  
 <span data-ttu-id="020d5-106">필수 요소.</span><span class="sxs-lookup"><span data-stu-id="020d5-106">Required.</span></span> <span data-ttu-id="020d5-107">변수 또는 정수 계열 형식의 속성 (`SByte`, `Byte`, `Short`, `UShort`를 `Integer`를 `UInteger`를 `Long`, 또는 `ULong`).</span><span class="sxs-lookup"><span data-stu-id="020d5-107">Variable or property of an integral type (`SByte`, `Byte`, `Short`, `UShort`, `Integer`, `UInteger`, `Long`, or `ULong`).</span></span>  
  
 `amount`  
 <span data-ttu-id="020d5-108">필수 요소.</span><span class="sxs-lookup"><span data-stu-id="020d5-108">Required.</span></span> <span data-ttu-id="020d5-109">숫자 식으로 확대 되는 데이터 형식의 `Integer`합니다.</span><span class="sxs-lookup"><span data-stu-id="020d5-109">Numeric expression of a data type that widens to `Integer`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="020d5-110">설명</span><span class="sxs-lookup"><span data-stu-id="020d5-110">Remarks</span></span>  
 <span data-ttu-id="020d5-111">왼쪽된에 있는 요소는 `<<=` 연산자는 간단한 스칼라 변수, 속성 또는 배열의 요소 수입니다.</span><span class="sxs-lookup"><span data-stu-id="020d5-111">The element on the left side of the `<<=` operator can be a simple scalar variable, a property, or an element of an array.</span></span> <span data-ttu-id="020d5-112">변수 또는 속성 일 수 없습니다 [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="020d5-112">The variable or property cannot be [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span></span>  
  
 <span data-ttu-id="020d5-113">`<<=` 연산자는 변수 또는 속성의 값에 산술 왼쪽된 시프트를 먼저 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="020d5-113">The `<<=` operator first performs an arithmetic left shift on the value of the variable or property.</span></span> <span data-ttu-id="020d5-114">다음 연산자는 다시 해당 변수 또는 속성에 해당 작업의 결과 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="020d5-114">The operator then assigns the result of that operation back to that variable or property.</span></span>  
  
 <span data-ttu-id="020d5-115">산술 shifts 순환있지 않습니다 즉, 결과의 한쪽 끝에서 벗어나 이동한 비트는 반대쪽 다시 도입 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="020d5-115">Arithmetic shifts are not circular, which means the bits shifted off one end of the result are not reintroduced at the other end.</span></span> <span data-ttu-id="020d5-116">산술 왼쪽 시프트에서 결과 데이터 형식의 범위를 벗어나는 이동 하는 비트는 무시 되 고 오른쪽 비워진 비트 위치 0으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="020d5-116">In an arithmetic left shift, the bits shifted beyond the range of the result data type are discarded, and the bit positions vacated on the right are set to zero.</span></span>  
  
## <a name="overloading"></a><span data-ttu-id="020d5-117">오버로딩</span><span class="sxs-lookup"><span data-stu-id="020d5-117">Overloading</span></span>  
 <span data-ttu-id="020d5-118">합니다 [<< 연산자](../../../visual-basic/language-reference/operators/left-shift-operator.md) 될 수 있습니다 *오버 로드 된*, 클래스 또는 구조체 수 할 동작 피연산자에 해당 클래스 또는 구조체 형식의 경우.</span><span class="sxs-lookup"><span data-stu-id="020d5-118">The [<< Operator](../../../visual-basic/language-reference/operators/left-shift-operator.md) can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="020d5-119">오버 로드 된 `<<` 연산자의 동작에 영향을 줍니다는 `<<=` 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="020d5-119">Overloading the `<<` operator affects the behavior of the `<<=` operator.</span></span> <span data-ttu-id="020d5-120">코드를 사용 하는 경우 `<<=` 클래스나 구조체에 오버 로드에서 `<<`, 다시 정의 된 동작을 이해 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="020d5-120">If your code uses `<<=` on a class or structure that overloads `<<`, be sure you understand its redefined behavior.</span></span> <span data-ttu-id="020d5-121">자세한 내용은 [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="020d5-121">For more information, see [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="020d5-122">예제</span><span class="sxs-lookup"><span data-stu-id="020d5-122">Example</span></span>  
 <span data-ttu-id="020d5-123">다음 예제에서는 합니다 `<<=` 비트 패턴의 시프트 연산자는 `Integer` 변수에 지정 된 크기 및 결과 할당 하 여 변수를 왼쪽입니다.</span><span class="sxs-lookup"><span data-stu-id="020d5-123">The following example uses the `<<=` operator to shift the bit pattern of an `Integer` variable left by the specified amount and assign the result to the variable.</span></span>  
  
 [!code-vb[VbVbalrOperators#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#13)]  
  
## <a name="see-also"></a><span data-ttu-id="020d5-124">참고자료</span><span class="sxs-lookup"><span data-stu-id="020d5-124">See also</span></span>
- [<span data-ttu-id="020d5-125"><< 연산자</span><span class="sxs-lookup"><span data-stu-id="020d5-125"><< Operator</span></span>](../../../visual-basic/language-reference/operators/left-shift-operator.md)
- [<span data-ttu-id="020d5-126">할당 연산자</span><span class="sxs-lookup"><span data-stu-id="020d5-126">Assignment Operators</span></span>](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [<span data-ttu-id="020d5-127">비트 시프트 연산자</span><span class="sxs-lookup"><span data-stu-id="020d5-127">Bit Shift Operators</span></span>](../../../visual-basic/language-reference/operators/bit-shift-operators.md)
- [<span data-ttu-id="020d5-128">Visual Basic에서의 연산자 우선 순위</span><span class="sxs-lookup"><span data-stu-id="020d5-128">Operator Precedence in Visual Basic</span></span>](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [<span data-ttu-id="020d5-129">기능별 연산자 목록</span><span class="sxs-lookup"><span data-stu-id="020d5-129">Operators Listed by Functionality</span></span>](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [<span data-ttu-id="020d5-130">문(C++)</span><span class="sxs-lookup"><span data-stu-id="020d5-130">Statements</span></span>](../../../visual-basic/programming-guide/language-features/statements.md)
