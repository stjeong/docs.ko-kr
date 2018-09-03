---
title: '#pragma warning(C# 참조)'
ms.date: 07/20/2015
f1_keywords:
- '#pragma warning'
helpviewer_keywords:
- '#pragma warning [C#]'
ms.assetid: 723493d5-9753-4cec-babb-54e2b8eb36b6
ms.openlocfilehash: 89ff8151d55ac58a1b114f7727297704ce26b9a7
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43481932"
---
# <a name="pragma-warning-c-reference"></a><span data-ttu-id="6ff51-102">#pragma warning(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="6ff51-102">#pragma warning (C# Reference)</span></span>
<span data-ttu-id="6ff51-103">`#pragma warning`은 특정 경고를 사용하거나 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ff51-103">`#pragma warning` can enable or disable certain warnings.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6ff51-104">구문</span><span class="sxs-lookup"><span data-stu-id="6ff51-104">Syntax</span></span>  
  
```csharp
#pragma warning disable warning-list  
#pragma warning restore warning-list  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6ff51-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6ff51-105">Parameters</span></span>  
 `warning-list`  
 <span data-ttu-id="6ff51-106">경고 번호를 쉼표로 구분한 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6ff51-106">A comma-separated list of warning numbers.</span></span> <span data-ttu-id="6ff51-107">"CS" 접두사는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6ff51-107">The "CS" prefix is optional.</span></span>  
  
 <span data-ttu-id="6ff51-108">경고 번호를 지정하지 않은 경우 `disable`은 모든 경고를 사용하지 않도록 설정하고 `restore`는 모든 경고를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ff51-108">When no warning numbers are specified, `disable` disables all warnings and `restore` enables all warnings.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6ff51-109">Visual Studio에서 경고 번호를 찾으려면 프로젝트를 빌드하고 **출력** 창에서 경고 번호를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6ff51-109">To find warning numbers in Visual Studio, build your project and then look for the warning numbers in the **Output** window.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6ff51-110">예</span><span class="sxs-lookup"><span data-stu-id="6ff51-110">Example</span></span>  
  
```csharp
// pragma_warning.cs  
using System;  
  
#pragma warning disable 414, CS3021  
[CLSCompliant(false)]  
public class C  
{  
    int i = 1;  
    static void Main()  
    {  
    }  
}  
#pragma warning restore CS3021  
[CLSCompliant(false)]  // CS3021  
public class D  
{  
    int i = 1;  
    public static void F()  
    {  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="6ff51-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6ff51-111">See Also</span></span>

- [<span data-ttu-id="6ff51-112">C# 참조</span><span class="sxs-lookup"><span data-stu-id="6ff51-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="6ff51-113">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="6ff51-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="6ff51-114">C# 전처리기 지시문</span><span class="sxs-lookup"><span data-stu-id="6ff51-114">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)  
- [<span data-ttu-id="6ff51-115">C# 컴파일러 오류</span><span class="sxs-lookup"><span data-stu-id="6ff51-115">C# Compiler Errors</span></span>](../../../csharp/language-reference/compiler-messages/index.md)
