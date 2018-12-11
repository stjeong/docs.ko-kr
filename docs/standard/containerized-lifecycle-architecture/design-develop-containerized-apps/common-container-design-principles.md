---
title: 일반적인 컨테이너 설계 원칙
description: Microsoft 플랫폼 및 도구를 사용하여 컨테이너화된 Docker 응용 프로그램 수명 주기
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 8aa388c7c19f532829d64208a48b6e556e43d802
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53152879"
---
# <a name="common-container-design-principles"></a><span data-ttu-id="c6e2e-103">일반적인 컨테이너 설계 원칙</span><span class="sxs-lookup"><span data-stu-id="c6e2e-103">Common container design principles</span></span>

<span data-ttu-id="c6e2e-104">계속 해 서 개발 프로세스에 가져오는 경우 컨테이너를 사용 하는 방법에 대해 언급할 몇 가지 기본 개념</span><span class="sxs-lookup"><span data-stu-id="c6e2e-104">Ahead of getting into the development process there are a few basic concepts worth mentioning with regard to how you use containers.</span></span>

## <a name="container-equals-a-process"></a><span data-ttu-id="c6e2e-105">컨테이너 프로세스 같음</span><span class="sxs-lookup"><span data-stu-id="c6e2e-105">Container equals a process</span></span>

<span data-ttu-id="c6e2e-106">컨테이너 모델 컨테이너는 단일 프로세스를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c6e2e-106">In the container model, a container represents a single process.</span></span> <span data-ttu-id="c6e2e-107">컨테이너를 프로세스 경계로 정의 하면 눈금 또는 일괄 처리 오프, 프로세스에 사용 되는 기본 형식 만들기를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6e2e-107">By defining a container as a process boundary, you begin to create the primitives used to scale, or batch-off, processes.</span></span> <span data-ttu-id="c6e2e-108">Docker 컨테이너를 실행 하는 경우 표시 됩니다는 [ENTRYPOINT](https://docs.docker.com/engine/reference/builder/#/entrypoint) 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6e2e-108">When you run a Docker container, you'll see an [ENTRYPOINT](https://docs.docker.com/engine/reference/builder/#/entrypoint) definition.</span></span> <span data-ttu-id="c6e2e-109">프로세스 및 컨테이너의 수명을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="c6e2e-109">This defines the process and the lifetime of the container.</span></span> <span data-ttu-id="c6e2e-110">프로세스가 완료 되 면 컨테이너 수명 주기가 종료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6e2e-110">When the process completes, the container life cycle ends.</span></span> <span data-ttu-id="c6e2e-111">웹 서버 및 Microsoft Azure로 구현 했을 수 있는 일괄 작업과 같은 단기 실행 프로세스와 같은 장기 실행 프로세스가 [WebJobs](https://azure.microsoft.com/documentation/articles/websites-webjobs-resources/)합니다.</span><span class="sxs-lookup"><span data-stu-id="c6e2e-111">There are long-running processes, such as web servers, and short-lived processes, such as batch jobs, which might have been implemented as Microsoft Azure [WebJobs](https://azure.microsoft.com/documentation/articles/websites-webjobs-resources/).</span></span> <span data-ttu-id="c6e2e-112">프로세스에 실패할 경우 컨테이너가 종료되며 조정자가 이어서 프로세스를 진행합니다.</span><span class="sxs-lookup"><span data-stu-id="c6e2e-112">If the process fails, the container ends, and the orchestrator takes over.</span></span> <span data-ttu-id="c6e2e-113">오 케 스트레이 터를 실행 하는 5 개의 인스턴스를 유지 하도록 지정 된 하나에 오류가 발생 하는 경우는 오 케 스트레이 터는 실패 한 프로세스를 바꾸려면 다른 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6e2e-113">If the orchestrator was instructed to keep five instances running and one fails, the orchestrator will create another container to replace the failed process.</span></span> <span data-ttu-id="c6e2e-114">일괄 작업에서 프로세스는 매개 변수와 함께 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6e2e-114">In a batch job, the process is started with parameters.</span></span> <span data-ttu-id="c6e2e-115">프로세스가 완료되면 작업이 완료됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6e2e-115">When the process completes, the work is complete.</span></span>

<span data-ttu-id="c6e2e-116">여러 프로세스를 단일 컨테이너에서 실행 하려는 경우를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6e2e-116">You might find a scenario in which you want multiple processes running in a single container.</span></span> <span data-ttu-id="c6e2e-117">아키텍처 문서에서 되지 않습니다는 "never," 항상 새로운 기술이 나는 "항상"입니다.</span><span class="sxs-lookup"><span data-stu-id="c6e2e-117">In any architecture document, there's never a "never," nor is there always an "always."</span></span> <span data-ttu-id="c6e2e-118">여러 프로세스를 요구 하는 시나리오에 대 한 일반적인 패턴을 사용 하는 것 [감독자](http://supervisord.org/)합니다.</span><span class="sxs-lookup"><span data-stu-id="c6e2e-118">For scenarios requiring multiple processes, a common pattern is to use [Supervisor](http://supervisord.org/).</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="c6e2e-119">[이전](design-docker-applications.md)
>[다음](monolithic-applications.md)</span><span class="sxs-lookup"><span data-stu-id="c6e2e-119">[Previous](design-docker-applications.md)
[Next](monolithic-applications.md)</span></span>