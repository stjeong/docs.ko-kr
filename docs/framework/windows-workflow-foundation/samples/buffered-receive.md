---
title: 버퍼링되는 수신
ms.date: 03/30/2017
ms.assetid: 9d46d9b9-96c9-4531-9695-ab526b4d704a
ms.openlocfilehash: b95577c71493275f30703b4366fab32a51097bd2
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43526806"
---
# <a name="buffered-receive"></a><span data-ttu-id="729c2-102">버퍼링되는 수신</span><span class="sxs-lookup"><span data-stu-id="729c2-102">Buffered Receive</span></span>
<span data-ttu-id="729c2-103">이 샘플에는 설정 하 고 버퍼링된 된 수신 기능에서 Windows WF (Workflow Foundation)를 구성 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-103">This sample demonstrates how to set up and configure the buffered receive feature in Windows Workflow Foundation (WF).</span></span> <span data-ttu-id="729c2-104">버퍼링된 수신 기능을 사용하면 워크플로 작성자가 메시지의 수신 순서에 신경을 쓰지 않고 워크플로를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-104">Buffered receive allows the workflow author to create a workflow without having to worry about the order in which messages are received.</span></span> <span data-ttu-id="729c2-105">버퍼링된 수신 기능은 메시지를 로컬로 버퍼링하고 워크플로에서 메시지를 받을 준비가 되었을 때 이를 전달하는 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-105">The buffered receive feature buffers messages locally and delivers them when the workflow is ready to receive them.</span></span>  
  
## <a name="demonstrates"></a><span data-ttu-id="729c2-106">세부 항목</span><span class="sxs-lookup"><span data-stu-id="729c2-106">Demonstrates</span></span>  
 <span data-ttu-id="729c2-107">메시징 활동에 버퍼링된 수신 기능을 사용하여 순서에 상관없이 메시지 처리</span><span class="sxs-lookup"><span data-stu-id="729c2-107">Out-of-order message processing using buffered receive with messaging activities.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="729c2-108">컴퓨터에 이 샘플이 이미 설치되어 있을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-108">The samples may already be installed on your machine.</span></span> <span data-ttu-id="729c2-109">계속하기 전에 다음(기본) 디렉터리를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="729c2-109">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="729c2-110">이 디렉터리가 없으면로 이동 [Windows Communication Foundation (WCF) 및.NET Framework 4 용 Windows WF (Workflow Foundation) 샘플](https://go.microsoft.com/fwlink/?LinkId=150780) 모든 Windows Communication Foundation (WCF)를 다운로드 하 고 [!INCLUDE[wf1](../../../../includes/wf1-md.md)] 샘플.</span><span class="sxs-lookup"><span data-stu-id="729c2-110">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="729c2-111">이 샘플은 다음 디렉터리에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-111">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\BufferedReceive`  
  
## <a name="discussion"></a><span data-ttu-id="729c2-112">토론</span><span class="sxs-lookup"><span data-stu-id="729c2-112">Discussion</span></span>  
 <span data-ttu-id="729c2-113">이 샘플에서는 Windows Communication Foundation (WCF) 서비스를 사용 하 여 구현 됩니다 [!INCLUDE[wf1](../../../../includes/wf1-md.md)] 시퀀스로 있고 <xref:System.ServiceModel.Activities.Receive> 활동입니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-113">In this sample, a Windows Communication Foundation (WCF) service is implemented using [!INCLUDE[wf1](../../../../includes/wf1-md.md)] and has a sequence of <xref:System.ServiceModel.Activities.Receive> activities.</span></span> <span data-ttu-id="729c2-114">이 워크플로는 간단한 대출 승인 프로세스를 모델링하며, 승인 여부를 결정해야 할 대출에 대한 알림 세 건을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-114">This workflow models a simple loan approval process where the workflow expects three notifications for a loan to be approved.</span></span> <span data-ttu-id="729c2-115">Windows Communication Foundation (WCF) 클라이언트 응용 프로그램 서비스에서 예상의 역순으로 알림 세 건된을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-115">A Windows Communication Foundation (WCF) client application sends three correlated notifications in the reverse order of what the service expects.</span></span> <span data-ttu-id="729c2-116">그러나 이 서비스에서는 버퍼링된 수신 기능을 사용하므로 순서가 맞지 않는 각 메시지를 버퍼링한 후 워크플로에서 해당 메시지를 받을 준비가 되었을 때 이를 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-116">Because the buffered receive feature is turned on at the service, each out-of-order message is buffered at the service and processed as the workflow becomes ready to receive it.</span></span>  
  
 <span data-ttu-id="729c2-117">버퍼링된 수신 기능을 사용하려면 바인딩을 통해 <xref:System.ServiceModel.Activities.ReceiveContent>가 지원되어야 하므로 이 서비스에서는 <xref:System.ServiceModel.NetMsmqBinding>을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-117">The buffered receive feature requires <xref:System.ServiceModel.Activities.ReceiveContent> support from the binding, therefore the service uses <xref:System.ServiceModel.NetMsmqBinding>.</span></span> <span data-ttu-id="729c2-118">이 바인딩에는 특별한 구성이 필요하지 않으므로 기본 설정이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-118">No special configuration is required for the binding, so the defaults are used.</span></span>  
  
```xml  
<endpoint address ="net.msmq://localhost/private/LoanService/Service1.xamlx"  
                  binding="netMsmqBinding"  
                  contract="ILoanService"/>  
```  
  
 <span data-ttu-id="729c2-119">이 서비스에서는 <xref:System.ServiceModel.Description.ServiceMetadataBehavior>를 사용하여 서비스에 대한 메타데이터도 노출합니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-119">The service also exposes metadata for the service using <xref:System.ServiceModel.Description.ServiceMetadataBehavior>.</span></span>  
  
 <span data-ttu-id="729c2-120">마찬가지로, 클라이언트 엔드포인트는 <xref:System.ServiceModel.NetMsmqBinding>을 사용하여 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-120">Similarly, the client endpoint is configured using <xref:System.ServiceModel.NetMsmqBinding>.</span></span> <span data-ttu-id="729c2-121">클라이언트 코드 및 구성을 사용 하 여 생성 되는 **서비스 참조 추가** Visual Studio의 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-121">The client code and configuration is generated by using the **Add Service Reference** feature of Visual Studio.</span></span> <span data-ttu-id="729c2-122">다음 예제에서는 App.config 파일에 생성된 클라이언트 엔드포인트를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-122">The following example is the generated client endpoint in the App.config file.</span></span>  
  
```xml  
<endpoint address="net.msmq://localhost/private/LoanService/Service1.xamlx"  
                binding="netMsmqBinding" bindingConfiguration="NetMsmqBinding_ILoanService"  
                contract="ServiceReference1.ILoanService" name="NetMsmqBinding_ILoanService" />  
```  
  
 <span data-ttu-id="729c2-123">이 샘플에는 다음과 같은 Windows 구성 요소를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-123">This sample requires that the following Windows components are enabled:</span></span>  
  
1.  [!INCLUDE[iis60](../../../../includes/iis60-md.md)]  
  
2.  [!INCLUDE[iis60](../../../../includes/iis60-md.md)]<span data-ttu-id="729c2-124"> 관리 호환성, 메타베이스 및 구성 호환성</span><span class="sxs-lookup"><span data-stu-id="729c2-124"> Management Compatibility, Metabase, and Configuration Compatibility</span></span>  
  
3.  <span data-ttu-id="729c2-125">World Wide Web 서비스, 응용 프로그램 개발 기능 및 ASP.NET</span><span class="sxs-lookup"><span data-stu-id="729c2-125">World Wide Web Services, Application Development Features, and ASP.NET</span></span>  
  
4.  <span data-ttu-id="729c2-126">MSMQ(Microsoft Message Queue) Server</span><span class="sxs-lookup"><span data-stu-id="729c2-126">Microsoft Message Queues (MSMQ) Server</span></span>  
  
#### <a name="to-set-up-and-build-the-sample"></a><span data-ttu-id="729c2-127">샘플을 설치하고 빌드하려면</span><span class="sxs-lookup"><span data-stu-id="729c2-127">To set up, and build the sample</span></span>  
  
1.  <span data-ttu-id="729c2-128">[!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] 명령 프롬프트에서 `aspnet_regiis –I`을 입력하여 ASP.NET을 등록하고 Enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-128">At a [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] command prompt, register ASP.NET by typing `aspnet_regiis –I` and press ENTER.</span></span>  
  
2.  <span data-ttu-id="729c2-129">관리자 권한으로 [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-129">Run [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] as an Administrator.</span></span>  
  
3.  <span data-ttu-id="729c2-130">LoanService.sln을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-130">Open LoanService.sln.</span></span>  
  
4.  <span data-ttu-id="729c2-131">LoanService 프로젝트에 대 한 가상 디렉터리를 만들려면 하려는 경우 선택 하는 메시지가 표시 되 면 **예**합니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-131">When asked if you would like to create the virtual directories for the LoanService project, select **Yes**.</span></span>  
  
#### <a name="to-set-up-the-service-queues"></a><span data-ttu-id="729c2-132">서비스 큐를 설정하려면</span><span class="sxs-lookup"><span data-stu-id="729c2-132">To set up the service queues</span></span>  
  
1.  <span data-ttu-id="729c2-133">F5 키를 눌러 LoanClient 응용 프로그램을 실행합니다. 이 응용 프로그램은 큐를 만들고 Service1.xamlx에 정의되어 있는 서비스를 활성화하는 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-133">Press F5 to run the LoanClient application that creates the queues and activates the service defined in Service1.xamlx.</span></span>  
  
2.  <span data-ttu-id="729c2-134">엽니다는 **컴퓨터 관리** 명령 프롬프트에서 Compmgmt.msc를 실행 하 여 콘솔.</span><span class="sxs-lookup"><span data-stu-id="729c2-134">Open the **Computer Management** console by running Compmgmt.msc from a command prompt.</span></span>  
  
3.  <span data-ttu-id="729c2-135">에 **컴퓨터 관리** 콘솔에서 **Service**를 **응용 프로그램**, **메시지 큐**, **개인 큐** .</span><span class="sxs-lookup"><span data-stu-id="729c2-135">In the **Computer Management** console, expand **Service**, **Applications**, **Message Queuing**, **Private Queues**.</span></span>  
  
4.  <span data-ttu-id="729c2-136">Loanservice/service1.xamlx 큐를 마우스 오른쪽 단추로 클릭 **속성**합니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-136">Right-click the loanservice/service1.xamlx queue and select **Properties**.</span></span>  
  
5.  <span data-ttu-id="729c2-137">선택 된 **보안** 탭을 추가 **누구나 메시지 받기**를 **메시지 보기** 및 **메시지 보내기** 권한.</span><span class="sxs-lookup"><span data-stu-id="729c2-137">Select the **Security** tab, and add **Everyone Receives Message**, **Peek Message** and **Send Message** permissions.</span></span>  
  
6.  <span data-ttu-id="729c2-138">[!INCLUDE[iis60](../../../../includes/iis60-md.md)] 관리자를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-138">Open the [!INCLUDE[iis60](../../../../includes/iis60-md.md)] Manager.</span></span>  
  
7.  <span data-ttu-id="729c2-139">이동할 **서버**, **사이트**, **Default Web site**, **개인**, **LoanService** 선택 **고급 옵션**</span><span class="sxs-lookup"><span data-stu-id="729c2-139">Browse to **Server**, **Sites**, **Default Web site**, **Private**, **LoanService** and select **Advanced Options**</span></span>  
  
8.  <span data-ttu-id="729c2-140">변경 된 **사용할 수 있는 프로토콜** 되도록 **http**를 **net.msmq**합니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-140">Change the **Enabled Protocols** to be **http**, **net.msmq**.</span></span>  
  
#### <a name="to-run-the-sample"></a><span data-ttu-id="729c2-141">이 샘플을 실행하려면</span><span class="sxs-lookup"><span data-stu-id="729c2-141">To run the sample</span></span>  
  
1.  <span data-ttu-id="729c2-142">이동할 http://localhost/private/loanservice/service1.xamlx 서비스가 실행 되 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-142">Browse to http://localhost/private/loanservice/service1.xamlx to ensure that the service is running.</span></span>  
  
2.  <span data-ttu-id="729c2-143">F5 키를 눌러 LoanClient 응용 프로그램을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-143">Press F5 to run the LoanClient application.</span></span> <span data-ttu-id="729c2-144">워크플로를 완료하면 메시지 교환 결과가 포함된 out.txt 파일이 C:\Inbox에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-144">Once the workflow is complete, an out.txt file should be saved to C:\Inbox that contains the result of the message exchange.</span></span>  
  
#### <a name="to-clean-up"></a><span data-ttu-id="729c2-145">정리하려면</span><span class="sxs-lookup"><span data-stu-id="729c2-145">To clean up</span></span>  
  
1.  <span data-ttu-id="729c2-146">엽니다는 **컴퓨터 관리** 명령 프롬프트에서 Compmgmt.msc를 실행 하 여 콘솔.</span><span class="sxs-lookup"><span data-stu-id="729c2-146">Open the **Computer Management** console by running Compmgmt.msc from a command prompt.</span></span>  
  
2.  <span data-ttu-id="729c2-147">확장 **서비스** 하 고 **응용 프로그램**를 **메시지 큐**를 **개인 큐**합니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-147">Expand **Service** and **Applications**, **Message Queuing**, **Private Queues**.</span></span>  
  
3.  <span data-ttu-id="729c2-148">loanservice/service1.xamlx 큐를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-148">Delete the loanservice/service1.xamlx queue.</span></span>  
  
4.  <span data-ttu-id="729c2-149">C:\Inbox 디렉터리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-149">Remove the C:\Inbox directory.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="729c2-150">컴퓨터에 이 샘플이 이미 설치되어 있을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-150">The samples may already be installed on your machine.</span></span> <span data-ttu-id="729c2-151">계속하기 전에 다음(기본) 디렉터리를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="729c2-151">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="729c2-152">이 디렉터리가 없으면로 이동 [Windows Communication Foundation (WCF) 및.NET Framework 4 용 Windows WF (Workflow Foundation) 샘플](https://go.microsoft.com/fwlink/?LinkId=150780) 모든 Windows Communication Foundation (WCF)를 다운로드 하 고 [!INCLUDE[wf1](../../../../includes/wf1-md.md)] 샘플.</span><span class="sxs-lookup"><span data-stu-id="729c2-152">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="729c2-153">이 샘플은 다음 디렉터리에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="729c2-153">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\BufferedReceive`
