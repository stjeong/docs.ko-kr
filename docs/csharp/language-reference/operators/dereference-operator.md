---
title: -&gt; 연산자 - C# 참조
ms.custom: seodec18
ms.date: 11/26/2018
f1_keywords:
- ->_CSharpKeyword
helpviewer_keywords:
- member access operator (->) [C#]
- -> operator [C#]
ms.assetid: e39ccdc1-f1ff-4a92-bf1d-ac2c8c11316a
ms.openlocfilehash: bb1ccd026f403e68565c5c7681943d8017578d01
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53234892"
---
# <a name="-gt-operator-c-reference"></a>-&gt; 연산자(C# 참조)

포인터 멤버 액세스 연산자 `->`는 포인터 간접 참조 및 멤버 액세스를 결합합니다.

`x`가 `T*` 형식의 포인터이고 `y`가 `T`의 액세스 가능한 멤버인 경우 다음 형식의 식을 가정해 보세요.

```csharp
x->y
```

위의 식은 아래의 식과 동일합니다.

```csharp
(*x).y
```

`->` 연산자에 [안전하지 않은](../keywords/unsafe.md) 컨텍스트가 필요합니다.

자세한 내용은 [방법: 포인터를 사용하여 멤버 액세스](../../programming-guide/unsafe-code-pointers/how-to-access-a-member-with-a-pointer.md)를 참조하세요.

## <a name="operator-overloadability"></a>연산자 오버로드 가능성

`->` 연산자를 오버로드할 수 없습니다.

## <a name="c-language-specification"></a>C# 언어 사양

자세한 내용은 [C# 언어 사양](../language-specification/index.md)의 [포인터 멤버 액세스](~/_csharplang/spec/unsafe-code.md#pointer-member-access) 섹션을 참조하세요.

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [C# 연산자](index.md)
- [포인터 형식](../../programming-guide/unsafe-code-pointers/pointer-types.md)
