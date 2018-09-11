---
title: '방법: 대리자 조합(멀티캐스트 대리자)(C# 프로그래밍 가이드)'
ms.date: 07/20/2015
helpviewer_keywords:
- delegates [C#], combining
- multicast delegates [C#]
ms.assetid: 4e689450-6d0c-46de-acfd-f961018ae5dd
ms.openlocfilehash: e3cc3f9082bd86004a7821b64c01253408c07641
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44083279"
---
# <a name="how-to-combine-delegates-multicast-delegatesc-programming-guide"></a><span data-ttu-id="ffbfe-102">방법: 대리자 조합(멀티캐스트 대리자)(C# 프로그래밍 가이드)</span><span class="sxs-lookup"><span data-stu-id="ffbfe-102">How to: Combine Delegates (Multicast Delegates)(C# Programming Guide)</span></span>
<span data-ttu-id="ffbfe-103">이 예제에서는 멀티캐스트 대리자를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-103">This example demonstrates how to create multicast delegates.</span></span> <span data-ttu-id="ffbfe-104">[대리자](../../../csharp/language-reference/keywords/delegate.md) 개체의 유용한 속성은 `+` 연산자를 사용하여 하나의 대리자 인스턴스에 여러 개체를 할당할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-104">A useful property of [delegate](../../../csharp/language-reference/keywords/delegate.md) objects is that multiple objects can be assigned to one delegate instance by using the `+` operator.</span></span> <span data-ttu-id="ffbfe-105">멀티캐스트 대리자는 할당된 대리자 목록을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-105">The multicast delegate contains a list of the assigned delegates.</span></span> <span data-ttu-id="ffbfe-106">멀티캐스트 대리자가 호출되면 목록에 있는 대리자가 순서대로 호출됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-106">When the multicast delegate is called, it invokes the delegates in the list, in order.</span></span> <span data-ttu-id="ffbfe-107">같은 형식의 대리자만 결합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-107">Only delegates of the same type can be combined.</span></span>  
  
 <span data-ttu-id="ffbfe-108">`-` 연산자는 멀티캐스트 대리자에서 구성 요소 대리자를 제거하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-108">The `-` operator can be used to remove a component delegate from a multicast delegate.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ffbfe-109">예</span><span class="sxs-lookup"><span data-stu-id="ffbfe-109">Example</span></span>  
 [!code-csharp[csProgGuideDelegates#11](../../../csharp/programming-guide/delegates/codesnippet/CSharp/how-to-combine-delegates-multicast-delegates_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="ffbfe-110">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ffbfe-110">See Also</span></span>

- <xref:System.MulticastDelegate>  
- [<span data-ttu-id="ffbfe-111">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="ffbfe-111">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="ffbfe-112">이벤트</span><span class="sxs-lookup"><span data-stu-id="ffbfe-112">Events</span></span>](../../../csharp/programming-guide/events/index.md)
