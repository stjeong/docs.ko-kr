---
title: 리소스 이름 지정
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- names [.NET Framework], localized resources
- localization, naming guidelines
- resource names
- global applications, naming guidelines
- international applications, naming guidelines
ms.assetid: 8b0e97f3-7877-44fd-bc76-e05d36d5d79c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a5b53fc383e6fc9a5f056bab4eabde9979cd734b
ms.sourcegitcommit: 700b9003ea6bdd83a53458bbc436c9b5778344f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/03/2018
ms.locfileid: "48260682"
---
# <a name="naming-resources"></a><span data-ttu-id="cd48d-102">리소스 이름 지정</span><span class="sxs-lookup"><span data-stu-id="cd48d-102">Naming Resources</span></span>
<span data-ttu-id="cd48d-103">지역화할 수 있는 리소스 속성 처럼 특정 개체를 통해 참조할 수, 있으므로 리소스에 대 한 명명 지침 속성 지침 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="cd48d-103">Because localizable resources can be referenced via certain objects as if they were properties, the naming guidelines for resources are similar to property guidelines.</span></span>  
  
 <span data-ttu-id="cd48d-104">**✓ DO** PascalCasing 리소스 키에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd48d-104">**✓ DO** use PascalCasing in resource keys.</span></span>  
  
 <span data-ttu-id="cd48d-105">**✓ DO** 설명 하는 대신 짧은 식별자를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd48d-105">**✓ DO** provide descriptive rather than short identifiers.</span></span>  
  
 <span data-ttu-id="cd48d-106">**X DO NOT** 주 CLR 언어의 언어 관련 키워드를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd48d-106">**X DO NOT** use language-specific keywords of the main CLR languages.</span></span>  
  
 <span data-ttu-id="cd48d-107">**✓ DO** 영숫자 문자와 밑줄 리소스 이름 지정 시에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd48d-107">**✓ DO** use only alphanumeric characters and underscores in naming resources.</span></span>  
  
 <span data-ttu-id="cd48d-108">**✓ DO** 예외 메시지 리소스에 대 한 다음과 같은 명명 규칙을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd48d-108">**✓ DO** use the following naming convention for exception message resources.</span></span>  
  
 <span data-ttu-id="cd48d-109">예외 형식 이름 및 예외 짧은 식별자 리소스 식별자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd48d-109">The resource identifier should be the exception type name plus a short identifier of the exception:</span></span>  
  
 `ArgumentExceptionIllegalCharacters`  
 `ArgumentExceptionInvalidName`  
 `ArgumentExceptionFileNameIsMalformed`  
  
 <span data-ttu-id="cd48d-110">*Portions © 2005, 2009 Microsoft Corporation. 모든 권리 보유.*</span><span class="sxs-lookup"><span data-stu-id="cd48d-110">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="cd48d-111">*Pearson Education, Inc의 동의로 재인쇄. 출처: [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) 작성자: Krzysztof Cwalina 및 Brad Abrams, 출판 정보: Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span><span class="sxs-lookup"><span data-stu-id="cd48d-111">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cd48d-112">참고자료</span><span class="sxs-lookup"><span data-stu-id="cd48d-112">See also</span></span>

- [<span data-ttu-id="cd48d-113">프레임워크 디자인 지침</span><span class="sxs-lookup"><span data-stu-id="cd48d-113">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="cd48d-114">명명 지침</span><span class="sxs-lookup"><span data-stu-id="cd48d-114">Naming Guidelines</span></span>](../../../docs/standard/design-guidelines/naming-guidelines.md)
