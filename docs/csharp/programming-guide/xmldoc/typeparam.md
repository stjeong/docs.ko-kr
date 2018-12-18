---
title: '&lt;typeparam&gt; - C# 프로그래밍 가이드'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- typeparam
helpviewer_keywords:
- <typeparam> C# XML tag
- typeparam C# XML tag
ms.assetid: 9b99d400-e911-4e55-99c6-64367c96aa4f
ms.openlocfilehash: 87629346238e92cf95141e72d79be37f8b11e48f
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53241816"
---
# <a name="lttypeparamgt-c-programming-guide"></a><span data-ttu-id="a236e-102">&lt;typeparam&gt;(C# 프로그래밍 가이드)</span><span class="sxs-lookup"><span data-stu-id="a236e-102">&lt;typeparam&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="a236e-103">구문</span><span class="sxs-lookup"><span data-stu-id="a236e-103">Syntax</span></span>  
  
```xml  
<typeparam name="name">description</typeparam>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a236e-104">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a236e-104">Parameters</span></span>  
 `name`  
 <span data-ttu-id="a236e-105">형식 매개 변수의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a236e-105">The name of the type parameter.</span></span> <span data-ttu-id="a236e-106">이름을 큰따옴표(“ ”)로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="a236e-106">Enclose the name in double quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="a236e-107">형식 매개 변수에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="a236e-107">A description for the type parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a236e-108">설명</span><span class="sxs-lookup"><span data-stu-id="a236e-108">Remarks</span></span>  
 <span data-ttu-id="a236e-109">`<typeparam>` 태그는 제네릭 형식 또는 메서드 선언의 주석에서 형식 매개 변수를 설명하는 데 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a236e-109">The `<typeparam>` tag should be used in the comment for a generic type or method declaration to describe a type parameter.</span></span> <span data-ttu-id="a236e-110">제네릭 형식 또는 메서드의 각 형식 매개 변수에 대한 태그를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a236e-110">Add a tag for each type parameter of the generic type or method.</span></span>  
  
 <span data-ttu-id="a236e-111">자세한 내용은 [제네릭](../../../csharp/programming-guide/generics/index.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a236e-111">For more information, see [Generics](../../../csharp/programming-guide/generics/index.md).</span></span>  
  
 <span data-ttu-id="a236e-112">`<typeparam>` 태그에 대한 텍스트는 IntelliSense와 [개체 브라우저 창](/visualstudio/ide/viewing-the-structure-of-code#BKMK_ObjectBrowser)의 코드 주석 웹 보고서에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a236e-112">The text for the `<typeparam>` tag will be displayed in IntelliSense, the [Object Browser Window](/visualstudio/ide/viewing-the-structure-of-code#BKMK_ObjectBrowser) code comment web report.</span></span>  
  
 <span data-ttu-id="a236e-113">[/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md)로 컴파일하여 문서 주석을 파일로 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="a236e-113">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a236e-114">예제</span><span class="sxs-lookup"><span data-stu-id="a236e-114">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#13](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/typeparam_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="a236e-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a236e-115">See Also</span></span>

- [<span data-ttu-id="a236e-116">C# 참조</span><span class="sxs-lookup"><span data-stu-id="a236e-116">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="a236e-117">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="a236e-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="a236e-118">문서 주석에 대한 권장 태그</span><span class="sxs-lookup"><span data-stu-id="a236e-118">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
