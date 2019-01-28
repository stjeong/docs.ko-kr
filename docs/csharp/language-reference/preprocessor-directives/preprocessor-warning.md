---
title: '#warning - C# 참조'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '#warning'
helpviewer_keywords:
- '#warning directive [C#]'
ms.assetid: e6fb496d-bb8b-4018-baf6-5b60a0c8902b
ms.openlocfilehash: 55768a354b2841021607ed40b4ef87b9767edcad
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54620320"
---
# <a name="warning-c-reference"></a>#warning(C# 참조)
`#warning`을 사용하면 코드의 특정 위치에서 [CS1030](../../misc/cs1030.md) 수준 1 컴파일러 경고를 생성할 수 있습니다. 예:  
  
```csharp
#warning Deprecated code in this method.  
```  
  
## <a name="remarks"></a>주의
 `#warning`은 일반적으로 조건부 지시문에 사용됩니다. [#error](../../../csharp/language-reference/preprocessor-directives/preprocessor-error.md)를 사용하여 사용자 정의 오류를 생성할 수도 있습니다.  
  
## <a name="example"></a>예제  

```csharp
// preprocessor_warning.cs  
// CS1030 expected  
#define DEBUG  
class MainClass
{  
    static void Main()
    {  
#if DEBUG  
#warning DEBUG is defined  
#endif  
    }  
}  
```  

## <a name="see-also"></a>참고 항목

- [C# 참조](../../../csharp/language-reference/index.md)
- [C# 프로그래밍 가이드](../../../csharp/programming-guide/index.md)
- [C# 전처리기 지시문](../../../csharp/language-reference/preprocessor-directives/index.md)
