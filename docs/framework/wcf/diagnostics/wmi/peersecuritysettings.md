---
title: PeerSecuritySettings
ms.date: 03/30/2017
ms.assetid: 24ae0d35-f3a3-419b-afd6-686e22aae27b
author: BrucePerlerMS
ms.openlocfilehash: c74ee82d7aa3a23f0ee6a69185ad45857c31bb0b
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47087881"
---
# <a name="peersecuritysettings"></a><span data-ttu-id="07384-102">PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="07384-102">PeerSecuritySettings</span></span>
<span data-ttu-id="07384-103">PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="07384-103">PeerSecuritySettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="07384-104">구문</span><span class="sxs-lookup"><span data-stu-id="07384-104">Syntax</span></span>  
  
```  
class PeerSecuritySettings  
{  
  string Mode;  
  PeerTransportSecuritySettings Transport;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="07384-105">메서드</span><span class="sxs-lookup"><span data-stu-id="07384-105">Methods</span></span>  
 <span data-ttu-id="07384-106">PeerSecuritySettings 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07384-106">The PeerSecuritySettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="07384-107">속성</span><span class="sxs-lookup"><span data-stu-id="07384-107">Properties</span></span>  
 <span data-ttu-id="07384-108">PeerSecuritySettings 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07384-108">The PeerSecuritySettings class has the following properties:</span></span>  
  
### <a name="mode"></a><span data-ttu-id="07384-109">모드</span><span class="sxs-lookup"><span data-stu-id="07384-109">Mode</span></span>  
 <span data-ttu-id="07384-110">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="07384-110">Data type: string</span></span>  
  
 <span data-ttu-id="07384-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="07384-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="07384-112">바인딩으로 구성된 엔드포인트가 메시지 수준 보안을 사용하는지 또는 전송 수준 보안을 사용하는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="07384-112">Whether message-level and transport-level security are used by an endpoint configured with the binding.</span></span>  
  
### <a name="transport"></a><span data-ttu-id="07384-113">전송</span><span class="sxs-lookup"><span data-stu-id="07384-113">Transport</span></span>  
 <span data-ttu-id="07384-114">데이터 형식: PeerTransportSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="07384-114">Data type: PeerTransportSecuritySettings</span></span>  
  
 <span data-ttu-id="07384-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="07384-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="07384-116">전송 보안 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="07384-116">Transport security settings.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="07384-117">요구 사항</span><span class="sxs-lookup"><span data-stu-id="07384-117">Requirements</span></span>  
  
|<span data-ttu-id="07384-118">MOF</span><span class="sxs-lookup"><span data-stu-id="07384-118">MOF</span></span>|<span data-ttu-id="07384-119">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07384-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="07384-120">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="07384-120">Namespace</span></span>|<span data-ttu-id="07384-121">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07384-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="07384-122">참고 항목</span><span class="sxs-lookup"><span data-stu-id="07384-122">See Also</span></span>  
 <xref:System.ServiceModel.PeerSecuritySettings>
