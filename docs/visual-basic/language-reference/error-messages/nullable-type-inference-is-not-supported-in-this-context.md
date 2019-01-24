---
title: 이 컨텍스트에서는 nullable 형식을 유추할 수 없습니다.
ms.date: 07/20/2015
f1_keywords:
- vbc36629
- bc36629
helpviewer_keywords:
- BC36629
ms.assetid: 0a1e2dbc-d9a4-433d-9306-c5540782b81d
ms.openlocfilehash: 7dffc5233656257cd892f573a2f8b9f91d781c21
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54611893"
---
# <a name="nullable-type-inference-is-not-supported-in-this-context"></a><span data-ttu-id="260bf-102">이 컨텍스트에서는 nullable 형식을 유추할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="260bf-102">Nullable type inference is not supported in this context</span></span>
<span data-ttu-id="260bf-103">값 형식 및 구조는 nullable 선언할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="260bf-103">Value types and structures can be declared nullable.</span></span>  
  
```vb  
Dim a? As Integer  
Dim b As Integer?  
```  
  
 <span data-ttu-id="260bf-104">그러나 nullable 선언 형식 유추와 함께에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="260bf-104">However, you cannot use the nullable declaration in combination with type inference.</span></span> <span data-ttu-id="260bf-105">다음 예제에서는이 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="260bf-105">The following examples cause this error.</span></span>  
  
```vb  
' Not valid.  
' Dim c? = 10  
' Dim d? = a  
```  
  
 <span data-ttu-id="260bf-106">**오류 ID:** BC36629</span><span class="sxs-lookup"><span data-stu-id="260bf-106">**Error ID:** BC36629</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="260bf-107">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="260bf-107">To correct this error</span></span>  
  
-   <span data-ttu-id="260bf-108">사용 하 여는 `As` 절 null 허용으로 변수를 선언 합니다.</span><span class="sxs-lookup"><span data-stu-id="260bf-108">Use an `As` clause to declare the variable as nullable.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="260bf-109">참고자료</span><span class="sxs-lookup"><span data-stu-id="260bf-109">See also</span></span>
- [<span data-ttu-id="260bf-110">Nullable 값 형식</span><span class="sxs-lookup"><span data-stu-id="260bf-110">Nullable Value Types</span></span>](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
- [<span data-ttu-id="260bf-111">지역 형식 유추</span><span class="sxs-lookup"><span data-stu-id="260bf-111">Local Type Inference</span></span>](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
