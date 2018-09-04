---
title: 시작 설정 스키마
ms.date: 03/30/2017
helpviewer_keywords:
- startup settings schema
- schema startup settings
- configuration schema [.NET Framework], startup settings
ms.assetid: 03de6972-442a-4648-9f3e-efa654e3b949
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 68f37e3efca784b94be90d5779c9bc402f144448
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43530336"
---
# <a name="startup-settings-schema"></a>시작 설정 스키마
시작 설정은 응용 프로그램을 실행해야 하는 공용 언어 런타임의 버전을 지정합니다.  
  
|요소|설명|  
|-------------|-----------------|  
|[\<requiredRuntime>](../../../../../docs/framework/configure-apps/file-schema/startup/requiredruntime-element.md)|응용 프로그램에서 1.0 버전의 공용 언어 런타임만 지원하도록 지정합니다. 런타임 버전 1.1로 빌드된 응용 프로그램은 **\<supportedRuntime>** 요소를 사용해야 합니다.|  
|[\<supportedRuntime>](../../../../../docs/framework/configure-apps/file-schema/startup/supportedruntime-element.md)|응용 프로그램이 지원하는 공용 언어 런타임 버전을 지정합니다.|  
|[\<startup>](../../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md)|**\<requiredRuntime>** 및 **\<supportedRuntime>** 요소가 포함되어 있습니다.|  
  
## <a name="see-also"></a>참고 항목  
 [구성 파일 스키마](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [\<PaveOver> 사용할 런타임 버전 지정](https://msdn.microsoft.com/library/c376208d-980d-42b4-865b-fbe0d9cc97c2)
