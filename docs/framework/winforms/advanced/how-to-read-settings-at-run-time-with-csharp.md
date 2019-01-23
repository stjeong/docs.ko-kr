---
title: '방법: 사용 하 여 런타임에 설정 읽기C#'
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], reading
- application settings [Windows Forms], run time
- application settings [Windows Forms], C#
ms.assetid: dbe8bf09-5e1c-49da-9192-154033d7240b
ms.openlocfilehash: d798b40e5e337ea7652c8e82cb7fa860a87528b9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54521753"
---
# <a name="how-to-read-settings-at-run-time-with-c"></a><span data-ttu-id="4996e-102">방법: 사용 하 여 런타임에 설정 읽기C#</span><span class="sxs-lookup"><span data-stu-id="4996e-102">How To: Read Settings at Run Time With C#</span></span> #
<span data-ttu-id="4996e-103">속성 개체를 통해 런타임에 응용 프로그램 범위 및 사용자 범위 설정을 둘 다 읽을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4996e-103">You can read both Application-scoped and User-scoped settings at run time via the Properties object.</span></span> <span data-ttu-id="4996e-104">속성 개체는 Properties.Settings.Default 멤버를 통해 프로젝트에 대한 기본 설정을 모두 노출합니다.</span><span class="sxs-lookup"><span data-stu-id="4996e-104">The Properties object exposes all of the default settings for the project via the Properties.Settings.Default member.</span></span>  
  
### <a name="to-read-settings-at-run-time-with-c"></a><span data-ttu-id="4996e-105">C#을 사용하여 런타임에 설정을 읽으려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="4996e-105">To Read Settings at Run Time with C#</span></span>  
  
-   <span data-ttu-id="4996e-106">Properties.Settings.Default 멤버를 통해 적절한 설정에 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="4996e-106">Access the appropriate setting via the Properties.Settings.Default member.</span></span> <span data-ttu-id="4996e-107">다음 예제에서는 `myColor` 설정을 BackColor 속성에 할당하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4996e-107">The following example shows how to assign a setting named `myColor` to a BackColor property.</span></span> <span data-ttu-id="4996e-108">`System.Drawing.Color` 형식의 `myColor` 설정이 포함된 설정 파일을 미리 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4996e-108">It requires you to have previously created a Settings file containing a setting named `myColor` of type `System.Drawing.Color`.</span></span> <span data-ttu-id="4996e-109">설정 파일을 만드는 방법에 대 한 자세한 내용은 [방법: 디자인 타임에 새 설정 만들기](../../../../docs/framework/winforms/advanced/how-to-create-a-new-setting-at-design-time.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="4996e-109">For information about creating a Settings file, see [How To: Create a New Setting at Design Time](../../../../docs/framework/winforms/advanced/how-to-create-a-new-setting-at-design-time.md).</span></span>  
  
    ```  
    // C#  
    this.BackColor = Properties.Settings.Default.myColor;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="4996e-110">참고자료</span><span class="sxs-lookup"><span data-stu-id="4996e-110">See also</span></span>
- [<span data-ttu-id="4996e-111">응용 프로그램 설정 및 사용자 설정 사용</span><span class="sxs-lookup"><span data-stu-id="4996e-111">Using Application Settings and User Settings</span></span>](../../../../docs/framework/winforms/advanced/using-application-settings-and-user-settings.md)
- [<span data-ttu-id="4996e-112">방법: 사용 하 여 런타임에 사용자 설정 쓰기C#</span><span class="sxs-lookup"><span data-stu-id="4996e-112">How To: Write User Settings at Run Time with C#</span></span>](../../../../docs/framework/winforms/advanced/how-to-write-user-settings-at-run-time-with-csharp.md)
- [<span data-ttu-id="4996e-113">응용 프로그램 설정 개요</span><span class="sxs-lookup"><span data-stu-id="4996e-113">Application Settings Overview</span></span>](../../../../docs/framework/winforms/advanced/application-settings-overview.md)
