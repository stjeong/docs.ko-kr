---
title: 'F# 이란'
description: 'F# 프로그래밍 언어란 무엇인지 그리고 F# 프로그래밍이 어떤 것인지에 대해 배웁니다. 다양한 데이터 타입들, 함수들 그리고 이것들이 어떻게 함께 어울리는지에 대해 배웁니다.'
ms.date: 08/03/2018
ms.openlocfilehash: 193747f380c61a387ed79ecca6abbcd90ee74376
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43863298"
---
# <a name="what-is-f"></a>F# 이란 #

F#은 정확하고 유지 보수가 쉬운 코드를 만들어주는 함수형 프로그래밍 언어입니다.

F# 프로그래밍은 주로 타입 추론 및 일반화된 타입 및 함수를 자동으로 정의하는 것을 포함합니다. 이를 통해 프로그래밍의 세부 사항들보다는 계속해서 문제 도메인에 집중하고 데이터를 다루게끔 해줍니다.

```fsharp
open System // 시스템 네임스페이스의 기능에 대한 접근을 가져옵니다.

// 이름을 가져오고 인사를 만들어내는 함수를 정의합니다.
let getGreeting name =
    sprintf "Hello, %s! Isn't F# great?" name

[<EntryPoint>]
let main args =
    // 이름들의 리스트를 정의합니다.
    let names = [ "Don"; "Julia"; "Xi" ]

    // 각 이름에 대한 인사를 출력합니다!
    names
    |> List.map getGreeting
    |> List.iter (fun greeting -> printfn "%s" greeting)

    0
```

F#은 다음과 같은 다양한 기능들이 있습니다.

* 간단한 구문
* 기본적으로 변경불가능
* 타입 추론 및 자동화된 일반화
* 일급 함수
* 강력한 데이터 타입
* 패턴 매칭
* 비동기 프로그래밍

기능들의 전체 모움은 [F# 언어 레퍼런스](language-reference/index.md)에 문서화 되어 있습니다.
기능의 전체 집합에 설명 되어는 [F # 언어 참조](language-reference/index.md)합니다.

## <a name="rich-data-types"></a>다양 한 데이터 타입

[레코드](language-reference/records.md) 및 [식별된 공용체](language-reference/discriminated-unions.md)와 같은 데이터 타입들을 사용하면 복잡한 데이터와 도메인들을 표현할 수 있습니다.

```fsharp
// 레코드들로 데이터를 그룹화
type SuccessfulWithdrawal = {
    Amount: decimal
    Balance: decimal
}

type FailedWithdrawal = {
    Amount: decimal
    Balance: decimal
    IsOverdraft: bool
}

// 식별된 공용체를 사용하여 1개 이상의 양식 데이터를 표현
type WithdrawalResult =
    | Success of SuccessfulWithdrawal
    | InsufficientFunds of FailedWithdrawal
    | CardExpired of System.DateTime
    | UndisclosedFailure
```

F# 레코드와 식별된 공용체는 기본적으로 null이 아니며 변경 불가능하며 비교할 수 있으므로 매우 쉽게 사용할 수 있습니다.

## <a name="enforced-correctness-with-functions-and-pattern-matching"></a>함수 및 패턴 매칭을 통한 정확성 강화

F# 함수는 실제로 선언하기 쉽고 강력합니다. [패턴 매칭](language-reference/pattern-matching.md)과 함께 사용하면 컴파일러가 정확성을 적용하는 동작을 정의할 수 있습니다.


```fsharp
// 인출 결과를 반환합니다.
let withdrawMoney amount = // 구현 생략

let handleWithdrawal amount =
    let w = withdrawMoney amount

    // The F# compiler enforces accounting for each case!
    match w with
    | Success s -> printfn "Successfully withdrew %f" s.Amount
    | InsufficientFunds f -> printfn "Failed: balance is %f" f.Balance
    | CardExpired d -> printfn "Failed: card expired on %O" d
    | UndisclosedFailure -> printfn "Failed: unknown :("
```

F# 함수는 또한 일급함수이기 때문에 매개 변수로 전달되고 다른 함수에서 반환될 수 있습니다.

## <a name="functions-to-define-operations-on-objects"></a>객체에 대한 연산을 정의하는 함수

F#은 객체를 완벽하게 지원합니다. 객체는 데이터와 함수를 혼합해야 할 때 유용한 데이터 타입입니다.

```fsharp
type Set<[<EqualityConditionOn>] ‘T when ‘T: comparison>(elements: seq<'T>) =
    member s.IsEmpty = // 구현 생략
    member s.Contains (value) =// 구현 생략
    member s.Add (value) = // 구현 생략
    // ...
    // 더 많은 구현 생략
    // ...
    interface IEnumerable<‘T>
    interface IReadOnlyCollection<‘T>

[<RequireQualifiedAccess>]
module Set =
    let isEmpty (set: Set<'T>) = set.IsEmpty

    let contains element (set: Set<'T>) = set.Contains(element)

    let add value (set: Set<'T>) = set.Add(value)
```

F#에서는 객체 지향적 코드를 작성하는 것 보다 함수를 조작하는 데 필요한 다른 데이터 타입으로 객체를 처리하는 코드를 작성합니다. [제네릭 인터페이스](language-reference/interfaces.md), [객체 식](language-reference/object-expressions.md) 및 [멤버](language-reference/members/index.md)의 현명한 사용과 같은 기능은 더 큰 F# 프로그램에서 일반적입니다.

## <a name="next-steps"></a>다음 단계

더 많은 F# 기능들의 모움은, [F# 둘러보기](tour.md)를 확인하십시오.
