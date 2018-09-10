---
title: -recurse(C# 컴파일러 옵션)
ms.date: 07/20/2015
f1_keywords:
- /recurse
helpviewer_keywords:
- /recurse compiler option [C#]
- recurse compiler option [C#]
- -recurse compiler option [C#]
ms.assetid: 4e8212e5-04e3-45b1-8a42-41bc50e683b0
ms.openlocfilehash: 1fc5591cb73164e15384eb4407a6e61e903eedbb
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43529899"
---
# <a name="-recurse-c-compiler-options"></a>-recurse(C# 컴파일러 옵션)
-recurse 옵션을 사용하면 지정된 디렉터리(dir) 또는 프로젝트 디렉터리의 모든 자식 디렉터리에 있는 소스 코드 파일을 컴파일할 수 있습니다.  
  
## <a name="syntax"></a>구문  
  
```console  
-recurse:[dir\]file  
```  
  
## <a name="arguments"></a>인수  
 `dir`(선택 사항)  
 검색을 시작하려는 디렉터리입니다. 지정하지 않으면 프로젝트 디렉터리에서 검색이 시작됩니다.  
  
 `file`  
 검색할 파일입니다. 와일드카드 문자가 허용됩니다.  
  
## <a name="remarks"></a>설명  
 **-recurse** 옵션을 사용하면 지정된 디렉터리(`dir`) 또는 프로젝트 디렉터리의 모든 자식 디렉터리에 있는 소스 코드 파일을 컴파일할 수 있습니다.  
  
 파일 이름에 와일드카드를 사용하면 **-recurse**를 사용하지 않고 프로젝트 디렉터리에서 일치하는 모든 파일을 컴파일할 수 있습니다.  
  
 이 컴파일러 옵션은 Visual Studio에서 사용할 수 없으며 프로그래밍 방식으로 변경할 수 없습니다.  
  
## <a name="example"></a>예  
 현재 디렉터리의 모든 C# 파일을 컴파일합니다.  
  
```console  
csc *.cs  
```  
  
 dir1\dir2 디렉터리와 자식 디렉터리에 있는 모든 C# 파일을 컴파일하여 dir2.dll을 생성합니다.  
  
```console  
csc -target:library -out:dir2.dll -recurse:dir1\dir2\*.cs  
```  
  
## <a name="see-also"></a>참고 항목  

- [C# 컴파일러 옵션](../../../csharp/language-reference/compiler-options/index.md)  
- [프로젝트 및 솔루션 속성 관리](/visualstudio/ide/managing-project-and-solution-properties)
