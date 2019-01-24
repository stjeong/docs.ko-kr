---
title: -verbose
ms.date: 03/13/2018
helpviewer_keywords:
- verbose compiler option [Visual Basic]
- -verbose compiler option [Visual Basic]
- /verbose compiler option [Visual Basic]
ms.assetid: d1aec0c1-0261-421d-9adc-5b13756100be
ms.openlocfilehash: 7a5dd305d1cc40e57d0f07f383151dc1a965bdda
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54513921"
---
# <a name="-verbose"></a><span data-ttu-id="95a05-102">-verbose</span><span class="sxs-lookup"><span data-stu-id="95a05-102">-verbose</span></span>
<span data-ttu-id="95a05-103">컴파일러에서 상태 및 오류에 대 한 자세한 정보 표시 메시지를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a05-103">Causes the compiler to produce verbose status and error messages.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="95a05-104">구문</span><span class="sxs-lookup"><span data-stu-id="95a05-104">Syntax</span></span>  
  
```  
-verbose[+ | -]  
```  
  
## <a name="arguments"></a><span data-ttu-id="95a05-105">인수</span><span class="sxs-lookup"><span data-stu-id="95a05-105">Arguments</span></span>  
 <span data-ttu-id="95a05-106">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="95a05-106">`+` &#124; `-`</span></span>  
 <span data-ttu-id="95a05-107">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="95a05-107">Optional.</span></span> <span data-ttu-id="95a05-108">지정 `-verbose` 지정 하는 것 같습니다 `-verbose+`는 컴파일러가을 자세한 정보 표시 메시지를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="95a05-108">Specifying `-verbose` is the same as specifying `-verbose+`, which causes the compiler to emit verbose messages.</span></span> <span data-ttu-id="95a05-109">이 옵션의 기본값은 `-verbose-`합니다.</span><span class="sxs-lookup"><span data-stu-id="95a05-109">The default for this option is `-verbose-`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="95a05-110">설명</span><span class="sxs-lookup"><span data-stu-id="95a05-110">Remarks</span></span>  
 <span data-ttu-id="95a05-111">`-verbose` 옵션은 컴파일러에서 생성 한 오류의 총 수에 대 한 정보를 표시, 모듈에서 어셈블리를 로드 하는 보고 및 현재 컴파일 중인 파일을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a05-111">The `-verbose` option displays information about the total number of errors issued by the compiler, reports which assemblies are being loaded by a module, and displays which files are currently being compiled.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="95a05-112">`-verbose` 옵션은 Visual Studio 개발 환경 내에서 사용할 수 있는 명령줄에서 컴파일할 경우에 사용할 수 있는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="95a05-112">The `-verbose` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="95a05-113">예제</span><span class="sxs-lookup"><span data-stu-id="95a05-113">Example</span></span>  
 <span data-ttu-id="95a05-114">다음 코드에서는 `In.vb` 받고 자세한 상태 정보를 표시 하도록 컴파일러에 지시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95a05-114">The following code compiles `In.vb` and directs the compiler to display verbose status information.</span></span>  
  
```console  
vbc -verbose in.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="95a05-115">참고자료</span><span class="sxs-lookup"><span data-stu-id="95a05-115">See also</span></span>
- [<span data-ttu-id="95a05-116">Visual Basic 명령줄 컴파일러</span><span class="sxs-lookup"><span data-stu-id="95a05-116">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="95a05-117">샘플 컴파일 명령줄</span><span class="sxs-lookup"><span data-stu-id="95a05-117">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
