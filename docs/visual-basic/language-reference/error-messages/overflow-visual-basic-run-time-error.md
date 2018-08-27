---
title: 오버플로가 발생했습니다(Visual Basic 런타임 오류).
ms.date: 07/20/2015
f1_keywords:
- vbrERRID_Overflow
ms.assetid: c6a23279-3086-412a-bcff-ff8ed2cb8c6f
ms.openlocfilehash: 7546676b85465577b357b7ad0757b4db8d40dbe3
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42934441"
---
# <a name="overflow-visual-basic-run-time-error"></a><span data-ttu-id="81566-102">오버플로가 발생했습니다(Visual Basic 런타임 오류).</span><span class="sxs-lookup"><span data-stu-id="81566-102">Overflow (Visual Basic Run-Time Error)</span></span>
<span data-ttu-id="81566-103">할당 대상의 한계를 초과 하 여 할당 하려고 할 때 오버플로가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="81566-103">An overflow results when you attempt an assignment that exceeds the limits of the assignment's target.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="81566-104">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="81566-104">To correct this error</span></span>  
  
1.  <span data-ttu-id="81566-105">할당, 계산 및 데이터 형식 변환 너무 커서 변수 값의 해당 형식에 대 한 허용 범위 내에서 표현할 수 없는 및 형식의 변수에 값 할당의 결과 보다 광범위 한 값을 수용할 수 있는지 확인 에 필요한 경우.</span><span class="sxs-lookup"><span data-stu-id="81566-105">Make sure that results of assignments, calculations, and data type conversions are not too large to be represented within the range of variables allowed for that type of value, and assign the value to a variable of a type that can hold a larger range of values, if necessary.</span></span>  
  
2.  <span data-ttu-id="81566-106">속성에 할당 수행 되는 속성의 범위에 맞는 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="81566-106">Make sure assignments to properties fit the range of the property to which they are made.</span></span>  
  
3.  <span data-ttu-id="81566-107">숫자는 정수를 강제 변환 되는 계산에 사용 되는 정수 보다 큰 결과 있지 않은 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="81566-107">Make sure that numbers used in calculations that are coerced into integers do not have results larger than integers.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="81566-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="81566-108">See Also</span></span>  
 <xref:System.Int32.MaxValue?displayProperty=nameWithType>  
 <xref:System.Double.MaxValue?displayProperty=nameWithType>  
 [<span data-ttu-id="81566-109">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="81566-109">Data Types</span></span>](../../../visual-basic/language-reference/data-types/index.md)  
 [<span data-ttu-id="81566-110">오류 형식</span><span class="sxs-lookup"><span data-stu-id="81566-110">Error Types</span></span>](../../../visual-basic/programming-guide/language-features/error-types.md)
