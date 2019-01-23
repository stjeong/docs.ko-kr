---
title: Stop 문(Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Stop
helpviewer_keywords:
- breakpoints, Stop statements
- Stop statements [Visual Basic], syntax
- Stop statements [Visual Basic]
- execution [Visual Basic], suspending
- processing, interrupting
- processes, interrupting
- execution [Visual Basic], stopping
ms.assetid: c9a9fde0-d649-4662-9bef-bd0146ebc2a7
ms.openlocfilehash: fa9a1942903dff6f673d87b67ebcad047a410425
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54624784"
---
# <a name="stop-statement-visual-basic"></a><span data-ttu-id="d3a65-102">Stop 문(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d3a65-102">Stop Statement (Visual Basic)</span></span>
<span data-ttu-id="d3a65-103">실행을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3a65-103">Suspends execution.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d3a65-104">구문</span><span class="sxs-lookup"><span data-stu-id="d3a65-104">Syntax</span></span>  
  
```  
Stop  
```  
  
## <a name="remarks"></a><span data-ttu-id="d3a65-105">설명</span><span class="sxs-lookup"><span data-stu-id="d3a65-105">Remarks</span></span>  
 <span data-ttu-id="d3a65-106">배치할 수 있습니다 `Stop` 어디서 나 실행을 일시 중단 하는 절차에에서는 문입니다.</span><span class="sxs-lookup"><span data-stu-id="d3a65-106">You can place `Stop` statements anywhere in procedures to suspend execution.</span></span> <span data-ttu-id="d3a65-107">사용 하 여 `Stop` 문을 코드에 중단점을 설정 하는 것과 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="d3a65-107">Using the `Stop` statement is similar to setting a breakpoint in the code.</span></span>  
  
 <span data-ttu-id="d3a65-108">합니다 `Stop` 문을 달리 하지만 실행을 일시 중단 `End`, 파일을 모두 닫고 하거나 컴파일된 실행 파일 (.exe) 파일에 없는 경우 변수를 지우지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3a65-108">The `Stop` statement suspends execution, but unlike `End`, it does not close any files or clear any variables, unless it is encountered in a compiled executable (.exe) file.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d3a65-109">경우는 `Stop` 통합된 개발 환경 (IDE) 외부에서 실행 되는 코드에서 문이, 디버거가 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3a65-109">If the `Stop` statement is encountered in code that is running outside of the integrated development environment (IDE), the debugger is invoked.</span></span> <span data-ttu-id="d3a65-110">코드 디버그 또는 정식 버전 모드로 컴파일된 여부에 관계 없이 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="d3a65-110">This is true regardless of whether the code was compiled in debug or retail mode.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d3a65-111">예제</span><span class="sxs-lookup"><span data-stu-id="d3a65-111">Example</span></span>  
 <span data-ttu-id="d3a65-112">이 예제에서는 합니다 `Stop` 각 반복에 대 한 실행을 일시 중단 하는 문을 `For...Next` 루프입니다.</span><span class="sxs-lookup"><span data-stu-id="d3a65-112">This example uses the `Stop` statement to suspend execution for each iteration through the `For...Next` loop.</span></span>  
  
 [!code-vb[VbVbalrStatements#56](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/stop-statement_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="d3a65-113">참고자료</span><span class="sxs-lookup"><span data-stu-id="d3a65-113">See also</span></span>
- [<span data-ttu-id="d3a65-114">End 문</span><span class="sxs-lookup"><span data-stu-id="d3a65-114">End Statement</span></span>](../../../visual-basic/language-reference/statements/end-statement.md)
