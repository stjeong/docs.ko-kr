---
title: '방법: LINQ to XML 예제 빌드(C#)'
ms.date: 07/20/2015
ms.assetid: e5d18fa1-2704-48fe-a44b-1564f97c9e9c
ms.openlocfilehash: 9884fa27cd0bad7c869596fd54e52df85871088e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54496272"
---
# <a name="how-to-build-linq-to-xml-examples-c"></a><span data-ttu-id="f8cea-102">방법: LINQ to XML 예제 빌드(C#)</span><span class="sxs-lookup"><span data-stu-id="f8cea-102">How to: Build LINQ to XML Examples (C#)</span></span>
<span data-ttu-id="f8cea-103">이 설명서의 다양한 코드 조각과 예제에서는 여러 가지 네임스페이스의 클래스와 형식을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cea-103">The various snippets and examples in this documentation use classes and types from a variety of namespaces.</span></span> <span data-ttu-id="f8cea-104">C# 코드를 컴파일하는 경우 적절한 `using` 지시문을 제공해야 하고,</span><span class="sxs-lookup"><span data-stu-id="f8cea-104">When compiling C# code, you need to supply appropriate `using` directives.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f8cea-105">예제</span><span class="sxs-lookup"><span data-stu-id="f8cea-105">Example</span></span>  
 <span data-ttu-id="f8cea-106">다음 코드에는 C# 예제에서 빌드하고 실행해야 하는 `using` 지시문이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8cea-106">The following code contains the `using` directives that the C# examples require to build and run.</span></span> <span data-ttu-id="f8cea-107">모든 `using` 지시문이 모든 예제에 필요한 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="f8cea-107">Not all `using` directives are required for every example.</span></span>  
  
```csharp  
using System;  
using System.Diagnostics;  
using System.Collections;  
using System.Collections.Generic;  
using System.Collections.Specialized;  
using System.Text;  
using System.Linq;  
using System.Xml;  
using System.Xml.Linq;  
using System.Xml.Schema;  
using System.Xml.XPath;  
using System.Xml.Xsl;  
using System.IO;  
using System.Threading;  
using System.Reflection;  
using System.IO.Packaging;  
```  
  
## <a name="see-also"></a><span data-ttu-id="f8cea-108">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f8cea-108">See also</span></span>

- [<span data-ttu-id="f8cea-109">LINQ to XML 프로그래밍 개요(C#)</span><span class="sxs-lookup"><span data-stu-id="f8cea-109">LINQ to XML Programming Overview (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-programming-overview.md)
