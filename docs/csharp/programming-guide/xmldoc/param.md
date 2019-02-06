---
title: <param> - C# 프로그래밍 가이드
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- param
- <param>
helpviewer_keywords:
- <param> C# XML tag
- param C# XML tag
ms.assetid: 46d329b1-5b84-4537-9e17-73ca97313e4e
ms.openlocfilehash: 3f1099da6a43ed7f48389a16e3be6a3b6b98a148
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271579"
---
# <a name="param-c-programming-guide"></a><span data-ttu-id="d1d05-102">\<param>(C# 프로그래밍 가이드)</span><span class="sxs-lookup"><span data-stu-id="d1d05-102">\<param> (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="d1d05-103">구문</span><span class="sxs-lookup"><span data-stu-id="d1d05-103">Syntax</span></span>  
  
```xml  
<param name="name">description</param>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d1d05-104">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d1d05-104">Parameters</span></span>  
 `name`  
 <span data-ttu-id="d1d05-105">메서드 매개 변수의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1d05-105">The name of a method parameter.</span></span> <span data-ttu-id="d1d05-106">이름을 큰따옴표(“ ”)로 묶습니다.</span><span class="sxs-lookup"><span data-stu-id="d1d05-106">Enclose the name in double quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="d1d05-107">매개 변수에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="d1d05-107">A description for the parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d1d05-108">주의</span><span class="sxs-lookup"><span data-stu-id="d1d05-108">Remarks</span></span>  
 <span data-ttu-id="d1d05-109">\<param> 태그는 메서드의 매개 변수 중 하나를 설명하기 위해 메서드 선언에 대한 주석에 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d05-109">The \<param> tag should be used in the comment for a method declaration to describe one of the parameters for the method.</span></span> <span data-ttu-id="d1d05-110">여러 매개 변수를 문서화하려면 여러 개의 \<param> 태그를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d05-110">To document multiple parameters, use multiple \<param> tags.</span></span>  
  
 <span data-ttu-id="d1d05-111">\<param> 태그에 대한 텍스트는 IntelliSense, 개체 브라우저 및 코드 주석 웹 보고서에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1d05-111">The text for the \<param> tag will be displayed in IntelliSense, the Object Browser, and in the Code Comment Web Report.</span></span>  
  
 <span data-ttu-id="d1d05-112">[/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md)로 컴파일하여 문서 주석을 파일로 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d05-112">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d1d05-113">예</span><span class="sxs-lookup"><span data-stu-id="d1d05-113">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#1](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/param_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="d1d05-114">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d1d05-114">See also</span></span>

- [<span data-ttu-id="d1d05-115">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="d1d05-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="d1d05-116">문서 주석에 대한 권장 태그</span><span class="sxs-lookup"><span data-stu-id="d1d05-116">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
