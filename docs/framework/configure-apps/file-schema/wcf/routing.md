---
title: '&lt;라우팅&gt;'
ms.date: 03/30/2017
ms.assetid: a210c209-3940-4288-9a8e-39b1e62606bc
ms.openlocfilehash: 220c18ab8ea6222fcf7d9fb8a93950281c9de796
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145148"
---
# <a name="ltroutinggt"></a>&lt;라우팅&gt;

Windows Communication Foundation (WCF)의 형식을 결정 하는 라우팅 필터 집합을 정의 하기 위한 구성 섹션을 나타냅니다 <xref:System.ServiceModel.Dispatcher.MessageFilter> 사용할 대상 끝점을 정의 하는 들어오는 메시지를 평가할 수 있을 뿐만 아니라 라우팅 테이블 필터가 일치할 때에 메시지를 보냅니다.

[**\<system.serviceModel >**](system-servicemodel.md)   
&nbsp;&nbsp;**\<라우팅 >**
  
## <a name="syntax"></a>구문  
  
```xml  
<system.serviceModel>
  <routing>
    <filters>
      <filter customType="String"
              filterData="String"
              filterType="Action/Address/AddressPrefix/And/Custom/Endpoint/MatchAll/XPath"
              name="String" />
    </filters>
    <routingTables>
      <table name="String">
        <entries>
          <add endpoint="String"
               filterName="String"
               priority="Integer" />
        </entries>
      </table>
    </routingTables>
  </routing>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a>특성 및 요소

다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.

### <a name="attributes"></a>특성

없음

### <a name="child-elements"></a>자식 요소

|     | 설명 |
| --- | ----------- |
| [**\<필터 >**](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md) | 들어오는 메시지를 평가할 때 Windows Communication Foundation (WCF) messagefilter 형식을 사용할지를 결정 하는 라우팅 필터 집합을 포함 합니다. |
| [**\<filterTables >**](../../../../../docs/framework/configure-apps/file-schema/wcf/filtertables.md) | 필터가 일치할 때 사용할 엔드포인트를 지정하기 위한 라우팅 필터와 대상 엔드포인트 간의 매핑을 포함합니다. |

### <a name="parent-elements"></a>부모 요소

|     | 설명 |
| --- | ----------- |
| **\<시스템입니다. ServiceModel >** | 모든 WCF 구성 요소의 루트 요소입니다. |

## <a name="see-also"></a>참고 항목

<xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>
