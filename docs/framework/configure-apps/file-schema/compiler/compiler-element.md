---
title: '&lt;컴파일러&gt; 요소'
ms.date: 08/14/2018
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#compiler
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.codedom/compilers/compiler
helpviewer_keywords:
- compiler configuration elements, <compiler> element
- <compiler> element
- compiler configuration attributes
- compiler element
ms.assetid: 7a151659-b803-4c27-b5ce-1c4aa0d5a823
author: mcleblanc
ms.author: markl
ms.openlocfilehash: a26fc0bda341e85ca54f3dee4addd14e4164209c
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47071023"
---
# <a name="ltcompilergt-element"></a><span data-ttu-id="b5b3b-102">&lt;컴파일러&gt; 요소</span><span class="sxs-lookup"><span data-stu-id="b5b3b-102">&lt;compiler&gt; Element</span></span>

<span data-ttu-id="b5b3b-103">언어 공급자에 대한 컴파일러 구성 특성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-103">Specifies the compiler configuration attributes for a language provider.</span></span>

<span data-ttu-id="b5b3b-104">\<구성 요소 > \<system.codedom 요소 > \<compilers 요소 > \<컴파일러 > 요소</span><span class="sxs-lookup"><span data-stu-id="b5b3b-104">\<configuration Element> \<system.codedom Element> \<compilers Element> \<compiler> Element</span></span>

## <a name="syntax"></a><span data-ttu-id="b5b3b-105">구문</span><span class="sxs-lookup"><span data-stu-id="b5b3b-105">Syntax</span></span>

```xml
<compiler
  language="languageName[;...;...]"
  extension="fileExtension[;...;...]"
  type="typeName, assemblyName"
  warningLevel="number"
  compilerOptions="option1 option2"
/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="b5b3b-106">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="b5b3b-106">Attributes and Elements</span></span>

<span data-ttu-id="b5b3b-107">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-107">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="b5b3b-108">특성</span><span class="sxs-lookup"><span data-stu-id="b5b3b-108">Attributes</span></span>

|<span data-ttu-id="b5b3b-109">특성</span><span class="sxs-lookup"><span data-stu-id="b5b3b-109">Attribute</span></span>|<span data-ttu-id="b5b3b-110">설명</span><span class="sxs-lookup"><span data-stu-id="b5b3b-110">Description</span></span>|
|---------------|-----------------|
|`compilerOptions`|<span data-ttu-id="b5b3b-111">선택적 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-111">Optional attribute.</span></span><br /><br /> <span data-ttu-id="b5b3b-112">컴파일에 추가 컴파일러 별 인수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-112">Specifies additional compiler-specific arguments for compilation.</span></span> <span data-ttu-id="b5b3b-113">에 대 한 값을 `compilerOptions` 특성 일반적으로 컴파일러에 대 한 컴파일러 옵션 항목에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-113">The values for the `compilerOptions` attribute are typically listed in a compiler options topic for the compiler.</span></span>|
|`extension`|<span data-ttu-id="b5b3b-114">필수 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-114">Required attribute.</span></span><br /><br /> <span data-ttu-id="b5b3b-115">언어 공급자에 대 한 소스 파일에서 사용 하는 파일 이름 확장명의 세미콜론으로 구분 된 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-115">Provides a semicolon-separated list of file name extensions used by source files for the language provider.</span></span> <span data-ttu-id="b5b3b-116">예를 들어, ".cs"가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-116">For example, ".cs".</span></span>|
|`language`|<span data-ttu-id="b5b3b-117">필수 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-117">Required attribute.</span></span><br /><br /> <span data-ttu-id="b5b3b-118">언어 공급자에서 지 원하는 언어 이름의 세미콜론으로 구분 된 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-118">Provides a semicolon-separated list of language names supported by the language provider.</span></span> <span data-ttu-id="b5b3b-119">예를 들어, "c#; cs; csharp"입니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-119">For example, "c#;cs;csharp".</span></span>|
|`type`|<span data-ttu-id="b5b3b-120">필수 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-120">Required attribute.</span></span><br /><br /> <span data-ttu-id="b5b3b-121">공급자 구현이 들어 있는 어셈블리의 이름을 포함 한 언어 공급자의 형식 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-121">Specifies the type name of the language provider, including the name of the assembly containing the provider implementation.</span></span> <span data-ttu-id="b5b3b-122">형식 이름에 정의 된 요구 사항에 맞아야 [정규화 된 형식 이름 지정](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-122">The type name must meet the requirements defined in [Specifying Fully Qualified Type Names](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span></span>|
|`warningLevel`|<span data-ttu-id="b5b3b-123">선택적 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-123">Optional attribute.</span></span><br /><br /> <span data-ttu-id="b5b3b-124">기본 컴파일러 경고 수준을;를 지정합니다. 컴파일 경고를 오류로 언어 공급자는 처리 수준을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-124">Specifies the default compiler warning level; determines the level at which the language provider treats compilation warnings as errors.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="b5b3b-125">자식 요소</span><span class="sxs-lookup"><span data-stu-id="b5b3b-125">Child Elements</span></span>

|<span data-ttu-id="b5b3b-126">요소</span><span class="sxs-lookup"><span data-stu-id="b5b3b-126">Element</span></span>|<span data-ttu-id="b5b3b-127">설명</span><span class="sxs-lookup"><span data-stu-id="b5b3b-127">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="b5b3b-128">\<providerOption > 요소</span><span class="sxs-lookup"><span data-stu-id="b5b3b-128">\<providerOption> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/provideroption-element.md)|<span data-ttu-id="b5b3b-129">언어 공급자에 대 한 컴파일러 버전 특성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-129">Specifies compiler version attributes for a language provider.</span></span>|

### <a name="parent-elements"></a><span data-ttu-id="b5b3b-130">부모 요소</span><span class="sxs-lookup"><span data-stu-id="b5b3b-130">Parent Elements</span></span>

|<span data-ttu-id="b5b3b-131">요소</span><span class="sxs-lookup"><span data-stu-id="b5b3b-131">Element</span></span>|<span data-ttu-id="b5b3b-132">설명</span><span class="sxs-lookup"><span data-stu-id="b5b3b-132">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="b5b3b-133">\<configuration> 요소</span><span class="sxs-lookup"><span data-stu-id="b5b3b-133">\<configuration> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|<span data-ttu-id="b5b3b-134">공용 언어 런타임 및 .NET Framework 응용 프로그램에서 사용하는 모든 구성 파일의 루트 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-134">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|
|[<span data-ttu-id="b5b3b-135">\<system.codedom > 요소</span><span class="sxs-lookup"><span data-stu-id="b5b3b-135">\<system.codedom> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/system-codedom-element.md)|<span data-ttu-id="b5b3b-136">사용 가능한 언어 공급자에 대한 컴파일러 구성 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-136">Specifies compiler configuration settings for available language providers.</span></span>|
|[<span data-ttu-id="b5b3b-137">\<컴파일러 > 요소</span><span class="sxs-lookup"><span data-stu-id="b5b3b-137">\<compilers> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)|<span data-ttu-id="b5b3b-138">컴파일러 구성 요소에 대 한 컨테이너 0 개 이상 포함 `<compiler>` 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-138">Container for compiler configuration elements; contains zero or more `<compiler>` elements.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b5b3b-139">설명</span><span class="sxs-lookup"><span data-stu-id="b5b3b-139">Remarks</span></span>

<span data-ttu-id="b5b3b-140">각 `<compiler>` 요소는 특정 언어 공급자에 대 한 컴파일러 구성 특성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-140">Each `<compiler>` element specifies the compiler configuration attributes for a specific language provider.</span></span> <span data-ttu-id="b5b3b-141">공급자 확장 합니다 <xref:System.CodeDom.Compiler.CodeDomProvider?displayProperty=nameWithType> ; 특정 언어에 대 한 클래스는 `<compiler>` 컴파일러 및 언어 공급자에 대 한 코드 생성기 설정 요소를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-141">The provider extends the <xref:System.CodeDom.Compiler.CodeDomProvider?displayProperty=nameWithType> class for a specific language; the `<compiler>` element defines the compiler and code generator settings for the language provider.</span></span>

<span data-ttu-id="b5b3b-142">.NET Framework는 컴퓨터 구성 파일(Machine.config)의 초기 컴파일러 설정을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-142">The .NET Framework defines the initial compiler settings in the machine configuration file (Machine.config).</span></span> <span data-ttu-id="b5b3b-143">개발자 및 컴파일러 공급업체는 새로운 <xref:System.CodeDom.Compiler.CodeDomProvider> 구현에 대한 구성 설정을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-143">Developers and compiler vendors can add configuration settings for a new <xref:System.CodeDom.Compiler.CodeDomProvider> implementation.</span></span> <span data-ttu-id="b5b3b-144"><xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> 메서드를 사용하여 컴퓨터에서 언어 공급자 및 컴파일러 구성 설정을 프로그래밍 방식으로 열거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-144">Use the <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> method to programmatically enumerate language provider and compiler configuration settings on a computer.</span></span>

<span data-ttu-id="b5b3b-145">응용 프로그램 또는 웹 구성 파일에서 컴파일러 요소 보완 하거나 컴퓨터 구성 파일의 설정을 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-145">Compiler elements in the application or Web configuration file can supplement or override the settings in the machine configuration file.</span></span> <span data-ttu-id="b5b3b-146">동일한 언어 이름 또는 파일 확장명으로 둘 이상의 공급자 구현을 구성 된 경우 마지막으로 일치 하는 구성 해당 언어 이름 또는 파일 확장에 대 한 모든 이전 구성된 공급자를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-146">If more than one provider implementation is configured for the same language name or the same file extension, the last matching configuration overrides any previous configured providers for that language name or file extension.</span></span>

## <a name="configuration-file"></a><span data-ttu-id="b5b3b-147">구성 파일</span><span class="sxs-lookup"><span data-stu-id="b5b3b-147">Configuration File</span></span>

<span data-ttu-id="b5b3b-148">컴퓨터 구성 파일 및 응용 프로그램 구성 파일에서이 요소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-148">This element can be used in the machine configuration file and the application configuration file.</span></span>

## <a name="example"></a><span data-ttu-id="b5b3b-149">예제</span><span class="sxs-lookup"><span data-stu-id="b5b3b-149">Example</span></span>

<span data-ttu-id="b5b3b-150">다음 예제에서는 일반적인 컴파일러 구성 요소를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b5b3b-150">The following example illustrates a typical compiler configuration element:</span></span>

```xml
<configuration>
  <system.codedom>
    <compilers>
      <!-- zero or more compiler elements -->
      <compiler
        language="c#;cs;csharp"
        extension=".cs"
        type="Microsoft.CSharp.CSharpCodeProvider, System,
          Version=2.0.3600.0, Culture=neutral,
          PublicKeyToken=b77a5c561934e089"
        compilerOptions="/optimize"
        warningLevel="1" />
    </compilers>
  </system.codedom>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="b5b3b-151">참고 항목</span><span class="sxs-lookup"><span data-stu-id="b5b3b-151">See Also</span></span>

- <xref:System.CodeDom.Compiler.CompilerInfo>
- <xref:System.CodeDom.Compiler.CodeDomProvider>
- [<span data-ttu-id="b5b3b-152">구성 파일 스키마</span><span class="sxs-lookup"><span data-stu-id="b5b3b-152">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="b5b3b-153">\<컴파일러 > 요소</span><span class="sxs-lookup"><span data-stu-id="b5b3b-153">\<compilers> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)
- <span data-ttu-id="b5b3b-154">[지정 완전히 정규화 된 형식 이름]-(... /.. /.. /.. /.. / docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md)</span><span class="sxs-lookup"><span data-stu-id="b5b3b-154">[Specifying Fully Qualified Type Names]-(../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md)</span></span>
- <span data-ttu-id="b5b3b-155">[컴파일 (ASP.NET 설정 스키마)에 대 한 컴파일러에 대 한 compiler 요소](https://msdn.microsoft.com/library/f7d6b078-5d42-4134-b3f7-62e1aba1df1e(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="b5b3b-155">[compiler Element for compilers for compilation (ASP.NET Settings Schema)](https://msdn.microsoft.com/library/f7d6b078-5d42-4134-b3f7-62e1aba1df1e(v=vs.100))</span></span>
