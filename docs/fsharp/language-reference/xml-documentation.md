---
title: XML 문서(F#)
description: 주석에서 문서를 생성 하는 것에 대 한 F# 지원에 알아봅니다.
ms.date: 05/16/2016
ms.openlocfilehash: 1a4cb132e65b630821e5eb2b39276c1de99aff80
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/02/2018
ms.locfileid: "45641627"
---
# <a name="xml-documentation"></a>XML 문서

삼중 슬래시 (/ / /)에서 문서를 생성할 수 있습니다 코드 F#의 주석입니다. XML 주석 코드 파일 (.fs) 또는 서명 (.fsi) 파일의 선언 앞에 있습니다.

## <a name="generating-documentation-from-comments"></a>주석에서 문서 생성

주석에서 문서를 생성 하는 것에 대 한 F# 지원 다른.NET Framework 언어에 동일 합니다. 다른.net 언어와 마찬가지로 합니다 [-doc 컴파일러 옵션](https://msdn.microsoft.com/library/434394ae-0d4a-459c-a684-bffede519a04) Sandcastle 등의 도구를 사용 하 여 설명서로 변환할 수 있는 정보가 포함 된 XML 파일을 만들 수 있습니다. 일반적으로 다른.NET Framework 언어로 작성 된 어셈블리를 사용 하 여 용도로 설계 된 도구를 사용 하 여 생성 된 설명서 F# 구문의 컴파일된 형태를 기반으로 하는 Api의 뷰를 생성 합니다. 도구 특히 F#을 지원 하지 않는 한 이러한 도구로 생성 된 설명서에는 API의 F# 뷰를 일치 하지 않습니다.

Xml에서 문서를 생성 하는 방법에 대 한 자세한 내용은 참조 하세요. [XML 문서 주석 &#40;C&#35; 프로그래밍 가이드&#41;](https://msdn.microsoft.com/library/b2s063f7)합니다.

## <a name="recommended-tags"></a>권장된 태그

두 가지 방법으로 XML 문서 주석을 기록할 수 있습니다. XML 태그를 사용 하지 않고는 삼중 슬래시 주석에서 직접 설명서 작성 방법은 하나입니다. 이 작업을 수행 하는 경우 전체 주석 텍스트 바로 뒤에 오는 코드 구문에 대 한 요약 설명이으로 간주 됩니다. 각 구문에 대 한 간략 한 요약만 작성 하려는 경우이 메서드를 사용 합니다. 다른 방법은 더 구조화 된 문서를 제공 하는 데 XML 태그를 사용할 것입니다. 두 번째 메서드를 사용 하면 간단히, 추가적인 주의 사항은, 각 매개 변수 및 형식 매개 변수, throw 된 예외에 대 한 설명서 및 반환 값의 설명에 대 한 별도 정보를 지정할 수 있습니다. 다음 표에서 F# XML 코드 주석에서 인식 되는 XML 태그를 설명 합니다.

|태그 구문|설명|
|----------|-----------|
|**&lt;c&gt;***텍스트***&lt;/c&gt;**|형식임 *텍스트* 코드입니다. 이 태그 텍스트를 표시 하는 코드에 대 한 적절 한 글꼴로 설명서 생성기에서 사용할 수 있습니다.|
|**&lt;요약&gt;***텍스트*** &lt; /요약&gt;**|형식임 *텍스트* 프로그램 요소에 대 한 간략 한 설명입니다. 설명의 하나 또는 두 개의 문장을 일반적으로 됩니다.|
|**&lt;주의&gt;***텍스트*** &lt; /r&gt;**|형식임 *텍스트* 프로그램 요소에 대 한 보충 정보를 포함 합니다.|
|**&lt;param name = "***이름을***"&gt;***설명***&lt;/param&gt;**|이름 및 함수 또는 메서드 매개 변수에 대 한 설명을 지정합니다.|
|**&lt;typeparam 이름 = "***이름을***"&gt;***설명***&lt;/typeparam&gt;**|이름 및 형식 매개 변수의 설명을 지정합니다.|
|**&lt;반환&gt;***텍스트*** &lt; /r&gt;**|형식임 *텍스트* 함수 또는 메서드 반환 값을 설명 합니다.|
|**&lt;예외 cref = "***형식***"&gt;***설명***&lt;/exception&gt;**|생성 될 수 있는 예외 및 throw 되는 상황의 형식을 지정 합니다.|
|**&lt;cref = "***참조***"&gt;***텍스트***&lt;참조&gt;**|다른 프로그램 요소에 대 한 인라인 링크를 지정합니다. 합니다 *참조* XML 문서 파일에 나타나는 이름입니다. 합니다 *텍스트* 링크에 나타나는 텍스트입니다.|
|**&lt;seealso cref = "***참조***" /&gt;**|다른 형식에 대 한 설명서도 참조 링크를 지정합니다. 합니다 *참조* XML 문서 파일에 나타나는 이름입니다. 설명서 페이지의 맨 아래에 일반적으로 표시 하는 링크를 참조 하세요.|
|**&lt;para&gt;***텍스트***&lt;/para&gt;**|텍스트 단락을 지정합니다. 내부 텍스트를 구분 하는 데는이 **주의** 태그입니다.|

## <a name="example"></a>예제

### <a name="description"></a>설명

다음은 서명 파일에는 일반적인 XML 문서 주석입니다.

### <a name="code"></a>코드

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet7101.fs)]

## <a name="example"></a>예제

### <a name="description"></a>설명

다음 예제에서는 XML 태그 없이 대체 메서드를 보여 줍니다. 이 예제에서는 주석에서 전체 텍스트 요약으로 간주 됩니다. 참고는 summary 태그를 명시적으로 지정 하지 않으면 지정할 수 없습니다 다른 태그와 같은 **param** 하거나 **반환** 태그입니다.

### <a name="code"></a>코드

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet7102.fs)]

## <a name="see-also"></a>참고자료

- [F# 언어 참조](index.md)
- [컴파일러 옵션](compiler-options.md)
