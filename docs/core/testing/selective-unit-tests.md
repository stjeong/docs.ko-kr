---
title: 선택적 단위 테스트 실행
description: 필터 식을 사용하여 .NET Core의 dotnet 테스트 명령을 통해 선택적 단위 테스트를 실행하는 방법입니다.
author: smadala
ms.date: 03/22/2017
ms.custom: seodec18
ms.openlocfilehash: 2ec6dc770f33acc4acea79e60cf6f9c33f1077d8
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53239945"
---
# <a name="running-selective-unit-tests"></a><span data-ttu-id="e87eb-103">선택적 단위 테스트 실행</span><span class="sxs-lookup"><span data-stu-id="e87eb-103">Running selective unit tests</span></span>

<span data-ttu-id="e87eb-104">.NET Core에서 `dotnet test` 명령과 함께 필터 식을 사용하여 선택적 테스트를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-104">With the `dotnet test` command in .NET Core, you can use a filter expression to run selective tests.</span></span> <span data-ttu-id="e87eb-105">이 문서에서는 실행되는 테스트를 필터링하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-105">This article demonstrates how to filter which test are run.</span></span> <span data-ttu-id="e87eb-106">다음 예제에서는 `dotnet test`를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-106">The following examples use `dotnet test`.</span></span> <span data-ttu-id="e87eb-107">`vstest.console.exe`를 사용하는 경우 `--filter `를 `--testcasefilter:`로 바꾸세요.</span><span class="sxs-lookup"><span data-stu-id="e87eb-107">If you're using `vstest.console.exe`, replace `--filter ` with `--testcasefilter:`.</span></span>

## <a name="mstest"></a><span data-ttu-id="e87eb-108">MSTest</span><span class="sxs-lookup"><span data-stu-id="e87eb-108">MSTest</span></span>

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

| <span data-ttu-id="e87eb-109">식</span><span class="sxs-lookup"><span data-stu-id="e87eb-109">Expression</span></span> | <span data-ttu-id="e87eb-110">결과</span><span class="sxs-lookup"><span data-stu-id="e87eb-110">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter Method` | <span data-ttu-id="e87eb-111">`FullyQualifiedName`에 `Method`가 포함된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-111">Runs tests whose `FullyQualifiedName` contains `Method`.</span></span> <span data-ttu-id="e87eb-112">`vstest 15.1+`에서 사용 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-112">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Name~TestMethod1` | <span data-ttu-id="e87eb-113">이름에 `TestMethod1`이 포함된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-113">Runs tests whose name contains `TestMethod1`.</span></span> |
| `dotnet test --filter ClassName=MSTestNamespace.UnitTest1` | <span data-ttu-id="e87eb-114">클래스 `MSTestNamespace.UnitTest1`에 속하는 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-114">Runs tests which are in class `MSTestNamespace.UnitTest1`.</span></span><br><span data-ttu-id="e87eb-115">**참고:** `ClassName` 값에는 네임스페이스가 있어야 하므로, `ClassName=UnitTest1`이 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-115">**Note:** The `ClassName` value should have a namespace, so `ClassName=UnitTest1` won't work.</span></span> |
| `dotnet test --filter FullyQualifiedName!=MSTestNamespace.UnitTest1.TestMethod1` | <span data-ttu-id="e87eb-116">`MSTestNamespace.UnitTest1.TestMethod1`을 제외한 모든 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-116">Runs all tests except `MSTestNamespace.UnitTest1.TestMethod1`.</span></span> |
| `dotnet test --filter TestCategory=CategoryA` | <span data-ttu-id="e87eb-117">`[TestCategory("CategoryA")]`로 주석이 추가된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-117">Runs tests which are annotated with `[TestCategory("CategoryA")]`.</span></span> |
| `dotnet test --filter Priority=2` | <span data-ttu-id="e87eb-118">`[Priority(2)]`로 주석이 추가된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-118">Runs tests which are annotated with `[Priority(2)]`.</span></span><br>

<span data-ttu-id="e87eb-119">**조건 연산자 | 및 &amp; 사용**</span><span class="sxs-lookup"><span data-stu-id="e87eb-119">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="e87eb-120">식</span><span class="sxs-lookup"><span data-stu-id="e87eb-120">Expression</span></span> | <span data-ttu-id="e87eb-121">결과</span><span class="sxs-lookup"><span data-stu-id="e87eb-121">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~UnitTest1&#124;TestCategory=CategoryA"</code> | <span data-ttu-id="e87eb-122">`FullyQualifiedName`에 `UnitTest1`이 **있거나** `TestCategory`가 `CategoryA`인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-122">Runs tests which have `UnitTest1` in `FullyQualifiedName` **or** `TestCategory` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~UnitTest1&TestCategory=CategoryA"` | <span data-ttu-id="e87eb-123">`FullyQualifiedName`에 `UnitTest1`**이 있고** `TestCategory`가 `CategoryA`인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-123">Runs tests which have `UnitTest1` in `FullyQualifiedName` **and** `TestCategory` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~UnitTest1&TestCategory=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="e87eb-124">`UnitTest1`을 포함하는 `FullyQualifiedName`**이 있고**`TestCategory`가 `CategoryA`**이거나** `Priority`가 1인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-124">Runs tests which have either `FullyQualifiedName` containing `UnitTest1` **and** `TestCategory` is `CategoryA` **or** `Priority` is 1.</span></span> |

## <a name="xunit"></a><span data-ttu-id="e87eb-125">xUnit</span><span class="sxs-lookup"><span data-stu-id="e87eb-125">xUnit</span></span>

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

| <span data-ttu-id="e87eb-126">식</span><span class="sxs-lookup"><span data-stu-id="e87eb-126">Expression</span></span> | <span data-ttu-id="e87eb-127">결과</span><span class="sxs-lookup"><span data-stu-id="e87eb-127">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter DisplayName=XUnitNamespace.TestClass1.Test1` | <span data-ttu-id="e87eb-128">`XUnitNamespace.TestClass1.Test1` 테스트를 하나만 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-128">Runs only one test, `XUnitNamespace.TestClass1.Test1`.</span></span> |
| `dotnet test --filter FullyQualifiedName!=XUnitNamespace.TestClass1.Test1` | <span data-ttu-id="e87eb-129">`XUnitNamespace.TestClass1.Test1`을 제외한 모든 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-129">Runs all tests except `XUnitNamespace.TestClass1.Test1`.</span></span> |
| `dotnet test --filter DisplayName~TestClass1` | <span data-ttu-id="e87eb-130">표시 이름에 `TestClass1`이 포함된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-130">Runs tests whose display name contains `TestClass1`.</span></span> |

<span data-ttu-id="e87eb-131">코드 예제에서 `Category` 및 `Priority` 키로 정의된 특성은 필터링에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-131">In the code example, the defined traits with keys `Category` and `Priority` can be used for filtering.</span></span>

| <span data-ttu-id="e87eb-132">식</span><span class="sxs-lookup"><span data-stu-id="e87eb-132">Expression</span></span> | <span data-ttu-id="e87eb-133">결과</span><span class="sxs-lookup"><span data-stu-id="e87eb-133">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter XUnit` | <span data-ttu-id="e87eb-134">`FullyQualifiedName`에 `XUnit`가 포함된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-134">Runs tests whose `FullyQualifiedName` contains `XUnit`.</span></span>  <span data-ttu-id="e87eb-135">`vstest 15.1+`에서 사용 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-135">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Category=CategoryA` | <span data-ttu-id="e87eb-136">`[Trait("Category", "CategoryA")]`가 있는 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-136">Runs tests which have `[Trait("Category", "CategoryA")]`.</span></span> |

<span data-ttu-id="e87eb-137">**조건 연산자 | 및 &amp; 사용**</span><span class="sxs-lookup"><span data-stu-id="e87eb-137">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="e87eb-138">식</span><span class="sxs-lookup"><span data-stu-id="e87eb-138">Expression</span></span> | <span data-ttu-id="e87eb-139">결과</span><span class="sxs-lookup"><span data-stu-id="e87eb-139">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~TestClass1&#124;Category=CategoryA"</code> | <span data-ttu-id="e87eb-140">`FullyQualifiedName`에 `TestClass1`이 **있거나**`Category`가 `CategoryA`인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-140">Runs tests which has `TestClass1` in `FullyQualifiedName` **or** `Category` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~TestClass1&Category=CategoryA"` | <span data-ttu-id="e87eb-141">`FullyQualifiedName`에 `TestClass1`**이 있고** `Category`가 `CategoryA`인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-141">Runs tests which has `TestClass1` in `FullyQualifiedName` **and** `Category` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~TestClass1&Category=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="e87eb-142">`TestClass1`을 포함하는 `FullyQualifiedName`**이 있고**`Category`가 `CategoryA`**이거나** `Priority`가 1인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-142">Runs tests which have either `FullyQualifiedName` containing `TestClass1` **and** `Category` is `CategoryA` **or** `Priority` is 1.</span></span> |

## <a name="nunit"></a><span data-ttu-id="e87eb-143">NUnit</span><span class="sxs-lookup"><span data-stu-id="e87eb-143">NUnit</span></span>

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

| <span data-ttu-id="e87eb-144">식</span><span class="sxs-lookup"><span data-stu-id="e87eb-144">Expression</span></span> | <span data-ttu-id="e87eb-145">결과</span><span class="sxs-lookup"><span data-stu-id="e87eb-145">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter Method` | <span data-ttu-id="e87eb-146">`FullyQualifiedName`에 `Method`가 포함된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-146">Runs tests whose `FullyQualifiedName` contains `Method`.</span></span> <span data-ttu-id="e87eb-147">`vstest 15.1+`에서 사용 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-147">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Name~TestMethod1` | <span data-ttu-id="e87eb-148">이름에 `TestMethod1`이 포함된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-148">Runs tests whose name contains `TestMethod1`.</span></span> |
| `dotnet test --filter FullyQualifiedName~NUnitNamespace.UnitTest1` | <span data-ttu-id="e87eb-149">클래스 `NUnitNamespace.UnitTest1`에 속하는 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-149">Runs tests which are in class `NUnitNamespace.UnitTest1`.</span></span><br>
| `dotnet test --filter FullyQualifiedName!=NUnitNamespace.UnitTest1.TestMethod1` | <span data-ttu-id="e87eb-150">`NUnitNamespace.UnitTest1.TestMethod1`을 제외한 모든 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-150">Runs all tests except `NUnitNamespace.UnitTest1.TestMethod1`.</span></span> |
| `dotnet test --filter TestCategory=CategoryA` | <span data-ttu-id="e87eb-151">`[Category("CategoryA")]`로 주석이 추가된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-151">Runs tests which are annotated with `[Category("CategoryA")]`.</span></span> |
| `dotnet test --filter Priority=2` | <span data-ttu-id="e87eb-152">`[Priority(2)]`로 주석이 추가된 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-152">Runs tests which are annotated with `[Priority(2)]`.</span></span><br>

<span data-ttu-id="e87eb-153">**조건 연산자 | 및 &amp; 사용**</span><span class="sxs-lookup"><span data-stu-id="e87eb-153">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="e87eb-154">식</span><span class="sxs-lookup"><span data-stu-id="e87eb-154">Expression</span></span> | <span data-ttu-id="e87eb-155">결과</span><span class="sxs-lookup"><span data-stu-id="e87eb-155">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~UnitTest1&#124;TestCategory=CategoryA"</code> | <span data-ttu-id="e87eb-156">`FullyQualifiedName`에 `UnitTest1`이 **있거나** `TestCategory`가 `CategoryA`인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-156">Runs tests which have `UnitTest1` in `FullyQualifiedName` **or** `TestCategory` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~UnitTest1&TestCategory=CategoryA"` | <span data-ttu-id="e87eb-157">`FullyQualifiedName`에 `UnitTest1`**이 있고** `TestCategory`가 `CategoryA`인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-157">Runs tests which have `UnitTest1` in `FullyQualifiedName` **and** `TestCategory` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~UnitTest1&TestCategory=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="e87eb-158">`UnitTest1`을 포함하는 `FullyQualifiedName`**이 있고**`TestCategory`가 `CategoryA`**이거나** `Priority`가 1인 테스트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e87eb-158">Runs tests which have either `FullyQualifiedName` containing `UnitTest1` **and** `TestCategory` is `CategoryA` **or** `Priority` is 1.</span></span> |
