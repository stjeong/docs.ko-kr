---
title: ':: 연산자 - C# 참조'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ::_CSharpKeyword
helpviewer_keywords:
- ':: operator [C#]'
- 'namespaces [C#], :: operator'
- namespace alias qualifier operator (::) [C#]
ms.assetid: 698b5a73-85cf-4e0e-9e8e-6496887f8527
ms.openlocfilehash: 2e456be075f3487676228244e0119ff46ed9a538
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243480"
---
# <a name="-operator-c-reference"></a>:: 연산자(C# 참조)
네임스페이스 별칭 한정자(`::`)는 식별자를 조회하는 데 사용됩니다. 다음 예제와 같이 항상 두 식별자 사이에 옵니다.  
  
 [!code-csharp[csRefOperators#27](../../../csharp/language-reference/operators/codesnippet/CSharp/namespace-alias-qualifer_1.cs)]  

`::` 연산자는 *using 별칭 지시문*과 함께 사용할 수도 있습니다.

```csharp
// using Col=System.Collections.Generic;
var numbers = new Col::List<int> { 1, 2, 3 };
```

## <a name="remarks"></a>설명  
 네임스페이스 별칭 한정자는 `global`일 수 있습니다. 별칭이 지정된 네임스페이스가 아니라 전역 네임스페이스에서 조회를 호출합니다.  
  
## <a name="for-more-information"></a>자세한 내용  
 `::` 연산자를 사용하는 방법의 예는 다음 섹션을 참조하세요.  
  
-   [방법: 전역 네임스페이스 별칭 사용](../../../csharp/programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)  
  
## <a name="c-language-specification"></a>C# 언어 사양  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>참고 항목

- [C# 참조](../../../csharp/language-reference/index.md)  
- [C# 프로그래밍 가이드](../../../csharp/programming-guide/index.md)  
- [C# 연산자](../../../csharp/language-reference/operators/index.md)  
- [네임스페이스 키워드](../../../csharp/language-reference/keywords/namespace-keywords.md)  
- [. 연산자](../../../csharp/language-reference/operators/member-access-operator.md)  
- [extern alias](../../../csharp/language-reference/keywords/extern-alias.md)
