---
title: -문서
ms.date: 03/10/2018
helpviewer_keywords:
- doc compiler option [Visual Basic]
- -doc compiler option [Visual Basic]
- /doc compiler option [Visual Basic]
ms.assetid: 5fc32ec9-a149-4648-994c-a8d0cccd0a65
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4c77d063d64354bf4693ce82509f36be9d2e5b0c
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46003895"
---
# <a name="-doc"></a><span data-ttu-id="52884-102">-문서</span><span class="sxs-lookup"><span data-stu-id="52884-102">-doc</span></span>
<span data-ttu-id="52884-103">XML 파일에 대해 문서 주석을 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="52884-103">Processes documentation comments to an XML file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="52884-104">구문</span><span class="sxs-lookup"><span data-stu-id="52884-104">Syntax</span></span>  
  
```  
-doc[+ | -]  
' -or-  
-doc:file  
```  
  
## <a name="arguments"></a><span data-ttu-id="52884-105">인수</span><span class="sxs-lookup"><span data-stu-id="52884-105">Arguments</span></span>  
  
|<span data-ttu-id="52884-106">용어</span><span class="sxs-lookup"><span data-stu-id="52884-106">Term</span></span>|<span data-ttu-id="52884-107">정의</span><span class="sxs-lookup"><span data-stu-id="52884-107">Definition</span></span>|  
|---|---|  
|<span data-ttu-id="52884-108">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="52884-108">`+` &#124; `-`</span></span>|<span data-ttu-id="52884-109">선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="52884-109">Optional.</span></span> <span data-ttu-id="52884-110">지정 +, 또는 `-doc`, 컴파일러에서 문서 정보를 생성 하 고 XML 파일에 배치 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="52884-110">Specifying +, or just `-doc`, causes the compiler to generate documentation information and place it in an XML file.</span></span> <span data-ttu-id="52884-111">지정 `-` 지정 하지 않는 것과 같습니다 `-doc`, 하므로 만들 문서 정보가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="52884-111">Specifying `-` is the equivalent of not specifying `-doc`, causing no documentation information to be created.</span></span>|  
|`file`|<span data-ttu-id="52884-112">`-doc:`를 사용하는 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="52884-112">Required if `-doc:` is used.</span></span> <span data-ttu-id="52884-113">컴파일의 소스 코드 파일에서 주석 사용 되는 출력 XML 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52884-113">Specifies the output XML file, which is populated with the comments from the source-code files of the compilation.</span></span> <span data-ttu-id="52884-114">파일 이름에 공백이 있으면 이름을 따옴표로 묶습니다 ("").</span><span class="sxs-lookup"><span data-stu-id="52884-114">If the file name contains a space, surround the name with quotation marks (" ").</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="52884-115">설명</span><span class="sxs-lookup"><span data-stu-id="52884-115">Remarks</span></span>  
 <span data-ttu-id="52884-116">`-doc` 옵션 컴파일러 설명서 주석이 들어 있는 XML 파일을 생성 하는지 여부를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="52884-116">The `-doc` option controls whether the compiler generates an XML file containing the documentation comments.</span></span> <span data-ttu-id="52884-117">사용 하는 경우는 `-doc:file` 구문을 `file` 매개 변수는 XML 파일의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52884-117">If you use the `-doc:file` syntax, the `file` parameter specifies the name of the XML file.</span></span> <span data-ttu-id="52884-118">사용 하는 경우 `-doc` 또는 `-doc+`, 컴파일러는 실행 파일 또는 작성 된 라이브러리에서 XML 파일 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="52884-118">If you use `-doc` or `-doc+`, the compiler takes the XML file name from the executable file or library that the compiler is creating.</span></span> <span data-ttu-id="52884-119">사용 하는 경우 `-doc-` 지정 하지 마십시오는 `-doc` 옵션을 컴파일러 만들어지지는지 않습니다 XML 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="52884-119">If you use `-doc-` or do not specify the `-doc` option, the compiler does not create an XML file.</span></span>  
  
 <span data-ttu-id="52884-120">소스 코드 파일에 문서 주석을 정의 앞에 야 수 있습니다.:</span><span class="sxs-lookup"><span data-stu-id="52884-120">In source-code files, documentation comments can precede the following definitions:</span></span>  
  
-   <span data-ttu-id="52884-121">사용자 정의 형식, 예는 [클래스](../../../visual-basic/language-reference/statements/class-statement.md) 또는 [인터페이스](../../../visual-basic/language-reference/statements/interface-statement.md)</span><span class="sxs-lookup"><span data-stu-id="52884-121">User-defined types, such as a [class](../../../visual-basic/language-reference/statements/class-statement.md) or [interface](../../../visual-basic/language-reference/statements/interface-statement.md)</span></span>  
  
-   <span data-ttu-id="52884-122">멤버는 필드와 같이 [이벤트](../../../visual-basic/language-reference/statements/event-statement.md)를 [속성](../../../visual-basic/language-reference/statements/property-statement.md)를 [함수](../../../visual-basic/language-reference/statements/function-statement.md), 또는 [서브루틴](../../../visual-basic/language-reference/statements/sub-statement.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="52884-122">Members, such as a field, [event](../../../visual-basic/language-reference/statements/event-statement.md), [property](../../../visual-basic/language-reference/statements/property-statement.md), [function](../../../visual-basic/language-reference/statements/function-statement.md), or [subroutine](../../../visual-basic/language-reference/statements/sub-statement.md).</span></span>  
  
 <span data-ttu-id="52884-123">Visual Studio를 사용 하 여 생성된 된 XML 파일을 사용 하도록 [IntelliSense](/visualstudio/ide/using-intellisense) 기능에서 XML 파일의 파일 이름을 지원 하려는 어셈블리와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="52884-123">To use the generated XML file with the Visual Studio [IntelliSense](/visualstudio/ide/using-intellisense) feature, let the file name of the XML file be the same as the assembly you want to support.</span></span> <span data-ttu-id="52884-124">Visual Studio 프로젝트에서 어셈블리를 참조할 때.xml 파일이 되도록 XML 파일을 어셈블리와 동일한 디렉터리에 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="52884-124">Make sure the XML file is in the same directory as the assembly so that when the assembly is referenced in the Visual Studio project, the .xml file is found as well.</span></span> <span data-ttu-id="52884-125">XML 설명서 파일이 프로젝트에서 참조 된 프로젝트 또는 프로젝트 내에서 코드에 대 한 작업에 IntelliSense에 대 한 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52884-125">XML documentation files are not required for IntelliSense to work for code within a project or within projects referenced by a project.</span></span>  
  
 <span data-ttu-id="52884-126">사용 하 여 컴파일하지 않으면 `/target:module`, XML 파일에는 태그가 포함 `<assembly></assembly>`합니다.</span><span class="sxs-lookup"><span data-stu-id="52884-126">Unless you compile with `/target:module`, the XML file contains the tags `<assembly></assembly>`.</span></span> <span data-ttu-id="52884-127">이러한 태그 컴파일의 출력 파일에 대 한 어셈블리 매니페스트를 포함 하는 파일의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52884-127">These tags specify the name of the file containing the assembly manifest for the output file of the compilation.</span></span>  
  
 <span data-ttu-id="52884-128">참조 [XML 주석 태그](../../../visual-basic/language-reference/xmldoc/index.md) 코드의 주석에서 문서를 생성 하는 방법에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="52884-128">See [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/index.md) for ways to generate documentation from comments in your code.</span></span>  
  
|<span data-ttu-id="52884-129">Visual studio에서 문서 통합 개발 환경 설정-</span><span class="sxs-lookup"><span data-stu-id="52884-129">To set -doc in the Visual Studio integrated development environment</span></span>|  
|---|  
|<span data-ttu-id="52884-130">1.  **솔루션 탐색기**에서 프로젝트를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="52884-130">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="52884-131">**프로젝트** 메뉴에서 **속성**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="52884-131">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="52884-132">2.  **컴파일** 탭을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="52884-132">2.  Click the **Compile** tab.</span></span><br /><span data-ttu-id="52884-133">3.  값을 설정 합니다 **XML 문서 파일 생성** 상자입니다.</span><span class="sxs-lookup"><span data-stu-id="52884-133">3.  Set the value in the **Generate XML documentation file** box.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="52884-134">예제</span><span class="sxs-lookup"><span data-stu-id="52884-134">Example</span></span>  
 <span data-ttu-id="52884-135">참조 [XML 사용 하 여 코드 문서화](../../../visual-basic/programming-guide/program-structure/documenting-your-code-with-xml.md) 샘플입니다.</span><span class="sxs-lookup"><span data-stu-id="52884-135">See [Documenting Your Code with XML](../../../visual-basic/programming-guide/program-structure/documenting-your-code-with-xml.md) for a sample.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="52884-136">참고 항목</span><span class="sxs-lookup"><span data-stu-id="52884-136">See Also</span></span>  
 [<span data-ttu-id="52884-137">Visual Basic 명령줄 컴파일러</span><span class="sxs-lookup"><span data-stu-id="52884-137">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="52884-138">코드를 XML로 문서화</span><span class="sxs-lookup"><span data-stu-id="52884-138">Documenting Your Code with XML</span></span>](../../../visual-basic/programming-guide/program-structure/documenting-your-code-with-xml.md)
