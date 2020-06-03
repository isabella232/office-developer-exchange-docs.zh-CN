---
title: FreeBusyAccessEnabled （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8d2d3276-b180-424e-a707-7256d14a1776
description: FreeBusyAccessEnabled 元素表示 FreeBusyAccessEnabled （）标志。 FreeBusyAccessEnabled 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: c148d8fa1301339f8579884dc02b6c9e452f3035
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461294"
---
# <a name="freebusyaccessenabled-soap"></a>FreeBusyAccessEnabled （SOAP）

**FreeBusyAccessEnabled**元素表示**FreeBusyAccessEnabled （）** 标志。 **FreeBusyAccessEnabled**元素仅供内部使用。 客户端不使用此元素。 
  
```XML
<FreeBusyAccessEnabled>true | false</FreeBusyAccessEnabled>
```

 **Boolean**
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

如果**FreeBusyAccessEnabled**元素的文本值为**true** ，则表示应使用共享关系从组织中的用户检索忙/闲信息。 **如果值为 false** ，则表示应取消共享关系。 
  
## <a name="remarks"></a>备注

使用此元素可允许或禁止显示服务器中的忙/闲信息。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetOrganizationRelationshipSettings 操作（SOAP）](getorganizationrelationshipsettings-operation-soap.md)

