### <a name="resolveassemblyreference-task-now-warns-of-dependencies-with-the-wrong-architecture"></a><span data-ttu-id="e1bd2-101">ResolveAssemblyReference 작업이 이제 잘못된 아키텍처의 종속성에 대해 경고</span><span class="sxs-lookup"><span data-stu-id="e1bd2-101">ResolveAssemblyReference task now warns of dependencies with the wrong architecture</span></span>

|   |   |
|---|---|
|<span data-ttu-id="e1bd2-102">설명</span><span class="sxs-lookup"><span data-stu-id="e1bd2-102">Details</span></span>|<span data-ttu-id="e1bd2-103">이 작업은 참조 또는 해당 종속성이 앱 아키텍처와 일치하지 않음을 나타내는 경고 MSB3270을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="e1bd2-103">The task emits a warning, MSB3270, which indicates that a reference or any of its dependencies does not match the app's architecture.</span></span> <span data-ttu-id="e1bd2-104">예를 들어 <code>AnyCPU</code> 옵션으로 컴파일된 앱에 x86 참조가 포함된 경우 이 경고가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="e1bd2-104">For example, this occurs if an app that was compiled with the <code>AnyCPU</code> option includes an x86 reference.</span></span> <span data-ttu-id="e1bd2-105">이로 인해 앱의 런타임 오류가 발생할 수 있습니다(앱이 x64 프로세스로 배포된 경우).</span><span class="sxs-lookup"><span data-stu-id="e1bd2-105">Such a scenario could result in an app failure at run time (in this case, if the app is deployed as an x64 process).</span></span>|
|<span data-ttu-id="e1bd2-106">제안 해결 방법</span><span class="sxs-lookup"><span data-stu-id="e1bd2-106">Suggestion</span></span>|<span data-ttu-id="e1bd2-107">영향에는 다음 두 가지 영역이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1bd2-107">There are two areas of impact:</span></span><ul><li><span data-ttu-id="e1bd2-108">다시 컴파일하면 앱이 이전 MSBuild 버전에서 컴파일되었을 때는 나타나지 않았던 경고가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1bd2-108">Recompilation generates warnings that did not appear when the app was compiled under a previous version of MSBuild.</span></span> <span data-ttu-id="e1bd2-109">하지만 런타임 오류가 발생한 소스를 경고에서 확인할 수 있으므로 이 문제를 조사하여 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1bd2-109">However, because the warning identifies a possible source of runtime failure, it should be investigated and addressed.</span></span></li><li><span data-ttu-id="e1bd2-110">경고가 오류로 처리되면 앱을 컴파일할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e1bd2-110">If warnings are treated as errors, the app will fail to compile.</span></span></li></ul>|
|<span data-ttu-id="e1bd2-111">범위</span><span class="sxs-lookup"><span data-stu-id="e1bd2-111">Scope</span></span>|<span data-ttu-id="e1bd2-112">부</span><span class="sxs-lookup"><span data-stu-id="e1bd2-112">Minor</span></span>|
|<span data-ttu-id="e1bd2-113">버전</span><span class="sxs-lookup"><span data-stu-id="e1bd2-113">Version</span></span>|<span data-ttu-id="e1bd2-114">4.5.1</span><span class="sxs-lookup"><span data-stu-id="e1bd2-114">4.5.1</span></span>|
|<span data-ttu-id="e1bd2-115">형식</span><span class="sxs-lookup"><span data-stu-id="e1bd2-115">Type</span></span>|<span data-ttu-id="e1bd2-116">대상 변경</span><span class="sxs-lookup"><span data-stu-id="e1bd2-116">Retargeting</span></span>|
