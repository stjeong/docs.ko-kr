---
title: '방법: 다른 워크플로 서비스를 호출하는 워크플로 서비스 만들기'
ms.date: 03/30/2017
ms.assetid: 99b3ee3e-aeb7-4e6f-8321-60fe6140eb67
ms.openlocfilehash: 1b30da34f7c85cccd98b18cd32b81c83630989b2
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43725061"
---
# <a name="how-to-create-a-workflow-service-that-calls-another-workflow-service"></a>방법: 다른 워크플로 서비스를 호출하는 워크플로 서비스 만들기

워크플로 서비스에서 다른 워크플로 서비스의 정보를 얻어야 하는 경우가 가끔 있습니다. 이 항목에서는 워크플로 서비스 간에 호출하는 방법을 보여 줍니다. 이 항목에서는 두 개의 워크플로 서비스를 만듭니다. 하나는 입력 문자열의 방향을 반대로 바꾸는 메서드가 있는 서비스이고, 다른 하나는 첫 번째 서비스를 사용하는 문자열의 방향을 반대로 바꾼 후 입력 문자열을 대문자로 변환하는 서비스입니다.

### <a name="to-create-the-reverser-workflow-service"></a>Reverser 워크플로 서비스를 만들려면

1.  Visual Studio를 엽니다.

2.  선택 **파일** > **새 프로젝트**합니다. 아래는 **워크플로** 에서 노드를 **설치 된 템플릿** 창 **WCF 워크플로 서비스 응용 프로그램**합니다. 솔루션의 이름을 `NestedServices` 을 클릭 한 다음 **확인**합니다.

3.  아래 **서버**, 했는지 **사용 하 여 로컬 IIS 웹 서버** 선택 합니다. 클릭 **가상 디렉터리 만들기**합니다. 클릭 **확인** 에서 대화 상자가 나타날 가상 디렉터리를 만들었습니다.

4.  솔루션 탐색기에서 Service1.xamlx의 이름을 `StringReverserService.xamlx`입니다.

5.  에 **프로젝트 속성** 새 프로젝트 페이지를 클릭 합니다 **웹** 탭 합니다. 설정 합니다 **시작 작업** 하 **특정 페이지**, 하 고 StringReverserService.xamlx를 시작 하려면 페이지를 선택 합니다.

6.  디자이너에서 StringReverserService.xamlx를 열고 기존 `ReceiveRequest` 및 `SendReply` 활동을 삭제한 다음 `ReceiveAndSendReply` 활동을 기존 시퀀스 활동으로 끌어 옵니다.

    1.  설정 된 **OperationName** 을 reversestring으로 합니다.

    2.  설정 된 **ServiceContractName** 을 ireversestring으로 설정 합니다.

    3.  선택 된 **CanCreateInstance** 확인란 합니다.

7.  선택 합니다 **SequentialService** 활동과 클릭 한 다음는 **변수** 디자이너의 아래쪽에 있는 탭입니다. String 형식의 StringToReverse 및 ReversedStringToReturn이라는 새로운 두 변수를 만듭니다.

8.  클릭 합니다 **정의** 링크를 **수신** 활동입니다. 클릭 합니다 **매개 변수**, 고 StringToReverse에 할당 되는 String 형식의 InputString 이라는 매개 변수를 만듭니다.

9. 클릭 합니다 **정의** 링크를 **SendReplyToReceive** 활동입니다. 클릭 합니다 **매개 변수**, 고 ReversedStringToReturn에 할당 된 String 형식의 ReversedString 이라는 매개 변수를 만듭니다.

10. 서비스의 논리를 구현하려면 프로젝트에 StringLibrary라는 새 클래스를 만듭니다.  클래스 정의를 다음 코드로 바꿉니다.

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

11. 입력에 대해 ReverseString 메서드를 호출 하려면 끌어를 **InvokeMethod** 사이의 공간에 도구 상자에서 활동을 **수신** 및 **SendReply** 활동입니다. 활동의 속성을 다음과 같이 설정합니다.

    1.  **MethodName**: reversestring으로

    2.  **결과**: ReversedStringToReturn

    3.  **매개 변수**: 사용 하 여 새 매개 변수를 만듭니다를 **방향** 의는 **형식** 문자열 및 **값** 이 stringtoreverse.

    4.  **TargetType**: NestedServices.StringLibrary

12. F5 키를 눌러 서비스를 테스트합니다. WCF 테스트 클라이언트가 표시되면 ReverseString() 메서드를 두 번 클릭합니다. 요청 창에서 입력 `Sample` InputString 매개 변수의 값에 대 한 합니다. 클릭 **호출할**합니다. 그러면 서비스에서 "elpmaS"를 반환합니다.

### <a name="to-create-the-uppercaser-workflow-service"></a>UpperCaser 워크플로 서비스를 만들려면

1.  NestedServices 프로젝트를 마우스 오른쪽 단추로 누르고 **추가** > **새 항목**합니다. 에 **워크플로** 노드를 선택 **WCF Workflow Service**를 새 서비스 이름 및 `UpperCaserService`합니다. **추가**를 클릭합니다. 그러면 UpperCaserService.xamlx라는 새 워크플로 서비스가 프로젝트에 추가됩니다.

2.  디자이너에서 UpperCaserService.xamlx를 열고 기존 삭제 **ReceiveRequest** 하 고 `SendReply` 활동을 끌어서를 `ReceiveAndSendReply` 활동을 기존 시퀀스 활동 합니다.

    1.  설정 된 **OperationName** 을 uppercasestring으로 합니다.

    2.  설정 된 **ServiceContractName** 을 iuppercasestring으로 설정 합니다.

    3.  선택 된 **CanCreateInstance** 확인란 합니다.

3.  SequentialService 활동을 선택한 다음 클릭 합니다 **변수** 디자이너의 아래쪽에 있는 탭입니다. String 형식의 StringToUpper, StringToReverse 및 StringToReturn이라는 세 개의 새로운 변수를 만듭니다.

4.  클릭 합니다 **정의** 링크를 **수신** 활동입니다. 클릭 합니다 **매개 변수**, 고 StringToUpper에 할당 되는 String 형식의 InputString 이라는 매개 변수를 만듭니다.

5.  클릭 합니다 **정의** 링크를 **SendReplyToReceive** 활동입니다. 클릭 합니다 **매개 변수**, 고 StringToReturn에 할당 된 String 형식의 ModifiedString 이라는 매개 변수를 만듭니다.

6.  서비스의 논리를 구현하려면 다음 코드를 사용하여 StringLibrary 클래스에 새 메서드를 만듭니다.

    ```
    public static String UpperCaseString(string StringToUpperCase)
    {
         return StringToUpperCase.ToUpper();

    }
    ```

7.  입력에 대해 UpperCaseString 메서드를 호출 하려면 끌어를 **InvokeMethod** 사이의 공간에 도구 상자에서 활동을 **수신** 및 **SendReply** 활동입니다. 활동의 속성을 다음과 같이 설정합니다.

    1.  **MethodName**: uppercasestring으로

    2.  **결과**: StringToReverse

    3.  **매개 변수**: 사용 하 여 새 매개 변수를 만듭니다를 **방향** 의는 **형식** 문자열 및 **값** stringtoupper 합니다.

    4.  **TargetType**: NestedServices.StringLibrary

8.  이제 수정된 문자열에 대해 첫 번째 서비스를 호출합니다. 프로젝트를 마우스 오른쪽 단추로 누르고 **추가** > **서비스 참조**합니다. 서비스에 대 한 서비스 참조 추가 http://localhost/NestedServices/StringReverserService.xamlx 첫 번째 웹 서비스에 액세스 하려면 사용자 지정 활동을 만드는 프로젝트를 빌드합니다.

9. 끌어 새 활동의 인스턴스, 워크플로 간에 **InvokeMethod** 활동 하며 **SendReplyToReceive** 활동입니다. 새 활동의 InputString 속성에 StringToReverse 변수를 할당하고 StringToReturn 속성에 StringToReturn 변수를 할당합니다.

10. NestedServices 프로젝트의 속성 페이지를 열고 변경 합니다 **특정 페이지** 에 **웹** UpperCaserService.xamlx 탭 합니다.

11. F5 키를 눌러 서비스를 테스트합니다. WCF 테스트 클라이언트가 표시되면 ReverseString() 메서드를 두 번 클릭합니다. 요청 창에서 입력 `Sample` InputString 매개 변수의 값에 대 한 합니다. 클릭 **호출할**합니다. 그러면 서비스에서 "ELPMAS"를 반환합니다.

### <a name="to-create-a-client-to-call-the-services"></a>서비스를 호출할 클라이언트를 만들려면

1.  솔루션에 Client라는 새 콘솔 응용 프로그램 프로젝트를 추가합니다.

2.  클라이언트 프로젝트를 마우스 오른쪽 단추로 누르고 **추가** > **서비스 참조**합니다. 표시 되는 창에서 클릭 **Discover**합니다. StringReverserService.xamlx를 선택하고 네임스페이스로 ReverseService를 입력합니다.  **확인**을 클릭합니다.

3.  Program.cs의 Main 메서드를 다음 코드로 바꿉니다.

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