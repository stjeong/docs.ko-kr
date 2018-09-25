---
title: '&lt;sessionSecurityTokenCache&gt;'
ms.date: 03/30/2017
ms.assetid: d43e676c-0153-485c-ab31-0257a2db7507
author: BrucePerlerMS
ms.openlocfilehash: b812673ac1c015adde357d3c0707d85643aad3e9
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47084334"
---
# <a name="ltsessionsecuritytokencachegt"></a>&lt;sessionSecurityTokenCache&gt;
서비스 또는 보안 토큰 처리기 컬렉션을 사용 하 여 세션 토큰에 대 한 캐시를 등록합니다.  
  
 \<system.identityModel>  
\<identityConfiguration>  
\<캐시 >  
\<sessionSecurityTokenCache >  
  
## <a name="syntax"></a>구문  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <caches>  
      <sessionSecurityTokenCache type=xs:string>  
      </sessionSecurityTokenCache>  
    </caches>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a>특성 및 요소  
 다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.  
  
### <a name="attributes"></a>특성  
  
|특성|설명|  
|---------------|-----------------|  
|type|형식에서 파생 되는 <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache> 클래스입니다.|  
  
### <a name="child-elements"></a>자식 요소  
 없음  
  
### <a name="parent-elements"></a>부모 요소  
  
|요소|설명|  
|-------------|-----------------|  
|[\<캐시 >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/caches.md)|서비스 또는 보안 토큰 처리기 컬렉션을 사용 하는 캐시를 등록 합니다.|  
  
## <a name="example"></a>예제  
 다음 XML 세션 보안 토큰을 보관 하기 위한 사용자 지정 캐시 구성을 보여 줍니다 (<xref:System.IdentityModel.Tokens.SessionSecurityToken>). 구성에서 가져온 것은 `ClaimsAwareWebFarm` 샘플입니다. 이 샘플에 대 한 자세한 내용은 참조 하세요. [WIF 코드 샘플 인덱스](../../../../../docs/framework/security/wif-code-sample-index.md)합니다.  
  
```xml  
<caches>  
  <sessionSecurityTokenCache type="CacheLibrary.SharedSessionSecurityTokenCache, CacheLibrary">  
    <!--cacheServiceAddress points to the centralized session security token cache service running in the web farm.-->  
    <cacheServiceAddress url="http://localhost:4161/SessionSecurityTokenCacheService.svc" />  
  </sessionSecurityTokenCache>  
</caches>  
```  
  
## <a name="see-also"></a>참고 항목  
 <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache>
