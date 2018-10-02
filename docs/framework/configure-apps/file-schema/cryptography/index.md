---
title: 암호화 설정 스키마
ms.date: 03/30/2017
helpviewer_keywords:
- configuration schema [.NET Framework], cryptography
- elements [.NET Framework], cryptography
- schema configuration settings
- cryptography, settings schema
- cryptography, mapping algorithm names
- configuration sections [.NET Framework]
- configuration settings [.NET Framework], cryptography
ms.assetid: 1f55050a-b2a3-4868-a3c0-da20826150f3
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 71d2edac1dd9a84c9d3c92049d2494c7c5bd54b0
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/02/2018
ms.locfileid: "48028221"
---
# <a name="cryptography-settings-schema"></a><span data-ttu-id="41eab-102">암호화 설정 스키마</span><span class="sxs-lookup"><span data-stu-id="41eab-102">Cryptography Settings Schema</span></span>
<span data-ttu-id="41eab-103">암호 설정 스키마에는 암호화 알고리즘을 구현하는 클래스에 알고리즘 이름을 매핑하는 방법을 지정하는 요소가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41eab-103">The cryptography settings schema contains elements that specify how to map friendly algorithm names to classes that implement cryptography algorithms.</span></span>  
  
 [<span data-ttu-id="41eab-104">**\<configuration>**</span><span class="sxs-lookup"><span data-stu-id="41eab-104">**\<configuration>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)  
  
 [<span data-ttu-id="41eab-105">**\<mscorlib>**</span><span class="sxs-lookup"><span data-stu-id="41eab-105">**\<mscorlib>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/mscorlib-element-for-cryptography-settings.md)  
  
 [<span data-ttu-id="41eab-106">**\<cryptographySettings>**</span><span class="sxs-lookup"><span data-stu-id="41eab-106">**\<cryptographySettings>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptographysettings-element.md)  
  
 [<span data-ttu-id="41eab-107">**\<cryptoNameMapping>**</span><span class="sxs-lookup"><span data-stu-id="41eab-107">**\<cryptoNameMapping>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptonamemapping-element.md)  
  
 [<span data-ttu-id="41eab-108">**\<cryptoClasses>**</span><span class="sxs-lookup"><span data-stu-id="41eab-108">**\<cryptoClasses>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptoclasses-element.md)  
  
 [<span data-ttu-id="41eab-109">**\<cryptoClass>**</span><span class="sxs-lookup"><span data-stu-id="41eab-109">**\<cryptoClass>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptoclass-element.md)  
  
 [<span data-ttu-id="41eab-110">**\<nameEntry>**</span><span class="sxs-lookup"><span data-stu-id="41eab-110">**\<nameEntry>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md)  
  
 [<span data-ttu-id="41eab-111">**\<oidMap>**</span><span class="sxs-lookup"><span data-stu-id="41eab-111">**\<oidMap>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/oidmap-element.md)  
  
 [<span data-ttu-id="41eab-112">**\<oidEntry>**</span><span class="sxs-lookup"><span data-stu-id="41eab-112">**\<oidEntry>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/oidentry-element.md)  
  
|<span data-ttu-id="41eab-113">요소</span><span class="sxs-lookup"><span data-stu-id="41eab-113">Element</span></span>|<span data-ttu-id="41eab-114">설명</span><span class="sxs-lookup"><span data-stu-id="41eab-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="41eab-115">**\<cryptoClasses**></span><span class="sxs-lookup"><span data-stu-id="41eab-115">**\<cryptoClasses**></span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptoclasses-element.md)|<span data-ttu-id="41eab-116">**\<nameEntry>** 요소에 있는 이름에 매핑되는 암호화 클래스의 목록이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41eab-116">Contains a list of cryptography classes that have a mapping to a friendly name in the **\<nameEntry>** element.</span></span>|  
|[<span data-ttu-id="41eab-117">**\<cryptoClass**></span><span class="sxs-lookup"><span data-stu-id="41eab-117">**\<cryptoClass**></span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptoclass-element.md)|<span data-ttu-id="41eab-118">**\<nameEntry>** 요소에 있는 이름에 매핑되는 암호화 클래스가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41eab-118">Contains a cryptography class that has a mapping to a friendly name in the **\<nameEntry>** element.</span></span>|  
|[<span data-ttu-id="41eab-119">**\<cryptographySettings**></span><span class="sxs-lookup"><span data-stu-id="41eab-119">**\<cryptographySettings**></span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptographysettings-element.md)|<span data-ttu-id="41eab-120">암호화 설정이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41eab-120">Contains cryptography settings.</span></span>|  
|[<span data-ttu-id="41eab-121">**\<cryptoNameMapping**></span><span class="sxs-lookup"><span data-stu-id="41eab-121">**\<cryptoNameMapping**></span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptonamemapping-element.md)|<span data-ttu-id="41eab-122">이름에 대한 클래스의 매핑이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41eab-122">Contains mappings of classes to friendly names.</span></span>|  
|[<span data-ttu-id="41eab-123">암호화 설정에 대한 **\<mscorlib>** 요소</span><span class="sxs-lookup"><span data-stu-id="41eab-123">**\<mscorlib>** element for cryptography settings</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/mscorlib-element-for-cryptography-settings.md)|<span data-ttu-id="41eab-124">**\<cryptographySettings>** 요소가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41eab-124">Contains the **\<cryptographySettings>** element.</span></span>|  
|[<span data-ttu-id="41eab-125">**\<nameEntry>**</span><span class="sxs-lookup"><span data-stu-id="41eab-125">**\<nameEntry>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md)|<span data-ttu-id="41eab-126">클래스 이름을 알고리즘 이름에 매핑하며, 이를 통해 하나의 클래스가 여러 이름을 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41eab-126">Maps a class name to a friendly algorithm name, which allows one class to have many friendly names.</span></span>|  
|[<span data-ttu-id="41eab-127">**\<oidEntry>**</span><span class="sxs-lookup"><span data-stu-id="41eab-127">**\<oidEntry>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/oidentry-element.md)|<span data-ttu-id="41eab-128">ASN.1 OID(개체 식별자)를 이름에 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="41eab-128">Maps an ASN.1 object identifier (OID) to a friendly name.</span></span>|  
|[<span data-ttu-id="41eab-129">**\<oidMap>**</span><span class="sxs-lookup"><span data-stu-id="41eab-129">**\<oidMap>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/oidmap-element.md)|<span data-ttu-id="41eab-130">클래스에 대한 ASN.1 OID 매핑이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41eab-130">Contains ASN.1 OID mappings to classes.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="41eab-131">참고 항목</span><span class="sxs-lookup"><span data-stu-id="41eab-131">See Also</span></span>  
 [<span data-ttu-id="41eab-132">구성 파일 스키마</span><span class="sxs-lookup"><span data-stu-id="41eab-132">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="41eab-133">암호화 서비스</span><span class="sxs-lookup"><span data-stu-id="41eab-133">Cryptographic Services</span></span>](../../../../../docs/standard/security/cryptographic-services.md)
