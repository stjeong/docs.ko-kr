---
title: 강력한 이름 지정 및.NET 라이브러리
description: 강력한 이름 지정.NET 라이브러리에 대 한 권장 사항을 사용 하는 것이 좋습니다.
author: jamesnk
ms.author: mairaw
ms.date: 10/16/2018
ms.openlocfilehash: e3f7d443eb9acc84c800ea2611b803733085391c
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49372812"
---
# <a name="strong-naming"></a>강력한 이름 지정

강력한 이름 키 생성을 사용 하 여 어셈블리를 서명 가리킵니다를 [강력한 이름의 어셈블리](../../framework/app-domains/strong-named-assemblies.md)합니다. 강력한 이름의 어셈블리인 경우 이름 및 어셈블리 버전 번호를 기준으로 고유 id를 생성 및 어셈블리 충돌 되지 않도록 도와 줍니다.

강력한 이름 단점은 Windows에서.NET Framework 어셈블리는 강력한 이름이 지정 되 면 어셈블리의 엄격 하 게 로드 사용 하도록 설정 합니다. 강력한 이름의 어셈블리 참조를 개발자가 강제 적용 하는 어셈블리에서 참조 된 버전을 정확히 일치 해야 합니다 [바인딩 리디렉션을 구성](../../framework/configure-apps/redirect-assembly-versions.md) 어셈블리를 사용 하는 경우:

```xml
<configuration>
   <runtime>
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
         <dependentAssembly>
            <assemblyIdentity name="myAssembly" publicKeyToken="32ab4ba45e0a69a1" culture="neutral" />
            <bindingRedirect oldVersion="1.0.0.0" newVersion="2.0.0.0"/>
         </dependentAssembly>
      </assemblyBinding>
   </runtime>
</configuration>
```

.NET 개발자는 강력한 이름에 대 한 불만 제기 내용 해당 하는 일반적으로 불만족 때 엄격한 어셈블리를 로드 합니다. 다행 스럽게도이 문제는.NET Framework에 격리 되어 있습니다. .NET core, Xamarin, UWP 및 다른.NET 구현과 대부분의 엄격한 어셈블리 로드 없는 하 고 강력한 이름 지정의 주요 단점은 제거 합니다.

중요 한 측면의 강력한 이름 바 이럴 있다는 것입니다: 강력한 이름의 어셈블리 수만 참조 다른 강력한 이름의 어셈블리입니다. 라이브러리 라는 강력한 없는 경우 응용 프로그램이 나이 사용 하 여 강력한 이름 지정 해야 하는 라이브러리를 빌드하는 개발자를 제외가 있습니다.

강력한 이름 이점은 다음과 같습니다.

1. 어셈블리를 참조 하 고 다른 강력한 이름의 어셈블리에서 사용할 수 있습니다.
2. 어셈블리를 전역 어셈블리 캐시 (GAC)에 저장할 수 있습니다.
3. 어셈블리를 다른 버전의 어셈블리와 함께 로드할 수 있습니다. Side-by-side-어셈블리 로드 플러그 인 아키텍처를 사용 하 여 응용 프로그램에서 일반적으로 필요 합니다.

## <a name="create-strong-named-net-libraries"></a>.NET 라이브러리를 명명 된 강력한 만들려면

강력한 오픈 소스.NET 라이브러리 이름을 지정 해야 합니다. 강력한 이름의 어셈블리는 대부분의 사람들이 사용할 수 있습니다 하 고만 로드 하는 엄격한 어셈블리에.NET Framework에 영향을 확인 합니다.

> [!NOTE]
> 이 지침은 NuGet.org에 게시 된.NET 라이브러리와 같은 분산된 공개적으로.NET 라이브러리와 관련이 있습니다. 강력한 이름 지정 하는 대부분의.NET 응용 프로그램에 필요 하지 않은 및 기본적으로 실행 하지 않아야 합니다.

**✔️ 하십시오** 강력한 라이브러리의 어셈블리 이름을 지정 합니다.

**✔️ 하십시오** 소스 제어 시스템에 강력한 이름으로 사용 된 키를 확인 합니다.

> 공개 키를 수정 하 고 동일한 키를 사용 하 여 라이브러리 소스 코드를 다시 컴파일해야 하는 개발자를 수 있습니다.

> [!IMPORTANT]
> 원하는 것이 id를 암호화 하는 경우 [Authenticode](/windows-hardware/drivers/install/authenticode) 하 고 [NuGet 패키지 서명](/nuget/create-packages/sign-a-package) 는 것이 좋습니다. 강력한 이름 지정 해서는 안 보안 고려 사항에 대 한 합니다.

**✔️ 하십시오** 바인딩 리디렉션 및 업데이트 하는 빈도 줄일 수 있도록만 주 버전 변경 내용에 대해 어셈블리 버전 증분 합니다.

> 에 대해 자세히 알아보세요 [버전 관리 및 어셈블리 버전](./versioning.md#assembly-version)합니다.

**❌ 하지** 추가, 제거 또는 강력한 이름 키를 변경 합니다.

> 어셈블리의 강력한 이름 키를 수정 합니다. 어셈블리의 id를 변경 하 고 사용 하는 컴파일된 코드를 중단 합니다. 자세한 내용은 [주요 변경 내용 이진](./breaking-changes.md#binary-breaking-change)합니다.

**❌ 하지** 라이브러리의 강력한 이름을 지정 하 고 비-강력한 이름의 버전을 게시 합니다. 예를 들어 `Contoso.Api` 및 `Contoso.Api.StrongNamed`를 지정합니다.

> 두 개의 패키지 분기만 개발자 에코 시스템에 게시합니다. 또한 응용 프로그램 패키지를 모두에 따라 최종적으로 개발자는 형식 이름 충돌을 발생할 수 있습니다. .NET은 관련해 서 이러한는 다른 어셈블리의 다른 형식

>[!div class="step-by-step"]
[이전](./cross-platform-targeting.md)
[다음](./nuget.md)
