---
title: OperationBehaviorAttribute
ms.date: 03/30/2017
ms.assetid: 8c9b0755-9e83-411f-bdcb-61a586022797
ms.openlocfilehash: d0bf59e6064748a045f761777a2f8f3e88f1cb5a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54504329"
---
# <a name="operationbehaviorattribute"></a><span data-ttu-id="6d664-102">OperationBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="6d664-102">OperationBehaviorAttribute</span></span>
<span data-ttu-id="6d664-103">OperationBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="6d664-103">OperationBehaviorAttribute</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6d664-104">구문</span><span class="sxs-lookup"><span data-stu-id="6d664-104">Syntax</span></span>  
  
```csharp
class OperationBehaviorAttribute : Behavior  
{  
  boolean AutoDisposeParameters;  
  string Impersonation;  
  string ReleaseInstanceMode;  
  boolean TransactionAutoComplete;  
  boolean TransactionScopeRequired;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="6d664-105">메서드</span><span class="sxs-lookup"><span data-stu-id="6d664-105">Methods</span></span>  
 <span data-ttu-id="6d664-106">OperationBehaviorAttribute 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d664-106">The OperationBehaviorAttribute class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="6d664-107">속성</span><span class="sxs-lookup"><span data-stu-id="6d664-107">Properties</span></span>  
 <span data-ttu-id="6d664-108">OperationBehaviorAttribute 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d664-108">The OperationBehaviorAttribute class has the following properties:</span></span>  
  
### <a name="autodisposeparameters"></a><span data-ttu-id="6d664-109">AutoDisposeParameters</span><span class="sxs-lookup"><span data-stu-id="6d664-109">AutoDisposeParameters</span></span>  
 <span data-ttu-id="6d664-110">데이터 형식: boolean</span><span class="sxs-lookup"><span data-stu-id="6d664-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="6d664-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6d664-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6d664-112">매개 변수에 대한 자동 삭제 기능 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="6d664-112">The state of the auto-dispose feature for parameters.</span></span>  
  
### <a name="impersonation"></a><span data-ttu-id="6d664-113">가장</span><span class="sxs-lookup"><span data-stu-id="6d664-113">Impersonation</span></span>  
 <span data-ttu-id="6d664-114">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="6d664-114">Data type: string</span></span>  
  
 <span data-ttu-id="6d664-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6d664-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6d664-116">작업에서 지원하는 호출자의 가장 수준을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6d664-116">Indicates the level of caller impersonation that the operation supports.</span></span>  
  
### <a name="releaseinstancemode"></a><span data-ttu-id="6d664-117">ReleaseInstanceMode</span><span class="sxs-lookup"><span data-stu-id="6d664-117">ReleaseInstanceMode</span></span>  
 <span data-ttu-id="6d664-118">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="6d664-118">Data type: string</span></span>  
  
 <span data-ttu-id="6d664-119">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6d664-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6d664-120">작업 과정에서 개체를 재활용하기 위해 호출하는 시점을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6d664-120">Indicates when in the course of an operation invocation to recycle the object.</span></span>  
  
### <a name="transactionautocomplete"></a><span data-ttu-id="6d664-121">TransactionAutoComplete</span><span class="sxs-lookup"><span data-stu-id="6d664-121">TransactionAutoComplete</span></span>  
 <span data-ttu-id="6d664-122">데이터 형식: boolean</span><span class="sxs-lookup"><span data-stu-id="6d664-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="6d664-123">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6d664-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6d664-124">처리되지 않은 예외가 발생하지 않을 때 현재 트랜잭션을 자동으로 커밋할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6d664-124">Indicates whether to automatically commit the current transaction if no unhandled exceptions occur.</span></span>  
  
### <a name="transactionscoperequired"></a><span data-ttu-id="6d664-125">TransactionScopeRequired</span><span class="sxs-lookup"><span data-stu-id="6d664-125">TransactionScopeRequired</span></span>  
 <span data-ttu-id="6d664-126">데이터 형식: boolean</span><span class="sxs-lookup"><span data-stu-id="6d664-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="6d664-127">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="6d664-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6d664-128">작업에서 트랜잭션이 필요한지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6d664-128">Indicates whether the operation requires a transaction.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6d664-129">요구 사항</span><span class="sxs-lookup"><span data-stu-id="6d664-129">Requirements</span></span>  
  
|<span data-ttu-id="6d664-130">MOF</span><span class="sxs-lookup"><span data-stu-id="6d664-130">MOF</span></span>|<span data-ttu-id="6d664-131">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d664-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="6d664-132">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="6d664-132">Namespace</span></span>|<span data-ttu-id="6d664-133">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d664-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6d664-134">참고자료</span><span class="sxs-lookup"><span data-stu-id="6d664-134">See also</span></span>
- <xref:System.ServiceModel.OperationBehaviorAttribute>
