---
title: SymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: b2e182b6-c041-4d80-a926-6058068d9f79
ms.openlocfilehash: 7b979a6872da15c4130e580a3f7327802f42db18
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54701393"
---
# <a name="symmetricsecuritybindingelement"></a><span data-ttu-id="56123-102">SymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="56123-102">SymmetricSecurityBindingElement</span></span>
<span data-ttu-id="56123-103">SymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="56123-103">SymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="56123-104">구문</span><span class="sxs-lookup"><span data-stu-id="56123-104">Syntax</span></span>  
  
```csharp
class SymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="56123-105">메서드</span><span class="sxs-lookup"><span data-stu-id="56123-105">Methods</span></span>  
 <span data-ttu-id="56123-106">SymmetricSecurityBindingElement 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56123-106">The SymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="56123-107">속성</span><span class="sxs-lookup"><span data-stu-id="56123-107">Properties</span></span>  
 <span data-ttu-id="56123-108">SymmetricSecurityBindingElement 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56123-108">The SymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="56123-109">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="56123-109">MessageProtectionOrder</span></span>  
 <span data-ttu-id="56123-110">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="56123-110">Data type: string</span></span>  
  
 <span data-ttu-id="56123-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="56123-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="56123-112">이 바인딩의 메시지 암호화 및 서명 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="56123-112">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="56123-113">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="56123-113">RequireSignatureConfirmation</span></span>  
 <span data-ttu-id="56123-114">데이터 형식: boolean</span><span class="sxs-lookup"><span data-stu-id="56123-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="56123-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="56123-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="56123-116">바인딩에 서명 확인이 필요한지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="56123-116">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="56123-117">요구 사항</span><span class="sxs-lookup"><span data-stu-id="56123-117">Requirements</span></span>  
  
|<span data-ttu-id="56123-118">MOF</span><span class="sxs-lookup"><span data-stu-id="56123-118">MOF</span></span>|<span data-ttu-id="56123-119">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56123-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="56123-120">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="56123-120">Namespace</span></span>|<span data-ttu-id="56123-121">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56123-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="56123-122">참고자료</span><span class="sxs-lookup"><span data-stu-id="56123-122">See also</span></span>
- <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>
