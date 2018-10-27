---
title: ServiceDebugBehavior
ms.date: 03/30/2017
ms.assetid: a5ec9061-1e95-43fb-b0d9-dbd0a7bc3c44
ms.openlocfilehash: 68b2350f257bc95d8e17f4b9049d67c7f67becae
ms.sourcegitcommit: b22705f1540b237c566721018f974822d5cd8758
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/19/2018
ms.locfileid: "49452864"
---
# <a name="servicedebugbehavior"></a><span data-ttu-id="d3a6f-102">ServiceDebugBehavior</span><span class="sxs-lookup"><span data-stu-id="d3a6f-102">ServiceDebugBehavior</span></span>
<span data-ttu-id="d3a6f-103">ServiceDebugBehavior</span><span class="sxs-lookup"><span data-stu-id="d3a6f-103">ServiceDebugBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d3a6f-104">구문</span><span class="sxs-lookup"><span data-stu-id="d3a6f-104">Syntax</span></span>  
  
```csharp
class ServiceDebugBehavior : Behavior  
{  
  boolean HttpHelpPageEnabled;  
  string HttpHelpPageUrl;  
  boolean HttpsHelpPageEnabled;  
  string HttpsHelpPageUrl;  
  boolean IncludeExceptionDetailInFaults;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="d3a6f-105">메서드</span><span class="sxs-lookup"><span data-stu-id="d3a6f-105">Methods</span></span>  
 <span data-ttu-id="d3a6f-106">ServiceDebugBehavior 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-106">The ServiceDebugBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="d3a6f-107">속성</span><span class="sxs-lookup"><span data-stu-id="d3a6f-107">Properties</span></span>  
 <span data-ttu-id="d3a6f-108">ServiceDebugBehavior 클래스에는 다음 속성이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-108">The ServiceDebugBehavior class has the following properties:</span></span>  
  
### <a name="httphelppageenabled"></a><span data-ttu-id="d3a6f-109">HttpHelpPageEnabled</span><span class="sxs-lookup"><span data-stu-id="d3a6f-109">HttpHelpPageEnabled</span></span>  
 <span data-ttu-id="d3a6f-110">데이터 형식: boolean</span><span class="sxs-lookup"><span data-stu-id="d3a6f-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="d3a6f-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="d3a6f-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d3a6f-112">`HttpGetUrl` 특성으로 제어되는 주소에서 서비스가 WSDL을 게시할지 여부를 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-112">Controls whether the service publishes its WSDL at the address controlled by the `HttpGetUrl` attribute.</span></span>  
  
### <a name="httphelppageurl"></a><span data-ttu-id="d3a6f-113">HttpHelpPageUrl</span><span class="sxs-lookup"><span data-stu-id="d3a6f-113">HttpHelpPageUrl</span></span>  
 <span data-ttu-id="d3a6f-114">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="d3a6f-114">Data type: string</span></span>  
  
 <span data-ttu-id="d3a6f-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="d3a6f-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d3a6f-116">HTTP를 사용한 검색을 위해 서비스 WSDL이 게시되는 위치를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-116">Sets the location at which the service WSDL is published for retrieval using HTTP.</span></span>  
  
### <a name="httpshelppageenabled"></a><span data-ttu-id="d3a6f-117">HttpsHelpPageEnabled</span><span class="sxs-lookup"><span data-stu-id="d3a6f-117">HttpsHelpPageEnabled</span></span>  
 <span data-ttu-id="d3a6f-118">데이터 형식: boolean</span><span class="sxs-lookup"><span data-stu-id="d3a6f-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="d3a6f-119">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="d3a6f-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d3a6f-120">`HttpsGetUrl` 특성으로 제어되는 주소에서 서비스가 HTTPS를 통해 WSDL을 게시할지 여부를 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-120">Controls whether the service publishes its WSDL over HTTPS at the address controlled by the `HttpsGetUrl` attribute.</span></span>  
  
### <a name="httpshelppageurl"></a><span data-ttu-id="d3a6f-121">HttpsHelpPageUrl</span><span class="sxs-lookup"><span data-stu-id="d3a6f-121">HttpsHelpPageUrl</span></span>  
 <span data-ttu-id="d3a6f-122">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="d3a6f-122">Data type: string</span></span>  
  
 <span data-ttu-id="d3a6f-123">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="d3a6f-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d3a6f-124">HTTPS를 사용한 검색을 위해 서비스 WSDL이 게시되는 위치를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-124">Sets the location at which the service WSDL is published for retrieval using HTTPS.</span></span>  
  
### <a name="includeexceptiondetailinfaults"></a><span data-ttu-id="d3a6f-125">IncludeExceptionDetailInFaults</span><span class="sxs-lookup"><span data-stu-id="d3a6f-125">IncludeExceptionDetailInFaults</span></span>  
 <span data-ttu-id="d3a6f-126">데이터 형식: boolean</span><span class="sxs-lookup"><span data-stu-id="d3a6f-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="d3a6f-127">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="d3a6f-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d3a6f-128">디버깅 목적으로 클라이언트에 반환되는 SOAP 오류 정보에 관리되는 예외 정보를 포함할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-128">Specifies whether to include managed exception information in the detail of SOAP faults returned to the clients for debugging purposes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d3a6f-129">요구 사항</span><span class="sxs-lookup"><span data-stu-id="d3a6f-129">Requirements</span></span>  
  
|<span data-ttu-id="d3a6f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d3a6f-130">MOF</span></span>|<span data-ttu-id="d3a6f-131">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="d3a6f-132">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="d3a6f-132">Namespace</span></span>|<span data-ttu-id="d3a6f-133">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3a6f-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d3a6f-134">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d3a6f-134">See Also</span></span>  
 <xref:System.ServiceModel.Description.ServiceDebugBehavior>
