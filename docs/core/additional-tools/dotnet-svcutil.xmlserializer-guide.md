# <a name="using-dotnet-svcutilxmlserializer-on-net-core"></a>.NET Core에서 dotnet-svcutil.xmlserializer 사용

## <a name="prerequisites"></a>전제 조건

dotnet-svcutil.xmlserializer가 작동하려면 다음이 필요합니다. 

* [.NET Core 2.1 SDK 이상](https://www.microsoft.com/net/download/dotnet-core/sdk-2.1.300)
* [.NET Core 런타임 2.1 이상](https://www.microsoft.com/net/download/dotnet-core/runtime-2.1.0)

`dotnet --info` 명령을 사용하여 이미 설치한 .NET Core SDK 및 런타임 버전을 확인할 수 있습니다.

.NET Core 콘솔 애플리케이션에서 dotnet-svcutil.xmlserializer를 사용하려면

1. .NET Framework에서 기본 템플릿 ‘WCF 서비스 애플리케이션’을 사용하여 ‘MyWCFService’라는 WCF 서비스를 만듭니다.  다음과 같이 서비스 메서드에 ```[XmlSerializerFormat]``` 특성을 추가합니다.
    ```c#
    [ServiceContract]
    public interface IService1
    {
        [XmlSerializerFormat]
        [OperationContract(Action = "http://tempuri.org/IService1/GetData", ReplyAction = "http://tempuri.org/IService1/GetDataResponse")]
        string GetData(int value);
    }
    ```
2. netcoreapp 2.1을 대상으로 하는 WCF 클라이언트 애플리케이션으로 .NET Core 콘솔 애플리케이션을 만듭니다. 예를 들어 다음 명령을 사용하여 ‘MyWCFClient’라는 앱을 만듭니다.
    ```
    dotnet new console --name MyWCFClient
    ```
    csproj가 netcoreapp 2.1을 대상으로 하는지 확인합니다. .csproj 파일에서 다음 XML 요소를 사용하면 됩니다.
    ```xml
    <TargetFramework>netcoreapp2.1</TargetFramework>
    ```
3. 다음 명령을 실행하여 System.ServiceModel.Http에 대한 패키지 참조를 추가합니다.
   
   ```dotnet add package System.ServiceModel.Http -v 4.5.0```

4. WCF 클라이언트 코드를 추가합니다.
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
5. .csproj 파일을 편집하고 dotnet-svcutil.xmlserializer 패키지에 대한 참조를 추가합니다. 예:

    i. `dotnet add package dotnet-svcutil.xmlserializer -v 1.0.0` 명령을 실행합니다.

    ii. MyWCFClient.csproj에 다음 줄을 추가합니다.
    ```xml
    <ItemGroup>
      <DotNetCliToolReference Include="dotnet-svcutil.xmlserializer" Version="1.0.0" />
    </ItemGroup>
    ```

6. `dotnet build`를 실행하여 애플리케이션을 빌드합니다. 모든 항목이 성공하면 MyWCFClient.XmlSerializers.dll이라는 어셈블리가 출력 폴더에 생성됩니다. 도구가 어셈블리 생성에 실패할 경우 빌드 출력에 경고가 표시됩니다.

7. 브라우저에서 http://localhost:2561/Service1.svc를 실행하여 WCF 서비스를 시작합니다. 그런 다음, 클라이언트 애플리케이션을 시작하면 미리 생성된 직렬 변환기가 런타임 시 자동으로 로드되어 사용됩니다.
