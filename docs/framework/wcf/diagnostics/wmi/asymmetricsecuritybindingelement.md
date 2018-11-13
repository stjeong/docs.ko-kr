---
title: AsymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: 7bd3b6be-8f77-4927-93ae-6fa371893cca
ms.openlocfilehash: 076313548828f1fbce9c68b48c0fa7db9cca095f
ms.sourcegitcommit: 296183dbe35077b5c5e5e74d5fbe7f399bc507ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/05/2018
ms.locfileid: "50982792"
---
# <a name="asymmetricsecuritybindingelement"></a><span data-ttu-id="9b886-102">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="9b886-102">AsymmetricSecurityBindingElement</span></span>
<span data-ttu-id="9b886-103">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="9b886-103">AsymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9b886-104">구문</span><span class="sxs-lookup"><span data-stu-id="9b886-104">Syntax</span></span>  
  
```csharp
class AsymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="9b886-105">메서드</span><span class="sxs-lookup"><span data-stu-id="9b886-105">Methods</span></span>  
 <span data-ttu-id="9b886-106">AsymmetricSecurityBindingElement 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b886-106">The AsymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="9b886-107">속성</span><span class="sxs-lookup"><span data-stu-id="9b886-107">Properties</span></span>  
 <span data-ttu-id="9b886-108">AsymmetricSecurityBindingElement 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b886-108">The AsymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="9b886-109">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="9b886-109">MessageProtectionOrder</span></span>  
 <span data-ttu-id="9b886-110">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="9b886-110">Data type: string</span></span>  
  
 <span data-ttu-id="9b886-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="9b886-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9b886-112">이 바인딩의 메시지 암호화 및 서명 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="9b886-112">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="9b886-113">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="9b886-113">RequireSignatureConfirmation</span></span>  
 <span data-ttu-id="9b886-114">데이터 형식: boolean</span><span class="sxs-lookup"><span data-stu-id="9b886-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="9b886-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="9b886-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9b886-116">바인딩에 서명 확인이 필요한지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="9b886-116">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9b886-117">요구 사항</span><span class="sxs-lookup"><span data-stu-id="9b886-117">Requirements</span></span>  
  
|<span data-ttu-id="9b886-118">MOF</span><span class="sxs-lookup"><span data-stu-id="9b886-118">MOF</span></span>|<span data-ttu-id="9b886-119">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b886-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="9b886-120">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="9b886-120">Namespace</span></span>|<span data-ttu-id="9b886-121">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b886-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9b886-122">참고 항목</span><span class="sxs-lookup"><span data-stu-id="9b886-122">See Also</span></span>  
 <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>
