---
title: PeerSecuritySettings
ms.date: 03/30/2017
ms.assetid: 24ae0d35-f3a3-419b-afd6-686e22aae27b
ms.openlocfilehash: 92aca4c790607de91314aacf6414d0dfacea9a9f
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50193164"
---
# <a name="peersecuritysettings"></a><span data-ttu-id="07e41-102">PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="07e41-102">PeerSecuritySettings</span></span>
<span data-ttu-id="07e41-103">PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="07e41-103">PeerSecuritySettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="07e41-104">구문</span><span class="sxs-lookup"><span data-stu-id="07e41-104">Syntax</span></span>  
  
```csharp
class PeerSecuritySettings  
{  
  string Mode;  
  PeerTransportSecuritySettings Transport;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="07e41-105">메서드</span><span class="sxs-lookup"><span data-stu-id="07e41-105">Methods</span></span>  
 <span data-ttu-id="07e41-106">PeerSecuritySettings 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07e41-106">The PeerSecuritySettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="07e41-107">속성</span><span class="sxs-lookup"><span data-stu-id="07e41-107">Properties</span></span>  
 <span data-ttu-id="07e41-108">PeerSecuritySettings 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07e41-108">The PeerSecuritySettings class has the following properties:</span></span>  
  
### <a name="mode"></a><span data-ttu-id="07e41-109">모드</span><span class="sxs-lookup"><span data-stu-id="07e41-109">Mode</span></span>  
 <span data-ttu-id="07e41-110">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="07e41-110">Data type: string</span></span>  
  
 <span data-ttu-id="07e41-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="07e41-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="07e41-112">바인딩으로 구성된 엔드포인트가 메시지 수준 보안을 사용하는지 또는 전송 수준 보안을 사용하는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="07e41-112">Whether message-level and transport-level security are used by an endpoint configured with the binding.</span></span>  
  
### <a name="transport"></a><span data-ttu-id="07e41-113">전송</span><span class="sxs-lookup"><span data-stu-id="07e41-113">Transport</span></span>  
 <span data-ttu-id="07e41-114">데이터 형식: PeerTransportSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="07e41-114">Data type: PeerTransportSecuritySettings</span></span>  
  
 <span data-ttu-id="07e41-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="07e41-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="07e41-116">전송 보안 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="07e41-116">Transport security settings.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="07e41-117">요구 사항</span><span class="sxs-lookup"><span data-stu-id="07e41-117">Requirements</span></span>  
  
|<span data-ttu-id="07e41-118">MOF</span><span class="sxs-lookup"><span data-stu-id="07e41-118">MOF</span></span>|<span data-ttu-id="07e41-119">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07e41-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="07e41-120">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="07e41-120">Namespace</span></span>|<span data-ttu-id="07e41-121">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07e41-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="07e41-122">참고 항목</span><span class="sxs-lookup"><span data-stu-id="07e41-122">See Also</span></span>  
 <xref:System.ServiceModel.PeerSecuritySettings>
