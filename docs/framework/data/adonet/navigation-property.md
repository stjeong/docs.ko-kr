---
title: 탐색 속성-ADO.NET
ms.date: 03/30/2017
ms.assetid: d0bf1a6a-1d84-484c-b7c3-b410fd8dc0b1
ms.openlocfilehash: 6729b22dbc012d5ccfabd64cd83b710833fe1b9d
ms.sourcegitcommit: 5dcfeb59179e81071f54840d4902cbe00b184294
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54857946"
---
# <a name="navigation-property"></a><span data-ttu-id="1f4b7-102">탐색 속성</span><span class="sxs-lookup"><span data-stu-id="1f4b7-102">Navigation property</span></span>

<span data-ttu-id="1f4b7-103">*탐색 속성* 은 선택적 속성에는 [엔터티 형식](entity-type.md) 탐색에 허용 되는 [끝](association-end.md) 의 [연결](association-type.md) 를 다른 끝입니다.</span><span class="sxs-lookup"><span data-stu-id="1f4b7-103">A *navigation property* is an optional property on an [entity type](entity-type.md) that allows for navigation from one [end](association-end.md) of an [association](association-type.md) to the other end.</span></span> <span data-ttu-id="1f4b7-104">달리 [속성](property.md), 탐색 속성 데이터를 전달 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4b7-104">Unlike other [properties](property.md), navigation properties do not carry data.</span></span>

<span data-ttu-id="1f4b7-105">탐색 속성 정의에는 다음 정보가 들어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4b7-105">A navigation property definition includes the following:</span></span>

- <span data-ttu-id="1f4b7-106">이름</span><span class="sxs-lookup"><span data-stu-id="1f4b7-106">A name.</span></span> <span data-ttu-id="1f4b7-107">(필수)</span><span class="sxs-lookup"><span data-stu-id="1f4b7-107">(Required)</span></span>

- <span data-ttu-id="1f4b7-108">탐색하는 연결</span><span class="sxs-lookup"><span data-stu-id="1f4b7-108">The association that it navigates.</span></span> <span data-ttu-id="1f4b7-109">(필수)</span><span class="sxs-lookup"><span data-stu-id="1f4b7-109">(Required)</span></span>

- <span data-ttu-id="1f4b7-110">탐색하는 연결의 End</span><span class="sxs-lookup"><span data-stu-id="1f4b7-110">The ends of the association that it navigates.</span></span> <span data-ttu-id="1f4b7-111">(필수)</span><span class="sxs-lookup"><span data-stu-id="1f4b7-111">(Required)</span></span>

<span data-ttu-id="1f4b7-112">탐색 속성은 연결의 양쪽 End에 있는 엔터티 형식 모두에 대해 선택적 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="1f4b7-112">Note that navigation properties are optional on both entity types at the ends of an association.</span></span> <span data-ttu-id="1f4b7-113">연결의 End에 있는 한 엔터티 형식에 대해 탐색 속성을 정의하는 경우 연결의 다른 End에 있는 엔터티 형식에 대해서는 탐색 속성을 정의할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4b7-113">If you define a navigation property on one entity type at the end of an association, you do not have to define a navigation property on the entity type at the other end of the association.</span></span>

<span data-ttu-id="1f4b7-114">탐색 속성의 데이터 형식에서 결정 됩니다 합니다 [복합성](association-end-multiplicity.md) 해당 원격 [연결 end](association-end.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4b7-114">The data type of a navigation property is determined by the [multiplicity](association-end-multiplicity.md) of its remote [association end](association-end.md).</span></span> <span data-ttu-id="1f4b7-115">예를 들어, `OrdersNavProp` 탐색 속성이 `Customer` 엔터티 형식에 존재하며 `Customer`와 `Order` 간의 일대다 연결을 탐색한다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4b7-115">For example, suppose a navigation property, `OrdersNavProp`, exists on a `Customer` entity type and navigates a one-to-many association between `Customer` and `Order`.</span></span> <span data-ttu-id="1f4b7-116">탐색 속성에 대 한 원격 연결 end의 다중성이 many 있으므로 (\*), 해당 데이터 형식이 컬렉션이 (의 `Order`).</span><span class="sxs-lookup"><span data-stu-id="1f4b7-116">Because the remote association end for the navigation property has multiplicity of many (\*), its data type is a collection (of `Order`).</span></span> <span data-ttu-id="1f4b7-117">마찬가지로 `CustomerNavProp` 탐색 속성이 `Order` 엔터티 형식에 존재하는 경우 원격 End의 복합성이 한 개(1)이므로 해당 데이터 형식은 `Customer`가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f4b7-117">Similarly, if a navigation property, `CustomerNavProp`, exists on the `Order` entity type, its data type would be `Customer`, because the multiplicity of the remote end is one (1).</span></span>

## <a name="example"></a><span data-ttu-id="1f4b7-118">예제</span><span class="sxs-lookup"><span data-stu-id="1f4b7-118">Example</span></span>

<span data-ttu-id="1f4b7-119">다음 다이어그램에서는 세 가지 엔터티 형식 `Book`, `Publisher` 및 `Author`가 포함된 개념적 모델을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f4b7-119">The diagram below shows a conceptual model with three entity types: `Book`, `Publisher`, and `Author`.</span></span> <span data-ttu-id="1f4b7-120">탐색 속성 `Publisher` 및 `Authors`는 Book 엔터티 형식에 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f4b7-120">Navigation properties, `Publisher` and `Authors`, are defined on the Book entity type.</span></span> <span data-ttu-id="1f4b7-121">탐색 속성 `Books`는 Publisher 엔터티 형식과 `Author` 엔터티 형식에 모두 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f4b7-121">Navigation property `Books` is defined on both the Publisher entity type and the `Author` entity type.</span></span>

<span data-ttu-id="1f4b7-122">![탐색 속성을 사용 하 여 모델](/media/modelwithnavprops.gif "ModelWithNavProps")</span><span class="sxs-lookup"><span data-stu-id="1f4b7-122">![Model with Navigation Properties](/media/modelwithnavprops.gif "ModelWithNavProps")</span></span>

<span data-ttu-id="1f4b7-123">합니다 [ADO.NET Entity Framework](./ef/index.md) 개념 스키마 정의 언어를 호출 하는 도메인 특정 언어 (DSL)를 사용 하 여 ([CSDL](./ef/language-reference/csdl-specification.md)) 개념적 모델을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4b7-123">The [ADO.NET Entity Framework](./ef/index.md) uses a domain-specific language (DSL) called conceptual schema definition language ([CSDL](./ef/language-reference/csdl-specification.md)) to define conceptual models.</span></span> <span data-ttu-id="1f4b7-124">다음 CSDL에서는 위의 다이어그램에 표시된 `Book` 엔터티 형식을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4b7-124">The following CSDL defines the `Book` entity type shown in the diagram above:</span></span>

[!code-xml[EDM_Example_Model#EntityExample](~/samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#entityexample)]

<span data-ttu-id="1f4b7-125">XML 특성 탐색 속성을 정의 하는 데 필요한 정보를 통신에 사용 되는 note: 특성 `Name` 속성의 이름을 포함 `Relationship` 탐색, 연결의 이름을 포함 하 고 `FromRole` 및 `ToRole` 연결의 end를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4b7-125">Note that XML attributes are used to communicate the information necessary to define a navigation property: The attribute `Name` contains the name of the property, `Relationship` contains the name of the association it navigates, and `FromRole` and `ToRole` contain the ends of the association.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f4b7-126">참고자료</span><span class="sxs-lookup"><span data-stu-id="1f4b7-126">See also</span></span>

- [<span data-ttu-id="1f4b7-127">엔터티 데이터 모델의 주요 개념</span><span class="sxs-lookup"><span data-stu-id="1f4b7-127">Entity Data Model Key Concepts</span></span>](entity-data-model-key-concepts.md)
- [<span data-ttu-id="1f4b7-128">엔터티 데이터 모델</span><span class="sxs-lookup"><span data-stu-id="1f4b7-128">Entity Data Model</span></span>](entity-data-model.md)
- [<span data-ttu-id="1f4b7-129">관계, 탐색 속성 및 외래 키</span><span class="sxs-lookup"><span data-stu-id="1f4b7-129">Relationships, navigation properties and foreign keys</span></span>](/ef/ef6/fundamentals/relationships)
