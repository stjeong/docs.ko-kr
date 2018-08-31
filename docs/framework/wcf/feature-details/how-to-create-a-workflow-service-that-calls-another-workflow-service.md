---
title: '방법: 다른 워크플로 서비스를 호출하는 워크플로 서비스 만들기'
ms.date: 03/30/2017
ms.assetid: 99b3ee3e-aeb7-4e6f-8321-60fe6140eb67
ms.openlocfilehash: 1b30da34f7c85cccd98b18cd32b81c83630989b2
ms.sourcegitcommit: fe02afbc39e78afd78cc6050e4a9c12a75f579f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43258360"
---
# <a name="how-to-create-a-workflow-service-that-calls-another-workflow-service"></a><span data-ttu-id="51b4f-102">방법: 다른 워크플로 서비스를 호출하는 워크플로 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="51b4f-102">How to: Create a Workflow Service That Calls Another Workflow Service</span></span>

<span data-ttu-id="51b4f-103">워크플로 서비스에서 다른 워크플로 서비스의 정보를 얻어야 하는 경우가 가끔 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-103">It is sometimes necessary for a workflow service to obtain information from another workflow service.</span></span> <span data-ttu-id="51b4f-104">이 항목에서는 워크플로 서비스 간에 호출하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-104">This topic demonstrates how to call one workflow service from another.</span></span> <span data-ttu-id="51b4f-105">이 항목에서는 두 개의 워크플로 서비스를 만듭니다. 하나는 입력 문자열의 방향을 반대로 바꾸는 메서드가 있는 서비스이고, 다른 하나는 첫 번째 서비스를 사용하는 문자열의 방향을 반대로 바꾼 후 입력 문자열을 대문자로 변환하는 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-105">In this topic, we’ll create two workflow services; one that has a method that reverses the input string, and another that converts the input string to uppercase after reversing the string that uses the first service.</span></span>

### <a name="to-create-the-reverser-workflow-service"></a><span data-ttu-id="51b4f-106">Reverser 워크플로 서비스를 만들려면</span><span class="sxs-lookup"><span data-stu-id="51b4f-106">To create the Reverser workflow service</span></span>

1.  <span data-ttu-id="51b4f-107">Visual Studio를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-107">Open Visual Studio.</span></span>

2.  <span data-ttu-id="51b4f-108">선택 **파일** > **새 프로젝트**합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-108">Select **File** > **New Project**.</span></span> <span data-ttu-id="51b4f-109">아래는 **워크플로** 에서 노드를 **설치 된 템플릿** 창 **WCF 워크플로 서비스 응용 프로그램**합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-109">Under the **Workflow** node in the **Installed Templates** pane, select **WCF Workflow Service Application**.</span></span> <span data-ttu-id="51b4f-110">솔루션의 이름을 `NestedServices` 을 클릭 한 다음 **확인**합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-110">Name the solution `NestedServices` and then click **OK**.</span></span>

3.  <span data-ttu-id="51b4f-111">아래 **서버**, 했는지 **사용 하 여 로컬 IIS 웹 서버** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-111">Under **Servers**, make sure that **Use Local IIS Web Server** is selected.</span></span> <span data-ttu-id="51b4f-112">클릭 **가상 디렉터리 만들기**합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-112">Click **Create Virtual Directory**.</span></span> <span data-ttu-id="51b4f-113">클릭 **확인** 에서 대화 상자가 나타날 가상 디렉터리를 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-113">Click **OK** in the dialog box stating that the virtual directory was successfully created.</span></span>

4.  <span data-ttu-id="51b4f-114">솔루션 탐색기에서 Service1.xamlx의 이름을 `StringReverserService.xamlx`입니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-114">In Solution Explorer, rename Service1.xamlx to `StringReverserService.xamlx`.</span></span>

5.  <span data-ttu-id="51b4f-115">에 **프로젝트 속성** 새 프로젝트 페이지를 클릭 합니다 **웹** 탭 합니다. 설정 합니다 **시작 작업** 하 **특정 페이지**, 하 고 StringReverserService.xamlx를 시작 하려면 페이지를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-115">On the **Project Properties** page for the new project, click the **Web** tab. Set the **Start Action** to **Specific Page**, and select StringReverserService.xamlx as the page to start.</span></span>

6.  <span data-ttu-id="51b4f-116">디자이너에서 StringReverserService.xamlx를 열고 기존 `ReceiveRequest` 및 `SendReply` 활동을 삭제한 다음 `ReceiveAndSendReply` 활동을 기존 시퀀스 활동으로 끌어 옵니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-116">Open StringReverserService.xamlx in the designer and delete the existing `ReceiveRequest` and `SendReply` activities, and then drag a `ReceiveAndSendReply` activity into the existing sequence activity.</span></span>

    1.  <span data-ttu-id="51b4f-117">설정 된 **OperationName** 을 reversestring으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-117">Set the **OperationName** to ReverseString.</span></span>

    2.  <span data-ttu-id="51b4f-118">설정 된 **ServiceContractName** 을 ireversestring으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-118">Set the **ServiceContractName** to IReverseString.</span></span>

    3.  <span data-ttu-id="51b4f-119">선택 된 **CanCreateInstance** 확인란 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-119">Select the **CanCreateInstance** check box.</span></span>

7.  <span data-ttu-id="51b4f-120">선택 합니다 **SequentialService** 활동과 클릭 한 다음는 **변수** 디자이너의 아래쪽에 있는 탭입니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-120">Select the **SequentialService** activity, and then click the **Variables** tab at the bottom of the designer.</span></span> <span data-ttu-id="51b4f-121">String 형식의 StringToReverse 및 ReversedStringToReturn이라는 새로운 두 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-121">Create two new variables named StringToReverse and ReversedStringToReturn of type String.</span></span>

8.  <span data-ttu-id="51b4f-122">클릭 합니다 **정의** 링크를 **수신** 활동입니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-122">Click the **Define** link in the **Receive** activity.</span></span> <span data-ttu-id="51b4f-123">클릭 합니다 **매개 변수**, 고 StringToReverse에 할당 되는 String 형식의 InputString 이라는 매개 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-123">Click the  **Parameters**, and create a parameter named InputString of type String that assigns to StringToReverse.</span></span>

9. <span data-ttu-id="51b4f-124">클릭 합니다 **정의** 링크를 **SendReplyToReceive** 활동입니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-124">Click the **Define** link in the **SendReplyToReceive** activity.</span></span> <span data-ttu-id="51b4f-125">클릭 합니다 **매개 변수**, 고 ReversedStringToReturn에 할당 된 String 형식의 ReversedString 이라는 매개 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-125">Click the **Parameters**, and create a parameter named ReversedString of type String, assigned to ReversedStringToReturn.</span></span>

10. <span data-ttu-id="51b4f-126">서비스의 논리를 구현하려면 프로젝트에 StringLibrary라는 새 클래스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-126">To implement the logic for the service, create a new class in the project called StringLibrary.</span></span>  <span data-ttu-id="51b4f-127">클래스 정의를 다음 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-127">Replace the class definition with the following code.</span></span>

    ```
    public class StringLibrary
        {
            public static String ReverseString(string StringToReverse)
            {
                char[] charArray = StringToReverse.ToCharArray();
                Array.Reverse(charArray);
                return new String(charArray);
            }
        }
    ```

11. <span data-ttu-id="51b4f-128">입력에 대해 ReverseString 메서드를 호출 하려면 끌어를 **InvokeMethod** 사이의 공간에 도구 상자에서 활동을 **수신** 및 **SendReply** 활동입니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-128">To call the ReverseString method on the input, drag an **InvokeMethod** activity from the toolbox to the space between the **Receive** and **SendReply** activities.</span></span> <span data-ttu-id="51b4f-129">활동의 속성을 다음과 같이 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-129">Set the properties of the activity as follows:</span></span>

    1.  <span data-ttu-id="51b4f-130">**MethodName**: reversestring으로</span><span class="sxs-lookup"><span data-stu-id="51b4f-130">**MethodName**: ReverseString</span></span>

    2.  <span data-ttu-id="51b4f-131">**결과**: ReversedStringToReturn</span><span class="sxs-lookup"><span data-stu-id="51b4f-131">**Result**: ReversedStringToReturn</span></span>

    3.  <span data-ttu-id="51b4f-132">**매개 변수**: 사용 하 여 새 매개 변수를 만듭니다를 **방향** 의는 **형식** 문자열 및 **값** 이 stringtoreverse.</span><span class="sxs-lookup"><span data-stu-id="51b4f-132">**Parameters**: Create a new parameter with a **Direction** of In, a **Type** of String, and a **Value** of StringToReverse.</span></span>

    4.  <span data-ttu-id="51b4f-133">**TargetType**: NestedServices.StringLibrary</span><span class="sxs-lookup"><span data-stu-id="51b4f-133">**TargetType**: NestedServices.StringLibrary</span></span>

12. <span data-ttu-id="51b4f-134">F5 키를 눌러 서비스를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-134">Test the service by pressing F5.</span></span> <span data-ttu-id="51b4f-135">WCF 테스트 클라이언트가 표시되면 ReverseString() 메서드를 두 번 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-135">In the WCF Test Client that appears, double-click the ReverseString() method.</span></span> <span data-ttu-id="51b4f-136">요청 창에서 입력 `Sample` InputString 매개 변수의 값에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-136">In the Request pane, enter `Sample` for the Value of the InputString parameter.</span></span> <span data-ttu-id="51b4f-137">클릭 **호출할**합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-137">Click **Invoke**.</span></span> <span data-ttu-id="51b4f-138">그러면 서비스에서 "elpmaS"를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-138">The service should return "elpmaS".</span></span>

### <a name="to-create-the-uppercaser-workflow-service"></a><span data-ttu-id="51b4f-139">UpperCaser 워크플로 서비스를 만들려면</span><span class="sxs-lookup"><span data-stu-id="51b4f-139">To create the UpperCaser workflow service</span></span>

1.  <span data-ttu-id="51b4f-140">NestedServices 프로젝트를 마우스 오른쪽 단추로 누르고 **추가** > **새 항목**합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-140">Right-click the NestedServices project and select **Add** > **New Item**.</span></span> <span data-ttu-id="51b4f-141">에 **워크플로** 노드를 선택 **WCF Workflow Service**를 새 서비스 이름 및 `UpperCaserService`합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-141">In the **Workflow** node, select **WCF Workflow Service**, and name the new service `UpperCaserService`.</span></span> <span data-ttu-id="51b4f-142">**추가**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-142">Click **Add**.</span></span> <span data-ttu-id="51b4f-143">그러면 UpperCaserService.xamlx라는 새 워크플로 서비스가 프로젝트에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-143">This should add a new workflow service called UpperCaserService.xamlx to the project.</span></span>

2.  <span data-ttu-id="51b4f-144">디자이너에서 UpperCaserService.xamlx를 열고 기존 삭제 **ReceiveRequest** 하 고 `SendReply` 활동을 끌어서를 `ReceiveAndSendReply` 활동을 기존 시퀀스 활동 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-144">Open UpperCaserService.xamlx in the designer and delete the existing **ReceiveRequest** and `SendReply` activities, and drag a `ReceiveAndSendReply` activity into the existing sequence activity.</span></span>

    1.  <span data-ttu-id="51b4f-145">설정 된 **OperationName** 을 uppercasestring으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-145">Set the **OperationName** to UpperCaseString.</span></span>

    2.  <span data-ttu-id="51b4f-146">설정 된 **ServiceContractName** 을 iuppercasestring으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-146">Set the **ServiceContractName** to IUpperCaseString.</span></span>

    3.  <span data-ttu-id="51b4f-147">선택 된 **CanCreateInstance** 확인란 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-147">Select the **CanCreateInstance** check box.</span></span>

3.  <span data-ttu-id="51b4f-148">SequentialService 활동을 선택한 다음 클릭 합니다 **변수** 디자이너의 아래쪽에 있는 탭입니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-148">Select the SequentialService activity, and then click the **Variables** tab at the bottom of the designer.</span></span> <span data-ttu-id="51b4f-149">String 형식의 StringToUpper, StringToReverse 및 StringToReturn이라는 세 개의 새로운 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-149">Create three new variables named StringToUpper, StringToReverse, and StringToReturn of type String.</span></span>

4.  <span data-ttu-id="51b4f-150">클릭 합니다 **정의** 링크를 **수신** 활동입니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-150">Click the **Define** link in the **Receive** activity.</span></span> <span data-ttu-id="51b4f-151">클릭 합니다 **매개 변수**, 고 StringToUpper에 할당 되는 String 형식의 InputString 이라는 매개 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-151">Click the **Parameters**, and create a parameter named InputString of type String that assigns to StringToUpper.</span></span>

5.  <span data-ttu-id="51b4f-152">클릭 합니다 **정의** 링크를 **SendReplyToReceive** 활동입니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-152">Click the **Define** link in the **SendReplyToReceive** activity.</span></span> <span data-ttu-id="51b4f-153">클릭 합니다 **매개 변수**, 고 StringToReturn에 할당 된 String 형식의 ModifiedString 이라는 매개 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-153">Click the **Parameters**, and create a parameter named ModifiedString of type String, assigned to StringToReturn.</span></span>

6.  <span data-ttu-id="51b4f-154">서비스의 논리를 구현하려면 다음 코드를 사용하여 StringLibrary 클래스에 새 메서드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-154">To implement the logic for the service, create a new method in the StringLibrary class using the following code.</span></span>

    ```
    public static String UpperCaseString(string StringToUpperCase)
    {
         return StringToUpperCase.ToUpper();

    }
    ```

7.  <span data-ttu-id="51b4f-155">입력에 대해 UpperCaseString 메서드를 호출 하려면 끌어를 **InvokeMethod** 사이의 공간에 도구 상자에서 활동을 **수신** 및 **SendReply** 활동입니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-155">To call the UpperCaseString method on the input, drag an **InvokeMethod** activity from the toolbox to the space between the **Receive** and **SendReply** activities.</span></span> <span data-ttu-id="51b4f-156">활동의 속성을 다음과 같이 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-156">Set the properties of the activity as follows:</span></span>

    1.  <span data-ttu-id="51b4f-157">**MethodName**: uppercasestring으로</span><span class="sxs-lookup"><span data-stu-id="51b4f-157">**MethodName**: UpperCaseString</span></span>

    2.  <span data-ttu-id="51b4f-158">**결과**: StringToReverse</span><span class="sxs-lookup"><span data-stu-id="51b4f-158">**Result**: StringToReverse</span></span>

    3.  <span data-ttu-id="51b4f-159">**매개 변수**: 사용 하 여 새 매개 변수를 만듭니다를 **방향** 의는 **형식** 문자열 및 **값** stringtoupper 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-159">**Parameters**: Create a new parameter with a **Direction** of In, a **Type** of String, and a **Value** of StringToUpper.</span></span>

    4.  <span data-ttu-id="51b4f-160">**TargetType**: NestedServices.StringLibrary</span><span class="sxs-lookup"><span data-stu-id="51b4f-160">**TargetType**: NestedServices.StringLibrary</span></span>

8.  <span data-ttu-id="51b4f-161">이제 수정된 문자열에 대해 첫 번째 서비스를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-161">We’ll now call the first service on the modified string.</span></span> <span data-ttu-id="51b4f-162">프로젝트를 마우스 오른쪽 단추로 누르고 **추가** > **서비스 참조**합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-162">Right-click the project and select **Add** > **Service Reference**.</span></span> <span data-ttu-id="51b4f-163">서비스에 대 한 서비스 참조 추가 http://localhost/NestedServices/StringReverserService.xamlx 첫 번째 웹 서비스에 액세스 하려면 사용자 지정 활동을 만드는 프로젝트를 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-163">Add a service reference to the service at http://localhost/NestedServices/StringReverserService.xamlx and build the project to create a custom activity to access the first Web service.</span></span>

9. <span data-ttu-id="51b4f-164">끌어 새 활동의 인스턴스, 워크플로 간에 **InvokeMethod** 활동 하며 **SendReplyToReceive** 활동입니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-164">Drag an instance of the new activity onto the workflow, between the **InvokeMethod** activity and the **SendReplyToReceive** activities.</span></span> <span data-ttu-id="51b4f-165">새 활동의 InputString 속성에 StringToReverse 변수를 할당하고 StringToReturn 속성에 StringToReturn 변수를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-165">Assign the variable StringToReverse to the InputString property of the new activity, and the variable StringToReturn to the StringToReturn property.</span></span>

10. <span data-ttu-id="51b4f-166">NestedServices 프로젝트의 속성 페이지를 열고 변경 합니다 **특정 페이지** 에 **웹** UpperCaserService.xamlx 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-166">Open the Properties page for the NestedServices project, and change the **Specific Page** in the **Web** tab to UpperCaserService.xamlx.</span></span>

11. <span data-ttu-id="51b4f-167">F5 키를 눌러 서비스를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-167">Test the service by pressing F5.</span></span> <span data-ttu-id="51b4f-168">WCF 테스트 클라이언트가 표시되면 ReverseString() 메서드를 두 번 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-168">In the WCF Test Client that appears, double-click the ReverseString() method.</span></span> <span data-ttu-id="51b4f-169">요청 창에서 입력 `Sample` InputString 매개 변수의 값에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-169">In the Request pane, enter `Sample` for the Value of the InputString parameter.</span></span> <span data-ttu-id="51b4f-170">클릭 **호출할**합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-170">Click **Invoke**.</span></span> <span data-ttu-id="51b4f-171">그러면 서비스에서 "ELPMAS"를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-171">The service should return "ELPMAS".</span></span>

### <a name="to-create-a-client-to-call-the-services"></a><span data-ttu-id="51b4f-172">서비스를 호출할 클라이언트를 만들려면</span><span class="sxs-lookup"><span data-stu-id="51b4f-172">To create a client to call the services</span></span>

1.  <span data-ttu-id="51b4f-173">솔루션에 Client라는 새 콘솔 응용 프로그램 프로젝트를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-173">Add a new Console application project called Client to the solution.</span></span>

2.  <span data-ttu-id="51b4f-174">클라이언트 프로젝트를 마우스 오른쪽 단추로 누르고 **추가** > **서비스 참조**합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-174">Right-click the Client project and select **Add** > **Service Reference**.</span></span> <span data-ttu-id="51b4f-175">표시 되는 창에서 클릭 **Discover**합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-175">In the window that appears, click **Discover**.</span></span> <span data-ttu-id="51b4f-176">StringReverserService.xamlx를 선택하고 네임스페이스로 ReverseService를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-176">Select StringReverserService.xamlx, and enter ReverseService as the namespace.</span></span>  <span data-ttu-id="51b4f-177">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-177">Click **OK**.</span></span>

3.  <span data-ttu-id="51b4f-178">Program.cs의 Main 메서드를 다음 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="51b4f-178">Replace the Main method in Program.cs with the following code.</span></span>

    ```
    static void Main(string[] args)
    {
        Console.Write("Input string to process:");
        String input = Console.ReadLine();
        var service = new ReverseService.ReverseStringClient();
        Console.WriteLine("Output from service: {0}", service.ReverseString(input));
        Console.ReadKey();
    }
    ```