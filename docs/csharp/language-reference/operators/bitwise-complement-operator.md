---
title: ~ 연산자(C# 참조)
ms.date: 07/20/2015
f1_keywords:
- ~_CSharpKeyword
helpviewer_keywords:
- tilde (~) one's complement operator [C#]
- ~ operator [C#]
- ~ [C#], bitwise complement operator
- bitwise complement operator [C#]
ms.assetid: 11bc078a-50e2-4d7e-9896-67ef669dc602
ms.openlocfilehash: 8af25217f9e7e66796192783a0b8e3415604dc90
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43510113"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="283b4-102">~ 연산자(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="283b4-102">~ Operator (C# Reference)</span></span>
<span data-ttu-id="283b4-103">`~` 연산자는 피연산자에 대해 비트 보수 연산을 수행하며, 각 비트를 반대로 하는 효과가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="283b4-103">The `~` operator performs a bitwise complement operation on its operand, which has the effect of reversing each bit.</span></span> <span data-ttu-id="283b4-104">비트 보수 연산자는 [int](../../../csharp/language-reference/keywords/int.md), [uint](../../../csharp/language-reference/keywords/uint.md), [long](../../../csharp/language-reference/keywords/long.md) 및 [ulong](../../../csharp/language-reference/keywords/ulong.md)에 대해 미리 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="283b4-104">Bitwise complement operators are predefined for [int](../../../csharp/language-reference/keywords/int.md), [uint](../../../csharp/language-reference/keywords/uint.md), [long](../../../csharp/language-reference/keywords/long.md), and [ulong](../../../csharp/language-reference/keywords/ulong.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="283b4-105">또한 `~` 기호는 종료자를 선언하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="283b4-105">The `~` symbol also is used to declare finalizers.</span></span> <span data-ttu-id="283b4-106">자세한 내용은 [종료자](../../../csharp/programming-guide/classes-and-structs/destructors.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="283b4-106">For more information, see [Finalizers](../../../csharp/programming-guide/classes-and-structs/destructors.md).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="283b4-107">설명</span><span class="sxs-lookup"><span data-stu-id="283b4-107">Remarks</span></span>  
 <span data-ttu-id="283b4-108">사용자 정의 형식은 `~` 연산자를 오버로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="283b4-108">User-defined types can overload the `~` operator.</span></span> <span data-ttu-id="283b4-109">자세한 내용은 [operator](../../../csharp/language-reference/keywords/operator.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="283b4-109">For more information, see [operator](../../../csharp/language-reference/keywords/operator.md).</span></span> <span data-ttu-id="283b4-110">정수 계열 형식에 대한 연산은 일반적으로 열거형에서 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="283b4-110">Operations on integral types are generally allowed on enumeration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="283b4-111">예</span><span class="sxs-lookup"><span data-stu-id="283b4-111">Example</span></span>  
 [!code-csharp[csRefOperators#25](../../../csharp/language-reference/operators/codesnippet/CSharp/bitwise-complement-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="283b4-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="283b4-112">See Also</span></span>

- [<span data-ttu-id="283b4-113">C# 참조</span><span class="sxs-lookup"><span data-stu-id="283b4-113">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="283b4-114">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="283b4-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="283b4-115">C# 연산자</span><span class="sxs-lookup"><span data-stu-id="283b4-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
- [<span data-ttu-id="283b4-116">종료자</span><span class="sxs-lookup"><span data-stu-id="283b4-116">Finalizers</span></span>](../../../csharp/programming-guide/classes-and-structs/destructors.md)
