---
title: XML 주석 예외에는 'cref' 특성이 있어야 합니다.
ms.date: 07/20/2015
f1_keywords:
- bc42319
- vbc42319
helpviewer_keywords:
- BC42319
ms.assetid: 62eeeba3-6811-48be-b1ef-c2e4feda3177
ms.openlocfilehash: a11bfe261ffb8ded95f2e513aaddf00aa00f702e
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55266639"
---
# <a name="xml-comment-exception-must-have-a-cref-attribute"></a><span data-ttu-id="da5f6-102">XML 주석 예외에는 'cref' 특성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da5f6-102">XML comment exception must have a 'cref' attribute</span></span>
<span data-ttu-id="da5f6-103">\<예외 > 태그는 메서드에서 throw 될 수 있는 예외를 문서화 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="da5f6-103">The \<exception> tag provides a way to document the exceptions that may be thrown by a method.</span></span> <span data-ttu-id="da5f6-104">필수 `cref` 특성 설명서 생성기에서 확인 하는 멤버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da5f6-104">The required `cref` attribute designates the name of a member, which is checked by the documentation generator.</span></span> <span data-ttu-id="da5f6-105">멤버가 있는 경우 문서 파일의 정식 요소 이름으로 변환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da5f6-105">If the member exists, it is translated to the canonical element name in the documentation file.</span></span>  
  
 <span data-ttu-id="da5f6-106">**오류 ID:** BC42319</span><span class="sxs-lookup"><span data-stu-id="da5f6-106">**Error ID:** BC42319</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="da5f6-107">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="da5f6-107">To correct this error</span></span>  
  
-   <span data-ttu-id="da5f6-108">추가 된 `cref` 예외에 특성을 다음과 같이 합니다.</span><span class="sxs-lookup"><span data-stu-id="da5f6-108">Add the `cref` attribute to the exception as follows:</span></span>  
  
    ```  
    '''<exception cref="member">description</exception>  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="da5f6-109">참고자료</span><span class="sxs-lookup"><span data-stu-id="da5f6-109">See also</span></span>
- [<span data-ttu-id="da5f6-110">\<exception></span><span class="sxs-lookup"><span data-stu-id="da5f6-110">\<exception></span></span>](../../../visual-basic/language-reference/xmldoc/exception.md)
- [<span data-ttu-id="da5f6-111">방법: XML 문서 만들기</span><span class="sxs-lookup"><span data-stu-id="da5f6-111">How to: Create XML Documentation</span></span>](../../../visual-basic/programming-guide/program-structure/how-to-create-xml-documentation.md)
- [<span data-ttu-id="da5f6-112">XML 주석 태그</span><span class="sxs-lookup"><span data-stu-id="da5f6-112">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
