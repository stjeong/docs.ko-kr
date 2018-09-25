---
title: '&lt;cryptoClass&gt; 요소'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings/cryptoNameMapping/cryptoClasses/cryptoClass
- http://schemas.microsoft.com/.NetConfiguration/v2.0#cryptoClass
helpviewer_keywords:
- cryptoClass element
- <cryptoClass> element
ms.assetid: 03db52ef-010e-44ea-b6fd-b9c900ecad50
author: mcleblanc
ms.author: markl
ms.openlocfilehash: e74cc5fa99473562b158cd5068fb8bbaeb6a4a17
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47083915"
---
# <a name="ltcryptoclassgt-element"></a><span data-ttu-id="53d84-102">&lt;cryptoClass&gt; 요소</span><span class="sxs-lookup"><span data-stu-id="53d84-102">&lt;cryptoClass&gt; Element</span></span>
<span data-ttu-id="53d84-103">[\<nameEntry>](../../../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md) 요소에 있는 이름에 매핑되는 암호화 클래스가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53d84-103">Contains a cryptography class that has a mapping to a friendly name in the [\<nameEntry>](../../../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md) element.</span></span>  
  
 <span data-ttu-id="53d84-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="53d84-104">\<configuration></span></span>  
<span data-ttu-id="53d84-105">\<mscorlib ></span><span class="sxs-lookup"><span data-stu-id="53d84-105">\<mscorlib></span></span>  
<span data-ttu-id="53d84-106">\<cryptographySettings ></span><span class="sxs-lookup"><span data-stu-id="53d84-106">\<cryptographySettings></span></span>  
<span data-ttu-id="53d84-107">\<cryptoNameMapping ></span><span class="sxs-lookup"><span data-stu-id="53d84-107">\<cryptoNameMapping></span></span>  
<span data-ttu-id="53d84-108">\<cryptoClasses ></span><span class="sxs-lookup"><span data-stu-id="53d84-108">\<cryptoClasses></span></span>  
<span data-ttu-id="53d84-109">\<cryptoClass ></span><span class="sxs-lookup"><span data-stu-id="53d84-109">\<cryptoClass></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="53d84-110">구문</span><span class="sxs-lookup"><span data-stu-id="53d84-110">Syntax</span></span>  
  
```xml  
<cryptoClass customClassName="fully qualified type name" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="53d84-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="53d84-111">Attributes and Elements</span></span>  
 <span data-ttu-id="53d84-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="53d84-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="53d84-113">특성</span><span class="sxs-lookup"><span data-stu-id="53d84-113">Attributes</span></span>  
  
|<span data-ttu-id="53d84-114">특성</span><span class="sxs-lookup"><span data-stu-id="53d84-114">Attribute</span></span>|<span data-ttu-id="53d84-115">설명</span><span class="sxs-lookup"><span data-stu-id="53d84-115">Description</span></span>|  
|---------------|-----------------|  
|`customClassName`|<span data-ttu-id="53d84-116">필수 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="53d84-116">Required attribute.</span></span><br /><br /> <span data-ttu-id="53d84-117">암호화 클래스에 대 한 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="53d84-117">Contains the information for the cryptography class.</span></span> <span data-ttu-id="53d84-118">클래스에 대 한 짧은 이름을 제공 하기 위해이 특성을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d84-118">Use this attribute to provide a short name for your class.</span></span> <span data-ttu-id="53d84-119">에 지정 된 요구 사항을 충족 하는 문자열을 지정 해야 합니다 [정규화 된 형식 이름 지정](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="53d84-119">You must specify a string that meets the requirements specified in [Specifying Fully Qualified Type Names](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="53d84-120">자식 요소</span><span class="sxs-lookup"><span data-stu-id="53d84-120">Child Elements</span></span>  
 <span data-ttu-id="53d84-121">없음</span><span class="sxs-lookup"><span data-stu-id="53d84-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="53d84-122">부모 요소</span><span class="sxs-lookup"><span data-stu-id="53d84-122">Parent Elements</span></span>  
  
|<span data-ttu-id="53d84-123">요소</span><span class="sxs-lookup"><span data-stu-id="53d84-123">Element</span></span>|<span data-ttu-id="53d84-124">설명</span><span class="sxs-lookup"><span data-stu-id="53d84-124">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="53d84-125">공용 언어 런타임 및 .NET Framework 응용 프로그램에서 사용하는 모든 구성 파일의 루트 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="53d84-125">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`cryptoClasses`|<span data-ttu-id="53d84-126">[\<nameEntry>](../../../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md) 요소에 있는 이름에 매핑되는 암호화 클래스의 목록이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53d84-126">Contains a list of cryptography classes that have a mapping to a friendly name in the [\<nameEntry>](../../../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md) element.</span></span>|  
|`cryptographySettings`|<span data-ttu-id="53d84-127">암호화 설정이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53d84-127">Contains cryptography settings.</span></span>|  
|`cryptoNameMapping`|<span data-ttu-id="53d84-128">이름에 대한 클래스의 매핑이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53d84-128">Contains mappings of classes to friendly names.</span></span>|  
|`mscorlib`|<span data-ttu-id="53d84-129">[\<cryptographySettings>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptographysettings-element.md) 요소가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53d84-129">Contains the [\<cryptographySettings>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptographysettings-element.md) element.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="53d84-130">예제</span><span class="sxs-lookup"><span data-stu-id="53d84-130">Example</span></span>  
 <span data-ttu-id="53d84-131">다음 방법을 보여 주는 예제는  **\<cryptoClass >** 암호화 클래스를 참조 하 고 런타임 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="53d84-131">The following example shows how use the **\<cryptoClass>** element to reference a cryptography class and to configure the runtime.</span></span> <span data-ttu-id="53d84-132">"RSA" 문자열을 전달할 수 있습니다는 <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> 메서드 및 사용법을 <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> 반환 하는 방법을 `MyCryptoRSAClass` 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="53d84-132">You can then pass the string "RSA" to the <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> method and use the <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> method to return a `MyCryptoRSAClass` object.</span></span>  
  
```xml  
<configuration>  
   <mscorlib>  
      <cryptographySettings>  
         <cryptoNameMapping>  
            <cryptoClasses>  
               <cryptoClass   MyCryptoRSA="MyCryptoRSAClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
            </cryptoClasses>  
            <nameEntry name="RSA" class="MyCryptoRSA"/>  
            <nameEntry name="System.Security.Cryptography.AsymmetricAlgorithm"  
                       class="MyCryptoRSA"/>  
         </cryptoNameMapping>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="53d84-133">참고 항목</span><span class="sxs-lookup"><span data-stu-id="53d84-133">See Also</span></span>  
 [<span data-ttu-id="53d84-134">구성 파일 스키마</span><span class="sxs-lookup"><span data-stu-id="53d84-134">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="53d84-135">암호화 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="53d84-135">Cryptography Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)  
 [<span data-ttu-id="53d84-136">암호화 서비스</span><span class="sxs-lookup"><span data-stu-id="53d84-136">Cryptographic Services</span></span>](../../../../../docs/standard/security/cryptographic-services.md)  
 [<span data-ttu-id="53d84-137">암호화 클래스 구성</span><span class="sxs-lookup"><span data-stu-id="53d84-137">Configuring Cryptography Classes</span></span>](../../../../../docs/framework/configure-apps/configure-cryptography-classes.md)
