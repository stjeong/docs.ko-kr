---
title: '방법: 설치된 .NET Framework 버전 확인'
ms.date: 02/20/2019
dev_langs:
- csharp
- vb
ms.custom: updateeachrelease
helpviewer_keywords:
- versions, determining for .NET Framework
- .NET Framework, determining version
ms.assetid: 40a67826-e4df-4f59-a651-d9eb0fdc755d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d7661b3ebaa8f29d6d3b2adbc56c405c8f0945f3
ms.sourcegitcommit: 07c4368273b446555cb2c85397ea266b39d5fe50
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56584176"
---
# <a name="how-to-determine-which-net-framework-versions-are-installed"></a>방법: 설치된 .NET Framework 버전 확인

사용자는 자신의 컴퓨터에 여러 버전의 .NET Framework를 설치하여 실행할 수 있습니다. 따라서 앱을 개발하거나 배포할 때는 사용자의 컴퓨터에 어떤 .NET Framework 버전이 설치되었는지 알아야 합니다. .NET Framework는 각 버전으로 식별되는 다음과 같은 2개의 주요 구성 요소로 구성됩니다.  
  
- 앱의 기능을 제공하는 형식 및 리소스 컬렉션에 해당하는 어셈블리 집합. .NET Framework와 어셈블리는 동일한 버전 번호를 공유합니다.  
  
- 앱 코드를 관리하고 실행하는 CLR(공용 언어 런타임). CLR은 고유한 버전 번호로 식별됩니다([버전 및 종속성](~/docs/framework/migration-guide/versions-and-dependencies.md) 참조).  
  
컴퓨터에 설치된 정확한 .NET Framework 버전 목록을 보려면 다음을 참조하여 레지스트리를 확인하거나 코드로 레지스트리를 쿼리합니다.  
  
 [레지스트리에서 .NET Framework 버전 1-4 찾기](#net_a)  
 [레지스트리에서 .NET Framework 버전 4.5 이상 찾기](#net_b)  
 [코드를 사용하여 레지스트리 쿼리(버전 1-4)](#net_c)  
 [코드를 사용하여 레지스트리 쿼리(버전 4.5 이상)](#net_d)  
 [PowerShell을 사용하여 레지스트리 쿼리(버전 4.5 이상)](#ps_a)  

 CLR 버전을 찾으려면 다음을 참조하여 도구나 코드를 사용합니다.  
  
 [Clrver 도구 사용](#clr_a)  
 [코드를 사용하여 System.Environment 클래스 쿼리](#clr_b)  

> [!NOTE]
> .NET Framework 버전과 CLR(공용 언어 런타임) 버전은 다릅니다. .NET Framework의 버전은 .NET Framework 클래스 라이브러리를 구성하는 어셈블리 세트를 기반으로 정해집니다. 예를 들어, .NET Framework 버전에는 4.5, 4.6.1, 4.7.2가 있습니다. CLR의 버전은 .NET Framework 애플리케이션이 실행되는 런타임을 기반으로 정해지며, 일반적으로 하나의 CLR 버전이 여러 개의 .NET Framework 버전을 지원합니다. CLR 버전 4.30319.*xxxxx*는 .NET Framework 버전 4~4.5.2를 지원하고, CLR 버전 4.30319.42000은 .NET Framework 4.6에서 시작하는 .NET Framework 버전을 지원합니다. 자세한 내용은 <xref:System.Environment.Version?displayProperty=nameWithType> 속성을 참조하세요.

 .NET Framework의 버전별로 설치된 업데이트를 검색하는 방법에 대한 자세한 내용은 [방법: 설치된 .NET Framework 업데이트 확인](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md)을 참조하세요. .NET Framework 설치에 대한 자세한 내용은 [개발자용 .NET Framework 설치](../../../docs/framework/install/guide-for-developers.md)를 참조하세요.  
  
<a name="net_a"></a>   
## <a name="find-net-framework-versions-1-4-in-the-registry"></a>레지스트리에서 .NET Framework 버전 1-4 찾기 
  
1.  **시작** 메뉴에서 **실행**을 선택합니다.  
  
2.  **열기** 상자에 **regedit.exe**를 입력합니다.  
  
     regedit.exe를 실행하려면 관리자 자격 증명이 있어야 합니다.  
  
3.  레지스트리 편집기에서 다음 하위 키를 엽니다.  
  
     `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP`  
  
     .NET Framework 버전 1.1~3.5의 경우, 설치된 버전이 `NDP` 하위 키 아래에 하위 키로 나열됩니다. 버전 번호는 버전 하위 키의 **Version** 항목에 저장됩니다. 
     
     .NET Framework 4의 경우, **Version** 항목은 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4.0\Client` 하위 키 또는 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4.0\Full` 하위 키 아래에, 또는 두 하위 키 아래에 있습니다.

    > [!NOTE]
    > 레지스트리의 "NET Framework Setup" 폴더는 마침표로 시작하지 않습니다.

    다음 그림은 .NET Framework 3.5의 하위 키와 **Version** 항목을 보여줍니다.

     ![.NET Framework 3.5의 레지스트리 항목.](../../../docs/framework/migration-guide/media/net-4-and-earlier.png ".NET Framework 4 및 이전 버전")

<a name="net_b"></a> 
## <a name="find-net-framework-versions-45-and-later-in-the-registry"></a>레지스트리에서 .NET Framework 버전 4.5 이상 찾기

1. **시작** 메뉴에서 **실행**을 선택합니다.

2. **열기** 상자에 **regedit.exe**를 입력합니다.

     regedit.exe를 실행하려면 관리자 자격 증명이 있어야 합니다.

3. 레지스트리 편집기에서 다음 하위 키를 엽니다.

     `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full`

     `Full` 하위 키에 대한 경로에는 `.NET Framework` 대신 `Net Framework` 하위 키가 포함되어 있습니다.

    > [!NOTE]
    > `Full` 하위 키가 없으면 .NET Framework 4.5 이상이 설치되어 있지 않은 것입니다.

     `Release`라는 DWORD 값을 확인합니다. `Release` DWORD가 있으면 컴퓨터에 .NET Framework 4.5 이상이 설치된 것입니다. 그 값은 특정 버전의 .NET Framework에 대응되는 릴리스 키입니다. 예를 들어, 다음 그림에서 `Release` DWORD의 값은 378389로, 이것은 .NET Framework 4.5의 릴리스 키입니다. 

     ![.NET Framework 4.5.](../../../docs/framework/migration-guide/media/clr-installdir.png "CLR_InstallDir")에 대한 레지스트리 항목입니다.

다음 표에서는 각 .NET Framework 버전의 `Release` DWORD의 최솟값을 보여줍니다. 이 값은 다음과 같이 사용할 수 있습니다.

- 최소 .NET Framework 버전이 설치되었는지 확인하려면, 레지스트리에서 확인한 `Release` DWORD 값이 표에 있는 값보다 ‘크거나 같은지’ 살펴봅니다. 예를 들어, 애플리케이션에 .NET Framework 4.7 이상이 필요한 경우, 릴리스 키 값이 최소 460798이어야 합니다.

- 여러 버전을 테스트하려면 최신 .NET Framework 버전부터 시작하고 역으로 버전을 줄여가며 하나씩 테스트합니다.

[!INCLUDE[Release key values note](~/includes/version-keys-note.md)]

|.NET Framework 버전|릴리스 DWORD의 값|
|--------------------------------|-------------|
|.NET Framework 4.5|378389|
|.NET Framework 4.5.1|378675|
|.NET Framework 4.5.2|379893|
|.NET Framework 4.6|393295|
|.NET Framework 4.6.1|394254|
|.NET Framework 4.6.2|394802|
|.NET Framework 4.7|460798|
|.NET Framework 4.7.1|461308|
|.NET Framework 4.7.2|461808|

특정 Windows 운영 체제 버전용 .NET Framework의 릴리스 키를 모두 확인하려면 [.NET Framework 릴리스 키 및 Windows 운영 체제 버전](release-keys-and-os-versions.md)을 참조하세요.

<a name="net_c"></a> 
## <a name="find-net-framework-versions-1-4-with-code"></a>코드를 사용하여 .NET Framework 버전 1-4 찾기

- <xref:Microsoft.Win32.RegistryKey?displayProperty=nameWithType> 클래스를 사용하여 Windows 레지스트리에서 `HKEY_LOCAL_MACHINE` 분기 아래에 있는 `Software\Microsoft\NET Framework Setup\NDP\` 하위 키에 액세스합니다.

     다음 코드에서는 이 쿼리의 예제를 보여 줍니다.

    > [!NOTE]
    > 이 코드는 .NET Framework 4.5 이상을 확인하는 방법을 보여주지 않습니다. 이전 섹션에 설명된 대로 `Release` DWORD를 확인하여 해당 버전을 검색합니다. .NET Framework 4.5 이상 버전을 확인하는 코드가 필요하면 이 문서의 다음 섹션을 참조하세요.

     [!code-csharp[ListVersions](../../../samples/snippets/csharp/framework/migration-guide/versions-installed1.cs)]
     [!code-vb[ListVersions](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed1.vb)]

<a name="net_d"></a> 
## <a name="find-net-framework-versions-45-and-later-with-code"></a>코드를 사용하여 .NET Framework 버전 4.5 이상 찾기

1. `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full` 키에 `Release` DWORD가 있으면 .NET Framework 4.5 이상이 컴퓨터에 설치된 것입니다. 이 키워드 값이 설치된 버전을 나타냅니다. 이 키워드를 확인하려면 <xref:Microsoft.Win32.RegistryKey.OpenBaseKey%2A?displayProperty=nameWithType> 및 <xref:Microsoft.Win32.RegistryKey.OpenSubKey%2A?displayProperty=nameWithType> 메서드를 사용하여 Windows 레지스트리의 하위 키에 액세스합니다.

2. `Release` 키워드 값을 확인하여 설치된 버전을 확인합니다. 이후 버전과의 호환성을 유지하려면 값이 [레지스트리에서 .NET Framework 버전 4.5 이상 찾기](#net_b) 섹션의 표에 있는 값보다 크거나 같은지 확인하면 됩니다.

다음 예제에서는 레지스트리에서 `Release` 값을 확인하여 .NET Framework 4.5 이상 버전이 설치되어 있는지 확인합니다.

[!code-csharp[ListVersions#5](../../../samples/snippets/csharp/framework/migration-guide/versions-installed3.cs)]
[!code-vb[ListVersions#5](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed3.vb)]

이 예제에서는 버전을 확인하기 위한 권장된 방법을 수행합니다.

- `Release` 항목의 값이 알려진 릴리즈 키의 값보다 *크거나 같은지* 확인합니다.

- 최신 버전에서 가장 오래된 버전 순서대로 확인합니다.

<a name="ps_a"></a> 
## <a name="check-for-a-minimum-required-net-framework-version-45-and-later-with-powershell"></a>PowerShell을 사용하여 필요한 최소 .NET Framework 버전(4.5 이상) 확인

다음 예제에서는 `Release` 키워드 값을 확인하여 .NET Framework 4.6.2 이상이 설치되어 있는지 확인합니다(설치된 경우 `True` 반환, 설치되지 않은 경우 `False` 반환).

    ```PowerShell
    # PowerShell 5
    Get-ChildItem 'HKLM:\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full\' | Get-ItemPropertyValue -Name Release | Foreach-Object { $_ -ge 394802 } 
    ```

    ```PowerShell
    # PowerShell 4
    (Get-ItemProperty "HKLM:SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full").Release -gt 394802
    ```

    You can replace `394802` in the previous example with another value from the following table in the [Find .NET Framework versions 4.5 and later in the registry](#net_b) section to check for a different minimum required .NET Framework version.
  
<a name="clr_a"></a> 
## <a name="find-the-current-clr-version-with-clrverexe"></a>Clrver.exe를 사용하여 현재 CLR 버전 찾기

CLR 버전 도구(Clrver.exe)를 사용하여 컴퓨터에 설치된 공용 언어 런타임의 버전을 확인합니다.

Visual Studio용 개발자 명령 프롬프트에서 `clrver`을 입력합니다. 이 명령은 다음과 유사한 출력 결과를 표시합니다.

```console
Versions installed on the machine:
v2.0.50727
v4.0.30319
```

이 도구의 사용 방법에 대한 자세한 내용은 [Clrver.exe(CLR 버전 도구)](~/docs/framework/tools/clrver-exe-clr-version-tool.md)를 참조하세요.

<a name="clr_b"></a> 
## <a name="find-the-current-clr-version-with-the-environment-class"></a>Environment 클래스를 사용하여 현재 CLR 버전 찾기

<xref:System.Environment.Version?displayProperty=nameWithType> 속성의 값을 가져와서 현재 코드를 실행하고 있는 런타임의 버전을 식별하는 <xref:System.Version> 개체를 가져올 수 있습니다. 이 속성은 현재 코드를 실행하고 있는 런타임의 버전을 반영하는 하나의 값을 반환하며, 컴퓨터에 설치된 어셈블리 버전이나 다른 런타임 버전은 반환하지 않습니다. <xref:System.Version.Major%2A?displayProperty=nameWithType> 속성을 사용하여 주 릴리스 식별자(예: 버전 4.0의 경우 “4”)를 가져오고, <xref:System.Version.Minor%2A?displayProperty=nameWithType> 속성을 사용하여 부 릴리스 식별자(예: 버전 4.0의 경우 “0”)를 가져오고, <xref:System.Version.ToString%2A?displayProperty=nameWithType> 메서드를 사용하여 전체 버전 문자열(예: 다음 코드에 표시된 것 같이 “4.0.30319.18010”)을 가져올 수 있습니다. 

.NET Framework 버전 4, 4.5, 4.5.1 및 4.5.2의 경우 <xref:System.Environment.Version%2A?displayProperty=nameWithType> 속성은 문자열 표시가 `4.0.30319.xxxxx` 형식인 <xref:System.Version> 개체를 반환합니다. .NET Framework 4.6 이상에서는 `4.0.30319.42000` 형식입니다.

> [!IMPORTANT]
> .NET Framework 4.5 이상의 경우 <xref:System.Environment.Version%2A?displayProperty=nameWithType> 속성을 사용하여 런타임의 버전을 확인하는 것을 권장하지 않습니다. 대신 이 문서의 앞부분에 나오는 [코드로 레지스트리를 쿼리하여 .NET Framework 버전을 찾으려면(.NET Framework 4.5 이상)](#net_d) 섹션에서 설명된 것처럼 레지스트리를 쿼리하는 것을 권장합니다.

다음 예제에서는 <xref:System.Environment.Version%2A?displayProperty=nameWithType> 속성을 사용하여 런타임 버전 정보를 가져옵니다.

[!code-csharp[ListVersions](../../../samples/snippets/csharp/framework/migration-guide/versions-installed2.cs)]
[!code-vb[ListVersions](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed2.vb)]

## <a name="see-also"></a>참고 항목

- [방법: 설치된 .NET Framework 업데이트 확인](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md)
- [개발자용 .NET Framework 설치](../../../docs/framework/install/guide-for-developers.md)
- [버전 및 종속성](~/docs/framework/migration-guide/versions-and-dependencies.md)
