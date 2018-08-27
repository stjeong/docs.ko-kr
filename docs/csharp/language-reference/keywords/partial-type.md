---
title: 부분(형식)(C# 참조)
ms.date: 07/20/2015
f1_keywords:
- partialtype
- partialtype_CSharpKeyword
helpviewer_keywords:
- partial types [C#]
ms.assetid: 27320743-a22e-4c7b-b0b3-53afe3607334
ms.openlocfilehash: 362a02815cb249d57c0bd19706714df1d71644f4
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42929665"
---
# <a name="partial-type-c-reference"></a><span data-ttu-id="2a851-102">부분(형식)(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="2a851-102">partial (Type) (C# Reference)</span></span>
<span data-ttu-id="2a851-103">부분 형식(Partial Type) 정의를 사용하면 클래스, 구조체 또는 인터페이스의 정의를 여러 파일로 분할할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a851-103">Partial type definitions allow for the definition of a class, struct, or interface to be split into multiple files.</span></span>  
  
 <span data-ttu-id="2a851-104">File1.cs:</span><span class="sxs-lookup"><span data-stu-id="2a851-104">In File1.cs:</span></span>  
  
 [!code-csharp[csrefKeywordsContextual#3](../../../csharp/language-reference/keywords/codesnippet/CSharp/partial-type_1.cs)]  
  
 <span data-ttu-id="2a851-105">File2.cs에서 선언은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2a851-105">In File2.cs the declaration:</span></span>  
  
 [!code-csharp[csrefKeywordsContextual#4](../../../csharp/language-reference/keywords/codesnippet/CSharp/partial-type_2.cs)]  
  
## <a name="remarks"></a><span data-ttu-id="2a851-106">설명</span><span class="sxs-lookup"><span data-stu-id="2a851-106">Remarks</span></span>  
 <span data-ttu-id="2a851-107">클래스, 구조체 또는 인터페이스 형식을 여러 파일에 분할하면 대형 프로젝트 또는 [Windows Forms 디자이너](../../../framework/winforms/controls/developing-windows-forms-controls-at-design-time.md)에서 제공하는 것과 같은 자동으로 생성된 코드로 작업할 때 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a851-107">Splitting a class, struct or interface type over several files can be useful when you are working with large projects, or with automatically generated code such as that provided by the [Windows Forms Designer](../../../framework/winforms/controls/developing-windows-forms-controls-at-design-time.md).</span></span> <span data-ttu-id="2a851-108">부분 형식(Partial Type)에는 [부분 메서드(Partial Method)](../../../csharp/language-reference/keywords/partial-method.md)가 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a851-108">A partial type may contain a [partial method](../../../csharp/language-reference/keywords/partial-method.md).</span></span> <span data-ttu-id="2a851-109">자세한 내용은 참조 [Partial 클래스 및 메서드](../../../csharp/programming-guide/classes-and-structs/partial-classes-and-methods.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="2a851-109">For more information, see [Partial Classes and Methods](../../../csharp/programming-guide/classes-and-structs/partial-classes-and-methods.md).</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="2a851-110">C# 언어 사양</span><span class="sxs-lookup"><span data-stu-id="2a851-110">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="2a851-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2a851-111">See Also</span></span>

- [<span data-ttu-id="2a851-112">C# 참조</span><span class="sxs-lookup"><span data-stu-id="2a851-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="2a851-113">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="2a851-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="2a851-114">한정자</span><span class="sxs-lookup"><span data-stu-id="2a851-114">Modifiers</span></span>](../../../csharp/language-reference/keywords/modifiers.md)  
- [<span data-ttu-id="2a851-115">제네릭 소개</span><span class="sxs-lookup"><span data-stu-id="2a851-115">Introduction to Generics</span></span>](../../../csharp/programming-guide/generics/introduction-to-generics.md)
