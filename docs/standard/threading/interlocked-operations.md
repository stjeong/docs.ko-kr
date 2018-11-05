---
title: 연동 작업
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Interlocked class, about Interlocked class
- threading [.NET Framework], Interlocked class
ms.assetid: cbda7114-c752-4f3e-ada1-b1e8dd262f2b
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6f96286da84e41e79fb0b6253d6f20eea89da21a
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50201357"
---
# <a name="interlocked-operations"></a><span data-ttu-id="a83fb-102">연동 작업</span><span class="sxs-lookup"><span data-stu-id="a83fb-102">Interlocked operations</span></span>

<span data-ttu-id="a83fb-103"><xref:System.Threading.Interlocked?displayProperty=nameWithType> 클래스는 여러 스레드에서 공유하는 변수에 대한 액세스를 동기화하는 메서드를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-103">The <xref:System.Threading.Interlocked?displayProperty=nameWithType> class provides methods that synchronize access to a variable that is shared by multiple threads.</span></span> <span data-ttu-id="a83fb-104">서로 다른 프로세스의 스레드는 변수가 공유 메모리에 있는 경우 이 메커니즘을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-104">The threads of different processes can use this mechanism if the variable is in shared memory.</span></span> <span data-ttu-id="a83fb-105">연동 작업은 원자성입니다. 즉, 전체 작업이 동일한 변수에 대한 다른 작업에 의해 중단될 수 없는 한 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-105">Interlocked operations are atomic — that is, the entire operation is a unit that cannot be interrupted by another operation on the same variable.</span></span> <span data-ttu-id="a83fb-106">이는 메모리 주소에서 값을 로드한 후 이를 변경하고 저장할 기회를 갖기 전에 스레드를 일시 중단할 수 있는 선점형 다중 스레딩과 함께 운영 체제에서 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-106">This is important in operating systems with preemptive multithreading, where a thread can be suspended after loading a value from a memory address, but before having the chance to alter it and store it.</span></span>  
  
 <span data-ttu-id="a83fb-107"><xref:System.Threading.Interlocked> 클래스는 다음과 같은 작업을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-107">The <xref:System.Threading.Interlocked> class provides the following operations:</span></span>  
  
-   <span data-ttu-id="a83fb-108"><xref:System.Threading.Interlocked.Add%2A?displayProperty=nameWithType> 메서드는 변수에 정수 값을 추가하고 변수의 새 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-108">The <xref:System.Threading.Interlocked.Add%2A?displayProperty=nameWithType> method adds an integer value to a variable and returns the new value of the variable.</span></span>  
  
-   <span data-ttu-id="a83fb-109"><xref:System.Threading.Interlocked.Read%2A?displayProperty=nameWithType> 메서드는 64비트 정수 값을 원자성 작업으로 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-109">The <xref:System.Threading.Interlocked.Read%2A?displayProperty=nameWithType> method reads a 64-bit integer value as an atomic operation.</span></span> <span data-ttu-id="a83fb-110">이는 64비트 정수 읽기가 일반적인 원자성 작업이 아닌 32비트 운영 체제에서 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-110">This is useful on 32-bit operating systems, where reading a 64-bit integer is not ordinarily an atomic operation.</span></span>  
  
-   <span data-ttu-id="a83fb-111"><xref:System.Threading.Interlocked.Increment%2A?displayProperty=nameWithType> 및 <xref:System.Threading.Interlocked.Decrement%2A?displayProperty=nameWithType> 메서드는 변수를 증가하거나 감소하고 결과 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-111">The <xref:System.Threading.Interlocked.Increment%2A?displayProperty=nameWithType> and <xref:System.Threading.Interlocked.Decrement%2A?displayProperty=nameWithType> methods increment or decrement a variable and return the resulting value.</span></span>  
  
-   <span data-ttu-id="a83fb-112"><xref:System.Threading.Interlocked.Exchange%2A?displayProperty=nameWithType> 메서드는 지정된 변수의 값에 대한 원자성 교환을 수행하고 해당 값을 반환하여 새 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-112">The <xref:System.Threading.Interlocked.Exchange%2A?displayProperty=nameWithType> method performs an atomic exchange of the value in a specified variable, returning that value and replacing it with a new value.</span></span> <span data-ttu-id="a83fb-113">이 메서드의 제네릭 <xref:System.Threading.Interlocked.Exchange%60%601%28%60%600%40%2C%60%600%29> 오버로드를 사용하여 모든 참조 형식의 변수에 대해 교환을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-113">Use a generic <xref:System.Threading.Interlocked.Exchange%60%601%28%60%600%40%2C%60%600%29> overload of this method to perform the exchange on a variable of any reference type.</span></span>  
  
-   <span data-ttu-id="a83fb-114"><xref:System.Threading.Interlocked.CompareExchange%2A?displayProperty=nameWithType> 메서드도 두 값을 교환하지만 비교 결과에 대해 불확정합니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-114">The <xref:System.Threading.Interlocked.CompareExchange%2A?displayProperty=nameWithType> method also exchanges two values, but contingent on the result of a comparison.</span></span> <span data-ttu-id="a83fb-115">이 메서드의 제네릭 <xref:System.Threading.Interlocked.CompareExchange%60%601%28%60%600%40%2C%60%600%2C%60%600%29> 오버로드를 사용하여 모든 참조 형식의 변수에 대해 교환을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-115">Use a generic <xref:System.Threading.Interlocked.CompareExchange%60%601%28%60%600%40%2C%60%600%2C%60%600%29> overload of this method to perform the exchange on a variable of any reference type.</span></span>  
  
 <span data-ttu-id="a83fb-116">최신 프로세서에서 <xref:System.Threading.Interlocked> 클래스의 메서드는 일반적으로 단일 명령으로 구현될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-116">On modern processors, the methods of the <xref:System.Threading.Interlocked> class can often be implemented by a single instruction.</span></span> <span data-ttu-id="a83fb-117">따라서 고성능 동기화를 제공하며 스핀 잠금과 같은 더 높은 수준의 동기화 메커니즘을 빌드하는 데 사용될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-117">Thus, they provide very high-performance synchronization and can be used to build higher-level synchronization mechanisms, like spin locks.</span></span>  
  
 <span data-ttu-id="a83fb-118"><xref:System.Threading.Monitor> 및 <xref:System.Threading.Interlocked> 클래스를 함께 사용하는 예제는 <xref:System.Threading.Monitor>를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a83fb-118">For an example that uses the <xref:System.Threading.Monitor> and <xref:System.Threading.Interlocked> classes in combination, see <xref:System.Threading.Monitor>.</span></span>  
  
## <a name="compareexchange-example"></a><span data-ttu-id="a83fb-119">CompareExchange 예제</span><span class="sxs-lookup"><span data-stu-id="a83fb-119">CompareExchange example</span></span>

 <span data-ttu-id="a83fb-120"><xref:System.Threading.Interlocked.CompareExchange%2A> 메서드를 사용하여 단순 증가 및 감소보다 복잡한 계산을 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-120">The <xref:System.Threading.Interlocked.CompareExchange%2A> method can be used to protect computations that are more complicated than simple increment and decrement.</span></span> <span data-ttu-id="a83fb-121">다음 예제에서는 부동 소수점 숫자로 저장되는 누계에 추가하는 스레드로부터 안전한 메서드를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-121">The following example demonstrates a thread-safe method that adds to a running total stored as a floating point number.</span></span> <span data-ttu-id="a83fb-122">(정수의 경우 <xref:System.Threading.Interlocked.Add%2A> 메서드는 더욱 간단한 솔루션입니다. ) 전체 코드 예제는 단정밀도 및 배정밀도 부동 소수점 인수(<xref:System.Threading.Interlocked.CompareExchange%28System.Single%40%2CSystem.Single%2CSystem.Single%29> 및 <xref:System.Threading.Interlocked.CompareExchange%28System.Double%40%2CSystem.Double%2CSystem.Double%29>)를 사용하는 <xref:System.Threading.Interlocked.CompareExchange%2A>의 오버로드를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a83fb-122">(For integers, the <xref:System.Threading.Interlocked.Add%2A> method is a simpler solution.) For complete code examples, see the overloads of <xref:System.Threading.Interlocked.CompareExchange%2A> that take single-precision and double-precision floating-point arguments (<xref:System.Threading.Interlocked.CompareExchange%28System.Single%40%2CSystem.Single%2CSystem.Single%29> and <xref:System.Threading.Interlocked.CompareExchange%28System.Double%40%2CSystem.Double%2CSystem.Double%29>).</span></span>  
  
 [!code-cpp[Conceptual.Interlocked#1](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.interlocked/cpp/source1.cpp#1)]
 [!code-csharp[Conceptual.Interlocked#1](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.interlocked/cs/source1.cs#1)]
 [!code-vb[Conceptual.Interlocked#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.interlocked/vb/source1.vb#1)]  
  
## <a name="untyped-overloads-of-exchange-and-compareexchange"></a><span data-ttu-id="a83fb-123">Exchange 및 CompareExchange의 형식화되지 않은 오버로드</span><span class="sxs-lookup"><span data-stu-id="a83fb-123">Untyped overloads of Exchange and CompareExchange</span></span>

 <span data-ttu-id="a83fb-124"><xref:System.Threading.Interlocked.Exchange%2A> 및 <xref:System.Threading.Interlocked.CompareExchange%2A> 메서드에는 <xref:System.Object> 형식의 인수를 사용하는 오버로드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-124">The <xref:System.Threading.Interlocked.Exchange%2A> and <xref:System.Threading.Interlocked.CompareExchange%2A> methods have overloads that take arguments of type <xref:System.Object>.</span></span> <span data-ttu-id="a83fb-125">이러한 각 오버로드의 첫 번째 인수는 `ref Object`(Visual Basic의 경우 `ByRef … As Object`)이며 형식 안전성을 위해서는 이 인수로 전달되는 변수를 <xref:System.Object>로 엄격하게 형식을 지정해야 합니다. 이러한 메서드를 호출할 때 <xref:System.Object> 형식으로 첫 번째 인수를 간단하게 캐스트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-125">The first argument of each of these overloads is `ref Object` (`ByRef … As Object` in Visual Basic), and type safety requires the variable passed to this argument to be typed strictly as <xref:System.Object>; you cannot simply cast the first argument to type <xref:System.Object> when calling these methods.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a83fb-126">.NET Framework 버전 2.0 이상에서 <xref:System.Threading.Interlocked.Exchange%2A> 및 <xref:System.Threading.Interlocked.CompareExchange%2A> 메서드의 제네릭 오버로드를 사용하여 강력한 형식의 변수를 교환합니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-126">In the .NET Framework version 2.0 and later, use the generic overloads of the <xref:System.Threading.Interlocked.Exchange%2A> and <xref:System.Threading.Interlocked.CompareExchange%2A> methods to exchange strongly typed variables.</span></span>  
  
 <span data-ttu-id="a83fb-127">다음 코드 예제에서는 .NET Framework 버전 1.0 또는 1.1에서 구현될 수 있는 것처럼 한 번만 설정될 수 있는 `ClassA` 형식의 속성을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a83fb-127">The following code example shows a property of type `ClassA` that can be set only once, as it might be implemented in the .NET Framework version 1.0 or 1.1.</span></span>  
  
 [!code-cpp[Conceptual.Interlocked#2](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.interlocked/cpp/source2.cpp#2)]
 [!code-csharp[Conceptual.Interlocked#2](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.interlocked/cs/source2.cs#2)]
 [!code-vb[Conceptual.Interlocked#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.interlocked/vb/source2.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="a83fb-128">참고 항목</span><span class="sxs-lookup"><span data-stu-id="a83fb-128">See also</span></span>

- <xref:System.Threading.Interlocked?displayProperty=nameWithType>  
- <xref:System.Threading.Monitor?displayProperty=nameWithType>  
- [<span data-ttu-id="a83fb-129">스레딩</span><span class="sxs-lookup"><span data-stu-id="a83fb-129">Threading</span></span>](index.md)  
- [<span data-ttu-id="a83fb-130">스레딩 개체 및 기능</span><span class="sxs-lookup"><span data-stu-id="a83fb-130">Threading objects and features</span></span>](threading-objects-and-features.md)
