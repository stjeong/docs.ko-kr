---
title: TextMessageEncodingBindingElement
ms.date: 03/30/2017
ms.assetid: 885e2d7a-3436-4093-bc5f-0a404c62acdc
ms.openlocfilehash: 2371c38aebe2bd8d6da93d702801556fad986ef9
ms.sourcegitcommit: b22705f1540b237c566721018f974822d5cd8758
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/19/2018
ms.locfileid: "49452575"
---
# <a name="textmessageencodingbindingelement"></a><span data-ttu-id="8de00-102">TextMessageEncodingBindingElement</span><span class="sxs-lookup"><span data-stu-id="8de00-102">TextMessageEncodingBindingElement</span></span>
<span data-ttu-id="8de00-103">TextMessageEncodingBindingElement</span><span class="sxs-lookup"><span data-stu-id="8de00-103">TextMessageEncodingBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8de00-104">구문</span><span class="sxs-lookup"><span data-stu-id="8de00-104">Syntax</span></span>  
  
```csharp
class TextMessageEncodingBindingElement : MessageEncodingBindingElement  
{  
  string Encoding;  
  sint32 MaxReadPoolSize;  
  sint32 MaxWritePoolSize;  
  XmlDictionaryReaderQuotas ReaderQuotas;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="8de00-105">메서드</span><span class="sxs-lookup"><span data-stu-id="8de00-105">Methods</span></span>  
 <span data-ttu-id="8de00-106">TextMessageEncodingBindingElement 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8de00-106">The TextMessageEncodingBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="8de00-107">속성</span><span class="sxs-lookup"><span data-stu-id="8de00-107">Properties</span></span>  
 <span data-ttu-id="8de00-108">TextMessageEncodingBindingElement 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8de00-108">The TextMessageEncodingBindingElement class has the following properties:</span></span>  
  
### <a name="encoding"></a><span data-ttu-id="8de00-109">인코딩</span><span class="sxs-lookup"><span data-stu-id="8de00-109">Encoding</span></span>  
 <span data-ttu-id="8de00-110">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="8de00-110">Data type: string</span></span>  
  
 <span data-ttu-id="8de00-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="8de00-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8de00-112">바인딩에서 메시지를 내보낼 때 사용되는 문자 집합 인코딩입니다.</span><span class="sxs-lookup"><span data-stu-id="8de00-112">The character set encoding to be used for emitting messages on the binding.</span></span>  
  
### <a name="maxreadpoolsize"></a><span data-ttu-id="8de00-113">MaxReadPoolSize</span><span class="sxs-lookup"><span data-stu-id="8de00-113">MaxReadPoolSize</span></span>  
 <span data-ttu-id="8de00-114">데이터 형식: sint32</span><span class="sxs-lookup"><span data-stu-id="8de00-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="8de00-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="8de00-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8de00-116">새 판독기를 할당하지 않고 동시에 읽을 수 있는 메시지 수를 정의하는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="8de00-116">An integer that defines how many messages can be read simultaneously without allocating new readers.</span></span>  
  
### <a name="maxwritepoolsize"></a><span data-ttu-id="8de00-117">MaxWritePoolSize</span><span class="sxs-lookup"><span data-stu-id="8de00-117">MaxWritePoolSize</span></span>  
 <span data-ttu-id="8de00-118">데이터 형식: sint32</span><span class="sxs-lookup"><span data-stu-id="8de00-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="8de00-119">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="8de00-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8de00-120">새 작성기를 할당하지 않고 동시에 보낼 수 있는 메시지 수를 정의하는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="8de00-120">An integer that defines how many messages can be sent simultaneously without allocating new writers.</span></span>  
  
### <a name="readerquotas"></a><span data-ttu-id="8de00-121">ReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="8de00-121">ReaderQuotas</span></span>  
 <span data-ttu-id="8de00-122">데이터 형식: XmlDictionaryReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="8de00-122">Data type: XmlDictionaryReaderQuotas</span></span>  
  
 <span data-ttu-id="8de00-123">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="8de00-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8de00-124">판독기의 할당량입니다.</span><span class="sxs-lookup"><span data-stu-id="8de00-124">The quotas of the readers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8de00-125">요구 사항</span><span class="sxs-lookup"><span data-stu-id="8de00-125">Requirements</span></span>  
  
|<span data-ttu-id="8de00-126">MOF</span><span class="sxs-lookup"><span data-stu-id="8de00-126">MOF</span></span>|<span data-ttu-id="8de00-127">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8de00-127">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="8de00-128">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="8de00-128">Namespace</span></span>|<span data-ttu-id="8de00-129">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8de00-129">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="8de00-130">참고 항목</span><span class="sxs-lookup"><span data-stu-id="8de00-130">See Also</span></span>  
 <xref:System.ServiceModel.Channels.TextMessageEncodingBindingElement>
