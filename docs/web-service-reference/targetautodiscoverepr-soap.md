---
title: TargetAutodiscoverEpr （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fdb9cc7a-cf0a-431b-9f6f-5f1db1792db7
description: TargetAutodiscoverEpr 元素表示 TargetAutodiscoverEpr 属性。 TargetAutodiscoverEpr 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: f8609f61021d5701f7a8fa2590a85824caf296c6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530287"
---
# <a name="targetautodiscoverepr-soap"></a>TargetAutodiscoverEpr （SOAP）

**TargetAutodiscoverEpr**元素表示**TargetAutodiscoverEpr**属性。 **TargetAutodiscoverEpr**元素仅供内部使用。 客户端不使用此元素。 
  
```XML
<TargetAutodiscoverEpr/>
```

 **anyURI**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[OrganizationRelationshipSettings （SOAP）](organizationrelationshipsettings-soap.md) <br/> |表示单个组织的组织关系列表。  <br/> |
   
## <a name="text-value"></a>文本值

此元素的文本值是组织关系的统一资源标识符（URI）。
  
## <a name="remarks"></a>备注

此元素指定外部组织的服务器的自动发现 URL。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetOrganizationRelationshipSettings 操作（SOAP）](getorganizationrelationshipsettings-operation-soap.md)

