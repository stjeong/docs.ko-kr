---
title: Visual Studio에서 Windows 서비스 응용 프로그램 만들기
ms.date: 09/10/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Windows service applications, walkthroughs
- Windows service applications, creating
ms.assetid: e24d8a3d-edc6-485c-b6e0-5672d91fb607
author: ghogen
manager: douge
ms.openlocfilehash: 27acdac5d34b96dd04fec1bb763edec9077ff928
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/24/2018
ms.locfileid: "46493609"
---
# <a name="walkthrough-create-a-windows-service-app"></a><span data-ttu-id="4a52e-102">연습: Windows 서비스 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="4a52e-102">Walkthrough: Create a Windows service app</span></span>

<span data-ttu-id="4a52e-103">이 문서에서는 이벤트 로그에 메시지를 쓰는 간단한 Windows 서비스 앱을 Visual Studio에서 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-103">This article demonstrates how to create a simple Windows service app in Visual Studio that writes messages to an event log.</span></span>

## <a name="create-a-service"></a><span data-ttu-id="4a52e-104">서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="4a52e-104">Create a service</span></span>

<span data-ttu-id="4a52e-105">우선 프로젝트를 만들고 서비스가 제대로 작동하는 데 필요한 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-105">To begin, create the project and set values that are required for the service to function correctly.</span></span>

1. <span data-ttu-id="4a52e-106">Visual Studio의 메뉴 모음에서 **파일** > **새로 만들기** > **프로젝트**를 선택하거나 **Ctrl**+**Shift**+**N**을 눌러 **새 프로젝트** 대화 상자를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-106">In Visual Studio, on the menu bar, choose **File** > **New** > **Project** (or press **Ctrl**+**Shift**+**N**) to open the **New Project** dialog.</span></span>

2. <span data-ttu-id="4a52e-107">**Windows 서비스** 프로젝트 템플릿을 탐색하여 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-107">Navigate to and select the **Windows Service** project template.</span></span> <span data-ttu-id="4a52e-108">**설치됨** > [**Visual C#** 또는 **Visual Basic**] > **Windows 데스크톱**을 확장하거나 오른쪽 위의 검색 상자에 **Windows 서비스**를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-108">Expand **Installed** > [**Visual C#** or **Visual Basic**] > **Windows Desktop**, or type **Windows Service** in the search box on the upper right.</span></span>

   ![Visual Studio의 새 프로젝트 대화 상자에 있는 Windows 서비스 템플릿](media/new-project-dialog.png)

   > [!NOTE]
   > <span data-ttu-id="4a52e-110">**Windows 서비스** 템플릿이 표시되지 않는 경우 **.NET 데스크톱 개발** 워크로드를 설치해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-110">If you don't see the **Windows Service** template, you may need to install the **.NET desktop development** workload.</span></span> <span data-ttu-id="4a52e-111">**새 프로젝트** 대화 상자에서 왼쪽 아래에 있는 **Visual Studio 설치 관리자 열기** 링크를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-111">In the **New Project** dialog, click the link that says **Open Visual Studio Installer** on the lower left.</span></span> <span data-ttu-id="4a52e-112">**Visual Studio 설치 관리자**에서 **.NET 데스크톱 개발** 워크로드를 선택한 다음, **수정**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-112">In **Visual Studio Installer**, select the **.NET desktop development** workload and then choose **Modify**.</span></span>

3. <span data-ttu-id="4a52e-113">프로젝트 이름을 **MyNewService**로 지정하고 **확인**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-113">Name the project **MyNewService**, and then choose **OK**.</span></span>

   <span data-ttu-id="4a52e-114">프로젝트 템플릿은 <xref:System.ServiceProcess.ServiceBase?displayProperty=nameWithType>에서 상속된 `Service1`이라는 구성 요소 클래스를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-114">The project template includes a component class named `Service1` that inherits from <xref:System.ServiceProcess.ServiceBase?displayProperty=nameWithType>.</span></span> <span data-ttu-id="4a52e-115">여기에는 서비스를 시작하는 코드 등의 많은 기본 서비스 코드가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-115">It includes much of the basic service code, such as the code to start the service.</span></span>

## <a name="rename-the-service"></a><span data-ttu-id="4a52e-116">서비스 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="4a52e-116">Rename the service</span></span>

<span data-ttu-id="4a52e-117">서비스 이름을 **Service1**에서 **MyNewService**로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-117">Rename the service from **Service1** to **MyNewService**.</span></span>

1. <span data-ttu-id="4a52e-118">Service1.cs(또는 Service1.vb)의 **디자인** 보기에서 **코드 보기로 전환** 링크를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-118">In the **Design** view for Service1.cs (or Service1.vb), click the link to **switch to code view**.</span></span> <span data-ttu-id="4a52e-119">**Service1**을 마우스 오른쪽 단추로 클릭하고 상황에 맞는 메뉴에서 **이름 바꾸기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-119">Right-click on **Service1** and select **Rename** from the context menu.</span></span> <span data-ttu-id="4a52e-120">**MyNewService**를 입력하고 **Enter** 키를 누르거나 **적용**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-120">Enter **MyNewService** and then press **Enter** or click **Apply**.</span></span>

2. <span data-ttu-id="4a52e-121">**Service1.cs [디자인]** 또는 **Service1.vb [디자인]** 의 **속성** 창에서 **ServiceName** 값을 **MyNewService**로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-121">In the **Properties** window for **Service1.cs [Design]** or **Service1.vb [Design]**, change the **ServiceName** value to **MyNewService**.</span></span>

3. <span data-ttu-id="4a52e-122">**솔루션 탐색기**에서 **Service1.cs**의 이름을 **MyNewService.cs**로 바꾸거나 **Service1.vb**의 이름을 **MyNewService.vb**로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-122">In **Solution Explorer**, rename **Service1.cs** to **MyNewService.cs**, or rename **Service1.vb** to **MyNewService.vb**.</span></span>

## <a name="add-features-to-the-service"></a><span data-ttu-id="4a52e-123">서비스에 기능 추가</span><span class="sxs-lookup"><span data-stu-id="4a52e-123">Add features to the service</span></span>

<span data-ttu-id="4a52e-124">다음 섹션에서는 Windows 서비스에 사용자 지정 이벤트 로그를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-124">In this section, you add a custom event log to the Windows service.</span></span> <span data-ttu-id="4a52e-125">이벤트 로그는 Windows 서비스와 연관이 없으며,</span><span class="sxs-lookup"><span data-stu-id="4a52e-125">Event logs are not associated in any way with Windows services.</span></span> <span data-ttu-id="4a52e-126">여기에서는 단지 Windows 서비스에 추가할 수 있는 구성 요소 종류의 한 예로 <xref:System.Diagnostics.EventLog> 구성 요소를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-126">The <xref:System.Diagnostics.EventLog> component is used here as an example of the type of component you can add to a Windows service.</span></span>

### <a name="add-custom-event-log-functionality"></a><span data-ttu-id="4a52e-127">사용자 지정 이벤트 로그 기능 추가</span><span class="sxs-lookup"><span data-stu-id="4a52e-127">Add custom event log functionality</span></span>

1. <span data-ttu-id="4a52e-128">**솔루션 탐색기**에서 **MyNewService.cs** 또는 **MyNewService.vb**의 상황에 맞는 메뉴를 열고 **뷰 디자이너**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-128">In **Solution Explorer**, open the context menu for **MyNewService.cs** or **MyNewService.vb**, and then choose **View Designer**.</span></span>

2. <span data-ttu-id="4a52e-129">**도구 상자** 의 **구성 요소**섹션에서 <xref:System.Diagnostics.EventLog> 구성 요소를 디자이너로 끌어 옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-129">From the **Components** section of the **Toolbox**, drag an <xref:System.Diagnostics.EventLog> component to the designer.</span></span>

3. <span data-ttu-id="4a52e-130">**솔루션 탐색기**에서 **MyNewService.cs** 또는 **MyNewService.vb**의 상황에 맞는 메뉴를 열고 **코드 보기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-130">In **Solution Explorer**, open the context menu for **MyNewService.cs** or **MyNewService.vb**, and then choose **View Code**.</span></span>

4. <span data-ttu-id="4a52e-131">사용자 지정 이벤트 로그를 정의하는 생성자를 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-131">Edit the constructor to define a custom event log:</span></span>

   ```csharp
   public MyNewService()
   {
        InitializeComponent();

        eventLog1 = new System.Diagnostics.EventLog();
        if (!System.Diagnostics.EventLog.SourceExists("MySource"))
        {
            System.Diagnostics.EventLog.CreateEventSource(
                "MySource", "MyNewLog");
        }
        eventLog1.Source = "MySource";
        eventLog1.Log = "MyNewLog";
    }
   ```

   [!code-vb[VbRadconService#2](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#2)]

### <a name="define-what-occurs-when-the-service-starts"></a><span data-ttu-id="4a52e-132">서비스가 시작될 때 수행되는 동작 정의</span><span class="sxs-lookup"><span data-stu-id="4a52e-132">Define what occurs when the service starts</span></span>

<span data-ttu-id="4a52e-133">코드 편집기에서 프로젝트를 만들 때 자동으로 재정의된 <xref:System.ServiceProcess.ServiceBase.OnStart%2A> 메서드를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-133">In the code editor, locate the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method that was automatically overridden when you created the project.</span></span> <span data-ttu-id="4a52e-134">서비스가 시작될 때 이벤트 로그에 항목을 기록하는 코드 줄을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-134">Add a line of code that writes an entry to the event log when the service starts:</span></span>

[!code-csharp[VbRadconService#3](../../../samples/snippets/csharp/VS_Snippets_VBCSharp/VbRadconService/CS/MyNewService.cs#3)]
[!code-vb[VbRadconService#3](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#3)]

<span data-ttu-id="4a52e-135">서비스 응용 프로그램은 오랫동안 실행되도록 설계되므로 대개 시스템의 특정 항목을 폴링하거나 모니터링합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-135">A service application is designed to be long-running, so it usually polls or monitors something in the system.</span></span> <span data-ttu-id="4a52e-136">모니터링은 <xref:System.ServiceProcess.ServiceBase.OnStart%2A> 메서드에서 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-136">The monitoring is set up in the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method.</span></span> <span data-ttu-id="4a52e-137">그러나 <xref:System.ServiceProcess.ServiceBase.OnStart%2A> 가 실제로 모니터링을 수행하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-137">However, <xref:System.ServiceProcess.ServiceBase.OnStart%2A> doesn’t actually do the monitoring.</span></span> <span data-ttu-id="4a52e-138">서비스의 작업이 시작되고 나면 <xref:System.ServiceProcess.ServiceBase.OnStart%2A> 메서드가 운영 체제에 반환되어야 하며</span><span class="sxs-lookup"><span data-stu-id="4a52e-138">The <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method must return to the operating system after the service's operation has begun.</span></span> <span data-ttu-id="4a52e-139">무제한 순환하거나 방해가 되어서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-139">It must not loop forever or block.</span></span> <span data-ttu-id="4a52e-140">간단한 폴링 메커니즘을 설정하려면 <xref:System.Timers.Timer?displayProperty=nameWithType> 구성 요소를 사용할 수 있습니다. 즉, <xref:System.ServiceProcess.ServiceBase.OnStart%2A> 메서드에서 구성 요소에 대한 매개 변수를 설정한 다음 <xref:System.Timers.Timer.Enabled%2A> 속성을 `true`로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-140">To set up a simple polling mechanism, you can use the <xref:System.Timers.Timer?displayProperty=nameWithType> component as follows: In the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method, set parameters on the component, and then set the <xref:System.Timers.Timer.Enabled%2A> property to `true`.</span></span> <span data-ttu-id="4a52e-141">타이머는 코드에서 주기적으로 이벤트를 발생시키며 그러는 동안에도 서비스에서는 모니터링을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-141">The timer raises events in your code periodically, at which time your service could do its monitoring.</span></span> <span data-ttu-id="4a52e-142">이렇게 하려면 다음 코드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-142">You can use the following code to do this:</span></span>

```csharp
// Set up a timer that triggers every minute.
System.Timers.Timer timer = new System.Timers.Timer();
timer.Interval = 60000; // 60 seconds
timer.Elapsed += new System.Timers.ElapsedEventHandler(this.OnTimer);
timer.Start();
```

```vb
' Set up a timer that triggers every minute.
Dim timer As System.Timers.Timer = New System.Timers.Timer()
timer.Interval = 60000 ' 60 seconds
AddHandler timer.Elapsed, AddressOf Me.OnTimer
timer.Start()
```

<span data-ttu-id="4a52e-143">멤버 변수를 클래스에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-143">Add a member variable to the class.</span></span> <span data-ttu-id="4a52e-144">여기에는 이벤트 로그에 기록할 다음 이벤트의 식별자가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-144">It contains the identifier of the next event to write into the event log.</span></span>

```csharp
private int eventId = 1;
```

```vb
Private eventId As Integer = 1
```

<span data-ttu-id="4a52e-145">타이머 이벤트를 처리하는 새 메서드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-145">Add a new method to handle the timer event:</span></span>

```csharp
public void OnTimer(object sender, System.Timers.ElapsedEventArgs args)
{
    // TODO: Insert monitoring activities here.
    eventLog1.WriteEntry("Monitoring the System", EventLogEntryType.Information, eventId++);
}
```

```vb
Private Sub OnTimer(sender As Object, e As Timers.ElapsedEventArgs)
    ' TODO: Insert monitoring activities here.
    eventLog1.WriteEntry("Monitoring the System", EventLogEntryType.Information, eventId)
    eventId = eventId + 1
End Sub
```

<span data-ttu-id="4a52e-146">주 스레드에서 모든 작업을 실행하는 대신 백그라운드 작업자 스레드를 사용하여 작업을 수행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-146">You might want to perform tasks by using background worker threads instead of running all your work on the main thread.</span></span> <span data-ttu-id="4a52e-147">자세한 내용은 <xref:System.ComponentModel.BackgroundWorker?displayProperty=fullName>을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4a52e-147">For more information, see <xref:System.ComponentModel.BackgroundWorker?displayProperty=fullName>.</span></span>

### <a name="define-what-occurs-when-the-service-is-stopped"></a><span data-ttu-id="4a52e-148">서비스가 중지될 때 수행되는 동작 정의</span><span class="sxs-lookup"><span data-stu-id="4a52e-148">Define what occurs when the service is stopped</span></span>

<span data-ttu-id="4a52e-149">서비스가 중지될 때 이벤트 로그에 항목을 추가하는 코드 줄을 <xref:System.ServiceProcess.ServiceBase.OnStop%2A> 메서드에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-149">Add a line of code to the <xref:System.ServiceProcess.ServiceBase.OnStop%2A> method that adds an entry to the event log when the service is stopped:</span></span>

```csharp
eventLog1.WriteEntry("In OnStop.");
```

[!code-vb[VbRadconService#4](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#4)]

### <a name="define-other-actions-for-the-service"></a><span data-ttu-id="4a52e-150">서비스의 다른 동작 정의</span><span class="sxs-lookup"><span data-stu-id="4a52e-150">Define other actions for the service</span></span>

<span data-ttu-id="4a52e-151"><xref:System.ServiceProcess.ServiceBase.OnPause%2A>, <xref:System.ServiceProcess.ServiceBase.OnContinue%2A> 및 <xref:System.ServiceProcess.ServiceBase.OnShutdown%2A> 메서드를 재정의하여 구성 요소에 대한 처리 작업을 추가로 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-151">You can override the <xref:System.ServiceProcess.ServiceBase.OnPause%2A>, <xref:System.ServiceProcess.ServiceBase.OnContinue%2A>, and <xref:System.ServiceProcess.ServiceBase.OnShutdown%2A> methods to define additional processing for your component.</span></span> <span data-ttu-id="4a52e-152">다음 코드에서는 <xref:System.ServiceProcess.ServiceBase.OnContinue%2A> 메서드를 재정의하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-152">The following code shows how you can override the <xref:System.ServiceProcess.ServiceBase.OnContinue%2A> method:</span></span>

[!code-csharp[VbRadconService#5](../../../samples/snippets/csharp/VS_Snippets_VBCSharp/VbRadconService/CS/MyNewService.cs#5)]
[!code-vb[VbRadconService#5](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#5)]

<span data-ttu-id="4a52e-153"><xref:System.Configuration.Install.Installer> 클래스를 통해 Windows 서비스를 설치할 때는 일부 사용자 지정 작업을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-153">Some custom actions have to occur when a Windows service is installed by the <xref:System.Configuration.Install.Installer> class.</span></span> <span data-ttu-id="4a52e-154">Visual Studio에서 특별히 Windows 서비스를 위해 이러한 설치 관리자를 만들어 프로젝트에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-154">Visual Studio can create these installers specifically for a Windows service and add them to your project.</span></span>

## <a name="set-service-status"></a><span data-ttu-id="4a52e-155">서비스 상태 설정</span><span class="sxs-lookup"><span data-stu-id="4a52e-155">Set service status</span></span>

<span data-ttu-id="4a52e-156">서비스는 서비스 제어 관리자에 상태를 보고합니다. 따라서 사용자는 서비스가 정상적으로 작동 중인지를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-156">Services report their status to the Service Control Manager, so that users can tell whether a service is functioning correctly.</span></span> <span data-ttu-id="4a52e-157">기본적으로 <xref:System.ServiceProcess.ServiceBase> 에서 상속되는 서비스는 중지됨, 일시 중지됨, 실행 중 등의 제한적인 상태 설정 집합을 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-157">By default, services that inherit from <xref:System.ServiceProcess.ServiceBase> report a limited set of status settings, including Stopped, Paused, and Running.</span></span> <span data-ttu-id="4a52e-158">서비스를 시작하는 데 시간이 다소 걸리는 경우에는 시작 보류 중 상태를 보고하면 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-158">If a service takes a little while to start up, it might be helpful to report a Start Pending status.</span></span> <span data-ttu-id="4a52e-159">또한 Windows [SetServiceStatus 함수](/windows/desktop/api/winsvc/nf-winsvc-setservicestatus)를 호출하는 코드를 추가하여 시작 보류 중 및 중지 보류 중 상태 설정을 구현할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-159">You can also implement the Start Pending and Stop Pending status settings by adding code that calls into the Windows [SetServiceStatus function](/windows/desktop/api/winsvc/nf-winsvc-setservicestatus).</span></span>

<span data-ttu-id="4a52e-160">서비스 보류 중 상태를 구현하려면</span><span class="sxs-lookup"><span data-stu-id="4a52e-160">To implement service pending status:</span></span>

1. <span data-ttu-id="4a52e-161">MyNewService.cs 또는 MyNewService.vb 파일에 <xref:System.Runtime.InteropServices?displayProperty=nameWithType> 네임스페이스에 대한 `using` 문 또는 `Imports` 선언을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-161">Add a `using` statement or `Imports` declaration for the <xref:System.Runtime.InteropServices?displayProperty=nameWithType> namespace in the MyNewService.cs or MyNewService.vb file:</span></span>

    ```csharp
    using System.Runtime.InteropServices;
    ```

    ```vb
    Imports System.Runtime.InteropServices
    ```

2. <span data-ttu-id="4a52e-162">`ServiceState` 값을 선언하고 상태에 대한 구조(플랫폼 호출에서 사용함)를 추가하려면 MyNewService.cs에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-162">Add the following code to MyNewService.cs to declare the `ServiceState` values and to add a structure for the status, which you'll use in a platform invoke call:</span></span>

    ```csharp
    public enum ServiceState
    {
        SERVICE_STOPPED = 0x00000001,
        SERVICE_START_PENDING = 0x00000002,
        SERVICE_STOP_PENDING = 0x00000003,
        SERVICE_RUNNING = 0x00000004,
        SERVICE_CONTINUE_PENDING = 0x00000005,
        SERVICE_PAUSE_PENDING = 0x00000006,
        SERVICE_PAUSED = 0x00000007,
    }

    [StructLayout(LayoutKind.Sequential)]
    public struct ServiceStatus
    {
        public int dwServiceType;
        public ServiceState dwCurrentState;
        public int dwControlsAccepted;
        public int dwWin32ExitCode;
        public int dwServiceSpecificExitCode;
        public int dwCheckPoint;
        public int dwWaitHint;
    };
    ```

    ```vb
    Public Enum ServiceState
        SERVICE_STOPPED = 1
        SERVICE_START_PENDING = 2
        SERVICE_STOP_PENDING = 3
        SERVICE_RUNNING = 4
        SERVICE_CONTINUE_PENDING = 5
        SERVICE_PAUSE_PENDING = 6
        SERVICE_PAUSED = 7
    End Enum

    <StructLayout(LayoutKind.Sequential)>
    Public Structure ServiceStatus
        Public dwServiceType As Long
        Public dwCurrentState As ServiceState
        Public dwControlsAccepted As Long
        Public dwWin32ExitCode As Long
        Public dwServiceSpecificExitCode As Long
        Public dwCheckPoint As Long
        Public dwWaitHint As Long
    End Structure
    ```

3. <span data-ttu-id="4a52e-163">이제 `MyNewService` 클래스에서 [플랫폼 호출](../interop/consuming-unmanaged-dll-functions.md)을 사용하여 [SetServiceStatus 함수](/windows/desktop/api/winsvc/nf-winsvc-setservicestatus)를 선언합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-163">Now, in the `MyNewService` class, declare the [SetServiceStatus function](/windows/desktop/api/winsvc/nf-winsvc-setservicestatus) by using [platform invoke](../interop/consuming-unmanaged-dll-functions.md):</span></span>

    ```csharp
    [DllImport("advapi32.dll", SetLastError = true)]
    private static extern bool SetServiceStatus(System.IntPtr handle, ref ServiceStatus serviceStatus);
    ```

    ```vb
    Declare Auto Function SetServiceStatus Lib "advapi32.dll" (ByVal handle As IntPtr, ByRef serviceStatus As ServiceStatus) As Boolean
    ```

4. <span data-ttu-id="4a52e-164">시작 보류 중 상태를 구현하려면 <xref:System.ServiceProcess.ServiceBase.OnStart%2A> 메서드 시작 부분에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-164">To implement the Start Pending status, add the following code to the beginning of the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method:</span></span>

    ```csharp
    // Update the service state to Start Pending.
    ServiceStatus serviceStatus = new ServiceStatus();
    serviceStatus.dwCurrentState = ServiceState.SERVICE_START_PENDING;
    serviceStatus.dwWaitHint = 100000;
    SetServiceStatus(this.ServiceHandle, ref serviceStatus);
    ```

    ```vb
    ' Update the service state to Start Pending.
    Dim serviceStatus As ServiceStatus = New ServiceStatus()
    serviceStatus.dwCurrentState = ServiceState.SERVICE_START_PENDING
    serviceStatus.dwWaitHint = 100000
    SetServiceStatus(Me.ServiceHandle, serviceStatus)
    ```

5. <span data-ttu-id="4a52e-165">상태를 실행 중으로 설정하는 코드를 <xref:System.ServiceProcess.ServiceBase.OnStart%2A> 메서드 끝에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-165">Add code to set the status to Running at the end of the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method.</span></span>

    ```csharp
    // Update the service state to Running.
    serviceStatus.dwCurrentState = ServiceState.SERVICE_RUNNING;
    SetServiceStatus(this.ServiceHandle, ref serviceStatus);
    ```

    ```vb
    ' Update the service state to Running.
    serviceStatus.dwCurrentState = ServiceState.SERVICE_RUNNING
    SetServiceStatus(Me.ServiceHandle, serviceStatus)
    ```

6. <span data-ttu-id="4a52e-166">(선택 사항) <xref:System.ServiceProcess.ServiceBase.OnStop%2A> 메서드에 대해 이 절차를 반복합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-166">(Optional) Repeat this procedure for the <xref:System.ServiceProcess.ServiceBase.OnStop%2A> method.</span></span>

> [!NOTE]
> <span data-ttu-id="4a52e-167">[서비스 제어 관리자](/windows/desktop/Services/service-control-manager)는 [SERVICE_STATUS 구조체](/windows/desktop/api/winsvc/ns-winsvc-_service_status)의 `dwWaitHint` 및 `dwCheckpoint` 멤버를 사용하여 Windows 서비스가 시작 또는 종료될 때까지 기다릴 시간을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-167">The [Service Control Manager](/windows/desktop/Services/service-control-manager) uses the `dwWaitHint` and `dwCheckpoint` members of the [SERVICE_STATUS structure](/windows/desktop/api/winsvc/ns-winsvc-_service_status) to determine how much time to wait for a Windows service to start or shut down.</span></span> <span data-ttu-id="4a52e-168"><xref:System.ServiceProcess.ServiceBase.OnStart%2A> 및 <xref:System.ServiceProcess.ServiceBase.OnStop%2A> 메서드가 오랫동안 실행되는 경우 서비스는 증분된 `dwCheckPoint` 값을 포함하여 [SetServiceStatus](/windows/desktop/api/winsvc/nf-winsvc-setservicestatus)를 다시 호출하여 시간을 더 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-168">If your <xref:System.ServiceProcess.ServiceBase.OnStart%2A> and <xref:System.ServiceProcess.ServiceBase.OnStop%2A> methods run long, your service can request more time by calling [SetServiceStatus](/windows/desktop/api/winsvc/nf-winsvc-setservicestatus) again with an incremented `dwCheckPoint` value.</span></span>

## <a name="add-installers-to-the-service"></a><span data-ttu-id="4a52e-169">서비스에 설치 관리자 추가</span><span class="sxs-lookup"><span data-stu-id="4a52e-169">Add installers to the service</span></span>

<span data-ttu-id="4a52e-170">Windows 서비스를 실행하려면 해당 서비스를 설치해야 합니다. 그러면 서비스 제어 관리자에 서비스가 등록됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-170">Before you can run a Windows service, you need to install it, which registers it with the Service Control Manager.</span></span> <span data-ttu-id="4a52e-171">등록 정보를 처리하는 설치 관리자를 프로젝트에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-171">You can add installers to your project that handle the registration details.</span></span>

1. <span data-ttu-id="4a52e-172">**솔루션 탐색기**에서 **MyNewService.cs** 또는 **MyNewService.vb**의 상황에 맞는 메뉴를 열고 **뷰 디자이너**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-172">In **Solution Explorer**, open the context menu for **MyNewService.cs** or **MyNewService.vb**, and then choose **View Designer**.</span></span>

2. <span data-ttu-id="4a52e-173">디자이너의 배경을 클릭하여 서비스 내용이 아닌 서비스 자체를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-173">Click the background of the designer to select the service itself, instead of any of its contents.</span></span>

3. <span data-ttu-id="4a52e-174">디자이너 창의 상황에 맞는 메뉴를 열고(포인팅 장치를 사용하는 경우 창 안쪽을 마우스 오른쪽 단추로 클릭) **설치 관리자 추가**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-174">Open the context menu for the designer window (if you’re using a pointing device, right-click inside the window), and then choose **Add Installer**.</span></span>

   <span data-ttu-id="4a52e-175">기본적으로 설치 관리자가 두 개 들어 있는 구성 요소 클래스가 프로젝트에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-175">By default, a component class that contains two installers is added to your project.</span></span> <span data-ttu-id="4a52e-176">구성 요소의 이름이 **ProjectInstaller**로 지정되며 구성 요소에는 서비스를 위한 설치 관리자와 서비스 관련 프로세스를 위한 설치 관리자가 들어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-176">The component is named **ProjectInstaller**, and the installers it contains are the installer for your service and the installer for the service's associated process.</span></span>

4. <span data-ttu-id="4a52e-177">**ProjectInstaller** 의 **디자인**뷰에서 Visual C# 프로젝트의 경우 **serviceInstaller1** 를 선택하고 Visual Basic 프로젝트의 경우 **ServiceInstaller1** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-177">In **Design** view for **ProjectInstaller**, choose **serviceInstaller1** for a Visual C# project, or **ServiceInstaller1** for a Visual Basic project.</span></span>

5. <span data-ttu-id="4a52e-178">**속성** 창에서 <xref:System.ServiceProcess.ServiceInstaller.ServiceName%2A> 속성이 **MyNewService**로 설정되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-178">In the **Properties** window, make sure the <xref:System.ServiceProcess.ServiceInstaller.ServiceName%2A> property is set to **MyNewService**.</span></span>

6. <span data-ttu-id="4a52e-179">**설명** 속성을 "샘플 서비스"와 같은 텍스트로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-179">Set the **Description** property to some text, such as "A sample service".</span></span> <span data-ttu-id="4a52e-180">이 텍스트는 서비스 창에 표시되며 사용자가 서비스를 식별하고 서비스의 용도를 이해하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-180">This text appears in the Services window and helps the user identify the service and understand what it’s used for.</span></span>

7. <span data-ttu-id="4a52e-181"><xref:System.ServiceProcess.ServiceInstaller.DisplayName%2A> 속성을 서비스 창의 **이름** 열에 표시할 텍스트로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-181">Set the <xref:System.ServiceProcess.ServiceInstaller.DisplayName%2A> property to the text that you want to appear in the Services window in the **Name** column.</span></span> <span data-ttu-id="4a52e-182">예를 들어 "MyNewService 표시 이름"을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-182">For example, you can enter "MyNewService Display Name".</span></span> <span data-ttu-id="4a52e-183">이 이름은 <xref:System.ServiceProcess.ServiceInstaller.ServiceName%2A> 명령을 사용하여 서비스를 시작하는 등의 경우 시스템에서 사용하는 이름인 `net start` 속성과는 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-183">This name can be different from the <xref:System.ServiceProcess.ServiceInstaller.ServiceName%2A> property, which is the name used by the system (for example, when you use the `net start` command to start your service).</span></span>

8. <span data-ttu-id="4a52e-184"><xref:System.ServiceProcess.ServiceInstaller.StartType%2A> 속성을 <xref:System.ServiceProcess.ServiceStartMode.Automatic>으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-184">Set the <xref:System.ServiceProcess.ServiceInstaller.StartType%2A> property to <xref:System.ServiceProcess.ServiceStartMode.Automatic>.</span></span>

     <span data-ttu-id="4a52e-185">![Windows 서비스에 대한 설치 관리자 속성](../../../docs/framework/windows-services/media/windowsservice-installerproperties.PNG "WindowsService_InstallerProperties")</span><span class="sxs-lookup"><span data-stu-id="4a52e-185">![Installer Properties for a Windows service](../../../docs/framework/windows-services/media/windowsservice-installerproperties.PNG "WindowsService_InstallerProperties")</span></span>

9. <span data-ttu-id="4a52e-186">디자이너에서 Visual C# 프로젝트의 경우 **serviceProcessInstaller1** 을 선택하고 Visual Basic 프로젝트의 경우 **ServiceProcessInstaller1** 을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-186">In the designer, choose **serviceProcessInstaller1** for a Visual C# project, or **ServiceProcessInstaller1** for a Visual Basic project.</span></span> <span data-ttu-id="4a52e-187"><xref:System.ServiceProcess.ServiceProcessInstaller.Account%2A> 속성을 <xref:System.ServiceProcess.ServiceAccount.LocalSystem>으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-187">Set the <xref:System.ServiceProcess.ServiceProcessInstaller.Account%2A> property to <xref:System.ServiceProcess.ServiceAccount.LocalSystem>.</span></span> <span data-ttu-id="4a52e-188">이렇게 하면 로컬 시스템 계정을 사용하여 서비스가 설치되고 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-188">This causes the service to be installed and to run using the local system account.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="4a52e-189"><xref:System.ServiceProcess.ServiceAccount.LocalSystem> 계정에는 광범위한 권한이 있습니다. 예를 들어, 이 계정은 이벤트 로그에 쓸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-189">The <xref:System.ServiceProcess.ServiceAccount.LocalSystem> account has broad permissions, including the ability to write to the event log.</span></span> <span data-ttu-id="4a52e-190">이 계정을 사용할 때는 악성 소프트웨어의 공격을 받을 가능성이 커지므로 주의해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-190">Use this account with caution, because it might increase your risk of attacks from malicious software.</span></span> <span data-ttu-id="4a52e-191">다른 작업에는 <xref:System.ServiceProcess.ServiceAccount.LocalService> 계정을 사용하는 것이 좋습니다. 이 계정은 로컬 컴퓨터에서 권한 없는 사용자의 역할을 하며 원격 서버에 익명 자격 증명을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-191">For other tasks, consider using the <xref:System.ServiceProcess.ServiceAccount.LocalService> account, which acts as a non-privileged user on the local computer and presents anonymous credentials to any remote server.</span></span> <span data-ttu-id="4a52e-192"><xref:System.ServiceProcess.ServiceAccount.LocalService> 계정을 사용하는 경우 이 예제는 실패합니다. 이벤트 로그에 대한 쓰기 권한이 필요하기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-192">This example fails if you try to use the <xref:System.ServiceProcess.ServiceAccount.LocalService> account, because it needs permission to write to the event log.</span></span>

<span data-ttu-id="4a52e-193">설치 관리자에 대한 자세한 내용은 [방법: 서비스 응용 프로그램에 설치 관리자 추가](../../../docs/framework/windows-services/how-to-add-installers-to-your-service-application.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4a52e-193">For more information about installers, see [How to: Add Installers to Your service Application](../../../docs/framework/windows-services/how-to-add-installers-to-your-service-application.md).</span></span>

## <a name="optional-set-startup-parameters"></a><span data-ttu-id="4a52e-194">(선택 사항) 시작 매개 변수 설정</span><span class="sxs-lookup"><span data-stu-id="4a52e-194">(Optional) Set startup parameters</span></span>

<span data-ttu-id="4a52e-195">다른 실행 파일과 마찬가지로 Windows 서비스에도 명령줄 인수나 시작 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-195">A Windows service, like any other executable, can accept command-line arguments, or startup parameters.</span></span> <span data-ttu-id="4a52e-196">프로세스 시작 매개 변수에 코드를 추가하면 사용자가 Windows 제어판의 서비스 창을 사용하여 고유한 사용자 지정 시작 매개 변수로 서비스를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-196">When you add code to process startup parameters, users can start your service with their own custom startup parameters by using the Services window in the Windows Control Panel.</span></span> <span data-ttu-id="4a52e-197">그러나 이러한 시작 매개 변수는 다음 번에 서비스를 시작할 때 유지되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-197">However, these startup parameters are not persisted the next time the service starts.</span></span> <span data-ttu-id="4a52e-198">시작 매개 변수를 영구적으로 설정하려는 경우 아래 절차에 나와 있는 것처럼 레지스트리에서 설정하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-198">To set startup parameters permanently, you can set them in the registry, as shown in this procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="4a52e-199">시작 매개 변수 추가를 결정하기 전에 시작 매개 변수가 서비스로 정보를 전달하는 가장 효율적인 방법인지를 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-199">Before you decide to add startup parameters, consider whether that is the best way to pass information to your service.</span></span> <span data-ttu-id="4a52e-200">시작 매개 변수는 쉽게 사용하고 구문 분석할 수 있으며 사용자가 쉽게 재정의할 수 있지만 설명서가 없으면 사용자가 검색하고 사용하기가 어려울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-200">Although startup parameters are easy to use and to parse, and users can easily override them, they might be harder for users to discover and use without documentation.</span></span> <span data-ttu-id="4a52e-201">일반적으로 서비스에 많은 시작 매개 변수가 필요한 경우에는 레지스트리나 구성 파일을 대신 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-201">Generally, if your service requires more than just a few startup parameters, you should consider using the registry or a configuration file instead.</span></span> <span data-ttu-id="4a52e-202">모든 Windows 서비스에는 레지스트리의 **HKLM\System\CurrentControlSet\services** 아래에 항목이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-202">Every Windows service has an entry in the registry under **HKLM\System\CurrentControlSet\services**.</span></span> <span data-ttu-id="4a52e-203">이 서비스의 키 아래에서 **매개 변수** 하위 키를 사용하여 서비스가 액세스할 수 있는 정보를 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-203">Under the service's key, you can use the **Parameters** subkey to store information that your service can access.</span></span> <span data-ttu-id="4a52e-204">Windows 서비스의 응용 프로그램 구성 파일은 다른 프로그램 형식에서와 같은 방식으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-204">You can use application configuration files for a Windows service the same way you do for other types of programs.</span></span> <span data-ttu-id="4a52e-205">예제 코드를 보려면 <xref:System.Configuration.ConfigurationManager.AppSettings%2A>를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4a52e-205">For example code, see <xref:System.Configuration.ConfigurationManager.AppSettings%2A>.</span></span>

<span data-ttu-id="4a52e-206">시작 매개 변수를 추가하려면</span><span class="sxs-lookup"><span data-stu-id="4a52e-206">To add startup parameters:</span></span>

1. <span data-ttu-id="4a52e-207">Program.cs 또는 MyNewService.Designer.vb의 `Main` 메서드에서 서비스 생성자에 전달할 입력 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-207">In the `Main` method in Program.cs or in MyNewService.Designer.vb, add an input parameter to pass to the service constructor:</span></span>

   ```csharp
   static void Main(string[] args)
   {
       ServiceBase[] ServicesToRun;
       ServicesToRun = new ServiceBase[]
       {
           new MyNewService(args)
       };
       ServiceBase.Run(ServicesToRun);
   }
   ```

   ```vb
   Shared Sub Main(ByVal cmdArgs() As String)
       Dim ServicesToRun() As System.ServiceProcess.ServiceBase = New System.ServiceProcess.ServiceBase() {New MyNewServiceVB(cmdArgs)}
       System.ServiceProcess.ServiceBase.Run(ServicesToRun)
   End Sub
   ```

2. <span data-ttu-id="4a52e-208">`MyNewService` 생성자를 다음과 같이 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-208">Change the `MyNewService` constructor as follows:</span></span>

   ```csharp
   public MyNewService(string[] args)
   {
       InitializeComponent();

        string eventSourceName = "MySource";
        string logName = "MyNewLog";

        if (args.Length > 0)
        {
            eventSourceName = args[0];
        }

        if (args.Length > 1)
        {
            logName = args[1];
        }

        eventLog1 = new System.Diagnostics.EventLog();

        if (!System.Diagnostics.EventLog.SourceExists(eventSourceName))
        {
            System.Diagnostics.EventLog.CreateEventSource(eventSourceName, logName);
        }

        eventLog1.Source = eventSourceName;
        eventLog1.Log = logName;
   }
   ```

   ```vb
   Public Sub New(ByVal cmdArgs() As String)
       InitializeComponent()
       Dim eventSourceName As String = "MySource"
       Dim logName As String = "MyNewLog"
       If (cmdArgs.Count() > 0) Then
           eventSourceName = cmdArgs(0)
       End If
       If (cmdArgs.Count() > 1) Then
           logName = cmdArgs(1)
       End If
       eventLog1 = New System.Diagnostics.EventLog()
       If (Not System.Diagnostics.EventLog.SourceExists(eventSourceName)) Then
           System.Diagnostics.EventLog.CreateEventSource(eventSourceName, logName)
       End If
       eventLog1.Source = eventSourceName
       eventLog1.Log = logName
   End Sub
   ```

   <span data-ttu-id="4a52e-209">이 코드는 제공된 시작 매개 변수에 따라 이벤트 소스 및 로그 이름을 설정하거나, 인수를 제공하지 않는 경우에는 기본값을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-209">This code sets the event source and log name according to the supplied startup parameters, or uses default values if no arguments are supplied.</span></span>

3. <span data-ttu-id="4a52e-210">명령줄 인수를 지정하려면 ProjectInstaller.cs 또는 ProjectInstaller.vb의 `ProjectInstaller` 클래스에 다음 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-210">To specify the command-line arguments, add the following code to the `ProjectInstaller` class in ProjectInstaller.cs or ProjectInstaller.vb:</span></span>

   ```csharp
   protected override void OnBeforeInstall(IDictionary savedState)
   {
       string parameter = "MySource1\" \"MyLogFile1";
       Context.Parameters["assemblypath"] = "\"" + Context.Parameters["assemblypath"] + "\" \"" + parameter + "\"";
       base.OnBeforeInstall(savedState);
   }
   ```

   ```vb
   Protected Overrides Sub OnBeforeInstall(ByVal savedState As IDictionary)
       Dim parameter As String = "MySource1"" ""MyLogFile1"
       Context.Parameters("assemblypath") = """" + Context.Parameters("assemblypath") + """ """ + parameter + """"
       MyBase.OnBeforeInstall(savedState)
   End Sub
   ```

   <span data-ttu-id="4a52e-211">이 코드는 기본 매개 변수 값을 추가하여 일반적으로 Windows 서비스 실행 파일의 전체 경로를 포함하는 **ImagePath** 레지스트리 키를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-211">This code modifies the **ImagePath** registry key, which typically contains the full path to the executable for the Windows service, by adding the default parameter values.</span></span> <span data-ttu-id="4a52e-212">경로와 개별 매개 변수는 따옴표로 묶어야 서비스가 올바르게 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-212">The quotation marks around the path (and around each individual parameter) are required for the service to start up correctly.</span></span> <span data-ttu-id="4a52e-213">이 Windows 서비스의 시작 매개 변수를 변경하려는 경우 사용자는 **ImagePath** 레지스트리 키에 지정된 매개 변수를 변경할 수 있습니다. 그러나 해당 키를 프로그래밍 방식으로 변경하고 사용자에게 친숙한 방식(예: 관리 또는 구성 유틸리티)으로 기능을 노출하는 것이 좀 더 효율적입니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-213">To change the startup parameters for this Windows service, users can change the parameters given in the **ImagePath** registry key, although the better way is to change it programmatically and expose the functionality to users in a friendly way (for example, in a management or configuration utility).</span></span>

## <a name="build-the-service"></a><span data-ttu-id="4a52e-214">서비스 빌드</span><span class="sxs-lookup"><span data-stu-id="4a52e-214">Build the service</span></span>

1. <span data-ttu-id="4a52e-215">**솔루션 탐색기**에서 프로젝트의 상황에 맞는 메뉴를 열고 **속성**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-215">In **Solution Explorer**, open the context menu for your project, and then choose **Properties**.</span></span>

   <span data-ttu-id="4a52e-216">프로젝트의 속성 페이지가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-216">The property pages for your project appear.</span></span>

2. <span data-ttu-id="4a52e-217">**응용 프로그램** 탭의 **시작 개체** 목록에서 **MyNewService.Program**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-217">On the **Application** tab, in the **Startup object** list, choose **MyNewService.Program**.</span></span>

3. <span data-ttu-id="4a52e-218">**솔루션 탐색기**에서 프로젝트의 상황에 맞는 메뉴를 열고 **빌드**를 선택하여 프로젝트를 빌드합니다(또는 **Ctrl**+**Shift**+**B**를 누름).</span><span class="sxs-lookup"><span data-stu-id="4a52e-218">In **Solution Explorer**, open the context menu for your project, and then choose **Build** to build the project (or press **Ctrl**+**Shift**+**B**).</span></span>

## <a name="install-the-service"></a><span data-ttu-id="4a52e-219">서비스 설치</span><span class="sxs-lookup"><span data-stu-id="4a52e-219">Install the service</span></span>

<span data-ttu-id="4a52e-220">이제 Windows 서비스를 빌드했으므로 이를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-220">Now that you've built the Windows service, you can install it.</span></span> <span data-ttu-id="4a52e-221">Windows 서비스를 설치하려면 설치할 컴퓨터에서 관리자 자격 증명이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-221">To install a Windows service, you must have administrator credentials on the computer on which you're installing it.</span></span>

1. <span data-ttu-id="4a52e-222">관리자 자격 증명을 사용하여 **Visual Studio에 대한 개발자 명령 프롬프트**를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-222">Open **Developer Command Prompt for Visual Studio** with administrative credentials.</span></span> <span data-ttu-id="4a52e-223">마우스를 사용하는 경우 Windows 시작 메뉴에서 **VS 2017에 대한 개발자 명령 프롬프트**를 마우스 오른쪽 단추로 클릭하고 **기타** > **관리자 권한으로 실행**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-223">If you’re using a mouse, right-click on **Developer Command Prompt for VS 2017** in the Windows Start menu, and then choose **More** > **Run as Administrator**.</span></span>

2. <span data-ttu-id="4a52e-224">**개발자 명령 프롬프트** 창에서 프로젝트의 출력이 포함된 폴더(기본적으로 프로젝트의 *\bin\Debug* 하위 디렉터리)로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-224">In the **Developer Command Prompt** window, navigate to the folder that contains your project's output (by default, it's the *\bin\Debug* subdirectory of your project).</span></span>

3. <span data-ttu-id="4a52e-225">다음 명령을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-225">Enter the following command:</span></span>

    ```shell
    installutil.exe MyNewService.exe
    ```

    <span data-ttu-id="4a52e-226">서비스를 성공적으로 설치한 경우 **installutil.exe**에서 설치에 성공했음을 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-226">If the service installs successfully, **installutil.exe** reports success.</span></span> <span data-ttu-id="4a52e-227">시스템에서 **InstallUtil.exe**를 찾을 수 없는 경우 해당 파일이 컴퓨터에 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-227">If the system could not find **InstallUtil.exe**, make sure that it exists on your computer.</span></span> <span data-ttu-id="4a52e-228">이 도구는 *%windir%\Microsoft.NET\Framework[64]\\[프레임워크 버전]* 폴더에 .NET Framework와 함께 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-228">This tool is installed with the .NET Framework to the folder *%windir%\Microsoft.NET\Framework[64]\\[framework version]*.</span></span> <span data-ttu-id="4a52e-229">예를 들어 32비트 버전의 기본 경로는 *%windir%\Microsoft.NET\Framework\v4.0.30319\InstallUtil.exe*입니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-229">For example, the default path for the 32-bit version is *%windir%\Microsoft.NET\Framework\v4.0.30319\InstallUtil.exe*.</span></span>

    <span data-ttu-id="4a52e-230">**Installutil.exe** 프로세스에서 실패를 보고하는 경우 설치 로그를 확인하여 이유를 찾아보세요.</span><span class="sxs-lookup"><span data-stu-id="4a52e-230">If the **installutil.exe** process reports failure, check the install log to find out why.</span></span> <span data-ttu-id="4a52e-231">기본적으로 로그는 서비스 실행 파일과 동일한 폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-231">By default the log is in the same folder as the service executable.</span></span> <span data-ttu-id="4a52e-232"><xref:System.ComponentModel.RunInstallerAttribute> 클래스가 `ProjectInstaller` 클래스에 없거나, 해당 특성이 **true**로 설정되지 않았거나, `ProjectInstaller` 클래스가 **public**으로 표시되지 않은 경우 설치에 실패할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-232">The installation can fail if  the <xref:System.ComponentModel.RunInstallerAttribute> Class is not present on the `ProjectInstaller` class, if the attribute is not set to **true**, or if the `ProjectInstaller` class is not marked **public**.</span></span>

<span data-ttu-id="4a52e-233">자세한 내용은 [How to: Install and Uninstall Services](../../../docs/framework/windows-services/how-to-install-and-uninstall-services.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4a52e-233">For more information, see [How to: Install and Uninstall Services](../../../docs/framework/windows-services/how-to-install-and-uninstall-services.md).</span></span>

## <a name="start-and-run-the-service"></a><span data-ttu-id="4a52e-234">서비스 시작 및 실행</span><span class="sxs-lookup"><span data-stu-id="4a52e-234">Start and run the service</span></span>

1. <span data-ttu-id="4a52e-235">Windows에서 **서비스** 데스크톱 앱을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-235">In Windows, open the **Services** desktop app.</span></span> <span data-ttu-id="4a52e-236">**Windows**+**R**을 눌러 **실행** 상자를 연 다음, **services.msc**를 입력하고 **Enter** 키를 누르거나 **확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-236">Press **Windows**+**R** to open the **Run** box, and then enter **services.msc** and press **Enter** or click **OK**.</span></span>

     <span data-ttu-id="4a52e-237">해당 서비스가 설정된 표시 이름의 사전순으로 **서비스**에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-237">You should see your service listed in **Services**, displayed alphabetically by the display name that you set for it.</span></span>

     ![서비스 창의 MyNewService입니다.](../../../docs/framework/windows-services/media/windowsservices-serviceswindow.PNG)

2. <span data-ttu-id="4a52e-239">**서비스**에서 서비스의 바로 가기 메뉴를 열고 **시작**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-239">In **Services**, open the shortcut menu for your service, and then choose **Start**.</span></span>

3. <span data-ttu-id="4a52e-240">서비스를 중지하려면 서비스의 바로 가기 메뉴를 열고 **중지**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-240">To stop the service, open the shortcut menu for the service, and then choose **Stop**.</span></span>

4. <span data-ttu-id="4a52e-241">(선택 사항) 명령줄에서 `net start ServiceName` 및 `net stop ServiceName` 명령을 사용하여 서비스를 시작하고 중지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-241">(Optional) From the command line, you can use the commands `net start ServiceName` and `net stop ServiceName` to start and stop your service.</span></span>

### <a name="verify-the-event-log-output-of-your-service"></a><span data-ttu-id="4a52e-242">서비스의 이벤트 로그 출력 확인</span><span class="sxs-lookup"><span data-stu-id="4a52e-242">Verify the event log output of your service</span></span>

1. <span data-ttu-id="4a52e-243">Windows 작업 표시줄의 검색 상자에 **이벤트 뷰어** 입력을 시작하고 검색 결과에서 **이벤트 뷰어**를 선택하여 **이벤트 뷰어**를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-243">Open **Event Viewer** by starting to type **Event Viewer** in the search box on the Windows task bar, and then selecting **Event Viewer** from the search results.</span></span>

   > [!TIP]
   > <span data-ttu-id="4a52e-244">Visual Studio에서 **서버 탐색기**를 열고(키보드: **Ctrl**+**Alt**+**S**) 로컬 컴퓨터의 **이벤트 로그** 노드를 확장하면 이벤트 로그에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-244">In Visual Studio, you can access event logs by opening **Server Explorer** (Keyboard: **Ctrl**+**Alt**+**S**) and expanding the **Event Logs** node for the local computer.</span></span>

2. <span data-ttu-id="4a52e-245">**이벤트 뷰어**에서 **응용 프로그램 및 서비스 로그**를 확장합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-245">In **Event Viewer**, expand **Applications and Services Logs**.</span></span>

3. <span data-ttu-id="4a52e-246">**MyNewLog**(또는 선택적 절차에 따라 명령줄 인수를 추가한 경우 **MyLogFile1**)의 목록을 찾아서 확장합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-246">Locate the listing for **MyNewLog** (or **MyLogFile1**, if you followed the optional procedure to add command-line arguments) and expand it.</span></span> <span data-ttu-id="4a52e-247">서비스에서 수행한 두 작업(시작 및 중지)의 항목이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-247">You should see entries for the two actions (start and stop) that your service performed.</span></span>

     ![이벤트 뷰어를 사용하여 이벤트 로그 항목 확인](../../../docs/framework/windows-services/media/windows-service-event-viewer.png)

## <a name="uninstall-the-service"></a><span data-ttu-id="4a52e-249">서비스 제거</span><span class="sxs-lookup"><span data-stu-id="4a52e-249">Uninstall the service</span></span>

1. <span data-ttu-id="4a52e-250">관리자 자격 증명을 사용하여 **Visual Studio에 대한 개발자 명령 프롬프트**를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-250">Open **Developer Command Prompt for Visual Studio** with administrative credentials.</span></span>

2. <span data-ttu-id="4a52e-251">명령 프롬프트 창에서 프로젝트의 출력이 포함된 폴더로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-251">In the command prompt window, navigate to the folder that contains your project's output.</span></span>

3. <span data-ttu-id="4a52e-252">다음 명령을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-252">Enter the following command:</span></span>

    ```shell
    installutil.exe /u MyNewService.exe
    ```

   <span data-ttu-id="4a52e-253">서비스를 성공적으로 제거한 경우 **installutil.exe**에서 서비스가 성공적으로 제거되었음을 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-253">If the service uninstalls successfully, **installutil.exe** reports that your service was successfully removed.</span></span> <span data-ttu-id="4a52e-254">자세한 내용은 [How to: Install and Uninstall Services](../../../docs/framework/windows-services/how-to-install-and-uninstall-services.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4a52e-254">For more information, see [How to: Install and Uninstall Services](../../../docs/framework/windows-services/how-to-install-and-uninstall-services.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="4a52e-255">다음 단계</span><span class="sxs-lookup"><span data-stu-id="4a52e-255">Next steps</span></span>

<span data-ttu-id="4a52e-256">이제 서비스가 만들어졌으므로, 다른 사용자가 Windows 서비스를 설치하는 데 사용할 수 있는 독립형 설치 프로그램을 만드는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-256">Now that you've created the service, you might want to create a standalone setup program that others can use to install your Windows service.</span></span> <span data-ttu-id="4a52e-257">ClickOnce는 Windows 서비스를 지원하지 않지만 [WiX Toolset](http://wixtoolset.org/)를 사용하여 Windows 서비스용 설치 관리자를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-257">ClickOnce doesn't support Windows services, but you can use the [WiX Toolset](http://wixtoolset.org/) to create an installer for a Windows service.</span></span> <span data-ttu-id="4a52e-258">다른 아이디어를 보려면 [설치 관리자 패키지 만들기](/visualstudio/deployment/deploying-applications-services-and-components#create-an-installer-package-windows-client)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4a52e-258">For other ideas, see [Create an installer package](/visualstudio/deployment/deploying-applications-services-and-components#create-an-installer-package-windows-client).</span></span>

<span data-ttu-id="4a52e-259">설치한 서비스에 명령을 보낼 수 있는 <xref:System.ServiceProcess.ServiceController> 구성 요소를 사용해 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-259">You might explore the use of a <xref:System.ServiceProcess.ServiceController> component, which enables you to send commands to the service you've installed.</span></span>

<span data-ttu-id="4a52e-260">이벤트 로그는 응용 프로그램이 실행될 때 만드는 것보다는 응용 프로그램이 설치될 때 설치 관리자를 사용하여 만드는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-260">You can use an installer to create an event log when the application is installed instead of creating the event log when the application runs.</span></span> <span data-ttu-id="4a52e-261">또한 이벤트 로그는 응용 프로그램이 제거되면 설치 관리자에 의해 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a52e-261">Additionally, the event log will be deleted by the installer when the application is uninstalled.</span></span> <span data-ttu-id="4a52e-262">자세한 내용은 <xref:System.Diagnostics.EventLogInstaller> 참조 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4a52e-262">For more information, see the <xref:System.Diagnostics.EventLogInstaller> reference page.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a52e-263">참고 항목</span><span class="sxs-lookup"><span data-stu-id="4a52e-263">See also</span></span>

- [<span data-ttu-id="4a52e-264">Windows 서비스 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="4a52e-264">Windows service applications</span></span>](../../../docs/framework/windows-services/index.md)
- [<span data-ttu-id="4a52e-265">Windows 서비스 응용 프로그램 소개</span><span class="sxs-lookup"><span data-stu-id="4a52e-265">Introduction to Windows service applications</span></span>](../../../docs/framework/windows-services/introduction-to-windows-service-applications.md)
- [<span data-ttu-id="4a52e-266">방법: Windows 서비스 응용 프로그램 디버그</span><span class="sxs-lookup"><span data-stu-id="4a52e-266">How to: Debug Windows service applications</span></span>](../../../docs/framework/windows-services/how-to-debug-windows-service-applications.md)
- <span data-ttu-id="4a52e-267">[Services (Windows)](https://msdn.microsoft.com/library/windows/desktop/ms685141.aspx)(서비스(Windows))</span><span class="sxs-lookup"><span data-stu-id="4a52e-267">[Services (Windows)](https://msdn.microsoft.com/library/windows/desktop/ms685141.aspx)</span></span>
