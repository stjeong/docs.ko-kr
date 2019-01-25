---
title: Operation 클래스
ms.date: 03/30/2017
ms.assetid: b19d1496-ef06-4d0c-b2ae-e728ec00cca0
ms.openlocfilehash: 9453d67854bb8439891661b07e3ab3aa373e23eb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54668303"
---
# <a name="operation-class"></a><span data-ttu-id="a7eb9-102">Operation 클래스</span><span class="sxs-lookup"><span data-stu-id="a7eb9-102">Operation class</span></span>
<span data-ttu-id="a7eb9-103">작업</span><span class="sxs-lookup"><span data-stu-id="a7eb9-103">Operation</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a7eb9-104">구문</span><span class="sxs-lookup"><span data-stu-id="a7eb9-104">Syntax</span></span>  
  
```csharp
class Operation  
{  
  string Action;  
  boolean AsyncPattern;  
  Behavior Behaviors[];  
  boolean IsCallback;  
  boolean IsInitiating;  
  boolean IsOneWay;  
  boolean IsTerminating;  
  string MethodSignature;  
  string Name;  
  string ParameterTypes[];  
  string ReplyAction;  
  string ReturnType;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="a7eb9-105">메서드</span><span class="sxs-lookup"><span data-stu-id="a7eb9-105">Methods</span></span>  
 <span data-ttu-id="a7eb9-106">Operation 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7eb9-106">The Operation class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="a7eb9-107">속성</span><span class="sxs-lookup"><span data-stu-id="a7eb9-107">Properties</span></span>  
 <span data-ttu-id="a7eb9-108">Operation 클래스에는 다음 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7eb9-108">The Operation class has the following properties:</span></span>  
  
### <a name="action"></a><span data-ttu-id="a7eb9-109">작업</span><span class="sxs-lookup"><span data-stu-id="a7eb9-109">Action</span></span>  
 <span data-ttu-id="a7eb9-110">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="a7eb9-110">Data type: string</span></span>  
  
 <span data-ttu-id="a7eb9-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a7eb9-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a7eb9-112">요청 메시지의 WS-Addressing 동작입니다.</span><span class="sxs-lookup"><span data-stu-id="a7eb9-112">The WS-Addressing action of the request message.</span></span>  
  
### <a name="asyncpattern"></a><span data-ttu-id="a7eb9-113">AsyncPattern</span><span class="sxs-lookup"><span data-stu-id="a7eb9-113">AsyncPattern</span></span>  
 <span data-ttu-id="a7eb9-114">데이터 형식: boolean</span><span class="sxs-lookup"><span data-stu-id="a7eb9-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="a7eb9-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a7eb9-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a7eb9-116">작업을 사용 하 여 비동기적으로 구현 됨을 나타냅니다는 `Begin`[꺽쇠괄호 열기/닫기] 및 `End`서비스 계약에 [꺾쇠 괄호 열기/닫기] 메서드 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="a7eb9-116">Indicates that an operation is implemented asynchronously using a `Begin`[open/close angle brackets] and `End`[open/close angle brackets] method pair in a service contract.</span></span>  
  
### <a name="behaviors"></a><span data-ttu-id="a7eb9-117">동작</span><span class="sxs-lookup"><span data-stu-id="a7eb9-117">Behaviors</span></span>  
 <span data-ttu-id="a7eb9-118">데이터 형식: 동작 배열</span><span class="sxs-lookup"><span data-stu-id="a7eb9-118">Data type: Behavior array</span></span>  
  
 <span data-ttu-id="a7eb9-119">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a7eb9-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a7eb9-120">이 작업과 연관된 동작입니다.</span><span class="sxs-lookup"><span data-stu-id="a7eb9-120">The behaviors associated with this operation.</span></span>  
  
### <a name="iscallback"></a><span data-ttu-id="a7eb9-121">IsCallback</span><span class="sxs-lookup"><span data-stu-id="a7eb9-121">IsCallback</span></span>  
 <span data-ttu-id="a7eb9-122">데이터 형식: boolean</span><span class="sxs-lookup"><span data-stu-id="a7eb9-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="a7eb9-123">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a7eb9-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a7eb9-124">작업이 콜백 작업인 경우 true입니다.</span><span class="sxs-lookup"><span data-stu-id="a7eb9-124">True when the operation is a callback operation.</span></span>  
  
### <a name="isinitiating"></a><span data-ttu-id="a7eb9-125">IsInitiating</span><span class="sxs-lookup"><span data-stu-id="a7eb9-125">IsInitiating</span></span>  
 <span data-ttu-id="a7eb9-126">데이터 형식: boolean</span><span class="sxs-lookup"><span data-stu-id="a7eb9-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="a7eb9-127">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a7eb9-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a7eb9-128">서버에서 세션을 시작할 수 있는 작업을 메서드에서 구현하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a7eb9-128">Indicates whether the method implements an operation that can initiate a session on the server.</span></span>  
  
### <a name="isoneway"></a><span data-ttu-id="a7eb9-129">IsOneWay</span><span class="sxs-lookup"><span data-stu-id="a7eb9-129">IsOneWay</span></span>  
 <span data-ttu-id="a7eb9-130">데이터 형식: boolean</span><span class="sxs-lookup"><span data-stu-id="a7eb9-130">Data type: boolean</span></span>  
  
 <span data-ttu-id="a7eb9-131">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a7eb9-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a7eb9-132">작업에서 회신 메시지를 반환하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a7eb9-132">Indicates whether an operation returns a reply message.</span></span>  
  
### <a name="isterminating"></a><span data-ttu-id="a7eb9-133">IsTerminating</span><span class="sxs-lookup"><span data-stu-id="a7eb9-133">IsTerminating</span></span>  
 <span data-ttu-id="a7eb9-134">데이터 형식: boolean</span><span class="sxs-lookup"><span data-stu-id="a7eb9-134">Data type: boolean</span></span>  
  
 <span data-ttu-id="a7eb9-135">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a7eb9-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a7eb9-136">작업에서 회신 메시지를 반환하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a7eb9-136">Indicates whether an operation returns a reply message.</span></span>  
  
### <a name="methodsignature"></a><span data-ttu-id="a7eb9-137">MethodSignature</span><span class="sxs-lookup"><span data-stu-id="a7eb9-137">MethodSignature</span></span>  
 <span data-ttu-id="a7eb9-138">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="a7eb9-138">Data type: string</span></span>  
  
 <span data-ttu-id="a7eb9-139">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a7eb9-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a7eb9-140">작업의 메서드 서명입니다.</span><span class="sxs-lookup"><span data-stu-id="a7eb9-140">The method signature of the operation.</span></span>  
  
### <a name="name"></a><span data-ttu-id="a7eb9-141">이름</span><span class="sxs-lookup"><span data-stu-id="a7eb9-141">Name</span></span>  
 <span data-ttu-id="a7eb9-142">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="a7eb9-142">Data type: string</span></span>  
  
 <span data-ttu-id="a7eb9-143">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a7eb9-143">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a7eb9-144">작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7eb9-144">The name of the operation.</span></span>  
  
### <a name="parametertypes"></a><span data-ttu-id="a7eb9-145">ParameterTypes</span><span class="sxs-lookup"><span data-stu-id="a7eb9-145">ParameterTypes</span></span>  
 <span data-ttu-id="a7eb9-146">데이터 형식: string array</span><span class="sxs-lookup"><span data-stu-id="a7eb9-146">Data type: string array</span></span>  
  
 <span data-ttu-id="a7eb9-147">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a7eb9-147">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a7eb9-148">작업의 매개 변수 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a7eb9-148">The types of the parameters of the operation.</span></span>  
  
### <a name="replyaction"></a><span data-ttu-id="a7eb9-149">ReplyAction</span><span class="sxs-lookup"><span data-stu-id="a7eb9-149">ReplyAction</span></span>  
 <span data-ttu-id="a7eb9-150">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="a7eb9-150">Data type: string</span></span>  
  
 <span data-ttu-id="a7eb9-151">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a7eb9-151">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a7eb9-152">작업의 회신 메시지에 대한 SOAP 동작 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a7eb9-152">The value of the SOAP action for the reply message of the operation.</span></span>  
  
### <a name="returntype"></a><span data-ttu-id="a7eb9-153">ReturnType</span><span class="sxs-lookup"><span data-stu-id="a7eb9-153">ReturnType</span></span>  
 <span data-ttu-id="a7eb9-154">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="a7eb9-154">Data type: string</span></span>  
  
 <span data-ttu-id="a7eb9-155">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a7eb9-155">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a7eb9-156">작업의 반환 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a7eb9-156">The return type of the operation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a7eb9-157">요구 사항</span><span class="sxs-lookup"><span data-stu-id="a7eb9-157">Requirements</span></span>  
  
|<span data-ttu-id="a7eb9-158">MOF</span><span class="sxs-lookup"><span data-stu-id="a7eb9-158">MOF</span></span>|<span data-ttu-id="a7eb9-159">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7eb9-159">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="a7eb9-160">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="a7eb9-160">Namespace</span></span>|<span data-ttu-id="a7eb9-161">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7eb9-161">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a7eb9-162">참고자료</span><span class="sxs-lookup"><span data-stu-id="a7eb9-162">See also</span></span>
- <xref:System.ServiceModel.Description.OperationDescription>
