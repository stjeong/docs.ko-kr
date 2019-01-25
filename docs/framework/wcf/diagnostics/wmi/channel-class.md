---
title: Channel 클래스
ms.date: 03/30/2017
ms.assetid: d9fae2ca-209c-4341-a0f5-6b79d1a67776
ms.openlocfilehash: 3fbf398cca7ae9adbbecb9439bf3cbd32eb03969
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54668394"
---
# <a name="channel-class"></a><span data-ttu-id="7080d-102">Channel 클래스</span><span class="sxs-lookup"><span data-stu-id="7080d-102">Channel class</span></span>
<span data-ttu-id="7080d-103">채널</span><span class="sxs-lookup"><span data-stu-id="7080d-103">Channel</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7080d-104">구문</span><span class="sxs-lookup"><span data-stu-id="7080d-104">Syntax</span></span>  
  
```csharp
class Channel  
{  
  string LocalAddress;  
  Endpoint ref;  
  string RemoteAddress;  
  string SessionId;  
  string Type;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="7080d-105">메서드</span><span class="sxs-lookup"><span data-stu-id="7080d-105">Methods</span></span>  
 <span data-ttu-id="7080d-106">Channel 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7080d-106">The Channel class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="7080d-107">속성</span><span class="sxs-lookup"><span data-stu-id="7080d-107">Properties</span></span>  
 <span data-ttu-id="7080d-108">Channel 클래스에는 다음 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7080d-108">The Channel class has the following properties.</span></span>  
  
### <a name="localaddress"></a><span data-ttu-id="7080d-109">LocalAddress</span><span class="sxs-lookup"><span data-stu-id="7080d-109">LocalAddress</span></span>  
 <span data-ttu-id="7080d-110">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="7080d-110">Data type: string</span></span>  
  
 <span data-ttu-id="7080d-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="7080d-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7080d-112">채널에 대한 로컬 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="7080d-112">The local endpoint for the channel.</span></span>  
  
### <a name="ref"></a><span data-ttu-id="7080d-113">ref</span><span class="sxs-lookup"><span data-stu-id="7080d-113">ref</span></span>  
 <span data-ttu-id="7080d-114">데이터 형식: 엔드포인트</span><span class="sxs-lookup"><span data-stu-id="7080d-114">Data type: Endpoint</span></span>  
  
 <span data-ttu-id="7080d-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="7080d-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7080d-116">채널이 연결되는 엔드포인트에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="7080d-116">A reference to the endpoint the channel connects to.</span></span>  
  
### <a name="remoteaddress"></a><span data-ttu-id="7080d-117">RemoteAddress</span><span class="sxs-lookup"><span data-stu-id="7080d-117">RemoteAddress</span></span>  
 <span data-ttu-id="7080d-118">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="7080d-118">Data type: string</span></span>  
  
 <span data-ttu-id="7080d-119">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="7080d-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7080d-120">채널과 연결된 원격 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="7080d-120">The remote address associated with the channel.</span></span>  
  
### <a name="sessionid"></a><span data-ttu-id="7080d-121">SessionId</span><span class="sxs-lookup"><span data-stu-id="7080d-121">SessionId</span></span>  
 <span data-ttu-id="7080d-122">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="7080d-122">Data type: string</span></span>  
  
 <span data-ttu-id="7080d-123">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="7080d-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7080d-124">현재 세션 ID(있는 경우)입니다.</span><span class="sxs-lookup"><span data-stu-id="7080d-124">The current session Id, if any.</span></span>  
  
### <a name="type"></a><span data-ttu-id="7080d-125">형식</span><span class="sxs-lookup"><span data-stu-id="7080d-125">Type</span></span>  
 <span data-ttu-id="7080d-126">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="7080d-126">Data type: string</span></span>  
  
 <span data-ttu-id="7080d-127">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="7080d-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="7080d-128">채널 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7080d-128">The type of the channel.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7080d-129">요구 사항</span><span class="sxs-lookup"><span data-stu-id="7080d-129">Requirements</span></span>  
  
|<span data-ttu-id="7080d-130">MOF</span><span class="sxs-lookup"><span data-stu-id="7080d-130">MOF</span></span>|<span data-ttu-id="7080d-131">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7080d-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="7080d-132">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="7080d-132">Namespace</span></span>|<span data-ttu-id="7080d-133">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7080d-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7080d-134">참고자료</span><span class="sxs-lookup"><span data-stu-id="7080d-134">See also</span></span>
- <xref:System.ServiceModel.Channels.ChannelBase>
