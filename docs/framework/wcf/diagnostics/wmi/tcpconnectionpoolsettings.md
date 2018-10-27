---
title: TcpConnectionPoolSettings
ms.date: 03/30/2017
ms.assetid: 19acfba3-c057-4dbc-bac7-8674d7844d83
ms.openlocfilehash: f9e1c043579f632f16a7cf36bf34c2467a743e47
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50189565"
---
# <a name="tcpconnectionpoolsettings"></a><span data-ttu-id="01191-102">TcpConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="01191-102">TcpConnectionPoolSettings</span></span>
<span data-ttu-id="01191-103">TcpConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="01191-103">TcpConnectionPoolSettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="01191-104">구문</span><span class="sxs-lookup"><span data-stu-id="01191-104">Syntax</span></span>  
  
```csharp
class TcpConnectionPoolSettings  
{  
  string GroupName;  
  datetime IdleTimeout;  
  datetime LeaseTimeout;  
  sint32 MaxOutboundConnectionsPerEndpoint;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="01191-105">메서드</span><span class="sxs-lookup"><span data-stu-id="01191-105">Methods</span></span>  
 <span data-ttu-id="01191-106">TcpConnectionPoolSettings 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01191-106">The TcpConnectionPoolSettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="01191-107">속성</span><span class="sxs-lookup"><span data-stu-id="01191-107">Properties</span></span>  
 <span data-ttu-id="01191-108">TcpConnectionPoolSettings 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01191-108">The TcpConnectionPoolSettings class has the following properties:</span></span>  
  
### <a name="groupname"></a><span data-ttu-id="01191-109">GroupName</span><span class="sxs-lookup"><span data-stu-id="01191-109">GroupName</span></span>  
 <span data-ttu-id="01191-110">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="01191-110">Data type: string</span></span>  
  
 <span data-ttu-id="01191-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="01191-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="01191-112">바인딩 요소가 사용하는 연결 풀의 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01191-112">The group name of the connection pool used by the binding element.</span></span>  
  
### <a name="idletimeout"></a><span data-ttu-id="01191-113">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="01191-113">IdleTimeout</span></span>  
 <span data-ttu-id="01191-114">데이터 형식: datetime</span><span class="sxs-lookup"><span data-stu-id="01191-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="01191-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="01191-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="01191-116">연결이 끊어지기 전에 유휴 상태일 수 있는 최대 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="01191-116">The maximum time the connection can be idle before being disconnected.</span></span>  
  
### <a name="leasetimeout"></a><span data-ttu-id="01191-117">LeaseTimeout</span><span class="sxs-lookup"><span data-stu-id="01191-117">LeaseTimeout</span></span>  
 <span data-ttu-id="01191-118">데이터 형식: datetime</span><span class="sxs-lookup"><span data-stu-id="01191-118">Data type: datetime</span></span>  
  
 <span data-ttu-id="01191-119">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="01191-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="01191-120">제한 시간을 초과하기 전에 대여 작업을 완료하기 위한 최대 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="01191-120">The maximum time for the lease operation to complete before timing out.</span></span>  
  
### <a name="maxoutboundconnectionsperendpoint"></a><span data-ttu-id="01191-121">MaxOutboundConnectionsPerEndpoint</span><span class="sxs-lookup"><span data-stu-id="01191-121">MaxOutboundConnectionsPerEndpoint</span></span>  
 <span data-ttu-id="01191-122">데이터 형식: sint32</span><span class="sxs-lookup"><span data-stu-id="01191-122">Data type: sint32</span></span>  
  
 <span data-ttu-id="01191-123">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="01191-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="01191-124">각 엔드포인트에 대한 최대 아웃바운드 연결 수입니다.</span><span class="sxs-lookup"><span data-stu-id="01191-124">The maximum outbound connections for each endpoint.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="01191-125">요구 사항</span><span class="sxs-lookup"><span data-stu-id="01191-125">Requirements</span></span>  
  
|<span data-ttu-id="01191-126">MOF</span><span class="sxs-lookup"><span data-stu-id="01191-126">MOF</span></span>|<span data-ttu-id="01191-127">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01191-127">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="01191-128">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="01191-128">Namespace</span></span>|<span data-ttu-id="01191-129">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01191-129">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="01191-130">참고 항목</span><span class="sxs-lookup"><span data-stu-id="01191-130">See Also</span></span>  
 <xref:System.ServiceModel.Channels.TcpConnectionPoolSettings>
