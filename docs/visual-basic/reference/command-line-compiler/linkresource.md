---
title: -linkresource (Visual Basic)
ms.date: 03/10/2018
helpviewer_keywords:
- /linkresource compiler option [Visual Basic]
- -linkresource compiler option [Visual Basic]
- linkresource compiler option [Visual Basic]
- /linkres compiler option [Visual Basic]
- linkres compiler option [Visual Basic]
- -linkres compiler option [Visual Basic]
ms.assetid: cf4dcad8-17b7-404c-9184-29358aa05b15
ms.openlocfilehash: 4f4b3db768b5466f8912b66a0a4709d0f773c1f3
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43554827"
---
# <a name="-linkresource-visual-basic"></a><span data-ttu-id="8cc78-102">-linkresource (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8cc78-102">-linkresource (Visual Basic)</span></span>
<span data-ttu-id="8cc78-103">관리되는 리소스에 대한 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8cc78-103">Creates a link to a managed resource.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8cc78-104">구문</span><span class="sxs-lookup"><span data-stu-id="8cc78-104">Syntax</span></span>  
  
```  
-linkresource:filename[,identifier[,public|private]]  
' -or-  
-linkres:filename[,identifier[,public|private]]  
```  
  
## <a name="arguments"></a><span data-ttu-id="8cc78-105">인수</span><span class="sxs-lookup"><span data-stu-id="8cc78-105">Arguments</span></span>  
 `filename`  
 <span data-ttu-id="8cc78-106">필수.</span><span class="sxs-lookup"><span data-stu-id="8cc78-106">Required.</span></span> <span data-ttu-id="8cc78-107">어셈블리에 연결할 리소스 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc78-107">The resource file to link to the assembly.</span></span> <span data-ttu-id="8cc78-108">파일 이름에 공백이 있으면 이름을 따옴표로 묶습니다 ("").</span><span class="sxs-lookup"><span data-stu-id="8cc78-108">If the file name contains a space, enclose the name in quotation marks (" ").</span></span>  
  
 `identifier`  
 <span data-ttu-id="8cc78-109">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc78-109">Optional.</span></span> <span data-ttu-id="8cc78-110">리소스의 논리적 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc78-110">The logical name for the resource.</span></span> <span data-ttu-id="8cc78-111">리소스를 로드 하는 데 사용 되는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc78-111">The name that is used to load the resource.</span></span> <span data-ttu-id="8cc78-112">기본값은 파일 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc78-112">The default is the name of the file.</span></span> <span data-ttu-id="8cc78-113">파일 인지 공용 또는 개인 어셈블리 매니페스트에서 예를 들어 지정할 수 있습니다: `-linkres:filename.res,myname.res,public`합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc78-113">Optionally, you can specify whether the file is public or private in the assembly manifest, for example: `-linkres:filename.res,myname.res,public`.</span></span> <span data-ttu-id="8cc78-114">기본적으로 `filename` 어셈블리에 공개 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc78-114">By default, `filename` is public in the assembly.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8cc78-115">설명</span><span class="sxs-lookup"><span data-stu-id="8cc78-115">Remarks</span></span>  
 <span data-ttu-id="8cc78-116">`-linkresource` 옵션은 출력 파일에 리소스 파일을 포함 하지 않습니다; 사용을 `-resource` 이 작업을 수행 하는 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc78-116">The `-linkresource` option does not embed the resource file in the output file; use the `-resource` option to do this.</span></span>  
  
 <span data-ttu-id="8cc78-117">`-linkresource` 옵션 중 하나 필요로 합니다 `-target` 이외의 옵션 `-target:module`합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc78-117">The `-linkresource` option requires one of the `-target` options other than `-target:module`.</span></span>  
  
 <span data-ttu-id="8cc78-118">경우 `filename` 는 [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] , 예를 들어에서 만든 리소스 파일을 [Resgen.exe (리소스 파일 생성기)](https://msdn.microsoft.com/library/8ef159de-b660-4bec-9213-c3fbc4d1c6f4) 개발 환경에서의 멤버를 사용 하 여 액세스할 수 있습니다 또는 <xref:System.Resources> 네임 스페이스.</span><span class="sxs-lookup"><span data-stu-id="8cc78-118">If `filename` is a [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] resource file created, for example, by the [Resgen.exe (Resource File Generator)](https://msdn.microsoft.com/library/8ef159de-b660-4bec-9213-c3fbc4d1c6f4) or in the development environment, it can be accessed with members in the <xref:System.Resources> namespace.</span></span> <span data-ttu-id="8cc78-119">자세한 내용은 <xref:System.Resources.ResourceManager>을 참조하세요. 로 시작 하는 메서드를 사용 하 여 런타임 시 다른 모든 리소스에 액세스 하려면 `GetManifestResource` 에 <xref:System.Reflection.Assembly> 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc78-119">(For more information, see <xref:System.Resources.ResourceManager>.) To access all other resources at run time, use the methods that begin with `GetManifestResource` in the <xref:System.Reflection.Assembly> class.</span></span>  
  
 <span data-ttu-id="8cc78-120">모든 파일 형식 파일 이름일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cc78-120">The file name can be any file format.</span></span> <span data-ttu-id="8cc78-121">예를 들어 네이티브 DLL을 어셈블리의 일부로 설정하면 전역 어셈블리 캐시에 설치하고 어셈블리의 관리 코드에서 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cc78-121">For example, you may want to make a native DLL part of the assembly, so that it can be installed into the global assembly cache and accessed from managed code in the assembly.</span></span>  
  
 <span data-ttu-id="8cc78-122">`-linkresource`의 약식은 `-linkres`입니다.</span><span class="sxs-lookup"><span data-stu-id="8cc78-122">The short form of `-linkresource` is `-linkres`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8cc78-123">`-linkresource` 옵션을 Visual Studio 개발 환경에서 사용할 수 없습니다. 즉, 사용 가능한 명령줄에서 컴파일할 때만 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc78-123">The `-linkresource` option is not available from the Visual Studio development environment; it is available only when you compile from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8cc78-124">예제</span><span class="sxs-lookup"><span data-stu-id="8cc78-124">Example</span></span>  
 <span data-ttu-id="8cc78-125">다음 코드 컴파일을 `in.vb` 리소스 파일에 대 한 링크가 `rf.resource`합니다.</span><span class="sxs-lookup"><span data-stu-id="8cc78-125">The following code compiles `in.vb` and links to resource file `rf.resource`.</span></span>  
  
```console  
vbc -linkresource:rf.resource in.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="8cc78-126">참고 항목</span><span class="sxs-lookup"><span data-stu-id="8cc78-126">See Also</span></span>  
 [<span data-ttu-id="8cc78-127">Visual Basic 명령줄 컴파일러</span><span class="sxs-lookup"><span data-stu-id="8cc78-127">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="8cc78-128">-target (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8cc78-128">-target (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/target.md)  
 [<span data-ttu-id="8cc78-129">-리소스 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8cc78-129">-resource (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/resource.md)  
 [<span data-ttu-id="8cc78-130">샘플 컴파일 명령줄</span><span class="sxs-lookup"><span data-stu-id="8cc78-130">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
