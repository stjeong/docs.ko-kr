---
title: '방법: 날짜 또는 시간을 나타내는 문자열 확인 (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], validating
- String data type [Visual Basic], validation
ms.assetid: ae7d4b29-3436-4032-bdbf-4650eb1c8e19
ms.openlocfilehash: 1a838d9d156ad9c05a70a4d4d72db1a288731c9b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54685401"
---
# <a name="how-to-validate-strings-that-represent-dates-or-times-visual-basic"></a><span data-ttu-id="5e42f-102">방법: 날짜 또는 시간을 나타내는 문자열 확인 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="5e42f-102">How to: Validate Strings That Represent Dates or Times (Visual Basic)</span></span>
<span data-ttu-id="5e42f-103">다음 코드 예제에서는 `Boolean` 문자열이 유효한 날짜 또는 시간을 나타내는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5e42f-103">The following code example sets a `Boolean` value that indicates whether a string represents a valid date or time.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5e42f-104">예제</span><span class="sxs-lookup"><span data-stu-id="5e42f-104">Example</span></span>  
 [!code-vb[VbVbcnRegEx#2](../../../../visual-basic/programming-guide/language-features/strings/codesnippet/VisualBasic/how-to-validate-strings-that-represent-dates-or-times_1.vb)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="5e42f-105">코드 컴파일</span><span class="sxs-lookup"><span data-stu-id="5e42f-105">Compiling the Code</span></span>  
 <span data-ttu-id="5e42f-106">바꿉니다 `("01/01/03")` 고 `"9:30 PM"` 유효성을 검사 하려는 시간과 날짜를 사용 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e42f-106">Replace `("01/01/03")` and `"9:30 PM"` with the date and time you want to validate.</span></span> <span data-ttu-id="5e42f-107">사용 하 여 다른 하드 코드 된 문자열을 사용 하 여 문자열을 바꿀 수 있습니다는 `String` 변수나 메서드를 사용 하 여 반환 하는 문자열 같은 `InputBox`합니다.</span><span class="sxs-lookup"><span data-stu-id="5e42f-107">You can replace the string with another hard-coded string, with a `String` variable, or with a method that returns a string, such as `InputBox`.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="5e42f-108">강력한 프로그래밍</span><span class="sxs-lookup"><span data-stu-id="5e42f-108">Robust Programming</span></span>  
 <span data-ttu-id="5e42f-109">이 메서드를 사용 하 여 문자열 변환 하려고 하기 전에 유효성을 검사 합니다 `String` 에 `DateTime` 변수.</span><span class="sxs-lookup"><span data-stu-id="5e42f-109">Use this method to validate the string before trying to convert the `String` to a `DateTime` variable.</span></span> <span data-ttu-id="5e42f-110">날짜 또는 시간을 먼저 확인 하 여 런타임 시 예외를 생성을 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e42f-110">By checking the date or time first, you can avoid generating an exception at run time.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e42f-111">참고자료</span><span class="sxs-lookup"><span data-stu-id="5e42f-111">See also</span></span>
- <xref:Microsoft.VisualBasic.Information.IsDate%2A>
- <xref:Microsoft.VisualBasic.Interaction.InputBox%2A>
- [<span data-ttu-id="5e42f-112">Visual Basic의 문자열 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="5e42f-112">Validating Strings in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/validating-strings.md)
