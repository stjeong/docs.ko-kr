---
title: 사용자 지정 추적 레코드
ms.date: 03/30/2017
ms.assetid: 24284565-c68b-40bf-b7f1-e148d151a6fc
ms.openlocfilehash: 7f866713b5d6f6c82dff80864f2eccb5d2f6cb30
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54529832"
---
# <a name="custom-tracking-records"></a><span data-ttu-id="5edd8-102">사용자 지정 추적 레코드</span><span class="sxs-lookup"><span data-stu-id="5edd8-102">Custom Tracking Records</span></span>
<span data-ttu-id="5edd8-103">이 항목에서는 사용자 지정 추적 레코드를 만들고 이 레코드와 함께 내보내질 데이터로 이 레코드를 채우는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5edd8-103">This topic demonstrates how to create custom tracking records and populate them with data to be emitted along with the records.</span></span>  
  
## <a name="emitting-custom-tracking-records"></a><span data-ttu-id="5edd8-104">사용자 지정 추적 레코드 내보내기</span><span class="sxs-lookup"><span data-stu-id="5edd8-104">Emitting Custom Tracking Records</span></span>  
 <span data-ttu-id="5edd8-105">다음 예제에 표시된 것처럼 코드 활동에서 사용자 지정 추적 레코드를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5edd8-105">Custom tracking records can be emitted from a code activity as shown in the following example.</span></span>  
  
```  
protected override void Execute(CodeActivityContext context)  
{  
…  
            CustomTrackingRecord customRecord = new CustomTrackingRecord("CustomEmailSentEvent");  
            customRecord.Data.Add("SendTime", sendTime);  
            context.Track(customRecord);  
}  
```  
  
 <span data-ttu-id="5edd8-106"><xref:System.Activities.Tracking.CustomTrackingRecord>에서 <xref:System.Activities.NativeActivityContext.Track%2A> 메서드를 호출하여 코드 활동에서 `ActvityContext`를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="5edd8-106">A <xref:System.Activities.Tracking.CustomTrackingRecord> is emitted in a code activity by invoking the <xref:System.Activities.NativeActivityContext.Track%2A> method on the `ActvityContext`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5edd8-107">참고자료</span><span class="sxs-lookup"><span data-stu-id="5edd8-107">See also</span></span>
- [<span data-ttu-id="5edd8-108">Windows Server App Fabric 모니터링</span><span class="sxs-lookup"><span data-stu-id="5edd8-108">Windows Server App Fabric Monitoring</span></span>](https://go.microsoft.com/fwlink/?LinkId=201273)
- [<span data-ttu-id="5edd8-109">App Fabric을 사용 하 여 응용 프로그램 모니터링</span><span class="sxs-lookup"><span data-stu-id="5edd8-109">Monitoring Applications with App Fabric</span></span>](https://go.microsoft.com/fwlink/?LinkId=201275)
