---
title: '&lt;구성&gt; 요소'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration
helpviewer_keywords:
- <configuration> element
- configuration element
- container tags, <configuration> element
ms.assetid: 2ec1c9dc-2e5c-4ef0-9958-81670ab88449
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: c5146ed8326b12e90d0fe6247b0c4aba3a69dd77
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43485783"
---
# <a name="configuration-element"></a><span data-ttu-id="b5cb0-102">\<구성 > 요소</span><span class="sxs-lookup"><span data-stu-id="b5cb0-102">\<configuration> element</span></span>

<span data-ttu-id="b5cb0-103">공용 언어 런타임 및 .NET Framework 응용 프로그램에서 사용하는 모든 구성 파일의 루트 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cb0-103">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>

<span data-ttu-id="b5cb0-104">**\<구성>**</span><span class="sxs-lookup"><span data-stu-id="b5cb0-104">**\<configuration>**</span></span>

## <a name="syntax"></a><span data-ttu-id="b5cb0-105">구문</span><span class="sxs-lookup"><span data-stu-id="b5cb0-105">Syntax</span></span>

```xml
<configuration>
  <!-- Configuration settings -->
</configuration>
```

## <a name="attributes"></a><span data-ttu-id="b5cb0-106">특성</span><span class="sxs-lookup"><span data-stu-id="b5cb0-106">Attributes</span></span>

<span data-ttu-id="b5cb0-107">없음</span><span class="sxs-lookup"><span data-stu-id="b5cb0-107">None</span></span>

## <a name="parent-element"></a><span data-ttu-id="b5cb0-108">부모 요소</span><span class="sxs-lookup"><span data-stu-id="b5cb0-108">Parent element</span></span>

<span data-ttu-id="b5cb0-109">없음</span><span class="sxs-lookup"><span data-stu-id="b5cb0-109">None</span></span>

## <a name="child-elements"></a><span data-ttu-id="b5cb0-110">자식 요소</span><span class="sxs-lookup"><span data-stu-id="b5cb0-110">Child elements</span></span>

|     | <span data-ttu-id="b5cb0-111">설명</span><span class="sxs-lookup"><span data-stu-id="b5cb0-111">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="b5cb0-112">**\<assemblyBinding >**</span><span class="sxs-lookup"><span data-stu-id="b5cb0-112">**\<assemblyBinding>**</span></span>](~/docs/framework/configure-apps/file-schema/assemblybinding-element-for-configuration.md) | <span data-ttu-id="b5cb0-113">구성 수준에서 어셈블리 바인딩 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5cb0-113">Specifies assembly binding policy at the configuration level.</span></span>|
| [<span data-ttu-id="b5cb0-114">**\<시작 >** 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="b5cb0-114">**\<startup>** Settings Schema</span></span>](~/docs/framework/configure-apps/file-schema/startup/index.md) | <span data-ttu-id="b5cb0-115">시작 설정 스키마의 모든 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cb0-115">All elements in the startup settings schema.</span></span> |
| [<span data-ttu-id="b5cb0-116">**\<런타임 >** 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="b5cb0-116">**\<runtime>** Settings Schema</span></span>](~/docs/framework/configure-apps/file-schema/runtime/index.md) | <span data-ttu-id="b5cb0-117">런타임 설정 스키마의 모든 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cb0-117">All elements in the runtime settings schema.</span></span> |
| [<span data-ttu-id="b5cb0-118">**\<system.runtime.remoting >** 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="b5cb0-118">**\<system.runtime.remoting>** Settings Schema</span></span>](https://msdn.microsoft.com/dc2d1e62-9af7-4ca1-99fd-98b93bb4db9e) | <span data-ttu-id="b5cb0-119">원격 설정 스키마의 모든 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cb0-119">All elements in the remoting settings schema.</span></span> |
| [<span data-ttu-id="b5cb0-120">**\<system.Net >** 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="b5cb0-120">**\<system.Net>** Settings Schema</span></span>](~/docs/framework/configure-apps/file-schema/network/index.md) | <span data-ttu-id="b5cb0-121">네트워크 설정 스키마의 모든 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cb0-121">All elements in the network settings schema.</span></span> |
| [<span data-ttu-id="b5cb0-122">**\<cryptographySettings >** 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="b5cb0-122">**\<cryptographySettings>** Settings Schema</span></span>](~/docs/framework/configure-apps/file-schema/cryptography/index.md) | <span data-ttu-id="b5cb0-123">암호화 설정 스키마의 모든 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cb0-123">All elements in the crypto settings schema.</span></span> |
| [<span data-ttu-id="b5cb0-124">**\<구성 >** 섹션 스키마</span><span class="sxs-lookup"><span data-stu-id="b5cb0-124">**\<configuration>** Sections Schema</span></span>](~/docs/framework/configure-apps/file-schema/configuration-sections-schema.md) | <span data-ttu-id="b5cb0-125">구성 섹션 설정 스키마의 모든 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cb0-125">All elements in the configuration section settings schema.</span></span> |
| [<span data-ttu-id="b5cb0-126">추적 및 디버그 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="b5cb0-126">Trace and Debug Settings Schema</span></span>](~/docs/framework/configure-apps/file-schema/trace-debug/index.md) | <span data-ttu-id="b5cb0-127">추적 및 디버그 설정 스키마의 모든 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cb0-127">All elements in the trace and debug settings schema.</span></span> |
| <span data-ttu-id="b5cb0-128">[ASP.NET 구성 설정 스키마](https://msdn.microsoft.com/library/b5ysx397(v=vs.100).aspx)</span><span class="sxs-lookup"><span data-stu-id="b5cb0-128">[ASP.NET Configuration Settings Schema](https://msdn.microsoft.com/library/b5ysx397(v=vs.100).aspx)</span></span> | <span data-ttu-id="b5cb0-129">ASP.NET 웹 사이트 및 응용 프로그램을 구성 하기 위한 요소를 포함 하는 ASP.NET 구성 스키마의 모든 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cb0-129">All elements in the ASP.NET configuration schema, which includes elements for configuring ASP.NET Web sites and applications.</span></span> <span data-ttu-id="b5cb0-130">레지스트리에 *Web.config* 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cb0-130">Used in *Web.config* files.</span></span> |
| [<span data-ttu-id="b5cb0-131">**\<webServices >** 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="b5cb0-131">**\<webServices>** Settings Schema</span></span>](https://msdn.microsoft.com/f84d6d55-1add-4eb7-ae46-33df5833ea2e) | <span data-ttu-id="b5cb0-132">웹 서비스 설정 스키마의 모든 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cb0-132">All elements in the Web services settings schema.</span></span> |
| [<span data-ttu-id="b5cb0-133">웹 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="b5cb0-133">Web Settings Schema</span></span>](~/docs/framework/configure-apps/file-schema/web/index.md) | <span data-ttu-id="b5cb0-134">ASP.NET이 IIS와 같은 호스트 응용 프로그램과 함께 작동하는 방법을 구성하기 위한 요소를 비롯한 웹 설정 스키마의 모든 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cb0-134">All elements in the Web settings schema, which includes elements for configuring how ASP.NET works with a host application such as IIS.</span></span> <span data-ttu-id="b5cb0-135">레지스트리에 *aspnet.config* 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cb0-135">Used in *aspnet.config* files.</span></span> |

## <a name="remarks"></a><span data-ttu-id="b5cb0-136">설명</span><span class="sxs-lookup"><span data-stu-id="b5cb0-136">Remarks</span></span>

<span data-ttu-id="b5cb0-137">각 구성 파일 하나만 있어야  **\<구성 >** 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b5cb0-137">Each configuration file must contain exactly one **\<configuration>** element.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5cb0-138">참고자료</span><span class="sxs-lookup"><span data-stu-id="b5cb0-138">See also</span></span>

[<span data-ttu-id="b5cb0-139">.NET Framework의 구성 파일 스키마</span><span class="sxs-lookup"><span data-stu-id="b5cb0-139">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)
