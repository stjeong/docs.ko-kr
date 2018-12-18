---
title: '방법: LINQ 외부에 람다 식 사용 - C# 프로그래밍 가이드'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- lambda expressions [C#], outside LINQ
ms.assetid: 2b519274-6ee4-4455-ab2e-aed67dbfd07c
ms.openlocfilehash: d4dc0375552ef1fe00f629c22b5296399b4cc99d
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243935"
---
# <a name="how-to-use-lambda-expressions-outside-linq-c-programming-guide"></a><span data-ttu-id="4c647-102">방법: LINQ 외부에 람다 식 사용(C# 프로그래밍 가이드)</span><span class="sxs-lookup"><span data-stu-id="4c647-102">How to: Use Lambda Expressions Outside LINQ (C# Programming Guide)</span></span>
<span data-ttu-id="4c647-103">람다 식은 [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] 쿼리로 제한되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c647-103">Lambda expressions are not limited to [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] queries.</span></span> <span data-ttu-id="4c647-104">대리자 값이 필요한 곳, 즉 무명 메서드를 사용할 수 있는 곳이면 어디서나 람다 식을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c647-104">You can use them anywhere a delegate value is expected, that is, wherever an anonymous method can be used.</span></span> <span data-ttu-id="4c647-105">다음 예제에서는 Windows Forms 이벤트 처리기에 람다 식을 사용하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4c647-105">The following example shows how to use a lambda expression in a Windows Forms event handler.</span></span> <span data-ttu-id="4c647-106">입력 형식(<xref:System.Object> 및 <xref:System.Windows.Forms.MouseEventArgs>)은 컴파일러에서 유추되며 람다 입력 매개 변수에서 명시적으로 지정되지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c647-106">Notice that the types of the inputs (<xref:System.Object> and <xref:System.Windows.Forms.MouseEventArgs>) are inferred by the compiler and do not have to be explicitly given in the lambda input parameters.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4c647-107">예제</span><span class="sxs-lookup"><span data-stu-id="4c647-107">Example</span></span>  
  
```csharp  
public partial class Form1 : Form  
{  
    public Form1()  
    {  
        InitializeComponent();  
        // Use a lambda expression to define an event handler.  
       this.Click += (s, e) => { MessageBox.Show(((MouseEventArgs)e).Location.ToString());};  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="4c647-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4c647-108">See Also</span></span>

- [<span data-ttu-id="4c647-109">람다 식</span><span class="sxs-lookup"><span data-stu-id="4c647-109">Lambda Expressions</span></span>](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md)  
- [<span data-ttu-id="4c647-110">무명 메서드</span><span class="sxs-lookup"><span data-stu-id="4c647-110">Anonymous Methods</span></span>](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md)  
- [<span data-ttu-id="4c647-111">LINQ(Language-Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="4c647-111">Language Integrated Query (LINQ))</span></span>](../../../csharp/programming-guide/concepts/linq/index.md)
