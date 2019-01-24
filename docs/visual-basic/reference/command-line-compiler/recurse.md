---
title: -recurse
ms.date: 03/13/2018
helpviewer_keywords:
- /recurse compiler option [Visual Basic]
- -recurse compiler option [Visual Basic]
- recurse compiler option [Visual Basic]
ms.assetid: 84a0b670-33ae-44c4-a46a-b90388809317
ms.openlocfilehash: b108a99c799523f3eb50c075a5dc67f0648403fa
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54552335"
---
# <a name="-recurse"></a><span data-ttu-id="33c36-102">-recurse</span><span class="sxs-lookup"><span data-stu-id="33c36-102">-recurse</span></span>
<span data-ttu-id="33c36-103">지정된 된 디렉터리 또는 프로젝트 디렉터리의 모든 자식 디렉터리에 있는 소스 코드 파일을 컴파일합니다.</span><span class="sxs-lookup"><span data-stu-id="33c36-103">Compiles source-code files in all child directories of either the specified directory or the project directory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="33c36-104">구문</span><span class="sxs-lookup"><span data-stu-id="33c36-104">Syntax</span></span>  
  
```  
-recurse:[dir\]file  
```  
  
## <a name="arguments"></a><span data-ttu-id="33c36-105">인수</span><span class="sxs-lookup"><span data-stu-id="33c36-105">Arguments</span></span>  
 `dir`  
 <span data-ttu-id="33c36-106">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="33c36-106">Optional.</span></span> <span data-ttu-id="33c36-107">검색을 시작하려는 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="33c36-107">The directory in which you want the search to begin.</span></span> <span data-ttu-id="33c36-108">지정 하지 않으면 프로젝트 디렉터리에서 검색을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="33c36-108">If not specified, the search begins in the project directory.</span></span>  
  
 `file`  
 <span data-ttu-id="33c36-109">필수 요소.</span><span class="sxs-lookup"><span data-stu-id="33c36-109">Required.</span></span> <span data-ttu-id="33c36-110">검색할 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="33c36-110">The file(s) to search for.</span></span> <span data-ttu-id="33c36-111">와일드카드 문자가 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="33c36-111">Wildcard characters are allowed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="33c36-112">설명</span><span class="sxs-lookup"><span data-stu-id="33c36-112">Remarks</span></span>  
 <span data-ttu-id="33c36-113">사용 하지 않고 프로젝트 디렉터리에서 일치 하는 모든 파일을 컴파일할 파일 이름에 와일드 카드를 사용할 수 있습니다 `-recurse`합니다.</span><span class="sxs-lookup"><span data-stu-id="33c36-113">You can use wildcards in a file name to compile all matching files in the project directory without using `-recurse`.</span></span> <span data-ttu-id="33c36-114">출력 파일 이름은 없으므로 지정 하는 경우 컴파일러 처리 하는 첫 번째 입력된 파일에서 출력 파일 이름으로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33c36-114">If no output file name is specified, the compiler bases the output file name on the first input file processed.</span></span> <span data-ttu-id="33c36-115">이 일반적으로 사전순으로 볼 때 컴파일된 파일 목록에서 첫 번째 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="33c36-115">This is generally the first file in the list of files compiled when viewed alphabetically.</span></span> <span data-ttu-id="33c36-116">이러한 이유로 사용 하 여 출력 파일을 지정 하는 가장 좋은 것은 `-out` 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="33c36-116">For this reason, it is best to specify an output file using the `-out` option.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="33c36-117">`-recurse` 옵션은 Visual Studio 개발 환경 내에서 사용할 수 있는 명령줄에서 컴파일할 경우에 사용할 수 있는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="33c36-117">The `-recurse` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="33c36-118">예제</span><span class="sxs-lookup"><span data-stu-id="33c36-118">Example</span></span>  
 <span data-ttu-id="33c36-119">다음 명령은 현재 디렉터리에 모든 Visual Basic 파일을 컴파일합니다.</span><span class="sxs-lookup"><span data-stu-id="33c36-119">The following command compiles all Visual Basic files in the current directory.</span></span>  
  
```console
vbc *.vb  
```  
  
 <span data-ttu-id="33c36-120">다음 명령에서 모든 Visual Basic 파일을 컴파일하고 합니다 `Test\ABC` 디렉터리와 모든 디렉터리 아래 생성 `Test.ABC.dll`.</span><span class="sxs-lookup"><span data-stu-id="33c36-120">The following command compiles all Visual Basic files in the `Test\ABC` directory and any directories below it, and then generates `Test.ABC.dll`.</span></span>  
  
```console
vbc -target:library -out:Test.ABC.dll -recurse:Test\ABC\*.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="33c36-121">참고자료</span><span class="sxs-lookup"><span data-stu-id="33c36-121">See also</span></span>
- [<span data-ttu-id="33c36-122">Visual Basic 명령줄 컴파일러</span><span class="sxs-lookup"><span data-stu-id="33c36-122">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="33c36-123">-out (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="33c36-123">-out (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/out.md)
- [<span data-ttu-id="33c36-124">샘플 컴파일 명령줄</span><span class="sxs-lookup"><span data-stu-id="33c36-124">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
