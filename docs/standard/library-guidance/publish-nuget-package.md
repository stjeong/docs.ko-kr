---
title: NuGet 패키지 게시
description: .NET 라이브러리를 NuGet에 게시 하기 위한 권장 사항을 사용 하는 것이 좋습니다.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 0602712311411ef3d59825bec8c5e550bc8d8265
ms.sourcegitcommit: d88024e6d6d8b242feae5f4007a709379355aa24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2018
ms.locfileid: "49370326"
---
# <a name="publishing-a-nuget-package"></a><span data-ttu-id="2eaae-103">NuGet 패키지 게시</span><span class="sxs-lookup"><span data-stu-id="2eaae-103">Publishing a NuGet package</span></span>

<span data-ttu-id="2eaae-104">NuGet 패키지 게시 되 고 패키지 리포지토리에서 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-104">NuGet packages are published and consumed from package repositories.</span></span> <span data-ttu-id="2eaae-105">상태인 NuGet.org 가장 널리 알려져 있고 리포지토리는 NuGet 패키지를 게시 하려면 여러 위치</span><span class="sxs-lookup"><span data-stu-id="2eaae-105">While NuGet.org is the most widely known and used repository, there are many places to publish NuGet packages:</span></span>

* <span data-ttu-id="2eaae-106">**[NuGet.org](https://www.nuget.org/)**  는 NuGet 패키지에 대 한 기본 온라인 리포지토리입니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-106">**[NuGet.org](https://www.nuget.org/)** is the primary online repository for NuGet packages.</span></span> <span data-ttu-id="2eaae-107">NuGet.org의 모든 패키지는 모든 사용자에 게 공개적으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-107">All packages on NuGet.org are publicly available to everyone.</span></span> <span data-ttu-id="2eaae-108">기본적으로 Visual Studio에는 NuGet.org를 패키지 소스로 하 고 많은 개발자가 NuGet.org 상호 작용 하는 것만 패키지 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-108">By default, Visual Studio has NuGet.org as a package source and for many developers NuGet.org is the only package repository they'll interact with.</span></span> <span data-ttu-id="2eaae-109">NuGet.org가 커뮤니티 피드백에 원하는 안정적인 패키지 및 시험판 버전을 게시 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-109">NuGet.org is the best place to publish stable packages and pre-release packages that you want community feedback on.</span></span>

* <span data-ttu-id="2eaae-110">**[MyGet](https://myget.org/)**  저장소 서비스가 지 원하는 [오픈 소스 프로젝트에 대 한 무료 사용자 지정 패키지 피드](https://www.myget.org/opensource)합니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-110">**[MyGet](https://myget.org/)** repository service supports [free custom package feeds for open-source projects](https://www.myget.org/opensource).</span></span> <span data-ttu-id="2eaae-111">MyGet 공용 사용자 지정 피드는 CI 서비스에 의해 생성 된 시험판 패키지를 게시 하는 데 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-111">A MyGet public custom feed is an ideal place to publish pre-release packages created by your CI service.</span></span> <span data-ttu-id="2eaae-112">또한 MyGet 개인 피드를 상업적으로 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-112">MyGet also provides private feeds commercially.</span></span>

* <span data-ttu-id="2eaae-113">A **[로컬 피드](/nuget/hosting-packages/local-feeds)** 해지고 패키지 리포지토리를 같은 폴더를 처리할 수 있습니다는 `*.nupkg` NuGet에서 액세스할 수 있는 폴더의 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-113">A **[local feed](/nuget/hosting-packages/local-feeds)** allows you to treat a folder like a package repository and makes the `*.nupkg` files in the folder accessible by NuGet.</span></span> <span data-ttu-id="2eaae-114">로컬 피드 NuGet 패키지를 NuGet.org에 게시 하기 전에 테스트 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-114">A local feed is useful for testing a NuGet package before publishing it to NuGet.org.</span></span>

> [!NOTE]
> <span data-ttu-id="2eaae-115">NuGet.org [패키지를 삭제할 수 없도록](/nuget/policies/deleting-packages) 업로드 되 면 합니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-115">NuGet.org [does not allow a package to be deleted](/nuget/policies/deleting-packages) once it is uploaded.</span></span> <span data-ttu-id="2eaae-116">UI에 공개적으로 표시 되지 않도록 패키지 나열 될 수 있습니다 하지만 `*.nupkg` 복원에 계속 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-116">A package can be unlisted so that it is not publicly visible in the UI but the `*.nupkg` can still be downloaded on restore.</span></span> <span data-ttu-id="2eaae-117">또한 nuget.org는 중복 된 패키지 버전을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-117">Also, nuget.org does not allow duplicate package versions.</span></span> <span data-ttu-id="2eaae-118">잘못 된 패키지의 나열을 취소 해야 하는 오류를 사용 하 여 NuGet 패키지를 수정 하려면 버전 번호를 증가 하 고 패키지의 새 버전을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-118">To correct a NuGet package with an error you have to unlist the incorrect package, increment the version number and publish a new version of the package.</span></span>

<span data-ttu-id="2eaae-119">**✔️ 마십시오** [안정적인 패키지 및 시험판 패키지를 게시](/nuget/create-packages/publish-a-package) NuGet.org에 커뮤니티 사용자 의견을 원하는 합니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-119">**✔️ DO** [publish stable packages and pre-release packages](/nuget/create-packages/publish-a-package) you want community feedback on to NuGet.org.</span></span>

<span data-ttu-id="2eaae-120">**✔️ 하십시오** 연속 통합 빌드에서 피드 시험판 패키지를 MyGet에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-120">**✔️ CONSIDER** publishing pre-release packages to a MyGet feed from a continuous integration build.</span></span>

<span data-ttu-id="2eaae-121">**✔️ 하십시오** 로컬 피드 또는 MyGet을 사용 하 여 개발 환경에서 패키지를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-121">**✔️ CONSIDER** testing packages in your development environment using a local feed or MyGet.</span></span> <span data-ttu-id="2eaae-122">패키지 작동을 확인 한 다음 NuGet.org에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-122">Check the package works then publish it to NuGet.org.</span></span>

## <a name="nugetorg-security"></a><span data-ttu-id="2eaae-123">NuGet.org 보안</span><span class="sxs-lookup"><span data-stu-id="2eaae-123">NuGet.org security</span></span>

<span data-ttu-id="2eaae-124">것이 중요 믿지 못할 자 NuGet 계정에 액세스 하 고 라이브러리의 악의적인 버전을 업로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-124">It's important that bad actors can't access your NuGet account and upload a malicious version of your library.</span></span> <span data-ttu-id="2eaae-125">NuGet.org는 패키지를 게시할 때 2 단계 인증 및 전자 메일 알림을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-125">NuGet.org offers two-factor authentication and email notifications when a package is published.</span></span> <span data-ttu-id="2eaae-126">NuGet.org에 로그인 한 후 이러한 기능을 사용 하도록 설정 합니다 **계정 설정** 페이지입니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-126">Enable these features after logging into NuGet.org on the **Account settings** page.</span></span>

<span data-ttu-id="2eaae-127">![대체 텍스트](./media/publish-nuget-package/nuget-2fa.png "NuGet 계정 보안")</span><span class="sxs-lookup"><span data-stu-id="2eaae-127">![alt text](./media/publish-nuget-package/nuget-2fa.png "NuGet Account Security")</span></span>

<span data-ttu-id="2eaae-128">**✔️ 수행** NuGet에 로그인 하려면 Microsoft 계정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-128">**✔️ DO** use a Microsoft account to sign in to NuGet.</span></span>

<span data-ttu-id="2eaae-129">**✔️ 수행** NuGet에 액세스 하기 위한 2 단계 인증을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-129">**✔️ DO** enable two-factor authentication for accessing NuGet.</span></span>

<span data-ttu-id="2eaae-130">**✔️ 수행** 패키지 게시 되 면 전자 메일 알림을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2eaae-130">**✔️ DO** enable email notification when a package is published.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="2eaae-131">[이전](./sourcelink.md)
[다음](./versioning.md)</span><span class="sxs-lookup"><span data-stu-id="2eaae-131">[Previous](./sourcelink.md)
[Next](./versioning.md)</span></span>
