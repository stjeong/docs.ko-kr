---
title: -moduleassemblyname
ms.date: 03/13/2018
helpviewer_keywords:
- moduleassemblyname compiler option [Visual Basic]
- /moduleassemblyname compiler option [Visual Basic]
- -moduleassemblyname compiler option [Visual Basic]
ms.assetid: 013a57b6-f425-4dd3-b333-512d72c42f55
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 479f9f639548eb81351d1df3f8f08b29b393cba1
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43890885"
---
# <a name="-moduleassemblyname"></a><span data-ttu-id="2a03f-102">-moduleassemblyname</span><span class="sxs-lookup"><span data-stu-id="2a03f-102">-moduleassemblyname</span></span>
<span data-ttu-id="2a03f-103">이 모듈이 속할 어셈블리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2a03f-103">Specifies the name of the assembly that this module will be a part of.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2a03f-104">구문</span><span class="sxs-lookup"><span data-stu-id="2a03f-104">Syntax</span></span>  
  
```  
-moduleassemblyname:assembly_name  
```  
  
## <a name="arguments"></a><span data-ttu-id="2a03f-105">인수</span><span class="sxs-lookup"><span data-stu-id="2a03f-105">Arguments</span></span>  
  
|<span data-ttu-id="2a03f-106">용어</span><span class="sxs-lookup"><span data-stu-id="2a03f-106">Term</span></span>|<span data-ttu-id="2a03f-107">정의</span><span class="sxs-lookup"><span data-stu-id="2a03f-107">Definition</span></span>|  
|---|---|  
|`assembly_name`|<span data-ttu-id="2a03f-108">이 모듈에 포함 될 어셈블리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a03f-108">The name of the assembly that this module will be a part of.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2a03f-109">설명</span><span class="sxs-lookup"><span data-stu-id="2a03f-109">Remarks</span></span>  
 <span data-ttu-id="2a03f-110">컴파일러 프로세스를 `-moduleassemblyname` 경우에만 옵션을 `-target:module` 옵션이 지정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="2a03f-110">The compiler processes the `-moduleassemblyname` option only if the `-target:module` option has been specified.</span></span> <span data-ttu-id="2a03f-111">이렇게 하면 컴파일러는 모듈을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a03f-111">This causes the compiler to create a module.</span></span> <span data-ttu-id="2a03f-112">컴파일러에서 생성 된 모듈은 지정 된 어셈블리에만 유효 합니다 `-moduleassemblyname` 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="2a03f-112">The module created by the compiler is valid only for the assembly specified with the `-moduleassemblyname` option.</span></span> <span data-ttu-id="2a03f-113">다른 어셈블리에 모듈을 배치 하는 경우 런타임 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a03f-113">If you place the module in a different assembly, run-time errors will occur.</span></span>  
  
 <span data-ttu-id="2a03f-114">`-moduleassemblyname` 옵션 다음에 해당할 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a03f-114">The `-moduleassemblyname` option is needed only when the following are true:</span></span>  
  
-   <span data-ttu-id="2a03f-115">모듈의 데이터 형식에 대 한 액세스에 필요한를 `Friend` 참조 된 어셈블리의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="2a03f-115">A data type in the module needs access to a `Friend` type in a referenced assembly.</span></span>  
  
-   <span data-ttu-id="2a03f-116">참조 된 어셈블리에 모듈을 빌드는 어셈블리를 friend 어셈블리 액세스 권한을 부여한 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a03f-116">The referenced assembly has granted friend assembly access to the assembly into which the module will be built.</span></span>  
  
 <span data-ttu-id="2a03f-117">모듈을 만드는 방법에 대 한 자세한 내용은 참조 하세요. [/target (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="2a03f-117">For more information about creating a module, see [/target (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md).</span></span> <span data-ttu-id="2a03f-118">Friend 어셈블리에 대 한 자세한 내용은 참조 하세요. [Friend 어셈블리](../../programming-guide/concepts/assemblies-gac/friend-assemblies.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="2a03f-118">For more information about friend assemblies, see [Friend Assemblies](../../programming-guide/concepts/assemblies-gac/friend-assemblies.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2a03f-119">`-moduleassemblyname` 옵션은 Visual Studio 개발 환경 내에서 사용할 수 없는 경우 즉, 사용할 수 있는 명령 프롬프트에서 컴파일할 때만 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a03f-119">The `-moduleassemblyname` option is not available from within the Visual Studio development environment; it is available only when you compile from a command prompt.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2a03f-120">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2a03f-120">See Also</span></span>  
 [<span data-ttu-id="2a03f-121">방법: 다중 파일 어셈블리 빌드</span><span class="sxs-lookup"><span data-stu-id="2a03f-121">How to: Build a Multifile Assembly</span></span>](../../../framework/app-domains/how-to-build-a-multifile-assembly.md)  
 [<span data-ttu-id="2a03f-122">Visual Basic 명령줄 컴파일러</span><span class="sxs-lookup"><span data-stu-id="2a03f-122">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="2a03f-123">-target (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2a03f-123">-target (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/target.md)  
 [<span data-ttu-id="2a03f-124">-main</span><span class="sxs-lookup"><span data-stu-id="2a03f-124">-main</span></span>](../../../visual-basic/reference/command-line-compiler/main.md)  
 [<span data-ttu-id="2a03f-125">-참조 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2a03f-125">-reference (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/reference.md)  
 [<span data-ttu-id="2a03f-126">-addmodule</span><span class="sxs-lookup"><span data-stu-id="2a03f-126">-addmodule</span></span>](../../../visual-basic/reference/command-line-compiler/addmodule.md)  
 [<span data-ttu-id="2a03f-127">어셈블리 및 전역 어셈블리 캐시</span><span class="sxs-lookup"><span data-stu-id="2a03f-127">Assemblies and the Global Assembly Cache</span></span>](../../../visual-basic/programming-guide/concepts/assemblies-gac/index.md)  
 [<span data-ttu-id="2a03f-128">샘플 컴파일 명령줄</span><span class="sxs-lookup"><span data-stu-id="2a03f-128">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [<span data-ttu-id="2a03f-129">Friend 어셈블리</span><span class="sxs-lookup"><span data-stu-id="2a03f-129">Friend Assemblies</span></span>](../../programming-guide/concepts/assemblies-gac/friend-assemblies.md)
