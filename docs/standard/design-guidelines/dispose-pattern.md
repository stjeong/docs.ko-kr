---
title: 삭제 패턴
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- Dispose method
- class library design guidelines [.NET Framework], Dispose method
- class library design guidelines [.NET Framework], Finalize method
- customizing Dispose method name
- Finalize method
ms.assetid: 31a6c13b-d6a2-492b-9a9f-e5238c983bcb
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ff52e17cfe4a4236e4d165c0961ca3a23fed9a72
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43864646"
---
# <a name="dispose-pattern"></a><span data-ttu-id="dda1a-102">삭제 패턴</span><span class="sxs-lookup"><span data-stu-id="dda1a-102">Dispose Pattern</span></span>
<span data-ttu-id="dda1a-103">모든 프로그램 실행 하는 동안 메모리, 시스템 핸들 또는 데이터베이스 연결 같은 하나 이상의 시스템 리소스를 획득합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-103">All programs acquire one or more system resources, such as memory, system handles, or database connections, during the course of their execution.</span></span> <span data-ttu-id="dda1a-104">개발자는 획득 되 고 사용 후 릴리스해야 합니다. 때문에 이러한 시스템 리소스를 사용할 때는 주의 해야 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-104">Developers have to be careful when using such system resources, because they must be released after they have been acquired and used.</span></span>  
  
 <span data-ttu-id="dda1a-105">CLR 자동 메모리 관리에 대 한 지원을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-105">The CLR provides support for automatic memory management.</span></span> <span data-ttu-id="dda1a-106">관리 되는 메모리 (C# 연산자를 사용 하 여 할당 된 메모리 `new`) 명시적으로 해제 될 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-106">Managed memory (memory allocated using the C# operator `new`) does not need to be explicitly released.</span></span> <span data-ttu-id="dda1a-107">가비지 수집기 (GC)에 의해 자동으로 해제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-107">It is released automatically by the garbage collector (GC).</span></span> <span data-ttu-id="dda1a-108">이 메모리를 해제 작업이 지루해 지 고 어려운 태스크에서 개발자를 해제 하 고는 전례 없는 생산성.NET Framework에서 제공 하는 주요 이유 중 하나 였습니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-108">This frees developers from the tedious and difficult task of releasing memory and has been one of the main reasons for the unprecedented productivity afforded by the .NET Framework.</span></span>  
  
 <span data-ttu-id="dda1a-109">그러나 관리 되는 메모리 많은 시스템 리소스 종류 중 하나일 뿐입니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-109">Unfortunately, managed memory is just one of many types of system resources.</span></span> <span data-ttu-id="dda1a-110">이외의 관리 되는 메모리 리소스는 여전히 명시적으로 해제 해야 하 고 관리 되지 않는 리소스 라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-110">Resources other than managed memory still need to be released explicitly and are referred to as unmanaged resources.</span></span> <span data-ttu-id="dda1a-111">GC 특별히 설계 되지 않았습니다 이러한 관리 되지 않는 리소스를 관리 하려면 관리 되지 않는 리소스를 관리 하는 것에 대 한 책임은 개발자의 손에 의미.</span><span class="sxs-lookup"><span data-stu-id="dda1a-111">The GC was specifically not designed to manage such unmanaged resources, which means that the responsibility for managing unmanaged resources lies in the hands of the developers.</span></span>  
  
 <span data-ttu-id="dda1a-112">CLR 관리 되지 않는 리소스를 해제에 대 한 도움을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-112">The CLR provides some help in releasing unmanaged resources.</span></span> <span data-ttu-id="dda1a-113"><xref:System.Object?displayProperty=nameWithType> 가상 메서드를 선언 <xref:System.Object.Finalize%2A> (종료자 라고도 함)는 라고 GC가 개체의 메모리 GC에 의해 회수 되 고 관리 되지 않는 리소스를 해제 하도록 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-113"><xref:System.Object?displayProperty=nameWithType> declares a virtual method <xref:System.Object.Finalize%2A> (also called the finalizer) that is called by the GC before the object’s memory is reclaimed by the GC and can be overridden to release unmanaged resources.</span></span> <span data-ttu-id="dda1a-114">종료자를 재정의 하는 종료 가능한 형식으로 참조 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-114">Types that override the finalizer are referred to as finalizable types.</span></span>  
  
 <span data-ttu-id="dda1a-115">종료자 일부 정리 시나리오에서는 유효 하지만, 두 가지 중요 한 단점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-115">Although finalizers are effective in some cleanup scenarios, they have two significant drawbacks:</span></span>  
  
-   <span data-ttu-id="dda1a-116">종료자는 GC에서 개체 컬렉션에 대 한 자격이 있는 것을 감지 하면 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-116">The finalizer is called when the GC detects that an object is eligible for collection.</span></span> <span data-ttu-id="dda1a-117">이 리소스를 더 이상 필요 하지 않은 후 결정 되지 않은 일정 기간 동안에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-117">This happens at some undetermined period of time after the resource is not needed anymore.</span></span> <span data-ttu-id="dda1a-118">개발자의 수 또는 종료자에 의해 리소스가 실제로 해제 되는 경우 시간과 리소스를 해제 하려는 경우 사이의 지연을 또는 여러 부족 한 리소스는 리소스 (쉽게 소진 될 수 있습니다.)를 획득 하는 프로그램에서 허용 되지 않을 수 있습니다. 리소스 사용 (예: 관리 되지 않는 대용량 메모리 버퍼)을 유지 하려면 비용이 많이 들에 사례입니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-118">The delay between when the developer could or would like to release the resource and the time when the resource is actually released by the finalizer might be unacceptable in programs that acquire many scarce resources (resources that can be easily exhausted) or in cases in which resources are costly to keep in use (e.g., large unmanaged memory buffers).</span></span>  
  
-   <span data-ttu-id="dda1a-119">CLR에 종료자를 호출 해야 하는 경우 다음 가비지 컬렉션 (컬렉션 간에 실행 종료자)의 반올림 될 때까지 컬렉션 개체의 메모리를 연기 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-119">When the CLR needs to call a finalizer, it must postpone collection of the object’s memory until the next round of garbage collection (the finalizers run between collections).</span></span> <span data-ttu-id="dda1a-120">이 개체의 메모리 및 모든 개체 참조를 긴 시간 동안 해제 되지 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-120">This means that the object’s memory (and all objects it refers to) will not be released for a longer period of time.</span></span>  
  
 <span data-ttu-id="dda1a-121">따라서 종료자에만 의존 하지 않을 또는 시나리오에는 성능이 매우 부족 한 리소스를 처리할 때 가능한 한 신속 하 게 관리 되지 않는 리소스를 회수 하는 경우 많은 시나리오에서 적절 한 추가 GC 오버 헤드 종료의 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-121">Therefore, relying exclusively on finalizers might not be appropriate in many scenarios when it is important to reclaim unmanaged resources as quickly as possible, when dealing with scarce resources, or in highly performant scenarios in which the added GC overhead of finalization is unacceptable.</span></span>  
  
 <span data-ttu-id="dda1a-122">프레임 워크는 제공 된 <xref:System.IDisposable?displayProperty=nameWithType> 개발자 필요 하지 않은으로 관리 되지 않는 리소스를 해제 하는 수동 방법을 제공 하기 위해 구현 해야 하는 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-122">The Framework provides the <xref:System.IDisposable?displayProperty=nameWithType> interface that should be implemented to provide the developer a manual way to release unmanaged resources as soon as they are not needed.</span></span> <span data-ttu-id="dda1a-123">또한 제공 된 <xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType> GC 차이점을 확인할 수 있는 개체의 수동으로 삭제 된 메서드와 개체의 메모리를 이전 회수 될 수 있습니다이 경우 더 이상 종료 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-123">It also provides the <xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType> method that can tell the GC that an object was manually disposed of and does not need to be finalized anymore, in which case the object’s memory can be reclaimed earlier.</span></span> <span data-ttu-id="dda1a-124">구현 하는 형식는 `IDisposable` 인터페이스는 삭제 가능한 형식 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-124">Types that implement the `IDisposable` interface are referred to as disposable types.</span></span>  
  
 <span data-ttu-id="dda1a-125">Dispose 패턴을 사용 및 종료자의 구현을 표준화 됩니다 및 `IDisposable` 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-125">The Dispose Pattern is intended to standardize the usage and implementation of finalizers and the `IDisposable` interface.</span></span>  
  
 <span data-ttu-id="dda1a-126">패턴의 주요 동기 부여는 구현의 복잡성을 줄이기 위해 합니다 <xref:System.Object.Finalize%2A> 하며 <xref:System.IDisposable.Dispose%2A> 메서드.</span><span class="sxs-lookup"><span data-stu-id="dda1a-126">The main motivation for the pattern is to reduce the complexity of the implementation of the <xref:System.Object.Finalize%2A> and the <xref:System.IDisposable.Dispose%2A> methods.</span></span> <span data-ttu-id="dda1a-127">복잡성은 메서드 (차이점은 챕터의 뒷부분에 설명 됨) 하는 전부는 아니지만 일부 코드 경로 공유 하는 팩트에서 기인 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-127">The complexity stems from the fact that the methods share some but not all code paths (the differences are described later in the chapter).</span></span> <span data-ttu-id="dda1a-128">또한 결정적 리소스 관리에 대 한 언어 지원 개선과 관련 된 패턴의 일부 요소에 대 한 기록 이유가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-128">In addition, there are historical reasons for some elements of the pattern related to the evolution of language support for deterministic resource management.</span></span>  
  
 <span data-ttu-id="dda1a-129">**✓ DO** 삭제 가능한 형식은의 인스턴스를 포함 하는 형식에 기본 Dispose 패턴을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-129">**✓ DO** implement the Basic Dispose Pattern on types containing instances of disposable types.</span></span> <span data-ttu-id="dda1a-130">참조 된 [기본 Dispose 패턴](#basic_pattern) 기본 패턴에 대 한 자세한 내용은 섹션입니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-130">See the [Basic Dispose Pattern](#basic_pattern) section for details on the basic pattern.</span></span>  
  
 <span data-ttu-id="dda1a-131">형식이 다른 삭제 가능한 개체의 수명을 담당 하는 경우 개발자는 너무을 삭제 하는 방법을 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-131">If a type is responsible for the lifetime of other disposable objects, developers need a way to dispose of them, too.</span></span> <span data-ttu-id="dda1a-132">컨테이너의를 사용 하 여 `Dispose` 메서드는이 가능 하 게 하는 편리한 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-132">Using the container’s `Dispose` method is a convenient way to make this possible.</span></span>  
  
 <span data-ttu-id="dda1a-133">**✓ DO** 기본 Dispose 패턴을 구현 하 고 보유 중인 리소스를 명시적으로 해제 해야 하 고 종료자가 없는 형식에 종료자를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-133">**✓ DO** implement the Basic Dispose Pattern and provide a finalizer on types holding resources that need to be freed explicitly and that do not have finalizers.</span></span>  
  
 <span data-ttu-id="dda1a-134">예를 들어 관리 되지 않는 메모리 버퍼를 저장 하는 형식에서 패턴을 구현 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-134">For example, the pattern should be implemented on types storing unmanaged memory buffers.</span></span> <span data-ttu-id="dda1a-135">합니다 [종료할 형식](#finalizable_types) 섹션 종료자를 구현 하는 데 관련 된 지침에 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-135">The [Finalizable Types](#finalizable_types) section discusses guidelines related to implementing finalizers.</span></span>  
  
 <span data-ttu-id="dda1a-136">**✓ CONSIDER** 클래스에 직접 저장 하지 않으므로 관리 되지 않는 리소스 또는 삭제 가능한 개체 이지만 수행 하는 하위 종류가 가능성은 기본 Dispose 패턴을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-136">**✓ CONSIDER** implementing the Basic Dispose Pattern on classes that themselves don’t hold unmanaged resources or disposable objects but are likely to have subtypes that do.</span></span>  
  
 <span data-ttu-id="dda1a-137">이 좋은 예로 <xref:System.IO.Stream?displayProperty=nameWithType> 클래스.</span><span class="sxs-lookup"><span data-stu-id="dda1a-137">A great example of this is the <xref:System.IO.Stream?displayProperty=nameWithType> class.</span></span> <span data-ttu-id="dda1a-138">모든 리소스를 포함 하지 않습니다 하는 추상 기본 클래스는 아니지만 대부분의 하위 클래스 및이 인해이 패턴을 구현 하 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-138">Although it is an abstract base class that doesn’t hold any resources, most of its subclasses do and because of this, it implements this pattern.</span></span>  
  
<a name="basic_pattern"></a>   
## <a name="basic-dispose-pattern"></a><span data-ttu-id="dda1a-139">기본 삭제 패턴</span><span class="sxs-lookup"><span data-stu-id="dda1a-139">Basic Dispose Pattern</span></span>  
 <span data-ttu-id="dda1a-140">패턴의 기본 구현을 포함 합니다 `System.IDisposable` 를 선언 하는 인터페이스를 `Dispose(bool)` 간에 공유 하도록 모든 리소스 정리 논리를 구현 하는 메서드를 `Dispose` 메서드와 선택적 종료자.</span><span class="sxs-lookup"><span data-stu-id="dda1a-140">The basic implementation of the pattern involves implementing the `System.IDisposable` interface and declaring the `Dispose(bool)` method that implements all resource cleanup logic to be shared between the `Dispose` method and the optional finalizer.</span></span>  
  
 <span data-ttu-id="dda1a-141">다음 예제에서는 기본 패턴의 간단한 구현을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-141">The following example shows a simple implementation of the basic pattern:</span></span>  
  
```csharp
public class DisposableResourceHolder : IDisposable {  
  
    private SafeHandle resource; // handle to a resource  
  
    public DisposableResourceHolder() {  
        this.resource = ... // allocates the resource  
    }  
  
    public void Dispose() {  
        Dispose(true);  
        GC.SuppressFinalize(this);  
    }  
  
    protected virtual void Dispose(bool disposing) {  
        if (disposing) {  
            if (resource!= null) resource.Dispose();  
        }  
    }  
}  
```  
  
 <span data-ttu-id="dda1a-142">부울 매개 변수 `disposing` 에서 메서드를 호출한 여부를 나타냅니다는 `IDisposable.Dispose` 구현 또는 종료자에서.</span><span class="sxs-lookup"><span data-stu-id="dda1a-142">The Boolean parameter `disposing` indicates whether the method was invoked from the `IDisposable.Dispose` implementation or from the finalizer.</span></span> <span data-ttu-id="dda1a-143">`Dispose(bool)` 구현을 다른 참조 개체 (예를 들어 이전 샘플의 리소스 필드)에 액세스 하기 전에 매개 변수를 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-143">The `Dispose(bool)` implementation should check the parameter before accessing other reference objects (e.g., the resource field in the preceding sample).</span></span> <span data-ttu-id="dda1a-144">이러한 개체에서 메서드를 호출할 때에 액세스 해야 합니다 `IDisposable.Dispose` 구현 (때는 `disposing` 매개 변수는 true와 같음).</span><span class="sxs-lookup"><span data-stu-id="dda1a-144">Such objects should only be accessed when the method is called from the `IDisposable.Dispose` implementation (when the `disposing` parameter is equal to true).</span></span> <span data-ttu-id="dda1a-145">메서드가 종료자에서 호출 된 경우 (`disposing` 은 false)를 다른 개체는 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-145">If the method is invoked from the finalizer (`disposing` is false), other objects should not be accessed.</span></span> <span data-ttu-id="dda1a-146">그 이유는 개체는 순서에 관계 없이 종료 하므로, 또는 해당 종속성 수 이미 종료 되었을 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-146">The reason is that objects are finalized in an unpredictable order and so they, or any of their dependencies, might already have been finalized.</span></span>  
  
 <span data-ttu-id="dda1a-147">또한이 섹션에서는 이미 삭제 패턴을 구현 하지 않는 기본 클래스에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-147">Also, this section applies to classes with a base that does not already implement the Dispose Pattern.</span></span> <span data-ttu-id="dda1a-148">이미 패턴을 구현 하는 클래스에서 상속 하는 경우 재정의 하기만 합니다 `Dispose(bool)` 추가 리소스 정리 논리를 제공 하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-148">If you are inheriting from a class that already implements the pattern, simply override the `Dispose(bool)` method to provide additional resource cleanup logic.</span></span>  
  
 <span data-ttu-id="dda1a-149">**✓ DO** 선언는 `protected virtual void Dispose(bool disposing)` 관련 된 모든 논리를 중앙 집중화 메서드 관리 되지 않는 리소스를 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-149">**✓ DO** declare a `protected virtual void Dispose(bool disposing)` method to centralize all logic related to releasing unmanaged resources.</span></span>  
  
 <span data-ttu-id="dda1a-150">이 메서드에서 모든 리소스 정리를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-150">All resource cleanup should occur in this method.</span></span> <span data-ttu-id="dda1a-151">메서드가 모두 종료자에서 호출 되 고 `IDisposable.Dispose` 메서드.</span><span class="sxs-lookup"><span data-stu-id="dda1a-151">The method is called from both the finalizer and the `IDisposable.Dispose` method.</span></span> <span data-ttu-id="dda1a-152">매개 변수는 종료 자가 내에서 호출 되는 경우에 false 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-152">The parameter will be false if being invoked from inside a finalizer.</span></span> <span data-ttu-id="dda1a-153">종료 하는 동안 실행 되는 모든 코드에는 다른 종료 가능한 개체에 액세스 하는 데 사용할 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-153">It should be used to ensure any code running during finalization is not accessing other finalizable objects.</span></span> <span data-ttu-id="dda1a-154">종료자를 구현 하는 다음 섹션에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-154">Details of implementing finalizers are described in the next section.</span></span>  
  
```csharp
protected virtual void Dispose(bool disposing) {  
    if (disposing) {  
        if (resource!= null) resource.Dispose();  
    }  
}  
```  
  
 <span data-ttu-id="dda1a-155">**✓ DO** 구현는 `IDisposable` 단순히 호출 하 여 인터페이스 `Dispose(true)` 이어서 `GC.SuppressFinalize(this)`합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-155">**✓ DO** implement the `IDisposable` interface by simply calling `Dispose(true)` followed by `GC.SuppressFinalize(this)`.</span></span>  
  
 <span data-ttu-id="dda1a-156">에 대 한 호출 `SuppressFinalize` 경우에 발생 해야 `Dispose(true)` 성공적으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-156">The call to `SuppressFinalize` should only occur if `Dispose(true)` executes successfully.</span></span>  
  
```csharp
public void Dispose(){  
    Dispose(true);  
    GC.SuppressFinalize(this);  
}  
```  
  
 <span data-ttu-id="dda1a-157">**X DO NOT** 매개 변수가 없는 확인 `Dispose` 가상 메서드.</span><span class="sxs-lookup"><span data-stu-id="dda1a-157">**X DO NOT** make the parameterless `Dispose` method virtual.</span></span>  
  
 <span data-ttu-id="dda1a-158">`Dispose(bool)` 메서드는 서브 클래스에서 재정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-158">The `Dispose(bool)` method is the one that should be overridden by subclasses.</span></span>  
  
```csharp
// bad design  
public class DisposableResourceHolder : IDisposable {  
    public virtual void Dispose() { ... }  
    protected virtual void Dispose(bool disposing) { ... }  
}  
  
// good design  
public class DisposableResourceHolder : IDisposable {  
    public void Dispose() { ... }  
    protected virtual void Dispose(bool disposing) { ... }  
}  
```  
  
 <span data-ttu-id="dda1a-159">**X DO NOT** 모든 오버 로드의 선언 된 `Dispose` 이외의 다른 방법 `Dispose()` 및 `Dispose(bool)`합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-159">**X DO NOT** declare any overloads of the `Dispose` method other than `Dispose()` and `Dispose(bool)`.</span></span>  
  
 <span data-ttu-id="dda1a-160">`Dispose` 이 패턴을 체계화 하 고 구현자, 사용자 및 컴파일러는 혼동을 방지 하기 위해 예약 된 단어를 고려 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-160">`Dispose` should be considered a reserved word to help codify this pattern and prevent confusion among implementers, users, and compilers.</span></span> <span data-ttu-id="dda1a-161">일부 언어 특정 형식에이 패턴을 구현 자동으로 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-161">Some languages might choose to automatically implement this pattern on certain types.</span></span>  
  
 <span data-ttu-id="dda1a-162">**✓ DO** 허용 된 `Dispose(bool)` 메서드를 두 번 이상 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-162">**✓ DO** allow the `Dispose(bool)` method to be called more than once.</span></span> <span data-ttu-id="dda1a-163">메서드는 첫 번째 호출 후 아무 작업도 하지 않도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-163">The method might choose to do nothing after the first call.</span></span>  
  
```csharp
public class DisposableResourceHolder : IDisposable {  
  
    bool disposed = false;  
  
    protected virtual void Dispose(bool disposing) {  
        if (disposed) return;  
        // cleanup  
        ...  
        disposed = true;  
    }  
}  
```  
  
 <span data-ttu-id="dda1a-164">**X AVOID** 내에서 예외를 throw `Dispose(bool)` 포함 하는 프로세스 손상 되어 중요 한 상황에 따라 제외 하 고 (누수, 일치 하지 않는 공유 상태 등.).</span><span class="sxs-lookup"><span data-stu-id="dda1a-164">**X AVOID** throwing an exception from within `Dispose(bool)` except under critical situations where the containing process has been corrupted (leaks, inconsistent shared state, etc.).</span></span>  
  
 <span data-ttu-id="dda1a-165">사용자가 기대 하는 호출 `Dispose` 예외가 발생 하지 것입니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-165">Users expect that a call to `Dispose` will not raise an exception.</span></span>  
  
 <span data-ttu-id="dda1a-166">경우 `Dispose` 예외를 발생 시킬 수 있습니다, finally 블록 정리 논리를 더 이상 실행 되지 것입니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-166">If `Dispose` could raise an exception, further finally-block cleanup logic will not execute.</span></span> <span data-ttu-id="dda1a-167">이 해결 하려면 사용자에 대 한 모든 호출을 래핑할 해야 `Dispose` (내는 finally 블록!) try 블록에는 잠재 고객을 매우 복잡 한 정리 처리기입니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-167">To work around this, the user would need to wrap every call to `Dispose` (within the finally block!) in a try block, which leads to very complex cleanup handlers.</span></span> <span data-ttu-id="dda1a-168">실행 하는 경우는 `Dispose(bool disposing)` 메서드를 삭제 하는 것이 false 예외가 throw 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-168">If executing a `Dispose(bool disposing)` method, never throw an exception if disposing is false.</span></span> <span data-ttu-id="dda1a-169">이렇게 종료자 컨텍스트 내에서 실행 하는 경우 프로세스가 종료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-169">Doing so will terminate the process if executing inside a finalizer context.</span></span>  
  
 <span data-ttu-id="dda1a-170">**✓ DO** throw 한 <xref:System.ObjectDisposedException> 개체의 삭제 된 후에 사용할 수 없는 멤버에서.</span><span class="sxs-lookup"><span data-stu-id="dda1a-170">**✓ DO** throw an <xref:System.ObjectDisposedException> from any member that cannot be used after the object has been disposed of.</span></span>  
  
```csharp
public class DisposableResourceHolder : IDisposable {  
    bool disposed = false;  
    SafeHandle resource; // handle to a resource  
  
    public void DoSomething() {  
        if (disposed) throw new ObjectDisposedException(...);  
        // now call some native methods using the resource   
        ...  
    }  
    protected virtual void Dispose(bool disposing) {  
        if (disposed) return;  
        // cleanup  
        ...  
        disposed = true;  
    }  
}  
```  
  
 <span data-ttu-id="dda1a-171">**✓ CONSIDER** 메서드를 제공 하 `Close()`, 외에 `Dispose()`, 영역에서 표준 용어 닫기 인지 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-171">**✓ CONSIDER** providing method `Close()`, in addition to the `Dispose()`, if close is standard terminology in the area.</span></span>  
  
 <span data-ttu-id="dda1a-172">귀하에 게 중요 한 것이 작업을 수행 하는 경우는 `Close` 구현은 동일 `Dispose` 구현를 `IDisposable.Dispose` 메서드 명시적으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-172">When doing so, it is important that you make the `Close` implementation identical to `Dispose` and consider implementing the `IDisposable.Dispose` method explicitly.</span></span>  
  
```csharp
public class Stream : IDisposable {  
    IDisposable.Dispose() {  
        Close();  
    }  
    public void Close() {  
        Dispose(true);  
        GC.SuppressFinalize(this);  
    }  
}  
```  
  
<a name="finalizable_types"></a>   
## <a name="finalizable-types"></a><span data-ttu-id="dda1a-173">종료할 형식</span><span class="sxs-lookup"><span data-stu-id="dda1a-173">Finalizable Types</span></span>  
 <span data-ttu-id="dda1a-174">종료 가능한 형식은 종료자를 재정의 하 고 종료 코드 경로 제공 하 여 기본 Dispose 패턴을 확장 하는 형식은 `Dispose(bool)` 메서드.</span><span class="sxs-lookup"><span data-stu-id="dda1a-174">Finalizable types are types that extend the Basic Dispose Pattern by overriding the finalizer and providing finalization code path in the `Dispose(bool)` method.</span></span>  
  
 <span data-ttu-id="dda1a-175">종료자는 주로 없기 때문에 시스템의 상태에 대 한 특정 (일반적으로 유효) 가정을 프로그램 실행 중에 올바르게 구현 하기가 매우 어렵습니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-175">Finalizers are notoriously difficult to implement correctly, primarily because you cannot make certain (normally valid) assumptions about the state of the system during their execution.</span></span> <span data-ttu-id="dda1a-176">다음 지침 신중 하 게 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-176">The following guidelines should be taken into careful consideration.</span></span>  
  
 <span data-ttu-id="dda1a-177">일부의 지침에만 적용는 `Finalize` 메서드를 코드에 있지만 종료자에서 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-177">Note that some of the guidelines apply not just to the `Finalize` method, but to any code called from a finalizer.</span></span> <span data-ttu-id="dda1a-178">기본 Dispose 패턴 이전에 정의 된 경우 즉, 내에서 실행 하는 논리 `Dispose(bool disposing)` 경우는 `disposing` 매개 변수가 false 인 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-178">In the case of the Basic Dispose Pattern previously defined, this means logic that executes inside `Dispose(bool disposing)` when the `disposing` parameter is false.</span></span>  
  
 <span data-ttu-id="dda1a-179">재정의 하지 않아야 함 기본 클래스 이미 종료을 기본 Dispose 패턴을 구현 하는 경우 `Finalize` 다시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-179">If the base class already is finalizable and implements the Basic Dispose Pattern, you should not override `Finalize` again.</span></span> <span data-ttu-id="dda1a-180">재정의 해야 하는 대신 방금는 `Dispose(bool)` 추가 리소스 정리 논리를 제공 하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-180">You should instead just override the `Dispose(bool)` method to provide additional resource cleanup logic.</span></span>  
  
 <span data-ttu-id="dda1a-181">다음 코드를 종료 가능 형식의 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-181">The following code shows an example of a finalizable type:</span></span>  
  
```csharp
public class ComplexResourceHolder : IDisposable {  
  
    private IntPtr buffer; // unmanaged memory buffer  
    private SafeHandle resource; // disposable handle to a resource  
  
    public ComplexResourceHolder() {  
        this.buffer = ... // allocates memory  
        this.resource = ... // allocates the resource  
    }  
  
    protected virtual void Dispose(bool disposing) {  
            ReleaseBuffer(buffer); // release unmanaged memory  
        if (disposing) { // release other disposable objects  
            if (resource!= null) resource.Dispose();  
        }  
    }  
  
    ~ComplexResourceHolder() {
        Dispose(false);  
    }  
  
    public void Dispose() {
        Dispose(true);  
        GC.SuppressFinalize(this);  
    }  
}  
```  
  
 <span data-ttu-id="dda1a-182">**X AVOID** 유형을 종료 가능 만드는 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-182">**X AVOID** making types finalizable.</span></span>  
  
 <span data-ttu-id="dda1a-183">종료 자가 필요 생각에 모든 사례를 신중 하 게 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-183">Carefully consider any case in which you think a finalizer is needed.</span></span> <span data-ttu-id="dda1a-184">실제에는 성능 및 코드에 해당 하는 복잡성의 관점에서 종료자를 사용 하 여 인스턴스를 사용 하 여 관련 된 비용이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-184">There is a real cost associated with instances with finalizers, from both a performance and code complexity standpoint.</span></span> <span data-ttu-id="dda1a-185">와 같은 리소스 래퍼를 사용 하는 것을 선호 <xref:System.Runtime.InteropServices.SafeHandle> 를 가능한 경우 관리 되지 않는 리소스를 캡슐화 하는 경우에 종료자 불필요 하 게 됩니다 래퍼 자체 리소스 정리 담당 하기 때문에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-185">Prefer using resource wrappers such as <xref:System.Runtime.InteropServices.SafeHandle> to encapsulate unmanaged resources where possible, in which case a finalizer becomes unnecessary because the wrapper is responsible for its own resource cleanup.</span></span>  
  
 <span data-ttu-id="dda1a-186">**X DO NOT** 값 형식을 개체로 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-186">**X DO NOT** make value types finalizable.</span></span>  
  
 <span data-ttu-id="dda1a-187">실제로 참조 형식에만 CLR에서 종료 가져오기 하 고 값 형식에 종료자를 배치 하려고 하므로 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-187">Only reference types actually get finalized by the CLR, and thus any attempt to place a finalizer on a value type will be ignored.</span></span> <span data-ttu-id="dda1a-188">C# 및 c + + 컴파일러는이 규칙을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-188">The C# and C++ compilers enforce this rule.</span></span>  
  
 <span data-ttu-id="dda1a-189">**✓ DO** 형식이 자체 종료 자가 없는 관리 되지 않는 리소스를 해제 하는 일을 담당 하는 경우 종료 가능 형식을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-189">**✓ DO** make a type finalizable if the type is responsible for releasing an unmanaged resource that does not have its own finalizer.</span></span>  
  
 <span data-ttu-id="dda1a-190">종료자를 구현 하는 경우 호출 하기만 하면 됩니다 `Dispose(false)` 내에서 모든 리소스 정리 논리를 배치 합니다 `Dispose(bool disposing)` 메서드.</span><span class="sxs-lookup"><span data-stu-id="dda1a-190">When implementing the finalizer, simply call `Dispose(false)` and place all resource cleanup logic inside the `Dispose(bool disposing)` method.</span></span>  
  
```csharp
public class ComplexResourceHolder : IDisposable {  
  
    ~ComplexResourceHolder() {
        Dispose(false);  
    }  
  
    protected virtual void Dispose(bool disposing) {
        ...  
    }  
}  
```  
  
 <span data-ttu-id="dda1a-191">**✓ DO** 줄어드는 경우 모든 형식에 대해 기본 Dispose 패턴을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-191">**✓ DO** implement the Basic Dispose Pattern on every finalizable type.</span></span>  
  
 <span data-ttu-id="dda1a-192">이렇게 하면 형식의 사용자 명시적으로 종료자 담당 같은 리소스의 명확한 정리 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-192">This gives users of the type a means to explicitly perform deterministic cleanup of those same resources for which the finalizer is responsible.</span></span>  
  
 <span data-ttu-id="dda1a-193">**X DO NOT** 는 것은 이미 종료 되었을 상당한 위험 있기 때문에 종료 자가 코드 경로에 추가 된 줄어드는 경우 개체에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-193">**X DO NOT** access any finalizable objects in the finalizer code path, because there is significant risk that they will have already been finalized.</span></span>  
  
 <span data-ttu-id="dda1a-194">예를 들어, 다른 종료 가능한 개체 B에 대 한 참조가 있는 종료 가능한 개체는 사용할 수 없습니다 안정적으로 B에서 A의 종료자 또는 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-194">For example, a finalizable object A that has a reference to another finalizable object B cannot reliably use B in A’s finalizer, or vice versa.</span></span> <span data-ttu-id="dda1a-195">종료자는 중요 한 종료에 대 한 약한 순서 보장) (짧은 임의의 순서로 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-195">Finalizers are called in a random order (short of a weak ordering guarantee for critical finalization).</span></span>  
  
 <span data-ttu-id="dda1a-196">또한 정적 변수에 저장 된 개체 또는 프로세스를 종료 하는 응용 프로그램 도메인 언로드로 동안 특정 지점에서 수집 가져오기는 주의 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-196">Also, be aware that objects stored in static variables will get collected at certain points during an application domain unload or while exiting the process.</span></span> <span data-ttu-id="dda1a-197">종료 가능한 개체 (또는 정적 변수에 저장 된 값을 사용할 수 있는 정적 메서드를 호출)를 가리키는 정적 변수 아닐 액세스 안전한 경우 <xref:System.Environment.HasShutdownStarted%2A?displayProperty=nameWithType> true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-197">Accessing a static variable that refers to a finalizable object (or calling a static method that might use values stored in static variables) might not be safe if <xref:System.Environment.HasShutdownStarted%2A?displayProperty=nameWithType> returns true.</span></span>  
  
 <span data-ttu-id="dda1a-198">**✓ DO** 확인 프로그램 `Finalize` 보호 된 메서드에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-198">**✓ DO** make your `Finalize` method protected.</span></span>  
  
 <span data-ttu-id="dda1a-199">C#, c + + 및 VB.NET 개발자 필요가 없습니다이 대 한 걱정이 지침을 적용 하는 데 도움이 컴파일러 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-199">C#, C++, and VB.NET developers do not need to worry about this, because the compilers help to enforce this guideline.</span></span>  
  
 <span data-ttu-id="dda1a-200">**X DO NOT** 종료자 논리 시스템에 중요 한 오류를 제외 하 고 답변된 예외 이스케이프 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-200">**X DO NOT** let exceptions escape from the finalizer logic, except for system-critical failures.</span></span>  
  
 <span data-ttu-id="dda1a-201">CLR (.NET Framework 버전 2.0)을 기준으로 전체 프로세스가 종료 됩니다 종료자에서 예외가 throw 되 면 실행 및 제어 된 방식으로 해제 되는 리소스에서 다른 종료자를 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-201">If an exception is thrown from a finalizer, the CLR will shut down the entire process (as of .NET Framework version 2.0), preventing other finalizers from executing and resources from being released in a controlled manner.</span></span>  
  
 <span data-ttu-id="dda1a-202">**✓ CONSIDER** 만들고 중요 한 종료 가능 개체를 사용 하 여 (포함 된 형식 계층 구조와 형식을 <xref:System.Runtime.ConstrainedExecution.CriticalFinalizerObject>)는 종료자 절대적으로 실행 해야 경우에 강제 응용 프로그램 도메인 언로드 및 스레드 상황에 대 한 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="dda1a-202">**✓ CONSIDER** creating and using a critical finalizable object (a type with a type hierarchy that contains <xref:System.Runtime.ConstrainedExecution.CriticalFinalizerObject>) for situations in which a finalizer absolutely must execute even in the face of forced application domain unloads and thread aborts.</span></span>  
  
 <span data-ttu-id="dda1a-203">*Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*</span><span class="sxs-lookup"><span data-stu-id="dda1a-203">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="dda1a-204">*Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span><span class="sxs-lookup"><span data-stu-id="dda1a-204">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dda1a-205">참고자료</span><span class="sxs-lookup"><span data-stu-id="dda1a-205">See also</span></span>

- <xref:System.IDisposable.Dispose%2A?displayProperty=nameWithType>  
- <xref:System.Object.Finalize%2A?displayProperty=nameWithType>  
- [<span data-ttu-id="dda1a-206">프레임워크 디자인 지침</span><span class="sxs-lookup"><span data-stu-id="dda1a-206">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="dda1a-207">일반 디자인 패턴</span><span class="sxs-lookup"><span data-stu-id="dda1a-207">Common Design Patterns</span></span>](../../../docs/standard/design-guidelines/common-design-patterns.md)  
- [<span data-ttu-id="dda1a-208">가비지 수집</span><span class="sxs-lookup"><span data-stu-id="dda1a-208">Garbage Collection</span></span>](../../../docs/standard/garbage-collection/index.md)
