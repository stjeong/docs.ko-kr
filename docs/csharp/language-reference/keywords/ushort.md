---
title: ushort 키워드 - C# 참조
ms.custom: seodec18
ms.date: 03/14/2017
f1_keywords:
- ushort
- ushort_CSharpKeyword
helpviewer_keywords:
- ushort keyword [C#]
ms.assetid: 1a7dbaae-b7a0-4111-872a-c88a6d3981ac
ms.openlocfilehash: 934e25576a8a24c176a54ec6af984459b513fe5a
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53614463"
---
# <a name="ushort-c-reference"></a>ushort(C# 참조)

`ushort` 키워드는 다음 표에 나와 있는 크기와 범위에 따라 값을 저장하는 정수 데이터 형식을 나타냅니다.

|형식|범위|크기|.NET 형식|
|----------|-----------|----------|-------------------------|
|`ushort`|0 ~ 65,535|부호 없는 16비트 정수|<xref:System.UInt16?displayProperty=nameWithType>|

## <a name="literals"></a>리터럴

10진수 리터럴, 16진수 리터럴 또는 (C# 7.0부터) 이진 리터럴을 할당하여 `ushort` 변수를 선언하고 초기화할 수 있습니다. 정수 리터럴이 `ushort` 범위를 벗어나는 경우(즉 <xref:System.UInt16.MinValue?displayProperty=nameWithType>보다 작거나 <xref:System.UInt16.MaxValue?displayProperty=nameWithType>보다 큰 경우) 컴파일 오류가 발생합니다.

다음 예제에서는 10진수, 16진수 및 이진 리터럴로 표현된 65,034와 같은 정수가 [int](int.md)에서 `ushort` 값으로 암시적으로 변환됩니다.

[!code-csharp[UShort](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#UShort)]

> [!NOTE]
> `0x` 또는 `0X` 접두사를 사용하여 16진수 리터럴을 나타내고, `0b` 또는 `0B` 접두사를 사용하여 이진 리터럴을 나타냅니다. 10진수 리터럴에는 접두사가 없습니다.

C# 7.0부터 가독성 향상을 위해 몇 가지 기능이 추가되었습니다.

- C# 7.0은 숫자 구분 기호로 밑줄 문자 `_`를 사용할 수 있습니다.
- C# 7.2는 접두사 뒤에 이진 또는 16진수 리터럴에 대한 자리 구분 기호로 `_`을 사용할 수 있습니다. 10진수 리터럴에 선행 밑줄이 있는 것이 허용되지 않습니다.

일부 예제는 다음과 같습니다.

[!code-csharp[UShort](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#UShortS)]

## <a name="compiler-overload-resolution"></a>컴파일러 오버로드 확인

오버로드된 메서드를 호출할 때 캐스트를 사용해야 합니다. 예를 들어 `ushort` 및 [int](int.md) 매개 변수를 사용하는 다음의 오버로드된 메서드를 살펴보세요.

```csharp
public static void SampleMethod(int i) {}
public static void SampleMethod(ushort s) {}
```

`ushort` 캐스트를 사용하면 올바른 형식이 호출됩니다. 예를 들면 다음과 같습니다.

```csharp
// Calls the method with the int parameter:
SampleMethod(5);
// Calls the method with the ushort parameter:
SampleMethod((ushort)5);
```

## <a name="conversions"></a>변환

`ushort`에서 [int](int.md), [uint](uint.md), [long](long.md), [ulong](ulong.md), [float](float.md), [double](double.md) 또는 [decimal](decimal.md)로의 미리 정의된 암시적 변환이 있습니다.

[byte](byte.md) 또는 [char](char.md)에서 `ushort`로 미리 정의된 암시적 변환이 있습니다. 아니면 캐스트를 사용해 명시적 변환을 수행해야 합니다. 예를 들어 다음 두 가지 `ushort` 변수 `x` 및 `y`를 고려해 보세요.

```csharp
ushort x = 5, y = 12;
```

다음 대입문은 대입 연산자의 오른쪽에 있는 산술 식이 기본적으로 `int`로 계산되므로 컴파일 오류를 생성합니다.

```csharp
ushort z = x + y;   // Error: conversion from int to ushort
```

이 문제를 해결하려면 다음 캐스트를 사용합니다.

```csharp
ushort z = (ushort)(x + y);   // OK: explicit conversion
```

그러나 대상 변수에 동일한 스토리지 크기 또는 더 큰 스토리지 크기가 있는 다음 명령문을 사용할 수 있습니다.

```csharp
int m = x + y;
long n = x + y;
```

부동 소수점 형식에서 `ushort`로의 암시적 변환은 없습니다. 예를 들어 명시적 캐스트를 사용하지 않는 경우 다음 문은 컴파일러 오류를 일으킵니다.

```csharp
// Error -- no implicit conversion from double:
ushort x = 3.0;
// OK -- explicit conversion:
ushort y = (ushort)3.0;
```

부동 소수점 형식 및 정수 형식이 혼합된 산술 식에 대한 자세한 내용은 [float](float.md) 및 [double](double.md)을 참조하세요.

암시적 숫자 변환 규칙에 대한 자세한 내용은 [암시적 숫자 변환 표](implicit-numeric-conversions-table.md)를 참조하세요.

## <a name="c-language-specification"></a>C# 언어 사양

자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [정수 형식](~/_csharplang/spec/types.md#integral-types)을 참조하세요. C# 언어 사양은 C# 구문 및 사용법에 대한 신뢰할 수 있는 소스입니다.

## <a name="see-also"></a>참고 항목

- <xref:System.UInt16>
- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 키워드](index.md)
- [정수 계열 형식 표](integral-types-table.md)
- [기본 제공 형식 표](built-in-types-table.md)
- [암시적 숫자 변환 표](implicit-numeric-conversions-table.md)
- [명시적 숫자 변환 표](explicit-numeric-conversions-table.md)
