---
title: '&lt;developmentMode&gt; 요소'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/developmentMode
- http://schemas.microsoft.com/.NetConfiguration/v2.0#developmentMode
helpviewer_keywords:
- developmentMode element
- container tags, <developmentMode> element
- <developmentMode> element
ms.assetid: 60e79a8c-415a-497d-be29-b9d0fd9bdee3
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 982bc04e362f82760226b1cd2b8b3febe9cc7107
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53612051"
---
# <a name="ltdevelopmentmodegt-element"></a><span data-ttu-id="874e0-102">&lt;developmentMode&gt; 요소</span><span class="sxs-lookup"><span data-stu-id="874e0-102">&lt;developmentMode&gt; Element</span></span>
<span data-ttu-id="874e0-103">런타임이 DEVPATH 환경 변수로 지정된 디렉터리에서 어셈블리를 검색할지를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="874e0-103">Specifies whether the runtime searches for assemblies in directories specified by the DEVPATH environment variable.</span></span>  
  
 <span data-ttu-id="874e0-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="874e0-104">\<configuration></span></span>  
<span data-ttu-id="874e0-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="874e0-105">\<runtime></span></span>  
<span data-ttu-id="874e0-106">\<developmentMode ></span><span class="sxs-lookup"><span data-stu-id="874e0-106">\<developmentMode></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="874e0-107">구문</span><span class="sxs-lookup"><span data-stu-id="874e0-107">Syntax</span></span>  
  
```xml  
<developmentMode developerInstallation="true | false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="874e0-108">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="874e0-108">Attributes and Elements</span></span>  
 <span data-ttu-id="874e0-109">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="874e0-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="874e0-110">특성</span><span class="sxs-lookup"><span data-stu-id="874e0-110">Attributes</span></span>  
  
|<span data-ttu-id="874e0-111">특성</span><span class="sxs-lookup"><span data-stu-id="874e0-111">Attribute</span></span>|<span data-ttu-id="874e0-112">설명</span><span class="sxs-lookup"><span data-stu-id="874e0-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="874e0-113">**developerInstallation**</span><span class="sxs-lookup"><span data-stu-id="874e0-113">**developerInstallation**</span></span>|<span data-ttu-id="874e0-114">런타임이 DEVPATH 환경 변수로 지정된 디렉터리에서 어셈블리를 검색할지를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="874e0-114">Specifies whether the runtime searches for assemblies in directories specified by the DEVPATH environment variable.</span></span>|  
  
## <a name="developerinstallation-attribute"></a><span data-ttu-id="874e0-115">developerInstallation 특성</span><span class="sxs-lookup"><span data-stu-id="874e0-115">developerInstallation Attribute</span></span>  
  
|<span data-ttu-id="874e0-116">값</span><span class="sxs-lookup"><span data-stu-id="874e0-116">Value</span></span>|<span data-ttu-id="874e0-117">설명</span><span class="sxs-lookup"><span data-stu-id="874e0-117">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="874e0-118">**true**</span><span class="sxs-lookup"><span data-stu-id="874e0-118">**true**</span></span>|<span data-ttu-id="874e0-119">DEVPATH 환경 변수로 지정 된 디렉터리에서 어셈블리를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="874e0-119">Searches for assemblies in directories specified by the DEVPATH environment variable.</span></span>|  
|<span data-ttu-id="874e0-120">**false**</span><span class="sxs-lookup"><span data-stu-id="874e0-120">**false**</span></span>|<span data-ttu-id="874e0-121">DEVPATH 환경 변수로 지정 된 디렉터리에서 어셈블리에 대 한 검색 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="874e0-121">Does not search for assemblies in directories specified by the DEVPATH environment variable.</span></span> <span data-ttu-id="874e0-122">이것이 기본값</span><span class="sxs-lookup"><span data-stu-id="874e0-122">This is the default</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="874e0-123">자식 요소</span><span class="sxs-lookup"><span data-stu-id="874e0-123">Child Elements</span></span>  
 <span data-ttu-id="874e0-124">없음</span><span class="sxs-lookup"><span data-stu-id="874e0-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="874e0-125">부모 요소</span><span class="sxs-lookup"><span data-stu-id="874e0-125">Parent Elements</span></span>  
  
|<span data-ttu-id="874e0-126">요소</span><span class="sxs-lookup"><span data-stu-id="874e0-126">Element</span></span>|<span data-ttu-id="874e0-127">설명</span><span class="sxs-lookup"><span data-stu-id="874e0-127">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="874e0-128">공용 언어 런타임 및 .NET Framework 응용 프로그램에서 사용하는 모든 구성 파일의 루트 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="874e0-128">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="874e0-129">어셈블리 바인딩 및 가비지 컬렉션에 대한 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="874e0-129">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="874e0-130">설명</span><span class="sxs-lookup"><span data-stu-id="874e0-130">Remarks</span></span>  
 <span data-ttu-id="874e0-131">개발 타임에만이 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="874e0-131">Use this setting only at development time.</span></span> <span data-ttu-id="874e0-132">런타임에서 DEVPATH에 있는 강력한 이름의 어셈블리의 버전을 확인 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="874e0-132">The runtime does not check the versions on strong-named assemblies found in the DEVPATH.</span></span> <span data-ttu-id="874e0-133">단순히 찾은 첫 번째 어셈블리를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="874e0-133">It simply uses the first assembly it finds.</span></span>  
  
## <a name="example"></a><span data-ttu-id="874e0-134">예제</span><span class="sxs-lookup"><span data-stu-id="874e0-134">Example</span></span>  
 <span data-ttu-id="874e0-135">다음 예제에서는 런타임이 DEVPATH 환경 변수로 지정 된 디렉터리에서 어셈블리를 검색 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="874e0-135">The following example shows how to cause the runtime to search for assemblies in directories specified by the DEVPATH environment variable.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <developmentMode developerInstallation="true"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="874e0-136">참고 항목</span><span class="sxs-lookup"><span data-stu-id="874e0-136">See Also</span></span>  
- [<span data-ttu-id="874e0-137">런타임 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="874e0-137">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
- [<span data-ttu-id="874e0-138">구성 파일 스키마</span><span class="sxs-lookup"><span data-stu-id="874e0-138">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
- [<span data-ttu-id="874e0-139">방법: DEVPATH를 사용 하 여 어셈블리를 찾습니다</span><span class="sxs-lookup"><span data-stu-id="874e0-139">How to: Locate Assemblies by Using DEVPATH</span></span>](../../../../../docs/framework/configure-apps/how-to-locate-assemblies-by-using-devpath.md)
