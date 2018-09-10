---
title: public 키워드(C# 참조)
ms.date: 07/20/2015
f1_keywords:
- public
- public_CSharpKeyword
helpviewer_keywords:
- public keyword [C#]
ms.assetid: 0ae45d16-a551-4b74-9845-57208de1328e
ms.openlocfilehash: 84a3bc49b6eea047d518edc01dab7f2301854b6a
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43518188"
---
# <a name="public-c-reference"></a>public(C# 참조)

`public` 키워드는 형식 및 형식 멤버에 대한 액세스 한정자입니다. 공용 액세스는 허용 범위가 가장 큰 액세스 수준입니다. 다음 예제와 같이, 공용 멤버 액세스에 대한 제한은 없습니다.

```csharp
class SampleClass
{
    public int x; // No access restrictions.
}
```

자세한 내용은 [액세스 한정자](../../programming-guide/classes-and-structs/access-modifiers.md) 및 [액세스 가능성 수준](accessibility-levels.md)을 참조하세요.

## <a name="example"></a>예

다음 예제에서는 두 개의 클래스, `PointTest` 및 `MainClass`를 선언합니다. `PointTest`의 공용 멤버 `x` 및 `y`는 `MainClass`에서 직접 액세스합니다.

[!code-csharp[csrefKeywordsModifiers#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#13)]

`public` 액세스 수준을 [private](private.md) 또는 [protected](protected.md)로 변경하면 오류 메시지가 표시됩니다.

보호 수준 때문에 'PointTest.y'에 액세스할 수 없습니다.

## <a name="c-language-specification"></a>C# 언어 사양

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [액세스 한정자](../../programming-guide/classes-and-structs/access-modifiers.md)
- [C# 키워드](index.md)
- [액세스 한정자](access-modifiers.md)
- [액세스 수준](accessibility-levels.md)
- [한정자](modifiers.md)
- [private](private.md)
- [protected](protected.md)
- [internal](internal.md)