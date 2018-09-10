---
title: global 상황별 키워드(C# 참조)
ms.date: 07/20/2015
f1_keywords:
- global
- global_CSharpKeyword
helpviewer_keywords:
- global keyword [C#]
ms.assetid: 8932c16a-6959-42c2-86e7-2c4221ab788b
ms.openlocfilehash: 837245e31a9a795aa2f13cfc6c33fefb6402801d
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/09/2018
ms.locfileid: "44217454"
---
# <a name="global-c-reference"></a><span data-ttu-id="2deb8-102">global(C# 참조)</span><span class="sxs-lookup"><span data-stu-id="2deb8-102">global (C# Reference)</span></span>

<span data-ttu-id="2deb8-103">`global` 상황별 키워드가 [:: 연산자](../operators/namespace-alias-qualifer.md) 앞에 배치되는 경우, 이 키워드는 전역 네임스페이스를 가리킵니다. 이는 모든 C# 프로그램의 기본 네임스페이스이며 다른 경우에는 명명되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2deb8-103">The `global` contextual keyword, when it comes before the [:: operator](../operators/namespace-alias-qualifer.md), refers to the global namespace, which is the default namespace for any C# program and is otherwise unnamed.</span></span> <span data-ttu-id="2deb8-104">자세한 내용은 [방법: 전역 네임스페이스 별칭 사용](../../programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2deb8-104">For more information, see [How to: Use the Global Namespace Alias](../../programming-guide/namespaces/how-to-use-the-global-namespace-alias.md).</span></span>

## <a name="example"></a><span data-ttu-id="2deb8-105">예</span><span class="sxs-lookup"><span data-stu-id="2deb8-105">Example</span></span>

<span data-ttu-id="2deb8-106">다음 예제에서는 `global` 상황별 키워드를 사용하여 `TestApp` 클래스가 전역 네임스페이스에 정의되도록 지정하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2deb8-106">The following example shows how to use the `global` contextual keyword to specify that the class `TestApp` is defined in the global namespace:</span></span>

[!code-csharp[csrefKeywordsContextual#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsContextual/CS/csrefKeywordsContextual.cs#13)]

## <a name="see-also"></a><span data-ttu-id="2deb8-107">참고 항목</span><span class="sxs-lookup"><span data-stu-id="2deb8-107">See also</span></span>

- [<span data-ttu-id="2deb8-108">네임스페이스</span><span class="sxs-lookup"><span data-stu-id="2deb8-108">Namespaces</span></span>](../../programming-guide/namespaces/index.md)