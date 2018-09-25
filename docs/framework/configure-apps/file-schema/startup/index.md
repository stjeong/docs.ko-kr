---
title: 시작 설정 스키마
ms.date: 03/30/2017
helpviewer_keywords:
- startup settings schema
- schema startup settings
- configuration schema [.NET Framework], startup settings
ms.assetid: 03de6972-442a-4648-9f3e-efa654e3b949
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 4cdf6a051552ab1effd9c4d9c783297a62602f7a
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47078164"
---
# <a name="startup-settings-schema"></a><span data-ttu-id="28089-102">시작 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="28089-102">Startup Settings Schema</span></span>
<span data-ttu-id="28089-103">시작 설정은 응용 프로그램을 실행해야 하는 공용 언어 런타임의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="28089-103">Startup settings specify the version of the common language runtime that should run the application.</span></span>  
  
|<span data-ttu-id="28089-104">요소</span><span class="sxs-lookup"><span data-stu-id="28089-104">Element</span></span>|<span data-ttu-id="28089-105">설명</span><span class="sxs-lookup"><span data-stu-id="28089-105">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="28089-106">\<requiredRuntime></span><span class="sxs-lookup"><span data-stu-id="28089-106">\<requiredRuntime></span></span>](../../../../../docs/framework/configure-apps/file-schema/startup/requiredruntime-element.md)|<span data-ttu-id="28089-107">응용 프로그램에서 1.0 버전의 공용 언어 런타임만 지원하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="28089-107">Specifies that the application supports only version 1.0 of the common language runtime.</span></span> <span data-ttu-id="28089-108">런타임 버전 1.1로 빌드된 응용 프로그램은 **\<supportedRuntime>** 요소를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28089-108">Applications built with runtime version 1.1 should use the **\<supportedRuntime>** element.</span></span>|  
|[<span data-ttu-id="28089-109">\<supportedRuntime></span><span class="sxs-lookup"><span data-stu-id="28089-109">\<supportedRuntime></span></span>](../../../../../docs/framework/configure-apps/file-schema/startup/supportedruntime-element.md)|<span data-ttu-id="28089-110">응용 프로그램이 지원하는 공용 언어 런타임 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="28089-110">Specifies which versions of the common language runtime the application supports.</span></span>|  
|[<span data-ttu-id="28089-111">\<startup></span><span class="sxs-lookup"><span data-stu-id="28089-111">\<startup></span></span>](../../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md)|<span data-ttu-id="28089-112">**\<requiredRuntime>** 및 **\<supportedRuntime>** 요소가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28089-112">Contains the **\<requiredRuntime>** and **\<supportedRuntime>** elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="28089-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="28089-113">See Also</span></span>  
 [<span data-ttu-id="28089-114">구성 파일 스키마</span><span class="sxs-lookup"><span data-stu-id="28089-114">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="28089-115">\<PaveOver> 사용할 런타임 버전 지정</span><span class="sxs-lookup"><span data-stu-id="28089-115">\<PaveOver> Specifying Which Runtime Version to Use</span></span>](https://msdn.microsoft.com/library/c376208d-980d-42b4-865b-fbe0d9cc97c2)
