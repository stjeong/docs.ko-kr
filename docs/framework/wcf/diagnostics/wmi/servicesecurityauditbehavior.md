---
title: ServiceSecurityAuditBehavior
ms.date: 03/30/2017
ms.assetid: 2c5809e7-5364-44ce-bc71-848be4672e2a
ms.openlocfilehash: e8b24877c2d76a3f2f90c27ae83374c7bca1328b
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50181162"
---
# <a name="servicesecurityauditbehavior"></a><span data-ttu-id="e3e93-102">ServiceSecurityAuditBehavior</span><span class="sxs-lookup"><span data-stu-id="e3e93-102">ServiceSecurityAuditBehavior</span></span>
<span data-ttu-id="e3e93-103">ServiceSecurityAuditBehavior</span><span class="sxs-lookup"><span data-stu-id="e3e93-103">ServiceSecurityAuditBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e3e93-104">구문</span><span class="sxs-lookup"><span data-stu-id="e3e93-104">Syntax</span></span>  
  
```csharp  
class ServiceSecurityAuditBehavior : Behavior  
{  
  string AuditLogLocation;  
  string MessageAuthenticationAuditLevel;  
  string ServiceAuthorizationAuditLevel;  
  boolean SuppressAuditFailure;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="e3e93-105">메서드</span><span class="sxs-lookup"><span data-stu-id="e3e93-105">Methods</span></span>  
 <span data-ttu-id="e3e93-106">ServiceSecurityAuditBehavior 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3e93-106">The ServiceSecurityAuditBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="e3e93-107">속성</span><span class="sxs-lookup"><span data-stu-id="e3e93-107">Properties</span></span>  
 <span data-ttu-id="e3e93-108">ServiceSecurityAuditBehavior 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3e93-108">The ServiceSecurityAuditBehavior class has the following properties:</span></span>  
  
### <a name="auditloglocation"></a><span data-ttu-id="e3e93-109">AuditLogLocation</span><span class="sxs-lookup"><span data-stu-id="e3e93-109">AuditLogLocation</span></span>  
 <span data-ttu-id="e3e93-110">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="e3e93-110">Data type: string</span></span>  
  
 <span data-ttu-id="e3e93-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="e3e93-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e3e93-112">감사 로그의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e93-112">The location of the audit log.</span></span>  
  
### <a name="messageauthenticationauditlevel"></a><span data-ttu-id="e3e93-113">MessageAuthenticationAuditLevel</span><span class="sxs-lookup"><span data-stu-id="e3e93-113">MessageAuthenticationAuditLevel</span></span>  
 <span data-ttu-id="e3e93-114">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="e3e93-114">Data type: string</span></span>  
  
 <span data-ttu-id="e3e93-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="e3e93-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e3e93-116">감사 이벤트 로깅에 사용되는 메시지 인증 수준의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e93-116">The type of message authentication level that is used to log audit events.</span></span>  
  
### <a name="serviceauthorizationauditlevel"></a><span data-ttu-id="e3e93-117">ServiceAuthorizationAuditLevel</span><span class="sxs-lookup"><span data-stu-id="e3e93-117">ServiceAuthorizationAuditLevel</span></span>  
 <span data-ttu-id="e3e93-118">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="e3e93-118">Data type: string</span></span>  
  
 <span data-ttu-id="e3e93-119">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="e3e93-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e3e93-120">감사 로그에 기록되는 권한 부여 이벤트의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e93-120">The types of authorization events that are recorded in the audit log.</span></span>  
  
### <a name="suppressauditfailure"></a><span data-ttu-id="e3e93-121">SuppressAuditFailure</span><span class="sxs-lookup"><span data-stu-id="e3e93-121">SuppressAuditFailure</span></span>  
 <span data-ttu-id="e3e93-122">데이터 형식: boolean</span><span class="sxs-lookup"><span data-stu-id="e3e93-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="e3e93-123">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="e3e93-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e3e93-124">감사 로그 쓰기의 실패를 표시하지 않기 위한 동작을 지정하는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e93-124">A boolean value that specifies the behavior for suppressing failures of writing to the audit log.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e3e93-125">요구 사항</span><span class="sxs-lookup"><span data-stu-id="e3e93-125">Requirements</span></span>  
  
|<span data-ttu-id="e3e93-126">MOF</span><span class="sxs-lookup"><span data-stu-id="e3e93-126">MOF</span></span>|<span data-ttu-id="e3e93-127">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3e93-127">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="e3e93-128">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="e3e93-128">Namespace</span></span>|<span data-ttu-id="e3e93-129">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3e93-129">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e3e93-130">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e3e93-130">See Also</span></span>  
 <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior>
