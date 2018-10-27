---
title: TransportBindingElement
ms.date: 03/30/2017
ms.assetid: 54ecfbee-53c0-410c-a7fa-a98f2e40c545
ms.openlocfilehash: 79d8b1f4a5127ca36eb57954cff6ee6a97e55e41
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50182660"
---
# <a name="transportbindingelement"></a><span data-ttu-id="3006a-102">TransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="3006a-102">TransportBindingElement</span></span>
<span data-ttu-id="3006a-103">TransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="3006a-103">TransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3006a-104">구문</span><span class="sxs-lookup"><span data-stu-id="3006a-104">Syntax</span></span>  
  
```csharp
class TransportBindingElement : BindingElement  
{  
  boolean ManualAddressing;  
  sint64 MaxBufferPoolSize;  
  sint64 MaxReceivedMessageSize;  
  string Scheme;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="3006a-105">메서드</span><span class="sxs-lookup"><span data-stu-id="3006a-105">Methods</span></span>  
 <span data-ttu-id="3006a-106">TransportBindingElement 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3006a-106">The TransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="3006a-107">속성</span><span class="sxs-lookup"><span data-stu-id="3006a-107">Properties</span></span>  
 <span data-ttu-id="3006a-108">TransportBindingElement 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3006a-108">The TransportBindingElement class has the following properties:</span></span>  
  
### <a name="manualaddressing"></a><span data-ttu-id="3006a-109">ManualAddressing</span><span class="sxs-lookup"><span data-stu-id="3006a-109">ManualAddressing</span></span>  
 <span data-ttu-id="3006a-110">데이터 형식: boolean</span><span class="sxs-lookup"><span data-stu-id="3006a-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="3006a-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="3006a-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3006a-112">사용자가 메시지 주소 지정을 제어하는지 여부를 지정하는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="3006a-112">A boolean value that specifies whether the user wants to take control of message addressing.</span></span>  
  
### <a name="maxbufferpoolsize"></a><span data-ttu-id="3006a-113">MaxBufferPoolSize</span><span class="sxs-lookup"><span data-stu-id="3006a-113">MaxBufferPoolSize</span></span>  
 <span data-ttu-id="3006a-114">데이터 형식: sint64</span><span class="sxs-lookup"><span data-stu-id="3006a-114">Data type: sint64</span></span>  
  
 <span data-ttu-id="3006a-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="3006a-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3006a-116">바인딩에 대한 최대 버퍼 풀 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="3006a-116">The maximum buffer pool size for the binding.</span></span>  
  
### <a name="maxreceivedmessagesize"></a><span data-ttu-id="3006a-117">MaxReceivedMessageSize</span><span class="sxs-lookup"><span data-stu-id="3006a-117">MaxReceivedMessageSize</span></span>  
 <span data-ttu-id="3006a-118">데이터 형식: sint64</span><span class="sxs-lookup"><span data-stu-id="3006a-118">Data type: sint64</span></span>  
  
 <span data-ttu-id="3006a-119">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="3006a-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3006a-120">이 바인딩에서 처리하는 메시지의 최대 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="3006a-120">The maximum size for a message that is processed by this binding.</span></span>  
  
### <a name="scheme"></a><span data-ttu-id="3006a-121">Scheme</span><span class="sxs-lookup"><span data-stu-id="3006a-121">Scheme</span></span>  
 <span data-ttu-id="3006a-122">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="3006a-122">Data type: string</span></span>  
  
 <span data-ttu-id="3006a-123">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="3006a-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3006a-124">전송을 위한 URI 스키마입니다.</span><span class="sxs-lookup"><span data-stu-id="3006a-124">The URI scheme for the transport.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3006a-125">요구 사항</span><span class="sxs-lookup"><span data-stu-id="3006a-125">Requirements</span></span>  
  
|<span data-ttu-id="3006a-126">MOF</span><span class="sxs-lookup"><span data-stu-id="3006a-126">MOF</span></span>|<span data-ttu-id="3006a-127">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3006a-127">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="3006a-128">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="3006a-128">Namespace</span></span>|<span data-ttu-id="3006a-129">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3006a-129">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3006a-130">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3006a-130">See Also</span></span>  
 <xref:System.ServiceModel.Channels.TransportBindingElement>
