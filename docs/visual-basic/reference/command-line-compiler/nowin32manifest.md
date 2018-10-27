---
title: -nowin32manifest (Visual Basic)
ms.date: 03/13/2018
helpviewer_keywords:
- /nowin32manifest compiler option [Visual Basic]
- nowin32manifest compiler option [Visual Basic]
- -nowin32manifest compiler option [Visual Basic]
ms.assetid: c0528aae-83b3-4425-99f0-19448e9843e3
ms.openlocfilehash: 382e8fd089211f6d23a1e6baff93bf08f19248c8
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50035763"
---
# <a name="-nowin32manifest-visual-basic"></a><span data-ttu-id="46043-102">-nowin32manifest (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="46043-102">-nowin32manifest (Visual Basic)</span></span>
<span data-ttu-id="46043-103">실행 파일에 응용 프로그램 매니페스트를 포함하지 않도록 컴파일러에 지시합니다.</span><span class="sxs-lookup"><span data-stu-id="46043-103">Instructs the compiler not to embed any application manifest into the executable file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="46043-104">구문</span><span class="sxs-lookup"><span data-stu-id="46043-104">Syntax</span></span>  
  
```  
-nowin32manifest  
```  
  
## <a name="remarks"></a><span data-ttu-id="46043-105">설명</span><span class="sxs-lookup"><span data-stu-id="46043-105">Remarks</span></span>  
 <span data-ttu-id="46043-106">이 옵션을 사용하는 경우 Win32 리소스 파일에서 또는 이후 빌드 단계 중에 응용 프로그램 매니페스트를 제공하지 않으면 Windows Vista에서 응용 프로그램에 가상화가 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="46043-106">When this option is used, the application will be subject to virtualization on Windows Vista unless you provide an application manifest in a Win32 Resource file or during a later build step.</span></span> <span data-ttu-id="46043-107">가상화에 대 한 자세한 내용은 참조 하세요. [Windows Vista의 ClickOnce 배포](/visualstudio/deployment/clickonce-deployment-on-windows-vista)합니다.</span><span class="sxs-lookup"><span data-stu-id="46043-107">For more information about virtualization, see [ClickOnce Deployment on Windows Vista](/visualstudio/deployment/clickonce-deployment-on-windows-vista).</span></span>  
  
 <span data-ttu-id="46043-108">매니페스트 생성에 대 한 자세한 내용은 참조 하세요. [-win32manifest (Visual Basic)](../../../visual-basic/reference/command-line-compiler/win32manifest.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="46043-108">For more information about manifest creation, see [-win32manifest (Visual Basic)](../../../visual-basic/reference/command-line-compiler/win32manifest.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46043-109">참고 항목</span><span class="sxs-lookup"><span data-stu-id="46043-109">See Also</span></span>  
 [<span data-ttu-id="46043-110">Visual Basic 명령줄 컴파일러</span><span class="sxs-lookup"><span data-stu-id="46043-110">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="46043-111">프로젝트 디자이너, 응용 프로그램 페이지(Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="46043-111">Application Page, Project Designer (Visual Basic)</span></span>](/visualstudio/ide/reference/application-page-project-designer-visual-basic)
