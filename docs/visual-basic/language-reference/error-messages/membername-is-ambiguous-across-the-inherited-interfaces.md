---
title: "'<membername>'은(는) 상속된 인터페이스 '<interfacename1>' 및 '<interfacename2>'에서 모호합니다."
ms.date: 07/20/2015
f1_keywords:
- vbc30685
- bc30685
helpviewer_keywords:
- BC30685
ms.assetid: 756add7a-23d5-4b4f-a48d-8297d6459c73
ms.openlocfilehash: 1548c9894d476cc4b92d6581362d309e7b4d00d4
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55264997"
---
# <a name="membername-is-ambiguous-across-the-inherited-interfaces-interfacename1-and-interfacename2"></a><span data-ttu-id="5d8a1-102">'\<membername >' 상속 된 인터페이스에서 모호\<interfacename1 >' 및 '\<interfacename2 >'</span><span class="sxs-lookup"><span data-stu-id="5d8a1-102">'\<membername>' is ambiguous across the inherited interfaces '\<interfacename1>' and '\<interfacename2>'</span></span>
<span data-ttu-id="5d8a1-103">여러 인터페이스에서 동일한 이름의 두 개 이상의 멤버를 상속 하는 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="5d8a1-103">The interface inherits two or more members with the same name from multiple interfaces.</span></span>  
  
 <span data-ttu-id="5d8a1-104">**오류 ID:** BC30685</span><span class="sxs-lookup"><span data-stu-id="5d8a1-104">**Error ID:** BC30685</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="5d8a1-105">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="5d8a1-105">To correct this error</span></span>  
  
-   <span data-ttu-id="5d8a1-106">사용 하려는 기본 인터페이스 값 캐스팅 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="5d8a1-106">Cast the value to the base interface that you want to use; for example:</span></span>  
  
    ```  
    Interface Left  
        Sub MySub()  
    End Interface  
  
    Interface Right  
        Sub MySub()  
    End Interface  
  
    Interface LeftRight  
        Inherits Left, Right  
    End Interface  
  
    Module test  
        Sub Main()  
            Dim x As LeftRight  
            ' x.MySub()  'x is ambiguous.  
            CType(x, Left).MySub() ' Cast to base type.  
            CType(x, Right).MySub() ' Call the other base type.  
        End Sub  
    End Module  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="5d8a1-107">참고자료</span><span class="sxs-lookup"><span data-stu-id="5d8a1-107">See also</span></span>
- [<span data-ttu-id="5d8a1-108">인터페이스</span><span class="sxs-lookup"><span data-stu-id="5d8a1-108">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
