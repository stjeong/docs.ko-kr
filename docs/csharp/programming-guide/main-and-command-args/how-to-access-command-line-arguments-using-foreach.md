---
title: '방법: foreach를 사용하여 명령줄 인수 액세스(C# 프로그래밍 가이드)'
ms.date: 07/20/2015
helpviewer_keywords:
- command-line arguments [C#]
ms.assetid: 89c3e335-3f5b-4e24-8c5a-b8036561fe8a
ms.openlocfilehash: 811ee09aec7afac70f3f2c2fe5fb002232935028
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43511338"
---
# <a name="how-to-access-command-line-arguments-using-foreach-c-programming-guide"></a><span data-ttu-id="8d353-102">방법: foreach를 사용하여 명령줄 인수 액세스(C# 프로그래밍 가이드)</span><span class="sxs-lookup"><span data-stu-id="8d353-102">How to: Access Command-Line Arguments Using foreach (C# Programming Guide)</span></span>
<span data-ttu-id="8d353-103">배열을 반복하는 또 다른 방법은 이 예제에 표시된 대로 [foreach](../../../csharp/language-reference/keywords/foreach-in.md) 문을 사용하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8d353-103">Another approach to iterating over the array is to use the [foreach](../../../csharp/language-reference/keywords/foreach-in.md) statement as shown in this example.</span></span> <span data-ttu-id="8d353-104">`foreach` 문은 배열, .NET Framework 컬렉션 클래스 또는 <xref:System.Collections.IEnumerable> 인터페이스를 구현하는 임의의 클래스나 구조체를 반복하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d353-104">The `foreach` statement can be used to iterate over an array, a .NET Framework collection class, or any class or struct that implements the <xref:System.Collections.IEnumerable> interface.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8d353-105">Visual Studio에서 응용 프로그램을 실행할 경우 [프로젝트 디자이너, 디버그 페이지](/visualstudio/ide/reference/debug-page-project-designer)에서 명령줄 인수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d353-105">When running an application in Visual Studio, you can specify command-line arguments in the [Debug Page, Project Designer](/visualstudio/ide/reference/debug-page-project-designer).</span></span>  
  
## <a name="example"></a><span data-ttu-id="8d353-106">예</span><span class="sxs-lookup"><span data-stu-id="8d353-106">Example</span></span>  
 <span data-ttu-id="8d353-107">이 예제에서는 `foreach`를 사용하여 명령줄을 출력하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8d353-107">This example demonstrates how to print out the command line arguments using `foreach`.</span></span>  
  
 [!code-csharp[csProgGuideMain#10](../../../csharp/programming-guide/inside-a-program/codesnippet/CSharp/how-to-access-command-line-arguments-using-foreach_1.cs)]  
  
 [!code-csharp[csProgGuideMain#11](../../../csharp/programming-guide/inside-a-program/codesnippet/CSharp/how-to-access-command-line-arguments-using-foreach_2.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="8d353-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="8d353-108">See Also</span></span>

- <xref:System.Array>  
- <xref:System.Collections>  
- [<span data-ttu-id="8d353-109">csc.exe를 사용한 명령줄 빌드</span><span class="sxs-lookup"><span data-stu-id="8d353-109">Command-line Building With csc.exe</span></span>](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)  
- [<span data-ttu-id="8d353-110">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="8d353-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="8d353-111">foreach, in</span><span class="sxs-lookup"><span data-stu-id="8d353-111">foreach, in</span></span>](../../../csharp/language-reference/keywords/foreach-in.md)  
- [<span data-ttu-id="8d353-112">Main()과 명령줄 인수</span><span class="sxs-lookup"><span data-stu-id="8d353-112">Main() and Command-Line Arguments</span></span>](../../../csharp/programming-guide/main-and-command-args/index.md)  
- [<span data-ttu-id="8d353-113">방법: 명령줄 인수 표시</span><span class="sxs-lookup"><span data-stu-id="8d353-113">How to: Display Command Line Arguments</span></span>](../../../csharp/programming-guide/main-and-command-args/how-to-display-command-line-arguments.md)  
- [<span data-ttu-id="8d353-114">Main() 반환 값</span><span class="sxs-lookup"><span data-stu-id="8d353-114">Main() Return Values</span></span>](../../../csharp/programming-guide/main-and-command-args/main-return-values.md)
