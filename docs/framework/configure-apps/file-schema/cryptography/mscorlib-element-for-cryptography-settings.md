---
title: '&lt;mscorlib&gt; 암호화 설정에 대 한 요소'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#mscorlib
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib
helpviewer_keywords:
- mscorlib element
- <mscorlib> element
ms.assetid: d549668f-31f1-4b92-8021-a9135c09ca3c
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 6a8a589077aba413fa89518e560373df816f8943
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50187847"
---
# <a name="ltmscorlibgt-element-for-cryptography-settings"></a><span data-ttu-id="dd734-102">&lt;mscorlib&gt; 암호화 설정에 대 한 요소</span><span class="sxs-lookup"><span data-stu-id="dd734-102">&lt;mscorlib&gt; Element for Cryptography Settings</span></span>
<span data-ttu-id="dd734-103">포함 된 [ \<cryptographySettings > 요소](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptographysettings-element.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="dd734-103">Contains the [\<cryptographySettings> element](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptographysettings-element.md).</span></span>  
  
 <span data-ttu-id="dd734-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="dd734-104">\<configuration></span></span>  
<span data-ttu-id="dd734-105">\<mscorlib ></span><span class="sxs-lookup"><span data-stu-id="dd734-105">\<mscorlib></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dd734-106">구문</span><span class="sxs-lookup"><span data-stu-id="dd734-106">Syntax</span></span>  
  
```xml  
      <mscorlib>   
</mscorlib>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="dd734-107">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="dd734-107">Attributes and Elements</span></span>  
 <span data-ttu-id="dd734-108">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="dd734-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="dd734-109">특성</span><span class="sxs-lookup"><span data-stu-id="dd734-109">Attributes</span></span>  
 <span data-ttu-id="dd734-110">없음</span><span class="sxs-lookup"><span data-stu-id="dd734-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="dd734-111">자식 요소</span><span class="sxs-lookup"><span data-stu-id="dd734-111">Child Elements</span></span>  
  
|<span data-ttu-id="dd734-112">요소</span><span class="sxs-lookup"><span data-stu-id="dd734-112">Element</span></span>|<span data-ttu-id="dd734-113">설명</span><span class="sxs-lookup"><span data-stu-id="dd734-113">Description</span></span>|  
|-------------|-----------------|  
|`cryptographySettings`|<span data-ttu-id="dd734-114">암호화 설정이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd734-114">Contains cryptography settings.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="dd734-115">부모 요소</span><span class="sxs-lookup"><span data-stu-id="dd734-115">Parent Elements</span></span>  
  
|<span data-ttu-id="dd734-116">요소</span><span class="sxs-lookup"><span data-stu-id="dd734-116">Element</span></span>|<span data-ttu-id="dd734-117">설명</span><span class="sxs-lookup"><span data-stu-id="dd734-117">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="dd734-118">공용 언어 런타임 및 .NET Framework 응용 프로그램에서 사용하는 모든 구성 파일의 루트 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="dd734-118">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="dd734-119">예제</span><span class="sxs-lookup"><span data-stu-id="dd734-119">Example</span></span>  
 <span data-ttu-id="dd734-120">다음 예제에서는 사용 하는 방법을 보여 줍니다 합니다  **\<mscorlib >** 암호화 클래스를 참조 하 고 런타임 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="dd734-120">The following example shows how to use the **\<mscorlib>** element to reference a cryptography class and to configure the runtime.</span></span> <span data-ttu-id="dd734-121">"RSA" 문자열을 전달할 수 있습니다는 <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> 메서드 및 사용법을 <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> 반환 하는 방법을 `MyCryptoRSAClass` 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="dd734-121">You can then pass the string "RSA" to the <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> method and use the <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> method to return a `MyCryptoRSAClass` object.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="dd734-122">참고 항목</span><span class="sxs-lookup"><span data-stu-id="dd734-122">See Also</span></span>  
- <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A>  
- <xref:System.Security.Cryptography>  
- [<span data-ttu-id="dd734-123">구성 파일 스키마</span><span class="sxs-lookup"><span data-stu-id="dd734-123">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
- [<span data-ttu-id="dd734-124">암호화 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="dd734-124">Cryptography Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)  
- [<span data-ttu-id="dd734-125">Cryptographic Services</span><span class="sxs-lookup"><span data-stu-id="dd734-125">Cryptographic Services</span></span>](../../../../../docs/standard/security/cryptographic-services.md)  
- [<span data-ttu-id="dd734-126">암호화 클래스 구성</span><span class="sxs-lookup"><span data-stu-id="dd734-126">Configuring Cryptography Classes</span></span>](../../../../../docs/framework/configure-apps/configure-cryptography-classes.md)
