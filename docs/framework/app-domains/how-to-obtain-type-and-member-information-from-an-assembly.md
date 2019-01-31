---
title: '방법: 어셈블리에서 형식 및 멤버 정보 가져오기'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- obtaining assembly information
- assemblies [.NET Framework], obtaining information from
ms.assetid: 348ae651-ccda-4f13-8eda-19e8337e9438
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ef3fbb7af3097a67cb39f0c3b2ee294b86f0600e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54701601"
---
# <a name="how-to-obtain-type-and-member-information-from-an-assembly"></a><span data-ttu-id="2bc5c-102">방법: 어셈블리에서 형식 및 멤버 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="2bc5c-102">How to: Obtain Type and Member Information from an Assembly</span></span>
<span data-ttu-id="2bc5c-103"><xref:System.Reflection> 네임스페이스에는 어셈블리에서 정보를 가져오는 다양한 메서드가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bc5c-103">The <xref:System.Reflection> namespace contains many methods for obtaining information from an assembly.</span></span> <span data-ttu-id="2bc5c-104">이 섹션에서는 이러한 메서드 중 하나를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2bc5c-104">This section demonstrates one of these methods.</span></span> <span data-ttu-id="2bc5c-105">자세한 내용은 [리플렉션 개요](../../../docs/framework/reflection-and-codedom/reflection.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2bc5c-105">For additional information, see [Reflection Overview](../../../docs/framework/reflection-and-codedom/reflection.md).</span></span>  
  
 <span data-ttu-id="2bc5c-106">다음 예제에서는 어셈블리에서 형식 및 멤버 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2bc5c-106">The following example obtains type and member information from an assembly.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2bc5c-107">예제</span><span class="sxs-lookup"><span data-stu-id="2bc5c-107">Example</span></span>  
 [!code-cpp[Conceptual.Types.ViewInfo#8](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.types.viewinfo/cpp/source6.cpp#8)]
 [!code-csharp[Conceptual.Types.ViewInfo#8](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.types.viewinfo/cs/source6.cs#8)]
 [!code-vb[Conceptual.Types.ViewInfo#8](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.types.viewinfo/vb/source6.vb#8)]  
  
## <a name="see-also"></a><span data-ttu-id="2bc5c-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2bc5c-108">See also</span></span>
- [<span data-ttu-id="2bc5c-109">애플리케이션 도메인으로 프로그래밍</span><span class="sxs-lookup"><span data-stu-id="2bc5c-109">Programming with Application Domains</span></span>](./application-domains.md#programming-with-application-domains)
- [<span data-ttu-id="2bc5c-110">리플렉션</span><span class="sxs-lookup"><span data-stu-id="2bc5c-110">Reflection</span></span>](../../../docs/framework/reflection-and-codedom/reflection.md)
- [<span data-ttu-id="2bc5c-111">애플리케이션 도메인 사용</span><span class="sxs-lookup"><span data-stu-id="2bc5c-111">Using Application Domains</span></span>](../../../docs/framework/app-domains/use.md)
