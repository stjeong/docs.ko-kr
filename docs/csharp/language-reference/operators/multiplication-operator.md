---
title: '* 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 04/04/2018
f1_keywords:
- '*_CSharpKeyword'
helpviewer_keywords:
- multiplication operator (*) [C#]
- '* operator [C#]'
ms.assetid: abd9a5f0-9b24-431e-971a-09ee1c45c50e
ms.openlocfilehash: f4490c4632d9344eb879ea55c20787b838781d91
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333735"
---
# <a name="-operator-c-reference"></a>* 연산자(C# 참조)

곱하기 연산자(`*`)는 피연산자의 곱을 계산합니다. 모든 숫자 형식에는 곱하기 연산자가 미리 정의되어 있습니다.

`*`는 역참조 연산자로 사용되어 포인터를 읽고 쓸 수도 있습니다.

## <a name="remarks"></a>주의

`*` 연산자는 포인터 형식의 선언과 포인터의 역참조에도 사용됩니다. 이 연산자는 [unsafe](../keywords/unsafe.md) 키워드로 표시되었으며 [/unsafe](../compiler-options/unsafe-compiler-option.md) 컴파일러 옵션이 필요한 안전하지 않은 컨텍스트에서만 사용할 수 있습니다.  역참조 연산자를 간접 참조 연산자라고도 합니다.

사용자 정의 형식으로 이항 `*` 연산자를 오버로드할 수 있습니다([operator](../keywords/operator.md) 참조). 이항 연산자가 오버로드되면 해당 대입 연산자도 암시적으로 오버로드됩니다.

## <a name="example"></a>예제

[!code-csharp-interactive[csRefOperators#50](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#50)]

## <a name="example"></a>예제

[!code-csharp[csRefOperators#51](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#51)]

## <a name="see-also"></a>참고 항목

- [C# 참조](../index.md)
- [C# 프로그래밍 가이드](../../programming-guide/index.md)
- [안전하지 않은 코드 및 포인터](../../programming-guide/unsafe-code-pointers/index.md)
- [C# 연산자](index.md)