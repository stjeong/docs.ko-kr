---
title: .NET Core 3.0의 새로운 기능
description: .NET Core 3.0에 있는 새로운 기능에 대해 알아봅니다.
dev_langs:
- csharp
- vb
author: thraka
ms.author: adegeo
ms.date: 12/04/2018
ms.openlocfilehash: 3ca833031eb8bb0f43a334f833f2e0075842d57d
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53156671"
---
# <a name="whats-new-in-net-core-30-preview-1"></a>.NET Core 3.0(Preview 1)의 새로운 기능

이 문서에서는 .NET Core 3.0(Preview 1)의 새로운 기능에 대해 설명합니다. 가장 중요한 개선 사항 중 하나는 Windows 데스크톱 애플리케이션에 대한 지원(Windows만 해당)입니다. Windows 데스크톱이라는 .NET Core 3.0 구성 요소를 활용하여 Windows Forms WPF(Windows Presentation Foundation) 애플리케이션을 포팅할 수 있습니다. 분명히 말하지만, Windows 데스크톱 구성 요소는 Windows에서만 지원됩니다. 자세한 내용은 아래의 [Windows 데스크톱](#windows-desktop) 섹션을 참조하세요.

.NET Core 3.0에서는 C# 8.0에 대한 지원이 추가되었습니다.

Windows, Mac 및 Linux에서 지금 바로 [.NET Core 3 Preview 1을 다운로드하여 시작](https://aka.ms/netcore3download)하세요. [.NET Core 3 Preview 1 릴리스 정보](https://aka.ms/netcore3releasenotes)에서 자세한 릴리스 정보를 확인할 수 있습니다.

자세한 내용은 [.NET Core 3.0 Preview 1 알림](https://blogs.msdn.microsoft.com/dotnet/2018/12/04/announcing-net-core-3-preview-1-and-open-sourcing-windows-desktop-frameworks/)을 참조하세요.

## <a name="net-standard-21"></a>.NET Standard 2.1

.NET Core 3.0에서는 .NET Standard 2.1을 구현합니다.

## <a name="default-executables"></a>기본 실행 파일

이제 .NET Core에서 기본적으로 실행 파일을 빌드합니다. 이는 전역으로 설치된 .NET Core 버전을 사용하는 애플리케이션을 위한 새로운 기능입니다. 지금까지는 [자체 포함 배포](../deploying/index.md#self-contained-deployments-scd)에만 실행 파일이 있었습니다.

사용 중인 SDK의 환경 및 플랫폼과 일치하는 경우 `dotnet build` 또는 `dotnet publish` 중에 실행 파일이 생성됩니다. 다른 네이티브 실행 파일과 마찬가지로 이러한 실행 파일에서도 다음과 같은 동일한 기능을 예상할 수 있습니다.

* 실행 파일을 두 번 클릭할 수 있습니다.
* Windows의 `myapp.exe`, Linux 및 macOS의 `./myapp`과 같은 애플리케이션을 명령 프롬프트에서 직접 시작할 수 있습니다.

> [!NOTE]
> 다른 런타임 환경의 경우 `dotnet publish -r` 또는 `dotnet build -r` 인수를 통해 특정 런타임을 지정할 수 없습니다.

## <a name="build-copies-dependencies"></a>빌드 복사본 종속성

이제 `dotnet build`가 애플리케이션에 대한 NuGet 종속성을 NuGet 캐시에서 빌드 출력 폴더로 복사합니다. 이전에는 종속성이 `dotnet publish` 중에만 복사되었습니다. 

연결, Razor 페이지 게시 등 여전히 게시해야 하는 일부 작업이 있습니다.


## <a name="local-dotnet-tools"></a>로컬 dotnet 도구

.NET Core 2.1은 전역 도구를 지원한 한편, .NET Core 3.0은 이제 로컬 도구를 지원합니다. 로컬 도구는 전역 도구와 유사하지만 디스크의 특정 위치와 연결됩니다. 이를 통해 프로젝트별 및 리포지토리별 도구를 사용할 수 있습니다. 로컬로 설치된 도구는 전역으로 사용할 수 없습니다.

로컬 도구는 현재 디렉터리에 있는 매니페스트 파일 이름 `dotnet-tools.json`을 사용합니다. 이 매니페스트 파일은 사용 가능한 도구를 정의합니다. 리포지토리 루트에 이 매니페스트 파일을 만들면 코드를 복제하는 누구든지 성공적인 코드 작업에 필요한 도구를 복원하고 사용할 수 있습니다.

로컬 도구 매니페스트 파일을 사용할 수 있는 경우 다음 명령을 사용하여 해당 도구를 자동으로 다운로드하고 로컬에 설치합니다.

```console
dotnet tool restore
```

다음 명령을 사용하여 로컬 도구를 실행합니다.

```console
dotnet tool run <tool-command-name>
```

로컬 도구가 호출되면 dotnet은 디렉터리 구조 위로 매니페스트를 검색합니다. 도구 매니페스트 파일이 있으면 해당 파일에서 요청된 도구를 검색합니다. 도구가 발견되면 도구를 찾는 데 필요한 정보를 NuGet 전역 패키지 위치에 포함합니다. 

도구가 매니페스트에서 발견되었지만 캐시에 없는 경우 사용자에게 오류가 표시됩니다. 사용자에게 `dotnet tool restore`를 실행하도록 요청하기 위해 미리 보기 1 이후에 메시지가 개선될 예정입니다.

디렉터리에 로컬 도구를 추가하려면 먼저 도구 매니페스트 파일을 만들어야 합니다. dotnet 새 템플릿과 같은 도구 매니페스트 파일 생성 메커니즘이 미리 보기 1 이후에 제공될 예정입니다. 미리 보기 1에서는 다음 내용을 포함하는 `dotnet-tools.json` 파일을 만들어야 합니다.

```json
{
  "version": 1,
  "isRoot": true,
  "tools": {}
}
```

매니페스트가 생성되고 나면 다음을 사용하여 매니페스트에 로컬 도구를 추가할 수 있습니다.

```console
dotnet tool install <toolPackageId>
```

다른 버전을 지정하지 않을 경우 이 명령에 따라 최신 버전의 도구가 설치됩니다.  최신 버전이 자동으로 선택된 경우에도 올바른 버전의 도구를 복원 또는 실행할 수 있도록 도구 버전이 도구 매니페스트 파일에 기록됩니다.

도구 매니페스트 파일은 리포지토리 작업에 필요한 버전 업데이트 등을 위한 수동 편집을 허용하도록 설계되었습니다.

예제 `dotnet-tools.json` 파일은 다음과 같습니다.

```json
{
  "version": 1,
  "isRoot": true,
  "tools": {
    "dotnetsay": {
      "version": "2.1.4",
      "commands": [
        "dotnetsay"
      ]
    },
    "t-rex": {
      "version": "1.0.103",
      "commands": [
        "t-rex"
      ]
    }
  }
}
```

도구 매니페스트 파일에서 도구를 제거하려면 다음 명령을 실행합니다.

```console
dotnet tool uninstall <toolPackageId>
```

전역 도구와 로컬 도구 둘 다, 호환되는 버전의 런타임이 필요합니다. 현재 NuGet.org의 많은 도구는 .NET Core 런타임 2.1을 대상으로 합니다. 이러한 도구를 전역 또는 로컬로 설치하려면 여전히 [NET Core 2.1 런타임](https://dotnet.microsoft.com/download/dotnet-core/2.1)을 설치해야 합니다.

자세한 내용은 [Local Tools Early Preview Documentation](https://github.com/dotnet/cli/issues/10288)(로컬 도구 초기 미리 보기 문서)을 참조하세요.

## <a name="windows-desktop"></a>Windows 바탕 화면

.NET Core 3.0 Preview 1부터 WPF 및 Windows Forms를 사용하여 Windows 데스크톱 애플리케이션을 빌드할 수 있습니다. 이러한 프레임워크는 [XAML 아일랜드](/windows/uwp/xaml-platform/xaml-host-controls)를 통해 Windows UI XAML 라이브러리(WinUI)의 최신 컨트롤 및 Fluent 스타일을 사용하는 것도 지원합니다.

Windows 데스크톱 구성 요소는 Windows .NET Core 3.0 SDK의 일부입니다.

다음 `dotnet` 명령을 사용하여 새 WPF 또는 Windows Forms 앱을 만들 수 있습니다.

```console
dotnet new wpf
dotnet new winforms
```

Visual Studio 2019 Preview 1에서 .NET Core 3.0 WPF 및 Windows Forms 프로젝트를 열고 시작 및 디버그할 수도 있습니다. 현재 Visual Studio 2017 15.9에서 이러한 프로젝트를 열 수 있지만 지원되는 시나리오는 아니며, [미리 보기를 사용](https://blogs.msdn.microsoft.com/dotnet/2018/11/13/net-core-tooling-update-for-visual-studio-2017-version-15-9/)하도록 설정해야 합니다.

새 프로젝트는 몇 가지 내용만 추가되고, 기존 .NET Core 프로젝트와 동일합니다. 기본 .NET Core 콘솔 프로젝트와 기본 Windows Forms 및 WPF 프로젝트의 비교는 다음과 같습니다.

.NET Core 콘솔 프로젝트에서 프로젝트는 `Microsoft.NET.Sdk` SDK를 사용하고 `netcoreapp3.0` 대상 프레임워크를 통해 .NET Core 3.0에 대한 종속성을 선언합니다. Windows 데스크톱 앱을 만들려면 `Microsoft.NET.Sdk.WindowsDesktop` SDK를 사용하고, 사용할 UI 프레임워크를 선택합니다.

```diff
-<Project Sdk="Microsoft.NET.Sdk">
+<Project Sdk="Microsoft.NET.Sdk.WindowsDesktop">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp3.0</TargetFramework>
+   <UseWPF>true</UseWPF>
  </PropertyGroup>
</Project>
```

WPF가 아닌 Windows Forms를 선택하려면 `UseWPF` 대신 `UseWindowsForms`를 설정합니다.

```diff
<Project Sdk="Microsoft.NET.Sdk.WindowsDesktop">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp3.0</TargetFramework>
-   <UseWPF>true</UseWPF>
+   <UseWindowsForms>true</UseWindowsForms>
  </PropertyGroup>
</Project>
```

앱이 두 프레임워크를 모두 사용하는 경우(예: Windows Forms 대화 상자에서 WPF 컨트롤을 호스트하는 경우) `UseWPF` 및 `UseWindowsForms`를 둘 다 `true`로 설정할 수 있습니다.

[dotnet/winforms](https://github.com/dotnet/winforms/issues),  [dotnet/wpf](https://github.com/dotnet/wpf/issues) 및 [dotnet/core](https://github.com/dotnet/core/issues) 리포지토리에서 피드백을 공유하세요.

## <a name="fast-built-in-json-support"></a>빠른 기본 제공 JSON 지원

`System.Text.Json.Utf8JsonReader`는 `ReadOnlySpan<byte>`에서 읽어온 UTF-8 인코드된 JSON 텍스트를 위한 고성능, 저할당, 전달 전용 판독기입니다. `Utf8JsonReader`는 사용자 지정 구문 분석기 및 역직렬 변환기를 빌드하는 데 활용할 수 있는 하위 수준의 기초 형식입니다. 새 `Utf8JsonReader`를 사용하여 JSON 페이로드를 읽을 경우 [Json.NET](https://www.newtonsoft.com/json)의 판독기를 사용하는 것에 비해 2배 더 빠릅니다. JSON 토큰을 (UTF-16) 문자열로 실현해야 할 때까지 할당하지 않습니다.

이 새로운 API에는 다음 구성 요소가 포함됩니다.

* 미리 보기 1: JSON 판독기(순차적 액세스)
* 향후 제공 예정: JSON 기록기, DOM(임의 액세스), poco 직렬 변환기, poco 역직렬 변환기

시작점으로 사용할 수 있는 `Utf8JsonReader`의 기본 판독기 루프는 다음과 같습니다.

```csharp
using System.Text.Json;

public static void Utf8JsonReaderLoop(ReadOnlySpan<byte> dataUtf8)
{
    var json = new Utf8JsonReader(dataUtf8, isFinalBlock: true, state: default);

    while (json.Read())
    {
        JsonTokenType tokenType = json.TokenType;
        ReadOnlySpan<byte> valueSpan = json.ValueSpan;
        switch (tokenType)
        {
            case JsonTokenType.StartObject:
            case JsonTokenType.EndObject:
                break;
            case JsonTokenType.StartArray:
            case JsonTokenType.EndArray:
                break;
            case JsonTokenType.PropertyName:
                break;
            case JsonTokenType.String:
                string valueString = json.GetStringValue();
                break;
            case JsonTokenType.Number:
                if (!json.TryGetInt32Value(out int valueInteger))
                {
                    throw new FormatException();
                }
                break;
            case JsonTokenType.True:
            case JsonTokenType.False:
                bool valueBool = json.GetBooleanValue();
                break;
            case JsonTokenType.Null:
                break;
            default:
                throw new ArgumentException();
        }
    }

    dataUtf8 = dataUtf8.Slice((int)json.BytesConsumed);
    JsonReaderState state = json.CurrentState;
}
```

.NET 에코시스템은 [Json.NET](https://www.newtonsoft.com/json) 및 여전히 유용한 기타 인기 있는 JSON 라이브러리를 사용해 왔습니다. Json.NET는 내부적으로 UTF-16인 .NET 문자열을 기본 데이터 형식으로 사용합니다. 

.NET Core 2.1 및 3.0에서는 `Span<T>` 및 UTF-8 문자열 사용을 기준으로 훨씬 적은 메모리가 필요하며 Kestrel, ASP.NET Core 웹 서버와 같은 처리량이 높은 애플리케이션 요구의 처리가 개선된 JSON API(예: `Utf8JsonReader`)를 작성할 수 있는 새로운 API가 추가되었습니다.

## <a name="ranges-and-indices"></a>범위 및 인덱스

새 `Index` 형식을 인덱싱에 사용할 수 있습니다. 시작부터 계산되는 `int`의 인덱스를 만들거나, 접두사 `^` 연산자(C#)를 사용하여 끝부터 계산되는 인덱스를 만들 수 있습니다.

```csharp
Index i1 = 3;  // number 3 from beginning
Index i2 = ^4; // number 4 from end
int[] a = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
Console.WriteLine($"{a[i1]}, {a[i2]}"); // "3, 6"
```

시작 인덱스와 끝 인덱스의 두 `Index` 값으로 구성되고 `x..y` 범위 식(C#)으로 작성할 수 있는 `Range` 유형도 있습니다. 조각을 생성하기 위해 `Range`를 사용하여 인덱싱할 수 있습니다.

```csharp
var slice = a[i1..i2]; // { 3, 4, 5 }
```

> [!NOTE]
> [C# 8.0](https://blogs.msdn.microsoft.com/dotnet/2018/11/12/building-c-8-0/)에서만 `Range` 및 `Index` 구문을 지원합니다.

## <a name="async-streams"></a>비동기 스트림

`IAsyncEnumerable<T>` 형식은 `IEnumerable<T>`의 새로운 비동기 버전입니다. 이 언어에서는 `await foreach`을 통해 해당 요소를 사용하고, `yield return`을 통해 요소를 생성할 수 있습니다.

다음 예제에서는 비동기 스트림의 생성 및 사용을 둘 다 보여 줍니다. `foreach` 문은 비동기이며, `yield return`을 사용하여 호출자에 대한 비동기 스트림을 생성합니다. 이 패턴(`yield return` 사용)은 비동기 스트림 생성을 위한 권장 모델입니다.

```csharp
async IAsyncEnumerable<int> GetBigResultsAsync()
{
    await foreach (var result in GetResultsAsync())
    {
        if (result > 20) yield return result; 
    }
}
```

> [!WARNING]
> .NET Core 3.0 Preview 1에는 현재 `await foreach` 관련 버그가 있습니다. 대신, `GetEnumerator` 및 `MoveNext`를 사용하여 요소를 처리합니다. 자세한 내용은 [roslyn/#31268](https://github.com/dotnet/roslyn/issues/31268)을 참조하세요.

`await foreach`를 수행할 수 있을 뿐 아니라, 비동기 반복기(예: `await` 및 `yield`가 둘 다 가능한 `IAsyncEnumerable/IAsyncEnumerator`를 반환하는 반복기)를 만들 수도 있습니다. 삭제해야 하는 개체의 경우 `Stream` 및 `Timer`와 같은 다양한 BCL 유형이 구현하는 `IAsyncDisposable`을 사용할 수 있습니다.

> [!NOTE]
> [C# 8.0](https://blogs.msdn.microsoft.com/dotnet/2018/11/12/building-c-8-0/)에서만 `await foreach` 구문을 지원합니다.

## <a name="type-sequencereader"></a>형식: SequenceReader

.NET Core 3.0에서는 `ReadOnlySequence<T>`용 판독기로 사용할 수 있는 `System.Buffers.SequenceReader`가 추가되었습니다. 이를 통해 여러 지원 버퍼에 걸쳐 있을 수 있는 `System.IO.Pipelines` 데이터의 고성능, 저할당 구문 분석이 가능합니다. 

다음 예제에서는 입력 `Sequence`를 유효한 `CR/LF` 구분 줄로 분석합니다.

```csharp
private static ReadOnlySpan<byte> CRLF => new byte[] { (byte)'\r', (byte)'\n' };

public static void ReadLines(ReadOnlySequence<byte> sequence)
{
    SequenceReader<byte> reader = new SequenceReader<byte>(sequence);

    while (!reader.End)
    {
        if (!reader.TryReadToAny(out ReadOnlySpan<byte> line, CRLF, advancePastDelimiter:false))
        {
            // Couldn't find another delimiter
            // ...
        }

        if (!reader.IsNext(CRLF, advancePast: true))
        {
            // Not a good CR/LF pair
            // ...
        }

        // line is valid, process
        ProcessLine(line);
    }
}
```

## <a name="type-metadataloadcontext"></a>형식: MetadataLoadContext

호출자의 애플리케이션 도메인에 영향을 주지 않고 어셈블리 메타데이터를 읽을 수 있도록 하는 `MetadataLoadContext` 형식이 추가되었습니다. 현재 런타임 환경과 다른 아키텍처 및 플랫폼용으로 빌드된 어셈블리를 포함하여, 어셈블리는 데이터로 읽힙니다. `MetadataLoadContext`는 .NET Framework에서만 사용할 수 있는 <xref:System.Reflection.Assembly.ReflectionOnlyLoad*>와 겹칩니다.

`MetdataLoadContext`는 [System.Reflection.MetadataLoadContext 패키지](https://www.nuget.org/packages/System.Reflection.MetadataLoadContext)에서 사용할 수 있습니다. .NET Standard 2.0 패키지입니다.

`MetadataLoadContext`는 <xref:System.Runtime.Loader.AssemblyLoadContext> 형식과 마찬가지로 API를 노출하지만 해당 형식을 기반으로 하지 않습니다. <xref:System.Runtime.Loader.AssemblyLoadContext>와 마찬가지로, `MetadataLoadContext`를 사용하면 격리된 어셈블리 로드 Universe 내에서 어셈블리를 로드할 수 있습니다. `MetdataLoadContext` API는 <xref:System.Reflection.Assembly> 개체를 반환하여 익숙한 리플렉션 API를 사용할 수 있도록 합니다. [MethodBase.Invoke](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/src/System/Reflection/TypeLoading/Methods/RoMethod.cs#L127) 등의 실행 지향 API는 허용되지 않으며 InvalidOperationException을 throw합니다.

다음 샘플은 지정된 인터페이스를 구현하는 어셈블리에서 구체적인 형식을 찾는 방법을 보여 줍니다.

```csharp
var paths = new string[] {@"C:\myapp\mscorlib.dll", @"C:\myapp\myapp.dll"};
var resolver = new PathAssemblyResolver(paths);
using (var lc = new MetadataLoadContext(resolver))
{
    Assembly a = lc.LoadFromAssemblyName("myapp");
    Type myInterface = a.GetType("MyApp.IPluginInterface");
    foreach (Type t in a.GetTypes())
    {
        if (t.IsClass && myInterface.IsAssignableFrom(t))
            Console.WriteLine($"Class {t.FullName} implements IPluginInterface");
    }
}
```

`MetadataLoadContext`에 대한 시나리오에는 어셈블리 세트를 데이터로 검사하고, 검사가 수행된 후 모든 파일 잠금 및 메모리가 해제되어야 하는 디자인 타임 기능, 빌드 타임 도구 및 런타임 강화 기능이 포함됩니다.

`MetadataLoadContext`에는 생성자에게 전달되는 확인자 클래스가 있습니다. 확인자의 작업은 `AssemblyName`이 제공될 경우 `Assembly`를 로드하는 것입니다. 확인자 클래스는 추상 `MetadataAssemblyResolver` 클래스에서 파생됩니다. 경로 기반 시나리오에 대한 확인자 구현은 `PathAssemblyResolver`를 사용하여 제공됩니다.

[MetadataLoadContext 테스트](https://github.com/dotnet/corefx/tree/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests)는 많은 사용 사례를 보여 줍니다. [어셈블리 테스트](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests/Assembly/AssemblyTests.cs)에서 시작하는 것이 좋습니다.

## <a name="tls-13--openssl-111-on-linux"></a>Linux의 TLS 1.3 및 OpenSSL 1.1.1

이제 .NET Core는 지정된 환경에서 사용 가능한 경우 [OpenSSL 1.1.1의 TLS 1.3 지원](https://www.openssl.org/blog/blog/2018/09/11/release111/)을 이용합니다. [OpenSSL 팀](https://www.openssl.org/blog/blog/2018/09/11/release111/)을 기준으로, TLS 1.3의 여러 가지 혜택이 있습니다.

* 클라이언트와 서버 간에 필요한 왕복 횟수가 감소하여 연결 시간이 향상되었습니다.

* 사용되지 않는 다양한 비보안 암호화 알고리즘이 제거되고 연결 핸드셰이크가 더 많이 암호화되어 보안이 개선되었습니다.

.NET Core 3.0 Preview 1은 **OpenSSL 1.1.1**, **OpenSSL 1.1.0** 또는 **OpenSSL 1.0.2**(Linux 시스템에서 발견된 가장 적합한 버전)를 활용할 수 있습니다.  **OpenSSL 1.1.1**이 사용 가능한 경우 SslStream 및 HttpClient 형식은 클라이언트와 서버가 둘 다 **TLS 1.3**을 지원할 경우 `SslProtocols.None`(시스템 기본 프로토콜)을 사용할 때 **TLS 1.3**을 사용합니다.

다음 샘플은 <https://www.cloudflare.com>에 연결하는 Ubuntu 18.10의 .NET Core 3.0 Preview 1을 보여 줍니다.

```csharp
using System;
using System.Net.Security;
using System.Net.Sockets;
using System.Threading.Tasks;

namespace tlstest
{
    class Program
    {
        static async Task Main()
        {
            using (TcpClient tcpClient = new TcpClient())
            {
                string targetHost = "www.cloudflare.com";

                await tcpClient.ConnectAsync(targetHost, 443);

                using (SslStream sslStream = new SslStream(tcpClient.GetStream()))
                {
                    await sslStream.AuthenticateAsClientAsync(targetHost);
                    await Console.Out.WriteLineAsync($"Connected to {targetHost} with {sslStream.SslProtocol}");
                }
            }
        }
    }
}
```

```console
user@comp-ubuntu1810:~/tlstest$ dotnet run
Connected to www.cloudflare.com with Tls13
user@comp-ubuntu1810:~/tlstest$ openssl version
OpenSSL 1.1.1  11 Sep 2018
```

>[!IMPORTANT]
>Windows 및 macOS에서는 아직 **TLS 1.3**을 지원하지 않습니다. 지원이 제공되면 .NET Core 3.0은 이러한 운영 체제에서 **TLS 1.3**을 지원합니다.

## <a name="cryptography"></a>암호화

`System.Security.Cryptography.AesGcm` 및 `System.Security.Cryptography.AesCcm`을 통해 구현된 **AES-GCM** 및 **AES-CCM** 암호에 대한 지원이 추가되었습니다. 이러한 알고리즘은 [AEAD(연결 데이터를 사용한 인증된 암호화) 알고리즘](https://en.wikipedia.org/wiki/Authenticated_encryption)이자, .NET Core에 추가된 최초의 AE(인증된 암호화) 알고리즘입니다.

다음 코드는 **AesGcm** 암호를 사용하여 임의 데이터를 암호화하고 암호를 해독하는 방법을 보여 줍니다.

**AesCcm**에 대한 코드는 거의 동일하게 표시됩니다(클래스 변수 이름만 다름)

```csharp
// key should be: pre-known, derived, or transported via another channel, such as RSA encryption
byte[] key = new byte[16];
RandomNumberGenerator.Fill(key);

byte[] nonce = new byte[12];
RandomNumberGenerator.Fill(nonce);

// normally this would be your data
byte[] dataToEncrypt = new byte[1234];
byte[] associatedData = new byte[333];
RandomNumberGenerator.Fill(dataToEncrypt);
RandomNumberGenerator.Fill(associatedData);

// these will be filled during the encryption
byte[] tag = new byte[16];
byte[] ciphertext = new byte[dataToEncrypt.Length];

using (AesGcm aesGcm = new AesGcm(key))
{
    aesGcm.Encrypt(nonce, dataToEncrypt, ciphertext, tag, associatedData);
}

// tag, nonce, ciphertext, associatedData should be sent to the other part

byte[] decryptedData = new byte[ciphertext.Length];

using (AesGcm aesGcm = new AesGcm(key))
{
    aesGcm.Decrypt(nonce, ciphertext, tag, decryptedData, associatedData);
}

// do something with the data
// this should always print that data is the same
Console.WriteLine($"AES-GCM: Decrypted data is{(dataToEncrypt.SequenceEqual(decryptedData) ? "the same as" : "different than")} original data.");
```

## <a name="cryptographic-key-importexport"></a>암호화 키 가져오기/내보내기

.NET Core 3.0 Preview 1은 X.509 인증서를 사용하지 않고도 표준 형식에서 비대칭 공개 키와 개인 키를 가져오고 내보낼 수 있도록 지원합니다.

모든 키 유형(RSA, DSA, ECDsa, ECDiffieHellman)은 공개 키에 대한 **X.509 SubjectPublicKeyInfo** 형식과 개인 키에 대한 **PKCS#8 PrivateKeyInfo** 및 **PKCS#8 EncryptedPrivateKeyInfo** 형식을 지원합니다. RSA는 **PKCS#1 RSAPublicKey** 및 **PKCS#1 RSAPrivateKey**를 추가로 지원합니다. 내보내기 메서드는 모두 DER로 인코드된 이진 데이터를 생성하고, 가져오기 메서드도 동일한 동작을 예상합니다. 키가 텍스트에 편리한 PEM 형식으로 저장된 경우 호출자는 가져오기 메서드를 호출하기 전에 콘텐츠를 base64로 디코드해야 합니다.

```csharp
using System;
using System.IO;
using System.Security.Cryptography;

namespace rsakeyprint
{
    class Program
    {
        static void Main(string[] args)
        {
            using (RSA rsa = RSA.Create())
            {
                byte[] keyBytes = File.ReadAllBytes(args[0]);
                rsa.ImportRSAPrivateKey(keyBytes, out int bytesRead);
 
                Console.WriteLine($"Read {bytesRead} bytes, {keyBytes.Length-bytesRead} extra byte(s) in file.");
                RSAParameters rsaParameters = rsa.ExportParameters(true);
                Console.WriteLine(BitConverter.ToString(rsaParameters.D));
            }
        }
    }
}
```

```console
user@comp-ubuntu1810:~/rsakeyprint$ echo Making a small key to save on screen space.
Making a small key to save on screen space.
user@comp-ubuntu1810:~/rsakeyprint$ openssl genrsa 768 | openssl rsa -outform der -out rsa.key
Generating RSA private key, 768 bit long modulus (2 primes)
..+++++++
........+++++++
e is 65537 (0x010001)
writing RSA key
user@comp-ubuntu1810:~/rsakeyprint$ dotnet run rsa.key
Read 461 bytes, 0 extra byte(s) in file.
0F-D0-82-34-F8-13-38-4A-7F-C7-52-4A-F6-93-F8-FB-6D-98-7A-6A-04-3B-BC-35-8C-7D-AC-A5-A3-6E-AD-C1-66-30-81-2C-2A-DE-DA-60-03-6A-2C-D9-76-15-7F-61-97-57-
79-E1-6E-45-62-C3-83-04-97-CB-32-EF-C5-17-5F-99-60-92-AE-B6-34-6F-30-06-03-AC-BF-15-24-43-84-EB-83-60-EF-4D-3B-BD-D9-5D-56-26-F0-51-CE-F1
user@comp-ubuntu1810:~/rsakeyprint$ openssl rsa -in rsa.key -inform der -text -noout | grep -A7 private
privateExponent:
    0f:d0:82:34:f8:13:38:4a:7f:c7:52:4a:f6:93:f8:
    fb:6d:98:7a:6a:04:3b:bc:35:8c:7d:ac:a5:a3:6e:
    ad:c1:66:30:81:2c:2a:de:da:60:03:6a:2c:d9:76:
    15:7f:61:97:57:79:e1:6e:45:62:c3:83:04:97:cb:
    32:ef:c5:17:5f:99:60:92:ae:b6:34:6f:30:06:03:
    ac:bf:15:24:43:84:eb:83:60:ef:4d:3b:bd:d9:5d:
    56:26:f0:51:ce:f1
```

PKCS#8 파일은 `System.Security.Cryptography.Pkcs.Pkcs8PrivateKeyInfo` 클래스를 통해 검사할 수 있습니다.

PFX/PKCS#12 파일은 각각 `System.Security.Cryptography.Pkcs.Pkcs12Info` 및 `System.Security.Cryptography.Pkcs.Pkcs12Builder`를 통해 검사하고 조작할 수 있습니다.

## <a name="serialport-for-linux"></a>Linux용 SerialPort

.NET Core 3.0은 이제 Linux에서 <xref:System.IO.Ports.SerialPort?displayProperty=nameWithType>을 지원합니다.

이전에는 .NET Core가 Windows에서만 `SerialPort` 형식 사용을 지원했습니다.

## <a name="more-bcl-improvements"></a>더 많은 BCL 개선 사항

.NET Core 2.1에서 도입된 `Span<T>`, `Memory<T>` 및 관련 형식이 .NET Core 3.0에서 최적화되었습니다. 이제 범위 구성, 조각화, 구문 분석, 서식 지정과 같은 일반적인 작업의 성능이 향상됩니다. 

또한 `String` 등의 형식이 내부적으로 개선되어, `Dictionary<TKey, TValue>` 및 기타 컬렉션에서 키로 사용할 때 보다 효율적으로 작동합니다. 코드 변경 없이도 이러한 개선 사항을 활용할 수 있습니다.

또한 다음 개선 사항이 .NET Core 3 Preview 1에서 새로 도입되었습니다.

* HttpClient에 기본 제공되는 Brotli 지원
* ThreadPool.UnsafeQueueWorkItem(IThreadPoolWorkItem)
* Unsafe.Unbox
* CancellationToken.Unregister
* 복합 산술 연산자
* TCP 연결 유지용 소켓 API
* StringBuilder.GetChunks
* IPEndPoint 구문 분석
* RandomNumberGenerator.GetInt32

## <a name="tiered-compilation"></a>계층화된 컴파일

[계층화된 컴파일](https://blogs.msdn.microsoft.com/dotnet/2018/08/02/tiered-compilation-preview-in-net-core-2-1/)은 .NET Core 3.0에서 기본적으로 켜져 있습니다. 런타임 시 JIT(Just-In-Time) 컴파일러를 보다 유연하게 사용해서 시작 시 성능과 처리량 극대화를 위한 성능을 둘 다 개선할 수 있도록 하는 기능입니다.

이 기능은 [.NET Core 2.1](https://blogs.msdn.microsoft.com/dotnet/2018/05/30/announcing-net-core-2-1/)에서 옵트인 기능으로 추가되었으며, [.NET Core 2.2 Preview 2](https://blogs.msdn.microsoft.com/dotnet/2018/09/12/announcing-net-core-2-2-preview-2/)에서 기본적으로 사용할 수 있었습니다. 이후에 .NET Core 2.2 릴리스에서 다시 옵트인으로 되돌려졌습니다.

## <a name="arm64-linux-support"></a>ARM64 Linux 지원

이 릴리스에서는 Linux에 대한 ARM64 지원이 추가되었습니다. 컨텍스트를 위해 .NET Core 2.1에서 Linux에 대한 ARM32 지원이 추가되었고, .NET Core 2.2에서 Windows에 대한 ARM32 지원이 추가되었습니다. ARM64는 현재 IoT 시나리오에서 주로 사용됩니다.

Alpine, Debian 및 Ubuntu [Docker 이미지를 ARM64용 .NET Core에 사용할 수 있습니다](https://hub.docker.com/r/microsoft/dotnet/).

자세한 내용은 [.NET Core ARM64 상태](https://github.com/dotnet/announcements/issues/82)를 참조하세요.

>[!NOTE]
> **ARM64** Windows 지원은 아직 사용할 수 없습니다.
