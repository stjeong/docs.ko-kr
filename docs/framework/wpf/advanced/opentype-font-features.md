---
title: OpenType 글꼴 기능
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- fonts [WPF], OpenType
- typography [WPF], OpenType font technology
- OpenType font technology [WPF]
ms.assetid: 4061a9d1-fe8b-4921-9e17-18ec7d2e3ea2
ms.openlocfilehash: f3d1dd9f7ef8122ac5573121e4f779fade776c8c
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43862146"
---
# <a name="opentype-font-features"></a><span data-ttu-id="42dda-102">OpenType 글꼴 기능</span><span class="sxs-lookup"><span data-stu-id="42dda-102">OpenType Font Features</span></span>
<span data-ttu-id="42dda-103">이 항목에서는 [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)]에 있는 [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 글꼴 기술의 주요 기능 일부에 대한 개요를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-103">This topic provides an overview of some of the key features of [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] font technology in [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)].</span></span>  
  

  
<a name="overview"></a>   
## <a name="opentype-font-format"></a><span data-ttu-id="42dda-104">OpenType 글꼴 서식</span><span class="sxs-lookup"><span data-stu-id="42dda-104">OpenType Font Format</span></span>  
 <span data-ttu-id="42dda-105">[!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 글꼴 서식은 PostScript 글꼴 데이터에 대한 지원을 추가하는 [!INCLUDE[TLA#tla_truetype](../../../../includes/tlasharptla-truetype-md.md)] 글꼴 서식의 확장입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-105">The [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] font format is an extension of the [!INCLUDE[TLA#tla_truetype](../../../../includes/tlasharptla-truetype-md.md)] font format, adding support for PostScript font data.</span></span> <span data-ttu-id="42dda-106">[!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 글꼴 서식은 [!INCLUDE[TLA#tla_ms](../../../../includes/tlasharptla-ms-md.md)]와 Adobe Corporation이 공동으로 개발했습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-106">The [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] font format was developed jointly by [!INCLUDE[TLA#tla_ms](../../../../includes/tlasharptla-ms-md.md)] and Adobe Corporation.</span></span> [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)]<span data-ttu-id="42dda-107"> 글꼴 및 [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 글꼴을 지원하는 운영 체제 서비스는 글꼴에 포함된 윤곽선이 [!INCLUDE[TLA2#tla_truetype](../../../../includes/tla2sharptla-truetype-md.md)] 윤곽선인지 아니면 CFF(PostScript) 윤곽선인지에 관계없이 글꼴을 설치하여 사용하는 간단한 방법을 사용자에게 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-107"> fonts and the operating system services which support [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] fonts provide users with a simple way to install and use fonts, whether the fonts contain [!INCLUDE[TLA2#tla_truetype](../../../../includes/tla2sharptla-truetype-md.md)] outlines or CFF (PostScript) outlines.</span></span>  
  
 <span data-ttu-id="42dda-108">[!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 글꼴 서식은 다음과 같이 개발자 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-108">The [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] font format addresses the following developer challenges:</span></span>  
  
-   <span data-ttu-id="42dda-109">광범위한 다중 플랫폼 지원</span><span class="sxs-lookup"><span data-stu-id="42dda-109">Broader multi-platform support.</span></span>  
  
-   <span data-ttu-id="42dda-110">국가별 문자 집합에 대한 지원 향상</span><span class="sxs-lookup"><span data-stu-id="42dda-110">Better support for international character sets.</span></span>  
  
-   <span data-ttu-id="42dda-111">글꼴 데이터 보호 향상</span><span class="sxs-lookup"><span data-stu-id="42dda-111">Better protection for font data.</span></span>  
  
-   <span data-ttu-id="42dda-112">보다 효율적인 글꼴 배포를 위한 파일 크기 축소</span><span class="sxs-lookup"><span data-stu-id="42dda-112">Smaller file sizes to make font distribution more efficient.</span></span>  
  
-   <span data-ttu-id="42dda-113">고급 입력 체계 컨트롤을 위한 폭넓은 지원</span><span class="sxs-lookup"><span data-stu-id="42dda-113">Broader support for advanced typographic control.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="42dda-114">Windows SDK에는 [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] 응용 프로그램과 함께 사용할 수 있는 샘플 [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 글꼴 집합이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-114">The Windows SDK contains a set of sample [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] fonts that you can use with [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] applications.</span></span> <span data-ttu-id="42dda-115">이 글꼴에서는 이 항목의 나머지 부분에서 보여 주는 대부분의 기능이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-115">These fonts provide most of the features illustrated in the rest of this topic.</span></span> <span data-ttu-id="42dda-116">자세한 내용은 [샘플 OpenType 글꼴 팩](../../../../docs/framework/wpf/advanced/sample-opentype-font-pack.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="42dda-116">For more information, see [Sample OpenType Font Pack](../../../../docs/framework/wpf/advanced/sample-opentype-font-pack.md).</span></span>  
  
 <span data-ttu-id="42dda-117">[!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 글꼴 서식에 대한 자세한 내용은 [OpenType 사양](https://go.microsoft.com/fwlink/?LinkId=96731)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="42dda-117">See the [OpenType Specification](https://go.microsoft.com/fwlink/?LinkId=96731) for details of the [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] font format.</span></span>  
  
### <a name="advanced-typographic-extensions"></a><span data-ttu-id="42dda-118">고급 입력 체계 확장</span><span class="sxs-lookup"><span data-stu-id="42dda-118">Advanced Typographic Extensions</span></span>  
 <span data-ttu-id="42dda-119">고급 입력 체계 표([!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 레이아웃 표)는 [!INCLUDE[TLA2#tla_truetype](../../../../includes/tla2sharptla-truetype-md.md)] 또는 CFF 윤곽선으로 글꼴 기능을 확장합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-119">The Advanced Typographic tables ([!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] Layout tables) extend the functionality of fonts with either [!INCLUDE[TLA2#tla_truetype](../../../../includes/tla2sharptla-truetype-md.md)] or CFF outlines.</span></span> [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)]<span data-ttu-id="42dda-120"> 레이아웃 글꼴에는 고품질 국제 입력 체계를 지원하도록 글꼴 기능을 확장하는 추가 정보가 들어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-120"> Layout fonts contain additional information that extends the capabilities of the fonts to support high-quality international typography.</span></span> <span data-ttu-id="42dda-121">대부분의 [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 글꼴은 사용 가능한 전체 [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 기능 중 하위 집합만 노출합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-121">Most [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] fonts expose only a subset of the total [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] features available.</span></span> [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)]<span data-ttu-id="42dda-122"> 글꼴은 다음과 같은 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-122"> fonts provide the following features.</span></span>  
  
-   <span data-ttu-id="42dda-123">합자, 위치 형식, 대체 문자 및 기타 글꼴 대체를 지원하는 문자와 문자 모양 간의 다양한 매핑</span><span class="sxs-lookup"><span data-stu-id="42dda-123">Rich mapping between characters and glyphs that support ligatures, positional forms, alternates, and other font substitutions.</span></span>  
  
-   <span data-ttu-id="42dda-124">2차원 위치 지정 및 문자 모양 첨부 지원</span><span class="sxs-lookup"><span data-stu-id="42dda-124">Support for two-dimensional positioning and glyph attachment.</span></span>  
  
-   <span data-ttu-id="42dda-125">명시적인 스크립트 및 언어 정보가 글꼴에 포함되어 텍스트 처리 응용 프로그램에서 동작을 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-125">Explicit script and language information contained in font, so a text-processing application can adjust its behavior accordingly.</span></span>  
  
 <span data-ttu-id="42dda-126">[!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 사양의 [“글꼴 파일 표”](https://www.microsoft.com/typography/otspec/otff.htm) 섹션에서 [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 레이아웃 표에 대해 자세히 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-126">The [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] Layout tables are described in more detail in the ["Font File Tables"](https://www.microsoft.com/typography/otspec/otff.htm) section of the [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] specification.</span></span>  
  
 <span data-ttu-id="42dda-127">이 개요의 나머지 부분에서는 확장성과 유연성을 시각적으로 흥미로운 일부 [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 의 속성에 의해 노출 되는 기능을 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-127">The remainder of this overview introduces the breadth and flexibility of some of the visually-interesting [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] features that are exposed by the properties of the <xref:System.Windows.Documents.Typography> object.</span></span> <span data-ttu-id="42dda-128">이 개체에 대한 자세한 내용은 [입력 체계 클래스](#typography_class)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="42dda-128">For more information on this object, see [Typography Class](#typography_class).</span></span>  
  
<a name="variants"></a>   
## <a name="variants"></a><span data-ttu-id="42dda-129">변형</span><span class="sxs-lookup"><span data-stu-id="42dda-129">Variants</span></span>  
 <span data-ttu-id="42dda-130">변형은 위 첨자 및 아래 첨자와 같은 다양한 입력 체계 스타일을 렌더링하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-130">Variants are used to render different typographic styles, such as superscripts and subscripts.</span></span>  
  
### <a name="superscripts-and-subscripts"></a><span data-ttu-id="42dda-131">위 첨자 및 아래 첨자</span><span class="sxs-lookup"><span data-stu-id="42dda-131">Superscripts and Subscripts</span></span>  
 <span data-ttu-id="42dda-132">합니다 <xref:System.Windows.Documents.Typography.Variants%2A> 속성을 사용 하면 위 첨자 및 아래 첨자 값을 설정 하는 [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 글꼴입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-132">The <xref:System.Windows.Documents.Typography.Variants%2A> property allows you to set superscript and subscript values for an [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] font.</span></span>  
  
 <span data-ttu-id="42dda-133">다음 텍스트는 Palatino Linotype 글꼴의 위 첨자를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-133">The following text displays superscripts for the Palatino Linotype font.</span></span>  
  
 <span data-ttu-id="42dda-134">![OpenType 위 첨자를 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont14.gif "opentypefont14")</span><span class="sxs-lookup"><span data-stu-id="42dda-134">![Text using OpenType superscripts](../../../../docs/framework/wpf/advanced/media/opentypefont14.gif "opentypefont14")</span></span>  
<span data-ttu-id="42dda-135">OpenType 위 첨자를 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-135">Text using OpenType superscripts</span></span>  
  
 <span data-ttu-id="42dda-136">다음 태그 예제에서는 속성을 사용 하 여 Palatino Linotype 글꼴의 위 첨자를 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-136">The following markup example shows how to define superscripts for the Palatino Linotype font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#12](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#12)]  
  
 <span data-ttu-id="42dda-137">다음 텍스트는 Palatino Linotype 글꼴의 아래 첨자를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-137">The following text displays subscripts for the Palatino Linotype font.</span></span>  
  
 <span data-ttu-id="42dda-138">![OpenType 아래 첨자를 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont15.gif "opentypefont15")</span><span class="sxs-lookup"><span data-stu-id="42dda-138">![Text using OpenType subscripts](../../../../docs/framework/wpf/advanced/media/opentypefont15.gif "opentypefont15")</span></span>  
<span data-ttu-id="42dda-139">OpenType 아래 첨자를 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-139">Text using OpenType subscripts</span></span>  
  
 <span data-ttu-id="42dda-140">다음 태그 예제에서는 속성을 사용 하 여 Palatino Linotype 글꼴의 아래 첨자를 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-140">The following markup example shows how to define subscripts for the Palatino Linotype font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#13](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#13)]  
  
### <a name="decorative-uses-of-superscripts-and-subscripts"></a><span data-ttu-id="42dda-141">위 첨자 및 아래 첨자의 장식 사용</span><span class="sxs-lookup"><span data-stu-id="42dda-141">Decorative Uses of Superscripts and Subscripts</span></span>  
 <span data-ttu-id="42dda-142">위 첨자와 아래 첨자를 사용하여 대/소문자 혼용 텍스트의 장식 효과를 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-142">You can also use superscripts and subscripts to create decorative effects of mixed case text.</span></span> <span data-ttu-id="42dda-143">다음 텍스트는 Palatino Linotype 글꼴의 위 첨자 및 아래 첨자 텍스트를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-143">The following text displays superscript and subscript text for the Palatino Linotype font.</span></span> <span data-ttu-id="42dda-144">대문자는 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-144">Note that the capitals are not affected.</span></span>  
  
 <span data-ttu-id="42dda-145">![OpenType 위 첨자 및 아래 첨자를 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont16.gif "opentypefont16")</span><span class="sxs-lookup"><span data-stu-id="42dda-145">![Text using OpenType superscripts and subscripts](../../../../docs/framework/wpf/advanced/media/opentypefont16.gif "opentypefont16")</span></span>  
<span data-ttu-id="42dda-146">OpenType 위 첨자 및 아래 첨자를 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-146">Text using OpenType superscripts and subscripts</span></span>  
  
 <span data-ttu-id="42dda-147">다음 태그 예제에서는 위 첨자 및 아래 첨자의 속성을 사용 하 여 글꼴을 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-147">The following markup example shows how to define superscripts and subscripts for a font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#14](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#14)]  
  
<a name="capitals"></a>   
## <a name="capitals"></a><span data-ttu-id="42dda-148">대문자</span><span class="sxs-lookup"><span data-stu-id="42dda-148">Capitals</span></span>  
 <span data-ttu-id="42dda-149">대문자는 대문자 스타일의 문자 모양으로 텍스트를 렌더링하는 일련의 입력 체계 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-149">Capitals are a set of typographical forms that render text in capital-styled glyphs.</span></span> <span data-ttu-id="42dda-150">일반적으로 텍스트를 모두 대문자로 렌더링하면 글자 사이의 간격이 너무 좁아 보이고 글자의 무게와 비율상 너무 무거워 보일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-150">Typically, when text is rendered as all capitals, the spacing between letters can appear too tight, and the weight and proportion of the letters too heavy.</span></span> [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)]<span data-ttu-id="42dda-151">은 작은 대문자, 꼬마 대문자, 제목 및 대문자 간격을 비롯하여 대문자에 대한 여러 가지 스타일 서식을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-151"> supports a number of styling formats for capitals, including small capitals, petite capitals, titling, and capital spacing.</span></span> <span data-ttu-id="42dda-152">이러한 스타일 서식을 사용하여 대문자 모양을 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-152">These styling formats allow you to control the appearance of capitals.</span></span>  
  
 <span data-ttu-id="42dda-153">다음 텍스트는 “SmallCaps” 및 “AllSmallCaps”로 스타일이 지정된 문자 앞에 Pescadero 글꼴의 표준 대문자를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-153">The following text displays standard capital letters for the Pescadero font, followed by the letters styled as "SmallCaps" and "AllSmallCaps".</span></span> <span data-ttu-id="42dda-154">이 경우 세 단어 모두 동일한 글꼴 크기가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-154">In this case, the same font size is used for all three words.</span></span>  
  
 <span data-ttu-id="42dda-155">![OpenType 대문자를 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont11.gif "opentypefont11")</span><span class="sxs-lookup"><span data-stu-id="42dda-155">![Text using OpenType capitals](../../../../docs/framework/wpf/advanced/media/opentypefont11.gif "opentypefont11")</span></span>  
<span data-ttu-id="42dda-156">OpenType 대문자를 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-156">Text using OpenType capitals</span></span>  
  
 <span data-ttu-id="42dda-157">다음 태그 예제에서는 속성을 사용 하 여 Pescadero 글꼴의 대문자를 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-157">The following markup example shows how to define capitals for the Pescadero font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span> <span data-ttu-id="42dda-158">“SmallCaps” 형식을 사용하는 경우 선행 대문자는 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-158">When the "SmallCaps" format is used, any leading capital letter is ignored.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#9](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#9)]  
  
### <a name="titling-capitals"></a><span data-ttu-id="42dda-159">제목 대문자</span><span class="sxs-lookup"><span data-stu-id="42dda-159">Titling Capitals</span></span>  
 <span data-ttu-id="42dda-160">제목 대문자는 무게와 비율이 더 가볍고 일반 대문자보다 세련된 느낌을 주도록 디자인되었습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-160">Titling capitals are lighter in weight and proportion and designed to give a more elegant look than normal capitals.</span></span> <span data-ttu-id="42dda-161">제목 대문자는 일반적으로 큰 글꼴 크기의 머리글로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-161">Titling capitals are typically used in larger font sizes as headings.</span></span> <span data-ttu-id="42dda-162">다음 텍스트는 Pescadero 글꼴의 일반 대문자 및 제목 대문자를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-162">The following text displays normal and titling capitals for the Pescadero font.</span></span> <span data-ttu-id="42dda-163">두 번째 줄에 있는 텍스트의 획(stem) 너비가 더 좁은 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-163">Notice the narrower stem widths of the text on the second line.</span></span>  
  
 <span data-ttu-id="42dda-164">![OpenType 제목 대문자를 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont20.gif "OpenTypeFont20")</span><span class="sxs-lookup"><span data-stu-id="42dda-164">![Text using OpenType titling capitals](../../../../docs/framework/wpf/advanced/media/opentypefont20.gif "OpenTypeFont20")</span></span>  
<span data-ttu-id="42dda-165">OpenType 제목 대문자를 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-165">Text using OpenType titling capitals</span></span>  
  
 <span data-ttu-id="42dda-166">다음 태그 예제에서는 속성을 사용 하 여 Pescadero 글꼴의 제목 대문자를 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-166">The following markup example shows how to define titling capitals for the Pescadero font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#OpenTypeFontSnippet17](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#opentypefontsnippet17)]  
  
### <a name="capital-spacing"></a><span data-ttu-id="42dda-167">대문자 간격</span><span class="sxs-lookup"><span data-stu-id="42dda-167">Capital Spacing</span></span>  
 <span data-ttu-id="42dda-168">대문자 간격은 텍스트에서 모두 대문자를 사용할 때 더 넓은 간격을 제공할 수 있도록 하는 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-168">Capital spacing is a feature that allows you to provide more spacing when using all capitals in text.</span></span> <span data-ttu-id="42dda-169">대문자는 대개 소문자와 함께 사용하도록 디자인되었습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-169">Capital letters are typically designed to blend with lowercase letters.</span></span> <span data-ttu-id="42dda-170">대문자와 소문자 사이에서는 적절해 보이는 간격이 모두 대문자를 사용할 때는 너무 좁게 보일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-170">Spacing that appears attractive between and a capital letter and a lowercase letter may look too tight when all capital letters are used.</span></span> <span data-ttu-id="42dda-171">다음 텍스트는 Pescadero 글꼴의 일반 간격 및 대문자 간격을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-171">The following text displays normal and capital spacing for the Pescadero font.</span></span>  
  
 <span data-ttu-id="42dda-172">![OpenType 대문자 간격을 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont21.gif "OpenTypeFont21")</span><span class="sxs-lookup"><span data-stu-id="42dda-172">![Text using OpenType capital spacing](../../../../docs/framework/wpf/advanced/media/opentypefont21.gif "OpenTypeFont21")</span></span>  
<span data-ttu-id="42dda-173">OpenType 대문자 간격을 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-173">Text using OpenType capital spacing</span></span>  
  
 <span data-ttu-id="42dda-174">다음 태그 예제에서는 속성을 사용 하 여 Pescadero 글꼴의 대문자 간격을 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-174">The following markup example shows how to define capital spacing for the Pescadero font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#OpenTypeFontSnippet18](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#opentypefontsnippet18)]  
  
<a name="ligatures"></a>   
## <a name="ligatures"></a><span data-ttu-id="42dda-175">합자</span><span class="sxs-lookup"><span data-stu-id="42dda-175">Ligatures</span></span>  
 <span data-ttu-id="42dda-176">합자는 읽기 쉽거나 보기 좋은 텍스트를 만들기 위해 단일 문자 모양으로 구성된 두 개 이상의 문자 모양입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-176">Ligatures are two or more glyphs that are formed into a single glyph in order to create more readable or attractive text.</span></span> [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)]<span data-ttu-id="42dda-177"> 글꼴은 네 가지 형식의 합자를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-177"> fonts support four types of ligatures:</span></span>  
  
-   <span data-ttu-id="42dda-178">**표준 합자**.</span><span class="sxs-lookup"><span data-stu-id="42dda-178">**Standard ligatures**.</span></span> <span data-ttu-id="42dda-179">가독성을 향상시키기 위해 디자인되었습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-179">Designed to enhance readability.</span></span> <span data-ttu-id="42dda-180">표준 합자에는 “fi”, “fl” 및 “ff”가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-180">Standard ligatures include "fi", "fl", and "ff".</span></span>  
  
-   <span data-ttu-id="42dda-181">**컨텍스트 합자**.</span><span class="sxs-lookup"><span data-stu-id="42dda-181">**Contextual ligatures**.</span></span> <span data-ttu-id="42dda-182">합자를 구성하는 문자 간에 더 나은 결합 동작을 제공하여 가독성을 높이도록 디자인되었습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-182">Designed to enhance readability by providing better joining behavior between the characters that make up the ligature.</span></span>  
  
-   <span data-ttu-id="42dda-183">**임의 합자**.</span><span class="sxs-lookup"><span data-stu-id="42dda-183">**Discretionary ligatures**.</span></span> <span data-ttu-id="42dda-184">장식용으로 디자인되었으며 가독성을 위해 별도로 디자인된 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-184">Designed to be ornamental, and not specifically designed for readability.</span></span>  
  
-   <span data-ttu-id="42dda-185">**기록 합자**.</span><span class="sxs-lookup"><span data-stu-id="42dda-185">**Historical ligatures**.</span></span> <span data-ttu-id="42dda-186">기록용으로 디자인되었으며 가독성을 위해 별도로 디자인된 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-186">Designed to be historical, and not specifically designed for readability.</span></span>  
  
 <span data-ttu-id="42dda-187">다음 텍스트는 Pericles 글꼴에 대한 표준 합자 문자 모양을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-187">The following text displays standard ligature glyphs for the Pericles font.</span></span>  
  
 <span data-ttu-id="42dda-188">![OpenType 표준 합자를 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont04.gif "opentypefont04")</span><span class="sxs-lookup"><span data-stu-id="42dda-188">![Text using OpenType standard ligatures](../../../../docs/framework/wpf/advanced/media/opentypefont04.gif "opentypefont04")</span></span>  
<span data-ttu-id="42dda-189">OpenType 표준 합자를 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-189">Text using OpenType standard ligatures</span></span>  
  
 <span data-ttu-id="42dda-190">다음 태그 예제에서는 속성을 사용 하 여 Pericles 글꼴에 대 한 표준 합자 문자 모양을 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-190">The following markup example shows how to define standard ligature glyphs for the Pericles font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#4](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#4)]  
  
 <span data-ttu-id="42dda-191">다음 텍스트는 Pericles 글꼴의 임의 합자 문자 모양을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-191">The following text displays discretionary ligature glyphs for the Pericles font.</span></span>  
  
 <span data-ttu-id="42dda-192">![OpenType 임의 합자를 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont05.gif "opentypefont05")</span><span class="sxs-lookup"><span data-stu-id="42dda-192">![Text using OpenType discretionary ligatures](../../../../docs/framework/wpf/advanced/media/opentypefont05.gif "opentypefont05")</span></span>  
<span data-ttu-id="42dda-193">OpenType 임의 합자를 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-193">Text using OpenType discretionary ligatures</span></span>  
  
 <span data-ttu-id="42dda-194">다음 태그 예제에서는 속성을 사용 하 여 Pericles 글꼴에 대 한 임의 합자 문자 모양을 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-194">The following markup example shows how to define discretionary ligature glyphs for the Pericles font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#5](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#5)]  
  
 <span data-ttu-id="42dda-195">기본적으로 [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)]의 [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 글꼴은 표준 합자를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-195">By default, [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] fonts in [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] enable standard ligatures.</span></span> <span data-ttu-id="42dda-196">예를 들어 Palatino Linotype 글꼴을 사용하면 표준 합자 “fi”, “ff”및 “fl”이 결합된 문자 모양으로 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-196">For example, if you use the Palatino Linotype font, the standard ligatures "fi", "ff", and "fl" appear as a combined character glyph.</span></span> <span data-ttu-id="42dda-197">각 표준 합자의 문자 쌍이 서로 붙어 있음을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-197">Notice that the pair of characters for each standard ligature touch each other.</span></span>  
  
 <span data-ttu-id="42dda-198">![OpenType 표준 합자를 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont06.gif "opentypefont06")</span><span class="sxs-lookup"><span data-stu-id="42dda-198">![Text using OpenType standard ligatures](../../../../docs/framework/wpf/advanced/media/opentypefont06.gif "opentypefont06")</span></span>  
<span data-ttu-id="42dda-199">OpenType 표준 합자를 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-199">Text using OpenType standard ligatures</span></span>  
  
 <span data-ttu-id="42dda-200">그러나 표준 합자 기능을 사용하지 않도록 설정하여 “ff”와 같이 표준 합자가 결합된 문자 모양이 아닌 두 개의 별도 문자 모양으로 표시되도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-200">However, you can disable standard ligature features so that a standard ligature such as "ff" displays as two separate glyphs, rather than as a combined character glyph.</span></span>  
  
 <span data-ttu-id="42dda-201">![비활성화 된 OpenType 표준 합자를 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont07.gif "opentypefont07")</span><span class="sxs-lookup"><span data-stu-id="42dda-201">![Text using disabled OpenType standard ligatures](../../../../docs/framework/wpf/advanced/media/opentypefont07.gif "opentypefont07")</span></span>  
<span data-ttu-id="42dda-202">비활성화된 OpenType 표준 합자를 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-202">Text using disabled OpenType standard ligatures</span></span>  
  
 <span data-ttu-id="42dda-203">다음 태그 예제에서는 속성을 사용 하 여 Palatino Linotype 글꼴에 대 한 표준 합자 문자 모양을 사용 하지 않도록 설정 하는 방법을 보여 줍니다는 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-203">The following markup example shows how to disable standard ligature glyphs for the Palatino Linotype font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#6](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#6)]  
  
<a name="swashes"></a>   
## <a name="swashes"></a><span data-ttu-id="42dda-204">선단 장식</span><span class="sxs-lookup"><span data-stu-id="42dda-204">Swashes</span></span>  
 <span data-ttu-id="42dda-205">선단 장식은 종종 붓글씨와 관련된 정교한 장식을 사용하는 장식용 문자 모양입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-205">Swashes are decorative glyphs that use elaborate ornamentation often associated with calligraphy.</span></span> <span data-ttu-id="42dda-206">다음 텍스트는 Pescadero 글꼴의 표준 및 선단 장식 문자 모양을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-206">The following text displays standard and swash glyphs for the Pescadero font.</span></span>  
  
 <span data-ttu-id="42dda-207">![OpenType 표준 및 선단 장식 문자 모양을 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont08.gif "opentypefont08")</span><span class="sxs-lookup"><span data-stu-id="42dda-207">![Text using OpenType standard and swash glyphs](../../../../docs/framework/wpf/advanced/media/opentypefont08.gif "opentypefont08")</span></span>  
<span data-ttu-id="42dda-208">OpenType 표준 및 선단 장식 문자 모양을 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-208">Text using OpenType standard and swash glyphs</span></span>  
  
 <span data-ttu-id="42dda-209">선단 장식은 종종 이벤트 발표와 같은 짧은 문장에서 장식 요소로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-209">Swashes are often used as decorative elements in short phrases such as event announcements.</span></span> <span data-ttu-id="42dda-210">다음 텍스트는 선단 장식을 사용하여 이벤트 이름의 대문자를 강조합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-210">The following text uses swashes to emphasize the capital letters of the name of the event.</span></span>  
  
 <span data-ttu-id="42dda-211">![OpenType 선단 장식을 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont09.gif "opentypefont09")</span><span class="sxs-lookup"><span data-stu-id="42dda-211">![Text using OpenType swashes](../../../../docs/framework/wpf/advanced/media/opentypefont09.gif "opentypefont09")</span></span>  
<span data-ttu-id="42dda-212">OpenType 선단 장식을 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-212">Text using OpenType swashes</span></span>  
  
 <span data-ttu-id="42dda-213">다음 태그 예제에서는 속성을 사용 하는 글꼴에 대 한 선단 장식을 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-213">The following markup example shows how to define swashes for a font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#7](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#7)]  
  
### <a name="contextual-swashes"></a><span data-ttu-id="42dda-214">컨텍스트 선단 장식</span><span class="sxs-lookup"><span data-stu-id="42dda-214">Contextual Swashes</span></span>  
 <span data-ttu-id="42dda-215">특정 조합의 선단 장식 문자 모양은 인접 문자에 내림 영자가 겹치는 것과 같이 보기 좋지 않은 모양이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-215">Certain combinations of swash glyphs can cause an unattractive appearance, such as overlapping descenders on adjacent letters.</span></span> <span data-ttu-id="42dda-216">컨텍스트 선단 장식을 사용하면 더 좋은 모양을 만드는 대체 선단 장식 문자 모양을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-216">Using a contextual swash allows you to use a substitute swash glyph that produces a better appearance.</span></span> <span data-ttu-id="42dda-217">다음 텍스트는 동일한 단어에 컨텍스트 선단 장식이 적용되기 전후의 모습을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-217">The following text shows the same word before and after a contextual swash is applied.</span></span>  
  
 <span data-ttu-id="42dda-218">![OpenType 컨텍스트 선단 장식을 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont19.gif "OpenTypeFont19")</span><span class="sxs-lookup"><span data-stu-id="42dda-218">![Text using OpenType contextual swashes](../../../../docs/framework/wpf/advanced/media/opentypefont19.gif "OpenTypeFont19")</span></span>  
<span data-ttu-id="42dda-219">OpenType 컨텍스트 선단 장식을 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-219">Text using OpenType contextual swashes</span></span>  
  
 <span data-ttu-id="42dda-220">다음 태그 예제에서는 속성을 사용 하 여 Pescadero 글꼴의 컨텍스트 선단 장식을 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-220">The following markup example shows how to define a contextual swash for the Pescadero font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#OpenTypeFontSnippet16](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#opentypefontsnippet16)]  
  
<a name="alternates"></a>   
## <a name="alternates"></a><span data-ttu-id="42dda-221">대체 문자</span><span class="sxs-lookup"><span data-stu-id="42dda-221">Alternates</span></span>  
 <span data-ttu-id="42dda-222">대체 문자는 표준 문자 모양으로 대체될 수 있는 문자 모양입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-222">Alternates are glyphs that can be substituted for a standard glyph.</span></span> <span data-ttu-id="42dda-223">다음 예제에서 사용된 Pericles 글꼴과 같은 [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 글꼴에는 텍스트의 다른 모양을 만드는 데 사용할 수 있는 대체 문자 모양이 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-223">[!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] fonts, such as the Pericles font used in the following examples, can contain alternate glyphs that you can use to create different appearances for text.</span></span> <span data-ttu-id="42dda-224">다음 텍스트는 Pericles 글꼴의 표준 문자 모양을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-224">The following text displays standard glyphs for the Pericles font.</span></span>  
  
 <span data-ttu-id="42dda-225">![OpenType 표준 문자 모양을 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont01.gif "opentypefont01")</span><span class="sxs-lookup"><span data-stu-id="42dda-225">![Text using OpenType standard glyphs](../../../../docs/framework/wpf/advanced/media/opentypefont01.gif "opentypefont01")</span></span>  
<span data-ttu-id="42dda-226">OpenType 표준 문자 모양을 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-226">Text using OpenType standard glyphs</span></span>  
  
 <span data-ttu-id="42dda-227">Pericles [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 글꼴에는 표준 문자 모양 집합에 스타일 대체 문자를 제공하는 추가 문자 모양이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-227">The Pericles [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] font contains additional glyphs that provide stylistic alternates to the standard set of glyphs.</span></span> <span data-ttu-id="42dda-228">다음 텍스트는 스타일 대체 문자 모양을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-228">The following text displays stylistic alternate glyphs.</span></span>  
  
 <span data-ttu-id="42dda-229">![OpenType 스타일 대체 문자 모양을 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont02.gif "opentypefont02")</span><span class="sxs-lookup"><span data-stu-id="42dda-229">![Text using OpenType stylistic alternate glyphs](../../../../docs/framework/wpf/advanced/media/opentypefont02.gif "opentypefont02")</span></span>  
<span data-ttu-id="42dda-230">OpenType 스타일 대체 문자 모양을 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-230">Text using OpenType stylistic alternate glyphs</span></span>  
  
 <span data-ttu-id="42dda-231">다음 태그 예제에서는 속성을 사용 하 여 Pericles 글꼴에 대 한 스타일 대체 문자 모양을 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-231">The following markup example shows how to define stylistic alternate glyphs for the Pericles font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#2)]  
  
 <span data-ttu-id="42dda-232">다음 텍스트는 Pericles 글꼴에 대한 여러 가지 다른 스타일 대체 문자 모양을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-232">The following text displays several other stylistic alternate glyphs for the Pericles font.</span></span>  
  
 <span data-ttu-id="42dda-233">![OpenType 스타일 대체 문자 모양을 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont03.gif "opentypefont03")</span><span class="sxs-lookup"><span data-stu-id="42dda-233">![Text using OpenType stylistic alternate glyphs](../../../../docs/framework/wpf/advanced/media/opentypefont03.gif "opentypefont03")</span></span>  
<span data-ttu-id="42dda-234">OpenType 스타일 대체 문자 모양을 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-234">Text using OpenType stylistic alternate glyphs</span></span>  
  
 <span data-ttu-id="42dda-235">다음 태그 예제에서는 이러한 다른 스타일 대체 문자 모양을 정의하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-235">The following markup example shows how to define these other stylistic alternate glyphs.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#3)]  
  
### <a name="random-contextual-alternates"></a><span data-ttu-id="42dda-236">임의 컨텍스트 대체 문자</span><span class="sxs-lookup"><span data-stu-id="42dda-236">Random Contextual Alternates</span></span>  
 <span data-ttu-id="42dda-237">임의 컨텍스트 대체 문자는 단일 문자에 대해 여러 개의 대체 문자 모양을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-237">Random contextual alternates provide multiple substitute glyphs for a single character.</span></span> <span data-ttu-id="42dda-238">이 기능은 스크립트 유형의 글꼴로 구현될 때 임의로 선택한 외관상 약간 다른 문자 집합을 사용하여 필기를 시뮬레이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-238">When implemented with script-type fonts, this feature can simulate handwriting by using of a set of randomly chosen glyphs with slight differences in appearance.</span></span> <span data-ttu-id="42dda-239">다음 텍스트는 Lindsey 글꼴에 대한 임의 컨텍스트 대체 문자를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-239">The following text uses random contextual alternates for the Lindsey font.</span></span> <span data-ttu-id="42dda-240">문자 “a”의 모양이 약간 다른 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-240">Notice that the letter "a" varies slightly in appearance</span></span>  
  
 <span data-ttu-id="42dda-241">![OpenType 임의 컨텍스트 대체 문자를 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont23.gif "OpenTypeFont23")</span><span class="sxs-lookup"><span data-stu-id="42dda-241">![Text using OpenType random contextual alternates](../../../../docs/framework/wpf/advanced/media/opentypefont23.gif "OpenTypeFont23")</span></span>  
<span data-ttu-id="42dda-242">OpenType 임의 컨텍스트 대체 항목을 사용한 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-242">Text using OpenType random contextual alternates</span></span>  
  
 <span data-ttu-id="42dda-243">다음 태그 예제에서는 속성을 사용 하 여 Lindsey 글꼴에 대 한 임의 컨텍스트 대체 문자를 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-243">The following markup example shows how to define random contextual alternates for the Lindsey font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#OpenTypeFontSnippet20](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/Window1.xaml#opentypefontsnippet20)]  
  
### <a name="historical-forms"></a><span data-ttu-id="42dda-244">기록 형식</span><span class="sxs-lookup"><span data-stu-id="42dda-244">Historical Forms</span></span>  
 <span data-ttu-id="42dda-245">기록 형식은 과거에는 일반적이었던 입력 체계 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-245">Historical forms are typographic conventions that were common in the past.</span></span> <span data-ttu-id="42dda-246">다음 텍스트는 Palatino Linotype 글꼴에 대한 기록 형식 문자 모양을 사용하여 “Boston, Massachusetts” 구문을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-246">The following text displays the phrase, "Boston, Massachusetts", using an historical form of glyphs for the Palatino Linotype font.</span></span>  
  
 <span data-ttu-id="42dda-247">![OpenType 기록 폼을 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont10.gif "opentypefont10")</span><span class="sxs-lookup"><span data-stu-id="42dda-247">![Text using OpenType historical forms](../../../../docs/framework/wpf/advanced/media/opentypefont10.gif "opentypefont10")</span></span>  
<span data-ttu-id="42dda-248">OpenType 기록 폼을 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-248">Text using OpenType historical forms</span></span>  
  
 <span data-ttu-id="42dda-249">다음 태그 예제에서는 속성을 사용 하 여 Palatino Linotype 글꼴에 대 한 기록 폼을 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-249">The following markup example shows how to define historical forms for the Palatino Linotype font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#8](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#8)]  
  
<a name="numerical_styles"></a>   
## <a name="numerical-styles"></a><span data-ttu-id="42dda-250">숫자 스타일</span><span class="sxs-lookup"><span data-stu-id="42dda-250">Numerical Styles</span></span>  
 <span data-ttu-id="42dda-251">OpenType 글꼴은 텍스트의 숫자 값으로 사용할 수 있는 많은 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-251">OpenType fonts support a large number of features that can be used with numerical values in text.</span></span>  
  
### <a name="fractions"></a><span data-ttu-id="42dda-252">소수</span><span class="sxs-lookup"><span data-stu-id="42dda-252">Fractions</span></span>  
 [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)]<span data-ttu-id="42dda-253"> 글꼴은 슬래시를 사용하거나 위아래로 표현된 분수 스타일을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-253"> fonts support styles for fractions, including slashed and stacked.</span></span>  
  
 <span data-ttu-id="42dda-254">다음 텍스트는 Palatino Linotype 글꼴의 분수 스타일을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-254">The following text displays fraction styles for the Palatino Linotype font.</span></span>  
  
 <span data-ttu-id="42dda-255">![OpenType를 사용 하 여 텍스트 슬래시 및 상하 형 분수](../../../../docs/framework/wpf/advanced/media/opentypefont12.gif "opentypefont12")</span><span class="sxs-lookup"><span data-stu-id="42dda-255">![Text using OpenType slashed and stacked fractions](../../../../docs/framework/wpf/advanced/media/opentypefont12.gif "opentypefont12")</span></span>  
<span data-ttu-id="42dda-256">OpenType 슬래시 및 상하형 분수를 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-256">Text using OpenType slashed and stacked fractions</span></span>  
  
 <span data-ttu-id="42dda-257">다음 태그 예제에서는 속성을 사용 하 여 Palatino Linotype 글꼴의 분수 스타일을 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-257">The following markup example shows how to define fraction styles for the Palatino Linotype font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#10](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#10)]  
  
### <a name="old-style-numerals"></a><span data-ttu-id="42dda-258">이전 스타일 숫자</span><span class="sxs-lookup"><span data-stu-id="42dda-258">Old Style Numerals</span></span>  
 [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)]<span data-ttu-id="42dda-259"> 글꼴은 이전 스타일 숫자 형식을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-259"> fonts support an old style numeral format.</span></span> <span data-ttu-id="42dda-260">이 형식은 더 이상 표준이 아닌 스타일의 숫자를 표시할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-260">This format is useful for displaying numerals in styles that are no longer standard.</span></span> <span data-ttu-id="42dda-261">다음 텍스트는 Palatino Linotype 글꼴의 표준 및 이전 스타일 숫자 형식으로 된 18세기 날짜를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-261">The following text displays an 18th century date in standard and old style numeral formats for the Palatino Linotype font.</span></span>  
  
 <span data-ttu-id="42dda-262">![OpenType 이전 스타일 숫자를 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont24.gif "OpenTypeFont24")</span><span class="sxs-lookup"><span data-stu-id="42dda-262">![Text using OpenType old style numerals](../../../../docs/framework/wpf/advanced/media/opentypefont24.gif "OpenTypeFont24")</span></span>  
<span data-ttu-id="42dda-263">OpenType 이전 스타일 숫자를 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-263">Text using OpenType old style numerals</span></span>  
  
 <span data-ttu-id="42dda-264">다음 텍스트는 Palatino Linotype 글꼴의 표준 숫자 뒤에 이전 스타일 숫자를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-264">The following text displays standard numerals for the Palatino Linotype font, followed by old style numerals.</span></span>  
  
 <span data-ttu-id="42dda-265">![OpenType 이전 스타일 숫자 집합을 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont13.gif "opentypefont13")</span><span class="sxs-lookup"><span data-stu-id="42dda-265">![Text using OpenType old style numeral sets](../../../../docs/framework/wpf/advanced/media/opentypefont13.gif "opentypefont13")</span></span>  
<span data-ttu-id="42dda-266">OpenType의 이전 스타일 숫자 집합을 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-266">Text using OpenType old style numeral sets</span></span>  
  
 <span data-ttu-id="42dda-267">다음 태그 예제에서는 속성을 사용 하 여 Palatino Linotype 글꼴에 대 한 이전 스타일 숫자를 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-267">The following markup example shows how to define old style numerals for the Palatino Linotype font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#11](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#11)]  
  
### <a name="proportional-and-tabular-figures"></a><span data-ttu-id="42dda-268">가변 폭 및 테이블 형식 숫자</span><span class="sxs-lookup"><span data-stu-id="42dda-268">Proportional and Tabular Figures</span></span>  
 [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)]<span data-ttu-id="42dda-269"> 글꼴은 숫자를 사용할 때 너비 정렬을 제어하기 위해 가변 폭 및 테이블 형식 숫자 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-269"> fonts support a proportional and tabular figure feature to control the alignment of widths when using numerals.</span></span> <span data-ttu-id="42dda-270">가변 폭 숫자는 각 숫자의 너비를 다르게 처리합니다. 예를 들어 “1”은 “5”보다 너비가 좁습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-270">Proportional figures treat each numeral as having a different width—"1" is narrower than "5".</span></span> <span data-ttu-id="42dda-271">테이블 형식 숫자는 같은 너비의 숫자로 처리되어 세로로 정렬되므로 금융 형식 정보의 가독성이 높아집니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-271">Tabular figures are treated as equal-width numerals so that they align vertically, which increases the readability of financial type information.</span></span>  
  
 <span data-ttu-id="42dda-272">다음 텍스트는 Miramonte 글꼴을 사용하여 첫 번째 열에 두 개의 가변 폭 숫자를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-272">The following text displays two proportional figures in the first column using the Miramonte font.</span></span> <span data-ttu-id="42dda-273">숫자 “5”와 “1” 사이의 너비 차이를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-273">Note the difference in width between the numerals "5" and "1".</span></span> <span data-ttu-id="42dda-274">두 번째 열은 테이블 형식 숫자 기능을 사용하여 너비가 조정된 동일한 두 개의 숫자 값을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-274">The second column shows the same two numeric values with the widths adjusted by using the tabular figure feature.</span></span>  
  
 <span data-ttu-id="42dda-275">![OpenType 가변 폭 및 테이블 형식 숫자를 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont22.gif "OpenTypeFont22")</span><span class="sxs-lookup"><span data-stu-id="42dda-275">![Text using OpenType proportional & tabular figures](../../../../docs/framework/wpf/advanced/media/opentypefont22.gif "OpenTypeFont22")</span></span>  
<span data-ttu-id="42dda-276">OpenType 가변 폭 및 테이블 형식 숫자를 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-276">Text using OpenType proportional and tabular figures</span></span>  
  
 <span data-ttu-id="42dda-277">다음 태그 예제에서는 속성을 사용 하 여 Miramonte 글꼴의 가변 폭 및 테이블 형식 숫자를 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-277">The following markup example shows how to define proportional and tabular figures for the Miramonte font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#OpenTypeFontSnippet19](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/Window1.xaml#opentypefontsnippet19)]  
  
### <a name="slashed-zero"></a><span data-ttu-id="42dda-278">슬래시 0</span><span class="sxs-lookup"><span data-stu-id="42dda-278">Slashed Zero</span></span>  
 [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)]<span data-ttu-id="42dda-279"> 글꼴은 문자 “O”와 숫자 “0”의 차이를 강조하기 위해 슬래시 0 숫자 형식을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-279"> fonts support a slashed zero numeral format to emphasize the difference between the letter "O" and the numeral "0".</span></span> <span data-ttu-id="42dda-280">슬래시 0 숫자는 금융 정보 및 비즈니스 정보의 식별자에 주로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-280">The slashed zero numeral is often used for identifiers in financial and business information.</span></span>  
  
 <span data-ttu-id="42dda-281">다음 텍스트는 Miramonte 글꼴을 사용하는 샘플 주문 식별자를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-281">The following text displays a sample order identifier using the Miramonte font.</span></span> <span data-ttu-id="42dda-282">첫 번째 줄에는 표준 숫자가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-282">The first line uses standard numerals.</span></span> <span data-ttu-id="42dda-283">두 번째 줄에서는 대문자 “O” 문자와의 대비를 높이기 위해 슬래시 0 숫자가 사용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-283">The second line used slashed zero numerals to provide better contrast with the uppercase "O" letter.</span></span>  
  
 <span data-ttu-id="42dda-284">![OpenType를 사용 하 여 텍스트의 슬래시 0 숫자](../../../../docs/framework/wpf/advanced/media/opentypefont17.gif "OpenTypeFont17")</span><span class="sxs-lookup"><span data-stu-id="42dda-284">![Text using OpenType slashed zero numerals](../../../../docs/framework/wpf/advanced/media/opentypefont17.gif "OpenTypeFont17")</span></span>  
<span data-ttu-id="42dda-285">OpenType 슬래시 0 숫자를 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-285">Text using OpenType slashed zero numerals</span></span>  
  
 <span data-ttu-id="42dda-286">다음 태그 예제에서는 정의 하는 방법을 보여 줍니다 슬래시 0 숫자의 속성을 사용 하 여 Miramonte 글꼴의 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-286">The following markup example shows how to define slashed zero numerals for the Miramonte font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#OpenTypeFontSnippet15](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#opentypefontsnippet15)]  
  
<a name="typography_class"></a>   
## <a name="typography-class"></a><span data-ttu-id="42dda-287">입력 체계 클래스</span><span class="sxs-lookup"><span data-stu-id="42dda-287">Typography Class</span></span>  
 <span data-ttu-id="42dda-288"><xref:System.Windows.Documents.Typography> 개체 집합 기능을 노출 하는 [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 글꼴 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-288">The <xref:System.Windows.Documents.Typography> object exposes the set of features that an [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] font supports.</span></span> <span data-ttu-id="42dda-289">속성을 설정 하 여 <xref:System.Windows.Documents.Typography> 태그에서 쉽게 작성할 수 있습니다 활용 하는 문서 [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-289">By setting the properties of <xref:System.Windows.Documents.Typography> in markup, you can easily author documents that take advantage of [!INCLUDE[TLA#tla_opentype](../../../../includes/tlasharptla-opentype-md.md)] features.</span></span>  
  
 <span data-ttu-id="42dda-290">다음 텍스트는 “SmallCaps” 및 “AllSmallCaps”로 스타일이 지정된 문자 앞에 Pescadero 글꼴의 표준 대문자를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-290">The following text displays standard capital letters for the Pescadero font, followed by the letters styled as "SmallCaps" and "AllSmallCaps".</span></span> <span data-ttu-id="42dda-291">이 경우 세 단어 모두 동일한 글꼴 크기가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-291">In this case, the same font size is used for all three words.</span></span>  
  
 <span data-ttu-id="42dda-292">![OpenType 대문자를 사용 하 여 텍스트](../../../../docs/framework/wpf/advanced/media/opentypefont11.gif "opentypefont11")</span><span class="sxs-lookup"><span data-stu-id="42dda-292">![Text using OpenType capitals](../../../../docs/framework/wpf/advanced/media/opentypefont11.gif "opentypefont11")</span></span>  
<span data-ttu-id="42dda-293">OpenType 대문자를 사용하는 텍스트</span><span class="sxs-lookup"><span data-stu-id="42dda-293">Text using OpenType capitals</span></span>  
  
 <span data-ttu-id="42dda-294">다음 태그 예제에서는 속성을 사용 하 여 Pescadero 글꼴의 대문자를 정의 하는 방법을 보여 줍니다는 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-294">The following markup example shows how to define capitals for the Pescadero font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span> <span data-ttu-id="42dda-295">“SmallCaps” 형식을 사용하는 경우 선행 대문자는 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-295">When the "SmallCaps" format is used, any leading capital letter is ignored.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#9](../../../../samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#9)]  
  
 <span data-ttu-id="42dda-296">다음 코드 예제에서는 이전 태그 예제와 동일한 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-296">The following code example accomplishes the same task as the previous markup example.</span></span>  
  
 [!code-csharp[TypographyCodeSnippets#TypographyCodeSnippet1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TypographyCodeSnippets/CSharp/Page1.xaml.cs#typographycodesnippet1)]
 [!code-vb[TypographyCodeSnippets#TypographyCodeSnippet1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TypographyCodeSnippets/visualbasic/page1.xaml.vb#typographycodesnippet1)]  
  
### <a name="typography-class-properties"></a><span data-ttu-id="42dda-297">입력 체계 클래스 속성</span><span class="sxs-lookup"><span data-stu-id="42dda-297">Typography Class Properties</span></span>  
 <span data-ttu-id="42dda-298">다음 표에서 속성, 값 및의 기본 설정을 합니다 <xref:System.Windows.Documents.Typography> 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42dda-298">The following table lists the properties, values, and default settings of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
|<span data-ttu-id="42dda-299">속성</span><span class="sxs-lookup"><span data-stu-id="42dda-299">Property</span></span>|<span data-ttu-id="42dda-300">값</span><span class="sxs-lookup"><span data-stu-id="42dda-300">Value(s)</span></span>|<span data-ttu-id="42dda-301">기본값</span><span class="sxs-lookup"><span data-stu-id="42dda-301">Default Value</span></span>|  
|--------------|----------------|-------------------|  
|<xref:System.Windows.Documents.Typography.AnnotationAlternates%2A>|<span data-ttu-id="42dda-302">숫자 값-바이트</span><span class="sxs-lookup"><span data-stu-id="42dda-302">Numeric value - byte</span></span>|<span data-ttu-id="42dda-303">0</span><span class="sxs-lookup"><span data-stu-id="42dda-303">0</span></span>|  
|<xref:System.Windows.Documents.Typography.Capitals%2A>|<span data-ttu-id="42dda-304"><xref:System.Windows.FontCapitals.AllPetiteCaps> &#124; <xref:System.Windows.FontCapitals.AllSmallCaps> &#124; <xref:System.Windows.FontCapitals.Normal> &#124; <xref:System.Windows.FontCapitals.PetiteCaps> &#124; <xref:System.Windows.FontCapitals.SmallCaps> &#124; <xref:System.Windows.FontCapitals.Titling> &#124; <xref:System.Windows.FontCapitals.Unicase></span><span class="sxs-lookup"><span data-stu-id="42dda-304"><xref:System.Windows.FontCapitals.AllPetiteCaps> &#124; <xref:System.Windows.FontCapitals.AllSmallCaps> &#124; <xref:System.Windows.FontCapitals.Normal> &#124; <xref:System.Windows.FontCapitals.PetiteCaps> &#124; <xref:System.Windows.FontCapitals.SmallCaps> &#124; <xref:System.Windows.FontCapitals.Titling> &#124; <xref:System.Windows.FontCapitals.Unicase></span></span>|<xref:System.Windows.FontCapitals.Normal?displayProperty=nameWithType>|  
|<xref:System.Windows.Documents.Typography.CapitalSpacing%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.CaseSensitiveForms%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.ContextualAlternates%2A>|<xref:System.Boolean>|`true`|  
|<xref:System.Windows.Documents.Typography.ContextualLigatures%2A>|<xref:System.Boolean>|`true`|  
|<xref:System.Windows.Documents.Typography.ContextualSwashes%2A>|<span data-ttu-id="42dda-305">숫자 값-바이트</span><span class="sxs-lookup"><span data-stu-id="42dda-305">Numeric value - byte</span></span>|<span data-ttu-id="42dda-306">0</span><span class="sxs-lookup"><span data-stu-id="42dda-306">0</span></span>|  
|<xref:System.Windows.Documents.Typography.DiscretionaryLigatures%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.EastAsianExpertForms%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.EastAsianLanguage%2A>|<span data-ttu-id="42dda-307"><xref:System.Windows.FontEastAsianLanguage.HojoKanji> &#124; <xref:System.Windows.FontEastAsianLanguage.Jis04> &#124; <xref:System.Windows.FontEastAsianLanguage.Jis78> &#124; <xref:System.Windows.FontEastAsianLanguage.Jis83> &#124; <xref:System.Windows.FontEastAsianLanguage.Jis90> &#124; <xref:System.Windows.FontEastAsianLanguage.NlcKanji> &#124; <xref:System.Windows.FontEastAsianLanguage.Normal> &#124; <xref:System.Windows.FontEastAsianLanguage.Simplified> &#124; <xref:System.Windows.FontEastAsianLanguage.Traditional> &#124; <xref:System.Windows.FontEastAsianLanguage.TraditionalNames></span><span class="sxs-lookup"><span data-stu-id="42dda-307"><xref:System.Windows.FontEastAsianLanguage.HojoKanji> &#124; <xref:System.Windows.FontEastAsianLanguage.Jis04> &#124; <xref:System.Windows.FontEastAsianLanguage.Jis78> &#124; <xref:System.Windows.FontEastAsianLanguage.Jis83> &#124; <xref:System.Windows.FontEastAsianLanguage.Jis90> &#124; <xref:System.Windows.FontEastAsianLanguage.NlcKanji> &#124; <xref:System.Windows.FontEastAsianLanguage.Normal> &#124; <xref:System.Windows.FontEastAsianLanguage.Simplified> &#124; <xref:System.Windows.FontEastAsianLanguage.Traditional> &#124; <xref:System.Windows.FontEastAsianLanguage.TraditionalNames></span></span>|<xref:System.Windows.FontEastAsianLanguage.Normal?displayProperty=nameWithType>|  
|<xref:System.Windows.Documents.Typography.EastAsianWidths%2A>|<span data-ttu-id="42dda-308"><xref:System.Windows.FontEastAsianWidths.Full> &#124; <xref:System.Windows.FontEastAsianWidths.Half> &#124; <xref:System.Windows.FontEastAsianWidths.Normal> &#124; <xref:System.Windows.FontEastAsianWidths.Proportional> &#124; <xref:System.Windows.FontEastAsianWidths.Quarter> &#124; <xref:System.Windows.FontEastAsianWidths.Third></span><span class="sxs-lookup"><span data-stu-id="42dda-308"><xref:System.Windows.FontEastAsianWidths.Full> &#124; <xref:System.Windows.FontEastAsianWidths.Half> &#124; <xref:System.Windows.FontEastAsianWidths.Normal> &#124; <xref:System.Windows.FontEastAsianWidths.Proportional> &#124; <xref:System.Windows.FontEastAsianWidths.Quarter> &#124; <xref:System.Windows.FontEastAsianWidths.Third></span></span>|<xref:System.Windows.FontEastAsianWidths.Normal?displayProperty=nameWithType>|  
|<xref:System.Windows.Documents.Typography.Fraction%2A>|<span data-ttu-id="42dda-309"><xref:System.Windows.FontFraction.Normal> &#124; <xref:System.Windows.FontFraction.Slashed> &#124; <xref:System.Windows.FontFraction.Stacked></span><span class="sxs-lookup"><span data-stu-id="42dda-309"><xref:System.Windows.FontFraction.Normal> &#124; <xref:System.Windows.FontFraction.Slashed> &#124; <xref:System.Windows.FontFraction.Stacked></span></span>|<xref:System.Windows.FontFraction.Normal?displayProperty=nameWithType>|  
|<xref:System.Windows.Documents.Typography.HistoricalForms%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.HistoricalLigatures%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.Kerning%2A>|<xref:System.Boolean>|`true`|  
|<xref:System.Windows.Documents.Typography.MathematicalGreek%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.NumeralAlignment%2A>|<span data-ttu-id="42dda-310"><xref:System.Windows.FontNumeralAlignment.Normal> &#124; <xref:System.Windows.FontNumeralAlignment.Proportional> &#124; <xref:System.Windows.FontNumeralAlignment.Tabular></span><span class="sxs-lookup"><span data-stu-id="42dda-310"><xref:System.Windows.FontNumeralAlignment.Normal> &#124; <xref:System.Windows.FontNumeralAlignment.Proportional> &#124; <xref:System.Windows.FontNumeralAlignment.Tabular></span></span>|<xref:System.Windows.FontNumeralAlignment.Normal?displayProperty=nameWithType>|  
|<xref:System.Windows.Documents.Typography.NumeralStyle%2A>|<xref:System.Boolean>|<xref:System.Windows.FontNumeralStyle.Normal?displayProperty=nameWithType>|  
|<xref:System.Windows.Documents.Typography.SlashedZero%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StandardLigatures%2A>|<xref:System.Boolean>|`true`|  
|<xref:System.Windows.Documents.Typography.StandardSwashes%2A>|<span data-ttu-id="42dda-311">숫자 값-바이트</span><span class="sxs-lookup"><span data-stu-id="42dda-311">numeric value – byte</span></span>|<span data-ttu-id="42dda-312">0</span><span class="sxs-lookup"><span data-stu-id="42dda-312">0</span></span>|  
|<xref:System.Windows.Documents.Typography.StylisticAlternates%2A>|<span data-ttu-id="42dda-313">숫자 값-바이트</span><span class="sxs-lookup"><span data-stu-id="42dda-313">numeric value – byte</span></span>|<span data-ttu-id="42dda-314">0</span><span class="sxs-lookup"><span data-stu-id="42dda-314">0</span></span>|  
|<xref:System.Windows.Documents.Typography.StylisticSet1%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet2%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet3%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet4%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet5%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet6%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet7%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet8%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet9%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet10%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet11%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet12%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet13%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet14%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet15%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet16%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet17%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet18%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet19%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet20%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.Variants%2A>|<span data-ttu-id="42dda-315"><xref:System.Windows.FontVariants.Inferior> &#124; <xref:System.Windows.FontVariants.Normal> &#124; <xref:System.Windows.FontVariants.Ordinal> &#124; <xref:System.Windows.FontVariants.Ruby> &#124; <xref:System.Windows.FontVariants.Subscript> &#124; <xref:System.Windows.FontVariants.Superscript></span><span class="sxs-lookup"><span data-stu-id="42dda-315"><xref:System.Windows.FontVariants.Inferior> &#124; <xref:System.Windows.FontVariants.Normal> &#124; <xref:System.Windows.FontVariants.Ordinal> &#124; <xref:System.Windows.FontVariants.Ruby> &#124; <xref:System.Windows.FontVariants.Subscript> &#124; <xref:System.Windows.FontVariants.Superscript></span></span>|<xref:System.Windows.FontVariants.Normal?displayProperty=nameWithType>|  
  
## <a name="see-also"></a><span data-ttu-id="42dda-316">참고 항목</span><span class="sxs-lookup"><span data-stu-id="42dda-316">See Also</span></span>  
 <xref:System.Windows.Documents.Typography>  
 [<span data-ttu-id="42dda-317">OpenType 사양</span><span class="sxs-lookup"><span data-stu-id="42dda-317">OpenType Specification</span></span>](https://go.microsoft.com/fwlink/?LinkId=96731)  
 [<span data-ttu-id="42dda-318">WPF의 입력 체계</span><span class="sxs-lookup"><span data-stu-id="42dda-318">Typography in WPF</span></span>](../../../../docs/framework/wpf/advanced/typography-in-wpf.md)  
 [<span data-ttu-id="42dda-319">샘플 OpenType 글꼴 팩</span><span class="sxs-lookup"><span data-stu-id="42dda-319">Sample OpenType Font Pack</span></span>](../../../../docs/framework/wpf/advanced/sample-opentype-font-pack.md)  
 [<span data-ttu-id="42dda-320">응용 프로그램과 함께 글꼴 패키징</span><span class="sxs-lookup"><span data-stu-id="42dda-320">Packaging Fonts with Applications</span></span>](../../../../docs/framework/wpf/advanced/packaging-fonts-with-applications.md)
