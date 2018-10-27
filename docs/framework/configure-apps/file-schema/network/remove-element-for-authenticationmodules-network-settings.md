---
title: '&lt;제거&gt; authenticationModules (네트워크 설정)에 대 한 요소'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/authenticationModules/remove
- http://schemas.microsoft.com/.NetConfiguration/v2.0#remove
helpviewer_keywords:
- remove element, authenticationModules
- <authenticationModules>, remove element
- <remove> element, authenticationModules
- authenticationModules, remove element
ms.assetid: abf79949-b05c-465a-b51c-bbeda9a74173
ms.openlocfilehash: 65b5b7f717912ecaee73a5b24e65d22b902a4e44
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50180707"
---
# <a name="ltremovegt-element-for-authenticationmodules-network-settings"></a>&lt;제거&gt; authenticationModules (네트워크 설정)에 대 한 요소
응용 프로그램에서 인증 모듈을 제거합니다.  
  
 \<configuration>  
\<system.net>  
\<authenticationModules >  
\<remove>  
  
## <a name="syntax"></a>구문  
  
```xml  
<remove   
   type="authentication module name"   
/>  
```  
  
## <a name="attributes-and-elements"></a>특성 및 요소  
 다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.  
  
### <a name="attributes"></a>특성  
  
|**특성**|**설명**|  
|-------------------|---------------------|  
|**type**|제거할 인증 모듈의 이름입니다.|  
  
### <a name="child-elements"></a>자식 요소  
 없음  
  
### <a name="parent-elements"></a>부모 요소  
  
|**요소**|**설명**|  
|-----------------|---------------------|  
|[authenticationModules](../../../../../docs/framework/configure-apps/file-schema/network/authenticationmodules-element-network-settings.md)|네트워크 요청을 인증 하는 데 사용 되는 모듈을 지정 합니다.|  
  
## <a name="remarks"></a>설명  
 `remove` 요소 또는 구성 계층 구조의 상위 수준 구성 파일에서 이전에 정의 된 인증 모듈을 제거 합니다.  
  
 에 대 한 값을 `type` 특성에는 올바른 클래스 이름 이어야 합니다.  
  
## <a name="configuration-files"></a>구성 파일  
 이 요소는 응용 프로그램 구성 파일 또는 컴퓨터 구성 파일(Machine.config)에서 사용할 수 있습니다.  
  
## <a name="example"></a>예제  
 다음 예제에서는 인증 모듈을 제거 합니다.  
  
```xml  
<configuration>  
  <system.net>  
    <authenticationModules>  
      <remove type="System.Net.NtlmClient" />  
    </authenticationModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a>참고 항목  
- <xref:System.Net.IAuthenticationModule>  
- <xref:System.Net.AuthenticationManager>  
- [네트워크 설정 스키마](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
