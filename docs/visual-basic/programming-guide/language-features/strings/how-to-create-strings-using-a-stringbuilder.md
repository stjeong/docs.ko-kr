---
title: '방법: Visual Basic에서 StringBuilder를 사용 하 여 문자열 만들기'
ms.date: 07/20/2015
helpviewer_keywords:
- StringBuilder class
- strings [Visual Basic], using StringBuilder
ms.assetid: 9c042880-aa16-432e-9ccb-cd00abda9ae3
ms.openlocfilehash: 84f0f41cf8ee23466d47dae3b1068c3bc5334072
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54528448"
---
# <a name="how-to-create-strings-using-a-stringbuilder-in-visual-basic"></a><span data-ttu-id="d6a1f-102">방법: Visual Basic에서 StringBuilder를 사용 하 여 문자열 만들기</span><span class="sxs-lookup"><span data-stu-id="d6a1f-102">How to: Create Strings Using a StringBuilder in Visual Basic</span></span>
<span data-ttu-id="d6a1f-103">이 예제를 사용 하 여 많은 짧은 문자열에서 긴 문자열을 생성 합니다 <xref:System.Text.StringBuilder> 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="d6a1f-103">This example constructs a long string from many smaller strings using the <xref:System.Text.StringBuilder> class.</span></span> <span data-ttu-id="d6a1f-104">합니다 <xref:System.Text.StringBuilder> 클래스 보다 더 효율적입니다는 `&=` 여러 문자열 연결 연산자.</span><span class="sxs-lookup"><span data-stu-id="d6a1f-104">The <xref:System.Text.StringBuilder> class is more efficient than the `&=` operator for concatenating many strings.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d6a1f-105">예제</span><span class="sxs-lookup"><span data-stu-id="d6a1f-105">Example</span></span>  
 <span data-ttu-id="d6a1f-106">다음 예에서는 인스턴스에 <xref:System.Text.StringBuilder> 클래스는 해당 인스턴스를 1,000 문자열을 추가 하 고 다음의 문자열 표현을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6a1f-106">The following example creates an instance of the <xref:System.Text.StringBuilder> class, appends 1,000 strings to that instance, and then returns its string representation.</span></span>  
  
 [!code-vb[VbVbalrStrings#70](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-create-strings-using-a-stringbuilder_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="d6a1f-107">참고자료</span><span class="sxs-lookup"><span data-stu-id="d6a1f-107">See also</span></span>
- [<span data-ttu-id="d6a1f-108">StringBuilder 클래스 사용</span><span class="sxs-lookup"><span data-stu-id="d6a1f-108">Using the StringBuilder Class</span></span>](../../../../standard/base-types/stringbuilder.md)
- [<span data-ttu-id="d6a1f-109">&= 연산자</span><span class="sxs-lookup"><span data-stu-id="d6a1f-109">&= Operator</span></span>](../../../../visual-basic/language-reference/operators/and-assignment-operator.md)
- [<span data-ttu-id="d6a1f-110">문자열</span><span class="sxs-lookup"><span data-stu-id="d6a1f-110">Strings</span></span>](../../../../visual-basic/programming-guide/language-features/strings/index.md)
- [<span data-ttu-id="d6a1f-111">새 문자열 만들기</span><span class="sxs-lookup"><span data-stu-id="d6a1f-111">Creating New Strings</span></span>](../../../../standard/base-types/creating-new.md)
- [<span data-ttu-id="d6a1f-112">문자열 조작</span><span class="sxs-lookup"><span data-stu-id="d6a1f-112">Manipulating Strings</span></span>](../../../../standard/base-types/manipulating-strings.md)
- <span data-ttu-id="d6a1f-113">[Strings 샘플](https://msdn.microsoft.com/library/be9e82a3-dc95-4aaa-9396-61b66e467e02(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="d6a1f-113">[Strings Sample](https://msdn.microsoft.com/library/be9e82a3-dc95-4aaa-9396-61b66e467e02(v=vs.100))</span></span>
