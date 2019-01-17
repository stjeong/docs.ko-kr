---
title: '방법: 개체 이니셜라이저를 사용하여 개체 초기화 - C# 프로그래밍 가이드'
ms.custom: seodec18
ms.date: 12/20/2018
helpviewer_keywords:
- object initializers [C#], how to use
- objects [C#], initializing
ms.assetid: 4b75ebb2-2e29-43de-929c-d736a8f27ce6
ms.openlocfilehash: 29987b9ba1f1f18f4e768766bd2391ebb5862f97
ms.sourcegitcommit: d09c77414e9e4fc72c79b04deee7a756a120674e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54084877"
---
# <a name="how-to-initialize-objects-by-using-an-object-initializer-c-programming-guide"></a><span data-ttu-id="cdd44-102">방법: 개체 이니셜라이저를 사용하여 개체 초기화(C# 프로그래밍 가이드)</span><span class="sxs-lookup"><span data-stu-id="cdd44-102">How to: Initialize Objects by Using an Object Initializer (C# Programming Guide)</span></span>

<span data-ttu-id="cdd44-103">개체 이니셜라이저를 사용하여 형식에 대한 생성자를 명시적으로 호출하지 않고 선언적 방식으로 형식 개체를 초기화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cdd44-103">You can use object initializers to initialize type objects in a declarative manner without explicitly invoking a constructor for the type.</span></span>  
  
<span data-ttu-id="cdd44-104">다음 예제에서는 명명된 개체와 함께 개체 이니셜라이저를 사용하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cdd44-104">The following examples show how to use object initializers with named objects.</span></span> <span data-ttu-id="cdd44-105">컴파일러는 먼저 기본 인스턴스 생성자에 액세스한 다음 멤버 초기화를 처리하여 개체 이니셜라이저를 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd44-105">The compiler processes object initializers by first accessing the default instance constructor and then processing the member initializations.</span></span> <span data-ttu-id="cdd44-106">따라서 클래스에서 기본 생성자가 `private`로 선언된 경우 공용 액세스가 필요한 개체 이니셜라이저는 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd44-106">Therefore, if the default constructor is declared as `private` in the class, object initializers that require public access will fail.</span></span>
  
<span data-ttu-id="cdd44-107">무명 형식을 정의하는 경우 개체 이니셜라이저를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd44-107">You must use an object initializer if you're defining an anonymous type.</span></span> <span data-ttu-id="cdd44-108">자세한 내용은 [방법: 쿼리에서 요소 속성의 하위 집합 반환](how-to-return-subsets-of-element-properties-in-a-query.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cdd44-108">For more information, see [How to: Return Subsets of Element Properties in a Query](how-to-return-subsets-of-element-properties-in-a-query.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="cdd44-109">예제</span><span class="sxs-lookup"><span data-stu-id="cdd44-109">Example</span></span>  

<span data-ttu-id="cdd44-110">다음 예제에서는 개체 이니셜라이저를 사용하여 새 `StudentName` 형식을 초기화하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cdd44-110">The following example shows how to initialize a new `StudentName` type by using object initializers.</span></span> <span data-ttu-id="cdd44-111">이 예제에서는 `StudentName` 형식의 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd44-111">This example sets properties in the `StudentName` type:</span></span>
  
[!code-csharp-interactive[InitializerObjectExample](../../../../samples/snippets/csharp/programming-guide/classes-and-structs/object-collection-initializers/HowToObjectInitializers.cs#HowToObjectInitializers)]  

<span data-ttu-id="cdd44-112">개체 이니셜라이저를 사용하여 개체의 이니셜라이저를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cdd44-112">Object initializers can be used to set indexers in an object.</span></span> <span data-ttu-id="cdd44-113">다음 예제에서는 인덱서를 사용하여 여러 포지션의 선수를 가져오고 설정하는 `BaseballTeam` 클래스를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd44-113">The following example defines a `BaseballTeam` class that uses an indexer to get and set players at different positions.</span></span> <span data-ttu-id="cdd44-114">이 이니셜라이저는 포지션을 가리키는 약어 또는 각 포지션에 사용되는 번호를 기준으로 선수에게 야구 득점표를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cdd44-114">The initializer can assign players, based on the abbreviation for the position, or the number used for each position baseball scorecards:</span></span>

[!code-csharp-interactive[InitializerIndexerExample](../../../../samples/snippets/csharp/programming-guide/classes-and-structs/object-collection-initializers/HowToIndexInitializer.cs#HowToIndexInitializer)]  

## <a name="see-also"></a><span data-ttu-id="cdd44-115">참고 항목</span><span class="sxs-lookup"><span data-stu-id="cdd44-115">See Also</span></span>

- [<span data-ttu-id="cdd44-116">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="cdd44-116">C# Programming Guide</span></span>](../index.md)  
- [<span data-ttu-id="cdd44-117">개체 이니셜라이저 및 컬렉션 이니셜라이저</span><span class="sxs-lookup"><span data-stu-id="cdd44-117">Object and Collection Initializers</span></span>](object-and-collection-initializers.md)
