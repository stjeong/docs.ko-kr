---
title: 소스 줄, 파일 및 경로 식별자(F#)
description: '기본 F # 식별자 값 사용 하면 소스 줄 번호, 디렉터리 및 파일 이름을 코드에 액세스할 수 있도록 하는 방법에 알아봅니다.'
ms.date: 05/16/2016
ms.openlocfilehash: 14f710d1412c3420ec627dc30216ba2e89f16bcd
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2018
ms.locfileid: "43865129"
---
# <a name="source-line-file-and-path-identifiers"></a><span data-ttu-id="02887-103">소스 줄, 파일 및 경로 식별자</span><span class="sxs-lookup"><span data-stu-id="02887-103">Source Line, File, and Path Identifiers</span></span>

<span data-ttu-id="02887-104">식별자 `__LINE__`, `__SOURCE_DIRECTORY__` 고 `__SOURCE_FILE__` 소스 줄 번호, 디렉터리 및 파일 이름을 코드에 액세스할 수 있는 기본 제공 값입니다.</span><span class="sxs-lookup"><span data-stu-id="02887-104">The identifiers `__LINE__`, `__SOURCE_DIRECTORY__` and `__SOURCE_FILE__` are built-in values that enable you to access the source line number, directory and file name in your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="02887-105">구문</span><span class="sxs-lookup"><span data-stu-id="02887-105">Syntax</span></span>

```fsharp
__LINE__
__SOURCE_DIRECTORY__
__SOURCE_FILE__
```

## <a name="remarks"></a><span data-ttu-id="02887-106">설명</span><span class="sxs-lookup"><span data-stu-id="02887-106">Remarks</span></span>

<span data-ttu-id="02887-107">이러한 각 값 형식이 `string`합니다.</span><span class="sxs-lookup"><span data-stu-id="02887-107">Each of these values has type `string`.</span></span>

<span data-ttu-id="02887-108">다음 표에서 소스 줄, 파일 및 F #에서 사용할 수 있는 경로 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="02887-108">The following table summarizes the source line, file, and path identifiers that are available in F#.</span></span> <span data-ttu-id="02887-109">이러한 식별자는 전처리기 매크로; 없습니다. 이러한 값은 컴파일러에서 인식 되는 기본 제공 값입니다.</span><span class="sxs-lookup"><span data-stu-id="02887-109">These identifiers are not preprocessor macros; they are built-in values that are recognized by the compiler.</span></span>

|<span data-ttu-id="02887-110">미리 정의 된 식별자</span><span class="sxs-lookup"><span data-stu-id="02887-110">Predefined identifier</span></span>|<span data-ttu-id="02887-111">설명</span><span class="sxs-lookup"><span data-stu-id="02887-111">Description</span></span>|
|---------------------|-----------|
|`__LINE__`|<span data-ttu-id="02887-112">현재 줄 번호를로 고려 `#line` 지시문입니다.</span><span class="sxs-lookup"><span data-stu-id="02887-112">Evaluates to the current line number, considering `#line` directives.</span></span>|
|`__SOURCE_DIRECTORY__`|<span data-ttu-id="02887-113">원본 디렉터리의 전체 경로 평가 고려 `#line` 지시문입니다.</span><span class="sxs-lookup"><span data-stu-id="02887-113">Evaluates to the current full path of the source directory, considering `#line` directives.</span></span>|
|`__SOURCE_FILE__`|<span data-ttu-id="02887-114">현재 소스 파일 이름과 경로 평가 고려 `#line` 지시문입니다.</span><span class="sxs-lookup"><span data-stu-id="02887-114">Evaluates to the current source file name and its path, considering `#line` directives.</span></span>|
<span data-ttu-id="02887-115">에 대 한 자세한 내용은 합니다 `#line` 지시문을 참조 하십시오 [컴파일러 지시문](compiler-directives.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="02887-115">For more information about the `#line` directive, see [Compiler Directives](compiler-directives.md).</span></span>

## <a name="example"></a><span data-ttu-id="02887-116">예제</span><span class="sxs-lookup"><span data-stu-id="02887-116">Example</span></span>

<span data-ttu-id="02887-117">다음 코드 예제에서는 이러한 값을 사용 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="02887-117">The following code example demonstrates the use of these values.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet7401.fs)]

<span data-ttu-id="02887-118">출력:</span><span class="sxs-lookup"><span data-stu-id="02887-118">Output:</span></span>

```
Line: 4
Source Directory: C:\Users\username\Documents\Visual Studio 2017\Projects\SourceInfo\SourceInfo
Source File: C:\Users\username\Documents\Visual Studio 2017\Projects\SourceInfo\SourceInfo\Program.fs
```

## <a name="see-also"></a><span data-ttu-id="02887-119">참고자료</span><span class="sxs-lookup"><span data-stu-id="02887-119">See also</span></span>

- [<span data-ttu-id="02887-120">컴파일러 지시문</span><span class="sxs-lookup"><span data-stu-id="02887-120">Compiler Directives</span></span>](compiler-directives.md)
- [<span data-ttu-id="02887-121">F# 언어 참조</span><span class="sxs-lookup"><span data-stu-id="02887-121">F# Language Reference</span></span>](index.md)
