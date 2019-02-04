---
title: C# 프로그램의 일반적인 구조 - C# 프로그래밍 가이드
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, program structure
ms.assetid: 5ae964a5-0ef0-40fe-88fb-6d1793371d0d
ms.openlocfilehash: 53908a21e573b7ac7d8347ebfe7f11202612fae1
ms.sourcegitcommit: b8ace47d839f943f785b89e2fff8092b0bf8f565
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/03/2019
ms.locfileid: "55675103"
---
# <a name="general-structure-of-a-c-program-c-programming-guide"></a><span data-ttu-id="38824-102">C# 프로그램의 일반적인 구조(C# 프로그래밍 가이드)</span><span class="sxs-lookup"><span data-stu-id="38824-102">General Structure of a C# Program (C# Programming Guide)</span></span>
<span data-ttu-id="38824-103">C# 프로그램은 하나 이상의 파일로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="38824-103">C# programs can consist of one or more files.</span></span> <span data-ttu-id="38824-104">각 파일에는 0개 이상의 네임스페이스가 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38824-104">Each file can contain zero or more namespaces.</span></span> <span data-ttu-id="38824-105">네임스페이스에는 다른 네임스페이스 외에 클래스, 구조체, 인터페이스, 열거형 및 대리자 같은 형식이 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38824-105">A namespace can contain types such as classes, structs, interfaces, enumerations, and delegates, in addition to other namespaces.</span></span> <span data-ttu-id="38824-106">다음은 이러한 모든 요소를 포함하는 C# 프로그램의 기본 구조입니다.</span><span class="sxs-lookup"><span data-stu-id="38824-106">The following is the skeleton of a C# program that contains all of these elements.</span></span>  
  
 [!code-csharp[csProgGuide#34](../../../csharp/programming-guide/inside-a-program/codesnippet/CSharp/general-structure-of-a-csharp-program_1.cs)]  
  
## <a name="related-sections"></a><span data-ttu-id="38824-107">관련 단원</span><span class="sxs-lookup"><span data-stu-id="38824-107">Related Sections</span></span>  
 <span data-ttu-id="38824-108">추가 정보</span><span class="sxs-lookup"><span data-stu-id="38824-108">For more information:</span></span>  
  
-   [<span data-ttu-id="38824-109">클래스</span><span class="sxs-lookup"><span data-stu-id="38824-109">Classes</span></span>](../../../csharp/programming-guide/classes-and-structs/classes.md)  
  
-   [<span data-ttu-id="38824-110">구조체</span><span class="sxs-lookup"><span data-stu-id="38824-110">Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/structs.md)  
  
-   [<span data-ttu-id="38824-111">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="38824-111">Namespaces</span></span>](../../../csharp/programming-guide/namespaces/index.md)  
  
-   [<span data-ttu-id="38824-112">인터페이스</span><span class="sxs-lookup"><span data-stu-id="38824-112">Interfaces</span></span>](../../../csharp/programming-guide/interfaces/index.md)  
  
-   [<span data-ttu-id="38824-113">대리자</span><span class="sxs-lookup"><span data-stu-id="38824-113">Delegates</span></span>](../../../csharp/programming-guide/delegates/index.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="38824-114">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="38824-114">C# Language Specification</span></span>  

<span data-ttu-id="38824-115">자세한 내용은 [C# 언어 사양](../../language-reference/language-specification/index.md)의 [기본 개념](~/_csharplang/spec/basic-concepts.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="38824-115">For more information, see [Basic concepts](~/_csharplang/spec/basic-concepts.md) in the [C# Language Specification](../../language-reference/language-specification/index.md).</span></span> <span data-ttu-id="38824-116">C# 언어 사양은 C# 구문 및 사용법에 대한 신뢰할 수 있는 소스입니다.</span><span class="sxs-lookup"><span data-stu-id="38824-116">The language specification is the definitive source for C# syntax and usage.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="38824-117">참고 항목</span><span class="sxs-lookup"><span data-stu-id="38824-117">See also</span></span>

- [<span data-ttu-id="38824-118">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="38824-118">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="38824-119">C# 프로그램 내부</span><span class="sxs-lookup"><span data-stu-id="38824-119">Inside a C# Program</span></span>](../../../csharp/programming-guide/inside-a-program/index.md)
- [<span data-ttu-id="38824-120">C# 참조</span><span class="sxs-lookup"><span data-stu-id="38824-120">C# Reference</span></span>](../../../csharp/language-reference/index.md)
