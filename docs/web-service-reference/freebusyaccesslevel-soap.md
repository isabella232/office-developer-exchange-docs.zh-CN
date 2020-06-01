---
title: FreeBusyAccessLevel （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a287b9c3-7fb6-4f2f-a8dc-15d4bc32394c
description: FreeBusyAccessLevel 元素表示 FreeBusyAccessLevel 属性。 FreeBusyAccessLevel 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 7ff0c6c72f924a2f1f8eee0dd152d19f6a8745e9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460048"
---
# <a name="freebusyaccesslevel-soap"></a>FreeBusyAccessLevel （SOAP）

**FreeBusyAccessLevel**元素表示**FreeBusyAccessLevel**属性。 **FreeBusyAccessLevel**元素仅供内部使用。 客户端不使用此元素。 
  
```XML
<FreeBusyAccessLevel/>
```

 **string**
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
   
## <a name="remarks"></a>备注

此元素指定响应中将返回的最大忙/闲详细信息量，并指示外部共享的忙/闲数据的级别。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetOrganizationRelationshipSettings 操作（SOAP）](getorganizationrelationshipsettings-operation-soap.md)

