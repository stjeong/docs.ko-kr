---
title: 주요 변경 내용 및.NET 라이브러리
description: .NET 라이브러리를 만들 때의 주요 변경 내용 탐색 하기 위한 권장 사항을 사용 하는 것이 좋습니다.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 83c01fdad7d836877bf692b87eeb0230219ded36
ms.sourcegitcommit: fd8d4587cc26e53f0e27e230d6e27d828ef4306b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2018
ms.locfileid: "49370342"
---
# <a name="breaking-changes"></a>주요 변경 내용

기존 사용자에 대 한 안정성과 향후 혁신 간의 균형을 유지 하는.NET 라이브러리에 대 한 것입니다. 라이브러리 작성자가 리팩터링 및 코드를 완벽 한 것 하위 수준 라이브러리에 대 한 특히 저하에 기존 사용자가 중단 될 때까지 재고에 대해 배웁니다.

## <a name="project-types-and-breaking-changes"></a>프로젝트 형식 및 주요 변경 내용

.NET 커뮤니티에서 라이브러리 사용 방법의 주요 변경 내용 최종 사용자가 개발자에 게 미치는 변경 합니다.

* **낮음 및 중간 수준 라이브러리** serializer, HTML 파서, 데이터베이스 개체 관계형 매퍼 또는 웹 프레임 워크와 같은 가장 영향을 받는 주요 변경 내용으로 됩니다.

  구성 요소 패키지에는 NuGet 종속성으로 최종 사용자 응용 프로그램을 빌드하는 개발자 및 다른 라이브러리에서 사용 됩니다. 예를 들어, 응용 프로그램을 빌드하는 하 고 오픈 소스 클라이언트를 사용 하 여 웹 서비스를 호출 합니다. 주요 업데이트를 클라이언트에 사용 하 여 종속성은 해결할 수 있습니다. 변경 해야 하는 오픈 소스 클라이언트 이므로 없습니다 제어할 수 있습니다. 라이브러리의 호환 버전을 찾고 클라이언트 라이브러리에 대 한 수정은 제출 또는 새 버전에 대 한 대기 해야 합니다. 최악의 상황은 서로 호환 되지 않는 버전의 세 번째 라이브러리에 종속 된 두 개의 라이브러리를 사용 하려는 경우입니다.

* **고급 라이브러리** UI의 도구 모음과 같은 컨트롤은 주요 변경 내용에 덜 민감합니다.

  고급 라이브러리는 최종 사용자 응용 프로그램에서 직접 참조 됩니다. 주요 변경 될 경우, 개발자를 최신 버전으로 업데이트 하도록 선택할 수 또는 주요 변경에 맞게 응용 프로그램을 수정할 수 있습니다.

**✔️ 수행** 라이브러리 사용 방법에 대해 생각해 보세요. 미치는 주요 변경 내용 해야 응용 프로그램 및 사용 하는 라이브러리에서?

**✔️ 수행** 하위 수준.NET 라이브러리를 개발 하는 경우 주요 변경 내용을 최소화 합니다.

**✔️ 하십시오** 새 NuGet 패키지로 라이브러리의 주 버전을 게시를 다시 작성 합니다.

## <a name="types-of-breaking-changes"></a>형식의 주요 변경 내용

서로 다른 범주로 동일 하 게 영향력이 강한 되지 않으며는 주요 변경 내용.

### <a name="source-breaking-change"></a>원본 주요 변경 내용

주요 변경 내용 원본 프로그램 실행에 영향을 주지 않습니다 하지만 하면 컴파일 오류가 발생 다음에 응용 프로그램이 다시 컴파일됩니다. 예를 들어, 새 오버 로드 모호성을 이전에 모호한 되지 않는 메서드 호출에서 만들거나 이름이 바뀐된 매개 변수 명명 된 매개 변수를 사용 하는 호출자의 연결이 끊어집니다.

```csharp
public class Task
{
    // Adding a type called Task could conflict with System.Threading.Tasks.Task at compilation
}
```

개발자가 응용 프로그램을 다시 컴파일해야 하는 경우에 주요 변경 내용 소스는 해로운, 이므로 가장 방해가 적은 주요 변경 합니다. 개발자는 자신의 손상 된 소스 코드를 쉽게 해결할 수 있습니다.

### <a name="behavior-breaking-change"></a>주요 변경 내용 동작

동작 변경 내용은 가장 일반적인 유형의 주요 변경 내용: 동작 변경이 거의 모든 사용자가 손상 될 수 있습니다. 라이브러리를 변경 합니다, 메서드 서명, 예: 예외 발생, 입력 또는 출력 데이터 형식을 모두 부정적인 영향을 줄 수 라이브러리 소비자입니다. 사용자가 이전에 손상 된 동작에 의존 하는 경우 버그 수정도 주요 변경 내용으로 한정할 수 있습니다.

기능을 추가 하 고 잘못 된 동작을 개선 한 것 이지만 주의 하지 않고 수 있도록이 업그레이드를 기존 사용자에 대 한 매우 어렵습니다. 동작의 주요 변경 내용으로 처리 하는 개발자가 노력 하 고 한 가지 방법은 설정을 뒤 숨기려면 하는 것입니다. 개발자를에서 동시 옵트인 하거나 주요 변경 내용 옵트아웃 하도록 선택 하는 동안 라이브러리의 최신 버전으로 업데이트할 수 있습니다. 이 전략에는 개발자를 사용 중인 코드 시간이 지남에 따라 조정 하는 동안 최신 정보를 얻을 수 있습니다.

예를 들어, ASP.NET Core MVC는 개념을 [호환성 버전](/aspnet/core/mvc/compatibility-version) 수정 기능 활성화 및 비활성화 하는 `MvcOptions`합니다.

**✔️ 하십시오** 기존 사용자에 게 적용 되며 사용 하면 개발자가 설정 된 기능에 옵트인 하는 경우 새로운 기능을 기본적으로 종료 합니다.

### <a name="binary-breaking-change"></a>이진 주요 변경 내용

라이브러리의 공용 API를 변경할 때 발생 하는 주요 변경 내용 이진 파일, 라이브러리의 이전 버전은 더 이상 API를 호출할 수 있도록에 대해 컴파일된 어셈블리입니다. 예를 들어, 새 매개 변수를 추가 하 여 메서드의 시그니처를 변경 하면 throw 라이브러리의 이전 버전에 대해 컴파일된 어셈블리는 <xref:System.MissingMethodException>합니다.

주요 변경 내용 이진 파일에서 페이지 나누기 수는 **전체 어셈블리**합니다. 사용 하 여 어셈블리 이름 바꾸기 `AssemblyName` 추가, 제거 또는 변경 된 어셈블리의 강력한 이름 지정 키로 어셈블리의 id를 변경 됩니다. 어셈블리 id의 변경을 사용 하는 모든 컴파일된 코드가 중단 됩니다.

**❌ 하지** 어셈블리 이름을 변경 합니다.

**❌ 하지** 추가, 제거 또는 강력한 이름 키를 변경 합니다.

**✔️ 하십시오** 인터페이스 대신 추상 기본 클래스를 사용 합니다.

> 인터페이스에 아무것도 추가 하면 실패를 구현 하는 기존 형식입니다. 추상 기본 클래스를 사용 하면 기본 가상 구현을 추가할 수 있습니다.

**✔️ 것이 좋습니다** 배치는 <xref:System.ObsoleteAttribute> 형식 및 멤버를 제거 하려는에서 합니다. 코드를 업데이트 합니다. 더 이상 사용 되지 않는 API를 사용 하기 위한 지침은 가져야 합니다.

> 형식과 메서드를 호출 하는 코드는 <xref:System.ObsoleteAttribute> 특성에 제공 된 메시지와 함께 빌드 경고를 생성 합니다. 사용 되지 않는 API 노출 시간을 사용 하 여 대부분의 더 이상 사용 되지 않는 API가 제거 되 면 있도록 마이그레이션할 경고 제공 사람들 사용 합니다.

```csharp
public class Document
{
    [Obsolete("LoadDocument(string) is obsolete. Use LoadDocument(Uri) instead.")]
    public static Document LoadDocument(string uri)
    {
        return LoadDocument(new Uri(uri));
    }

    public static Document LoadDocument(Uri uri)
    {
        // Load the document
    }
}
```

## <a name="see-also"></a>참고자료

* [C# 개발자를 위한 버전 및 업데이트 고려 사항](../../csharp/whats-new/version-update-considerations.md)
* [.NET에서 API-주요 변경 내용에 대 한 명확한 지침](https://stackoverflow.com/questions/1456785/a-definitive-guide-to-api-breaking-changes-in-net)
* [CoreFX 주요 변경 규칙](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/breaking-change-rules.md)

>[!div class="step-by-step"]
[이전](./versioning.md)
