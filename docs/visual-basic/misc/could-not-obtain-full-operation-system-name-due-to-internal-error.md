---
title: 내부 오류로 인해 전체 작업 시스템 이름을 가져올 수 없습니다.
ms.date: 07/20/2015
f1_keywords:
- vbrDiagnosticInfo_FullOSName
ms.assetid: f69da02b-eb9a-4284-bb9e-3025517ae6c1
ms.openlocfilehash: df7a91ea5763c0fe4b7a1993bec29f1b1bb43fcc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54723297"
---
# <a name="could-not-obtain-full-operation-system-name-due-to-internal-error"></a><span data-ttu-id="ee947-102">내부 오류로 인해 전체 작업 시스템 이름을 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ee947-102">Could not obtain full operation system name due to internal error</span></span>
<span data-ttu-id="ee947-103">내부 오류로 인해 전체 작업 시스템 이름을 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ee947-103">Could not obtain full operation system name due to internal error.</span></span> <span data-ttu-id="ee947-104">이는 현재 컴퓨터에 존재하지 않는 WMI에 의해 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee947-104">This might be caused by WMI not existing on the current machine.</span></span>  
  
 <span data-ttu-id="ee947-105">`My.Computer.Info.OSFullName` 속성 호출이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="ee947-105">A call to the `My.Computer.Info.OSFullName` property failed.</span></span> <span data-ttu-id="ee947-106">현재 컴퓨터에 WMI(Windows Management Instrumentation)가 설치되지 않아서 이 오류가 발생했을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee947-106">A possible cause for this failure is if Windows Management Instrumentation (WMI) is not installed on the current computer.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="ee947-107">이 오류를 해결하려면</span><span class="sxs-lookup"><span data-stu-id="ee947-107">To correct this error</span></span>  
  
1.  <span data-ttu-id="ee947-108">`Try...Catch` 속성을 호출하는 주변에 `My.Computer.Info.OSFullName` 블록을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ee947-108">Add a `Try...Catch` block around the call to the `My.Computer.Info.OSFullName` property.</span></span>  
  
2.  <span data-ttu-id="ee947-109">WMI 및 설치 하는 방법에 대 한 자세한 내용은 이동한 후 "Windows Management Instrumentation Core"를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee947-109">For more information about WMI and how to install it, go to  and search for "Windows Management Instrumentation Core".</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ee947-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="ee947-110">See also</span></span>
- [<span data-ttu-id="ee947-111">My.Computer.Info.OSFullName</span><span class="sxs-lookup"><span data-stu-id="ee947-111">My.Computer.Info.OSFullName</span></span>](xref:Microsoft.VisualBasic.Devices.ComputerInfo.OSFullName)
- [<span data-ttu-id="ee947-112">Visual Basic에서 예외 및 오류 처리</span><span class="sxs-lookup"><span data-stu-id="ee947-112">Exception and Error Handling in Visual Basic</span></span>](https://msdn.microsoft.com/library/3e351e73-cf23-40ab-8b60-05794160529e)
- [<span data-ttu-id="ee947-113">Try...Catch...Finally 문</span><span class="sxs-lookup"><span data-stu-id="ee947-113">Try...Catch...Finally Statement</span></span>](../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
