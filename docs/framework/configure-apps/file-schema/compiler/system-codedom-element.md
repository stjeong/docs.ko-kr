---
title: '&lt;system.codedom&gt; 요소'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.codedom
- http://schemas.microsoft.com/.NetConfiguration/v2.0#system.codedom
helpviewer_keywords:
- compiler configuration elements, <system.codedom> element
- system.codedom element
- <system.codedom> element
ms.assetid: 672a68f7-e69f-4479-ac30-e980085ec4fe
author: mcleblanc
ms.author: markl
ms.openlocfilehash: ea9fd06887c9a4bc9f121945f27753dfc666cfec
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47078392"
---
# <a name="ltsystemcodedomgt-element"></a><span data-ttu-id="0bf5b-102">&lt;system.codedom&gt; 요소</span><span class="sxs-lookup"><span data-stu-id="0bf5b-102">&lt;system.codedom&gt; Element</span></span>
<span data-ttu-id="0bf5b-103">사용 가능한 언어 공급자에 대한 컴파일러 구성 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-103">Specifies compiler configuration settings for available language providers.</span></span>  
  
 <span data-ttu-id="0bf5b-104">\<구성 > 요소</span><span class="sxs-lookup"><span data-stu-id="0bf5b-104">\<configuration> Element</span></span>  
<span data-ttu-id="0bf5b-105">\<system.codedom > 요소</span><span class="sxs-lookup"><span data-stu-id="0bf5b-105">\<system.codedom> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0bf5b-106">구문</span><span class="sxs-lookup"><span data-stu-id="0bf5b-106">Syntax</span></span>  
  
```xml  
<system.codedom>  
  <compilers> ... </compilers>  
</system.codedom>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0bf5b-107">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="0bf5b-107">Attributes and Elements</span></span>  
 <span data-ttu-id="0bf5b-108">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0bf5b-109">특성</span><span class="sxs-lookup"><span data-stu-id="0bf5b-109">Attributes</span></span>  
 <span data-ttu-id="0bf5b-110">없음</span><span class="sxs-lookup"><span data-stu-id="0bf5b-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="0bf5b-111">자식 요소</span><span class="sxs-lookup"><span data-stu-id="0bf5b-111">Child Elements</span></span>  
  
|<span data-ttu-id="0bf5b-112">요소</span><span class="sxs-lookup"><span data-stu-id="0bf5b-112">Element</span></span>|<span data-ttu-id="0bf5b-113">설명</span><span class="sxs-lookup"><span data-stu-id="0bf5b-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0bf5b-114">\<compilers></span><span class="sxs-lookup"><span data-stu-id="0bf5b-114">\<compilers></span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)|<span data-ttu-id="0bf5b-115">컴파일러 구성 요소용 컨테이너입니다. 0개 이상의 [\<compiler>](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md) 요소가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-115">Container for compiler configuration elements; contains zero or more [\<compiler>](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md) elements.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0bf5b-116">부모 요소</span><span class="sxs-lookup"><span data-stu-id="0bf5b-116">Parent Elements</span></span>  
  
|<span data-ttu-id="0bf5b-117">요소</span><span class="sxs-lookup"><span data-stu-id="0bf5b-117">Element</span></span>|<span data-ttu-id="0bf5b-118">설명</span><span class="sxs-lookup"><span data-stu-id="0bf5b-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0bf5b-119">\<구성></span><span class="sxs-lookup"><span data-stu-id="0bf5b-119">\<configuration></span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|<span data-ttu-id="0bf5b-120">공용 언어 런타임 및 .NET Framework 응용 프로그램에서 사용하는 모든 구성 파일의 루트 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-120">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0bf5b-121">설명</span><span class="sxs-lookup"><span data-stu-id="0bf5b-121">Remarks</span></span>  
  
## <a name="net-framework-version-20"></a><span data-ttu-id="0bf5b-122">.NET framework 버전 2.0</span><span class="sxs-lookup"><span data-stu-id="0bf5b-122">.NET Framework Version 2.0</span></span>  
 <span data-ttu-id="0bf5b-123">합니다 [ \<system.codedom >](../../../../../docs/framework/configure-apps/file-schema/compiler/system-codedom-element.md) 요소와 같은.NET Framework와 함께 설치 되는 기본 공급자 외에도 컴퓨터에 설치 된 언어 공급자에 대 한 컴파일러 구성 설정을 포함 합니다 <xref:Microsoft.CSharp.CSharpCodeProvider> 하며 <xref:Microsoft.VisualBasic.VBCodeProvider>합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-123">The [\<system.codedom>](../../../../../docs/framework/configure-apps/file-schema/compiler/system-codedom-element.md) element contains compiler configuration settings for language providers installed on a computer in addition to the default providers that are installed with the .NET Framework, such as the <xref:Microsoft.CSharp.CSharpCodeProvider> and the <xref:Microsoft.VisualBasic.VBCodeProvider>.</span></span> <span data-ttu-id="0bf5b-124">합니다 [ \<컴파일러 >](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md) 요소에는 0 개 이상 포함 되어 [ \<컴파일러 >](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md) 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-124">The [\<compilers>](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md) element contains zero or more [\<compiler>](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md) elements.</span></span> <span data-ttu-id="0bf5b-125">각 [ \<컴파일러 >](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md) 요소는 특정 언어 공급자에 대 한 컴파일러 구성 특성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-125">Each [\<compiler>](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md) element specifies the compiler configuration attributes for a specific language provider.</span></span>  
  
 <span data-ttu-id="0bf5b-126">개발자 및 컴파일러 공급 구성 설정을 추가할 수 컴퓨터 구성 파일 (Machine.config)에 새 <xref:System.CodeDom.Compiler.CodeDomProvider> 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-126">Developers and compiler vendors can add configuration settings to the machine configuration file (Machine.config) for a new <xref:System.CodeDom.Compiler.CodeDomProvider> implementation.</span></span> <span data-ttu-id="0bf5b-127">사용 된 <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> 기본 언어 공급자 및 컴퓨터 컴파일러 구성 설정에 의해 식별 된 언어 공급자를 프로그래밍 방식으로 열거 하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-127">Use the <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> method to programmatically enumerate both the default language providers and language providers identified by the compiler configuration settings on a computer.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0bf5b-128">.NET Framework 버전 1.0 및 1.1에서는.NET Framework에서 제공 하는 공급자에서 식별 된 기본 언어를 [ \<컴파일러 >](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md) 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-128">In the .NET Framework versions 1.0 and 1.1, the default language providers supplied by the .NET Framework are identified in the [\<compilers>](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md) element.</span></span> <span data-ttu-id="0bf5b-129">.NET framework 버전 2.0에서 기본 언어 공급자에서 식별 되지 않습니다 합니다 [ \<컴파일러 >](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md) 요소를 사용 하 여 열거할 수 있지만 <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A> 메서드.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-129">In the .NET Framework version 2.0, the default language providers are not identified in the [\<compilers>](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md) element, but can be enumerated using the <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A> method.</span></span>  
  
## <a name="net-framework-versions-10-and-11"></a><span data-ttu-id="0bf5b-130">.NET framework 버전 1.0 및 1.1</span><span class="sxs-lookup"><span data-stu-id="0bf5b-130">.NET Framework Versions 1.0 and 1.1</span></span>  
 <span data-ttu-id="0bf5b-131">합니다 [ \<system.codedom >](../../../../../docs/framework/configure-apps/file-schema/compiler/system-codedom-element.md) 요소는 컴퓨터의 언어 공급자에 대 한 컴파일러 구성 설정을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-131">The [\<system.codedom>](../../../../../docs/framework/configure-apps/file-schema/compiler/system-codedom-element.md) element contains the compiler configuration settings for language providers on a computer.</span></span> <span data-ttu-id="0bf5b-132">합니다 [ \<컴파일러 >](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md) 요소에는 0 개 이상 포함 되어 [ \<컴파일러 >](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md) 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-132">The [\<compilers>](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md) element contains zero or more [\<compiler>](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md) elements.</span></span> <span data-ttu-id="0bf5b-133">각 [ \<컴파일러 >](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md) 요소는 특정 언어 공급자에 대 한 컴파일러 구성 특성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-133">Each [\<compiler>](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md) element specifies the compiler configuration attributes for a specific language provider.</span></span>  
  
 <span data-ttu-id="0bf5b-134">.NET Framework는 컴퓨터 구성 파일(Machine.config)의 초기 컴파일러 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-134">The .NET Framework defines the initial compiler settings in the machine configuration file (Machine.config).</span></span> <span data-ttu-id="0bf5b-135">개발자 및 컴파일러 공급업체는 새로운 <xref:System.CodeDom.Compiler.CodeDomProvider> 구현에 대한 구성 설정을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-135">Developers and compiler vendors can add configuration settings for a new <xref:System.CodeDom.Compiler.CodeDomProvider> implementation.</span></span> <span data-ttu-id="0bf5b-136"><xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> 메서드를 사용하여 컴퓨터에서 언어 공급자 및 컴파일러 구성 설정을 프로그래밍 방식으로 열거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-136">Use the <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> method to programmatically enumerate language provider and compiler configuration settings on a computer.</span></span>  
  
## <a name="configuration-file"></a><span data-ttu-id="0bf5b-137">구성 파일</span><span class="sxs-lookup"><span data-stu-id="0bf5b-137">Configuration File</span></span>  
 <span data-ttu-id="0bf5b-138">컴퓨터 구성 파일 및 응용 프로그램 구성 파일에서이 요소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-138">This element can be used in the machine configuration file and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0bf5b-139">예제</span><span class="sxs-lookup"><span data-stu-id="0bf5b-139">Example</span></span>  
 <span data-ttu-id="0bf5b-140">다음 예제에서는 일반적인 컴파일러 구성을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0bf5b-140">The following example illustrates a typical compiler configuration.</span></span>  
  
```xml  
<configuration>  
  <system.codedom>  
    <compilers>  
      <!-- zero or more compiler elements -->  
      <compiler   
        language="c#;cs;csharp"  
        extension=".cs"  
        type="Microsoft.CSharp.CSharpCodeProvider, System,   
          Version=1.0.5000.0, Culture=neutral,   
          PublicKeyToken=b77a5c561934e089"  
        compilerOptions=""  
        warningLevel="1" />  
    </compilers>  
  </system.codedom>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="0bf5b-141">참고 항목</span><span class="sxs-lookup"><span data-stu-id="0bf5b-141">See Also</span></span>  
 <xref:System.CodeDom.Compiler.CompilerInfo>  
 <xref:System.CodeDom.Compiler.CodeDomProvider>  
 [<span data-ttu-id="0bf5b-142">구성 파일 스키마</span><span class="sxs-lookup"><span data-stu-id="0bf5b-142">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="0bf5b-143">컴파일러 및 언어 공급자 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="0bf5b-143">Compiler and Language Provider Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/index.md)  
 [<span data-ttu-id="0bf5b-144">\<compiler> 요소</span><span class="sxs-lookup"><span data-stu-id="0bf5b-144">\<compiler> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md)
