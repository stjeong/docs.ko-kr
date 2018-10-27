---
title: '방법: 16진수 문자열을 숫자로 변환(Visual Basic)'
ms.date: 01/31/2018
helpviewer_keywords:
- numbers [Visual Basic], hexadecimals
- hexadecimals [Visual Basic], decimals
- examples [Visual Basic], string conversion
- decimals [Visual Basic], hexadecimals
- string conversion [Visual Basic], hexadecimal to numbers
ms.assetid: 76675807-eadb-4c08-bd50-e6c6ff4b8ced
ms.openlocfilehash: 65184bbb742ad549a8398d55dc7bdeed05a9d973
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50048556"
---
# <a name="how-to-convert-hexadecimal-strings-to-numbers-visual-basic"></a><span data-ttu-id="84d34-102">방법: 16진수 문자열을 숫자로 변환(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="84d34-102">How to: Convert Hexadecimal Strings to Numbers (Visual Basic)</span></span>
<span data-ttu-id="84d34-103">사용 하는 정수를 16 진수 문자열로 변환 하는이 예제는 <xref:System.Convert.ToInt32%2A?displayProperty=nameWithType> 메서드.</span><span class="sxs-lookup"><span data-stu-id="84d34-103">This example converts a hexadecimal string to an integer using the <xref:System.Convert.ToInt32%2A?displayProperty=nameWithType> method.</span></span>  
  
## <a name="to-convert-a-hexadecimal-string-to-a-number"></a><span data-ttu-id="84d34-104">16 진수 문자열을 숫자로 변환 하려면</span><span class="sxs-lookup"><span data-stu-id="84d34-104">To convert a hexadecimal string to a number</span></span>  
  
-   <span data-ttu-id="84d34-105">사용 된 <xref:System.Convert.ToInt32(System.String,System.Int32)> 정수를 16 진수로 표시 된 숫자를 변환 하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="84d34-105">Use the <xref:System.Convert.ToInt32(System.String,System.Int32)> method to convert the number expressed in base-16 to an integer.</span></span>  
  
     <span data-ttu-id="84d34-106">첫 번째 인수는 <xref:System.Convert.ToInt32(System.String,System.Int32)> 메서드는 변환할 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="84d34-106">The first argument of the <xref:System.Convert.ToInt32(System.String,System.Int32)> method is the string to convert.</span></span> <span data-ttu-id="84d34-107">두 번째 인수는 숫자에서 기 수를 나타냅니다. 16 진수는 16입니다.</span><span class="sxs-lookup"><span data-stu-id="84d34-107">The second argument describes what base the number is expressed in; hexadecimal is base 16.</span></span>  
  
     [!code-vb[HexConversion](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-convert-hexadecimal-strings-to-numbers_1.vb)]  

- <span data-ttu-id="84d34-108">16 진수 문자열 제한이 다음 note:</span><span class="sxs-lookup"><span data-stu-id="84d34-108">Note that the hexadecimal string has the following restrictions:</span></span>

   - <span data-ttu-id="84d34-109">포함할 수 없습니다는 `&h` 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="84d34-109">It cannot include the `&h` prefix.</span></span>
   - <span data-ttu-id="84d34-110">포함할 수 없습니다는 `_` 숫자 구분 기호입니다.</span><span class="sxs-lookup"><span data-stu-id="84d34-110">It cannot include the `_` digit separator.</span></span>

   <span data-ttu-id="84d34-111">접두사 또는 숫자 구분 기호 있는 경우에 대 한 호출을 <xref:System.Convert.ToInt32(System.String,System.Int32)> 메서드가 throw를 <xref:System.FormatException>입니다.</span><span class="sxs-lookup"><span data-stu-id="84d34-111">If the prefix or a digit separator is present, the call to the <xref:System.Convert.ToInt32(System.String,System.Int32)> method throws a <xref:System.FormatException>.</span></span>

## <a name="see-also"></a><span data-ttu-id="84d34-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="84d34-112">See Also</span></span>  
 <xref:Microsoft.VisualBasic.Conversion.Hex%2A>  
 <xref:System.Convert.ToInt32%2A?displayProperty=nameWithType>
