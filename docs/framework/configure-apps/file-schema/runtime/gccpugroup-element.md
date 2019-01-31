---
title: <GCCpuGroup> 요소
ms.date: 03/30/2017
helpviewer_keywords:
- GCCpuGroup element
- <GCCpuGroup> element
ms.assetid: c1fc7d6c-7220-475c-a312-5b8b201f66e0
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a389403d58bb0b4fb4f98e25d2c9a6b2cf337281
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55264640"
---
# <a name="gccpugroup-element"></a><span data-ttu-id="3296a-102">\<GCCpuGroup > 요소</span><span class="sxs-lookup"><span data-stu-id="3296a-102">\<GCCpuGroup> Element</span></span>
<span data-ttu-id="3296a-103">가비지 수집에서 여러 CPU 그룹을 지원할지를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3296a-103">Specifies whether garbage collection supports multiple CPU groups.</span></span>  
  
 <span data-ttu-id="3296a-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="3296a-104">\<configuration></span></span>  
<span data-ttu-id="3296a-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="3296a-105">\<runtime></span></span>  
<span data-ttu-id="3296a-106">\<GCCpuGroup></span><span class="sxs-lookup"><span data-stu-id="3296a-106">\<GCCpuGroup></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3296a-107">구문</span><span class="sxs-lookup"><span data-stu-id="3296a-107">Syntax</span></span>  
  
```xml  
<GCCpuGroup    
   enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3296a-108">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="3296a-108">Attributes and Elements</span></span>  
 <span data-ttu-id="3296a-109">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="3296a-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3296a-110">특성</span><span class="sxs-lookup"><span data-stu-id="3296a-110">Attributes</span></span>  
  
|<span data-ttu-id="3296a-111">특성</span><span class="sxs-lookup"><span data-stu-id="3296a-111">Attribute</span></span>|<span data-ttu-id="3296a-112">설명</span><span class="sxs-lookup"><span data-stu-id="3296a-112">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="3296a-113">필수 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="3296a-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="3296a-114">가비지 수집에서 여러 CPU 그룹을 지원할지를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3296a-114">Specifies whether garbage collection supports multiple CPU groups.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="3296a-115">enabled 특성</span><span class="sxs-lookup"><span data-stu-id="3296a-115">enabled Attribute</span></span>  
  
|<span data-ttu-id="3296a-116">값</span><span class="sxs-lookup"><span data-stu-id="3296a-116">Value</span></span>|<span data-ttu-id="3296a-117">설명</span><span class="sxs-lookup"><span data-stu-id="3296a-117">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="3296a-118">가비지 수집에서 여러 CPU 그룹을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3296a-118">Garbage collection does not support multiple CPU groups.</span></span> <span data-ttu-id="3296a-119">이 값이 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="3296a-119">This is the default.</span></span>|  
|`true`|<span data-ttu-id="3296a-120">가비지 수집이 서버 가비지 수집을 사용 하는 경우 여러 CPU 그룹을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3296a-120">Garbage collection supports multiple CPU groups, if server garbage collection is enabled.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3296a-121">자식 요소</span><span class="sxs-lookup"><span data-stu-id="3296a-121">Child Elements</span></span>  
 <span data-ttu-id="3296a-122">없음</span><span class="sxs-lookup"><span data-stu-id="3296a-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3296a-123">부모 요소</span><span class="sxs-lookup"><span data-stu-id="3296a-123">Parent Elements</span></span>  
  
|<span data-ttu-id="3296a-124">요소</span><span class="sxs-lookup"><span data-stu-id="3296a-124">Element</span></span>|<span data-ttu-id="3296a-125">설명</span><span class="sxs-lookup"><span data-stu-id="3296a-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="3296a-126">공용 언어 런타임 및 .NET Framework 애플리케이션에서 사용하는 모든 구성 파일의 루트 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="3296a-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="3296a-127">어셈블리 바인딩 및 가비지 컬렉션에 대한 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="3296a-127">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3296a-128">설명</span><span class="sxs-lookup"><span data-stu-id="3296a-128">Remarks</span></span>  
 <span data-ttu-id="3296a-129">컴퓨터에 여러 CPU 그룹이 시간과 서버 가비지 컬렉션이 설정 되었는지 (참조를 [ \<gcServer >](../../../../../docs/framework/configure-apps/file-schema/runtime/gcserver-element.md) 요소), 모든 CPU 그룹에 걸쳐 가비지 컬렉션을 확장 하 고 모든 코어에는이 요소를 사용 하도록 설정 계정 만들기 및 힙 분산 하는 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="3296a-129">When a computer has multiple CPU groups and server garbage collection is enabled (see the [\<gcServer>](../../../../../docs/framework/configure-apps/file-schema/runtime/gcserver-element.md) element), enabling this element extends garbage collection across all CPU groups and takes all cores into account when creating and balancing heaps.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3296a-130">이 요소는 가비지 수집 스레드에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3296a-130">This element applies only to garbage collection threads.</span></span> <span data-ttu-id="3296a-131">런타임이 모든 CPU 그룹에 사용자 스레드를 분산할 수 있도록 설정할 수도 있습니다는 [< Thread_UseAllCpuGroups >](../../../../../docs/framework/configure-apps/file-schema/runtime/thread-useallcpugroups-element.md) 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="3296a-131">To enable the runtime to distribute user threads across all CPU groups, you must also enable the [<Thread_UseAllCpuGroups>](../../../../../docs/framework/configure-apps/file-schema/runtime/thread-useallcpugroups-element.md) element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3296a-132">예제</span><span class="sxs-lookup"><span data-stu-id="3296a-132">Example</span></span>  
 <span data-ttu-id="3296a-133">다음 예제에서는 여러 CPU 그룹에 대 한 가비지 수집을 사용 하도록 설정 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3296a-133">The following example shows how to enable garbage collection for multiple CPU groups.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <GCCpuGroup enabled="true"/>  
      <gcServer enabled="true"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="3296a-134">참고자료</span><span class="sxs-lookup"><span data-stu-id="3296a-134">See also</span></span>
- [<span data-ttu-id="3296a-135">런타임 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="3296a-135">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="3296a-136">구성 파일 스키마</span><span class="sxs-lookup"><span data-stu-id="3296a-136">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="3296a-137">방법: 동시 가비지 수집을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="3296a-137">How to: Disable Concurrent Garbage Collection</span></span>](https://msdn.microsoft.com/library/ba2c6c67-5778-497c-9fac-5f793b5500c7)
- [<span data-ttu-id="3296a-138">워크스테이션 및 서버 가비지 수집</span><span class="sxs-lookup"><span data-stu-id="3296a-138">Workstation and server garbage collection</span></span>](../../../../../docs/standard/garbage-collection/fundamentals.md#workstation_and_server_garbage_collection)
