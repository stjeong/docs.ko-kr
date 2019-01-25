---
title: 신뢰할 수 있는 세션
ms.date: 03/30/2017
f1_keywords:
- Windows Communication Foundation, sessions and instances
- WCF, sessions and instances
- sessions and instances [WCF]
helpviewer_keywords:
- instances [WCF]
- sessions [WCF]
ms.assetid: 143951b3-3aa0-4540-b4b7-d33e77e874a1
ms.openlocfilehash: 1d87f6f4d94763dc8f6ac7e929c22b17940097ca
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54735427"
---
# <a name="reliable-sessions"></a><span data-ttu-id="63a2c-102">신뢰할 수 있는 세션</span><span class="sxs-lookup"><span data-stu-id="63a2c-102">Reliable Sessions</span></span>

<span data-ttu-id="63a2c-103">이 섹션에서는 무엇을 Windows Communication Foundation (WCF) 신뢰할 수 있는 세션, 용도, 방법 및 경우 하나를 사용 하려면 바인딩 구성, 지원 및 모범 사례에 대 한 포인터를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="63a2c-103">This section describes what a Windows Communication Foundation (WCF) reliable session is, what it's used for, how and when to use one, what binding configurations support it, and pointers on best practices.</span></span> <span data-ttu-id="63a2c-104">다음 표에서는 이 단원의 필수 사항 및 관련 항목에 대한 세부 정보를 요약하여 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="63a2c-104">The following table summarizes details about the essential points and related topics in this section.</span></span>

<span data-ttu-id="63a2c-105">신뢰할 수 있는 세션 WCF 끝점 간에 보내진 메시지가 SOAP 또는 전송 매개 자를 통해 전송 되 고 전송 된 동일한 순서로 한 번만 있고, 선택적으로 배달 하는 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="63a2c-105">The reliable session WCF provides featrues ensuring that messages sent between endpoints are transferred across SOAP or transport intermediaries and are delivered only once and, optionally, in the same order in which they were sent.</span></span>

<span data-ttu-id="63a2c-106">WCF 응용 프로그램에서 신뢰할 수 있는 세션을 사용 하려면 기본적으로 또는 필요에 따라 신뢰할 수 있는 세션을 지 원하는 WCF의 시스템 제공 바인딩 중 하나를 사용 하거나 세션을 지 원하는 고유한 사용자 지정 바인딩을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="63a2c-106">To use a reliable session with a WCF application, either use one of the system-provided bindings in WCF that support a reliable session by default or as an option, or create your own custom binding that supports the session.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="63a2c-107">섹션 내용</span><span class="sxs-lookup"><span data-stu-id="63a2c-107">In This Section</span></span>

<span data-ttu-id="63a2c-108">[신뢰할 수 있는 세션 개요](../../../../docs/framework/wcf/feature-details/reliable-sessions-overview.md) </span><span class="sxs-lookup"><span data-stu-id="63a2c-108">[Reliable Sessions Overview](../../../../docs/framework/wcf/feature-details/reliable-sessions-overview.md) </span></span>  
<span data-ttu-id="63a2c-109">신뢰할 수 있는 세션, 사용 시기, 신뢰할 수 있는 세션을 지원하는 다른 바인딩 및 그러한 바인딩의 작동 방식에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="63a2c-109">Describes reliable sessions, when to use them, the different bindings that support reliable sessions, and how they work.</span></span>

<span data-ttu-id="63a2c-110">[방법: 신뢰할 수 있는 세션 내에서 메시지 교환](../../../../docs/framework/wcf/feature-details/how-to-exchange-messages-within-a-reliable-session.md) </span><span class="sxs-lookup"><span data-stu-id="63a2c-110">[How to: Exchange Messages Within a Reliable Session](../../../../docs/framework/wcf/feature-details/how-to-exchange-messages-within-a-reliable-session.md) </span></span>  
<span data-ttu-id="63a2c-111">구성에 지정된 사용자 지정 바인딩을 사용하여 HTTP를 통해 신뢰할 수 있는 세션을 만드는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="63a2c-111">Describes how to create a reliable session over HTTP using a custom binding specified in the configuration.</span></span>

<span data-ttu-id="63a2c-112">[방법: 신뢰할 수 있는 세션 내에서 메시지 보안](../../../../docs/framework/wcf/feature-details/how-to-secure-messages-within-reliable-sessions.md) </span><span class="sxs-lookup"><span data-stu-id="63a2c-112">[How to: Secure Messages within Reliable Sessions](../../../../docs/framework/wcf/feature-details/how-to-secure-messages-within-reliable-sessions.md) </span></span>  
<span data-ttu-id="63a2c-113">신뢰할 수 있는 세션의 보안을 유지하는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="63a2c-113">Describes how to secure a reliable session.</span></span>

<span data-ttu-id="63a2c-114">[방법: HTTPS를 사용 하 여 사용자 지정 신뢰할 수 있는 세션 바인딩 만들기](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-reliable-session-binding-with-https.md) </span><span class="sxs-lookup"><span data-stu-id="63a2c-114">[How to: Create a Custom Reliable Session Binding with HTTPS](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-reliable-session-binding-with-https.md) </span></span>  
<span data-ttu-id="63a2c-115">HTTPS를 통해 신뢰할 수 있는 세션을 만드는 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="63a2c-115">Describes how to create a reliable session over HTTPS.</span></span>

<span data-ttu-id="63a2c-116">[신뢰할 수 있는 세션에 대 한 모범 사례](../../../../docs/framework/wcf/feature-details/best-practices-for-reliable-sessions.md) </span><span class="sxs-lookup"><span data-stu-id="63a2c-116">[Best Practices for Reliable Sessions](../../../../docs/framework/wcf/feature-details/best-practices-for-reliable-sessions.md) </span></span>  
<span data-ttu-id="63a2c-117">신뢰할 수 있는 세션 사용과 관련된 몇 가지 최선의 방법에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="63a2c-117">Describes some of the best practices associated with using a reliable session.</span></span>

## <a name="reference"></a><span data-ttu-id="63a2c-118">참조</span><span class="sxs-lookup"><span data-stu-id="63a2c-118">Reference</span></span>

<xref:System.ServiceModel.ReliableSession>

## <a name="see-also"></a><span data-ttu-id="63a2c-119">참고자료</span><span class="sxs-lookup"><span data-stu-id="63a2c-119">See also</span></span>

- [<span data-ttu-id="63a2c-120">큐 및 신뢰할 수 있는 세션</span><span class="sxs-lookup"><span data-stu-id="63a2c-120">Queues and Reliable Sessions</span></span>](../../../../docs/framework/wcf/feature-details/queues-and-reliable-sessions.md)
- [<span data-ttu-id="63a2c-121">세션, 인스턴스 및 동시성</span><span class="sxs-lookup"><span data-stu-id="63a2c-121">Sessions, Instancing, and Concurrency</span></span>](../../../../docs/framework/wcf/feature-details/sessions-instancing-and-concurrency.md)
