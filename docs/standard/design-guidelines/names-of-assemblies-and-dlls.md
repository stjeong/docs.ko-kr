---
title: 어셈블리 및 DLL의 이름
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- names [.NET Framework], DLLs
- names [.NET Framework], assemblies
- assemblies [.NET Framework], names
- DLLs, names
ms.assetid: e800b610-31b4-4949-9c14-cb60e9f254be
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 97bd152cff53fb1c2edb107b6d6b34bd91ca1c49
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/11/2018
ms.locfileid: "44366949"
---
# <a name="names-of-assemblies-and-dlls"></a><span data-ttu-id="fa13a-102">어셈블리 및 DLL의 이름</span><span class="sxs-lookup"><span data-stu-id="fa13a-102">Names of Assemblies and DLLs</span></span>
<span data-ttu-id="fa13a-103">어셈블리는 단위 배포 및 관리 코드 프로그램에 대 한 id입니다.</span><span class="sxs-lookup"><span data-stu-id="fa13a-103">An assembly is the unit of deployment and identity for managed code programs.</span></span> <span data-ttu-id="fa13a-104">어셈블리는 하나 이상의 파일에 걸쳐 수 있지만 일반적으로 어셈블리 일대일로 매핑되는 DLL입니다.</span><span class="sxs-lookup"><span data-stu-id="fa13a-104">Although assemblies can span one or more files, typically an assembly maps one-to-one with a DLL.</span></span> <span data-ttu-id="fa13a-105">따라서 다음 어셈블리 명명 규칙에 매핑할 수 있는 유일한 DLL 명명 규칙을 설명이 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa13a-105">Therefore, this section describes only DLL naming conventions, which then can be mapped to assembly naming conventions.</span></span>  
  
 <span data-ttu-id="fa13a-106">**✓ DO** 대량의 System.Data 등의 기능을 제안 하는 Dll 어셈블리의 이름을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa13a-106">**✓ DO** choose names for your assembly DLLs that suggest large chunks of functionality, such as System.Data.</span></span>  
  
 <span data-ttu-id="fa13a-107">어셈블리 및 DLL 이름을 네임 스페이스 이름에 해당 없지만 어셈블리 이름을 지정할 때 네임 스페이스의 이름을 따르는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fa13a-107">Assembly and DLL names don’t have to correspond to namespace names, but it is reasonable to follow the namespace name when naming assemblies.</span></span> <span data-ttu-id="fa13a-108">경험에의 하면 어셈블리에 포함 된 네임 스페이스의 공통 접두사를 기준으로 DLL 이름을 지정 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fa13a-108">A good rule of thumb is to name the DLL based on the common prefix of the namespaces contained in the assembly.</span></span> <span data-ttu-id="fa13a-109">예를 들어 두 개의 네임 스페이스를 사용 하 여 어셈블리 `MyCompany.MyTechnology.FirstFeature` 하 고 `MyCompany.MyTechnology.SecondFeature`를 호출할 수 `MyCompany.MyTechnology.dll`입니다.</span><span class="sxs-lookup"><span data-stu-id="fa13a-109">For example, an assembly with two namespaces, `MyCompany.MyTechnology.FirstFeature` and `MyCompany.MyTechnology.SecondFeature`, could be called `MyCompany.MyTechnology.dll`.</span></span>  
  
 <span data-ttu-id="fa13a-110">**✓ CONSIDER** 다음 패턴에 따라 Dll 이름 지정:</span><span class="sxs-lookup"><span data-stu-id="fa13a-110">**✓ CONSIDER** naming DLLs according to the following pattern:</span></span>  
  
 `<Company>.<Component>.dll`  
  
 <span data-ttu-id="fa13a-111">여기서 `<Component>` -점으로 구분 된 하나 이상의 절을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa13a-111">where `<Component>` contains one or more dot-separated clauses.</span></span> <span data-ttu-id="fa13a-112">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="fa13a-112">For example:</span></span>  
  
 <span data-ttu-id="fa13a-113">`Litware.Controls.dll`.</span><span class="sxs-lookup"><span data-stu-id="fa13a-113">`Litware.Controls.dll`.</span></span>  
  
 <span data-ttu-id="fa13a-114">*Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*</span><span class="sxs-lookup"><span data-stu-id="fa13a-114">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="fa13a-115">*Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span><span class="sxs-lookup"><span data-stu-id="fa13a-115">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa13a-116">참고자료</span><span class="sxs-lookup"><span data-stu-id="fa13a-116">See also</span></span>

- [<span data-ttu-id="fa13a-117">프레임워크 디자인 지침</span><span class="sxs-lookup"><span data-stu-id="fa13a-117">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="fa13a-118">명명 지침</span><span class="sxs-lookup"><span data-stu-id="fa13a-118">Naming Guidelines</span></span>](../../../docs/standard/design-guidelines/naming-guidelines.md)
