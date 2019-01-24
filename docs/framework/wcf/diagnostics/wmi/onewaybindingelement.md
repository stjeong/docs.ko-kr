---
title: OneWayBindingElement
ms.date: 03/30/2017
ms.assetid: 5c7e17c3-39b9-4214-ae08-9e6141734305
ms.openlocfilehash: d84184febd6db3f233aae6fe558b8e0f50a9cb82
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54608838"
---
# <a name="onewaybindingelement"></a><span data-ttu-id="b142c-102">OneWayBindingElement</span><span class="sxs-lookup"><span data-stu-id="b142c-102">OneWayBindingElement</span></span>
<span data-ttu-id="b142c-103">OneWayBindingElement</span><span class="sxs-lookup"><span data-stu-id="b142c-103">OneWayBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b142c-104">구문</span><span class="sxs-lookup"><span data-stu-id="b142c-104">Syntax</span></span>  
  
```csharp
class OneWayBindingElement : BindingElement  
{  
  ChannelPoolSettings ChannelPoolSettings;  
  sint32 MaxAcceptedChannels;  
  boolean PacketRoutable;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="b142c-105">메서드</span><span class="sxs-lookup"><span data-stu-id="b142c-105">Methods</span></span>  
 <span data-ttu-id="b142c-106">OneWayBindingElement 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b142c-106">The OneWayBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="b142c-107">속성</span><span class="sxs-lookup"><span data-stu-id="b142c-107">Properties</span></span>  
 <span data-ttu-id="b142c-108">OneWayBindingElement 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b142c-108">The OneWayBindingElement class has the following properties:</span></span>  
  
### <a name="channelpoolsettings"></a><span data-ttu-id="b142c-109">ChannelPoolSettings</span><span class="sxs-lookup"><span data-stu-id="b142c-109">ChannelPoolSettings</span></span>  
 <span data-ttu-id="b142c-110">데이터 형식: ChannelPoolSettings</span><span class="sxs-lookup"><span data-stu-id="b142c-110">Data type: ChannelPoolSettings</span></span>  
  
 <span data-ttu-id="b142c-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="b142c-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b142c-112">채널 풀 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="b142c-112">The channel pool settings.</span></span>  
  
### <a name="maxacceptedchannels"></a><span data-ttu-id="b142c-113">MaxAcceptedChannels</span><span class="sxs-lookup"><span data-stu-id="b142c-113">MaxAcceptedChannels</span></span>  
 <span data-ttu-id="b142c-114">데이터 형식: sint32</span><span class="sxs-lookup"><span data-stu-id="b142c-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="b142c-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="b142c-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b142c-116">허용되는 최대 채널 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b142c-116">The maximum number of accepted channels.</span></span>  
  
### <a name="packetroutable"></a><span data-ttu-id="b142c-117">PacketRoutable</span><span class="sxs-lookup"><span data-stu-id="b142c-117">PacketRoutable</span></span>  
 <span data-ttu-id="b142c-118">데이터 형식: boolean</span><span class="sxs-lookup"><span data-stu-id="b142c-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="b142c-119">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="b142c-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b142c-120">패킷을 라우팅할 수 있는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b142c-120">A value that indicates whether the packet is routable.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b142c-121">요구 사항</span><span class="sxs-lookup"><span data-stu-id="b142c-121">Requirements</span></span>  
  
|<span data-ttu-id="b142c-122">MOF</span><span class="sxs-lookup"><span data-stu-id="b142c-122">MOF</span></span>|<span data-ttu-id="b142c-123">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b142c-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="b142c-124">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="b142c-124">Namespace</span></span>|<span data-ttu-id="b142c-125">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b142c-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b142c-126">참고자료</span><span class="sxs-lookup"><span data-stu-id="b142c-126">See also</span></span>
- <xref:System.ServiceModel.Channels.OneWayBindingElement>
