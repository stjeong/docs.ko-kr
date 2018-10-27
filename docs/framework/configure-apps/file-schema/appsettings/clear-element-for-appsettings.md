---
title: '&lt;지우기&gt; 요소에 대 한 &lt;appSettings&gt;'
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/appSettings/clear
helpviewer_keywords:
- clear Element
- <clear> Element
ms.assetid: 6d18c7be-27db-438b-8fb5-765d396b0b7b
author: guardrex
ms.author: mairaw
ms.openlocfilehash: bc52e3149c213925ea64a8421ee65befeea4161e
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50184220"
---
# <a name="clear-element-for-appsettings"></a><span data-ttu-id="db205-102">\<지우기 > 요소에 대 한 \<appSettings ></span><span class="sxs-lookup"><span data-stu-id="db205-102">\<clear> element for \<appSettings></span></span>

<span data-ttu-id="db205-103">사용자 지정 응용 프로그램 설정을 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="db205-103">Clears custom application settings.</span></span>

<span data-ttu-id="db205-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="db205-104">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="db205-105">&nbsp;&nbsp;[**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) </span><span class="sxs-lookup"><span data-stu-id="db205-105">&nbsp;&nbsp;[**\<appSettings>**](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) </span></span>  
<span data-ttu-id="db205-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<지우기 >**</span><span class="sxs-lookup"><span data-stu-id="db205-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<clear>**</span></span>

## <a name="syntax"></a><span data-ttu-id="db205-107">구문</span><span class="sxs-lookup"><span data-stu-id="db205-107">Syntax</span></span>

```xml
<appSettings>
  <clear />
</appSettings>
```

## <a name="attributes"></a><span data-ttu-id="db205-108">특성</span><span class="sxs-lookup"><span data-stu-id="db205-108">Attributes</span></span>

<span data-ttu-id="db205-109">없음</span><span class="sxs-lookup"><span data-stu-id="db205-109">None</span></span>

## <a name="parent-element"></a><span data-ttu-id="db205-110">부모 요소</span><span class="sxs-lookup"><span data-stu-id="db205-110">Parent element</span></span>

|     | <span data-ttu-id="db205-111">설명</span><span class="sxs-lookup"><span data-stu-id="db205-111">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="db205-112">**\<appSettings>**</span><span class="sxs-lookup"><span data-stu-id="db205-112">**\<appSettings>**</span></span>](~/docs/framework/configure-apps/file-schema/appsettings/appsettings-element-for-configuration.md) | <span data-ttu-id="db205-113">파일 경로, XML 웹 서비스 Url 또는 기타 사용자 지정 응용 프로그램 구성 정보와 같은 사용자 지정 응용 프로그램 설정을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="db205-113">Contains custom application settings, such as file paths, XML Web service URLs, or any other custom application configuration information.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="db205-114">자식 요소</span><span class="sxs-lookup"><span data-stu-id="db205-114">Child elements</span></span>

<span data-ttu-id="db205-115">없음</span><span class="sxs-lookup"><span data-stu-id="db205-115">None</span></span>

## <a name="example"></a><span data-ttu-id="db205-116">예제</span><span class="sxs-lookup"><span data-stu-id="db205-116">Example</span></span>

<span data-ttu-id="db205-117">다음 예제에서는 사용자 지정 구성 설정의 선택을 취소 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="db205-117">The following example shows how to clear custom configuration settings:</span></span>

```xml
<appSettings>
  <clear />
</appSettings>
```

## <a name="see-also"></a><span data-ttu-id="db205-118">참고자료</span><span class="sxs-lookup"><span data-stu-id="db205-118">See also</span></span>

- [<span data-ttu-id="db205-119">.NET Framework의 구성 파일 스키마</span><span class="sxs-lookup"><span data-stu-id="db205-119">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)
