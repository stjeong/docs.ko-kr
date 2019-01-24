---
title: TcpConnectionPoolSettings
ms.date: 03/30/2017
ms.assetid: 19acfba3-c057-4dbc-bac7-8674d7844d83
ms.openlocfilehash: 4e89dbe35a5232c612555b273c3d771aad42aeb0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54584807"
---
# <a name="tcpconnectionpoolsettings"></a><span data-ttu-id="2e797-102">TcpConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="2e797-102">TcpConnectionPoolSettings</span></span>
<span data-ttu-id="2e797-103">TcpConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="2e797-103">TcpConnectionPoolSettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2e797-104">구문</span><span class="sxs-lookup"><span data-stu-id="2e797-104">Syntax</span></span>  
  
```csharp
class TcpConnectionPoolSettings  
{  
  string GroupName;  
  datetime IdleTimeout;  
  datetime LeaseTimeout;  
  sint32 MaxOutboundConnectionsPerEndpoint;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="2e797-105">메서드</span><span class="sxs-lookup"><span data-stu-id="2e797-105">Methods</span></span>  
 <span data-ttu-id="2e797-106">TcpConnectionPoolSettings 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e797-106">The TcpConnectionPoolSettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="2e797-107">속성</span><span class="sxs-lookup"><span data-stu-id="2e797-107">Properties</span></span>  
 <span data-ttu-id="2e797-108">TcpConnectionPoolSettings 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e797-108">The TcpConnectionPoolSettings class has the following properties:</span></span>  
  
### <a name="groupname"></a><span data-ttu-id="2e797-109">GroupName</span><span class="sxs-lookup"><span data-stu-id="2e797-109">GroupName</span></span>  
 <span data-ttu-id="2e797-110">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="2e797-110">Data type: string</span></span>  
  
 <span data-ttu-id="2e797-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="2e797-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="2e797-112">바인딩 요소가 사용하는 연결 풀의 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e797-112">The group name of the connection pool used by the binding element.</span></span>  
  
### <a name="idletimeout"></a><span data-ttu-id="2e797-113">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="2e797-113">IdleTimeout</span></span>  
 <span data-ttu-id="2e797-114">데이터 형식: datetime</span><span class="sxs-lookup"><span data-stu-id="2e797-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="2e797-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="2e797-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="2e797-116">연결이 끊어지기 전에 유휴 상태일 수 있는 최대 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="2e797-116">The maximum time the connection can be idle before being disconnected.</span></span>  
  
### <a name="leasetimeout"></a><span data-ttu-id="2e797-117">LeaseTimeout</span><span class="sxs-lookup"><span data-stu-id="2e797-117">LeaseTimeout</span></span>  
 <span data-ttu-id="2e797-118">데이터 형식: datetime</span><span class="sxs-lookup"><span data-stu-id="2e797-118">Data type: datetime</span></span>  
  
 <span data-ttu-id="2e797-119">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="2e797-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="2e797-120">제한 시간을 초과하기 전에 대여 작업을 완료하기 위한 최대 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="2e797-120">The maximum time for the lease operation to complete before timing out.</span></span>  
  
### <a name="maxoutboundconnectionsperendpoint"></a><span data-ttu-id="2e797-121">MaxOutboundConnectionsPerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e797-121">MaxOutboundConnectionsPerEndpoint</span></span>  
 <span data-ttu-id="2e797-122">데이터 형식: sint32</span><span class="sxs-lookup"><span data-stu-id="2e797-122">Data type: sint32</span></span>  
  
 <span data-ttu-id="2e797-123">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="2e797-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="2e797-124">각 엔드포인트에 대한 최대 아웃바운드 연결 수입니다.</span><span class="sxs-lookup"><span data-stu-id="2e797-124">The maximum outbound connections for each endpoint.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2e797-125">요구 사항</span><span class="sxs-lookup"><span data-stu-id="2e797-125">Requirements</span></span>  
  
|<span data-ttu-id="2e797-126">MOF</span><span class="sxs-lookup"><span data-stu-id="2e797-126">MOF</span></span>|<span data-ttu-id="2e797-127">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e797-127">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="2e797-128">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="2e797-128">Namespace</span></span>|<span data-ttu-id="2e797-129">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e797-129">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="2e797-130">참고자료</span><span class="sxs-lookup"><span data-stu-id="2e797-130">See also</span></span>
- <xref:System.ServiceModel.Channels.TcpConnectionPoolSettings>
