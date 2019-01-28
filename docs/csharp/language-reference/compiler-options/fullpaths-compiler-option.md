---
title: -fullpaths(C# 컴파일러 옵션)
ms.date: 07/20/2015
f1_keywords:
- /fullpaths
helpviewer_keywords:
- /fullpaths compiler option [C#]
- absolute paths [C#]
- fullpaths compiler option [C#]
- full paths [C#]
- -fullpaths compiler option [C#]
ms.assetid: d2a5f857-cbb2-430b-879c-d648aaf0b8c4
ms.openlocfilehash: 160938e631d9f9e49d53bbec8806c7a134864701
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54637687"
---
# <a name="-fullpaths-c-compiler-options"></a><span data-ttu-id="e0ed1-102">-fullpaths(C# 컴파일러 옵션)</span><span class="sxs-lookup"><span data-stu-id="e0ed1-102">-fullpaths (C# Compiler Options)</span></span>
<span data-ttu-id="e0ed1-103">**-fullpaths** 옵션을 사용하면 컴파일러에서는 컴파일 오류 및 경고 목록을 만들때 파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e0ed1-103">The **-fullpaths** option causes the compiler to specify the full path to the file when listing compilation errors and warnings.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e0ed1-104">구문</span><span class="sxs-lookup"><span data-stu-id="e0ed1-104">Syntax</span></span>  
  
```console  
-fullpaths  
```  
  
## <a name="remarks"></a><span data-ttu-id="e0ed1-105">주의</span><span class="sxs-lookup"><span data-stu-id="e0ed1-105">Remarks</span></span>  
 <span data-ttu-id="e0ed1-106">기본적으로 컴파일 도중 발생하는 오류와 경고에서는 오류가 발견된 파일의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e0ed1-106">By default, errors and warnings that result from compilation specify the name of the file in which an error was found.</span></span> <span data-ttu-id="e0ed1-107">**-fullpaths** 옵션을 사용하면 컴파일러에서는 파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e0ed1-107">The **-fullpaths** option causes the compiler to specify the full path to the file.</span></span>  
  
 <span data-ttu-id="e0ed1-108">이 컴파일러 옵션은 Visual Studio에서 사용할 수 없으며 프로그래밍 방식으로 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e0ed1-108">This compiler option is unavailable in Visual Studio and cannot be changed programmatically.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e0ed1-109">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e0ed1-109">See also</span></span>

- [<span data-ttu-id="e0ed1-110">C# 컴파일러 옵션</span><span class="sxs-lookup"><span data-stu-id="e0ed1-110">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)
