---
title: 컴파일러 경고 CS3024
ms.date: 07/20/2015
f1_keywords:
- CS3024
helpviewer_keywords:
- CS3024
ms.assetid: fef9db31-9a7f-42d5-ad37-3e7faf661f95
ms.openlocfilehash: e49c131328f132ae6372167818d084df51ef6c78
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "56799463"
---
# <a name="compiler-warning-cs3024"></a>컴파일러 경고 CS3024
'type' 제약 조건 형식이 CLS 규격이 아닙니다.  
  
 CLS 규격이 아닌 형식을 제네릭 형식 제약 조건으로 사용하면 일부 언어에서 작성된 코드가 제네릭 클래스를 사용할 수 없으므로 컴파일러에서 이런 경고가 발생합니다.  
  
### <a name="to-eliminate-this-warning"></a>이 경고를 제거하려면  
  
1.  형식 제약 조건에 대해 CLS 규격 형식을 사용합니다.  
  
## <a name="example"></a>예제  
 다음 예제에서는 여러 위치에서 CS3024를 생성합니다.  
  
```csharp  
// cs3024.cs  
// Compile with: /target:library  
 [assembly: System.CLSCompliant(true)]  
  
[type: System.CLSCompliant(false)]  
public class TestClass // CS3024  
{  
    public ushort us;  
}  
[type: System.CLSCompliant(false)]  
public interface ITest // CS3024  
{}  
public interface I<T> where T : TestClass  
{}  
public class TestClass_2<T> where T : ITest  
{}  
public class TestClass_3<T> : I<T> where T : TestClass  
{}  
public class TestClass_4<T> : TestClass_2<T> where T : ITest  
{}  
public class Test  
{  
    public static int Main()  
    {  
        return 0;  
    }  
}  
```  
  
## <a name="see-also"></a>참고자료

- [형식 매개 변수에 대한 제약 조건](../../csharp/programming-guide/generics/constraints-on-type-parameters.md)
