---
title: -warnaserror (Visual Basic)
ms.date: 03/13/2018
helpviewer_keywords:
- warnaserror compiler option [Visual Basic]
- /warnaserror compiler option [Visual Basic]
- -warnaserror compiler option [Visual Basic]
ms.assetid: 49819f1d-a1bd-4201-affe-5afe6d9712e1
ms.openlocfilehash: 89f6566bd733ff92d464c026102429d3fc5cf0c1
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50047854"
---
# <a name="-warnaserror-visual-basic"></a><span data-ttu-id="71238-102">-warnaserror (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="71238-102">-warnaserror (Visual Basic)</span></span>
<span data-ttu-id="71238-103">컴파일러에서 맨 처음 발견 되는 경고를 오류로 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="71238-103">Causes the compiler to treat the first occurrence of a warning as an error.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="71238-104">구문</span><span class="sxs-lookup"><span data-stu-id="71238-104">Syntax</span></span>  
  
```  
-warnaserror[+ | -][:numberList]  
```  
  
## <a name="arguments"></a><span data-ttu-id="71238-105">인수</span><span class="sxs-lookup"><span data-stu-id="71238-105">Arguments</span></span>  
  
|<span data-ttu-id="71238-106">용어</span><span class="sxs-lookup"><span data-stu-id="71238-106">Term</span></span>|<span data-ttu-id="71238-107">정의</span><span class="sxs-lookup"><span data-stu-id="71238-107">Definition</span></span>|  
|---|---|  
|<span data-ttu-id="71238-108">+ &#124; -</span><span class="sxs-lookup"><span data-stu-id="71238-108">+ &#124; -</span></span>|<span data-ttu-id="71238-109">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="71238-109">Optional.</span></span> <span data-ttu-id="71238-110">기본적으로 `-warnaserror-` 은 적용 경고 해도 컴파일러에서 출력 파일을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="71238-110">By default, `-warnaserror-` is in effect; warnings do not prevent the compiler from producing an output file.</span></span> <span data-ttu-id="71238-111">합니다 `-warnaserror` 동일한 옵션으로 `-warnaserror+`, 경고가 오류로 처리 되도록 하면 합니다.</span><span class="sxs-lookup"><span data-stu-id="71238-111">The `-warnaserror` option, which is the same as `-warnaserror+`, causes warnings to be treated as errors.</span></span>|  
|`numberList`|<span data-ttu-id="71238-112">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="71238-112">Optional.</span></span> <span data-ttu-id="71238-113">경고 ID의 쉼표로 구분 된 목록에는 숫자는 `-warnaserror` 옵션은 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="71238-113">Comma-delimited list of the warning ID numbers to which the `-warnaserror` option applies.</span></span> <span data-ttu-id="71238-114">경고 ID가 없습니다. 지정 된 경우는 `-warnaserror` 옵션은 모든 경고에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="71238-114">If no warning ID is specified, the `-warnaserror` option applies to all warnings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="71238-115">설명</span><span class="sxs-lookup"><span data-stu-id="71238-115">Remarks</span></span>  
 <span data-ttu-id="71238-116">`-warnaserror` 옵션 모든 경고를 오류로 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="71238-116">The `-warnaserror` option treats all warnings as errors.</span></span> <span data-ttu-id="71238-117">일반적으로 보고 됩니다. 경고 대신 오류로 보고 되는 모든 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="71238-117">Any messages that would ordinarily be reported as warnings are instead reported as errors.</span></span> <span data-ttu-id="71238-118">컴파일러 경고로 동일한 경고를 계속 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="71238-118">The compiler reports subsequent occurrences of the same warning as warnings.</span></span>  
  
 <span data-ttu-id="71238-119">기본적으로 `-warnaserror-` 만 정보를 경고 하면 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="71238-119">By default, `-warnaserror-` is in effect, which causes the warnings to be informational only.</span></span> <span data-ttu-id="71238-120">합니다 `-warnaserror` 동일한 옵션으로 `-warnaserror+`, 경고가 오류로 처리 되도록 하면 합니다.</span><span class="sxs-lookup"><span data-stu-id="71238-120">The `-warnaserror` option, which is the same as `-warnaserror+`, causes warnings to be treated as errors.</span></span>  
  
 <span data-ttu-id="71238-121">특정 경고만 오류로 처리를 하려는 경우 오류로 처리할 경고 번호의 쉼표로 구분 된 목록을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71238-121">If you want only a few specific warnings to be treated as errors, you may specify a comma-separated list of warning numbers to treat as errors.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="71238-122">`-warnaserror` 옵션에 경고가 표시 되는 방식을 제어 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71238-122">The `-warnaserror` option does not control how warnings are displayed.</span></span> <span data-ttu-id="71238-123">사용 된 [-nowarn](../../../visual-basic/reference/command-line-compiler/nowarn.md) 경고를 사용 하지 않도록 설정 하는 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="71238-123">Use the [-nowarn](../../../visual-basic/reference/command-line-compiler/nowarn.md) option to disable warnings.</span></span>  
  
|<span data-ttu-id="71238-124">-Warnaserror를 Visual Studio IDE에서 모든 경고를 오류로 처리를 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="71238-124">To set -warnaserror to treat all warnings as errors in the Visual Studio IDE</span></span>|  
|---|  
|<span data-ttu-id="71238-125">1.  **솔루션 탐색기**에서 프로젝트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="71238-125">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="71238-126">**프로젝트** 메뉴에서 **속성**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="71238-126">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="71238-127">2.  **컴파일** 탭을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="71238-127">2.  Click the **Compile** tab.</span></span><br /><span data-ttu-id="71238-128">3.  있는지 확인 합니다 **모든 경고 사용 안 함** 확인 확인란이 선택 되지 않은 합니다.</span><span class="sxs-lookup"><span data-stu-id="71238-128">3.  Make sure the **Disable all warnings** check box is unchecked.</span></span><br /><span data-ttu-id="71238-129">4.  확인 합니다 **모든 경고를 오류로 처리** 확인란 합니다.</span><span class="sxs-lookup"><span data-stu-id="71238-129">4.  Check the **Treat all warnings as errors** check box.</span></span>|  
  
|<span data-ttu-id="71238-130">-Warnaserror 특정 경고 Visual Studio IDE에서 오류를 처리 하도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="71238-130">To set -warnaserror to treat specific warnings as errors in the Visual Studio IDE</span></span>|  
|---|  
|<span data-ttu-id="71238-131">1.  **솔루션 탐색기**에서 프로젝트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="71238-131">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="71238-132">**프로젝트** 메뉴에서 **속성**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="71238-132">On the **Project** menu, click **Properties**.</span></span><br /><span data-ttu-id="71238-133">2.  **컴파일** 탭을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="71238-133">2.  Click the **Compile** tab.</span></span><br /><span data-ttu-id="71238-134">3.  있는지 확인 합니다 **모든 경고 사용 안 함** 확인 확인란이 선택 되지 않은 합니다.</span><span class="sxs-lookup"><span data-stu-id="71238-134">3.  Make sure the **Disable all warnings** check box is unchecked.</span></span><br /><span data-ttu-id="71238-135">4.  있는지 확인 합니다 **모든 경고를 오류로 처리** 확인 확인란이 선택 되지 않은 합니다.</span><span class="sxs-lookup"><span data-stu-id="71238-135">4.  Make sure the **Treat all warnings as errors** check box is unchecked.</span></span><br /><span data-ttu-id="71238-136">5.  선택 **오류** 에서 합니다 **알림** 경고를 오류로 처리 되어야 하는 인접 한 열입니다.</span><span class="sxs-lookup"><span data-stu-id="71238-136">5.  Select **Error** from the **Notification** column adjacent to the warning that should be treated as an error.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="71238-137">예제</span><span class="sxs-lookup"><span data-stu-id="71238-137">Example</span></span>  
 <span data-ttu-id="71238-138">다음 코드에서는 `In.vb` 를 처음으로 찾은 모든 경고에 대 한 오류를 표시 하도록 컴파일러에 지시 합니다.</span><span class="sxs-lookup"><span data-stu-id="71238-138">The following code compiles `In.vb` and directs the compiler to display an error for the first occurrence of every warning it finds.</span></span>  
  
```console
vbc -warnaserror in.vb  
```  
  
## <a name="example"></a><span data-ttu-id="71238-139">예제</span><span class="sxs-lookup"><span data-stu-id="71238-139">Example</span></span>  
 <span data-ttu-id="71238-140">다음 코드에서는 `T2.vb` 만 사용 하지 않는 로컬 변수 (42024)에 대 한 경고를 오류로 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="71238-140">The following code compiles `T2.vb` and treats only the warning for unused local variables (42024) as an error.</span></span>  
  
```console
vbc -warnaserror:42024 t2.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="71238-141">참고 항목</span><span class="sxs-lookup"><span data-stu-id="71238-141">See Also</span></span>  
 [<span data-ttu-id="71238-142">Visual Basic 명령줄 컴파일러</span><span class="sxs-lookup"><span data-stu-id="71238-142">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="71238-143">샘플 컴파일 명령줄</span><span class="sxs-lookup"><span data-stu-id="71238-143">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [<span data-ttu-id="71238-144">Configuring Warnings in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="71238-144">Configuring Warnings in Visual Basic</span></span>](/visualstudio/ide/configuring-warnings-in-visual-basic)
