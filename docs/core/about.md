---
title: .NET 코어 정보 
description: Learn about .NET Core.
author: richlander
ms.author: mairaw
ms.date: 08/01/2018
---
# .NET 코어 정보

.NET Core는 다음과 같은 특징을 갖고 있습니다:

- **크로스플랫폼:** Windows, macOS, Linux [운영체제](https://github.com/dotnet/core/blob/master/os-lifecycle-policy.md)에서 구동됩니다.
- **아키텍쳐 일관성:** x64, x86, ARM을 포함한 다양한 아키텍쳐에서 코드가 똑같이 동작합니다.
- **명령줄 도구:** 로컬 개발환경과 지속적 통합 환경에서 쉽게 사용할 수 있는 명령줄 도구를 포함하고 있습니다.
- **유연한 개발:** 응용 프로그램에 포함되거나 유저 또는 시스템 전체에 격리된 채로 사용될 수 있습니다. [Docker 컨테이너](docker/index.md)와 함께 사용될 수 있습니다.
- **호환성:** .NET Core는 [.NET Standard](../standard/net-standard.md)를 통해 .NET Framework, Xamarin, Mono와 호환됩니다.
- **오픈 소스:** .NET Core 플랫폼은 오픈소스이고, MIT와 Apache 2 라이센스를 사용합니다. .NET Core는 [.NET 재단](https://dotnetfoundation.org/)의 프로젝트입니다.
- **Microsoft의 지원:** .NET Core는 [.NET Core Support](https://www.microsoft.com/net/core/support/)를 통해 Microsoft의 지원을 받습니다.

## 언어

C#, Visual Basic, F# 언어가 .NET Core로 응용 프로그램과 라이브러리를 작성하는 데 사용될 수 있습니다. 이 언어들은 [Visual Studio](https://visualstudio.microsoft.com/vs/), [Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp), Sublime Text, Vim 등 최고의 텍스트 에디터 또는 IDE에 통합되어 있거나 통합시킬 수 있습니다. 통합 중 일부는 [OmniSharp](http://www.omnisharp.net)와 [Ionide](https://ionide.io) 등 외부에서 제공됩니다.

## API

.NET Core는 많은 경우를 위해 API를 제공합니다. 그 예는 다음과 같습니다:

- 원시 타입들, 예를 들어 [bool][bool]과 [int][int]
- 컬렉션, 예를 들어 <xref:System.Collections.Generic.List%601?displayProperty=nameWithType>와 <xref:System.Collections.Generic.Dictionary%602?displayProperty=nameWithType>
- 유틸리티 타입들, 예를 들어 <xref:System.Net.Http.HttpClient?displayProperty=nameWithType>와 <xref:System.IO.FileStream?displayProperty=nameWithType>.
- 데이터 타입들, 예를 들어 <xref:System.Data.DataSet?displayProperty=nameWithType>과 [DbSet][dbset].
- 고성능 타입들, 예를 들어 <xref:System.Numerics.Vector?displayProperty=nameWithType>와 [Pipelines][pipelines].

.NET Core는 [.NET Standard](../standard/net-standard.md) 규격을 구현함으로서 .NET Framework와 Mono API 사이의 호환성을 제공합니다.

[bool]: https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/bool
[int]: https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/int
[pipelines]: https://blogs.msdn.microsoft.com/dotnet/2018/07/09/system-io-pipelines-high-performance-io-in-net/
[dbset]: https://www.nuget.org/packages/Microsoft.EntityFrameworkCore/

## 프레임워크

많은 프레임워크가 .NET Core로 만들어졌습니다:

- [ASP.NET Core](/aspnet/core/)
- [Windows 10 Universal Windows Platform (UWP)](https://developer/microsoft.com/windows)
- [Tizen](https://developer.tizen.org/development/training/.net-application)

## 구성

.NET Core는 다음 부분으로 구성되어 있습니다:

- [.NET Core 런타임](https://github.com/dotnet/coreclr)은 타입 시스템, 어셈블리 로딩, 가비지 컬렉터, 네이티브 명령어와 그 밖의 기본 서비스를 제공합니다. [.NET Core framework 라이브러리](https://github.com/dotnet/corefx)는 원시 데이터 타입, 응용 프로그램 구성 타입, 그리고 기본적인 유틸리티를 제공합니다.
- [ASP.NET 런타임](https://github.com/aspnet/home)은 현대적인 클라우드 기반의 인터넷 애플리케이션, 예를 들어 웹 앱, IoT 앱, 그리고 모바일 백엔드 개발을 위한 프레임워크를 제공합니다.
- [.NET Core CLI(명령줄 인터페이스) 도구](https://github.com/dotnet/cli)와 언어 컴파일러들([Roslyn](https://github.com/dotnet/roslyn)과 [F#](https://github.com/microsoft/visualfsharp))는 .NET Core 개발자 경험을 가능하게 합니다.
- [dotnet 도구](https://github.com/dotnet/core-setup)는 .NET Core 응용 프로그램과 CLI 도구를 실행하는데 사용됩니다. 런타임을 정하고 실행하며, 어셈블리 로딩 정책을 제공하고 응용 프로그램과 도구들을 실행합니다.

이 구성요소들은 다음 방법으로 배포됩니다:

- [.NET Core 런타임](https://www.microsoft.com/net/download/dotnet-core/2.1) -- .NET Core 런타임과 프레임워크 라이브러리들을 포함합니다.
- [ASP.NET Core 런타임](https://www.microsoft.com/net/download/dotnet-core/2.1) -- ASP.NET COre과 .NET Core 런타임과 프레임워크 라이브러리들을 포함합니다.
- [.NET COre SDK](https://www.microsoft.com/net/download/dotnet-core/2.1) -- .NET CLI 도구들, ASP.NET Core 런타임, .NET Core 런타임과 프레임워크를 포함합니다.

### 오픈 소스

[.NET Core](https://github.com/dotnet/core)는 오픈소스([MIT 라이센스](https://github.com/dotnet/core/blob/master/LICENSE.TXT))이며 2014년 Microsoft에 의해 [.NET 재단](https://dotnetfoundation.org)에 기여되었습니다. 지금은 .NET 재단에서 가장 활발한 프로젝트 중 하나입니다. 개인 및 회사에서 개인적, 학술적, 그리고 상업적 목적으로 자유롭게 사용될 수 있습니다. 많은 회사가 .NET Core를 응용 프로그램, 도구, 새로운 플랫폼과 호스팅 서비스의 일부로 사용합니다. 이 중 몇몇 회사는 GitHub에서 .NET Core에 중요한 기여를 했고, [.NET 재단 Technical Steering Group](https://dotnetfoundation.org/blog/tsg-welcome)에서 제품 방향에 가이던스를 제공합니다.

### 적응성을 위한 설계

.NET Core는 다른 .NET 제품들과 비슷하게 개발되었지만 상대적으로 독특합니다. .NET Core는 새로운 플랫폼과 워크로드에 대한 더 넓은 적응성을 갖도록 설계되었습니다. 여러 OS와 CPU로 이식되었고 이식 작업은 더욱 진행될 것입니다.

이 제품은 여러 부분으로 나뉘어 있어, 다양한 부분이 새 플랫폼에 따로 적용되도록 되어 있습니다. 런타임과 플랫폼 한정적인 기초 라이브러리들은 하나의 단위로 이식되어야 합니다. 플랫폼 중립적인 라이브러리들은 구조를 통해 있는 그대로 모든 플랫폼에서 작동해야 합니다. 프로젝트는 전체든 일부이든 개발자의 효율을 올리기 위해 플랫폼 한정적인 코드를 줄이고, 알고리즘이든 API든 플랫폼 중립적인 C# 코드를 선호하는 경향이 있습니다.

어떻게 .NET Core가 다양한 운영 체제를 지원하는가 하는 것은 자주 있는 질문입니다. 특히 구현이 분리되어 있는지 아니면 [조건부 컴파일](https://en.wikipedia.org/wiki/Conditional_compilation)이 사용되는지 자주 질문받습니다. 둘 모두 사용되고, 조건부 컴파일을 강하게 선호합니다.

아래의 차트에서 [CoreFX](https://github.com/dotnet/corefx)의 대부분이 모든 플랫폼에서 공유되는 플랫폼 중립적인 코드로 되어있다는 것을 알 수 있습니다. 플랫폼 중립적인 코드는 이식 가능한 하나의 어셈블리로 구현되어 모든 플랫폼에서 사용될 수 있습니다.

![CoreFX: 플랫폼 당 코드의 줄 수](../images/corefx-platforms-loc.png)

Windows와 Unix 구현은 크기가 거의 같습니다. [Microsoft.Win32.Registry](https://github.com/dotnet/corefx/tree/master/src/Microsoft.Win32.Registry)처럼 Windows에서만 제공되는 기능 때문에 Windows가 약간 더 큰 구현을 갖고 있지만 역시 많은 Unix만의 개념들은 포함되지 않습니다. 또 Linux와 macOS의 구현중 다수가 Unix 구현을 통해 공유되고, Linux와 macOS만의 구현은 거의 크기가 같은 것을 알 수 있습니다.

.NET Core에는 플랫폼 한정적인 라이브러리와 플랫폼 중립적인 라이브러리가 섞여있습니다. 몇가지 예제에서 이런 패턴을 볼 수 있습니다:

- [CoreCLR](https://github.com/dotnet/coreclr)은 플랫폼 한정적입니다. 메모리 관리자와 스레드 스케줄러 등은 OS의 하부 시스템 위에서 만들어져 있습니다.
- [System.IO](https://github.com/dotnet/corefx/tree/master/src/System.IO)와 [System.Security.Cryptography.Algorithms](https://github.com/dotnet/corefx/tree/master/src/System.Security.Cryptography.Algorithms)는 저장소와 암호학 API들이 각 OS마다 다르기 때문에 플랫폼 한정적입니다.
- [System.Collections](https://github.com/dotnet/corefx/tree/master/src/System.Collections)와 [System.Linq](https://github.com/dotnet/corefx/tree/master/src/System.Linq)는 플랫폼 중립적이며, 자료 구조를 생성하고 관리합니다.

## 다른 .NET 구현체와의 비교

.NET Core의 범위와 형태를 이해하려면 다른 .NET 구현체들과 비교하는 것이 가장 쉬울 것입니다.

### .NET Framework와의 비교

.NET은 Microsoft에 의해 2000년에 처음 소개되었고 진보해왔습니다. .NET Framework는 약 20년간 Microsoft에서 만들어진 .NET 구현체중 가장 우선되어 왔습니다.

.NET Core와 .NET Framework와의 주요 차이점은 다음과 같습니다:

- **App-models** -- .NET Core는 .NET Framework의 모든 app-model을 지원하지는 않습니다. 예를 들어 ASP.NET Web Forms와 MVC를 지원하지 않습니다. [.NET Core 3는 WPF와 Windows Forms를 지원](https://blogs.msdn.microsoft.com/dotnet/2018/05/07/net-core-3-and-support-for-windows-desktop-applications/)한다고 발표했습니다.
- **API** -- .NET Core는 .NET Framework Base Class 라이브러리의 많은 부분을 지원하지만 약간의 조정사항이 있습니다 (어셈블리 이름이 다릅니다; 일부 사례에서 타입에 드러난 멤버들이 다릅니다). 이런 차이점은 .NET Core로 소스를 이식할 때 바꿔야 합니다 ([microsoft/dotnet-apiport](https://github.com/microsoft/dotnet-apiport)를 참조하십시오). .NET Core는 [.NET Standard](../standard/net-standard.md) API 명세를 구현합니다.
- **하위 시스템** -- .NET Core는 .NET Framework의 하위 시스템들 중 일부를 구현하며, 더 간단한 구현과 프로그래밍 모델을 지향합니다. 예를 들어, Code Access Security (CAS)는 지원되지 않지만 리플렉션은 지원됩니다.
- **플랫폼** -- .NET Framework는 Windows와 Windows Server를 지원합니다. .NET Core는 macOS와 Linux도 지원합니다.
- **오픈 소스** -- .NET Core는 오픈소스입니다. [읽기만 허용되는 .NET Framework의 일부](https://github.com/microsoft/referencesource)는 오픈소스입니다.

.NET Core가 .NET Framework와 다른 .NET 구현체와 독특하고 중요한 차이점을 갖고 있긴 하지만 이들 구현체끼리는 소스를 사용하거나 바이너리를 공유하는 테크닉을 통해 공유하는 코드가 있는 것은 분명합니다.

### Mono와의 비교

[Mono](https://www.mono-project.com/)는 원래 크로스 플랫폼이며 [오픈 소스](https://github.com/mono/mono) .NET 구현체이며, 2004년 처음 발표되었습니다. .NET Framework의 커뮤니티 복제판이라고 생각할 수 있습니다. Mono 팀은 공개된 [.NET standards](https://github.com/dotnet/corclr/blob/master/Documentation/project-docs/dotnet-standards.md) (특히 ECMA 335)를 따르며 호환성 있는 구현을 위해 Microsoft에 의해 배포되었습니다.

.NET Core와 Mono의 주요 차이점은 다음과 같습니다:

- **App-model** -- Mono는 .NET Framework app-model의 일부를 지원하며 (예를 들어 Windows Forms) Xamarin 제품을 통해 추가적으로 지원하는 것들이 있습니다 (에를 들어 [Xamarin.iOS](https://www.xamarin.com/paltform)) .NET Core는 이것들은 지원하지 않습니다.
- **API** -- Mono는 .NET Framework API의 [많은 부분](https://docs.go-mono.com/?link=root%3a%2fclasslib)를 지원하며, 같은 어셈블리 이름과 구조를 사용합니다.
- **플랫폼** -- Mono는 많은 플랫폼과 CPU를 지원합니다.
- **오픈소스** -- Mono와 .NET Core는 둘 다 MIT 라이센스를 사용하고 .NET 재단의 프로젝트입니다.
- **지향점** -- 최근 몇 년간 Mono의 주요한 지향점은 모바일 플랫폼인 반면 .NET Core는 클라우드와 데스크탑 워크로드에 집중하고 있습니다.

