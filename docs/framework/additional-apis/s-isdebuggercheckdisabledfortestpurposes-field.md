---
title: s_isDebuggerCheckDisabledForTestPurposes 필드
ms.date: 03/30/2017
ms.technology:
- dotnet-wpf
api_name:
- System.Windows.Diagnostics.VisualDiagnostics.s_isDebuggerCheckDisabledForTestPurposes
api_location:
- PresentationCore.dll
api_type:
- Assembly
ms.assetid: 9033a513-c255-4f31-b6d7-09b8d8c50e2d
ms.openlocfilehash: f490ccb4675a434e3f3336723e321f256b10093d
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149178"
---
# <a name="sisdebuggercheckdisabledfortestpurposes-field"></a><span data-ttu-id="10c4f-102">s_isDebuggerCheckDisabledForTestPurposes 필드</span><span class="sxs-lookup"><span data-stu-id="10c4f-102">s_isDebuggerCheckDisabledForTestPurposes Field</span></span>

<span data-ttu-id="10c4f-103">이 개인 필드에는 `System.Windows.Diagnostics.VisualDiagnostics` 클래스는 현재 디버거의 내부 검사를 수행할지 여부를 확인 하려면 Visual Studio에서 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="10c4f-103">This private field in the `System.Windows.Diagnostics.VisualDiagnostics` class is used by Visual Studio to determine whether an internal check for an active debugger will be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="10c4f-104">구문</span><span class="sxs-lookup"><span data-stu-id="10c4f-104">Syntax</span></span>
  
```csharp  
private static bool s_isDebuggerCheckDisabledForTestPurposes
```
  
> [!WARNING]
>  <span data-ttu-id="10c4f-105">API를 `System.Windows.Diagnostics.VisualDiagnostics` 클래스 디버거에서 응용 프로그램이 실행 되는 경우에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10c4f-105">API's in the `System.Windows.Diagnostics.VisualDiagnostics` class are only available when an application is running under a debugger.</span></span> <span data-ttu-id="10c4f-106">설정할 `s_isDebuggerCheckDisabledForTestPurposes` 에 `true` 디버거 외부에서 Api에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10c4f-106">Set `s_isDebuggerCheckDisabledForTestPurposes` to `true` to access the APIs outside of a debugger.</span></span>  
>   
>  <span data-ttu-id="10c4f-107">Microsoft는 어떤 상황에서 프로덕션 응용 프로그램에서이 필드의 사용을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10c4f-107">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>  

## <a name="requirements"></a><span data-ttu-id="10c4f-108">요구 사항</span><span class="sxs-lookup"><span data-stu-id="10c4f-108">Requirements</span></span>

<span data-ttu-id="10c4f-109">**네임스페이스:** <xref:System.Windows.Diagnostics></span><span class="sxs-lookup"><span data-stu-id="10c4f-109">**Namespace:** <xref:System.Windows.Diagnostics></span></span>

<span data-ttu-id="10c4f-110">**어셈블리:** PresentationCore (presentationcore.dll)</span><span class="sxs-lookup"><span data-stu-id="10c4f-110">**Assembly:** PresentationCore (in PresentationCore.dll)</span></span>

<span data-ttu-id="10c4f-111">**.NET framework 버전:** 4.6부터 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10c4f-111">**.NET Framework versions:** Available since 4.6.</span></span>