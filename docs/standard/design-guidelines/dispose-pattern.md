---
title: 삭제 패턴
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- Dispose method
- class library design guidelines [.NET Framework], Dispose method
- class library design guidelines [.NET Framework], Finalize method
- customizing Dispose method name
- Finalize method
ms.assetid: 31a6c13b-d6a2-492b-9a9f-e5238c983bcb
author: KrzysztofCwalina
ms.openlocfilehash: ee6e9898ae93e2e6628eadec150a3c9c05f5d9c5
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53147719"
---
# <a name="dispose-pattern"></a>삭제 패턴
모든 프로그램 실행 하는 동안 메모리, 시스템 핸들 또는 데이터베이스 연결 같은 하나 이상의 시스템 리소스를 획득합니다. 개발자는 획득 되 고 사용 후 릴리스해야 합니다. 때문에 이러한 시스템 리소스를 사용할 때는 주의 해야 해야 합니다.  
  
 CLR 자동 메모리 관리에 대 한 지원을 제공합니다. 관리 되는 메모리 (C# 연산자를 사용 하 여 할당 된 메모리 `new`) 명시적으로 해제 될 필요가 없습니다. 가비지 수집기 (GC)에 의해 자동으로 해제 됩니다. 이 메모리를 해제 작업이 지루해 지 고 어려운 태스크에서 개발자를 해제 하 고는 전례 없는 생산성.NET Framework에서 제공 하는 주요 이유 중 하나 였습니다.  
  
 그러나 관리 되는 메모리 많은 시스템 리소스 종류 중 하나일 뿐입니다. 이외의 관리 되는 메모리 리소스는 여전히 명시적으로 해제 해야 하 고 관리 되지 않는 리소스 라고 합니다. GC 특별히 설계 되지 않았습니다 이러한 관리 되지 않는 리소스를 관리 하려면 관리 되지 않는 리소스를 관리 하는 것에 대 한 책임은 개발자의 손에 의미.  
  
 CLR 관리 되지 않는 리소스를 해제에 대 한 도움을 제공 합니다. <xref:System.Object?displayProperty=nameWithType> 가상 메서드를 선언 <xref:System.Object.Finalize%2A> (종료자 라고도 함)는 라고 GC가 개체의 메모리 GC에 의해 회수 되 고 관리 되지 않는 리소스를 해제 하도록 재정의할 수 있습니다. 종료자를 재정의 하는 종료 가능한 형식으로 참조 됩니다.  
  
 종료자 일부 정리 시나리오에서는 유효 하지만, 두 가지 중요 한 단점이 있습니다.  
  
-   종료자는 GC에서 개체 컬렉션에 대 한 자격이 있는 것을 감지 하면 호출 됩니다. 이 리소스를 더 이상 필요 하지 않은 후 결정 되지 않은 일정 기간 동안에 발생 합니다. 개발자의 수 또는 종료자에 의해 리소스가 실제로 해제 되는 경우 시간과 리소스를 해제 하려는 경우 사이의 지연을 또는 여러 부족 한 리소스는 리소스 (쉽게 소진 될 수 있습니다.)를 획득 하는 프로그램에서 허용 되지 않을 수 있습니다. 리소스 사용 (예: 관리 되지 않는 대용량 메모리 버퍼)을 유지 하려면 비용이 많이 들에 사례입니다.  
  
-   CLR에 종료자를 호출 해야 하는 경우 다음 가비지 컬렉션 (컬렉션 간에 실행 종료자)의 반올림 될 때까지 컬렉션 개체의 메모리를 연기 해야 합니다. 이 개체의 메모리 및 모든 개체 참조를 긴 시간 동안 해제 되지 것을 의미 합니다.  
  
 따라서 종료자에만 의존 하지 않을 또는 시나리오에는 성능이 매우 부족 한 리소스를 처리할 때 가능한 한 신속 하 게 관리 되지 않는 리소스를 회수 하는 경우 많은 시나리오에서 적절 한 추가 GC 오버 헤드 종료의 허용 되지 않습니다.  
  
 프레임 워크는 제공 된 <xref:System.IDisposable?displayProperty=nameWithType> 개발자 필요 하지 않은으로 관리 되지 않는 리소스를 해제 하는 수동 방법을 제공 하기 위해 구현 해야 하는 인터페이스입니다. 또한 제공 된 <xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType> GC 차이점을 확인할 수 있는 개체의 수동으로 삭제 된 메서드와 개체의 메모리를 이전 회수 될 수 있습니다이 경우 더 이상 종료 필요 하지 않습니다. 구현 하는 형식는 `IDisposable` 인터페이스는 삭제 가능한 형식 이라고 합니다.  
  
 Dispose 패턴을 사용 및 종료자의 구현을 표준화 됩니다 및 `IDisposable` 인터페이스입니다.  
  
 패턴의 주요 동기 부여는 구현의 복잡성을 줄이기 위해 합니다 <xref:System.Object.Finalize%2A> 하며 <xref:System.IDisposable.Dispose%2A> 메서드. 복잡성은 메서드 (차이점은 챕터의 뒷부분에 설명 됨) 하는 전부는 아니지만 일부 코드 경로 공유 하는 팩트에서 기인 합니다. 또한 결정적 리소스 관리에 대 한 언어 지원 개선과 관련 된 패턴의 일부 요소에 대 한 기록 이유가 있습니다.  
  
 **✓ DO** 삭제 가능한 형식은의 인스턴스를 포함 하는 형식에 기본 Dispose 패턴을 구현 합니다. 참조 된 [기본 Dispose 패턴](#basic_pattern) 기본 패턴에 대 한 자세한 내용은 섹션입니다.  
  
 형식이 다른 삭제 가능한 개체의 수명을 담당 하는 경우 개발자는 너무을 삭제 하는 방법을 해야 합니다. 컨테이너의를 사용 하 여 `Dispose` 메서드는이 가능 하 게 하는 편리한 방법입니다.  
  
 **✓ DO** 기본 Dispose 패턴을 구현 하 고 보유 중인 리소스를 명시적으로 해제 해야 하 고 종료자가 없는 형식에 종료자를 제공 합니다.  
  
 예를 들어 관리 되지 않는 메모리 버퍼를 저장 하는 형식에서 패턴을 구현 되어야 합니다. 합니다 [종료할 형식](#finalizable_types) 섹션 종료자를 구현 하는 데 관련 된 지침에 설명 합니다.  
  
 **✓ CONSIDER** 클래스에 직접 저장 하지 않으므로 관리 되지 않는 리소스 또는 삭제 가능한 개체 이지만 수행 하는 하위 종류가 가능성은 기본 Dispose 패턴을 구현 합니다.  
  
 이 좋은 예로 <xref:System.IO.Stream?displayProperty=nameWithType> 클래스. 모든 리소스를 포함 하지 않습니다 하는 추상 기본 클래스는 아니지만 대부분의 하위 클래스 및이 인해이 패턴을 구현 하 합니다.  
  
<a name="basic_pattern"></a>   
## <a name="basic-dispose-pattern"></a>기본 삭제 패턴  
 패턴의 기본 구현을 포함 합니다 `System.IDisposable` 를 선언 하는 인터페이스를 `Dispose(bool)` 간에 공유 하도록 모든 리소스 정리 논리를 구현 하는 메서드를 `Dispose` 메서드와 선택적 종료자.  
  
 다음 예제에서는 기본 패턴의 간단한 구현을 보여 줍니다.  
  
```csharp
public class DisposableResourceHolder : IDisposable {  
  
    private SafeHandle resource; // handle to a resource  
  
    public DisposableResourceHolder() {  
        this.resource = ... // allocates the resource  
    }  
  
    public void Dispose() {  
        Dispose(true);  
        GC.SuppressFinalize(this);  
    }  
  
    protected virtual void Dispose(bool disposing) {  
        if (disposing) {  
            if (resource!= null) resource.Dispose();  
        }  
    }  
}  
```  
  
 부울 매개 변수 `disposing` 에서 메서드를 호출한 여부를 나타냅니다는 `IDisposable.Dispose` 구현 또는 종료자에서. `Dispose(bool)` 구현을 다른 참조 개체 (예를 들어 이전 샘플의 리소스 필드)에 액세스 하기 전에 매개 변수를 확인 해야 합니다. 이러한 개체에서 메서드를 호출할 때에 액세스 해야 합니다 `IDisposable.Dispose` 구현 (때는 `disposing` 매개 변수는 true와 같음). 메서드가 종료자에서 호출 된 경우 (`disposing` 은 false)를 다른 개체는 액세스할 수 없습니다. 그 이유는 개체는 순서에 관계 없이 종료 하므로, 또는 해당 종속성 수 이미 종료 되었을 합니다.  
  
 또한이 섹션에서는 이미 삭제 패턴을 구현 하지 않는 기본 클래스에 적용 됩니다. 이미 패턴을 구현 하는 클래스에서 상속 하는 경우 재정의 하기만 합니다 `Dispose(bool)` 추가 리소스 정리 논리를 제공 하는 방법입니다.  
  
 **✓ DO** 선언는 `protected virtual void Dispose(bool disposing)` 관련 된 모든 논리를 중앙 집중화 메서드 관리 되지 않는 리소스를 해제 합니다.  
  
 이 메서드에서 모든 리소스 정리를 수행 합니다. 메서드가 모두 종료자에서 호출 되 고 `IDisposable.Dispose` 메서드. 매개 변수는 종료 자가 내에서 호출 되는 경우에 false 됩니다. 종료 하는 동안 실행 되는 모든 코드에는 다른 종료 가능한 개체에 액세스 하는 데 사용할 해야 합니다. 종료자를 구현 하는 다음 섹션에 나와 있습니다.  
  
```csharp
protected virtual void Dispose(bool disposing) {  
    if (disposing) {  
        if (resource!= null) resource.Dispose();  
    }  
}  
```  
  
 **✓ DO** 구현는 `IDisposable` 단순히 호출 하 여 인터페이스 `Dispose(true)` 이어서 `GC.SuppressFinalize(this)`합니다.  
  
 에 대 한 호출 `SuppressFinalize` 경우에 발생 해야 `Dispose(true)` 성공적으로 실행 합니다.  
  
```csharp
public void Dispose(){  
    Dispose(true);  
    GC.SuppressFinalize(this);  
}  
```  
  
 **X DO NOT** 매개 변수가 없는 확인 `Dispose` 가상 메서드.  
  
 `Dispose(bool)` 메서드는 서브 클래스에서 재정의 해야 합니다.  
  
```csharp
// bad design  
public class DisposableResourceHolder : IDisposable {  
    public virtual void Dispose() { ... }  
    protected virtual void Dispose(bool disposing) { ... }  
}  
  
// good design  
public class DisposableResourceHolder : IDisposable {  
    public void Dispose() { ... }  
    protected virtual void Dispose(bool disposing) { ... }  
}  
```  
  
 **X DO NOT** 모든 오버 로드의 선언 된 `Dispose` 이외의 다른 방법 `Dispose()` 및 `Dispose(bool)`합니다.  
  
 `Dispose` 이 패턴을 체계화 하 고 구현자, 사용자 및 컴파일러는 혼동을 방지 하기 위해 예약 된 단어를 고려 되어야 합니다. 일부 언어 특정 형식에이 패턴을 구현 자동으로 선택할 수 있습니다.  
  
 **✓ DO** 허용 된 `Dispose(bool)` 메서드를 두 번 이상 호출할 수 있습니다. 메서드는 첫 번째 호출 후 아무 작업도 하지 않도록 선택할 수 있습니다.  
  
```csharp
public class DisposableResourceHolder : IDisposable {  
  
    bool disposed = false;  
  
    protected virtual void Dispose(bool disposing) {  
        if (disposed) return;  
        // cleanup  
        ...  
        disposed = true;  
    }  
}  
```  
  
 **X AVOID** 내에서 예외를 throw `Dispose(bool)` 포함 하는 프로세스 손상 되어 중요 한 상황에 따라 제외 하 고 (누수, 일치 하지 않는 공유 상태 등.).  
  
 사용자가 기대 하는 호출 `Dispose` 예외가 발생 하지 것입니다.  
  
 경우 `Dispose` 예외를 발생 시킬 수 있습니다, finally 블록 정리 논리를 더 이상 실행 되지 것입니다. 이 해결 하려면 사용자에 대 한 모든 호출을 래핑할 해야 `Dispose` (내는 finally 블록!) try 블록에는 잠재 고객을 매우 복잡 한 정리 처리기입니다. 실행 하는 경우는 `Dispose(bool disposing)` 메서드를 삭제 하는 것이 false 예외가 throw 되지 않습니다. 이렇게 종료자 컨텍스트 내에서 실행 하는 경우 프로세스가 종료 됩니다.  
  
 **✓ DO** throw 한 <xref:System.ObjectDisposedException> 개체의 삭제 된 후에 사용할 수 없는 멤버에서.  
  
```csharp
public class DisposableResourceHolder : IDisposable {  
    bool disposed = false;  
    SafeHandle resource; // handle to a resource  
  
    public void DoSomething() {  
        if (disposed) throw new ObjectDisposedException(...);  
        // now call some native methods using the resource   
        ...  
    }  
    protected virtual void Dispose(bool disposing) {  
        if (disposed) return;  
        // cleanup  
        ...  
        disposed = true;  
    }  
}  
```  
  
 **✓ CONSIDER** 메서드를 제공 하 `Close()`, 외에 `Dispose()`, 영역에서 표준 용어 닫기 인지 합니다.  
  
 귀하에 게 중요 한 것이 작업을 수행 하는 경우는 `Close` 구현은 동일 `Dispose` 구현를 `IDisposable.Dispose` 메서드 명시적으로 합니다.  
  
```csharp
public class Stream : IDisposable {  
    IDisposable.Dispose() {  
        Close();  
    }  
    public void Close() {  
        Dispose(true);  
        GC.SuppressFinalize(this);  
    }  
}  
```  
  
<a name="finalizable_types"></a>   
## <a name="finalizable-types"></a>종료할 형식  
 종료 가능한 형식은 종료자를 재정의 하 고 종료 코드 경로 제공 하 여 기본 Dispose 패턴을 확장 하는 형식은 `Dispose(bool)` 메서드.  
  
 종료자는 주로 없기 때문에 시스템의 상태에 대 한 특정 (일반적으로 유효) 가정을 프로그램 실행 중에 올바르게 구현 하기가 매우 어렵습니다. 다음 지침 신중 하 게 고려해 야 합니다.  
  
 일부의 지침에만 적용는 `Finalize` 메서드를 코드에 있지만 종료자에서 호출 합니다. 기본 Dispose 패턴 이전에 정의 된 경우 즉, 내에서 실행 하는 논리 `Dispose(bool disposing)` 경우는 `disposing` 매개 변수가 false 인 합니다.  
  
 재정의 하지 않아야 함 기본 클래스 이미 종료을 기본 Dispose 패턴을 구현 하는 경우 `Finalize` 다시 합니다. 재정의 해야 하는 대신 방금는 `Dispose(bool)` 추가 리소스 정리 논리를 제공 하는 방법입니다.  
  
 다음 코드를 종료 가능 형식의 예를 보여 줍니다.  
  
```csharp
public class ComplexResourceHolder : IDisposable {  
  
    private IntPtr buffer; // unmanaged memory buffer  
    private SafeHandle resource; // disposable handle to a resource  
  
    public ComplexResourceHolder() {  
        this.buffer = ... // allocates memory  
        this.resource = ... // allocates the resource  
    }  
  
    protected virtual void Dispose(bool disposing) {  
        ReleaseBuffer(buffer); // release unmanaged memory  
        if (disposing) { // release other disposable objects  
            if (resource!= null) resource.Dispose();  
        }  
    }  
  
    ~ComplexResourceHolder() {
        Dispose(false);  
    }  
  
    public void Dispose() {
        Dispose(true);  
        GC.SuppressFinalize(this);  
    }  
}  
```  
  
 **X AVOID** 유형을 종료 가능 만드는 합니다.  
  
 종료 자가 필요 생각에 모든 사례를 신중 하 게 고려 합니다. 실제에는 성능 및 코드에 해당 하는 복잡성의 관점에서 종료자를 사용 하 여 인스턴스를 사용 하 여 관련 된 비용이 있습니다. 와 같은 리소스 래퍼를 사용 하는 것을 선호 <xref:System.Runtime.InteropServices.SafeHandle> 를 가능한 경우 관리 되지 않는 리소스를 캡슐화 하는 경우에 종료자 불필요 하 게 됩니다 래퍼 자체 리소스 정리 담당 하기 때문에 있습니다.  
  
 **X DO NOT** 값 형식을 개체로 확인 합니다.  
  
 실제로 참조 형식에만 CLR에서 종료 가져오기 하 고 값 형식에 종료자를 배치 하려고 하므로 무시 됩니다. C# 및 c + + 컴파일러는이 규칙을 적용 합니다.  
  
 **✓ DO** 형식이 자체 종료 자가 없는 관리 되지 않는 리소스를 해제 하는 일을 담당 하는 경우 종료 가능 형식을 확인 합니다.  
  
 종료자를 구현 하는 경우 호출 하기만 하면 됩니다 `Dispose(false)` 내에서 모든 리소스 정리 논리를 배치 합니다 `Dispose(bool disposing)` 메서드.  
  
```csharp
public class ComplexResourceHolder : IDisposable {  
  
    ~ComplexResourceHolder() {
        Dispose(false);  
    }  
  
    protected virtual void Dispose(bool disposing) {
        ...  
    }  
}  
```  
  
 **✓ DO** 줄어드는 경우 모든 형식에 대해 기본 Dispose 패턴을 구현 합니다.  
  
 이렇게 하면 형식의 사용자 명시적으로 종료자 담당 같은 리소스의 명확한 정리 작업을 수행할 수 있습니다.  
  
 **X DO NOT** 는 것은 이미 종료 되었을 상당한 위험 있기 때문에 종료 자가 코드 경로에 추가 된 줄어드는 경우 개체에 액세스 합니다.  
  
 예를 들어, 다른 종료 가능한 개체 B에 대 한 참조가 있는 종료 가능한 개체는 사용할 수 없습니다 안정적으로 B에서 A의 종료자 또는 그 반대의 경우도 마찬가지입니다. 종료자는 중요 한 종료에 대 한 약한 순서 보장) (짧은 임의의 순서로 호출 됩니다.  
  
 또한 정적 변수에 저장 된 개체 또는 프로세스를 종료 하는 응용 프로그램 도메인 언로드로 동안 특정 지점에서 수집 가져오기는 주의 합니다. 종료 가능한 개체 (또는 정적 변수에 저장 된 값을 사용할 수 있는 정적 메서드를 호출)를 가리키는 정적 변수 아닐 액세스 안전한 경우 <xref:System.Environment.HasShutdownStarted%2A?displayProperty=nameWithType> true를 반환 합니다.  
  
 **✓ DO** 확인 프로그램 `Finalize` 보호 된 메서드에 있습니다.  
  
 C#, c + + 및 VB.NET 개발자 필요가 없습니다이 대 한 걱정이 지침을 적용 하는 데 도움이 컴파일러 때문입니다.  
  
 **X DO NOT** 종료자 논리 시스템에 중요 한 오류를 제외 하 고 답변된 예외 이스케이프 합니다.  
  
 CLR (.NET Framework 버전 2.0)을 기준으로 전체 프로세스가 종료 됩니다 종료자에서 예외가 throw 되 면 실행 및 제어 된 방식으로 해제 되는 리소스에서 다른 종료자를 방지 합니다.  
  
 **✓ CONSIDER** 만들고 중요 한 종료 가능 개체를 사용 하 여 (포함 된 형식 계층 구조와 형식을 <xref:System.Runtime.ConstrainedExecution.CriticalFinalizerObject>)는 종료자 절대적으로 실행 해야 경우에 강제 응용 프로그램 도메인 언로드 및 스레드 상황에 대 한 중단합니다.  
  
 *Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*  
  
 *사용 권한에서 교육, inc. 피어슨 재인쇄 [Framework 디자인 지침: 다시 사용할 수 있는.NET 라이브러리, 2nd Edition에 대 한 규칙, 관용구 패턴과](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina를 Brad Abrams Addison Wesley Professional에서 2008 년 10 월 22 일 Microsoft Windows 개발 시리즈의 일부로 게시 합니다.*  
  
## <a name="see-also"></a>참고 항목

- <xref:System.IDisposable.Dispose%2A?displayProperty=nameWithType>  
- <xref:System.Object.Finalize%2A?displayProperty=nameWithType>  
- [프레임워크 디자인 지침](../../../docs/standard/design-guidelines/index.md)  
- [일반 디자인 패턴](../../../docs/standard/design-guidelines/common-design-patterns.md)  
- [가비지 수집](../../../docs/standard/garbage-collection/index.md)
