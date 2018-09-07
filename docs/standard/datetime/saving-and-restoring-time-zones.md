---
title: 저장 및 표준 시간대 복원
ms.date: 04/10/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- restoring time zones
- deserialization [.NET Framework], time zones
- serialization [.NET Framework], time zones
- time zone objects [.NET Framework], restoring
- saving time zones
- time zone objects [.NET Framework], deserializing
- time zones [.NET Framework], saving
- time zones [.NET Framework], restoring
- time zone objects [.NET Framework], serializing
- time zone objects [.NET Framework], saving
ms.assetid: 4028b310-e7ce-49d4-a646-1e83bfaf6f9d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1dc983f1f0b2405f207d69c62b800ee854fcd409
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44081770"
---
# <a name="saving-and-restoring-time-zones"></a><span data-ttu-id="80528-102">저장 및 표준 시간대 복원</span><span class="sxs-lookup"><span data-stu-id="80528-102">Saving and restoring time zones</span></span>

<span data-ttu-id="80528-103"><xref:System.TimeZoneInfo> 미리 정의 된 표준 시간대 데이터를 검색할 레지스트리 의존 하는 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="80528-103">The <xref:System.TimeZoneInfo> class relies on the registry to retrieve predefined time zone data.</span></span> <span data-ttu-id="80528-104">그러나 레지스트리는 동적 구조입니다.</span><span class="sxs-lookup"><span data-stu-id="80528-104">However, the registry is a dynamic structure.</span></span> <span data-ttu-id="80528-105">또한 레지스트리에 포함 된 표준 시간대 정보는 운영 체제에서 현재 연도 대 한 시간 조정 및 변환을 처리 하는 데 주로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80528-105">Additionally, the time zone information that the registry contains is used by the operating system primarily to handle time adjustments and conversions for the current year.</span></span> <span data-ttu-id="80528-106">여기에 정확 하 게 표준 시간대 데이터에 의존 하는 응용 프로그램에 대 한 두 가지 주요 의미가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80528-106">This has two major implications for applications that rely on accurate time zone data:</span></span>

* <span data-ttu-id="80528-107">레지스트리에서 응용 프로그램에 필요한 표준 시간대를 정의할 수 있습니다 하거나 해당 있습니다 바뀌거나 레지스트리에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="80528-107">A time zone that is required by an application may not be defined in the registry, or it may have been renamed or removed from the registry.</span></span>

* <span data-ttu-id="80528-108">레지스트리에 정의 된 표준 시간대에는 기록 표준 시간대 변환에 필요한 특정 조정 규칙에 대 한 정보가 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80528-108">A time zone that is defined in the registry may lack information about the particular adjustment rules that are necessary for historical time zone conversions.</span></span>

<span data-ttu-id="80528-109"><xref:System.TimeZoneInfo> (저장) serialization 및 deserialization (복원)의 표준 시간대 데이터에 대 한 지원을 통해 이러한 한계를 해결 하는 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="80528-109">The <xref:System.TimeZoneInfo> class addresses these limitations through its support for serialization (saving) and deserialization (restoring) of time zone data.</span></span>

## <a name="time-zone-serialization-and-deserialization"></a><span data-ttu-id="80528-110">표준 시간대 serialization 및 deserialization</span><span class="sxs-lookup"><span data-stu-id="80528-110">Time zone serialization and deserialization</span></span>

<span data-ttu-id="80528-111">저장 및 직렬화 및 표준 시간대 데이터를 역직렬화 하 여 표준 시간대 복원 두 메서드 호출을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="80528-111">Saving and restoring a time zone by serializing and deserializing time zone data involves just two method calls:</span></span>

* <span data-ttu-id="80528-112">Serialize 할 수 있습니다는 <xref:System.TimeZoneInfo> 해당 개체를 호출 하 여 개체 <xref:System.TimeZoneInfo.ToSerializedString%2A> 메서드.</span><span class="sxs-lookup"><span data-stu-id="80528-112">You can serialize a <xref:System.TimeZoneInfo> object by calling that object's <xref:System.TimeZoneInfo.ToSerializedString%2A> method.</span></span> <span data-ttu-id="80528-113">메서드 매개 변수를 사용 하 고 표준 시간대 정보가 포함 된 문자열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="80528-113">The method takes no parameters and returns a string that contains time zone information.</span></span>

* <span data-ttu-id="80528-114">Deserialize 할 수는 <xref:System.TimeZoneInfo> 해당 문자열을 전달 하 여 serialize 된 문자열에서 개체를 `static` (`Shared` Visual basic에서) <xref:System.TimeZoneInfo.FromSerializedString%2A?displayProperty=nameWithType> 메서드.</span><span class="sxs-lookup"><span data-stu-id="80528-114">You can deserialize a <xref:System.TimeZoneInfo> object from a serialized string by passing that string to the `static` (`Shared` in Visual Basic) <xref:System.TimeZoneInfo.FromSerializedString%2A?displayProperty=nameWithType> method.</span></span>

## <a name="serialization-and-deserialization-scenarios"></a><span data-ttu-id="80528-115">Serialization 및 deserialization 시나리오</span><span class="sxs-lookup"><span data-stu-id="80528-115">Serialization and deserialization scenarios</span></span>

<span data-ttu-id="80528-116">저장 (또는 직렬화) 하는 기능을 <xref:System.TimeZoneInfo> 나중에 사용할 개체를 문자열로 및 복원 (또는 역직렬화)를 증가 유틸리티와의 유연성을 <xref:System.TimeZoneInfo> 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="80528-116">The ability to save (or serialize) a <xref:System.TimeZoneInfo> object to a string and to restore (or deserialize) it for later use increases both the utility and the flexibility of the <xref:System.TimeZoneInfo> class.</span></span> <span data-ttu-id="80528-117">이 섹션에서는 몇 가지는 serialization 및 deserialization에는 가장 유용한 상황 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="80528-117">This section examines some of the situations in which serialization and deserialization are most useful.</span></span>

### <a name="serializing-and-deserializing-time-zone-data-in-an-application"></a><span data-ttu-id="80528-118">직렬화 및 역직렬화 응용 프로그램에서 표준 시간대 데이터</span><span class="sxs-lookup"><span data-stu-id="80528-118">Serializing and deserializing time zone data in an application</span></span>

<span data-ttu-id="80528-119">필요한 경우 serialize 된 표준 시간대 문자열에서 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80528-119">A serialized time zone can be restored from a string when it is needed.</span></span> <span data-ttu-id="80528-120">레지스트리에서 검색할 표준 시간대 날짜 및 시간을 특정 날짜 범위 내에서 정확 하 게 변환할 수 없는 경우 응용 프로그램은이 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80528-120">An application might do this if the time zone retrieved from the registry is unable to correctly convert a date and time within a particular date range.</span></span> <span data-ttu-id="80528-121">예를 들어, Windows XP 레지스트리에서 표준 시간대 데이터는 일반적으로 Windows Vista 레지스트리에 정의 된 표준 시간대 조정 규칙에 대 한 두 가지 정보를 제공 하는 동안에 하나의 조정 규칙을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80528-121">For example, time zone data in the Windows XP registry supports a single adjustment rule, while time zones defined in the Windows Vista registry typically provide information about two adjustment rules.</span></span> <span data-ttu-id="80528-122">이 과거 시간 변환 정확 하지 않을 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="80528-122">This means that historical time conversions may be inaccurate.</span></span> <span data-ttu-id="80528-123">표준 시간대 데이터의 serialization 및 deserialization에는이 제한을 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80528-123">Serialization and deserialization of time zone data can handle this limitation.</span></span>

<span data-ttu-id="80528-124">다음 예제에서는 사용자 지정에서에서 <xref:System.TimeZoneInfo> 미국을 나타내도록 조정 규칙 없이 클래스 정의 동부 표준 시간대에서에서 1917 년 미국의 일광 절약 시간제를 도입 하기 전에 합니다.</span><span class="sxs-lookup"><span data-stu-id="80528-124">In the following example, a custom <xref:System.TimeZoneInfo> class that has no adjustment rules is defined to represent the U.S. Eastern Standard Time zone from 1883 to 1917, before the introduction of daylight saving time in the United States.</span></span> <span data-ttu-id="80528-125">사용자 지정 표준 시간대는 전역 범위가 있는 변수에 serialize 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80528-125">The custom time zone is serialized in a variable that has global scope.</span></span> <span data-ttu-id="80528-126">표준 시간대 변환 메서드 `ConvertUtcTime`, UTC (Coordinated Universal Time) 시간 변환에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80528-126">The time zone conversion method, `ConvertUtcTime`, is passed Coordinated Universal Time (UTC) times to convert.</span></span> <span data-ttu-id="80528-127">날짜 및 시간 또는 이전 버전에서 1917 발생 하는 경우 사용자 지정 동부 표준시 표준 시간대 serialize 된 문자열에서 복원 되 고 레지스트리에서 검색할 표준 시간대를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="80528-127">If the date and time occurs in 1917 or earlier, the custom Eastern Standard Time zone is restored from a serialized string and replaces the time zone retrieved from the registry.</span></span>

[!code-csharp[System.TimeZone2.Serialization.1#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.TimeZone2.Serialization.1/cs/Serialization.cs#1)]
[!code-vb[System.TimeZone2.Serialization.1#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.TimeZone2.Serialization.1/vb/Serialization.vb#1)]

### <a name="handling-time-zone-exceptions"></a><span data-ttu-id="80528-128">표준 시간대 예외 처리</span><span class="sxs-lookup"><span data-stu-id="80528-128">Handling time zone exceptions</span></span>

<span data-ttu-id="80528-129">레지스트리는 동적 구조 이므로 내용이 실수나 고의로 수정 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80528-129">Because the registry is a dynamic structure, its contents are subject to accidental or deliberate modification.</span></span> <span data-ttu-id="80528-130">즉, 시간대 레지스트리에 정의 되어 있어야 하 고 성공적으로 실행 하도록 응용 프로그램에 필요한 매개 변수가 없을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80528-130">This means that a time zone that should be defined in the registry and that is required for an application to execute successfully may be absent.</span></span> <span data-ttu-id="80528-131">표준 시간대 serialization 및 deserialization에 대 한 지원은 결과 처리 하지만 선택의 여지가 거의 해야 <xref:System.TimeZoneNotFoundException> 응용 프로그램을 종료 하 여 합니다.</span><span class="sxs-lookup"><span data-stu-id="80528-131">Without support for time zone serialization and deserialization, you have little choice but to handle the resulting <xref:System.TimeZoneNotFoundException> by ending the application.</span></span> <span data-ttu-id="80528-132">그러나 표준 시간대 직렬화 및 역직렬화를 사용 하 여 처리할 수 있습니다 예기치 않은 <xref:System.TimeZoneNotFoundException> 복원 하 여 필요한 표준 시간대는 직렬화 된 문자열 및 응용 프로그램에서 계속 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80528-132">However, by using time zone serialization and deserialization, you can handle an unexpected <xref:System.TimeZoneNotFoundException> by restoring the required time zone from a serialized string, and the application will continue to run.</span></span>

<span data-ttu-id="80528-133">다음 예제에서는 만들고 사용자 지정 중앙 표준 시간대를 serialize 합니다.</span><span class="sxs-lookup"><span data-stu-id="80528-133">The following example creates and serializes a custom Central Standard Time zone.</span></span> <span data-ttu-id="80528-134">그런 다음 레지스트리에서 중앙 표준 시간대를 검색 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="80528-134">It then tries to retrieve the Central Standard Time zone from the registry.</span></span> <span data-ttu-id="80528-135">검색 작업 중 하나를 throw 하는 경우는 <xref:System.TimeZoneNotFoundException> 또는 <xref:System.InvalidTimeZoneException>, 예외 처리기는 표준 시간대를 역직렬화 합니다.</span><span class="sxs-lookup"><span data-stu-id="80528-135">If the retrieval operation throws either a <xref:System.TimeZoneNotFoundException> or an <xref:System.InvalidTimeZoneException>, the exception handler deserializes the time zone.</span></span>

[!code-csharp[System.TimeZone2.Serialization.2#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.TimeZone2.Serialization.2/cs/Serialization2.cs#1)]
[!code-vb[System.TimeZone2.Serialization.2#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.TimeZone2.Serialization.2/vb/Serialization2.vb#1)]

### <a name="storing-a-serialized-string-and-restoring-it-when-needed"></a><span data-ttu-id="80528-136">직렬화 된 문자열을 저장 하 고 필요에 따라 복원</span><span class="sxs-lookup"><span data-stu-id="80528-136">Storing a serialized string and restoring it when needed</span></span>

<span data-ttu-id="80528-137">앞의 예제에서는 문자열 변수에 표준 시간대 정보를 저장 있고 필요에 따라 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80528-137">The previous examples have stored time zone information to a string variable and restored it when needed.</span></span> <span data-ttu-id="80528-138">그러나 응용 프로그램 또는 레지스트리에서 영역 정보 자체에 저장할 수는 외부 파일에 리소스와 같은 일부 저장소 매체에 serialize 된 시간을 포함 하는 문자열 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="80528-138">However, the string that contains serialized time zone information can itself be stored in some storage medium, such as an external file, a resource file embedded in the application, or the registry.</span></span> <span data-ttu-id="80528-139">(참고 하 여 사용자 지정 표준 시간대에 대 한 정보 시스템의 표준 시간대 레지스트리 키 외에도 저장 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="80528-139">(Note that information about custom time zones should be stored apart from the system's time zone keys in the registry.)</span></span>

<span data-ttu-id="80528-140">응용 프로그램 자체에서 표준 시간대 생성 루틴을 구분도이 방식으로 직렬화 된 표준 시간대 문자열을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="80528-140">Storing a serialized time zone string in this manner also separates the time zone creation routine from the application itself.</span></span> <span data-ttu-id="80528-141">예를 들어, 표준 시간대 생성 루틴을 실행 하 고 응용 프로그램에서 사용할 수 있는 기록 표준 시간대 정보를 포함 하는 데이터 파일을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80528-141">For example, a time zone creation routine can execute and create a data file that contains historical time zone information that an application can use.</span></span> <span data-ttu-id="80528-142">데이터 파일 수를 응용 프로그램을 함께 설치할 수 열 수 있습니다 및 응용 프로그램을 사용 해야 하는 경우 하나 이상의 해당 표준 시간대를 deserialize 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80528-142">The data file can be then be installed with the application, and it can be opened and one or more of its time zones can be deserialized when the application requires them.</span></span>

<span data-ttu-id="80528-143">Serialize 된 표준 시간대 데이터를 저장 하는 포함된 리소스를 사용 하는 예제를 참조 하세요 [방법: 포함된 리소스에 표준 시간대 저장](../../../docs/standard/datetime/save-time-zones-to-an-embedded-resource.md) 및 [방법: 포함된 리소스에서 표준 시간대 복원](../../../docs/standard/datetime/restore-time-zones-from-an-embedded-resource.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="80528-143">For an example that uses an embedded resource to store serialized time zone data, see [How to: Save time zones to an embedded resource](../../../docs/standard/datetime/save-time-zones-to-an-embedded-resource.md) and [How to: Restore time zones from an embedded resource](../../../docs/standard/datetime/restore-time-zones-from-an-embedded-resource.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="80528-144">참고자료</span><span class="sxs-lookup"><span data-stu-id="80528-144">See also</span></span>

* [<span data-ttu-id="80528-145">날짜, 시간 및 표준 시간대</span><span class="sxs-lookup"><span data-stu-id="80528-145">Dates, times, and time zones</span></span>](../../../docs/standard/datetime/index.md)
