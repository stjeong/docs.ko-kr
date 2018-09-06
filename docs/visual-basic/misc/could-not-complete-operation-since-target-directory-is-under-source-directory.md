---
title: 대상 디렉터리가 소스 디렉터리 아래에 있기 때문에 작업을 완료할 수 없습니다.
ms.date: 07/20/2015
f1_keywords:
- vbrIO_CyclicOperation
ms.assetid: 850d3a24-5d51-4ac8-a912-630efcd75278
ms.openlocfilehash: b821034731514362a3725c390e02542b536f0a59
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43890806"
---
# <a name="could-not-complete-operation-since-target-directory-is-under-source-directory"></a><span data-ttu-id="51355-102">대상 디렉터리가 소스 디렉터리 아래에 있기 때문에 작업을 완료할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="51355-102">Could not complete operation since target directory is under source directory</span></span>
<span data-ttu-id="51355-103">순환 작업이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="51355-103">A cyclic operation has failed.</span></span> <span data-ttu-id="51355-104">순환 작업이 계속 실행되므로 완료할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="51355-104">Cyclic operations cycle and therefore cannot complete.</span></span> <span data-ttu-id="51355-105">예를 들어 개체 A는 개체 B에서 상속하려고 하고 개체 B는 개체 A에서 상속하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="51355-105">For example, Object A may attempt to inherit from Object B, which in turn inherits from Object A.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="51355-106">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="51355-106">To correct this error</span></span>  
  
-   <span data-ttu-id="51355-107">상속 시 순환 참조가 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="51355-107">When inheriting, make sure that there are no cyclic references.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="51355-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="51355-108">See Also</span></span>  
 [<span data-ttu-id="51355-109">오류 형식</span><span class="sxs-lookup"><span data-stu-id="51355-109">Error Types</span></span>](../../visual-basic/programming-guide/language-features/error-types.md)  
 [<span data-ttu-id="51355-110">디버깅 기본 사항: 중단점</span><span class="sxs-lookup"><span data-stu-id="51355-110">Debugging Basics: Breakpoints</span></span>](https://msdn.microsoft.com/library/752a02c2-0ac7-4c8b-aa1b-4b2b3b21152e)
