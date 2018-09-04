---
title: Windows용 WCF 서비스 및 이벤트 추척
ms.date: 03/30/2017
ms.assetid: eda4355d-0bd0-4dc9-80a2-d2c832152272
ms.openlocfilehash: 11f476b966886d4a114f7870b4c029e200ee84e0
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43504774"
---
# <a name="wcf-services-and-event-tracing-for-windows"></a><span data-ttu-id="d2014-102">Windows용 WCF 서비스 및 이벤트 추척</span><span class="sxs-lookup"><span data-stu-id="d2014-102">WCF Services and Event Tracing for Windows</span></span>
<span data-ttu-id="d2014-103">이 샘플에서 이벤트 추적에 대 한 Windows (ETW) 이벤트를 내보내는 분석 추적을 Windows Communication Foundation (WCF)를 사용 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-103">This sample demonstrates how to use the analytic tracing in Windows Communication Foundation (WCF) to emit events in Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="d2014-104">분석 추적은 프로덕션 환경에서 WCF 서비스의 문제를 해결할 수 있는 WCF 스택의 주요 지점에서 내보내는 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-104">The analytic traces are events emitted at key points in the WCF stack that allow troubleshooting of WCF services in production environment.</span></span>  
  
 <span data-ttu-id="d2014-105">WCF 서비스의 분석 추적은 추적을 켤 수 있지만 프로덕션 환경에서 성능에 미치는 영향이 최소화 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-105">Analytic trace in WCF services is tracing that can be turned on in a production environment with minimal impact on performance.</span></span> <span data-ttu-id="d2014-106">이러한 추적은 ETW 세션에 이벤트로 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-106">These traces are emitted as events to an ETW session.</span></span>  
  
 <span data-ttu-id="d2014-107">이 샘플 이벤트 뷰어를 사용 하 여 볼 수 있는 이벤트 로그에 이벤트 서비스에서 내보낸 된 기본적인 WCF 서비스를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-107">This sample includes a basic WCF service in which events are emitted from the service to the event log, which can be viewed using Event Viewer.</span></span> <span data-ttu-id="d2014-108">WCF 서비스에서 이벤트를 수신 하는 전용된 ETW 세션을 시작 하는 것도 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-108">It is also possible to start a dedicated ETW session that listens for events from the WCF service.</span></span> <span data-ttu-id="d2014-109">이 샘플에는 이벤트 뷰어를 사용하여 읽을 수 있는 이진 파일에 이벤트를 저장하는 전용 ETW 세션을 만드는 스크립트가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-109">The sample includes a script to create a dedicated ETW session that stores events in a binary file that can be read using Event Viewer.</span></span>  
  
#### <a name="to-use-this-sample"></a><span data-ttu-id="d2014-110">이 샘플을 사용하려면</span><span class="sxs-lookup"><span data-stu-id="d2014-110">To use this sample</span></span>  
  
1.  <span data-ttu-id="d2014-111">[!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)]에서 EtwAnalyticTraceSample.sln 솔루션 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-111">Using [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], open the EtwAnalyticTraceSample.sln solution file.</span></span>  
  
2.  <span data-ttu-id="d2014-112">Ctrl+Shift+B를 눌러 솔루션을 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-112">To build the solution, press CTRL+SHIFT+B.</span></span>  
  
3.  <span data-ttu-id="d2014-113">Ctrl+F5를 눌러 솔루션을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-113">To run the solution, press CTRL+F5.</span></span>  
  
     <span data-ttu-id="d2014-114">웹 브라우저에서 클릭 **Calculator.svc**합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-114">In the Web browser, click **Calculator.svc**.</span></span> <span data-ttu-id="d2014-115">서비스의 WSDL 문서에 대한 URI가 브라우저에 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-115">The URI of the WSDL document for the service should appear in the browser.</span></span> <span data-ttu-id="d2014-116">이 URI를 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-116">Copy that URI.</span></span>  
  
     <span data-ttu-id="d2014-117">기본적으로 서비스 1378 포트에서 요청 수신을 시작 (http://localhost:1378/Calculator.svc)합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-117">By default, the service starts listening for requests on port 1378 (http://localhost:1378/Calculator.svc).</span></span>  
  
4.  <span data-ttu-id="d2014-118">WCF 테스트 클라이언트 (WcfTestClient.exe)를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-118">Run the WCF test client (WcfTestClient.exe).</span></span>  
  
     <span data-ttu-id="d2014-119">WCF 테스트 클라이언트 (WcfTestClient.exe)에 \< [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] Install > WcfTestClient.exe \Common7\IDE\ (기본 [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] 설치 디렉터리는 C:\Program Files\Microsoft Visual Studio 10.0).</span><span class="sxs-lookup"><span data-stu-id="d2014-119">The WCF test client (WcfTestClient.exe) is located in the \<[!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] Install Dir>\Common7\IDE\ WcfTestClient.exe (default [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] install dir is C:\Program Files\Microsoft Visual Studio 10.0).</span></span>  
  
5.  <span data-ttu-id="d2014-120">WCF 테스트 클라이언트 내에서 선택 하 여 서비스를 추가할 **파일**를 차례로 **서비스 추가**합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-120">Within the WCF test client, add the service by selecting **File**, and then **Add Service**.</span></span>  
  
     <span data-ttu-id="d2014-121">입력 상자에 엔드포인트 주소를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-121">Add the endpoint address in the input box.</span></span> <span data-ttu-id="d2014-122">기본값은 http://localhost:1378/Calculator.svc입니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-122">The default is http://localhost:1378/Calculator.svc.</span></span>  
  
6.  <span data-ttu-id="d2014-123">이벤트 뷰어 응용 프로그램을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-123">Open the Event Viewer application.</span></span>  
  
     <span data-ttu-id="d2014-124">서비스를 호출 하기 전에 이벤트 뷰어를 시작 하 고 WCF 서비스에서 내보낸 추적 이벤트에 대 한 이벤트 로그에서이 수신 대기 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-124">Before invoking the service, start Event Viewer and ensure that the event log is listening for tracking events emitted from the WCF service.</span></span>  
  
7.  <span data-ttu-id="d2014-125">**시작** 메뉴에서 **관리 도구**를 차례로 **이벤트 뷰어**합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-125">From the **Start** menu, select **Administrative Tools**, and then **Event Viewer**.</span></span>  <span data-ttu-id="d2014-126">사용 하도록 설정 합니다 **분석** 하 고 **디버그** 로그 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-126">Enable the **Analytic** and **Debug** logs.</span></span>  
  
8.  <span data-ttu-id="d2014-127">이동할 이벤트 뷰어의 트리 뷰에서 **이벤트 뷰어**, **Applications and Services Logs**를 **Microsoft**를 **Windows**, 한 다음 **응용 프로그램 서버-응용 프로그램**합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-127">In the tree view in Event Viewer, navigate to **Event Viewer**, **Applications and Services Logs**, **Microsoft**, **Windows**, and then **Application Server-Applications**.</span></span> <span data-ttu-id="d2014-128">마우스 오른쪽 단추로 클릭 **응용 프로그램 서버-응용 프로그램**를 선택 **뷰**를 차례로 **분석 및 디버그 로그 표시**합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-128">Right-click **Application Server-Applications**, select **View**, and then **Show Analytic and Debug Logs**.</span></span>  
  
     <span data-ttu-id="d2014-129">있는지 확인 합니다 **분석 및 디버그 로그 표시** 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-129">Ensure that the **Show Analytic and Debug Logs** option is checked.</span></span>  
  
9. <span data-ttu-id="d2014-130">사용 하도록 설정 합니다 **분석** 로그 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-130">Enable the **Analytic** log.</span></span>  
  
     <span data-ttu-id="d2014-131">이동할 이벤트 뷰어의 트리 뷰에서 **이벤트 뷰어**, **Applications and Services Logs**를 **Microsoft**를 **Windows**, 한 다음 **응용 프로그램 서버-응용 프로그램**합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-131">In the tree view in Event Viewer, navigate to **Event Viewer**, **Applications and Services Logs**, **Microsoft**, **Windows**, and then **Application Server-Applications**.</span></span> <span data-ttu-id="d2014-132">마우스 오른쪽 단추로 클릭 **분석** 선택한 **로그 사용**합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-132">Right-click **Analytic** and select **Enable Log**.</span></span>  
  
#### <a name="to-test-the-service"></a><span data-ttu-id="d2014-133">서비스를 테스트하려면</span><span class="sxs-lookup"><span data-stu-id="d2014-133">To test the service</span></span>  
  
1.  <span data-ttu-id="d2014-134">WCF 테스트 클라이언트를 다시 전환 하 고 두 번 클릭 `Divide` 0의 분모를 지정 하는 기본값을 그대로 유지 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-134">Switch back to WCF test client and double-click `Divide` and keep the default values, which specify a denominator of 0.</span></span>  
  
     <span data-ttu-id="d2014-135">분모가 0이면 서비스에서는 오류를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-135">If the denominator is 0, then the service throws a fault.</span></span>  
  
2.  <span data-ttu-id="d2014-136">서비스에서 내보낸 이벤트를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-136">Observe the events emitted from the service.</span></span>  
  
     <span data-ttu-id="d2014-137">이벤트 뷰어로 다시 전환 하 고 이동할 **이벤트 뷰어**를 **Applications and Services Logs**를 **Microsoft**를 **Windows**, 고 **응용 프로그램 서버-응용 프로그램**합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-137">Switch back to Event Viewer and navigate to **Event Viewer**, **Applications and Services Logs**, **Microsoft**, **Windows**, and then **Application Server-Applications**.</span></span> <span data-ttu-id="d2014-138">마우스 오른쪽 단추로 클릭 **분석** 선택한 **새로 고침**합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-138">Right-click **Analytic** and select **Refresh**.</span></span>  
  
     <span data-ttu-id="d2014-139">WCF 분석 추적 이벤트가 이벤트 뷰어에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-139">The WCF analytic trace events are displayed in the event viewer.</span></span> <span data-ttu-id="d2014-140">서비스에서 오류가 throw되었으므로 이벤트 뷰어에 오류 추적 이벤트가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-140">Notice that because a fault was thrown by the service an error trace event is displayed in the event viewer.</span></span>  
  
3.  <span data-ttu-id="d2014-141">1-2단계를 반복하되 이번에는 유효한 입력을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-141">Repeat steps 1 and 2, but with valid inputs.</span></span> <span data-ttu-id="d2014-142">`N2` 매개 변수 값으로는 0 이외의 모든 숫자를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-142">The value of the `N2` parameter can be any number other than 0.</span></span>  
  
     <span data-ttu-id="d2014-143">분석 채널을 새로 고쳐 WCF 이벤트에 오류 이벤트가 포함되어 있지 않은지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-143">Refresh the analytic channel to view the WCF events do not include any error events.</span></span>  
  
 <span data-ttu-id="d2014-144">이 샘플에서는 WCF 서비스에서 내보낸 분석 추적 이벤트를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-144">The sample demonstrates the analytic trace events emitted from a WCF service.</span></span>  
  
#### <a name="to-cleanup-optional"></a><span data-ttu-id="d2014-145">정리하려면(옵션)</span><span class="sxs-lookup"><span data-stu-id="d2014-145">To cleanup (Optional)</span></span>  
  
1.  <span data-ttu-id="d2014-146">이벤트 뷰어를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-146">Open Event Viewer.</span></span>  
  
2.  <span data-ttu-id="d2014-147">이동할 **이벤트 뷰어**를 **Applications and Services Logs**를 **Microsoft**를 **Windows**를 차례로  **응용 프로그램 서버-응용 프로그램**합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-147">Navigate to **Event Viewer**, **Applications and Services Logs**, **Microsoft**, **Windows**, and then **Application-Server-Applications**.</span></span> <span data-ttu-id="d2014-148">마우스 오른쪽 단추로 클릭 **분석** 선택한 **로그 사용 안 함**합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-148">Right-click **Analytic** and select **Disable Log**.</span></span>  
  
3.  <span data-ttu-id="d2014-149">이동할 **이벤트 뷰어**를 **Applications and Services Logs**를 **Microsoft**를 **Windows**를 차례로  **응용 프로그램 서버-응용 프로그램**합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-149">Navigate to **Event Viewer**, **Applications and Services Logs**, **Microsoft**, **Windows**, and then **Application-Server-Applications**.</span></span> <span data-ttu-id="d2014-150">마우스 오른쪽 단추로 클릭 **분석** 선택한 **로그 지우기**합니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-150">Right-click **Analytic** and select **Clear Log**.</span></span>  
  
4.  <span data-ttu-id="d2014-151">선택 된 **의 선택을 취소** 이벤트를 지우려면 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-151">Choose the **Clear** option to clear the events.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="d2014-152">컴퓨터에 이 샘플이 이미 설치되어 있을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-152">The samples may already be installed on your computer.</span></span> <span data-ttu-id="d2014-153">계속하기 전에 다음(기본) 디렉터리를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="d2014-153">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="d2014-154">이 디렉터리가 없으면로 이동 [Windows Communication Foundation (WCF) 및.NET Framework 4 용 Windows WF (Workflow Foundation) 샘플](https://go.microsoft.com/fwlink/?LinkId=150780) 모든 Windows Communication Foundation (WCF)를 다운로드 하 고 [!INCLUDE[wf1](../../../../includes/wf1-md.md)] 샘플.</span><span class="sxs-lookup"><span data-stu-id="d2014-154">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="d2014-155">이 샘플은 다음 디렉터리에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2014-155">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Management\ETWTracing`  
  
## <a name="see-also"></a><span data-ttu-id="d2014-156">참고 항목</span><span class="sxs-lookup"><span data-stu-id="d2014-156">See Also</span></span>  
 [<span data-ttu-id="d2014-157">AppFabric 모니터링 샘플</span><span class="sxs-lookup"><span data-stu-id="d2014-157">AppFabric Monitoring Samples</span></span>](https://go.microsoft.com/fwlink/?LinkId=193959)
