---
title: -codepage (Visual Basic)
ms.date: 03/09/2018
helpviewer_keywords:
- -codepage compiler option [Visual Basic]
- codepage compiler option [Visual Basic]
- -codepage compiler option [Visual Basic]
ms.assetid: be36ec33-6800-4505-838c-4124564f5cc9
ms.openlocfilehash: 8aee51df3ba9f92ca662fbbfbd73998e4a3b4538
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43882606"
---
# <a name="-codepage-visual-basic"></a><span data-ttu-id="61140-102">-codepage (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="61140-102">-codepage (Visual Basic)</span></span>
<span data-ttu-id="61140-103">컴파일할 때 모든 소스 코드 파일에 사용할 코드 페이지를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="61140-103">Specifies the code page to use for all source-code files in the compilation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="61140-104">구문</span><span class="sxs-lookup"><span data-stu-id="61140-104">Syntax</span></span>  
  
```  
-codepage:id  
```  
  
## <a name="arguments"></a><span data-ttu-id="61140-105">인수</span><span class="sxs-lookup"><span data-stu-id="61140-105">Arguments</span></span>  
  
|<span data-ttu-id="61140-106">용어</span><span class="sxs-lookup"><span data-stu-id="61140-106">Term</span></span>|<span data-ttu-id="61140-107">정의</span><span class="sxs-lookup"><span data-stu-id="61140-107">Definition</span></span>|  
|---|---|  
|`id`|<span data-ttu-id="61140-108">필수.</span><span class="sxs-lookup"><span data-stu-id="61140-108">Required.</span></span> <span data-ttu-id="61140-109">컴파일러에서 지정한 코드 페이지를 사용 하 여 `id` 원본 파일의 인코딩을 해석 합니다.</span><span class="sxs-lookup"><span data-stu-id="61140-109">The compiler uses the code page specified by `id` to interpret the encoding of the source files.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="61140-110">설명</span><span class="sxs-lookup"><span data-stu-id="61140-110">Remarks</span></span>  
 <span data-ttu-id="61140-111">특정 인코딩을 사용 하 여 저장 된 소스 코드를 컴파일하는 데 사용할 수 있습니다 `-codepage` 사용할 코드 페이지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61140-111">To compile source code saved with a specific encoding, you can use `-codepage` to specify which code page should be used.</span></span> <span data-ttu-id="61140-112">`-codepage` 옵션 컴파일에서 모든 소스 코드 파일에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61140-112">The `-codepage` option applies to all source-code files in your compilation.</span></span> <span data-ttu-id="61140-113">자세한 내용은 [.NET Framework의 문자 인코딩](https://msdn.microsoft.com/library/bf6d9823-4c2d-48af-b280-919c5af66ae9)합니다.</span><span class="sxs-lookup"><span data-stu-id="61140-113">For more information, see [Character Encoding in the .NET Framework](https://msdn.microsoft.com/library/bf6d9823-4c2d-48af-b280-919c5af66ae9).</span></span>  
  
 <span data-ttu-id="61140-114">`-codepage` 옵션의 현재 ANSI 코드 페이지, Unicode 또는 u t F-8을 사용 하 여 서명을 사용 하 여 소스 코드 파일을 저장 한 경우에 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61140-114">The `-codepage` option is not needed if the source-code files were saved using the current ANSI code page, Unicode, or UTF-8 with a signature.</span></span> <span data-ttu-id="61140-115">Visual Studio 저장 모든 소스 코드 파일의 현재 ANSI 코드 페이지를 사용 하 여 기본적으로 사용자에서 다른 인코딩을 지정 하지 않는 경우는 **Encoding** 대화 상자.</span><span class="sxs-lookup"><span data-stu-id="61140-115">Visual Studio saves all source-code files with the current ANSI code page by default, unless the user specifies another encoding in the **Encoding** dialog box.</span></span> <span data-ttu-id="61140-116">Visual Studio에서 사용 하는 **Encoding** 대화 상자를 다른 코드 페이지를 사용 하 여 저장 하는 소스 코드 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="61140-116">Visual Studio uses the **Encoding** dialog box to open source-code files saved with a different code page.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="61140-117">`-codepage` 옵션은 Visual Studio 개발 환경 내에서 사용할 수 있는 명령줄에서 컴파일할 경우에 사용할 수 있는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="61140-117">The `-codepage` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61140-118">참고 항목</span><span class="sxs-lookup"><span data-stu-id="61140-118">See Also</span></span>  
 [<span data-ttu-id="61140-119">Visual Basic 명령줄 컴파일러</span><span class="sxs-lookup"><span data-stu-id="61140-119">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
