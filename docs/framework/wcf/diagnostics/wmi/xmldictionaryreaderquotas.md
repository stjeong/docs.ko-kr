---
title: XmlDictionaryReaderQuotas
ms.date: 03/30/2017
ms.assetid: 9b4ca8b4-0a89-4758-97ab-528a8ce18f07
ms.openlocfilehash: 9bc519509b00383be333ac605688950d2709117c
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50199476"
---
# <a name="xmldictionaryreaderquotas"></a><span data-ttu-id="ba4fb-102">XmlDictionaryReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="ba4fb-102">XmlDictionaryReaderQuotas</span></span>
<span data-ttu-id="ba4fb-103">XmlDictionaryReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="ba4fb-103">XmlDictionaryReaderQuotas</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ba4fb-104">구문</span><span class="sxs-lookup"><span data-stu-id="ba4fb-104">Syntax</span></span>  
  
```csharp
class XmlDictionaryReaderQuotas  
{  
  sint32 MaxArrayLength;  
  sint32 MaxBytesPerRead;  
  sint32 MaxDepth;  
  sint32 MaxNameTableCharCount;  
  sint32 MaxStringContentLength;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="ba4fb-105">메서드</span><span class="sxs-lookup"><span data-stu-id="ba4fb-105">Methods</span></span>  
 <span data-ttu-id="ba4fb-106">XmlDictionaryReaderQuotas 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba4fb-106">The XmlDictionaryReaderQuotas class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="ba4fb-107">속성</span><span class="sxs-lookup"><span data-stu-id="ba4fb-107">Properties</span></span>  
 <span data-ttu-id="ba4fb-108">XmlDictionaryReaderQuotas 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba4fb-108">The XmlDictionaryReaderQuotas class has the following properties:</span></span>  
  
### <a name="maxarraylength"></a><span data-ttu-id="ba4fb-109">MaxArrayLength</span><span class="sxs-lookup"><span data-stu-id="ba4fb-109">MaxArrayLength</span></span>  
 <span data-ttu-id="ba4fb-110">데이터 형식: sint32</span><span class="sxs-lookup"><span data-stu-id="ba4fb-110">Data type: sint32</span></span>  
  
 <span data-ttu-id="ba4fb-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="ba4fb-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="ba4fb-112">허용된 최대 배열 길이입니다.</span><span class="sxs-lookup"><span data-stu-id="ba4fb-112">The maximum allowed array length.</span></span>  
  
### <a name="maxbytesperread"></a><span data-ttu-id="ba4fb-113">MaxBytesPerRead</span><span class="sxs-lookup"><span data-stu-id="ba4fb-113">MaxBytesPerRead</span></span>  
 <span data-ttu-id="ba4fb-114">데이터 형식: sint32</span><span class="sxs-lookup"><span data-stu-id="ba4fb-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="ba4fb-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="ba4fb-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="ba4fb-116">각 읽기에 대해 반환되는 최대 허용 바이트입니다.</span><span class="sxs-lookup"><span data-stu-id="ba4fb-116">The maximum allowed bytes returned for each read.</span></span>  
  
### <a name="maxdepth"></a><span data-ttu-id="ba4fb-117">MaxDepth</span><span class="sxs-lookup"><span data-stu-id="ba4fb-117">MaxDepth</span></span>  
 <span data-ttu-id="ba4fb-118">데이터 형식: sint32</span><span class="sxs-lookup"><span data-stu-id="ba4fb-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="ba4fb-119">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="ba4fb-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="ba4fb-120">각 읽기에 대한 최대 중첩 노드 깊이입니다.</span><span class="sxs-lookup"><span data-stu-id="ba4fb-120">The maximum nested node depth for each read.</span></span>  
  
### <a name="maxnametablecharcount"></a><span data-ttu-id="ba4fb-121">MaxNameTableCharCount</span><span class="sxs-lookup"><span data-stu-id="ba4fb-121">MaxNameTableCharCount</span></span>  
 <span data-ttu-id="ba4fb-122">데이터 형식: sint32</span><span class="sxs-lookup"><span data-stu-id="ba4fb-122">Data type: sint32</span></span>  
  
 <span data-ttu-id="ba4fb-123">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="ba4fb-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="ba4fb-124">표 이름에 허용된 최대 문자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ba4fb-124">The maximum characters allowed in a table name.</span></span>  
  
### <a name="maxstringcontentlength"></a><span data-ttu-id="ba4fb-125">MaxStringContentLength</span><span class="sxs-lookup"><span data-stu-id="ba4fb-125">MaxStringContentLength</span></span>  
 <span data-ttu-id="ba4fb-126">데이터 형식: sint32</span><span class="sxs-lookup"><span data-stu-id="ba4fb-126">Data type: sint32</span></span>  
  
 <span data-ttu-id="ba4fb-127">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="ba4fb-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="ba4fb-128">XML 요소 콘텐츠에 허용되는 최대 문자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ba4fb-128">The maximum characters allowed in XML element content.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ba4fb-129">요구 사항</span><span class="sxs-lookup"><span data-stu-id="ba4fb-129">Requirements</span></span>  
  
|<span data-ttu-id="ba4fb-130">MOF</span><span class="sxs-lookup"><span data-stu-id="ba4fb-130">MOF</span></span>|<span data-ttu-id="ba4fb-131">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba4fb-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="ba4fb-132">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="ba4fb-132">Namespace</span></span>|<span data-ttu-id="ba4fb-133">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba4fb-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ba4fb-134">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ba4fb-134">See Also</span></span>  
 <xref:System.Xml.XmlDictionaryReaderQuotas>  
 <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>
