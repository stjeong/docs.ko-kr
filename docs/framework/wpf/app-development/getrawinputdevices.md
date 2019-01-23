---
title: GetRawInputDevices
ms.date: 03/30/2017
helpviewer_keywords:
- raw input [WPF]
ms.assetid: c4d37ecd-065a-4d1c-9e6c-26804ae968ca
ms.openlocfilehash: 18564e0de8f88e89f8fb71d28ee3bfeccceea4ff
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54507566"
---
# <a name="getrawinputdevices"></a><span data-ttu-id="2ebff-102">GetRawInputDevices</span><span class="sxs-lookup"><span data-stu-id="2ebff-102">GetRawInputDevices</span></span>
<span data-ttu-id="2ebff-103">PresentationHost.exe가 호스트 응용 프로그램과 관련된 원시 입력 장치(휴먼 인터페이스 장치)를 검색할 수 있게 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ebff-103">Allows PresentationHost.exe to discover the raw input devices (Human Interface Devices) that the host application is interested in.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2ebff-104">구문</span><span class="sxs-lookup"><span data-stu-id="2ebff-104">Syntax</span></span>  
  
```  
HRESULT GetRawInputDevices( [out] IEnumRAWINPUTDEVICE **ppEnum );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2ebff-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2ebff-105">Parameters</span></span>  
 `ppEnum`  
  
 <span data-ttu-id="2ebff-106">[out] 에 대 한 포인터를 [IEnumRAWINPUTDEVICE](../../../../docs/framework/wpf/app-development/ienumrawinputdevice.md) 원시 입력된 장치를 열거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ebff-106">[out] A pointer to an [IEnumRAWINPUTDEVICE](../../../../docs/framework/wpf/app-development/ienumrawinputdevice.md) for enumerating the raw input devices.</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="2ebff-107">속성 값/반환 값</span><span class="sxs-lookup"><span data-stu-id="2ebff-107">Property Value/Return Value</span></span>  
 <span data-ttu-id="2ebff-108">HRESULT:</span><span class="sxs-lookup"><span data-stu-id="2ebff-108">HRESULT:</span></span>  
  
 <span data-ttu-id="2ebff-109">S_OK- [IEnumRAWINPUTDEVICE](../../../../docs/framework/wpf/app-development/ienumrawinputdevice.md) S_OK가 반환 된 경우 PresentationHost.exe에서 사용만 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ebff-109">S_OK - [IEnumRAWINPUTDEVICE](../../../../docs/framework/wpf/app-development/ienumrawinputdevice.md) will only be used by PresentationHost.exe if S_OK is returned.</span></span>  
  
 <span data-ttu-id="2ebff-110">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="2ebff-110">E_NOTIMPL</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2ebff-111">설명</span><span class="sxs-lookup"><span data-stu-id="2ebff-111">Remarks</span></span>  
 <span data-ttu-id="2ebff-112">원시 입력 장치는 키보드, 마우스 및 리모콘과 같은 덜 일반적인 장치를 포함하는 입력 장치 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="2ebff-112">Raw input devices are the set of input devices that includes keyboards, mice, and less traditional devices like remote controls.</span></span>  
  
 <span data-ttu-id="2ebff-113">원시 입력 장치 목록이 검색된 후 PresentationHost.exe는 WM_INPUT 알림 메시지를 받을 장치를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="2ebff-113">Once the list of raw input devices has been retrieved, PresentationHost.exe registers with the devices to receive WM_INPUT notification messages.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2ebff-114">참고자료</span><span class="sxs-lookup"><span data-stu-id="2ebff-114">See also</span></span>
- [<span data-ttu-id="2ebff-115">GetRawInputDeviceList</span><span class="sxs-lookup"><span data-stu-id="2ebff-115">GetRawInputDeviceList</span></span>](/windows/desktop/api/winuser/nf-winuser-getrawinputdevicelist)
- [<span data-ttu-id="2ebff-116">FilterInputMessage</span><span class="sxs-lookup"><span data-stu-id="2ebff-116">FilterInputMessage</span></span>](../../../../docs/framework/wpf/app-development/filterinputmessage.md)
