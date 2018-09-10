---
title: '방법: .NET Framework 스트림과 Windows 런타임 스트림 간 변환'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
ms.assetid: 23a763ea-8348-4244-9f8c-a4280b870b47
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b3cfaf4cf22bba445d774c653ff7797d535bcde2
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43398967"
---
# <a name="how-to-convert-between-net-framework-streams-and-windows-runtime-streams"></a>방법: .NET Framework 스트림과 Windows 런타임 스트림 간 변환

Windows 스토어 앱용 .NET Framework는 전체 .NET Framework의 하위 집합입니다. Windows 스토어 앱에 대한 보안과 기타 요구 사항 때문에, 파일을 열고 읽기 위해 전체 .NET Framework API 집합을 사용할 수 없습니다. 자세한 내용은 [Windows 스토어 앱용 .NET 개요](https://docs.microsoft.com/previous-versions/windows/apps/br230302(v=vs.140))를 참조하세요. 그러나 다른 스트림 조작 작업에 대한 .NET Framework API를 사용하고 싶을 수 있습니다. 이러한 스트림을 조작하려면 <xref:System.IO.MemoryStream> 또는 <xref:System.IO.FileStream>과 같은 .NET Framework 스트림 형식과 <xref:Windows.Storage.Streams.IInputStream>,<xref:Windows.Storage.Streams.IOutputStream> 또는 <xref:Windows.Storage.Streams.IRandomAccessStream>과 같은 Windows 런타임 스트림 간에 변환해야 할 수 있습니다.

[System.IO.WindowsRuntimeStreamExtensions](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.aspx) 클래스에는 이러한 변환을 쉽게 하는 메서드가 포함되어 있습니다. 하지만, 이런 메서드를 사용하는 결과에 영향을 미칠 .NET Framework과 Windows 런타임의 스트림 간에는 기본적인 차이가 있습니다. 다음 섹션에 세부 사항이 설명되어 있습니다.

## <a name="converting-from-a-windows-runtime-stream-to-a-net-framework-stream"></a>Windows 런타임 스트림에서 .NET Framework 스트림으로 변환

다음 [System.IO.WindowsRuntimeStreamExtensions ](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.aspx) 메서드 중 하나를 사용하여 Windows 런타임 스트림에서 .NET Framework 스트림으로 변환할 수 있습니다.

[System.IO.WindowsRuntimeStreamExtensions.AsStream](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asstream.aspx)  
Windows 런타임의 임의 액세스 스트림을 Windows 스토어 앱용 .NET 하위 집합에서 관리되는 스트림으로 변환합니다.

[System.IO.WindowsRuntimeStreamExtensions.AsStreamForWrite](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asstreamforwrite.aspx)  
Windows 런타임의 출력 스트림을 Windows 스토어 앱용 .NET 하위 집합에서 관리되는 스트림으로 변환합니다.

[System.IO.WindowsRuntimeStreamExtensions.AsStreamForRead](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asstreamforread.aspx)  
Windows 런타임의 입력 스트림을 Windows 스토어 앱용 .NET 하위 집합에서 관리되는 스트림으로 변환합니다.

Windows 런타임은 읽기 전용, 쓰기 전용 또는 읽기와 쓰기를 지원하는 스트림 형식을 제공하고, Windows 런타임 스트림을 .NET Framework 스트림으로 변환할 때 이러한 기능이 유지됩니다. 더구나 Windows 런타임 스트림을 .NET Framework 스트림으로 변환하고 그 반대로 변환하는 경우 원래 Windows 런타임 인스턴스를 다시 얻습니다. 변환하려는 Windows 런타임 스트림의 기능과 일치하는 변환 메서드를 사용하는 것이 가장 좋습니다. 하지만 <xref:Windows.Storage.Streams.IRandomAccessStream>을 읽고 쓸 수 있으므로(<xref:Windows.Storage.Streams.IOutputStream>과 <xref:Windows.Storage.Streams.IInputStream> 둘 다 구현함) 변환 메서드 중 어떤 메서드든 사용할 수 있고 원래 스트림의 기능이 유지됩니다. 예를 들어 [System.IO.WindowsRuntimeStreamExtensions.AsStreamForRead](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asstreamforread.aspx)를 사용하여 <xref:Windows.Storage.Streams.IRandomAccessStream>을 변환하면 변환된 .NET Framework 스트림은 읽기 전용으로 제한되지 않으며 쓸 수도 있습니다.

### <a name="to-convert-from-a-windows-runtime-random-access-stream-to-a-net-framework-stream"></a>Windows 런타임 임의 액세스 스트림에서 .NET Framework 스트림으로 변환하려면

- [System.IO.WindowsRuntimeStreamExtensions.AsStream](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asstream.aspx) 메서드를 사용합니다.

  다음 코드 예제에서는 사용자로 하여금 파일을 선택하고 Windows 런타임 API를 사용하여 열게 하고, 읽힌 다음 텍스트 블록으로 출력되는 .NET Framework 스트림으로 변환하는 방법을 보여 줍니다. 이 시나리오에서는, 결과를 출력하기 전에 .NET Framework API를 사용하여 스트림을 일반적으로 조작할 수 있습니다.

  이 예제를 실행하려면, `TextBlock1` 이라는 텍스트 블록과  `Button1`이라는 버튼을 포함한 Windows 스토어 XAML 앱을 만들어야 합니다. 단추 클릭 이벤트는 이 예제에 표시된 `button1_Click` 메서드와 연결되어야 합니다.

  [!code-csharp[System.IO.WindowsRuntimeStreamExtensionsEx#Imports](~/samples/snippets/csharp/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/cs/mainpage.xaml.cs#imports)]
  [!code-vb[System.IO.WindowsRuntimeStreamExtensionsEx#Imports](~/samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/vb/mainpage.xaml.vb#imports)]
  [!code-csharp[System.IO.WindowsRuntimeStreamExtensionsEx#1](~/samples/snippets/csharp/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/cs/mainpage.xaml.cs#1)]
  [!code-vb[System.IO.WindowsRuntimeStreamExtensionsEx#1](~/samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/vb/mainpage.xaml.vb#1)]

## <a name="converting-from-a-net-framework-stream-to-a-windows-runtime-stream"></a>.NET Framework 스트림에서 Windows 런타임 스트림으로 변환

다음 [System.IO.WindowsRuntimeStreamExtensions ](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.aspx) 메서드 중 하나를 사용하여 .NET Framework에서 Windows 런타임 스트림으로 변환할 수 있습니다.

[System.IO.WindowsRuntimeStreamExtensions.AsInputStream](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asinputstream.aspx) Windows 스토어 앱용 .NET 하위 집합에서 관리되는 스트림을 Windows 런타임의 입력 스트림으로 변환합니다.

[System.IO.WindowsRuntimeStreamExtensions.AsOutputStream](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asoutputstream.aspx) Windows 스토어 앱용 .NET 하위 집합에서 관리되는 스트림을 Windows 런타임의 출력 스트림으로 변환합니다.

[AsRandomAccessStream](../../../docs/standard/cross-platform/windowsruntimestreamextensions-asrandomaccessstream-method.md) Windows 스토어 앱용 .NET 하위 집합에서 관리되는 스트림을 Windows 런타임에서 읽거나 쓰는 데 사용할 수 있는 임의 액세스 스트림으로 변환합니다.

.NET Framework 스트림을 Windows 런타임 스트림으로 변환할 때 변환된 스트림의 기능은 원본 스트림에 따라 다릅니다. 예를 들어, 원본 스트림이 읽기와 쓰기를 모두 지원하고 [System.IO.WindowsRuntimeStreamExtensions.AsInputStream](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions.asinputstream.aspx)을 호출하여 스트림을 변환하는 경우, 반환되는 형식은 `IInputStream` 및 `IOutputStream`을 구현하는 `IRandomAccessStream`이 되며 읽기 및 쓰기를 지원합니다.

.NET Framework 스트림은 변환 후에도 복제를 지원하지 않습니다. 즉, .NET Framework 스트림을 Windows 런타임 스트림으로 변환하고 <xref:Windows.Storage.Streams.RandomAccessStreamOverStream.CloneStream%2A>를 호출하거나 <xref:Windows.Storage.Streams.RandomAccessStreamOverStream.CloneStream%2A>를 직접 호출하는 <xref:Windows.Storage.Streams.InMemoryRandomAccessStream.GetInputStreamAt%2A> 또는 <xref:Windows.Storage.Streams.IRandomAccessStream.GetOutputStreamAt%2A> 예외가 발생합니다.

### <a name="to-convert-from-a-net-framework-stream-to-a-windows-runtime-random-access-stream"></a>.NET Framework 스트림에서 Windows 런타임 임의 액세스 스트림으로 변환하려면

- 다음 예제에 표시된 것처럼 [AsRandomAccessStream](../../../docs/standard/cross-platform/windowsruntimestreamextensions-asrandomaccessstream-method.md) 메서드를 사용합니다.

  > [!IMPORTANT]
  > 사용 중인 .NET Framework 스트림이 검색을 지원하는지 확인하거나, 이런 스트림을 지원하는 스트림에 복사합니다. <xref:System.IO.Stream.CanSeek%2A?displayProperty=nameWithType> 속성을 사용하여 이를 확인할 수 있습니다.

  이 예제를 실행하려면 .NET Framework 4.5.1을 대상으로 하고 `TextBlock2` 라는 텍스트 블록과 `Button2`라는 단추를 포함한 Windows 스토어 XAML 앱을 만들어야 합니다. 단추 클릭 이벤트는 이 예제에 표시된 `button2_Click` 메서드와 연결되어야 합니다.

  [!code-csharp[System.IO.WindowsRuntimeStreamExtensionsEx#Imports](~/samples/snippets/csharp/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/cs/mainpage.xaml.cs#imports)]
  [!code-vb[System.IO.WindowsRuntimeStreamExtensionsEx#Imports](~/samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/vb/mainpage.xaml.vb#imports)]
  [!code-csharp[System.IO.WindowsRuntimeStreamExtensionsEx#2](~/samples/snippets/csharp/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/cs/mainpage.xaml.cs#2)]
  [!code-vb[System.IO.WindowsRuntimeStreamExtensionsEx#2](~/samples/snippets/visualbasic/VS_Snippets_CLR_System/system.io.windowsruntimestreamextensionsex/vb/mainpage.xaml.vb#2)]

## <a name="see-also"></a>참고 항목

[퀵 스타트: 파일 읽기 및 쓰기(Windows)](https://msdn.microsoft.com/library/windows/apps/hh464978.aspx)  
[Windows 스토어 앱용 .NET 개요](https://msdn.microsoft.com/library/windows/apps/br230302.aspx)  
[Windows 스토어 앱용 .NET – 지원되는 API](https://msdn.microsoft.com/library/windows/apps/br230232.aspx)  