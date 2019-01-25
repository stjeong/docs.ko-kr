---
title: CALL_ID 구조체
ms.date: 03/30/2017
api_name:
- CALL_ID
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- CALL_ID
helpviewer_keywords:
- CALL_ID structure [.NET Framework debugging]
ms.assetid: bfd46324-afec-4782-9c18-586d81fb4740
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 204c2dfbf28f95c1b8c2d2c1b757730e64a8e91d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54503705"
---
# <a name="callid-structure"></a><span data-ttu-id="ba17b-102">CALL_ID 구조체</span><span class="sxs-lookup"><span data-stu-id="ba17b-102">CALL_ID Structure</span></span>
<span data-ttu-id="ba17b-103">디버거에 호출 되는 함수에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba17b-103">Provides information to a debugger about a function that is being called.</span></span> <span data-ttu-id="ba17b-104">참조 된 [INotifySink2](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md) 자세한 정보에 대 한 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="ba17b-104">See the [INotifySink2](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md) interface for more information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ba17b-105">구문</span><span class="sxs-lookup"><span data-stu-id="ba17b-105">Syntax</span></span>  
  
```  
typedef struct tagCALL_ID  
{  
    LPCOLESTR       szMachine;  
    DWORD           dwPid;  
    USER_THREAD     *pUserThread;  
    STACK_ADDRESS   addrStackPointer;  
    LPCOLESTR       szEntryPoint;  
    LPCOLESTR       szDestinationMachine;  
} CALL_ID;  
```  
  
## <a name="members"></a><span data-ttu-id="ba17b-106">멤버</span><span class="sxs-lookup"><span data-stu-id="ba17b-106">Members</span></span>  
  
|<span data-ttu-id="ba17b-107">멤버</span><span class="sxs-lookup"><span data-stu-id="ba17b-107">Member</span></span>|<span data-ttu-id="ba17b-108">설명</span><span class="sxs-lookup"><span data-stu-id="ba17b-108">Description</span></span>|  
|------------|-----------------|  
|`szMachine`|<span data-ttu-id="ba17b-109">호출 하는 컴퓨터를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba17b-109">Identifies the machine that is making the call.</span></span>|  
|`dwPid`|<span data-ttu-id="ba17b-110">컴퓨터 프로세서를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="ba17b-110">Identifies the machine processor.</span></span>|  
|`pUserThread`|<span data-ttu-id="ba17b-111">호출을 실행 하는 스레드를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba17b-111">Identifies the thread that is executing the call.</span></span>|  
|`addrStackPointer`|<span data-ttu-id="ba17b-112">호출 스택의 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba17b-112">Specifies the address of the call stack.</span></span>|  
|`szEntryPoint`|<span data-ttu-id="ba17b-113">호출의 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba17b-113">Specifies the address of the call.</span></span>|  
|`szDestinationMachine`|<span data-ttu-id="ba17b-114">호출을 실행 하는 컴퓨터를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba17b-114">Identifies the machine that will execute the call.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ba17b-115">요구 사항</span><span class="sxs-lookup"><span data-stu-id="ba17b-115">Requirements</span></span>  
 <span data-ttu-id="ba17b-116">**헤더:** ProtocolNotify2.idl</span><span class="sxs-lookup"><span data-stu-id="ba17b-116">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ba17b-117">참고자료</span><span class="sxs-lookup"><span data-stu-id="ba17b-117">See also</span></span>
- [<span data-ttu-id="ba17b-118">INotifySink2 인터페이스</span><span class="sxs-lookup"><span data-stu-id="ba17b-118">INotifySink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md)
- [<span data-ttu-id="ba17b-119">진단 기호 저장소 구조체</span><span class="sxs-lookup"><span data-stu-id="ba17b-119">Diagnostics Symbol Store Structures</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-structures.md)
