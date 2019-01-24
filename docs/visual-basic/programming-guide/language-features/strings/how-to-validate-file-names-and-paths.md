---
title: '방법: 파일 이름 및 Visual Basic에서 경로 확인'
ms.date: 07/20/2015
helpviewer_keywords:
- file names [Visual Basic], validating
- strings [Visual Basic], validating
- Boolean values [Visual Basic]
- paths [Visual Basic], validating
ms.assetid: f673462d-57b7-4120-b13a-6a7592f7ab2c
ms.openlocfilehash: c0d39ecbaf9ca23c72e45b8839d268fbc38fe48e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54648452"
---
# <a name="how-to-validate-file-names-and-paths-in-visual-basic"></a><span data-ttu-id="857a8-102">방법: 파일 이름 및 Visual Basic에서 경로 확인</span><span class="sxs-lookup"><span data-stu-id="857a8-102">How to: Validate File Names and Paths in Visual Basic</span></span>
<span data-ttu-id="857a8-103">이 예는 `Boolean` 문자열로 파일 이름이 나 경로 나타내는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="857a8-103">This example returns a `Boolean` value that indicates whether a string represents a file name or path.</span></span> <span data-ttu-id="857a8-104">유효성 검사 이름을 파일 시스템에서 허용 되지 않는 문자를 포함 하는 경우를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="857a8-104">The validation checks if the name contains characters that are not allowed by the file system.</span></span>  
  
## <a name="example"></a><span data-ttu-id="857a8-105">예제</span><span class="sxs-lookup"><span data-stu-id="857a8-105">Example</span></span>  
 [!code-vb[VbVbcnRegEx#4](../../../../visual-basic/programming-guide/language-features/strings/codesnippet/VisualBasic/how-to-validate-file-names-and-paths_1.vb)]  
  
 <span data-ttu-id="857a8-106">이 예제는 콜론 또는 디렉터리 이름이 없는 이름을 올바르게 배치가 아니면 이름의 길이 시스템 정의 최대 길이 초과 하는 경우를 확인 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="857a8-106">This example does not check if the name has incorrectly placed colons, or directories with no name, or if the length of the name exceeds the system-defined maximum length.</span></span> <span data-ttu-id="857a8-107">또한 확인 하지 않습니다 응용 프로그램은 지정 된 이름의 파일 시스템 리소스에 액세스 하는 경우.</span><span class="sxs-lookup"><span data-stu-id="857a8-107">It also does not check if the application has permission to access the file-system resource with the specified name.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="857a8-108">참고자료</span><span class="sxs-lookup"><span data-stu-id="857a8-108">See also</span></span>
- <xref:System.IO.Path.GetInvalidPathChars%2A>
- [<span data-ttu-id="857a8-109">Visual Basic의 문자열 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="857a8-109">Validating Strings in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/validating-strings.md)
