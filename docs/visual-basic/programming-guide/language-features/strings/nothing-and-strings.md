---
title: Visual Basic의 Nothing 및 문자열
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], Nothing
ms.assetid: 261380af-2024-4ecf-823b-43b1034d92cd
ms.openlocfilehash: 65a69861c2a74a3191a45eb782a97f289b0c0726
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54574172"
---
# <a name="nothing-and-strings-in-visual-basic"></a><span data-ttu-id="fdd82-102">Visual Basic의 Nothing 및 문자열</span><span class="sxs-lookup"><span data-stu-id="fdd82-102">Nothing and Strings in Visual Basic</span></span>
<span data-ttu-id="fdd82-103">Visual Basic 런타임 및 [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] 평가 `Nothing` 다르게는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="fdd82-103">The Visual Basic runtime and the [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] evaluate `Nothing` differently when it comes to strings.</span></span>  
  
## <a name="visual-basic-runtime-and-the-net-framework"></a><span data-ttu-id="fdd82-104">Visual Basic 런타임 및.NET Framework</span><span class="sxs-lookup"><span data-stu-id="fdd82-104">Visual Basic Runtime and the .NET Framework</span></span>  
 <span data-ttu-id="fdd82-105">다음 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fdd82-105">Consider the following example:</span></span>  
  
 [!code-vb[VbVbalrStrings#47](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/nothing-and-strings_1.vb)]  
  
 <span data-ttu-id="fdd82-106">Visual Basic 런타임 일반적으로 평가 `Nothing` 을 빈 문자열 ("").</span><span class="sxs-lookup"><span data-stu-id="fdd82-106">The Visual Basic runtime usually evaluates `Nothing` as an empty string ("").</span></span> <span data-ttu-id="fdd82-107">그러나 합니다 [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] 하지 않는 문자열 작업을 수행 하려고 시도 될 때마다 예외를 throw 및 `Nothing`합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd82-107">The [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] does not, however, and throws an exception whenever an attempt is made to perform a string operation on `Nothing`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fdd82-108">참고자료</span><span class="sxs-lookup"><span data-stu-id="fdd82-108">See also</span></span>
- [<span data-ttu-id="fdd82-109">Visual Basic의 문자열 소개</span><span class="sxs-lookup"><span data-stu-id="fdd82-109">Introduction to Strings in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)
