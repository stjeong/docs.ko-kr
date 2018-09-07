---
title: 암호화 체계 만들기
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- encryption [.NET Framework], creating cryptographic schemes
- cryptography [.NET Framework], creating cryptographic schemes
ms.assetid: d40c509f-5a5e-46cc-94cb-a951e9ab6843
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2db6d4229ac777801aff792c86fe0e5e9a1b4994
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44080269"
---
# <a name="creating-a-cryptographic-scheme"></a><span data-ttu-id="c7709-102">암호화 체계 만들기</span><span class="sxs-lookup"><span data-stu-id="c7709-102">Creating a Cryptographic Scheme</span></span>
<span data-ttu-id="c7709-103">.NET Framework의 암호화 구성 요소를 결합하여 다양한 체계를 만들고 데이터를 암호화 및 암호 해독할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7709-103">The cryptographic components of the .NET Framework can be combined to create different schemes to encrypt and decrypt data.</span></span>  
  
 <span data-ttu-id="c7709-104">데이터 암호화 및 암호 해독을 위한 간단한 암호화 체계에서는 다음 단계를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7709-104">A simple cryptographic scheme for encrypting and decrypting data might specify the following steps:</span></span>  
  
1.  <span data-ttu-id="c7709-105">각 당사자가 공개/개인 키 쌍을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c7709-105">Each party generates a public/private key pair.</span></span>  
  
2.  <span data-ttu-id="c7709-106">양쪽 당사자가 공개 키를 교환합니다.</span><span class="sxs-lookup"><span data-stu-id="c7709-106">The parties exchange their public keys.</span></span>  
  
3.  <span data-ttu-id="c7709-107">예를 들어 각 당사자가 TripleDES 암호화를 위한 비밀 키를 생성하고 상대방의 공개 키를 사용하여 새로 만든 키를 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="c7709-107">Each party generates a secret key for TripleDES encryption, for example, and encrypts the newly created key using the other's public key.</span></span>  
  
4.  <span data-ttu-id="c7709-108">각 당사자가 상대방에게 데이터를 보내고 상대방의 비밀 키와 자신의 비밀 키를 특정 순서로 결합하여 새 비밀 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c7709-108">Each party sends the data to the other and combines the other's secret key with its own, in a particular order, to create a new secret key.</span></span>  
  
5.  <span data-ttu-id="c7709-109">양쪽 당사자가 대칭 암호화를 사용하여 대화를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c7709-109">The parties then initiate a conversation using symmetric encryption.</span></span>  
  
 <span data-ttu-id="c7709-110">암호화 체계를 만드는 과정은 간단한 작업이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="c7709-110">Creating a cryptographic scheme is not a trivial task.</span></span> <span data-ttu-id="c7709-111">암호화를 사용 하는 방법은 Platform SDK 설명서의 암호화 항목을 참조 하세요. http://msdn.microsoft.com/library합니다.</span><span class="sxs-lookup"><span data-stu-id="c7709-111">For more information on using cryptography, see the Cryptography topic in the Platform SDK documentation at http://msdn.microsoft.com/library.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c7709-112">참고자료</span><span class="sxs-lookup"><span data-stu-id="c7709-112">See also</span></span>

- [<span data-ttu-id="c7709-113">Cryptographic Services</span><span class="sxs-lookup"><span data-stu-id="c7709-113">Cryptographic Services</span></span>](../../../docs/standard/security/cryptographic-services.md)
