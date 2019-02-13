---
title: SOA 응용 프로그램
description: 컨테이너 SOA 응용 프로그램에 대 한 유용한 배포 옵션을 또한 수 있음을 염두에 두어야 합니다.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: 4fd39e075c5730cf7fddb0138cdb5267a914c91f
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56221266"
---
# <a name="soa-applications"></a><span data-ttu-id="4150e-103">SOA 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="4150e-103">SOA applications</span></span>

<span data-ttu-id="4150e-104">SOA 용어를 남용된 되었으며 다른 사람에 게 많은 의미로 합니다.</span><span class="sxs-lookup"><span data-stu-id="4150e-104">SOA was an overused term and meant so many different things to different people.</span></span> <span data-ttu-id="4150e-105">하지만 서로 다른 종류로 분류할 수 있는 여러 서비스 (일반적으로 HTTP 서비스)에서 분해 하 여 응용 프로그램의 아키텍처 구조 하는 하위 시스템에는 최소한와 공통 분모, SOA, 또는 서비스 지향, 평균 등의 또는 계층으로 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4150e-105">But at a minimum and as a common denominator, SOA, or service orientation, mean that you structure the architecture of your application by decomposing it in multiple services (most commonly as HTTP services) that can be classified in different types like subsystems or, in other cases, as tiers.</span></span>

<span data-ttu-id="4150e-106">현재 배포할 수 있습니다 이러한 서비스 Docker 컨테이너와 모든 종속성에 컨테이너 이미지 내에 포함 되므로 배포 관련 문제를 해결 하는.</span><span class="sxs-lookup"><span data-stu-id="4150e-106">Today, you can deploy those services as Docker containers, which solves deployment-related issues because all of the dependencies are included within the container image.</span></span> <span data-ttu-id="4150e-107">그러나 스케일 아웃 Soa 해야 하는 경우에 따라 단일 인스턴스를 배포 하는 경우 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4150e-107">However, when you need to scale-out SOAs, you might encounter challenges if you are deploying based on single instances.</span></span> <span data-ttu-id="4150e-108">이것이 있는 Docker 클러스터링 소프트웨어 또는 오 케 스트레이 터는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4150e-108">This is where a Docker clustering software or orchestrator will help you.</span></span> <span data-ttu-id="4150e-109">살펴보겠습니다이 다음 섹션에서 자세히 경우 마이크로 서비스 접근 방식을 살펴봅니다.</span><span class="sxs-lookup"><span data-stu-id="4150e-109">We'll look at this in greater detail in the next section when we examine microservices approaches.</span></span>

<span data-ttu-id="4150e-110">하루 끝 컨테이너 클러스터링 솔루션은 모두 기존 SOA 아키텍처에 대 한 각 마이크로 서비스는 해당 데이터 모델을 소유 하는 고급 마이크로 서비스 아키텍처에 대 한 유용한입니다.</span><span class="sxs-lookup"><span data-stu-id="4150e-110">At the end of the day, the container clustering solutions are useful for both a traditional SOA architecture or for a more advanced microservices architecture in which each microservice owns its data model.</span></span> <span data-ttu-id="4150e-111">및를 여러 데이터베이스 덕분 있습니다도 수 스케일 아웃 SOA 서비스에서 공유 하는 모놀리식 데이터베이스와 함께 작업 하는 대신 데이터 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="4150e-111">And, thanks to multiple databases, you also can scale-out the data tier instead of working with monolithic databases shared by the SOA services.</span></span> <span data-ttu-id="4150e-112">그러나 데이터를 분할 하는 방법에 대 한 토론 순수 하 게에 대 한 아키텍처 및 디자인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4150e-112">However, the discussion about splitting the data is purely about architecture and design.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="4150e-113">[이전](state-and-data-in-docker-applications.md)
>[다음](orchestrate-high-scalability-availability.md)</span><span class="sxs-lookup"><span data-stu-id="4150e-113">[Previous](state-and-data-in-docker-applications.md)
[Next](orchestrate-high-scalability-availability.md)</span></span>