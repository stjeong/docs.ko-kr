---
title: '방법: 데이터베이스 이름 지정'
ms.date: 03/30/2017
ms.assetid: b80f0fd2-7f75-45fe-9e12-496f80f183df
ms.openlocfilehash: a1198a294cd4921728919981bae213c0ee891da6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54556377"
---
# <a name="how-to-specify-database-names"></a><span data-ttu-id="d2c86-102">방법: 데이터베이스 이름 지정</span><span class="sxs-lookup"><span data-stu-id="d2c86-102">How to: Specify Database Names</span></span>
<span data-ttu-id="d2c86-103">연결에서 이름이 제공되지 않은 경우 <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A> 특성의 <xref:System.Data.Linq.Mapping.DatabaseAttribute> 속성을 사용하여 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2c86-103">Use the <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A> property on a <xref:System.Data.Linq.Mapping.DatabaseAttribute> attribute to specify the name of a database when a name is not supplied by the connection.</span></span>  
  
 <span data-ttu-id="d2c86-104">코드 샘플은 <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A>을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d2c86-104">For code samples, see <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A>.</span></span>  
  
### <a name="to-specify-the-name-of-the-database"></a><span data-ttu-id="d2c86-105">데이터베이스의 이름을 지정하려면</span><span class="sxs-lookup"><span data-stu-id="d2c86-105">To specify the name of the database</span></span>  
  
1.  <span data-ttu-id="d2c86-106">데이터베이스의 클래스 선언에 <xref:System.Data.Linq.Mapping.DatabaseAttribute> 특성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d2c86-106">Add the <xref:System.Data.Linq.Mapping.DatabaseAttribute> attribute to the class declaration for the database.</span></span>  
  
2.  <span data-ttu-id="d2c86-107"><xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A> 특성에 <xref:System.Data.Linq.Mapping.DatabaseAttribute> 속성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d2c86-107">Add the <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A> property to the <xref:System.Data.Linq.Mapping.DatabaseAttribute> attribute.</span></span>  
  
3.  <span data-ttu-id="d2c86-108"><xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A> 속성 값을 지정할 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2c86-108">Set the <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A> property value to the name that you want to specify.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d2c86-109">참고자료</span><span class="sxs-lookup"><span data-stu-id="d2c86-109">See also</span></span>
- [<span data-ttu-id="d2c86-110">LINQ to SQL 개체 모델</span><span class="sxs-lookup"><span data-stu-id="d2c86-110">The LINQ to SQL Object Model</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)
- [<span data-ttu-id="d2c86-111">방법: 코드 편집기를 사용 하 여 엔터티 클래스 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="d2c86-111">How to: Customize Entity Classes by Using the Code Editor</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
