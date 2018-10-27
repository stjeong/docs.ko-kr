---
title: ClientCredentials
ms.date: 03/30/2017
ms.assetid: 41dffd6b-8f14-4fed-aefb-2a1bb168efb3
ms.openlocfilehash: 8b6200f84f352d49cf142d9c8b97d1c2b36149b2
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50180902"
---
# <a name="clientcredentials"></a><span data-ttu-id="6788c-102">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="6788c-102">ClientCredentials</span></span>
<span data-ttu-id="6788c-103">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="6788c-103">ClientCredentials</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6788c-104">구문</span><span class="sxs-lookup"><span data-stu-id="6788c-104">Syntax</span></span>  
  
```csharp
class ClientCredentials : Behavior  
{  
  string ClientCertificate;  
  string HttpDigest;  
  string IssuedToken;  
  string Peer;  
  string ServiceCertificate;  
  boolean SupportInteractive;  
  string UserName;  
  string Windows;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="6788c-105">메서드</span><span class="sxs-lookup"><span data-stu-id="6788c-105">Methods</span></span>  
 <span data-ttu-id="6788c-106">ClientCredentials 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6788c-106">The ClientCredentials class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="6788c-107">속성</span><span class="sxs-lookup"><span data-stu-id="6788c-107">Properties</span></span>  
 <span data-ttu-id="6788c-108">ClientCredentials 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6788c-108">The ClientCredentials class has the following properties:</span></span>  
  
### <a name="clientcertificate"></a><span data-ttu-id="6788c-109">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6788c-109">ClientCertificate</span></span>  
 <span data-ttu-id="6788c-110">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="6788c-110">Data type: string</span></span>  
  
 <span data-ttu-id="6788c-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6788c-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6788c-112">서비스를 인증하는 데 클라이언트가 사용하는 X.509 인증서입니다.</span><span class="sxs-lookup"><span data-stu-id="6788c-112">The X.509 certificate the client uses to authenticate to the service.</span></span>  
  
### <a name="httpdigest"></a><span data-ttu-id="6788c-113">HttpDigest</span><span class="sxs-lookup"><span data-stu-id="6788c-113">HttpDigest</span></span>  
 <span data-ttu-id="6788c-114">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="6788c-114">Data type: string</span></span>  
  
 <span data-ttu-id="6788c-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6788c-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6788c-116">현재 Http Digest 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="6788c-116">The current Http Digest credential.</span></span>  
  
### <a name="issuedtoken"></a><span data-ttu-id="6788c-117">IssuedToken</span><span class="sxs-lookup"><span data-stu-id="6788c-117">IssuedToken</span></span>  
 <span data-ttu-id="6788c-118">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="6788c-118">Data type: string</span></span>  
  
 <span data-ttu-id="6788c-119">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6788c-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6788c-120">로컬 보안 토큰 서비스에 연결하기 위해 사용되는 엔드포인트 주소 및 바인딩입니다.</span><span class="sxs-lookup"><span data-stu-id="6788c-120">The endpoint address and binding used to contact the local security token service.</span></span>  
  
### <a name="peer"></a><span data-ttu-id="6788c-121">Peer</span><span class="sxs-lookup"><span data-stu-id="6788c-121">Peer</span></span>  
 <span data-ttu-id="6788c-122">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="6788c-122">Data type: string</span></span>  
  
 <span data-ttu-id="6788c-123">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6788c-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6788c-124">메시의 다른 노드에게 자신을 인증하기 위해 피어 노드가 사용하는 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="6788c-124">The credentials that the peer node uses to authenticate itself to other nodes in the mesh.</span></span>  
  
### <a name="servicecertificate"></a><span data-ttu-id="6788c-125">ServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="6788c-125">ServiceCertificate</span></span>  
 <span data-ttu-id="6788c-126">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="6788c-126">Data type: string</span></span>  
  
 <span data-ttu-id="6788c-127">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6788c-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6788c-128">서비스의 X.509 인증서입니다.</span><span class="sxs-lookup"><span data-stu-id="6788c-128">The service's X.509 certificate.</span></span>  
  
### <a name="supportinteractive"></a><span data-ttu-id="6788c-129">SupportInteractive</span><span class="sxs-lookup"><span data-stu-id="6788c-129">SupportInteractive</span></span>  
 <span data-ttu-id="6788c-130">데이터 형식: boolean</span><span class="sxs-lookup"><span data-stu-id="6788c-130">Data type: boolean</span></span>  
  
 <span data-ttu-id="6788c-131">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6788c-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6788c-132">자격 증명이 대화형 협상을 지원하는지 여부를 지정하는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="6788c-132">A Boolean value that specifies whether the credential supports interactive negotiation.</span></span>  
  
### <a name="username"></a><span data-ttu-id="6788c-133">UserName</span><span class="sxs-lookup"><span data-stu-id="6788c-133">UserName</span></span>  
 <span data-ttu-id="6788c-134">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="6788c-134">Data type: string</span></span>  
  
 <span data-ttu-id="6788c-135">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6788c-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6788c-136">서비스에게 자신을 인증하기 위해 클라이언트가 사용하는 사용자 이름 및 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="6788c-136">The username and password the client uses to authenticate itself to the service.</span></span>  
  
### <a name="windows"></a><span data-ttu-id="6788c-137">Windows</span><span class="sxs-lookup"><span data-stu-id="6788c-137">Windows</span></span>  
 <span data-ttu-id="6788c-138">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="6788c-138">Data type: string</span></span>  
  
 <span data-ttu-id="6788c-139">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6788c-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6788c-140">서비스에게 자신을 인증하기 위해 클라이언트가 사용하는 Windows 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="6788c-140">The windows credentials the client uses to authenticate itself to the service.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6788c-141">요구 사항</span><span class="sxs-lookup"><span data-stu-id="6788c-141">Requirements</span></span>  
  
|<span data-ttu-id="6788c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6788c-142">MOF</span></span>|<span data-ttu-id="6788c-143">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6788c-143">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="6788c-144">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="6788c-144">Namespace</span></span>|<span data-ttu-id="6788c-145">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6788c-145">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6788c-146">참고 항목</span><span class="sxs-lookup"><span data-stu-id="6788c-146">See Also</span></span>  
 <xref:System.ServiceModel.Description.ClientCredentials>
