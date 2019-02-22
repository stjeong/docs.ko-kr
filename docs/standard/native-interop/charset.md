---
title: 문자 집합 및 마샬링 - .NET
description: CharSet의 여러 값을 통해 .NET에서 데이터를 네이티브 코드로 마샬링하는 방식을 변경하는 방법을 알아봅니다.
author: jkoritzinsky
ms.author: jekoritz
ms.date: 01/18/2019
ms.openlocfilehash: 2ff6c485906db481cb5236f83e885ba9fd46450b
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/19/2019
ms.locfileid: "56411409"
---
# <a name="charsets-and-marshalling"></a><span data-ttu-id="f96a0-103">문자 집합 및 마샬링</span><span class="sxs-lookup"><span data-stu-id="f96a0-103">Charsets and marshalling</span></span>

<span data-ttu-id="f96a0-104">`char` 값, `string` 개체 및 `System.Text.StringBuilder` 개체가 마샬링되는 방식은 P/Invoke 또는 구조체 중 하나의 `CharSet` 필드 값에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="f96a0-104">The way `char` values, `string` objects, and `System.Text.StringBuilder` objects are marshalled depends on the value of the `CharSet` field on either the P/Invoke or structure.</span></span> <span data-ttu-id="f96a0-105">P/Invoke를 선언할 때 <xref:System.Runtime.InteropServices.DllImportAttribute.CharSet?displayProperty=nameWithType> 필드를 설정하여 P/Invoke의 `CharSet`를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f96a0-105">You can set the `CharSet` of a P/Invoke by setting the <xref:System.Runtime.InteropServices.DllImportAttribute.CharSet?displayProperty=nameWithType> field when declaring your P/Invoke.</span></span> <span data-ttu-id="f96a0-106">구조체의 `CharSet`를 설정하려면 구조체 선언의 <xref:System.Runtime.InteropServices.StructLayoutAttribute.CharSet?displayProperty=nameWithType> 필드를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f96a0-106">To set the `CharSet` for a structure, set the <xref:System.Runtime.InteropServices.StructLayoutAttribute.CharSet?displayProperty=nameWithType> field on your struct declaration.</span></span> <span data-ttu-id="f96a0-107">이러한 특성 필드가 설정되지 않은 경우 사용할 `CharSet`는 언어 컴파일러에서 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="f96a0-107">When these attribute fields are not set, it is up to the language compiler to determine which `CharSet` to use.</span></span> <span data-ttu-id="f96a0-108">C#에서는 기본적으로 <xref:System.Runtime.InteropServices.CharSet.Ansi> 문자 집합을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f96a0-108">C# uses the <xref:System.Runtime.InteropServices.CharSet.Ansi> charset by default.</span></span>

<span data-ttu-id="f96a0-109">다음 표에서는 각 문자 집합과 해당 문자 집합으로 마샬링할 때 문자 또는 문자열을 나타내는 방법 간의 매핑을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f96a0-109">The following table shows a mapping between each charset and how a character or string is represented when marshalled with that charset:</span></span>

| <span data-ttu-id="f96a0-110">CharSet</span><span class="sxs-lookup"><span data-stu-id="f96a0-110">CharSet</span></span> | <span data-ttu-id="f96a0-111">Windows</span><span class="sxs-lookup"><span data-stu-id="f96a0-111">Windows</span></span> | <span data-ttu-id="f96a0-112">Unix</span><span class="sxs-lookup"><span data-stu-id="f96a0-112">Unix</span></span> | <span data-ttu-id="f96a0-113">Unix의 Mono</span><span class="sxs-lookup"><span data-stu-id="f96a0-113">Mono on Unix</span></span> |
|---------|---------|-------|-------|
| <span data-ttu-id="f96a0-114">Ansi</span><span class="sxs-lookup"><span data-stu-id="f96a0-114">Ansi</span></span>    | <span data-ttu-id="f96a0-115">`char`(ANSI)</span><span class="sxs-lookup"><span data-stu-id="f96a0-115">`char` (ANSI)</span></span>  | <span data-ttu-id="f96a0-116">`char`(macOS의 ANSI, Linux의 UTF-8)</span><span class="sxs-lookup"><span data-stu-id="f96a0-116">`char` (ANSI on macOS, UTF-8 on Linux)</span></span> | <span data-ttu-id="f96a0-117">`char`(UTF-8)</span><span class="sxs-lookup"><span data-stu-id="f96a0-117">`char` (UTF-8)</span></span> |
| <span data-ttu-id="f96a0-118">유니코드(Unicode)</span><span class="sxs-lookup"><span data-stu-id="f96a0-118">Unicode</span></span> | <span data-ttu-id="f96a0-119">`wchar_t`(UTF-16)</span><span class="sxs-lookup"><span data-stu-id="f96a0-119">`wchar_t` (UTF-16)</span></span> | <span data-ttu-id="f96a0-120">`char16_t`(UTF-16)</span><span class="sxs-lookup"><span data-stu-id="f96a0-120">`char16_t` (UTF-16)</span></span> | <span data-ttu-id="f96a0-121">`char16_t`(UTF-16)</span><span class="sxs-lookup"><span data-stu-id="f96a0-121">`char16_t` (UTF-16)</span></span> |
| <span data-ttu-id="f96a0-122">자동</span><span class="sxs-lookup"><span data-stu-id="f96a0-122">Auto</span></span> | <span data-ttu-id="f96a0-123">`wchar_t`(UTF-16)</span><span class="sxs-lookup"><span data-stu-id="f96a0-123">`wchar_t` (UTF-16)</span></span> | <span data-ttu-id="f96a0-124">`char16_t`(UTF-16)</span><span class="sxs-lookup"><span data-stu-id="f96a0-124">`char16_t` (UTF-16)</span></span> | <span data-ttu-id="f96a0-125">`char`(UTF-8)</span><span class="sxs-lookup"><span data-stu-id="f96a0-125">`char` (UTF-8)</span></span> |

<span data-ttu-id="f96a0-126">문자 집합을 선택할 때 네이티브 표현에 필요한 표현을 알고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f96a0-126">Make sure you know what representation your native representation expects when picking your charset.</span></span>
