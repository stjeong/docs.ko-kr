---
title: SecurityBindingElement
ms.date: 03/30/2017
ms.assetid: ef93b6e6-3524-48a8-94d3-c8837f1872f9
author: BrucePerlerMS
ms.openlocfilehash: 19c65b3028ad63b8a78205d00f44cc32322648d5
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47069976"
---
# <a name="securitybindingelement"></a><span data-ttu-id="c99c7-102">SecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="c99c7-102">SecurityBindingElement</span></span>
<span data-ttu-id="c99c7-103">SecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="c99c7-103">SecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c99c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="c99c7-104">Syntax</span></span>  
  
```  
class SecurityBindingElement : BindingElement  
{  
  string DefaultAlgorithmSuite;  
  boolean IncludeTimestamp;  
  string KeyEntropyMode;  
  LocalServiceSecuritySettings LocalServiceSecuritySettings;  
  string MessageSecurityVersion;  
  string SecurityHeaderLayout;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="c99c7-105">메서드</span><span class="sxs-lookup"><span data-stu-id="c99c7-105">Methods</span></span>  
 <span data-ttu-id="c99c7-106">SecurityBindingElement 클래스는 메서드를 정의하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c99c7-106">The SecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="c99c7-107">속성</span><span class="sxs-lookup"><span data-stu-id="c99c7-107">Properties</span></span>  
 <span data-ttu-id="c99c7-108">SecurityBindingElement 클래스에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c99c7-108">The SecurityBindingElement class has the following properties:</span></span>  
  
### <a name="defaultalgorithmsuite"></a><span data-ttu-id="c99c7-109">DefaultAlgorithmSuite</span><span class="sxs-lookup"><span data-stu-id="c99c7-109">DefaultAlgorithmSuite</span></span>  
 <span data-ttu-id="c99c7-110">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="c99c7-110">Data type: string</span></span>  
  
 <span data-ttu-id="c99c7-111">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="c99c7-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c99c7-112">바인딩과 함께 사용할 알고리즘을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c99c7-112">Specifies the algorithms to use with the binding.</span></span>  
  
### <a name="includetimestamp"></a><span data-ttu-id="c99c7-113">IncludeTimestamp</span><span class="sxs-lookup"><span data-stu-id="c99c7-113">IncludeTimestamp</span></span>  
 <span data-ttu-id="c99c7-114">데이터 형식: boolean</span><span class="sxs-lookup"><span data-stu-id="c99c7-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="c99c7-115">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="c99c7-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c99c7-116">각 메시지에 타임스탬프가 포함되는지 여부를 지정하는 부울 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c99c7-116">A Boolean value that specifies whether each message contains a timestamp.</span></span>  
  
### <a name="keyentropymode"></a><span data-ttu-id="c99c7-117">KeyEntropyMode</span><span class="sxs-lookup"><span data-stu-id="c99c7-117">KeyEntropyMode</span></span>  
 <span data-ttu-id="c99c7-118">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="c99c7-118">Data type: string</span></span>  
  
 <span data-ttu-id="c99c7-119">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="c99c7-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c99c7-120">키를 만드는 데 사용되는 엔트로피의 소스입니다.</span><span class="sxs-lookup"><span data-stu-id="c99c7-120">The source of entropy used to create keys.</span></span>  
  
### <a name="localservicesecuritysettings"></a><span data-ttu-id="c99c7-121">LocalServiceSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="c99c7-121">LocalServiceSecuritySettings</span></span>  
 <span data-ttu-id="c99c7-122">데이터 형식: LocalServiceSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="c99c7-122">Data type: LocalServiceSecuritySettings</span></span>  
  
 <span data-ttu-id="c99c7-123">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="c99c7-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c99c7-124">로컬 서비스에 대한 바인딩 특정 보안 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="c99c7-124">The binding specific security properties for the local service.</span></span>  
  
### <a name="messagesecurityversion"></a><span data-ttu-id="c99c7-125">MessageSecurityVersion</span><span class="sxs-lookup"><span data-stu-id="c99c7-125">MessageSecurityVersion</span></span>  
 <span data-ttu-id="c99c7-126">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="c99c7-126">Data type: string</span></span>  
  
 <span data-ttu-id="c99c7-127">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="c99c7-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c99c7-128">메시지 보안에 사용된 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="c99c7-128">The version used for message security.</span></span>  
  
### <a name="securityheaderlayout"></a><span data-ttu-id="c99c7-129">SecurityHeaderLayout</span><span class="sxs-lookup"><span data-stu-id="c99c7-129">SecurityHeaderLayout</span></span>  
 <span data-ttu-id="c99c7-130">데이터 형식: string</span><span class="sxs-lookup"><span data-stu-id="c99c7-130">Data type: string</span></span>  
  
 <span data-ttu-id="c99c7-131">액세스 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="c99c7-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c99c7-132">이 바인딩의 보안 헤더에 있는 요소의 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="c99c7-132">The order of elements in the security header for this binding.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c99c7-133">요구 사항</span><span class="sxs-lookup"><span data-stu-id="c99c7-133">Requirements</span></span>  
  
|<span data-ttu-id="c99c7-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c99c7-134">MOF</span></span>|<span data-ttu-id="c99c7-135">Servicemodel.mof에 선언되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c99c7-135">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="c99c7-136">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="c99c7-136">Namespace</span></span>|<span data-ttu-id="c99c7-137">root\ServiceModel에 정의되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c99c7-137">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c99c7-138">참고 항목</span><span class="sxs-lookup"><span data-stu-id="c99c7-138">See Also</span></span>  
 <xref:System.ServiceModel.Channels.SecurityBindingElement>
