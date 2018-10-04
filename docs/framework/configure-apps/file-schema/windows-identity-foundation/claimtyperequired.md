---
title: '&lt;claimTypeRequired&gt;'
ms.date: 03/30/2017
ms.assetid: c469d71f-6c77-4a24-97aa-53efa126ceef
author: BrucePerlerMS
ms.openlocfilehash: df4494de6b76943849db2bedef8f43ad894b6bd1
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48780663"
---
# <a name="ltclaimtyperequiredgt"></a>&lt;claimTypeRequired&gt;
들어오는 보안 토큰에 대 한 필수 클레임 집합을 지정 합니다.  
  
 \<system.identityModel>  
\<identityConfiguration>  
\<claimTypeRequired >  
  
## <a name="syntax"></a>구문  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <claimTypeRequired>  
    </claimTypeRequired>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a>특성 및 요소  
 다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.  
  
### <a name="attributes"></a>특성  
 없음  
  
### <a name="child-elements"></a>자식 요소  
  
|요소|설명|  
|-------------|-----------------|  
|[\<claimType >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/claimtype.md)|들어오는 보안 토큰에 대 한 단일 옵션 또는 필요한 클레임을 지정합니다.|  
  
### <a name="parent-elements"></a>부모 요소  
  
|요소|설명|  
|-------------|-----------------|  
|[\<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|서비스 수준 id 설정을 지정합니다.|
