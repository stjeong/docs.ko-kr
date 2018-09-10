---
title: = 연산자(C# 참조)
ms.date: 07/20/2015
f1_keywords:
- =_CSharpKeyword
helpviewer_keywords:
- = operator [C#]
ms.assetid: d802a6d5-32f0-42b8-b180-12f5a081bfc1
ms.openlocfilehash: 9cd1af400a9afdb7942a49dee7e7f7bb78387f2d
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43507356"
---
# <a name="-operator-c-reference"></a>= 연산자(C# 참조)
대입 연산자(`=`)는 왼쪽 피연산자가 나타내는 저장소 위치, 속성 또는 인덱서에 오른쪽 피연산자의 값을 저장하고 그 값을 해당 결과로 반환합니다. 피연산자는 동일한 형식이어야 합니다(또는 오른쪽 피연산자를 왼쪽 피연산자의 형식으로 암시적으로 변환할 수 있어야 함).  
  
## <a name="remarks"></a>설명  
 대입 연산자는 오버로드할 수 없습니다. 그러나 형식에 대한 암시적 변환 연산자를 정의할 수 있으며, 이 연산자를 통해 해당 형식에 대입 연산자를 사용할 수 있습니다. 자세한 내용은 [변환 연산자 사용](../../../csharp/programming-guide/statements-expressions-operators/using-conversion-operators.md)을 참조하세요.  
  
## <a name="example"></a>예  
 [!code-csharp[csRefOperators#49](../../../csharp/language-reference/operators/codesnippet/CSharp/assignment-operator_1.cs)]  
  
## <a name="see-also"></a>참고 항목

- [C# 참조](../../../csharp/language-reference/index.md)  
- [C# 프로그래밍 가이드](../../../csharp/programming-guide/index.md)  
- [C# 연산자](../../../csharp/language-reference/operators/index.md)
