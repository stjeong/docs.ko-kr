---
title: WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream) 메서드
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
api_name:
- System.IO.WindowsRuntimeStreamExtensions.AsRandomAccessStream
api_location:
- System.Runtime.WindowsRuntime.dll
ms.assetid: dcc72283-caed-49ee-b45d-ccaf94e97129
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a712414163446606cbc93154bc821d3b1166fe8f
ms.sourcegitcommit: fe02afbc39e78afd78cc6050e4a9c12a75f579f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43254259"
---
# <a name="windowsruntimestreamextensionsasrandomaccessstreamsystemiostream-method"></a><span data-ttu-id="0c2ee-102">WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream) 메서드</span><span class="sxs-lookup"><span data-stu-id="0c2ee-102">WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream) Method</span></span>

<span data-ttu-id="0c2ee-103">[.NET Framework 4.5.1 이상 버전에서 지원됨]</span><span class="sxs-lookup"><span data-stu-id="0c2ee-103">[Supported in the .NET Framework 4.5.1 and later versions]</span></span>

<span data-ttu-id="0c2ee-104">지정된 스트림을 임의 액세스 스트림으로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-104">Converts the specified stream to a random access stream.</span></span>

<span data-ttu-id="0c2ee-105">**: Namespace** <xref:System.IO?displayProperty=nameWithType> 
 **어셈블리:** System.Runtime.WindowsRuntime (system.runtime.windowsruntime.dll에서)</span><span class="sxs-lookup"><span data-stu-id="0c2ee-105">**Namespace:** <xref:System.IO?displayProperty=nameWithType>
**Assembly:** System.Runtime.WindowsRuntime (in System.Runtime.WindowsRuntime.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0c2ee-106">구문</span><span class="sxs-lookup"><span data-stu-id="0c2ee-106">Syntax</span></span>

```csharp
[CLSCompliantAttribute(false)]
public static IRandomAccessStream AsRandomAccessStream(Stream stream)
```

```vb
'Declaration
<ExtensionAttribute> _
<CLSCompliantAttribute(False)> _
Public Shared Function AsRandomAccessStream ( _
        stream As Stream) As IRandomAccessStream
```

## <a name="parameters"></a><span data-ttu-id="0c2ee-107">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0c2ee-107">Parameters</span></span>

`stream`

<span data-ttu-id="0c2ee-108">형식: <xref:System.IO.Stream?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="0c2ee-108">Type: <xref:System.IO.Stream?displayProperty=nameWithType></span></span>  
<span data-ttu-id="0c2ee-109">변환할 스트림입니다.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-109">The stream to convert.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c2ee-110">반환 값</span><span class="sxs-lookup"><span data-stu-id="0c2ee-110">Return Value</span></span>

<span data-ttu-id="0c2ee-111">형식: <xref:Windows.Storage.Streams.RandomAccessStream></span><span class="sxs-lookup"><span data-stu-id="0c2ee-111">Type: <xref:Windows.Storage.Streams.RandomAccessStream></span></span>  
<span data-ttu-id="0c2ee-112">[!INCLUDE[wrt](../../../includes/wrt-md.md)] 임의 액세스 스트림은 변환된 된 스트림을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-112">A [!INCLUDE[wrt](../../../includes/wrt-md.md)] random access stream, which represents the converted stream.</span></span>

## <a name="exceptions"></a><span data-ttu-id="0c2ee-113">예외</span><span class="sxs-lookup"><span data-stu-id="0c2ee-113">Exceptions</span></span>

|<span data-ttu-id="0c2ee-114">예외</span><span class="sxs-lookup"><span data-stu-id="0c2ee-114">Exception</span></span>|<span data-ttu-id="0c2ee-115">조건</span><span class="sxs-lookup"><span data-stu-id="0c2ee-115">Condition</span></span>|
|---------------|---------------|
|<xref:System.NotSupportedException>|<span data-ttu-id="0c2ee-116">변환할 스트림은 검색을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-116">The stream to convert does not support seeking.</span></span>|

## <a name="remarks"></a><span data-ttu-id="0c2ee-117">설명</span><span class="sxs-lookup"><span data-stu-id="0c2ee-117">Remarks</span></span>

<span data-ttu-id="0c2ee-118">이 확장 메서드는 Windows 스토어 앱을 개발하는 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-118">This extension method is available only when you develop Windows Store apps.</span></span> <span data-ttu-id="0c2ee-119">이 메서드는 Windows 스토어 앱의 스트림을 작업하는 데 편리를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-119">This method provides a convenient way of working with streams in Windows Store apps.</span></span> <span data-ttu-id="0c2ee-120">변환하려는 .NET Framework 스트림은 검색을 지원해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-120">The .NET Framework stream you want to convert must support seeking.</span></span> <span data-ttu-id="0c2ee-121">자세한 내용은 <xref:System.IO.Stream.Seek%2A?displayProperty=nameWithType> 메서드를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-121">For more information, see the <xref:System.IO.Stream.Seek%2A?displayProperty=nameWithType> method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0c2ee-122">이 API는 .NET Framework 4.5.1 이상 버전에서 지원되지만 4.5 버전에서는 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-122">This API is supported in the .NET Framework 4.5.1 and later versions, but not in version 4.5.</span></span>

## <a name="version-information"></a><span data-ttu-id="0c2ee-123">버전 정보</span><span class="sxs-lookup"><span data-stu-id="0c2ee-123">Version Information</span></span>

<span data-ttu-id="0c2ee-124">**Windows 스토어 앱 용.NET**</span><span class="sxs-lookup"><span data-stu-id="0c2ee-124">**.NET for Windows Store apps**</span></span>

<span data-ttu-id="0c2ee-125">지원: Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0c2ee-125">Supported in: Windows 8.1</span></span>

## <a name="see-also"></a><span data-ttu-id="0c2ee-126">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0c2ee-126">See Also</span></span>

<span data-ttu-id="0c2ee-127">[System.IO.WindowsRuntimeStreamExtensions](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions(v=vs.110).aspx)</span><span class="sxs-lookup"><span data-stu-id="0c2ee-127">[System.IO.WindowsRuntimeStreamExtensions](https://msdn.microsoft.com/library/system.io.windowsruntimestreamextensions(v=vs.110).aspx)</span></span>  
[<span data-ttu-id="0c2ee-128">방법: .NET Framework 스트림과 Windows 런타임 스트림 간 변환</span><span class="sxs-lookup"><span data-stu-id="0c2ee-128">How to: Convert Between .NET Framework Streams and Windows Runtime Streams</span></span>](../io/how-to-convert-between-dotnet-streams-and-winrt-streams.md)  