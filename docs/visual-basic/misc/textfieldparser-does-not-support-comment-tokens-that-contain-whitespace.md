---
title: TextFieldParser는 공백이 포함 된 주석 토큰을 지원 하지 않습니다.
ms.date: 07/20/2015
f1_keywords:
- vbrTextFieldParser_WhitespaceInToken
ms.assetid: 55107656-270e-4bbb-841a-478904df8e07
ms.openlocfilehash: a8931d67cd728cf98bc4d83044c65fad6642b021
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/09/2018
ms.locfileid: "44252807"
---
# <a name="textfieldparser-does-not-support-comment-tokens-that-contain-white-space"></a><span data-ttu-id="63ec3-102">TextFieldParser는 공백이 포함 된 주석 토큰을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63ec3-102">TextFieldParser does not support comment tokens that contain white space</span></span>
<span data-ttu-id="63ec3-103">공백이 포함된 주석 토큰이 제공되었습니다.</span><span class="sxs-lookup"><span data-stu-id="63ec3-103">A comment token that contains white space has been supplied.</span></span> <span data-ttu-id="63ec3-104">토큰의 시작 부분에 공백이 발생하지 않는 한 `TextFieldParser` 는 공백을 포함하는 주석 토큰을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63ec3-104">The `TextFieldParser` does not support comment tokens that contain white space unless the white space occurs at the beginning of the token.</span></span> <span data-ttu-id="63ec3-105">토큰의 시작 부분에 있는 공백은 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="63ec3-105">White space occurring at the beginning of a token is ignored.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="63ec3-106">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="63ec3-106">To correct this error</span></span>  
  
-   <span data-ttu-id="63ec3-107">올바른 주석 토큰을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="63ec3-107">Supply a correct comment token.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="63ec3-108">참고자료</span><span class="sxs-lookup"><span data-stu-id="63ec3-108">See also</span></span>

- [<span data-ttu-id="63ec3-109">TextFieldParser.CommentTokens Property</span><span class="sxs-lookup"><span data-stu-id="63ec3-109">TextFieldParser.CommentTokens Property</span></span>](xref:Microsoft.VisualBasic.FileIO.TextFieldParser.CommentTokens%2A)  
- [<span data-ttu-id="63ec3-110">TextFieldParser 개체를 사용하여 텍스트 파일 구문 분석</span><span class="sxs-lookup"><span data-stu-id="63ec3-110">Parsing Text Files with the TextFieldParser Object</span></span>](../../visual-basic/developing-apps/programming/drives-directories-files/parsing-text-files-with-the-textfieldparser-object.md)  
- [<span data-ttu-id="63ec3-111">TextFieldParser 개체</span><span class="sxs-lookup"><span data-stu-id="63ec3-111">TextFieldParser Object</span></span>](../../visual-basic/language-reference/objects/textfieldparser-object.md)
