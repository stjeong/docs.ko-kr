---
title: <states>의 <activityStateQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: a7cc2018-2b79-44f1-825a-bb7ca08690a3
ms.openlocfilehash: 97664518f7c7c0078cef1c81035724a02c9857c0
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55257735"
---
# <a name="states-of-activitystatequery"></a>\<states> of \<activityStateQuery>
추적 레코드를 내보내야 할 구독된 활동의 상태를 포함하는 구성 요소의 컬렉션입니다.  
  
 추적 프로필 쿼리에 대 한 자세한 내용은 참조 하세요. [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)합니다.  
  
\<system.serviceModel>  
\<tracking>  
\<trackingProfile>  
\<workflow>  
\<activityStateQueries>  
\<activityStateQuery>  
\<states>  
  
## <a name="syntax"></a>구문  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <activityStateQueries>
        <activityStateQuery activityName="String" />
        <states>
          <state name="String" />
        </states>
      </activityStateQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a>특성 및 요소  
 다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.  
  
### <a name="attributes"></a>특성  
 없음  
  
### <a name="child-elements"></a>자식 요소  
  
|요소|설명|  
|-------------|-----------------|  
|[\<state>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/state-of-states.md)|추적 레코드를 내보내야 할 구독된 활동의 상태를 포함하는 구성 요소입니다.|  
  
### <a name="parent-elements"></a>부모 요소  
  
|요소|설명|  
|-------------|-----------------|  
|[\<activityStateQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)|부모 활동에 의한 자식 활동 취소 요청을 추적하는 데 사용되는 구성 요소를 나타냅니다. 추적 참가자가 취소 요청 레코드 개체를 구독하려면 쿼리가 필요합니다.|  
  
## <a name="remarks"></a>설명  
 ActivityStateQuery의 한 가지 고유한 특징은 워크플로 실행을 추적할 때 데이터를 추출하는 기능입니다. 이 기능은 추적 레코드 사후 실행에 액세스할 때 추가 컨텍스트를 제공합니다. 사용할 수는 [ \<인수 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/arguments.md)를 [ \<상태 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) 고 [ \<상태 >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md) 변수 또는 인수를 추출 하는 요소 워크플로의 모든 활동입니다. 다음 예제에서는 활동의 `Closed` 추적 레코드를 내보낼 때 변수와 인수를 추출하는 활동 상태 쿼리를 보여 줍니다. ActivityStateRecord 사용해 서만 추출할 수 있으므로 구독 하는 추적 내에서 변수 및 인수를 사용 하 여 프로 파일링 [ \<activityStateQuery >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activitystatequery.md)합니다.  
  
```xml  
<activityStateQuery activityName="SendEmailActivity">  
  <states>  
    <state name="Closed"/>  
  </states>  
  <variables>  
    <variable name="FromAddress"/>  
  </variables>  
  <arguments>  
    <argument name="Result"/>  
  </arguments>  
</activityStateQuery>  
```  
  
## <a name="see-also"></a>참고자료
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.ActivityStateQuery?displayProperty=nameWithType>
- [워크플로 추적](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [추적 프로필](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
