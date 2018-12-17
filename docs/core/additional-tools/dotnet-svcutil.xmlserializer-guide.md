# <a name="using-dotnet-svcutilxmlserializer-on-net-core"></a><span data-ttu-id="47a9f-101">.NET Core에서 dotnet-svcutil.xmlserializer 사용</span><span class="sxs-lookup"><span data-stu-id="47a9f-101">Using dotnet-svcutil.xmlserializer on .NET Core</span></span>

## <a name="prerequisites"></a><span data-ttu-id="47a9f-102">전제 조건</span><span class="sxs-lookup"><span data-stu-id="47a9f-102">Prerequisites</span></span>

<span data-ttu-id="47a9f-103">dotnet-svcutil.xmlserializer가 작동하려면 다음이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="47a9f-103">The following is required for dotnet-svcutil.xmlserializer to work.</span></span> 

* [<span data-ttu-id="47a9f-104">.NET Core 2.1 SDK 이상</span><span class="sxs-lookup"><span data-stu-id="47a9f-104">.NET Core 2.1 SDK or later</span></span>](https://www.microsoft.com/net/download/dotnet-core/sdk-2.1.300)
* [<span data-ttu-id="47a9f-105">.NET Core 런타임 2.1 이상</span><span class="sxs-lookup"><span data-stu-id="47a9f-105">.NET Core Runtime 2.1 or later</span></span>](https://www.microsoft.com/net/download/dotnet-core/runtime-2.1.0)

<span data-ttu-id="47a9f-106">`dotnet --info` 명령을 사용하여 이미 설치한 .NET Core SDK 및 런타임 버전을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47a9f-106">You can use the command `dotnet --info` to check which versions of .NET Core SDK and runtime you already have installed.</span></span>

<span data-ttu-id="47a9f-107">.NET Core 콘솔 애플리케이션에서 dotnet-svcutil.xmlserializer를 사용하려면</span><span class="sxs-lookup"><span data-stu-id="47a9f-107">To use dotnet-svcutil.xmlserializer in a .NET Core console application:</span></span>

1. <span data-ttu-id="47a9f-108">.NET Framework에서 기본 템플릿 ‘WCF 서비스 애플리케이션’을 사용하여 ‘MyWCFService’라는 WCF 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="47a9f-108">Create a WCF Service named 'MyWCFService' using the default template 'WCF Service Application' in .NET Framework.</span></span>  <span data-ttu-id="47a9f-109">다음과 같이 서비스 메서드에 ```[XmlSerializerFormat]``` 특성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="47a9f-109">Add ```[XmlSerializerFormat]``` attribute on the service method like the following</span></span>
    ```c#
    [ServiceContract]
    public interface IService1
    {
        [XmlSerializerFormat]
        [OperationContract(Action = "http://tempuri.org/IService1/GetData", ReplyAction = "http://tempuri.org/IService1/GetDataResponse")]
        string GetData(int value);
    }
    ```
2. <span data-ttu-id="47a9f-110">netcoreapp 2.1을 대상으로 하는 WCF 클라이언트 애플리케이션으로 .NET Core 콘솔 애플리케이션을 만듭니다. 예를 들어 다음 명령을 사용하여 ‘MyWCFClient’라는 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="47a9f-110">Create a .NET Core console application as WCF client application that targets at netcoreapp 2.1, e.g. create an app named 'MyWCFClient' with the command,</span></span>
    ```
    dotnet new console --name MyWCFClient
    ```
    <span data-ttu-id="47a9f-111">csproj가 netcoreapp 2.1을 대상으로 하는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="47a9f-111">Make sure your csproj targets a netcoreapp 2.1.</span></span> <span data-ttu-id="47a9f-112">.csproj 파일에서 다음 XML 요소를 사용하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47a9f-112">This is done using the following XML element in your .csproj file</span></span>
    ```xml
    <TargetFramework>netcoreapp2.1</TargetFramework>
    ```
3. <span data-ttu-id="47a9f-113">다음 명령을 실행하여 System.ServiceModel.Http에 대한 패키지 참조를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="47a9f-113">Add a package reference to System.ServiceModel.Http by running the following command:</span></span>
   
   ```dotnet add package System.ServiceModel.Http -v 4.5.0```

4. <span data-ttu-id="47a9f-114">WCF 클라이언트 코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="47a9f-114">Add the WCF Client code:</span></span>
    ```csharp
    using System.ServiceModel;
    
    class Program
    {
        static void Main(string[] args)
        {
            var myBinding = new BasicHttpBinding();
            var myEndpoint = new EndpointAddress("http://localhost:2561/Service1.svc"); //Fill your service url here
            var myChannelFactory = new ChannelFactory<IService1>(myBinding, myEndpoint);
            IService1 client = myChannelFactory.CreateChannel();
            string s = client.GetData(1);
            ((ICommunicationObject)client).Close();
        }
    }

    [ServiceContract]
    public interface IService1
    {
        [XmlSerializerFormat]
        [OperationContract(Action = "http://tempuri.org/IService1/GetData", ReplyAction = "http://tempuri.org/IService1/GetDataResponse")]
        string GetData(int value);
    }
    ```
5. <span data-ttu-id="47a9f-115">.csproj 파일을 편집하고 dotnet-svcutil.xmlserializer 패키지에 대한 참조를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="47a9f-115">Edit the .csproj file and add a reference to the dotnet-svcutil.xmlserializer package.</span></span> <span data-ttu-id="47a9f-116">예:</span><span class="sxs-lookup"><span data-stu-id="47a9f-116">For example:</span></span>

    <span data-ttu-id="47a9f-117">i.</span><span class="sxs-lookup"><span data-stu-id="47a9f-117">i.</span></span> <span data-ttu-id="47a9f-118">`dotnet add package dotnet-svcutil.xmlserializer -v 1.0.0` 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="47a9f-118">Run command: `dotnet add package dotnet-svcutil.xmlserializer -v 1.0.0`</span></span>

    <span data-ttu-id="47a9f-119">ii.</span><span class="sxs-lookup"><span data-stu-id="47a9f-119">ii.</span></span> <span data-ttu-id="47a9f-120">MyWCFClient.csproj에 다음 줄을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="47a9f-120">Add the following lines in MyWCFClient.csproj,</span></span>
    ```xml
    <ItemGroup>
      <DotNetCliToolReference Include="dotnet-svcutil.xmlserializer" Version="1.0.0" />
    </ItemGroup>
    ```

6. <span data-ttu-id="47a9f-121">`dotnet build`를 실행하여 애플리케이션을 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="47a9f-121">Build the application by running `dotnet build`.</span></span> <span data-ttu-id="47a9f-122">모든 항목이 성공하면 MyWCFClient.XmlSerializers.dll이라는 어셈블리가 출력 폴더에 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="47a9f-122">If everything succeeds, an assembly named MyWCFClient.XmlSerializers.dll will be generated in the output folder.</span></span> <span data-ttu-id="47a9f-123">도구가 어셈블리 생성에 실패할 경우 빌드 출력에 경고가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="47a9f-123">You will see warnings in the build output if the tool failed to generate the assembly.</span></span>

7. <span data-ttu-id="47a9f-124">브라우저에서 http://localhost:2561/Service1.svc를 실행하여 WCF 서비스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="47a9f-124">Start the WCF service e.g. by running http://localhost:2561/Service1.svc in the browser.</span></span> <span data-ttu-id="47a9f-125">그런 다음, 클라이언트 애플리케이션을 시작하면 미리 생성된 직렬 변환기가 런타임 시 자동으로 로드되어 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="47a9f-125">Then start the client application, and it will automatically load and use the pre-generated serializers at runtime.</span></span>
