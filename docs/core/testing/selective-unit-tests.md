---
title: 선택적 단위 테스트 실행
description: 필터 식을 사용하여 dotnet 명령으로 선택적 단위 테스트를 실행하는 방법을 보여 줍니다.
author: smadala
ms.author: mairaw
ms.date: 03/22/2017
ms.openlocfilehash: 428e31014f5d8d487deb7c4b4317ebcef13c294d
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42935182"
---
# <a name="running-selective-unit-tests"></a><span data-ttu-id="83584-103">선택적 단위 테스트 실행</span><span class="sxs-lookup"><span data-stu-id="83584-103">Running selective unit tests</span></span>

<span data-ttu-id="83584-104">다음 예제에서는 `dotnet test`를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-104">The following examples use `dotnet test`.</span></span> <span data-ttu-id="83584-105">`vstest.console.exe`를 사용하는 경우 `--filter `를 `--testcasefilter:`로 바꾸세요.</span><span class="sxs-lookup"><span data-stu-id="83584-105">If you're using `vstest.console.exe`, replace `--filter ` with `--testcasefilter:`.</span></span>

## <a name="mstest"></a><span data-ttu-id="83584-106">MSTest</span><span class="sxs-lookup"><span data-stu-id="83584-106">MSTest</span></span>

```csharp
using Microsoft.VisualStudio.TestTools.UnitTesting;

namespace MSTestNamespace
{
    [TestClass]
    public class UnitTest1
    {
        [TestCategory("CategoryA")]
        [Priority(1)]
        [TestMethod]
        public void TestMethod1()
        {
        }

        [Priority(2)]
        [TestMethod]
        public void TestMethod2()
        {
        }
    }
}
```

| <span data-ttu-id="83584-107">식</span><span class="sxs-lookup"><span data-stu-id="83584-107">Expression</span></span> | <span data-ttu-id="83584-108">결과</span><span class="sxs-lookup"><span data-stu-id="83584-108">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter Method` | <span data-ttu-id="83584-109">`FullyQualifiedName`에 `Method`가 포함된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-109">Runs tests whose `FullyQualifiedName` contains `Method`.</span></span> <span data-ttu-id="83584-110">`vstest 15.1+`에서 사용 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-110">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Name~TestMethod1` | <span data-ttu-id="83584-111">이름에 `TestMethod1`이 포함된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-111">Runs tests whose name contains `TestMethod1`.</span></span> |
| `dotnet test --filter ClassName=MSTestNamespace.UnitTest1` | <span data-ttu-id="83584-112">클래스 `MSTestNamespace.UnitTest1`에 속하는 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-112">Runs tests which are in class `MSTestNamespace.UnitTest1`.</span></span><br><span data-ttu-id="83584-113">**참고:** `ClassName` 값에는 네임스페이스가 있어야 하므로, `ClassName=UnitTest1`이 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83584-113">**Note:** The `ClassName` value should have a namespace, so `ClassName=UnitTest1` won't work.</span></span> |
| `dotnet test --filter FullyQualifiedName!=MSTestNamespace.UnitTest1.TestMethod1` | <span data-ttu-id="83584-114">`MSTestNamespace.UnitTest1.TestMethod1`을 제외한 모든 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-114">Runs all tests except `MSTestNamespace.UnitTest1.TestMethod1`.</span></span> |
| `dotnet test --filter TestCategory=CategoryA` | <span data-ttu-id="83584-115">`[TestCategory("CategoryA")]`로 주석이 추가된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-115">Runs tests which are annotated with `[TestCategory("CategoryA")]`.</span></span> |
| `dotnet test --filter Priority=2` | <span data-ttu-id="83584-116">`[Priority(2)]`로 주석이 추가된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-116">Runs tests which are annotated with `[Priority(2)]`.</span></span><br>

<span data-ttu-id="83584-117">**조건 연산자 | 및 &amp; 사용**</span><span class="sxs-lookup"><span data-stu-id="83584-117">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="83584-118">식</span><span class="sxs-lookup"><span data-stu-id="83584-118">Expression</span></span> | <span data-ttu-id="83584-119">결과</span><span class="sxs-lookup"><span data-stu-id="83584-119">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~UnitTest1&#124;TestCategory=CategoryA"</code> | <span data-ttu-id="83584-120">`FullyQualifiedName`에 `UnitTest1`이 **있거나** `TestCategory`가 `CategoryA`인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-120">Runs tests which have `UnitTest1` in `FullyQualifiedName` **or** `TestCategory` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~UnitTest1&TestCategory=CategoryA"` | <span data-ttu-id="83584-121">`FullyQualifiedName`에 `UnitTest1`**이 있고** `TestCategory`가 `CategoryA`인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-121">Runs tests which have `UnitTest1` in `FullyQualifiedName` **and** `TestCategory` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~UnitTest1&TestCategory=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="83584-122">`UnitTest1`을 포함하는 `FullyQualifiedName`**이 있고**`TestCategory`가 `CategoryA`**이거나** `Priority`가 1인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-122">Runs tests which have either `FullyQualifiedName` containing `UnitTest1` **and** `TestCategory` is `CategoryA` **or** `Priority` is 1.</span></span> |

## <a name="xunit"></a><span data-ttu-id="83584-123">xUnit</span><span class="sxs-lookup"><span data-stu-id="83584-123">xUnit</span></span>

```csharp
using Xunit;

namespace XUnitNamespace
{
    public class TestClass1
    {
        [Trait("Category", "CategoryA")]
        [Trait("Priority", "1")]
        [Fact]
        public void Test1()
        {
        }

        [Trait("Priority", "2")]
        [Fact]
        public void Test2()
        {
        }
    }
}
```

| <span data-ttu-id="83584-124">식</span><span class="sxs-lookup"><span data-stu-id="83584-124">Expression</span></span> | <span data-ttu-id="83584-125">결과</span><span class="sxs-lookup"><span data-stu-id="83584-125">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter DisplayName=XUnitNamespace.TestClass1.Test1` | <span data-ttu-id="83584-126">`XUnitNamespace.TestClass1.Test1` 테스트를 하나만 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-126">Runs only one test, `XUnitNamespace.TestClass1.Test1`.</span></span> |
| `dotnet test --filter FullyQualifiedName!=XUnitNamespace.TestClass1.Test1` | <span data-ttu-id="83584-127">`XUnitNamespace.TestClass1.Test1`을 제외한 모든 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-127">Runs all tests except `XUnitNamespace.TestClass1.Test1`.</span></span> |
| `dotnet test --filter DisplayName~TestClass1` | <span data-ttu-id="83584-128">표시 이름에 `TestClass1`이 포함된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-128">Runs tests whose display name contains `TestClass1`.</span></span> |

<span data-ttu-id="83584-129">코드 예제에서 `Category` 및 `Priority` 키로 정의된 특성은 필터링에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83584-129">In the code example, the defined traits with keys `Category` and `Priority` can be used for filtering.</span></span>

| <span data-ttu-id="83584-130">식</span><span class="sxs-lookup"><span data-stu-id="83584-130">Expression</span></span> | <span data-ttu-id="83584-131">결과</span><span class="sxs-lookup"><span data-stu-id="83584-131">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter XUnit` | <span data-ttu-id="83584-132">`FullyQualifiedName`에 `XUnit`가 포함된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-132">Runs tests whose `FullyQualifiedName` contains `XUnit`.</span></span>  <span data-ttu-id="83584-133">`vstest 15.1+`에서 사용 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-133">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Category=CategoryA` | <span data-ttu-id="83584-134">`[Trait("Category", "CategoryA")]`가 있는 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-134">Runs tests which have `[Trait("Category", "CategoryA")]`.</span></span> |

<span data-ttu-id="83584-135">**조건 연산자 | 및 &amp; 사용**</span><span class="sxs-lookup"><span data-stu-id="83584-135">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="83584-136">식</span><span class="sxs-lookup"><span data-stu-id="83584-136">Expression</span></span> | <span data-ttu-id="83584-137">결과</span><span class="sxs-lookup"><span data-stu-id="83584-137">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~TestClass1&#124;Category=CategoryA"</code> | <span data-ttu-id="83584-138">`FullyQualifiedName`에 `TestClass1`이 **있거나**`Category`가 `CategoryA`인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-138">Runs tests which has `TestClass1` in `FullyQualifiedName` **or** `Category` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~TestClass1&Category=CategoryA"` | <span data-ttu-id="83584-139">`FullyQualifiedName`에 `TestClass1`**이 있고** `Category`가 `CategoryA`인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-139">Runs tests which has `TestClass1` in `FullyQualifiedName` **and** `Category` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~TestClass1&Category=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="83584-140">`TestClass1`을 포함하는 `FullyQualifiedName`**이** 있고 `Category`가 `CategoryA`**이거나** `Priority`가 1인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-140">Runs tests which have either `FullyQualifiedName` containing `TestClass1` **and** `Category` is `CategoryA` **or** `Priority` is 1.</span></span> |

## <a name="nunit"></a><span data-ttu-id="83584-141">NUnit</span><span class="sxs-lookup"><span data-stu-id="83584-141">NUnit</span></span>

```csharp
using NUnit.Framework;

namespace NUnitNamespace
{
    public class UnitTest1
    {
        [Category("CategoryA")]
        [Property("Priority", 1)]
        [Test]
        public void TestMethod1()
        {
        }

        [Property("Priority", 2)]
        [Test]
        public void TestMethod2()
        {
        }
    }
}
```

| <span data-ttu-id="83584-142">식</span><span class="sxs-lookup"><span data-stu-id="83584-142">Expression</span></span> | <span data-ttu-id="83584-143">결과</span><span class="sxs-lookup"><span data-stu-id="83584-143">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter Method` | <span data-ttu-id="83584-144">`FullyQualifiedName`에 `Method`가 포함된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-144">Runs tests whose `FullyQualifiedName` contains `Method`.</span></span> <span data-ttu-id="83584-145">`vstest 15.1+`에서 사용 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-145">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Name~TestMethod1` | <span data-ttu-id="83584-146">이름에 `TestMethod1`이 포함된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-146">Runs tests whose name contains `TestMethod1`.</span></span> |
| `dotnet test --filter FullyQualifiedName~NUnitNamespace.UnitTest1` | <span data-ttu-id="83584-147">클래스 `NUnitNamespace.UnitTest1`에 속하는 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-147">Runs tests which are in class `NUnitNamespace.UnitTest1`.</span></span><br>
| `dotnet test --filter FullyQualifiedName!=NUnitNamespace.UnitTest1.TestMethod1` | <span data-ttu-id="83584-148">`NUnitNamespace.UnitTest1.TestMethod1`을 제외한 모든 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-148">Runs all tests except `NUnitNamespace.UnitTest1.TestMethod1`.</span></span> |
| `dotnet test --filter TestCategory=CategoryA` | <span data-ttu-id="83584-149">`[Category("CategoryA")]`로 주석이 추가된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-149">Runs tests which are annotated with `[Category("CategoryA")]`.</span></span> |
| `dotnet test --filter Priority=2` | <span data-ttu-id="83584-150">`[Priority(2)]`로 주석이 추가된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-150">Runs tests which are annotated with `[Priority(2)]`.</span></span><br>

<span data-ttu-id="83584-151">**조건 연산자 | 및 &amp; 사용**</span><span class="sxs-lookup"><span data-stu-id="83584-151">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="83584-152">식</span><span class="sxs-lookup"><span data-stu-id="83584-152">Expression</span></span> | <span data-ttu-id="83584-153">결과</span><span class="sxs-lookup"><span data-stu-id="83584-153">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~UnitTest1&#124;TestCategory=CategoryA"</code> | <span data-ttu-id="83584-154">`FullyQualifiedName`에 `UnitTest1`이 **있거나** `TestCategory`가 `CategoryA`인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-154">Runs tests which have `UnitTest1` in `FullyQualifiedName` **or** `TestCategory` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~UnitTest1&TestCategory=CategoryA"` | <span data-ttu-id="83584-155">`FullyQualifiedName`에 `UnitTest1`**이 있고** `TestCategory`가 `CategoryA`인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-155">Runs tests which have `UnitTest1` in `FullyQualifiedName` **and** `TestCategory` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~UnitTest1&TestCategory=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="83584-156">`UnitTest1`을 포함하는 `FullyQualifiedName`**이** 있고 `TestCategory`가 `CategoryA`**이거나** `Priority`가 1인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="83584-156">Runs tests which have either `FullyQualifiedName` containing `UnitTest1` **and** `TestCategory` is `CategoryA` **or** `Priority` is 1.</span></span> |
