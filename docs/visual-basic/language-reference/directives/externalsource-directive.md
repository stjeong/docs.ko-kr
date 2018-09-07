---
title: '#ExternalSource 지시문 (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- '#Externalsource'
- '#ExternalSource'
- vb.ExternalSource
- Externalsource
- vb.#ExternalSource
- ExternalSource
helpviewer_keywords:
- ExternalSource directive (#ExternalSource)
- '#ExternalSource directive'
ms.assetid: 243bc6a2-34c3-4eeb-a776-9fd2bf988149
ms.openlocfilehash: dcde8507eb033d0a47d5c5d3fa36176cd63b0856
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43861791"
---
# <a name="externalsource-directive"></a><span data-ttu-id="b15db-102">#ExternalSource 지시문</span><span class="sxs-lookup"><span data-stu-id="b15db-102">#ExternalSource Directive</span></span>
<span data-ttu-id="b15db-103">소스 코드의 특정 줄과 소스 외부에 있는 텍스트 간의 매핑을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b15db-103">Indicates a mapping between specific lines of source code and text external to the source.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b15db-104">구문</span><span class="sxs-lookup"><span data-stu-id="b15db-104">Syntax</span></span>  
  
```  
#ExternalSource( StringLiteral , IntLiteral )  
    [ LogicalLine+ ]  
#End ExternalSource  
```  
  
## <a name="parts"></a><span data-ttu-id="b15db-105">요소</span><span class="sxs-lookup"><span data-stu-id="b15db-105">Parts</span></span>  
 `StringLiteral`  
 <span data-ttu-id="b15db-106">외부 원본에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b15db-106">The path to the external source.</span></span>  
  
 `IntLiteral`  
 <span data-ttu-id="b15db-107">외부 원본의 첫 번째 줄의 줄 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="b15db-107">The line number of the first line of the external source.</span></span>  
  
 `LogicalLine`  
 <span data-ttu-id="b15db-108">외부 원본에서 오류가 발생 하는 줄.</span><span class="sxs-lookup"><span data-stu-id="b15db-108">The line where the error occurs in the external source.</span></span>  
  
 `#End ExternalSource`  
 <span data-ttu-id="b15db-109">`#ExternalSource` 블록을 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="b15db-109">Terminates the `#ExternalSource` block.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b15db-110">설명</span><span class="sxs-lookup"><span data-stu-id="b15db-110">Remarks</span></span>  
 <span data-ttu-id="b15db-111">이 지시문은 컴파일러 및 디버거가 의해서만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b15db-111">This directive is used only by the compiler and the debugger.</span></span>  
  
 <span data-ttu-id="b15db-112">소스 파일을 소스 파일에서 코드의 특정 줄과 외부.aspx 파일 같이 원본에 있는 텍스트 간의 매핑을 나타내는 외부 소스 지시문을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b15db-112">A source file may include external source directives, which indicate a mapping between specific lines of code in the source file and text external to the source, such as an .aspx file.</span></span> <span data-ttu-id="b15db-113">지정 된 소스 코드에서를 컴파일하는 동안 오류가 발생 하면 외부 원본에서 오는 것으로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b15db-113">If errors are encountered in the designated source code during compilation, they are identified as coming from the external source.</span></span>  
  
 <span data-ttu-id="b15db-114">외부 소스 지시문 컴파일에 영향을 주지 않으며 중첩할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b15db-114">External source directives have no effect on compilation and cannot be nested.</span></span> <span data-ttu-id="b15db-115">이러한는 내부 용도로 응용 프로그램에서 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15db-115">They are intended for internal use by the application only.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b15db-116">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b15db-116">See Also</span></span>  
 [<span data-ttu-id="b15db-117">조건부 컴파일</span><span class="sxs-lookup"><span data-stu-id="b15db-117">Conditional Compilation</span></span>](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
