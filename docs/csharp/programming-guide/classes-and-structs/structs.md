---
title: 구조체 - C# 프로그래밍 가이드
ms.custom: seodec18
ms.date: 08/21/2018
helpviewer_keywords:
- C# language, structs
- structs [C#]
ms.assetid: b7cf4ff2-0eb7-4e5c-93d5-b2196b4f5d89
ms.openlocfilehash: 609169d4624802f679f9661b7aa0596403cc48e7
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55261622"
---
# <a name="structs-c-programming-guide"></a><span data-ttu-id="be4b1-102">구조체(C# 프로그래밍 가이드)</span><span class="sxs-lookup"><span data-stu-id="be4b1-102">Structs (C# Programming Guide)</span></span>

<span data-ttu-id="be4b1-103">구조체는 [struct](../../language-reference/keywords/struct.md) 키워드를 사용하여 정의합니다. 예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="be4b1-103">Structs are defined by using the [struct](../../language-reference/keywords/struct.md) keyword, for example:</span></span>  
  
[!code-csharp[csProgGuideObjects#39](./codesnippet/CSharp/structs_1.cs)]  
  
<span data-ttu-id="be4b1-104">구조체는 클래스와 대부분 동일한 구문을 공유합니다.</span><span class="sxs-lookup"><span data-stu-id="be4b1-104">Structs share most of the same syntax as classes.</span></span> <span data-ttu-id="be4b1-105">구조체의 이름은 유효한 C# [식별자 이름](../inside-a-program/identifier-names.md)이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="be4b1-105">The name of the struct must be a valid C# [identifier name](../inside-a-program/identifier-names.md).</span></span> <span data-ttu-id="be4b1-106">구조체는 다음과 같은 방법으로 클래스보다 더 제한적입니다.</span><span class="sxs-lookup"><span data-stu-id="be4b1-106">Structs are more limited than classes in the following ways:</span></span>  
  
- <span data-ttu-id="be4b1-107">구조체 선언 내에서 필드가 const 또는 static으로 선언된 경우가 아니면 필드를 초기화할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="be4b1-107">Within a struct declaration, fields cannot be initialized unless they are declared as const or static.</span></span>  
- <span data-ttu-id="be4b1-108">구조체는 기본 생성자(매개 변수가 없는 생성자) 또는 종료자를 선언할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="be4b1-108">A struct cannot declare a default constructor (a constructor without parameters) or a finalizer.</span></span>  
- <span data-ttu-id="be4b1-109">할당 시 구조체가 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="be4b1-109">Structs are copied on assignment.</span></span> <span data-ttu-id="be4b1-110">구조체를 새 변수에 할당하면 모든 데이터가 복사되고, 새 복사본을 수정해도 원래 복사본의 데이터는 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be4b1-110">When a struct is assigned to a new variable, all the data is copied, and any modification to the new copy does not change the data for the original copy.</span></span> <span data-ttu-id="be4b1-111">`Dictionary<string, myStruct>`와 같은 값 형식의 컬렉션으로 작업할 때 이 점을 명심해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="be4b1-111">This is important to remember when working with collections of value types such as `Dictionary<string, myStruct>`.</span></span>  
- <span data-ttu-id="be4b1-112">구조체는 참조 형식인 클래스와 달리 값 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="be4b1-112">Structs are value types, unlike classes, which are reference types.</span></span>  
- <span data-ttu-id="be4b1-113">클래스와 달리 구조체는 `new` 연산자를 사용하지 않고 인스턴스화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be4b1-113">Unlike classes, structs can be instantiated without using a `new` operator.</span></span>  
- <span data-ttu-id="be4b1-114">구조체는 매개 변수가 있는 생성자를 선언할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be4b1-114">Structs can declare constructors that have parameters.</span></span> 
- <span data-ttu-id="be4b1-115">구조체는 다른 구조체 또는 클래스에서 상속될 수 없으며, 클래스의 기본 클래스가 될 수도 없습니다.</span><span class="sxs-lookup"><span data-stu-id="be4b1-115">A struct cannot inherit from another struct or class, and it cannot be the base of a class.</span></span> <span data-ttu-id="be4b1-116">모든 구조체는 <xref:System.Object>에서 상속하는 <xref:System.ValueType>에서 직접 상속합니다.</span><span class="sxs-lookup"><span data-stu-id="be4b1-116">All structs inherit directly from <xref:System.ValueType>, which inherits from <xref:System.Object>.</span></span>  
- <span data-ttu-id="be4b1-117">구조체는 인터페이스를 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be4b1-117">A struct can implement interfaces.</span></span> 
- <span data-ttu-id="be4b1-118">변수가 널 nullable 형식으로 선언되지 않으면 구조체는 `null`일 수 없으며 구조체 변수에 `null`을 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="be4b1-118">A struct cannot be `null`, and a struct variable cannot be assigned `null` unless the variable is declared as a nullable type.</span></span>
  
## <a name="related-sections"></a><span data-ttu-id="be4b1-119">관련 단원</span><span class="sxs-lookup"><span data-stu-id="be4b1-119">Related sections</span></span>  

<span data-ttu-id="be4b1-120">추가 정보</span><span class="sxs-lookup"><span data-stu-id="be4b1-120">For more information:</span></span>  
  
- [<span data-ttu-id="be4b1-121">구조체 사용</span><span class="sxs-lookup"><span data-stu-id="be4b1-121">Using Structs</span></span>](using-structs.md)
- [<span data-ttu-id="be4b1-122">생성자</span><span class="sxs-lookup"><span data-stu-id="be4b1-122">Constructors</span></span>](constructors.md)
- [<span data-ttu-id="be4b1-123">Nullable 형식</span><span class="sxs-lookup"><span data-stu-id="be4b1-123">Nullable Types</span></span>](../nullable-types/index.md)
- [<span data-ttu-id="be4b1-124">방법: 메서드에 구조체를 전달하는 것과 클래스 참조를 전달하는 것의 차이점 이해</span><span class="sxs-lookup"><span data-stu-id="be4b1-124">How to: Know the Difference Between Passing a Struct and Passing a Class Reference to a Method</span></span>](how-to-know-the-difference-passing-a-struct-and-passing-a-class-to-a-method.md)
- [<span data-ttu-id="be4b1-125">방법: 구조체 간의 사용자 정의 변환 구현</span><span class="sxs-lookup"><span data-stu-id="be4b1-125">How to: Implement User-Defined Conversions Between Structs</span></span>](../statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)

## <a name="see-also"></a><span data-ttu-id="be4b1-126">참고 항목</span><span class="sxs-lookup"><span data-stu-id="be4b1-126">See also</span></span>

- [<span data-ttu-id="be4b1-127">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="be4b1-127">C# Programming Guide</span></span>](../index.md)
- [<span data-ttu-id="be4b1-128">클래스 및 구조체</span><span class="sxs-lookup"><span data-stu-id="be4b1-128">Classes and Structs</span></span>](index.md)
- [<span data-ttu-id="be4b1-129">클래스</span><span class="sxs-lookup"><span data-stu-id="be4b1-129">Classes</span></span>](classes.md)
- [<span data-ttu-id="be4b1-130">식별자 이름</span><span class="sxs-lookup"><span data-stu-id="be4b1-130">Identifier names</span></span>](../inside-a-program/identifier-names.md)
