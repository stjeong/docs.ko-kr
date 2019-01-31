---
title: <binding>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 666183d6-4d1f-45c7-ac64-bdf93ee8f36f
ms.openlocfilehash: fb51eb1962603439b89a203eb668dfb543049170
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271475"
---
# <a name="binding"></a><span data-ttu-id="d5fd4-101">\<binding></span><span class="sxs-lookup"><span data-stu-id="d5fd4-101">\<binding></span></span>
<span data-ttu-id="d5fd4-102">`binding` 요소를 사용하여 WCF(Windows Communication Foundation)에서 제공하는 미리 정의된 다양한 바인딩 형식을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5fd4-102">You can use the `binding` element to configure different types of predefined bindings provided by Windows Communication Foundation (WCF).</span></span>  
  
## <a name="system-provided-binding"></a><span data-ttu-id="d5fd4-103">시스템 제공 바인딩</span><span class="sxs-lookup"><span data-stu-id="d5fd4-103">System-Provided Binding</span></span>  
 <span data-ttu-id="d5fd4-104">시스템 제공 바인딩은 WCF 메시지 스택의 복잡성을 숨깁니다.</span><span class="sxs-lookup"><span data-stu-id="d5fd4-104">System-provided bindings hide the complexity of the WCF messaging stack.</span></span> <span data-ttu-id="d5fd4-105">시스템 제공 바인딩을 사용하는 응용 프로그램은 스택을 완전히 제어할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d5fd4-105">Applications using system-provided bindings do not require full control over the stack.</span></span> <span data-ttu-id="d5fd4-106">각 시스템 제공 바인딩에는 바인딩이 처리하는 사용 시나리오에 가장 적합한 특성이 노출됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5fd4-106">The attributes exposed on each system-provided binding are the ones most appropriate for the usage scenario the binding addresses.</span></span>  
  
 <span data-ttu-id="d5fd4-107">각 시스템 제공 바인딩의 구성 섹션은 바인딩 구성에 사용되는 일부 구성을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5fd4-107">The configuration section for each system-provided binding can define several configurations used to configure the binding.</span></span> <span data-ttu-id="d5fd4-108">각 구성은 고유한 이름으로 식별됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5fd4-108">Each configuration is identified by a unique name.</span></span>  
  
 <span data-ttu-id="d5fd4-109">시스템 제공 바인딩에는 요소나 특성을 추가할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d5fd4-109">It is not possible to add elements or attributes to a system-provided binding.</span></span> <span data-ttu-id="d5fd4-110">이렇게 하려면 이 항목의 "사용자 지정 바인딩" 섹션에 설명된 것처럼 사용자 지정 바인딩을 구현해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5fd4-110">To do so, you should implement a custom binding as described in the "Custom Binding" section of this topic.</span></span> <span data-ttu-id="d5fd4-111">시스템 제공 바인딩과 완전히 같으며 사용자 응용 프로그램이 제어하려는 몇 가지 설정을 추가로 제공하는 사용자 지정 바인딩을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5fd4-111">It is possible to define a custom binding that mimics a system-provided binding perfectly and adds a few settings the user application wants to have control over.</span></span>  
  
## <a name="custom-binding"></a><span data-ttu-id="d5fd4-112">사용자 지정 바인딩</span><span class="sxs-lookup"><span data-stu-id="d5fd4-112">Custom Binding</span></span>  
 <span data-ttu-id="d5fd4-113">사용자 지정 바인딩은 WCF 메시징 스택에 대한 모든 권한을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d5fd4-113">Custom bindings provide full control over the WCF messaging stack.</span></span> <span data-ttu-id="d5fd4-114">개별 바인딩에서는 스택에 나타나는 순서대로 스택 요소의 구성 요소를 지정함으로써 메시지 스택을 정의하며,</span><span class="sxs-lookup"><span data-stu-id="d5fd4-114">An individual binding defines the message stack by specifying the configuration elements for the stack elements in the order they appear on the stack.</span></span> <span data-ttu-id="d5fd4-115">각 요소는 스택의 한 요소를 정의하고 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="d5fd4-115">Each element defines and configures the one element of the stack.</span></span> <span data-ttu-id="d5fd4-116">각 사용자 지정 바인딩에는 `transport` 요소가 하나만 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5fd4-116">There must be one and only one `transport` element in each custom binding.</span></span> <span data-ttu-id="d5fd4-117">이 요소가 없으면 메시징 스택이 완전하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5fd4-117">Without this element, the messaging stack is incomplete.</span></span>  
  
 <span data-ttu-id="d5fd4-118">스택에서 요소가 나타나는 순서는 작업이 메시지에 적용되는 순서이므로 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="d5fd4-118">The order in which elements appear in the stack matters, because it is the order in which operations are applied to the message.</span></span> <span data-ttu-id="d5fd4-119">다음과 같은 스택 요소 순서를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d5fd4-119">The recommended order of stack elements is the following:</span></span>  
  
1.  <span data-ttu-id="d5fd4-120">Transactions(선택적)</span><span class="sxs-lookup"><span data-stu-id="d5fd4-120">Transactions (optional)</span></span>  
  
2.  <span data-ttu-id="d5fd4-121">Reliable Messaging(선택적)</span><span class="sxs-lookup"><span data-stu-id="d5fd4-121">Reliable Messaging (optional)</span></span>  
  
3.  <span data-ttu-id="d5fd4-122">Security(선택적)</span><span class="sxs-lookup"><span data-stu-id="d5fd4-122">Security (optional)</span></span>  
  
4.  <span data-ttu-id="d5fd4-123">인코더</span><span class="sxs-lookup"><span data-stu-id="d5fd4-123">Encoder</span></span>  
  
5.  <span data-ttu-id="d5fd4-124">전송</span><span class="sxs-lookup"><span data-stu-id="d5fd4-124">Transport</span></span>  
  
 <span data-ttu-id="d5fd4-125">사용자 지정 바인딩은 `name` 특성으로 식별됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5fd4-125">Custom bindings are identified by their `name` attribute.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d5fd4-126">참고자료</span><span class="sxs-lookup"><span data-stu-id="d5fd4-126">See also</span></span>
- <xref:System.ServiceModel.Configuration.BindingsSection>
- <xref:System.ServiceModel.Channels.Binding>
- <xref:System.ServiceModel.Channels.BindingElement>
- [<span data-ttu-id="d5fd4-127">바인딩</span><span class="sxs-lookup"><span data-stu-id="d5fd4-127">Bindings</span></span>](../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="d5fd4-128">사용자 지정 바인딩</span><span class="sxs-lookup"><span data-stu-id="d5fd4-128">Custom Bindings</span></span>](../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="d5fd4-129">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="d5fd4-129">\<customBinding></span></span>](../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
