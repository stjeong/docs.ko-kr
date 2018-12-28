---
title: '&lt;disableCommitThreadStack&gt; 요소'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/disableCommitThreadStack
- http://schemas.microsoft.com/.NetConfiguration/v2.0#disableCommitThreadStack
helpviewer_keywords:
- <disableCommitThreadStack> element
- disableCommitThreadStack element
ms.assetid: 3559d46a-7640-4c72-9a11-7e980768929e
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 69b2c9f3bbd4fb7562272903d3ab78e3a4312298
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53611648"
---
# <a name="ltdisablecommitthreadstackgt-element"></a><span data-ttu-id="6e5a3-102">&lt;disableCommitThreadStack&gt; 요소</span><span class="sxs-lookup"><span data-stu-id="6e5a3-102">&lt;disableCommitThreadStack&gt; Element</span></span>
<span data-ttu-id="6e5a3-103">스레드가 시작될 때 전체 스레드 스택을 커밋할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-103">Specifies whether the full thread stack is committed when a thread is started.</span></span>  
  
 <span data-ttu-id="6e5a3-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="6e5a3-104">\<configuration></span></span>  
<span data-ttu-id="6e5a3-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="6e5a3-105">\<runtime></span></span>  
<span data-ttu-id="6e5a3-106">\<disableCommitThreadStack ></span><span class="sxs-lookup"><span data-stu-id="6e5a3-106">\<disableCommitThreadStack></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6e5a3-107">구문</span><span class="sxs-lookup"><span data-stu-id="6e5a3-107">Syntax</span></span>  
  
```xml  
<disableCommitThreadStack enabled="0|1"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6e5a3-108">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="6e5a3-108">Attributes and Elements</span></span>  
 <span data-ttu-id="6e5a3-109">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6e5a3-110">특성</span><span class="sxs-lookup"><span data-stu-id="6e5a3-110">Attributes</span></span>  
  
|<span data-ttu-id="6e5a3-111">특성</span><span class="sxs-lookup"><span data-stu-id="6e5a3-111">Attribute</span></span>|<span data-ttu-id="6e5a3-112">설명</span><span class="sxs-lookup"><span data-stu-id="6e5a3-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6e5a3-113">사용</span><span class="sxs-lookup"><span data-stu-id="6e5a3-113">enabled</span></span>|<span data-ttu-id="6e5a3-114">필수 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-114">Required attribute.</span></span><br /><br /> <span data-ttu-id="6e5a3-115">스레드 시작 시 전체 스레드 스택 커밋하기(기본 동작)의 해제 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-115">Specifies whether committing the full thread stack on thread startup (the default behavior) is disabled.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="6e5a3-116">enabled 특성</span><span class="sxs-lookup"><span data-stu-id="6e5a3-116">enabled Attribute</span></span>  
  
|<span data-ttu-id="6e5a3-117">값</span><span class="sxs-lookup"><span data-stu-id="6e5a3-117">Value</span></span>|<span data-ttu-id="6e5a3-118">설명</span><span class="sxs-lookup"><span data-stu-id="6e5a3-118">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="6e5a3-119">0</span><span class="sxs-lookup"><span data-stu-id="6e5a3-119">0</span></span>|<span data-ttu-id="6e5a3-120">스레드가 시작될 때 전체 스레드 스택을 커밋하는 공용 언어 런타임의 기본 동작을 해제하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-120">Do not disable the default behavior of the common language runtime, which is to commit the full thread stack when a thread is started.</span></span>|  
|<span data-ttu-id="6e5a3-121">1</span><span class="sxs-lookup"><span data-stu-id="6e5a3-121">1</span></span>|<span data-ttu-id="6e5a3-122">스레드가 시작될 때 전체 스레드 스택을 커밋하는 공용 언어 런타임의 기본 동작을 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-122">Disable the default behavior of the common language runtime, which is to commit the full thread stack when a thread is started.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6e5a3-123">자식 요소</span><span class="sxs-lookup"><span data-stu-id="6e5a3-123">Child Elements</span></span>  
 <span data-ttu-id="6e5a3-124">없음</span><span class="sxs-lookup"><span data-stu-id="6e5a3-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6e5a3-125">부모 요소</span><span class="sxs-lookup"><span data-stu-id="6e5a3-125">Parent Elements</span></span>  
  
|<span data-ttu-id="6e5a3-126">요소</span><span class="sxs-lookup"><span data-stu-id="6e5a3-126">Element</span></span>|<span data-ttu-id="6e5a3-127">설명</span><span class="sxs-lookup"><span data-stu-id="6e5a3-127">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="6e5a3-128">공용 언어 런타임 및 [!INCLUDE[dnprdnshort](../../../../../includes/dnprdnshort-md.md)] 응용 프로그램에서 사용하는 모든 구성 파일의 루트 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-128">The root element in every configuration file used by the common language runtime and [!INCLUDE[dnprdnshort](../../../../../includes/dnprdnshort-md.md)] applications.</span></span>|  
|`runtime`|<span data-ttu-id="6e5a3-129">어셈블리 바인딩 및 가비지 컬렉션에 대한 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-129">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6e5a3-130">설명</span><span class="sxs-lookup"><span data-stu-id="6e5a3-130">Remarks</span></span>  
 <span data-ttu-id="6e5a3-131">공용 언어 런타임의 기본 동작은 스레드가 시작될 때 전체 스레드 스택을 커밋하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-131">The default behavior of the common language runtime is to commit the full thread stack when a thread is started.</span></span> <span data-ttu-id="6e5a3-132">메모리가 제한적인 서버에서 대량의 스레드를 만들어야 하며 이러한 스레드 대부분이 스택 공간을 매우 적게 사용하는 경우, 스레드가 시작될 때 공용 언어 런타임이 전체 스레드 스택을 즉시 커밋하지 않는다면 서버 성능이 개선될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-132">If a large number of threads must be created on a server that has limited memory, and most of those threads will use very little stack space, the server might perform better if the common language runtime does not commit the full thread stack immediately when a thread is started.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6e5a3-133">관리되지 않는 호스트는 `STARTUP_DISABLE_COMMITTHREADSTACK` STARTUP_FLAGS [열거형에서](../../../../../docs/framework/unmanaged-api/hosting/startup-flags-enumeration.md) 시작 플래그를 사용하면 동일한 결과를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-133">Unmanaged hosts can use the `STARTUP_DISABLE_COMMITTHREADSTACK` startup flag in the [STARTUP_FLAGS](../../../../../docs/framework/unmanaged-api/hosting/startup-flags-enumeration.md) enumeration to accomplish the same result.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6e5a3-134">예제</span><span class="sxs-lookup"><span data-stu-id="6e5a3-134">Example</span></span>  
 <span data-ttu-id="6e5a3-135">다음 예제에서는 스레드 시작 시 전체 스레드 스택을 커밋하는 공용 언어 런타임의 기본 동작을 해제하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6e5a3-135">The following example shows how to disable the default behavior of the common language runtime, which is to commit the full thread stack on thread startup.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <disableCommitThreadStack enabled="1" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="6e5a3-136">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6e5a3-136">See Also</span></span>  
- [<span data-ttu-id="6e5a3-137">런타임 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="6e5a3-137">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
- [<span data-ttu-id="6e5a3-138">구성 파일 스키마</span><span class="sxs-lookup"><span data-stu-id="6e5a3-138">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
