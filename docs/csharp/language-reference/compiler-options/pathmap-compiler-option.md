---
title: -pathmap(C# 컴파일러 옵션)
ms.date: 05/16/2018
f1_keywords:
- /pathmap
helpviewer_keywords:
- -pathmap compiler option [C#]
- pathmap compiler option [C#]
- /pathmap compiler option [C#]
ms.openlocfilehash: 277ab8e094f28fd5e3cbba4de12e742bb9614730
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43475922"
---
# <a name="-pathmap-c-compiler-options"></a><span data-ttu-id="28668-102">-pathmap(C# 컴파일러 옵션)</span><span class="sxs-lookup"><span data-stu-id="28668-102">-pathmap (C# Compiler Options)</span></span>

<span data-ttu-id="28668-103">**-pathmap** 컴파일러 옵션은 실제 경로를 컴파일러에서 출력되는 소스 경로 이름에 매핑하는 방법을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="28668-103">The **-pathmap** compiler option specifies how to map physical paths to source path names output by the compiler.</span></span>

## <a name="syntax"></a><span data-ttu-id="28668-104">구문</span><span class="sxs-lookup"><span data-stu-id="28668-104">Syntax</span></span>

```console
-pathmap:path1=sourcePath1,path2=sourcePath2
```

## <a name="arguments"></a><span data-ttu-id="28668-105">인수</span><span class="sxs-lookup"><span data-stu-id="28668-105">Arguments</span></span>

 <span data-ttu-id="28668-106">`path1` 현재 환경에서 소스 파일의 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="28668-106">`path1` The full path to the source files in the current environment</span></span>

 <span data-ttu-id="28668-107">`sourcePath1` 출력 파일에서 `path1`을 대체하는 소스 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="28668-107">`sourcePath1` The source path substituted for `path1` in any output files.</span></span>

<span data-ttu-id="28668-108">매핑되는 소스 경로를 여럿 지정하려면 각각을 쉼표로 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="28668-108">To specify multiple mapped source paths, separate each with a comma.</span></span>

## <a name="remarks"></a><span data-ttu-id="28668-109">설명</span><span class="sxs-lookup"><span data-stu-id="28668-109">Remarks</span></span>

<span data-ttu-id="28668-110">컴파일러가 출력에 소스 경로를 쓰는 이유는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="28668-110">The compiler writes the source path path into its output for the following reasons:</span></span>

1. <span data-ttu-id="28668-111">선택적 매개 변수에 <xref:System.Runtime.CompilerServices.CallerFilePathAttribute>를 적용할 때 소스 경로가 인수 대신 사용되는 경우</span><span class="sxs-lookup"><span data-stu-id="28668-111">The source path is substituted for an argument when the <xref:System.Runtime.CompilerServices.CallerFilePathAttribute> is applied to an optional parameter.</span></span>
1. <span data-ttu-id="28668-112">소스 경로가 PDB 파일에 포함된 경우</span><span class="sxs-lookup"><span data-stu-id="28668-112">The source path is embedded in a PDB file.</span></span>
1. <span data-ttu-id="28668-113">PDB 파일의 경로가 PE(이식 가능한 실행 파일) 파일에 포함된 경우</span><span class="sxs-lookup"><span data-stu-id="28668-113">The path of the PDB file is embedded into a PE (portable executable) file.</span></span>

<span data-ttu-id="28668-114">이 옵션은 컴파일러가 실행되는 컴퓨터의 실제 경로 각각을 출력 파일에 써야 하는 해당 경로에 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="28668-114">This option maps each physical path on the machine where the compiler runs to a corresponding path that should be written in the output files.</span></span>

## <a name="example"></a><span data-ttu-id="28668-115">예</span><span class="sxs-lookup"><span data-stu-id="28668-115">Example</span></span>

<span data-ttu-id="28668-116">**C:\\work\\tests** 디렉터리에 `t.cs`를 컴파일하고 출력에서 디렉터리를 **\publish**에 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="28668-116">Compile `t.cs` in the directory **C:\\work\\tests** and map that directory to **\publish** in the output:</span></span>

```console
csc -pathmap:C:\work\tests=\publish t.cs
```

## <a name="see-also"></a><span data-ttu-id="28668-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="28668-117">See also</span></span>

- [<span data-ttu-id="28668-118">C# 컴파일러 옵션</span><span class="sxs-lookup"><span data-stu-id="28668-118">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)  
- [<span data-ttu-id="28668-119">프로젝트 및 솔루션 속성 관리</span><span class="sxs-lookup"><span data-stu-id="28668-119">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)
