---
title: 주요 변경 내용 및.NET 라이브러리
description: .NET 라이브러리를 만들 때의 주요 변경 내용 탐색 하기 위한 권장 사항을 사용 하는 것이 좋습니다.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 83c01fdad7d836877bf692b87eeb0230219ded36
ms.sourcegitcommit: fd8d4587cc26e53f0e27e230d6e27d828ef4306b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2018
ms.locfileid: "49370342"
---
# <a name="breaking-changes"></a><span data-ttu-id="46cc3-103">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="46cc3-103">Breaking changes</span></span>

<span data-ttu-id="46cc3-104">기존 사용자에 대 한 안정성과 향후 혁신 간의 균형을 유지 하는.NET 라이브러리에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-104">It's important for a .NET library to find a balance between stability for existing users and innovation for the future.</span></span> <span data-ttu-id="46cc3-105">라이브러리 작성자가 리팩터링 및 코드를 완벽 한 것 하위 수준 라이브러리에 대 한 특히 저하에 기존 사용자가 중단 될 때까지 재고에 대해 배웁니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-105">Library authors lean towards refactoring and rethinking code until it's perfect, but breaking your existing users has a negative impact, especially for low-level libraries.</span></span>

## <a name="project-types-and-breaking-changes"></a><span data-ttu-id="46cc3-106">프로젝트 형식 및 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="46cc3-106">Project types and breaking changes</span></span>

<span data-ttu-id="46cc3-107">.NET 커뮤니티에서 라이브러리 사용 방법의 주요 변경 내용 최종 사용자가 개발자에 게 미치는 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-107">How a library is used by the .NET community changes the effect of breaking changes on end-user developers.</span></span>

* <span data-ttu-id="46cc3-108">**낮음 및 중간 수준 라이브러리** serializer, HTML 파서, 데이터베이스 개체 관계형 매퍼 또는 웹 프레임 워크와 같은 가장 영향을 받는 주요 변경 내용으로 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-108">**Low and middle-level libraries** like a serializer, HTML parser, database object-relational mapper, or web framework are the most affected by breaking changes.</span></span>

  <span data-ttu-id="46cc3-109">구성 요소 패키지에는 NuGet 종속성으로 최종 사용자 응용 프로그램을 빌드하는 개발자 및 다른 라이브러리에서 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-109">Building block packages are used by end-user developers to build applications, and by other libraries as NuGet dependencies.</span></span> <span data-ttu-id="46cc3-110">예를 들어, 응용 프로그램을 빌드하는 하 고 오픈 소스 클라이언트를 사용 하 여 웹 서비스를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-110">For example, you're building an application and are using an open-source client to call a web service.</span></span> <span data-ttu-id="46cc3-111">주요 업데이트를 클라이언트에 사용 하 여 종속성은 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-111">A breaking update to a dependency the client uses isn't something you can fix.</span></span> <span data-ttu-id="46cc3-112">변경 해야 하는 오픈 소스 클라이언트 이므로 없습니다 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-112">It's the open-source client that needs to be changed and you have no control over it.</span></span> <span data-ttu-id="46cc3-113">라이브러리의 호환 버전을 찾고 클라이언트 라이브러리에 대 한 수정은 제출 또는 새 버전에 대 한 대기 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-113">You have to find compatible versions of the libraries or submit a fix to the client library and wait for a new version.</span></span> <span data-ttu-id="46cc3-114">최악의 상황은 서로 호환 되지 않는 버전의 세 번째 라이브러리에 종속 된 두 개의 라이브러리를 사용 하려는 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-114">The worst-case situation is if you want to use two libraries that depend on mutually incompatible versions of a third library.</span></span>

* <span data-ttu-id="46cc3-115">**고급 라이브러리** UI의 도구 모음과 같은 컨트롤은 주요 변경 내용에 덜 민감합니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-115">**High-level libraries** like a suite of UI controls are less sensitive to breaking changes.</span></span>

  <span data-ttu-id="46cc3-116">고급 라이브러리는 최종 사용자 응용 프로그램에서 직접 참조 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-116">High-level libraries are directly referenced in an end-user application.</span></span> <span data-ttu-id="46cc3-117">주요 변경 될 경우, 개발자를 최신 버전으로 업데이트 하도록 선택할 수 또는 주요 변경에 맞게 응용 프로그램을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-117">If breaking changes occur, the developer can choose to update to the latest version, or can modify their application to work with the breaking change.</span></span>

<span data-ttu-id="46cc3-118">**✔️ 수행** 라이브러리 사용 방법에 대해 생각해 보세요.</span><span class="sxs-lookup"><span data-stu-id="46cc3-118">**✔️ DO** think about how your library will be used.</span></span> <span data-ttu-id="46cc3-119">미치는 주요 변경 내용 해야 응용 프로그램 및 사용 하는 라이브러리에서?</span><span class="sxs-lookup"><span data-stu-id="46cc3-119">What effect will breaking changes have on applications and libraries that use it?</span></span>

<span data-ttu-id="46cc3-120">**✔️ 수행** 하위 수준.NET 라이브러리를 개발 하는 경우 주요 변경 내용을 최소화 합니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-120">**✔️ DO** minimize breaking changes when developing a low-level .NET library.</span></span>

<span data-ttu-id="46cc3-121">**✔️ 하십시오** 새 NuGet 패키지로 라이브러리의 주 버전을 게시를 다시 작성 합니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-121">**✔️ CONSIDER** publishing a major rewrite of a library as a new NuGet package.</span></span>

## <a name="types-of-breaking-changes"></a><span data-ttu-id="46cc3-122">형식의 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="46cc3-122">Types of breaking changes</span></span>

<span data-ttu-id="46cc3-123">서로 다른 범주로 동일 하 게 영향력이 강한 되지 않으며는 주요 변경 내용.</span><span class="sxs-lookup"><span data-stu-id="46cc3-123">Breaking changes fall into different categories and aren't equally impactful.</span></span>

### <a name="source-breaking-change"></a><span data-ttu-id="46cc3-124">원본 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="46cc3-124">Source breaking change</span></span>

<span data-ttu-id="46cc3-125">주요 변경 내용 원본 프로그램 실행에 영향을 주지 않습니다 하지만 하면 컴파일 오류가 발생 다음에 응용 프로그램이 다시 컴파일됩니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-125">A source breaking change doesn't affect program execution but will cause compilation errors the next time the application is recompiled.</span></span> <span data-ttu-id="46cc3-126">예를 들어, 새 오버 로드 모호성을 이전에 모호한 되지 않는 메서드 호출에서 만들거나 이름이 바뀐된 매개 변수 명명 된 매개 변수를 사용 하는 호출자의 연결이 끊어집니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-126">For example, a new overload can create an ambiguity in method calls that were unambiguous previously, or a renamed parameter will break callers that use named parameters.</span></span>

```csharp
public class Task
{
    // Adding a type called Task could conflict with System.Threading.Tasks.Task at compilation
}
```

<span data-ttu-id="46cc3-127">개발자가 응용 프로그램을 다시 컴파일해야 하는 경우에 주요 변경 내용 소스는 해로운, 이므로 가장 방해가 적은 주요 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-127">Because a source breaking change is only harmful when developers recompile their applications, it's the least disruptive breaking change.</span></span> <span data-ttu-id="46cc3-128">개발자는 자신의 손상 된 소스 코드를 쉽게 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-128">Developers can fix their own broken source code easily.</span></span>

### <a name="behavior-breaking-change"></a><span data-ttu-id="46cc3-129">주요 변경 내용 동작</span><span class="sxs-lookup"><span data-stu-id="46cc3-129">Behavior breaking change</span></span>

<span data-ttu-id="46cc3-130">동작 변경 내용은 가장 일반적인 유형의 주요 변경 내용: 동작 변경이 거의 모든 사용자가 손상 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-130">Behavior changes are the most common type of breaking change: almost any change in behavior could break someone.</span></span> <span data-ttu-id="46cc3-131">라이브러리를 변경 합니다, 메서드 서명, 예: 예외 발생, 입력 또는 출력 데이터 형식을 모두 부정적인 영향을 줄 수 라이브러리 소비자입니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-131">Changes to your library, such as method signatures, exceptions thrown or input or output data formats, could all negatively impact your library consumers.</span></span> <span data-ttu-id="46cc3-132">사용자가 이전에 손상 된 동작에 의존 하는 경우 버그 수정도 주요 변경 내용으로 한정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-132">Even a bug fix can qualify as a breaking change if users relied on the previously broken behavior.</span></span>

<span data-ttu-id="46cc3-133">기능을 추가 하 고 잘못 된 동작을 개선 한 것 이지만 주의 하지 않고 수 있도록이 업그레이드를 기존 사용자에 대 한 매우 어렵습니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-133">Adding features and improving bad behaviors is a good thing, but without care it can make it very hard for existing users to upgrade.</span></span> <span data-ttu-id="46cc3-134">동작의 주요 변경 내용으로 처리 하는 개발자가 노력 하 고 한 가지 방법은 설정을 뒤 숨기려면 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-134">One approach to helping developers deal with behavior breaking changes is to hide them behind settings.</span></span> <span data-ttu-id="46cc3-135">개발자를에서 동시 옵트인 하거나 주요 변경 내용 옵트아웃 하도록 선택 하는 동안 라이브러리의 최신 버전으로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-135">Settings let developers update to the latest version of your library while at the same time choosing to opt in or opt out of breaking changes.</span></span> <span data-ttu-id="46cc3-136">이 전략에는 개발자를 사용 중인 코드 시간이 지남에 따라 조정 하는 동안 최신 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-136">This strategy lets developers stay up to date while letting their consuming code adapt over time.</span></span>

<span data-ttu-id="46cc3-137">예를 들어, ASP.NET Core MVC는 개념을 [호환성 버전](/aspnet/core/mvc/compatibility-version) 수정 기능 활성화 및 비활성화 하는 `MvcOptions`합니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-137">For example, ASP.NET Core MVC has the concept of a [compatibility version](/aspnet/core/mvc/compatibility-version) that modifies the features enabled and disabled on `MvcOptions`.</span></span>

<span data-ttu-id="46cc3-138">**✔️ 하십시오** 기존 사용자에 게 적용 되며 사용 하면 개발자가 설정 된 기능에 옵트인 하는 경우 새로운 기능을 기본적으로 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-138">**✔️ CONSIDER** leaving new features off by default, if they affect existing users, and let developers opt in to the feature with a setting.</span></span>

### <a name="binary-breaking-change"></a><span data-ttu-id="46cc3-139">이진 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="46cc3-139">Binary breaking change</span></span>

<span data-ttu-id="46cc3-140">라이브러리의 공용 API를 변경할 때 발생 하는 주요 변경 내용 이진 파일, 라이브러리의 이전 버전은 더 이상 API를 호출할 수 있도록에 대해 컴파일된 어셈블리입니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-140">A binary breaking change happens when you change the public API of your library, so assemblies compiled against older versions of your library are no longer able to call the API.</span></span> <span data-ttu-id="46cc3-141">예를 들어, 새 매개 변수를 추가 하 여 메서드의 시그니처를 변경 하면 throw 라이브러리의 이전 버전에 대해 컴파일된 어셈블리는 <xref:System.MissingMethodException>합니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-141">For example, changing a method's signature by adding a new parameter will cause assemblies compiled against the older version of the library to throw a <xref:System.MissingMethodException>.</span></span>

<span data-ttu-id="46cc3-142">주요 변경 내용 이진 파일에서 페이지 나누기 수는 **전체 어셈블리**합니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-142">A binary breaking change can also break an **entire assembly**.</span></span> <span data-ttu-id="46cc3-143">사용 하 여 어셈블리 이름 바꾸기 `AssemblyName` 추가, 제거 또는 변경 된 어셈블리의 강력한 이름 지정 키로 어셈블리의 id를 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-143">Renaming an assembly with `AssemblyName` will change the assembly's identity, as will adding, removing, or changing the assembly's strong naming key.</span></span> <span data-ttu-id="46cc3-144">어셈블리 id의 변경을 사용 하는 모든 컴파일된 코드가 중단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-144">A change of an assembly's identity will break all compiled code that uses it.</span></span>

<span data-ttu-id="46cc3-145">**❌ 하지** 어셈블리 이름을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-145">**❌ DO NOT** change an assembly name.</span></span>

<span data-ttu-id="46cc3-146">**❌ 하지** 추가, 제거 또는 강력한 이름 키를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-146">**❌ DO NOT** add, remove, or change the strong naming key.</span></span>

<span data-ttu-id="46cc3-147">**✔️ 하십시오** 인터페이스 대신 추상 기본 클래스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-147">**✔️ CONSIDER** using abstract base classes instead of interfaces.</span></span>

> <span data-ttu-id="46cc3-148">인터페이스에 아무것도 추가 하면 실패를 구현 하는 기존 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-148">Adding anything to an interface will cause existing types that implement it to fail.</span></span> <span data-ttu-id="46cc3-149">추상 기본 클래스를 사용 하면 기본 가상 구현을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-149">An abstract base class allows you to add a default virtual implementation.</span></span>

<span data-ttu-id="46cc3-150">**✔️ 것이 좋습니다** 배치는 <xref:System.ObsoleteAttribute> 형식 및 멤버를 제거 하려는에서 합니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-150">**✔️ CONSIDER** placing the <xref:System.ObsoleteAttribute> on types and members that you intend to remove.</span></span> <span data-ttu-id="46cc3-151">코드를 업데이트 합니다. 더 이상 사용 되지 않는 API를 사용 하기 위한 지침은 가져야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-151">The attribute should have instructions for updating code to no longer use the obsolete API.</span></span>

> <span data-ttu-id="46cc3-152">형식과 메서드를 호출 하는 코드는 <xref:System.ObsoleteAttribute> 특성에 제공 된 메시지와 함께 빌드 경고를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-152">Code that calls types and methods with the <xref:System.ObsoleteAttribute> will generate a build warning with the message supplied to the attribute.</span></span> <span data-ttu-id="46cc3-153">사용 되지 않는 API 노출 시간을 사용 하 여 대부분의 더 이상 사용 되지 않는 API가 제거 되 면 있도록 마이그레이션할 경고 제공 사람들 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="46cc3-153">The warnings give people who use the obsolete API surface time to migrate so that when the obsolete API is removed, most are no longer using it.</span></span>

```csharp
public class Document
{
    [Obsolete("LoadDocument(string) is obsolete. Use LoadDocument(Uri) instead.")]
    public static Document LoadDocument(string uri)
    {
        return LoadDocument(new Uri(uri));
    }

    public static Document LoadDocument(Uri uri)
    {
        // Load the document
    }
}
```

## <a name="see-also"></a><span data-ttu-id="46cc3-154">참고자료</span><span class="sxs-lookup"><span data-stu-id="46cc3-154">See also</span></span>

* [<span data-ttu-id="46cc3-155">C# 개발자를 위한 버전 및 업데이트 고려 사항</span><span class="sxs-lookup"><span data-stu-id="46cc3-155">Version and update considerations for C# developers</span></span>](../../csharp/whats-new/version-update-considerations.md)
* [<span data-ttu-id="46cc3-156">.NET에서 API-주요 변경 내용에 대 한 명확한 지침</span><span class="sxs-lookup"><span data-stu-id="46cc3-156">A definitive guide to API-breaking changes in .NET</span></span>](https://stackoverflow.com/questions/1456785/a-definitive-guide-to-api-breaking-changes-in-net)
* [<span data-ttu-id="46cc3-157">CoreFX 주요 변경 규칙</span><span class="sxs-lookup"><span data-stu-id="46cc3-157">CoreFX Breaking Change Rules</span></span>](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/breaking-change-rules.md)

>[!div class="step-by-step"]
[<span data-ttu-id="46cc3-158">이전</span><span class="sxs-lookup"><span data-stu-id="46cc3-158">Previous</span></span>](./versioning.md)
