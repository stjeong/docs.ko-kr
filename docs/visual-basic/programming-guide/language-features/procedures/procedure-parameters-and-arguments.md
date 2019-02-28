---
title: 프로시저 매개 변수 및 인수(Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], arguments
- procedures [Visual Basic], argument lists
- values [Visual Basic], passing to procedures
- arguments [Visual Basic], passing
- procedures [Visual Basic], parameters
- Visual Basic code, argument lists
- Visual Basic code, procedures
- parameters [Visual Basic], Visual Basic procedures
- parameters [Visual Basic], lists
- arguments [Visual Basic], Visual Basic procedures
- arguments [Visual Basic], procedures
- parameter lists [Visual Basic]
- Visual Basic code, parameter lists
- argument lists [Visual Basic]
- procedures [Visual Basic], parameter lists
ms.assetid: ff275aff-aa13-40df-bd4c-63486db8c1e9
ms.openlocfilehash: f7291d809c754249c155eb9382f3fcd8a63c20c7
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56972557"
---
# <a name="procedure-parameters-and-arguments-visual-basic"></a><span data-ttu-id="b4eeb-102">프로시저 매개 변수 및 인수(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b4eeb-102">Procedure Parameters and Arguments (Visual Basic)</span></span>
<span data-ttu-id="b4eeb-103">대부분의 경우 프로시저를 호출한 후 나타나는 상황에 대 한 일부 정보를 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-103">In most cases, a procedure needs some information about the circumstances in which it has been called.</span></span> <span data-ttu-id="b4eeb-104">반복 또는 공유 작업을 수행 하는 프로시저는 각 호출에 대 한 다른 정보를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-104">A procedure that performs repeated or shared tasks uses different information for each call.</span></span> <span data-ttu-id="b4eeb-105">이 정보는 변수, 상수 및 호출할 때 프로시저에 전달 하는 식으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-105">This information consists of variables, constants, and expressions that you pass to the procedure when you call it.</span></span>  
  
 <span data-ttu-id="b4eeb-106">A *매개 변수* 프로시저에는 호출할 때 제공 하는 값을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-106">A *parameter* represents a value that the procedure expects you to supply when you call it.</span></span> <span data-ttu-id="b4eeb-107">해당 매개 변수를 정의 하는 프로시저의 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-107">The procedure's declaration defines its parameters.</span></span>  
  
 <span data-ttu-id="b4eeb-108">매개 변수가 없는, 매개 변수 하나 또는 둘 이상 있는 프로시저를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-108">You can define a procedure with no parameters, one parameter, or more than one.</span></span> <span data-ttu-id="b4eeb-109">매개 변수를 지정 하는 프로시저 정의의 일부로 호출 되는 *매개 변수 목록*합니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-109">The part of the procedure definition that specifies the parameters is called the *parameter list*.</span></span>  
  
 <span data-ttu-id="b4eeb-110">*인수* 프로시저를 호출할 때 프로시저 매개 변수에 제공한 값을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-110">An *argument* represents the value you supply to a procedure parameter when you call the procedure.</span></span> <span data-ttu-id="b4eeb-111">호출 코드는 프로시저를 호출할 때 인수를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-111">The calling code supplies the arguments when it calls the procedure.</span></span> <span data-ttu-id="b4eeb-112">인수를 지정 하는 프로시저 호출의 일부 라고 합니다 *인수 목록*합니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-112">The part of the procedure call that specifies the arguments is called the *argument list*.</span></span>  
  
 <span data-ttu-id="b4eeb-113">다음 그림에서는 프로시저를 호출 하는 코드를 보여 줍니다. `safeSquareRoot` 서로 다른 두 위치에서.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-113">The following illustration shows code calling the procedure `safeSquareRoot` from two different places.</span></span> <span data-ttu-id="b4eeb-114">변수 값을 전달 하는 첫 번째 호출 `x` (4.0) 매개 변수에 `number`, 및 반환 값은 `root` (2.0) 변수에 할당 된 `y`합니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-114">The first call passes the value of the variable `x` (4.0) to the parameter `number`, and the return value in `root` (2.0) is assigned to the variable `y`.</span></span> <span data-ttu-id="b4eeb-115">두 번째 호출은 전달에 리터럴 값 9.0 `number`, (3.0) 반환 값을 변수에 할당 합니다 `z`.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-115">The second call passes the literal value 9.0 to `number`, and assigns the return value (3.0) to variable `z`.</span></span>  
  
 <span data-ttu-id="b4eeb-116">![매개 변수에 인수를 전달 하는 그래픽 다이어그램](./media/parametersargue.gif "ParametersArgue")</span><span class="sxs-lookup"><span data-stu-id="b4eeb-116">![Graphic diagram of passing argument to parameter](./media/parametersargue.gif "ParametersArgue")</span></span>  
<span data-ttu-id="b4eeb-117">매개 변수에 인수를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-117">Passing an argument to a parameter</span></span>  
  
 <span data-ttu-id="b4eeb-118">자세한 내용은 [매개 변수 간의 차이점 및 인수](./differences-between-parameters-and-arguments.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-118">For more information, see [Differences Between Parameters and Arguments](./differences-between-parameters-and-arguments.md).</span></span>  
  
## <a name="parameter-data-type"></a><span data-ttu-id="b4eeb-119">매개 변수 데이터 형식</span><span class="sxs-lookup"><span data-stu-id="b4eeb-119">Parameter Data Type</span></span>  
 <span data-ttu-id="b4eeb-120">매개 변수의 데이터 형식을 사용 하 여 정의한는 `As` 선언 절.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-120">You define a data type for a parameter by using the `As` clause in its declaration.</span></span> <span data-ttu-id="b4eeb-121">예를 들어, 다음 함수는 문자열 및 정수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-121">For example, the following function accepts a string and an integer.</span></span>  
  
 [!code-vb[VbVbcnProcedures#32](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#32)]  
  
 <span data-ttu-id="b4eeb-122">형식 검사 스위치 하는 경우 ([Option Strict 문](../../../../visual-basic/language-reference/statements/option-strict-statement.md))은 `Off,` 는 `As` 절은 선택 사항 제외 하 고 하나의 매개 변수를 사용 하는 경우 모든 매개 변수 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-122">If the type checking switch ([Option Strict Statement](../../../../visual-basic/language-reference/statements/option-strict-statement.md)) is `Off,` the `As` clause is optional, except that if any one parameter uses it, all parameters must use it.</span></span> <span data-ttu-id="b4eeb-123">형식 검사가 `On`, `As` 절이 모든 프로시저 매개 변수에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-123">If type checking is `On`, the `As` clause is required for all procedure parameters.</span></span>  
  
 <span data-ttu-id="b4eeb-124">호출 코드에서는 해당 매개 변수를와 다른 데이터 형식과 같은 인수를 제공할 경우 `Byte` 에 `String` 매개 변수를 다음 중 하나를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-124">If the calling code expects to supply an argument with a data type different from that of its corresponding parameter, such as `Byte` to a `String` parameter, it must do one of the following:</span></span>  
  
-   <span data-ttu-id="b4eeb-125">인수만 지정 매개 변수 데이터 형식으로 변환할 데이터 형식</span><span class="sxs-lookup"><span data-stu-id="b4eeb-125">Supply only arguments with data types that widen to the parameter data type;</span></span>  
  
-   <span data-ttu-id="b4eeb-126">설정 `Option Strict Off` 암시적 축소 변환을; 수 있도록 또는</span><span class="sxs-lookup"><span data-stu-id="b4eeb-126">Set `Option Strict Off` to allow implicit narrowing conversions; or</span></span>  
  
-   <span data-ttu-id="b4eeb-127">변환 키워드를 사용 하 여 데이터 형식을 명시적으로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-127">Use a conversion keyword to explicitly convert the data type.</span></span>  
  
### <a name="type-parameters"></a><span data-ttu-id="b4eeb-128">형식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b4eeb-128">Type Parameters</span></span>  
 <span data-ttu-id="b4eeb-129">A *제네릭 프로시저* 하나 이상의 정의 *형식 매개 변수* 일반 매개 변수 외에도 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-129">A *generic procedure* also defines one or more *type parameters* in addition to its normal parameters.</span></span> <span data-ttu-id="b4eeb-130">제네릭 프로시저를 호출 데이터 형식 요구 사항을 각각의 개별 호출은 조정할 수 있도록 프로시저를 호출할 때마다 다른 데이터 형식을 전달 하도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-130">A generic procedure allows the calling code to pass different data types each time it calls the procedure, so it can tailor the data types to the requirements of each individual call.</span></span> <span data-ttu-id="b4eeb-131">[Generic Procedures in Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/generic-procedures.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-131">See [Generic Procedures in Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/generic-procedures.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b4eeb-132">참고자료</span><span class="sxs-lookup"><span data-stu-id="b4eeb-132">See also</span></span>
- [<span data-ttu-id="b4eeb-133">절차</span><span class="sxs-lookup"><span data-stu-id="b4eeb-133">Procedures</span></span>](./index.md)
- [<span data-ttu-id="b4eeb-134">Sub 프로시저</span><span class="sxs-lookup"><span data-stu-id="b4eeb-134">Sub Procedures</span></span>](./sub-procedures.md)
- [<span data-ttu-id="b4eeb-135">Function 프로시저</span><span class="sxs-lookup"><span data-stu-id="b4eeb-135">Function Procedures</span></span>](./function-procedures.md)
- [<span data-ttu-id="b4eeb-136">속성 프로시저</span><span class="sxs-lookup"><span data-stu-id="b4eeb-136">Property Procedures</span></span>](./property-procedures.md)
- [<span data-ttu-id="b4eeb-137">연산자 프로시저</span><span class="sxs-lookup"><span data-stu-id="b4eeb-137">Operator Procedures</span></span>](./operator-procedures.md)
- [<span data-ttu-id="b4eeb-138">방법: 프로시저의 매개 변수를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4eeb-138">How to: Define a Parameter for a Procedure</span></span>](./how-to-define-a-parameter-for-a-procedure.md)
- [<span data-ttu-id="b4eeb-139">방법: 프로시저에 인수 전달</span><span class="sxs-lookup"><span data-stu-id="b4eeb-139">How to: Pass Arguments to a Procedure</span></span>](./how-to-pass-arguments-to-a-procedure.md)
- [<span data-ttu-id="b4eeb-140">값 또는 참조로 인수 전달</span><span class="sxs-lookup"><span data-stu-id="b4eeb-140">Passing Arguments by Value and by Reference</span></span>](./passing-arguments-by-value-and-by-reference.md)
- [<span data-ttu-id="b4eeb-141">프로시저 오버로딩</span><span class="sxs-lookup"><span data-stu-id="b4eeb-141">Procedure Overloading</span></span>](./procedure-overloading.md)
- [<span data-ttu-id="b4eeb-142">Visual Basic의 형식 변환</span><span class="sxs-lookup"><span data-stu-id="b4eeb-142">Type Conversions in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)
