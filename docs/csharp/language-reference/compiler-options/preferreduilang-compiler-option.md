---
title: -preferreduilang(C# 컴파일러 옵션)
ms.date: 07/20/2015
f1_keywords:
- /preferreduilang
helpviewer_keywords:
- preferreduilang compiler option [C#]
- /preferreduilang compiler option [C#]
- -preferreduilang compiler option [C#]
ms.assetid: 68b2462f-6778-48d7-8052-62805fe8e02c
ms.openlocfilehash: a1fbbb8415e5e3405f039489aa071b0624065a9d
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43405893"
---
# <a name="-preferreduilang-c-compiler-options"></a><span data-ttu-id="bfdd2-102">-preferreduilang(C# 컴파일러 옵션)</span><span class="sxs-lookup"><span data-stu-id="bfdd2-102">-preferreduilang (C# Compiler Options)</span></span>
<span data-ttu-id="bfdd2-103">`-preferreduilang` 컴파일러 옵션을 사용하여 C# 컴파일러에서 오류 메시지 등의 출력을 표시하는 언어를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bfdd2-103">By using the `-preferreduilang` compiler option, you can specify the language in which the C# compiler displays output, such as error messages.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bfdd2-104">구문</span><span class="sxs-lookup"><span data-stu-id="bfdd2-104">Syntax</span></span>  
  
```console  
-preferreduilang: language  
```  
  
## <a name="arguments"></a><span data-ttu-id="bfdd2-105">인수</span><span class="sxs-lookup"><span data-stu-id="bfdd2-105">Arguments</span></span>  
 `language`  
 <span data-ttu-id="bfdd2-106">컴파일러 출력에 사용할 언어의 [언어 이름](/windows/desktop/Intl/language-names)입니다.</span><span class="sxs-lookup"><span data-stu-id="bfdd2-106">The [language name](/windows/desktop/Intl/language-names) of the language to use for compiler output.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bfdd2-107">설명</span><span class="sxs-lookup"><span data-stu-id="bfdd2-107">Remarks</span></span>  
 <span data-ttu-id="bfdd2-108">`-preferreduilang` 컴파일러 옵션을 사용하여 C# 컴파일러에서 오류 메시지와 기타 명령줄 출력에 사용할 언어를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bfdd2-108">You can use the `-preferreduilang` compiler option to specify the language that you want the C# compiler to use for error messages and other command-line output.</span></span> <span data-ttu-id="bfdd2-109">해당 언어의 언어 팩이 설치되지 않은 경우 운영 체제의 언어 설정이 대신 사용되고 오류가 보고되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bfdd2-109">If the language pack for the language is not installed, the language setting of the operating system is used instead, and no error is reported.</span></span>  
  
```csharp  
csc.exe -preferreduilang:ja-JP  
```  
  
## <a name="requirements"></a><span data-ttu-id="bfdd2-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="bfdd2-110">Requirements</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bfdd2-111">참고 항목</span><span class="sxs-lookup"><span data-stu-id="bfdd2-111">See Also</span></span>

- [<span data-ttu-id="bfdd2-112">C# 컴파일러 옵션</span><span class="sxs-lookup"><span data-stu-id="bfdd2-112">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)
