---
title: 선택적 매개 변수는 기본값을 지정해야 합니다.
ms.date: 07/20/2015
f1_keywords:
- vbc30812
- bc30812
helpviewer_keywords:
- BC30812
ms.assetid: 5091a250-be66-413b-98a3-2a9974c4d600
ms.openlocfilehash: dbbcc748a65942e3a89785b267e9231f4a4a01a8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54686181"
---
# <a name="optional-parameters-must-specify-a-default-value"></a><span data-ttu-id="68487-102">선택적 매개 변수는 기본값을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="68487-102">Optional parameters must specify a default value</span></span>
<span data-ttu-id="68487-103">선택적 매개 변수는 매개 변수가 없는 호출 프로시저에서 제공 하는 경우 사용할 수 있는 기본 값을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="68487-103">Optional parameters must provide default values that can be used if no parameter is supplied by a calling procedure.</span></span>  
  
 <span data-ttu-id="68487-104">**오류 ID:** BC30812</span><span class="sxs-lookup"><span data-stu-id="68487-104">**Error ID:** BC30812</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="68487-105">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="68487-105">To correct this error</span></span>  
  
-   <span data-ttu-id="68487-106">선택적 매개 변수; 기본값 지정 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="68487-106">Specify default values for optional parameters; for example:</span></span>  
  
    ```  
    Sub Proc1(ByVal X As Integer,   
          Optional ByVal Y As String = "Default Value")  
       MsgBox("Default argument is: " & Y)  
    End Sub  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="68487-107">참고자료</span><span class="sxs-lookup"><span data-stu-id="68487-107">See also</span></span>
- [<span data-ttu-id="68487-108">선택 사항</span><span class="sxs-lookup"><span data-stu-id="68487-108">Optional</span></span>](../../../visual-basic/language-reference/modifiers/optional.md)
