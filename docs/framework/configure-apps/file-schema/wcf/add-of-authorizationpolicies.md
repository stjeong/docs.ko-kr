---
title: '&lt;authorizationPolicies&gt;의 &lt;add&gt;'
ms.date: 03/30/2017
ms.assetid: 613a03d8-4384-4556-bce2-8c23286c0bb0
ms.openlocfilehash: c283f99bedc16352ffca4c41c3d4628271200695
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54577522"
---
# <a name="ltaddgt-of-ltauthorizationpoliciesgt"></a><span data-ttu-id="58a53-102">&lt;authorizationPolicies&gt;의 &lt;add&gt;</span><span class="sxs-lookup"><span data-stu-id="58a53-102">&lt;add&gt; of &lt;authorizationPolicies&gt;</span></span>
<span data-ttu-id="58a53-103">클레임 변형에 대한 권한 부여 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="58a53-103">Specifies an authorization policy for claim transformation.</span></span>  
  
 <span data-ttu-id="58a53-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="58a53-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="58a53-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="58a53-105">\<behaviors></span></span>  
<span data-ttu-id="58a53-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="58a53-106">\<behavior></span></span>  
<span data-ttu-id="58a53-107">\<serviceAuthorization></span><span class="sxs-lookup"><span data-stu-id="58a53-107">\<serviceAuthorization></span></span>  
<span data-ttu-id="58a53-108">\<authorizationPolicies></span><span class="sxs-lookup"><span data-stu-id="58a53-108">\<authorizationPolicies></span></span>  
<span data-ttu-id="58a53-109">\<add></span><span class="sxs-lookup"><span data-stu-id="58a53-109">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="58a53-110">구문</span><span class="sxs-lookup"><span data-stu-id="58a53-110">Syntax</span></span>  
  
```xml  
<authorizationPolicies>
  <add policyType="String" />
</authorizationPolicies>
```  
  
## <a name="type"></a><span data-ttu-id="58a53-111">형식</span><span class="sxs-lookup"><span data-stu-id="58a53-111">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="58a53-112">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="58a53-112">Attributes and Elements</span></span>  
 <span data-ttu-id="58a53-113">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="58a53-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="58a53-114">특성</span><span class="sxs-lookup"><span data-stu-id="58a53-114">Attributes</span></span>  
  
|<span data-ttu-id="58a53-115">특성</span><span class="sxs-lookup"><span data-stu-id="58a53-115">Attribute</span></span>|<span data-ttu-id="58a53-116">설명</span><span class="sxs-lookup"><span data-stu-id="58a53-116">Description</span></span>|  
|---------------|-----------------|  
|`policyType`|<span data-ttu-id="58a53-117">필수 String 특성입니다.</span><span class="sxs-lookup"><span data-stu-id="58a53-117">A required String attribute.</span></span><br /><br /> <span data-ttu-id="58a53-118">Windows Communication Foundation (WCF) 액세스 제어 모델 형식으로 권한 부여 정책의 집합을 프로 비전을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58a53-118">The Windows Communication Foundation (WCF) access control model supports provisioning a set of authorization policies as types.</span></span> <span data-ttu-id="58a53-119">이 특성은 한 입력 클레임 집합을 다른 클레임 집합으로 변형할 수 있도록 하는 권한 부여 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="58a53-119">This attribute specifies an authorization policy, which enables transformation of one set of input claims into another set of claims.</span></span> <span data-ttu-id="58a53-120">그에 따라 액세스 제어가 부여되거나 거부됩니다.</span><span class="sxs-lookup"><span data-stu-id="58a53-120">Access control can be granted or denied based on that.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="58a53-121">자식 요소</span><span class="sxs-lookup"><span data-stu-id="58a53-121">Child Elements</span></span>  
 <span data-ttu-id="58a53-122">없음</span><span class="sxs-lookup"><span data-stu-id="58a53-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="58a53-123">부모 요소</span><span class="sxs-lookup"><span data-stu-id="58a53-123">Parent Elements</span></span>  
  
|<span data-ttu-id="58a53-124">요소</span><span class="sxs-lookup"><span data-stu-id="58a53-124">Element</span></span>|<span data-ttu-id="58a53-125">설명</span><span class="sxs-lookup"><span data-stu-id="58a53-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="58a53-126">\<authorizationPolicies></span><span class="sxs-lookup"><span data-stu-id="58a53-126">\<authorizationPolicies></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/authorizationpolicies.md)|<span data-ttu-id="58a53-127">권한 부여 정책 형식 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="58a53-127">Specifies a collection of authorization policy types.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="58a53-128">설명</span><span class="sxs-lookup"><span data-stu-id="58a53-128">Remarks</span></span>  
 <span data-ttu-id="58a53-129">각 인증 정책에는 문자열에 해당하는 단일 필수 `policyType` 특성이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58a53-129">Each authorization policy contains a single required `policyType` attribute that is a string.</span></span> <span data-ttu-id="58a53-130">이 특성은 한 입력 클레임 집합을 다른 클레임 집합으로 변환할 수 있도록 하는 인증 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="58a53-130">The attribute specifies an authorization policy, which enables transformation of one set of input claims into another set of claims.</span></span> <span data-ttu-id="58a53-131">그에 따라 액세스 제어가 부여되거나 거부됩니다.</span><span class="sxs-lookup"><span data-stu-id="58a53-131">Access control can be granted or denied based on that.</span></span> <span data-ttu-id="58a53-132">권한 부여 정책이 작동 하는 방법에 대 한 자세한 내용은 참조 하세요. <xref:System.IdentityModel.Policy.IAuthorizationPolicy> 하 고 [권한 부여 정책](../../../../../docs/framework/wcf/samples/authorization-policy.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="58a53-132">For more information on how an authorization policy works, see <xref:System.IdentityModel.Policy.IAuthorizationPolicy> and [Authorization Policy](../../../../../docs/framework/wcf/samples/authorization-policy.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="58a53-133">참고자료</span><span class="sxs-lookup"><span data-stu-id="58a53-133">See also</span></span>
- <xref:System.ServiceModel.Configuration.ServiceAuthorizationElement>
- <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior.ExternalAuthorizationPolicies%2A>
- <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior>
- <xref:System.ServiceModel.Configuration.AuthorizationPolicyTypeElement>
- <xref:System.ServiceModel.Configuration.ServiceAuthorizationElement.AuthorizationPolicies%2A>
- <xref:System.ServiceModel.Configuration.AuthorizationPolicyTypeElementCollection>
- <xref:System.IdentityModel.Policy.IAuthorizationPolicy>
- [<span data-ttu-id="58a53-134">서비스 작업에 대한 액세스 승인</span><span class="sxs-lookup"><span data-stu-id="58a53-134">Authorizing Access to Service Operations</span></span>](../../../../../docs/framework/wcf/samples/authorizing-access-to-service-operations.md)
- [<span data-ttu-id="58a53-135">방법: 서비스에 대 한 사용자 지정 권한 부여 관리자 만들기</span><span class="sxs-lookup"><span data-stu-id="58a53-135">How to: Create a Custom Authorization Manager for a Service</span></span>](../../../../../docs/framework/wcf/extending/how-to-create-a-custom-authorization-manager-for-a-service.md)
- [<span data-ttu-id="58a53-136">\<add></span><span class="sxs-lookup"><span data-stu-id="58a53-136">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-authorizationpolicies.md)
- [<span data-ttu-id="58a53-137">권한 부여 정책</span><span class="sxs-lookup"><span data-stu-id="58a53-137">Authorization Policy</span></span>](../../../../../docs/framework/wcf/samples/authorization-policy.md)
