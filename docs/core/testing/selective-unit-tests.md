---
title: 선택적 단위 테스트 실행
description: 필터 식을 사용하여 dotnet 명령으로 선택적 단위 테스트를 실행하는 방법을 보여 줍니다.
author: smadala
ms.author: mairaw
ms.date: 03/22/2017
ms.openlocfilehash: 428e31014f5d8d487deb7c4b4317ebcef13c294d
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43517222"
---
# <a name="running-selective-unit-tests"></a><span data-ttu-id="e4805-103">선택적 단위 테스트 실행</span><span class="sxs-lookup"><span data-stu-id="e4805-103">Running selective unit tests</span></span>

<span data-ttu-id="e4805-104">다음 예제에서는 `dotnet test`를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-104">The following examples use `dotnet test`.</span></span> <span data-ttu-id="e4805-105">`vstest.console.exe`를 사용하는 경우 `--filter `를 `--testcasefilter:`로 바꾸세요.</span><span class="sxs-lookup"><span data-stu-id="e4805-105">If you're using `vstest.console.exe`, replace `--filter ` with `--testcasefilter:`.</span></span>

## <a name="mstest"></a><span data-ttu-id="e4805-106">MSTest</span><span class="sxs-lookup"><span data-stu-id="e4805-106">MSTest</span></span>

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

| <span data-ttu-id="e4805-107">식</span><span class="sxs-lookup"><span data-stu-id="e4805-107">Expression</span></span> | <span data-ttu-id="e4805-108">결과</span><span class="sxs-lookup"><span data-stu-id="e4805-108">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter Method` | <span data-ttu-id="e4805-109">`FullyQualifiedName`에 `Method`가 포함된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-109">Runs tests whose `FullyQualifiedName` contains `Method`.</span></span> <span data-ttu-id="e4805-110">`vstest 15.1+`에서 사용 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-110">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Name~TestMethod1` | <span data-ttu-id="e4805-111">이름에 `TestMethod1`이 포함된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-111">Runs tests whose name contains `TestMethod1`.</span></span> |
| `dotnet test --filter ClassName=MSTestNamespace.UnitTest1` | <span data-ttu-id="e4805-112">클래스 `MSTestNamespace.UnitTest1`에 속하는 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-112">Runs tests which are in class `MSTestNamespace.UnitTest1`.</span></span><br><span data-ttu-id="e4805-113">**참고:** `ClassName` 값에는 네임스페이스가 있어야 하므로, `ClassName=UnitTest1`이 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-113">**Note:** The `ClassName` value should have a namespace, so `ClassName=UnitTest1` won't work.</span></span> |
| `dotnet test --filter FullyQualifiedName!=MSTestNamespace.UnitTest1.TestMethod1` | <span data-ttu-id="e4805-114">`MSTestNamespace.UnitTest1.TestMethod1`을 제외한 모든 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-114">Runs all tests except `MSTestNamespace.UnitTest1.TestMethod1`.</span></span> |
| `dotnet test --filter TestCategory=CategoryA` | <span data-ttu-id="e4805-115">`[TestCategory("CategoryA")]`로 주석이 추가된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-115">Runs tests which are annotated with `[TestCategory("CategoryA")]`.</span></span> |
| `dotnet test --filter Priority=2` | <span data-ttu-id="e4805-116">`[Priority(2)]`로 주석이 추가된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-116">Runs tests which are annotated with `[Priority(2)]`.</span></span><br>

<span data-ttu-id="e4805-117">**조건 연산자 | 및 &amp; 사용**</span><span class="sxs-lookup"><span data-stu-id="e4805-117">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="e4805-118">식</span><span class="sxs-lookup"><span data-stu-id="e4805-118">Expression</span></span> | <span data-ttu-id="e4805-119">결과</span><span class="sxs-lookup"><span data-stu-id="e4805-119">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~UnitTest1&#124;TestCategory=CategoryA"</code> | <span data-ttu-id="e4805-120">`FullyQualifiedName`에 `UnitTest1`이 **있거나** `TestCategory`가 `CategoryA`인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-120">Runs tests which have `UnitTest1` in `FullyQualifiedName` **or** `TestCategory` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~UnitTest1&TestCategory=CategoryA"` | <span data-ttu-id="e4805-121">`FullyQualifiedName`에 `UnitTest1`**이 있고** `TestCategory`가 `CategoryA`인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-121">Runs tests which have `UnitTest1` in `FullyQualifiedName` **and** `TestCategory` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~UnitTest1&TestCategory=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="e4805-122">`UnitTest1`을 포함하는 `FullyQualifiedName`**이 있고**`TestCategory`가 `CategoryA`**이거나** `Priority`가 1인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-122">Runs tests which have either `FullyQualifiedName` containing `UnitTest1` **and** `TestCategory` is `CategoryA` **or** `Priority` is 1.</span></span> |

## <a name="xunit"></a><span data-ttu-id="e4805-123">xUnit</span><span class="sxs-lookup"><span data-stu-id="e4805-123">xUnit</span></span>

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

| <span data-ttu-id="e4805-124">식</span><span class="sxs-lookup"><span data-stu-id="e4805-124">Expression</span></span> | <span data-ttu-id="e4805-125">결과</span><span class="sxs-lookup"><span data-stu-id="e4805-125">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter DisplayName=XUnitNamespace.TestClass1.Test1` | <span data-ttu-id="e4805-126">`XUnitNamespace.TestClass1.Test1` 테스트를 하나만 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-126">Runs only one test, `XUnitNamespace.TestClass1.Test1`.</span></span> |
| `dotnet test --filter FullyQualifiedName!=XUnitNamespace.TestClass1.Test1` | <span data-ttu-id="e4805-127">`XUnitNamespace.TestClass1.Test1`을 제외한 모든 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-127">Runs all tests except `XUnitNamespace.TestClass1.Test1`.</span></span> |
| `dotnet test --filter DisplayName~TestClass1` | <span data-ttu-id="e4805-128">표시 이름에 `TestClass1`이 포함된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-128">Runs tests whose display name contains `TestClass1`.</span></span> |

<span data-ttu-id="e4805-129">코드 예제에서 `Category` 및 `Priority` 키로 정의된 특성은 필터링에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-129">In the code example, the defined traits with keys `Category` and `Priority` can be used for filtering.</span></span>

| <span data-ttu-id="e4805-130">식</span><span class="sxs-lookup"><span data-stu-id="e4805-130">Expression</span></span> | <span data-ttu-id="e4805-131">결과</span><span class="sxs-lookup"><span data-stu-id="e4805-131">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter XUnit` | <span data-ttu-id="e4805-132">`FullyQualifiedName`에 `XUnit`가 포함된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-132">Runs tests whose `FullyQualifiedName` contains `XUnit`.</span></span>  <span data-ttu-id="e4805-133">`vstest 15.1+`에서 사용 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-133">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Category=CategoryA` | <span data-ttu-id="e4805-134">`[Trait("Category", "CategoryA")]`가 있는 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-134">Runs tests which have `[Trait("Category", "CategoryA")]`.</span></span> |

<span data-ttu-id="e4805-135">**조건 연산자 | 및 &amp; 사용**</span><span class="sxs-lookup"><span data-stu-id="e4805-135">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="e4805-136">식</span><span class="sxs-lookup"><span data-stu-id="e4805-136">Expression</span></span> | <span data-ttu-id="e4805-137">결과</span><span class="sxs-lookup"><span data-stu-id="e4805-137">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~TestClass1&#124;Category=CategoryA"</code> | <span data-ttu-id="e4805-138">`FullyQualifiedName`에 `TestClass1`이 **있거나**`Category`가 `CategoryA`인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-138">Runs tests which has `TestClass1` in `FullyQualifiedName` **or** `Category` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~TestClass1&Category=CategoryA"` | <span data-ttu-id="e4805-139">`FullyQualifiedName`에 `TestClass1`**이 있고** `Category`가 `CategoryA`인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-139">Runs tests which has `TestClass1` in `FullyQualifiedName` **and** `Category` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~TestClass1&Category=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="e4805-140">`TestClass1`을 포함하는 `FullyQualifiedName`**이 있고**`Category`가 `CategoryA`**이거나** `Priority`가 1인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-140">Runs tests which have either `FullyQualifiedName` containing `TestClass1` **and** `Category` is `CategoryA` **or** `Priority` is 1.</span></span> |

## <a name="nunit"></a><span data-ttu-id="e4805-141">NUnit</span><span class="sxs-lookup"><span data-stu-id="e4805-141">NUnit</span></span>

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

| <span data-ttu-id="e4805-142">식</span><span class="sxs-lookup"><span data-stu-id="e4805-142">Expression</span></span> | <span data-ttu-id="e4805-143">결과</span><span class="sxs-lookup"><span data-stu-id="e4805-143">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter Method` | <span data-ttu-id="e4805-144">`FullyQualifiedName`에 `Method`가 포함된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-144">Runs tests whose `FullyQualifiedName` contains `Method`.</span></span> <span data-ttu-id="e4805-145">`vstest 15.1+`에서 사용 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-145">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Name~TestMethod1` | <span data-ttu-id="e4805-146">이름에 `TestMethod1`이 포함된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-146">Runs tests whose name contains `TestMethod1`.</span></span> |
| `dotnet test --filter FullyQualifiedName~NUnitNamespace.UnitTest1` | <span data-ttu-id="e4805-147">클래스 `NUnitNamespace.UnitTest1`에 속하는 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-147">Runs tests which are in class `NUnitNamespace.UnitTest1`.</span></span><br>
| `dotnet test --filter FullyQualifiedName!=NUnitNamespace.UnitTest1.TestMethod1` | <span data-ttu-id="e4805-148">`NUnitNamespace.UnitTest1.TestMethod1`을 제외한 모든 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-148">Runs all tests except `NUnitNamespace.UnitTest1.TestMethod1`.</span></span> |
| `dotnet test --filter TestCategory=CategoryA` | <span data-ttu-id="e4805-149">`[Category("CategoryA")]`로 주석이 추가된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-149">Runs tests which are annotated with `[Category("CategoryA")]`.</span></span> |
| `dotnet test --filter Priority=2` | <span data-ttu-id="e4805-150">`[Priority(2)]`로 주석이 추가된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-150">Runs tests which are annotated with `[Priority(2)]`.</span></span><br>

<span data-ttu-id="e4805-151">**조건 연산자 | 및 &amp; 사용**</span><span class="sxs-lookup"><span data-stu-id="e4805-151">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="e4805-152">식</span><span class="sxs-lookup"><span data-stu-id="e4805-152">Expression</span></span> | <span data-ttu-id="e4805-153">결과</span><span class="sxs-lookup"><span data-stu-id="e4805-153">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~UnitTest1&#124;TestCategory=CategoryA"</code> | <span data-ttu-id="e4805-154">`FullyQualifiedName`에 `UnitTest1`이 **있거나** `TestCategory`가 `CategoryA`인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-154">Runs tests which have `UnitTest1` in `FullyQualifiedName` **or** `TestCategory` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~UnitTest1&TestCategory=CategoryA"` | <span data-ttu-id="e4805-155">`FullyQualifiedName`에 `UnitTest1`**이 있고** `TestCategory`가 `CategoryA`인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-155">Runs tests which have `UnitTest1` in `FullyQualifiedName` **and** `TestCategory` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~UnitTest1&TestCategory=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="e4805-156">`UnitTest1`을 포함하는 `FullyQualifiedName`**이 있고**`TestCategory`가 `CategoryA`**이거나** `Priority`가 1인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4805-156">Runs tests which have either `FullyQualifiedName` containing `UnitTest1` **and** `TestCategory` is `CategoryA` **or** `Priority` is 1.</span></span> |
