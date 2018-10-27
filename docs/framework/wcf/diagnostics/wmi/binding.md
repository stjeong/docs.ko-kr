---
title: Binding2
ms.date: 03/30/2017
ms.assetid: 09511c6c-5749-4bb0-874e-0f0be36bfe04
ms.openlocfilehash: 84e304f3dedcbd785d6238e6cb5eb142c288b995
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50033835"
---
# <a name="binding"></a><span data-ttu-id="6a6a9-102">바인딩</span><span class="sxs-lookup"><span data-stu-id="6a6a9-102">Binding</span></span>
<span data-ttu-id="6a6a9-103">wmi 바인딩</span><span class="sxs-lookup"><span data-stu-id="6a6a9-103">wmi Binding</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6a6a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="6a6a9-104">Syntax</span></span>  
  
```csharp
class Binding  
{  
  BindingElement BindingElements[];  
  datetime CloseTimeout;  
  string Name;  
  string Namespace;  
  datetime OpenTimeout;  
  datetime ReceiveTimeout;  
  string Scheme;  
  datetime SendTimeout;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="6a6a9-105">메서드</span><span class="sxs-lookup"><span data-stu-id="6a6a9-105">Methods</span></span>  
 <span data-ttu-id="6a6a9-106">바인딩 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a6a9-106">The Binding class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="6a6a9-107">속성</span><span class="sxs-lookup"><span data-stu-id="6a6a9-107">Properties</span></span>  
 <span data-ttu-id="6a6a9-108">Binding 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a6a9-108">The Binding class has the following properties.</span></span>  
  
### <a name="bindingelements"></a><span data-ttu-id="6a6a9-109">BindingElements</span><span class="sxs-lookup"><span data-stu-id="6a6a9-109">BindingElements</span></span>  
 <span data-ttu-id="6a6a9-110">데이터 형식: BindingElement array</span><span class="sxs-lookup"><span data-stu-id="6a6a9-110">Data type: BindingElement array</span></span>  
  
 <span data-ttu-id="6a6a9-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6a6a9-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6a6a9-112">바인딩이 구현한 바인딩 요소의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="6a6a9-112">The collection of binding elements implemented by the binding.</span></span>  
  
### <a name="closetimeout"></a><span data-ttu-id="6a6a9-113">CloseTimeout</span><span class="sxs-lookup"><span data-stu-id="6a6a9-113">CloseTimeout</span></span>  
 <span data-ttu-id="6a6a9-114">데이터 형식: datetime</span><span class="sxs-lookup"><span data-stu-id="6a6a9-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="6a6a9-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6a6a9-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6a6a9-116">닫기 작업을 완료하기 위해 제공된 시간 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="6a6a9-116">The interval of time provided for a close operation to complete.</span></span>  
  
### <a name="name"></a><span data-ttu-id="6a6a9-117">이름</span><span class="sxs-lookup"><span data-stu-id="6a6a9-117">Name</span></span>  
 <span data-ttu-id="6a6a9-118">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="6a6a9-118">Data type: string</span></span>  
  
 <span data-ttu-id="6a6a9-119">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6a6a9-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6a6a9-120">바인딩 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a6a9-120">The name of the binding.</span></span>  
  
### <a name="namespace"></a><span data-ttu-id="6a6a9-121">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="6a6a9-121">Namespace</span></span>  
 <span data-ttu-id="6a6a9-122">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="6a6a9-122">Data type: string</span></span>  
  
 <span data-ttu-id="6a6a9-123">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6a6a9-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6a6a9-124">바인딩의 XML 네임스페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="6a6a9-124">The XML namespace of the binding.</span></span>  
  
### <a name="opentimeout"></a><span data-ttu-id="6a6a9-125">OpenTimeout</span><span class="sxs-lookup"><span data-stu-id="6a6a9-125">OpenTimeout</span></span>  
 <span data-ttu-id="6a6a9-126">데이터 형식: datetime</span><span class="sxs-lookup"><span data-stu-id="6a6a9-126">Data type: datetime</span></span>  
  
 <span data-ttu-id="6a6a9-127">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6a6a9-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6a6a9-128">열기 작업을 완료하기 위해 제공된 시간 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="6a6a9-128">The interval of time provided for an open operation to complete.</span></span>  
  
### <a name="receivetimeout"></a><span data-ttu-id="6a6a9-129">ReceiveTimeout</span><span class="sxs-lookup"><span data-stu-id="6a6a9-129">ReceiveTimeout</span></span>  
 <span data-ttu-id="6a6a9-130">데이터 형식: datetime</span><span class="sxs-lookup"><span data-stu-id="6a6a9-130">Data type: datetime</span></span>  
  
 <span data-ttu-id="6a6a9-131">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6a6a9-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6a6a9-132">받기 작업을 완료하기 위해 제공된 시간 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="6a6a9-132">The interval of time provided for a receive operation to complete.</span></span>  
  
### <a name="scheme"></a><span data-ttu-id="6a6a9-133">Scheme</span><span class="sxs-lookup"><span data-stu-id="6a6a9-133">Scheme</span></span>  
 <span data-ttu-id="6a6a9-134">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="6a6a9-134">Data type: string</span></span>  
  
 <span data-ttu-id="6a6a9-135">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6a6a9-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6a6a9-136">바인딩이 빌드한 채널 및 수신기 팩터리에서 사용하는 URI 전송 체계입니다.</span><span class="sxs-lookup"><span data-stu-id="6a6a9-136">The URI transport scheme that is used by the channel and listener factories that are built by the binding.</span></span>  
  
### <a name="sendtimeout"></a><span data-ttu-id="6a6a9-137">SendTimeout</span><span class="sxs-lookup"><span data-stu-id="6a6a9-137">SendTimeout</span></span>  
 <span data-ttu-id="6a6a9-138">데이터 형식: datetime</span><span class="sxs-lookup"><span data-stu-id="6a6a9-138">Data type: datetime</span></span>  
  
 <span data-ttu-id="6a6a9-139">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6a6a9-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6a6a9-140">보내기 작업을 완료하기 위해 제공된 시간 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="6a6a9-140">The interval of time provided for a send operation to complete.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6a6a9-141">요구 사항</span><span class="sxs-lookup"><span data-stu-id="6a6a9-141">Requirements</span></span>  
  
|<span data-ttu-id="6a6a9-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6a6a9-142">MOF</span></span>|<span data-ttu-id="6a6a9-143">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a6a9-143">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="6a6a9-144">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="6a6a9-144">Namespace</span></span>|<span data-ttu-id="6a6a9-145">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a6a9-145">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6a6a9-146">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6a6a9-146">See Also</span></span>  
 <xref:System.ServiceModel.Channels.Binding>
