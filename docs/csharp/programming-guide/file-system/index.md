---
title: 파일 시스템 및 레지스트리(C# 프로그래밍 가이드)
ms.date: 07/20/2015
helpviewer_keywords:
- file system [C#]
- registry [C#]
- files [C#]
ms.assetid: 0f2511cf-2b02-4b41-b001-b1754677c38f
ms.openlocfilehash: 3625f7a108675a3a9ab6be16ef94ae7e7c107612
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44060572"
---
# <a name="file-system-and-the-registry-c-programming-guide"></a><span data-ttu-id="e16f0-102">파일 시스템 및 레지스트리(C# 프로그래밍 가이드)</span><span class="sxs-lookup"><span data-stu-id="e16f0-102">File System and the Registry (C# Programming Guide)</span></span>
<span data-ttu-id="e16f0-103">다음 항목에서는 C# 및 .NET Framework를 사용하여 파일, 폴더 및 레지스트리에 대한 다양한 기본 작업을 수행하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e16f0-103">The following topics show how to use C# and the .NET Framework to perform various basic operations on files, folders, and the Registry.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="e16f0-104">섹션 내용</span><span class="sxs-lookup"><span data-stu-id="e16f0-104">In This Section</span></span>  
  
|<span data-ttu-id="e16f0-105">**제목**</span><span class="sxs-lookup"><span data-stu-id="e16f0-105">**Title**</span></span>|<span data-ttu-id="e16f0-106">**설명**</span><span class="sxs-lookup"><span data-stu-id="e16f0-106">**Description**</span></span>|  
|---------------|---------------------|  
|[<span data-ttu-id="e16f0-107">방법: 디렉터리 트리 반복</span><span class="sxs-lookup"><span data-stu-id="e16f0-107">How to: Iterate Through a Directory Tree</span></span>](../../../csharp/programming-guide/file-system/how-to-iterate-through-a-directory-tree.md)|<span data-ttu-id="e16f0-108">디렉터리 트리를 수동으로 반복하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e16f0-108">Shows how to manually iterate through a directory tree.</span></span>|  
|[<span data-ttu-id="e16f0-109">방법: 파일, 폴더 및 드라이브에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="e16f0-109">How to: Get Information About Files, Folders, and Drives</span></span>](../../../csharp/programming-guide/file-system/how-to-get-information-about-files-folders-and-drives.md)|<span data-ttu-id="e16f0-110">파일, 폴더 및 드라이브에 대한 생성 시간 및 크기와 같은 정보를 검색하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e16f0-110">Shows how to retrieve information such as creation times and size, about files, folders and drives.</span></span>|  
|[<span data-ttu-id="e16f0-111">방법: 파일 또는 폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="e16f0-111">How to: Create a File or Folder</span></span>](../../../csharp/programming-guide/file-system/how-to-create-a-file-or-folder.md)|<span data-ttu-id="e16f0-112">새 파일 또는 폴더를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e16f0-112">Shows how to create a new file or folder.</span></span>|  
|[<span data-ttu-id="e16f0-113">방법: 파일 및 폴더 복사, 삭제 및 이동(C# 프로그래밍 가이드)</span><span class="sxs-lookup"><span data-stu-id="e16f0-113">How to: Copy, Delete, and Move Files and Folders (C# Programming Guide)</span></span>](../../../csharp/programming-guide/file-system/how-to-copy-delete-and-move-files-and-folders.md)|<span data-ttu-id="e16f0-114">파일 및 폴더를 복사, 삭제 및 이동하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e16f0-114">Shows how to copy, delete and move files and folders.</span></span>|  
|[<span data-ttu-id="e16f0-115">방법: 파일 작업에 대한 진행률 대화 상자 제공</span><span class="sxs-lookup"><span data-stu-id="e16f0-115">How to: Provide a Progress Dialog Box for File Operations</span></span>](../../../csharp/programming-guide/file-system/how-to-provide-a-progress-dialog-box-for-file-operations.md)|<span data-ttu-id="e16f0-116">특정 파일 작업에 대한 표준 Windows 진행률 대화 상자를 표시하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e16f0-116">Shows how to display a standard Windows progress dialog for certain file operations.</span></span>|  
|[<span data-ttu-id="e16f0-117">방법: 텍스트 파일에 쓰기</span><span class="sxs-lookup"><span data-stu-id="e16f0-117">How to: Write to a Text File</span></span>](../../../csharp/programming-guide/file-system/how-to-write-to-a-text-file.md)|<span data-ttu-id="e16f0-118">텍스트 파일에 쓰는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e16f0-118">Shows how to write to a text file.</span></span>|  
|[<span data-ttu-id="e16f0-119">방법: 텍스트 파일에서 읽기</span><span class="sxs-lookup"><span data-stu-id="e16f0-119">How to: Read From a Text File</span></span>](../../../csharp/programming-guide/file-system/how-to-read-from-a-text-file.md)|<span data-ttu-id="e16f0-120">텍스트 파일에서 읽는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e16f0-120">Shows how to read from a text file.</span></span>|  
|[<span data-ttu-id="e16f0-121">방법: 텍스트 파일을 한 번에 한 줄씩 읽기</span><span class="sxs-lookup"><span data-stu-id="e16f0-121">How to: Read a Text File One Line at a Time</span></span>](../../../csharp/programming-guide/file-system/how-to-read-a-text-file-one-line-at-a-time.md)|<span data-ttu-id="e16f0-122">한 번에 하나씩 파일에서 텍스트를 검색하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e16f0-122">Shows how to retrieve text from a file one line at a time.</span></span>|  
|[<span data-ttu-id="e16f0-123">방법: 레지스트리에 키 만들기</span><span class="sxs-lookup"><span data-stu-id="e16f0-123">How to: Create a Key In the Registry</span></span>](../../../csharp/programming-guide/file-system/how-to-create-a-key-in-the-registry.md)|<span data-ttu-id="e16f0-124">시스템 레지스트리에 키를 작성하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e16f0-124">Shows how to write a key to the system registry.</span></span>|  
  
## <a name="related-sections"></a><span data-ttu-id="e16f0-125">관련 단원</span><span class="sxs-lookup"><span data-stu-id="e16f0-125">Related Sections</span></span>  
 [<span data-ttu-id="e16f0-126">파일 및 스트림 I/O</span><span class="sxs-lookup"><span data-stu-id="e16f0-126">File and Stream I/O</span></span>](../../../standard/io/index.md)  
  
 [<span data-ttu-id="e16f0-127">방법: 파일 및 폴더 복사, 삭제 및 이동(C# 프로그래밍 가이드)</span><span class="sxs-lookup"><span data-stu-id="e16f0-127">How to: Copy, Delete, and Move Files and Folders (C# Programming Guide)</span></span>](../../../csharp/programming-guide/file-system/how-to-copy-delete-and-move-files-and-folders.md)  
  
 [<span data-ttu-id="e16f0-128">C# 프로그래밍 가이드</span><span class="sxs-lookup"><span data-stu-id="e16f0-128">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
  
 [<span data-ttu-id="e16f0-129">파일, 폴더 및 드라이브</span><span class="sxs-lookup"><span data-stu-id="e16f0-129">Files, Folders and Drives</span></span>](../../../csharp/programming-guide/file-system/index.md)  
  
 <xref:System.IO?displayProperty=nameWithType>
