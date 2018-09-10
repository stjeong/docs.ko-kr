---
title: .NET Core 설치 관리
description: 나란히 설치 전략을 사용하여 머신에서 여러 버전의 .NET Core SDK 및 런타임을 관리합니다.
author: leecow
ms.author: wiwagn
ms.date: 08/22/2018
ms.openlocfilehash: 06c3f43e7917efb8fd31898044d8f5d920c2cada
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43523677"
---
# <a name="manage-net-core-installations"></a>.NET Core 설치 관리

.NET Core는 여러 버전의 SDK 및 런타임을 나란히 배치하여 .NET Core 응용 프로그램을 빌드하고 실행하기 위한 버전 종속 유연성을 가능하게 합니다. 이러한 설치 및 자동 버전 롤포워드 동작은 유용한 혜택을 제공하지만 분명한 단점이 하나 있습니다. .NET Core SDK 또는 .NET Core 런타임 업데이트가 설치되면 이전 버전은 디스크에 남아 있습니다. 여러 설치된 버전은 시간이 지남에 따라 디스크 사용량을 증가시킵니다. 50개 초과 .NET Core SDK 업데이트가 릴리스되었습니다. 제거할 수 있는 시스템에 여러 버전의 SDK 및 런타임이 설치되어 있을 수 있습니다.

## <a name="safe-to-remove"></a>안전한 제거는?

[.NET Core 버전 선택](selection.md) 동작 및 .NET Core의 런타임 호환성을 업데이트하여 이전 버전을 안전하게 제거할 수 있습니다. .NET Core 런타임 업데이트는 1.x 및 2.x와 같은 주 버전 '대역' 내에서 호환됩니다. 또한 .NET Core SDK의 최신 릴리스는 호환 가능한 방식으로 이전 버전의 런타임을 대상으로 하는 응용 프로그램을 빌드하는 기능을 일반적으로 유지합니다.

일반적으로 응용 프로그램에 필요한 최신 SDK 및 런타임의 최신 패치 버전만 있으면 됩니다. 이전 SDK 또는 런타임 버전을 유지하는 인스턴스에는 project.json 기반 응용 프로그램 유지 관리가 포함됩니다.  응용 프로그램에 이전 SDK 또는 런타임에 대한 특정 이유가 없는 경우 이전 버전을 안전하게 제거할 수 있습니다.

.NET Core를 제거하는 방법은 플랫폼마다 다르며, .NET Core 버전 간에 다소 차이가 있습니다. 더 이상 필요 없는 .NET Core 버전을 제거하는 방법에 대한 자세한 내용은 [.NET Core 설명서](../index.md)에서 ['.NET Core 런타임 및 SDK 제거 방법'](remove-runtime-sdk-versions.md)을 참조하세요.
