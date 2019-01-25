---
title: PrintForm 구성 요소 (Visual Basic)를 참조 하는 응용 프로그램 배포
ms.date: 07/20/2015
helpviewer_keywords:
- PrintForm component [Visual Basic], deploying
ms.assetid: b595ea44-a712-4625-a761-190c64f59bbe
ms.openlocfilehash: 78d332c88b45fa9b1204d9d5352a6027409254e2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54562429"
---
# <a name="deploying-applications-that-reference-the-printform-component-visual-basic"></a><span data-ttu-id="6b73f-102">PrintForm 구성 요소 (Visual Basic)를 참조 하는 응용 프로그램 배포</span><span class="sxs-lookup"><span data-stu-id="6b73f-102">Deploying applications that reference the PrintForm component (Visual Basic)</span></span>
<span data-ttu-id="6b73f-103"><xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> 구성 요소를 참조하는 응용 프로그램을 배포하려면 대상 컴퓨터에 구성 요소를 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b73f-103">If you want to deploy an application that references the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component, the component must be installed on the destination computer.</span></span>  
  
 <span data-ttu-id="6b73f-104">PowerPack 컨트롤은 Visual Studio에 더 포함되지 않지만 [다운로드 센터](https://www.microsoft.com/en-us/download/details.aspx?id=25169)에서 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b73f-104">The PowerPack controls are no longer included in Visual Studio, but you can download them from the [Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=25169).</span></span>  
  
## <a name="installing-the-printform-as-a-prerequisite"></a><span data-ttu-id="6b73f-105">PrintForm을 필수 조건으로 설치</span><span class="sxs-lookup"><span data-stu-id="6b73f-105">Installing the PrintForm as a prerequisite</span></span>  
 <span data-ttu-id="6b73f-106">애플리케이션을 성공적으로 배포하려면 애플리케이션이 참조하는 모든 구성 요소도 배포해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b73f-106">To successfully deploy an application, you must also deploy all components that are referenced by the application.</span></span> <span data-ttu-id="6b73f-107">필수 조건 구성 요소를 설치하는 프로세스를 *부트스트래핑*이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b73f-107">The process of installing prerequisite components is known as *bootstrapping*.</span></span>  
  
 <span data-ttu-id="6b73f-108">경우는 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> 구성 요소가 개발 컴퓨터에 설치 되어, Microsoft Visual Basic Power Packs 부트스트래퍼 패키지가 Visual Studio 부트스트래퍼 디렉터리에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b73f-108">When the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component is installed on your development computer, a Microsoft Visual Basic Power Packs bootstrapper package is added to the Visual Studio bootstrapper directory.</span></span> <span data-ttu-id="6b73f-109">이 패키지는 [!INCLUDE[ndptecclick](~/includes/ndptecclick-md.md)] 또는 Windows Installer 배포에 대한 필수 조건을 추가하는 절차를 수행할 때 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b73f-109">This package is then available when you follow the procedures for adding prerequisites for either [!INCLUDE[ndptecclick](~/includes/ndptecclick-md.md)] or Windows Installer deployment.</span></span>  
  
 <span data-ttu-id="6b73f-110">기본적으로 부트스트랩된 구성 요소는 설치 패키지와 같은 위치에서 배포됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b73f-110">By default, bootstrapped components are deployed from the same location as the installation package.</span></span> <span data-ttu-id="6b73f-111">또는 사용자가 필요한 경우 다운로드할 수 있는 URL 또는 파일 공유 위치에서 구성 요소를 배포하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b73f-111">Alternatively, you can choose to deploy the components from a URL or file share location from which users can download them as necessary.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6b73f-112">부트스트랩된 구성 요소를 설치하려면 사용자는 컴퓨터에서 관리 권한이나 비슷한 사용자 권한이 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b73f-112">To install bootstrapped components, the user might need administrative or similar user permissions on the computer.</span></span> <span data-ttu-id="6b73f-113">[!INCLUDE[ndptecclick](~/includes/ndptecclick-md.md)] 응용 프로그램의 경우 이는 응용 프로그램에서 지정된 보안 수준과 관계없이 응용 프로그램을 설치할 관리 권한이 사용자에게 필요함을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="6b73f-113">For [!INCLUDE[ndptecclick](~/includes/ndptecclick-md.md)] applications, this means that the user will need administrative permissions to install the application, regardless of the security level specified by the application.</span></span> <span data-ttu-id="6b73f-114">애플리케이션이 설치되고 나면 사용자는 관리 권한 없이 애플리케이션을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b73f-114">After the application is installed, the user can run the application without administrative permissions.</span></span>  
  
 <span data-ttu-id="6b73f-115">설치하는 동안 대상 컴퓨터에 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> 구성 요소가 없을 경우 해당 구성 요소를 설치할지 묻는 메시지가 사용자에게 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b73f-115">During installation, users will be prompted to install the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component if it is not present on the destination computer.</span></span>  
  
 <span data-ttu-id="6b73f-116">부트스트래핑 대신 Microsoft Systems Management Server와 같은 전자 소프트웨어 배포 시스템을 사용하여 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> 구성 요소를 미리 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b73f-116">As an alternative to bootstrapping, you can pre-deploy the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> component by using an electronic software distribution system like Microsoft Systems Management Server.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6b73f-117">참고자료</span><span class="sxs-lookup"><span data-stu-id="6b73f-117">See also</span></span>
- [<span data-ttu-id="6b73f-118">방법: ClickOnce 애플리케이션의 필수 구성 요소 설치</span><span class="sxs-lookup"><span data-stu-id="6b73f-118">How to: Install Prerequisites with a ClickOnce Application</span></span>](/visualstudio/deployment/how-to-install-prerequisites-with-a-clickonce-application)
- [<span data-ttu-id="6b73f-119">PrintForm 구성 요소</span><span class="sxs-lookup"><span data-stu-id="6b73f-119">PrintForm Component</span></span>](../../../visual-basic/developing-apps/printing/printform-component.md)
