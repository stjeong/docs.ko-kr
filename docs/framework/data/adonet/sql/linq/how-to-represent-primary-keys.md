---
title: '방법: 기본 키 표현'
ms.date: 03/30/2017
ms.assetid: 63c65289-6539-42b2-8493-891c232018fa
ms.openlocfilehash: a7cea40b30243c6b15da0500a59ba801f2c8da68
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54687429"
---
# <a name="how-to-represent-primary-keys"></a>방법: 기본 키 표현
사용 하 여는 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.IsPrimaryKey%2A> 속성에는 <xref:System.Data.Linq.Mapping.ColumnAttribute> 속성 또는 데이터베이스 열에 대 한 기본 키를 나타내는 필드를 지정 하는 특성입니다.  
  
 코드 예는 <xref:System.Data.Linq.Mapping.ColumnAttribute.IsPrimaryKey%2A>를 참조하세요.  
  
> [!NOTE]
>  [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]에서는 기본 키로 계산된 열을 지원하지 않습니다.  
  
### <a name="to-designate-a-property-or-field-as-a-primary-key"></a>속성 또는 필드를 기본 키로 지정하려면  
  
1.  <xref:System.Data.Linq.Mapping.ColumnAttribute.IsPrimaryKey%2A> 특성에 <xref:System.Data.Linq.Mapping.ColumnAttribute> 속성을 추가합니다.  
  
2.  값을 `true`로 지정합니다.  
  
## <a name="see-also"></a>참고자료
- [LINQ to SQL 개체 모델](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)
- [방법: 코드 편집기를 사용 하 여 엔터티 클래스 사용자 지정](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
