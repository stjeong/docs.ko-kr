---
title: 기본 속성 &#39; &lt;propertyname1&gt; &#39; 기본 속성과 충돌 &#39; &lt;propertyname2&gt; &#39; 에서 &#39; &lt;classname&gt; &#39;로 선언 해야 하므로 &#39;그림자&#39;
ms.date: 07/20/2015
f1_keywords:
- vbc40007
- bc40007
helpviewer_keywords:
- BC40007
ms.assetid: 692ccf76-5715-4f11-a972-84cf9de30bc1
ms.openlocfilehash: 3099467fa3c5a162c13c9235fb8d55375953ba3a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54521428"
---
# <a name="default-property-39ltpropertyname1gt39-conflicts-with-default-property-39ltpropertyname2gt39-in-39ltclassnamegt39-and-so-should-be-declared-39shadows39"></a><span data-ttu-id="ab671-102">기본 속성 &#39; &lt;propertyname1&gt; &#39; 기본 속성과 충돌 &#39; &lt;propertyname2&gt; &#39; 에서 &#39; &lt;classname&gt; &#39;로 선언 해야 하므로 &#39;그림자&#39;</span><span class="sxs-lookup"><span data-stu-id="ab671-102">Default property &#39;&lt;propertyname1&gt;&#39; conflicts with default property &#39;&lt;propertyname2&gt;&#39; in &#39;&lt;classname&gt;&#39; and so should be declared &#39;Shadows&#39;</span></span>
<span data-ttu-id="ab671-103">기본 클래스에 정의 된 속성과 동일한 이름을 가진 속성이 선언 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab671-103">A property is declared with the same name as a property defined in the base class.</span></span> <span data-ttu-id="ab671-104">이 이런 경우이 클래스의 속성이 기본 클래스 속성을 숨겨야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab671-104">In this situation, the property in this class should shadow the base class property.</span></span>  
  
 <span data-ttu-id="ab671-105">이 메시지는 경고입니다.</span><span class="sxs-lookup"><span data-stu-id="ab671-105">This message is a warning.</span></span> <span data-ttu-id="ab671-106">기본적으로`Shadows` 로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab671-106">`Shadows` is assumed by default.</span></span> <span data-ttu-id="ab671-107">경고를 숨기거나 오류로 처리하는 방법에 대한 자세한 내용은 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ab671-107">For more information about hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="ab671-108">**오류 ID:** BC40007</span><span class="sxs-lookup"><span data-stu-id="ab671-108">**Error ID:** BC40007</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="ab671-109">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="ab671-109">To correct this error</span></span>  
  
-   <span data-ttu-id="ab671-110">추가 된 `Shadows` 속성의 이름을 선언 되는 선언 또는 변경 하는 키워드입니다.</span><span class="sxs-lookup"><span data-stu-id="ab671-110">Add the `Shadows` keyword to the declaration, or change the name of the property being declared.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab671-111">참고자료</span><span class="sxs-lookup"><span data-stu-id="ab671-111">See also</span></span>
- [<span data-ttu-id="ab671-112">Shadows</span><span class="sxs-lookup"><span data-stu-id="ab671-112">Shadows</span></span>](../../../visual-basic/language-reference/modifiers/shadows.md)
- [<span data-ttu-id="ab671-113">Visual Basic의 숨김 기능</span><span class="sxs-lookup"><span data-stu-id="ab671-113">Shadowing in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)
