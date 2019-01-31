---
title: <add>의 <backupList>
ms.date: 03/30/2017
ms.assetid: bc5939fc-314a-4ea4-a533-c96958da7173
ms.openlocfilehash: e61ee275a7e98f13370504f5f15fdbe62a8221bd
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55285794"
---
# <a name="add-of-backuplist"></a>\<추가 >의 \<backupList >
백업 엔드포인트 요소를 정의하는 구성 요소를 나타냅니다.  
  
 \<system.serviceModel>  
\<라우팅 >  
\<backupLists>  
\<backupList>  
\<add>  
  
## <a name="syntax"></a>구문  
  
```xml  
<routing>
  <backupLists>
    <backupList name="String">
      <add endpointName="String" />
    </backupList>
  </backupLists>
</routing>
```  
  
```csharp  
```  
  
## <a name="attributes-and-elements"></a>특성 및 요소  
 다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.  
  
### <a name="attributes"></a>특성  
  
|특성|설명|  
|---------------|-----------------|  
|name|백업 엔드포인트의 이름을 지정하는 문자열입니다.|  
  
### <a name="child-elements"></a>자식 요소  
 없음  
  
### <a name="parent-elements"></a>부모 요소  
  
|요소|설명|  
|-------------|-----------------|  
|[\<routing>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|원하는 경우 기본 끝점에 연결할 수 없습니다를 사용 하도록 라우팅 서비스는 끝점의 목록을 포함 합니다.|  
  
## <a name="see-also"></a>참고자료
- <xref:System.ServiceModel.Routing.Configuration.BackupEndpointElement?displayProperty=nameWithType>
