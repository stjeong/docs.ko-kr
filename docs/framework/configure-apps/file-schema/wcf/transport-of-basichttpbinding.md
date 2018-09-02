---
title: '&lt;basicHttpBinding&gt;의 &lt;transport&gt;'
ms.date: 03/30/2017
ms.assetid: 4c5ba293-3d7e-47a6-b84e-e9022857b7e5
ms.openlocfilehash: f3f9ad2c8b587a87abea7dc22abb98fdfb6ea77e
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43416003"
---
# <a name="lttransportgt-of-ltbasichttpbindinggt"></a><span data-ttu-id="ccd33-102">&lt;basicHttpBinding&gt;의 &lt;transport&gt;</span><span class="sxs-lookup"><span data-stu-id="ccd33-102">&lt;transport&gt; of &lt;basicHttpBinding&gt;</span></span>
<span data-ttu-id="ccd33-103">HTTP 전송의 인증 매개 변수를 제어하는 속성을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-103">Defines properties that control authentication parameters for the HTTP transport.</span></span>  
  
 <span data-ttu-id="ccd33-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="ccd33-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="ccd33-105">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="ccd33-105">\<bindings></span></span>  
<span data-ttu-id="ccd33-106">\<basicHttpBinding></span><span class="sxs-lookup"><span data-stu-id="ccd33-106">\<basicHttpBinding></span></span>  
<span data-ttu-id="ccd33-107">\<바인딩 ></span><span class="sxs-lookup"><span data-stu-id="ccd33-107">\<binding></span></span>  
<span data-ttu-id="ccd33-108">\<security></span><span class="sxs-lookup"><span data-stu-id="ccd33-108">\<security></span></span>  
<span data-ttu-id="ccd33-109">\<transport></span><span class="sxs-lookup"><span data-stu-id="ccd33-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ccd33-110">구문</span><span class="sxs-lookup"><span data-stu-id="ccd33-110">Syntax</span></span>  
  
```xml  
<basicHttpBinding>  
    <binding>  
        <security  
        mode="None|Transport|Message|TransportWithMessageCredential|TransportCredentialOnly">  
            <transport clientCredentialType="None|Basic|Digest|Ntlm|Windows"  
             proxyCredentialType="None|Basic|Digest|Ntlm|Windows" realm="string" >  
                <extendedProtectionPolicy  
                     policyEnforcement="Never|WhenSupported|Always"  
                     protectionScenario="TransportSelected|TrustedProxy">  
                    <customServiceNames></customServiceNames>  
                        </extendedProtectionPolicy>  
            </transport>  
        </security>  
    </binding>  
</basicHttpBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ccd33-111">특성 및 요소</span><span class="sxs-lookup"><span data-stu-id="ccd33-111">Attributes and Elements</span></span>  
 <span data-ttu-id="ccd33-112">다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ccd33-113">특성</span><span class="sxs-lookup"><span data-stu-id="ccd33-113">Attributes</span></span>  
  
|<span data-ttu-id="ccd33-114">특성</span><span class="sxs-lookup"><span data-stu-id="ccd33-114">Attribute</span></span>|<span data-ttu-id="ccd33-115">설명</span><span class="sxs-lookup"><span data-stu-id="ccd33-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ccd33-116">clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="ccd33-116">clientCredentialType</span></span>|<span data-ttu-id="ccd33-117">-HTTP 인증을 사용 하 여 클라이언트 인증을 수행할 때 사용할 자격 증명의 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-117">-   Specifies the type of credential to be used when performing client authentication using HTTP authentication.</span></span>  <span data-ttu-id="ccd33-118">기본값은 `None`입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-118">The default is `None`.</span></span> <span data-ttu-id="ccd33-119">이 특성은 <xref:System.ServiceModel.HttpClientCredentialType> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-119">This attribute is of type <xref:System.ServiceModel.HttpClientCredentialType>.</span></span>|  
|<span data-ttu-id="ccd33-120">proxyCredentialType</span><span class="sxs-lookup"><span data-stu-id="ccd33-120">proxyCredentialType</span></span>|<span data-ttu-id="ccd33-121">-프록시를 사용 하 여 HTTP를 통해 도메인 내에서 클라이언트 인증을 수행할 때 사용할 자격 증명의 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-121">-   Specifies the type of credential to be used when performing client authentication from within a domain using a proxy over HTTP.</span></span> <span data-ttu-id="ccd33-122">이 특성은 부모 `mode` 요소의 `security` 특성이 `Transport` 또는 `TransportCredentialsOnly`일 때만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-122">This attribute is applicable only when the `mode` attribute of the parent `security` element is `Transport` or `TransportCredentialsOnly`.</span></span> <span data-ttu-id="ccd33-123">이 특성은 <xref:System.ServiceModel.HttpProxyCredentialType> 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-123">This attribute is of type <xref:System.ServiceModel.HttpProxyCredentialType>.</span></span>|  
|<span data-ttu-id="ccd33-124">realm</span><span class="sxs-lookup"><span data-stu-id="ccd33-124">realm</span></span>|<span data-ttu-id="ccd33-125">다이제스트 또는 기본 인증의 HTTP 인증 체계에 사용되는 영역을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-125">A string that specifies the realm that is used by the HTTP authentication scheme for digest or basic authentication.</span></span> <span data-ttu-id="ccd33-126">기본값은 빈 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-126">The default is an empty string.</span></span>|  
|<span data-ttu-id="ccd33-127">policyEnforcement</span><span class="sxs-lookup"><span data-stu-id="ccd33-127">policyEnforcement</span></span>|<span data-ttu-id="ccd33-128">이 열거형은 <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy>가 적용되는 경우를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-128">This enumeration specifies when the <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> should be enforced.</span></span><br /><br /> <span data-ttu-id="ccd33-129">1.  Never - 정책이 적용되지 않습니다(확장 보호가 사용되지 않음).</span><span class="sxs-lookup"><span data-stu-id="ccd33-129">1.  Never – The policy is never enforced (Extended Protection is disabled).</span></span><br /><span data-ttu-id="ccd33-130">2.  WhenSupported – 클라이언트에서 확장 보호를 지원하는 경우에만 정책이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-130">2.  WhenSupported – The policy is enforced only if the client supports Extended Protection.</span></span><br /><span data-ttu-id="ccd33-131">3.  Always – 정책이 항상 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-131">3.  Always – The policy is always enforced.</span></span> <span data-ttu-id="ccd33-132">확장 보호를 지원하지 않는 클라이언트는 인증되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-132">Clients which don’t support Extended Protection will fail to authenticate.</span></span>|  
|<span data-ttu-id="ccd33-133">protectionScenario</span><span class="sxs-lookup"><span data-stu-id="ccd33-133">protectionScenario</span></span>|<span data-ttu-id="ccd33-134">이 열거형은 정책을 통해 적용되는 보호 시나리오를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-134">This enumeration specifies the protection scenario enforced by the policy.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="ccd33-135">clientCredentialType 특성</span><span class="sxs-lookup"><span data-stu-id="ccd33-135">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="ccd33-136">값</span><span class="sxs-lookup"><span data-stu-id="ccd33-136">Value</span></span>|<span data-ttu-id="ccd33-137">설명</span><span class="sxs-lookup"><span data-stu-id="ccd33-137">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="ccd33-138">없음</span><span class="sxs-lookup"><span data-stu-id="ccd33-138">None</span></span>|<span data-ttu-id="ccd33-139">메시지가 전송 중에 보호되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-139">Messages are not secured during transfer.</span></span>|  
|<span data-ttu-id="ccd33-140">Basic</span><span class="sxs-lookup"><span data-stu-id="ccd33-140">Basic</span></span>|<span data-ttu-id="ccd33-141">기본 인증을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-141">Specifies basic authentication.</span></span>|  
|<span data-ttu-id="ccd33-142">Digest</span><span class="sxs-lookup"><span data-stu-id="ccd33-142">Digest</span></span>|<span data-ttu-id="ccd33-143">다이제스트 인증을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-143">Specifies digest authentication.</span></span>|  
|<span data-ttu-id="ccd33-144">Ntlm</span><span class="sxs-lookup"><span data-stu-id="ccd33-144">Ntlm</span></span>|<span data-ttu-id="ccd33-145">Windows 인증이 실패할 경우 가능하면 NTLM 인증을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-145">Specifies NTLM authentication when possible, and if Windows authentication fails.</span></span>|  
|<span data-ttu-id="ccd33-146">Windows</span><span class="sxs-lookup"><span data-stu-id="ccd33-146">Windows</span></span>|<span data-ttu-id="ccd33-147">Windows 통합 인증을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-147">Specifies Windows integrated authentication.</span></span>|  
  
## <a name="proxycredentialtype-attribute"></a><span data-ttu-id="ccd33-148">proxyCredentialType 특성</span><span class="sxs-lookup"><span data-stu-id="ccd33-148">proxyCredentialType Attribute</span></span>  
  
|<span data-ttu-id="ccd33-149">값</span><span class="sxs-lookup"><span data-stu-id="ccd33-149">Value</span></span>|<span data-ttu-id="ccd33-150">설명</span><span class="sxs-lookup"><span data-stu-id="ccd33-150">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="ccd33-151">없음</span><span class="sxs-lookup"><span data-stu-id="ccd33-151">None</span></span>|<span data-ttu-id="ccd33-152">-메시지 전송 하는 동안 보안이 유지 되지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-152">-   Messages are not secured during transfer.</span></span>|  
|<span data-ttu-id="ccd33-153">Basic</span><span class="sxs-lookup"><span data-stu-id="ccd33-153">Basic</span></span>|<span data-ttu-id="ccd33-154">RFC 2617 – HTTP 인증: 기본 및 다이제스트 인증에 정의된 대로 기본 인증을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-154">Specifies basic authentication as defined by RFC 2617 – HTTP Authentication: Basic and Digest Authentication.</span></span>|  
|<span data-ttu-id="ccd33-155">Digest</span><span class="sxs-lookup"><span data-stu-id="ccd33-155">Digest</span></span>|<span data-ttu-id="ccd33-156">RFC 2617 – HTTP 인증: 기본 및 다이제스트 인증에 정의된 대로 다이제스트 인증을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-156">Specifies digest authentication as defined by RFC 2617 – HTTP Authentication: Basic and Digest Authentication.</span></span>|  
|<span data-ttu-id="ccd33-157">Ntlm</span><span class="sxs-lookup"><span data-stu-id="ccd33-157">Ntlm</span></span>|<span data-ttu-id="ccd33-158">Windows 인증이 실패할 경우 가능하면 NTLM 인증을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-158">Specifies NTLM authentication when possible, and if Windows authentication fails.</span></span>|  
|<span data-ttu-id="ccd33-159">Windows</span><span class="sxs-lookup"><span data-stu-id="ccd33-159">Windows</span></span>|<span data-ttu-id="ccd33-160">Windows 통합 인증을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-160">Specifies Windows integrated authentication.</span></span>|  
|<span data-ttu-id="ccd33-161">인증서</span><span class="sxs-lookup"><span data-stu-id="ccd33-161">Certificate</span></span>|<span data-ttu-id="ccd33-162">인증서를 사용하여 클라이언트 인증을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-162">Performs client authentication using a certificate.</span></span> <span data-ttu-id="ccd33-163">이 옵션은 부모 `Mode` 요소의 `security` 특성이 Transport로 설정되어 있을 때만 작동하며 TransportCredentialOnly로 설정된 경우에는 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-163">This option works only if the `Mode` attribute of the parent `security` element is set to Transport, and will not work if it is set to TransportCredentialOnly.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ccd33-164">자식 요소</span><span class="sxs-lookup"><span data-stu-id="ccd33-164">Child Elements</span></span>  
 <span data-ttu-id="ccd33-165">없음</span><span class="sxs-lookup"><span data-stu-id="ccd33-165">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ccd33-166">부모 요소</span><span class="sxs-lookup"><span data-stu-id="ccd33-166">Parent Elements</span></span>  
  
|<span data-ttu-id="ccd33-167">요소</span><span class="sxs-lookup"><span data-stu-id="ccd33-167">Element</span></span>|<span data-ttu-id="ccd33-168">설명</span><span class="sxs-lookup"><span data-stu-id="ccd33-168">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ccd33-169">\<security></span><span class="sxs-lookup"><span data-stu-id="ccd33-169">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-basichttpbinding.md)|<span data-ttu-id="ccd33-170">에 대 한 보안 기능을 정의 합니다 [ \<basicHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-170">Defines the security capabilities for the [\<basicHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md).</span></span>|  
  
## <a name="example"></a><span data-ttu-id="ccd33-171">예제</span><span class="sxs-lookup"><span data-stu-id="ccd33-171">Example</span></span>  
 <span data-ttu-id="ccd33-172">다음 예제에서는 기본 바인딩이 있는 SSL 전송 보안을 사용하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-172">The following example demonstrates the use of SSL transport security with the basic binding.</span></span> <span data-ttu-id="ccd33-173">기본적으로 기본 바인딩은 HTTP 통신을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd33-173">By default, the basic binding supports HTTP communication.</span></span>  
  
```xml  
<system.serviceModel>  
   <services>  
      <service   
          type="Microsoft.ServiceModel.Samples.CalculatorService"  
          behaviorConfiguration="CalculatorServiceBehavior">  
         <endpoint address=""  
               binding="basicHttpBinding"  
               bindingConfiguration="Binding1"   
               contract="Microsoft.ServiceModel.Samples.ICalculator" />  
      </service>  
   </services>  
    <bindings>  
        <basicHttpBinding>  
        <!-- Configure basicHttpBinding with Transport security -- >  
        <!-- mode and clientCredentialType set to None.-->  
           <binding name="Binding1">  
               <security mode="Transport">  
                   <transport clientCredentialType="None"  
                              proxyCredentialType="None">  
                       <extendedProtectionPolicy  
                          policyEnforcement="WhenSupported"  
                          protectionScenario="TransportSelected">  
                    <customServiceNames></customServiceNames>  
                       </extendedProtectionPolicy>  
               </security>  
           </binding>  
        </basicHttpBinding>  
    </bindings>  
</system.serviceModel>  
```  
  
## <a name="see-also"></a><span data-ttu-id="ccd33-174">참고 항목</span><span class="sxs-lookup"><span data-stu-id="ccd33-174">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.BasicHttpSecurityElement.Transport%2A>  
 <xref:System.ServiceModel.BasicHttpSecurity.Transport%2A>  
 <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement>  
 <xref:System.ServiceModel.HttpTransportSecurity>  
 [<span data-ttu-id="ccd33-175">서비스 및 클라이언트에 보안 설정</span><span class="sxs-lookup"><span data-stu-id="ccd33-175">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="ccd33-176">바인딩</span><span class="sxs-lookup"><span data-stu-id="ccd33-176">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="ccd33-177">시스템 제공 바인딩 구성</span><span class="sxs-lookup"><span data-stu-id="ccd33-177">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="ccd33-178">바인딩을 사용 하 여 Windows Communication Foundation 서비스 및 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="ccd33-178">Using Bindings to Configure Windows Communication Foundation Services and Clients</span></span>](https://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [<span data-ttu-id="ccd33-179">\<binding></span><span class="sxs-lookup"><span data-stu-id="ccd33-179">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
