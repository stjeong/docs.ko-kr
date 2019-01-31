---
title: 기본 속성 '<propertyname1>'은(는) '<propertyname2>'의 기본 속성 '<classname>'과(와) 충돌하므로 'Shadows'로 선언해야 합니다.
ms.date: 07/20/2015
f1_keywords:
- vbc40007
- bc40007
helpviewer_keywords:
- BC40007
ms.assetid: 692ccf76-5715-4f11-a972-84cf9de30bc1
ms.openlocfilehash: bc75b01532ffb112622d7f9bc837490c627883b3
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55270395"
---
# <a name="default-property-propertyname1-conflicts-with-default-property-propertyname2-in-classname-and-so-should-be-declared-shadows"></a><span data-ttu-id="d66a2-102">기본 속성 '\<propertyname1 >' 기본 속성과 충돌 '\<propertyname2 >'에서 '\<classname >' h'로 선언 해야 하므로</span><span class="sxs-lookup"><span data-stu-id="d66a2-102">Default property '\<propertyname1>' conflicts with default property '\<propertyname2>' in '\<classname>' and so should be declared 'Shadows'</span></span>
<span data-ttu-id="d66a2-103">기본 클래스에 정의 된 속성과 동일한 이름을 가진 속성이 선언 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d66a2-103">A property is declared with the same name as a property defined in the base class.</span></span> <span data-ttu-id="d66a2-104">이 이런 경우이 클래스의 속성이 기본 클래스 속성을 숨겨야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d66a2-104">In this situation, the property in this class should shadow the base class property.</span></span>  
  
 <span data-ttu-id="d66a2-105">이 메시지는 경고입니다.</span><span class="sxs-lookup"><span data-stu-id="d66a2-105">This message is a warning.</span></span> <span data-ttu-id="d66a2-106">기본적으로`Shadows` 로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="d66a2-106">`Shadows` is assumed by default.</span></span> <span data-ttu-id="d66a2-107">경고를 숨기거나 오류로 처리하는 방법에 대한 자세한 내용은 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d66a2-107">For more information about hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="d66a2-108">**오류 ID:** BC40007</span><span class="sxs-lookup"><span data-stu-id="d66a2-108">**Error ID:** BC40007</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="d66a2-109">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="d66a2-109">To correct this error</span></span>  
  
-   <span data-ttu-id="d66a2-110">추가 된 `Shadows` 속성의 이름을 선언 되는 선언 또는 변경 하는 키워드입니다.</span><span class="sxs-lookup"><span data-stu-id="d66a2-110">Add the `Shadows` keyword to the declaration, or change the name of the property being declared.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d66a2-111">참고자료</span><span class="sxs-lookup"><span data-stu-id="d66a2-111">See also</span></span>
- [<span data-ttu-id="d66a2-112">Shadows</span><span class="sxs-lookup"><span data-stu-id="d66a2-112">Shadows</span></span>](../../../visual-basic/language-reference/modifiers/shadows.md)
- [<span data-ttu-id="d66a2-113">Visual Basic의 숨김 기능</span><span class="sxs-lookup"><span data-stu-id="d66a2-113">Shadowing in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)
