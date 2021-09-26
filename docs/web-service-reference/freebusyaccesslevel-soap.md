---
title: FreeBusyAccessLevel (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a287b9c3-7fb6-4f2f-a8dc-15d4bc32394c
description: FreeBusyAccessLevel 元素表示 FreeBusyAccessLevel 属性。 FreeBusyAccessLevel 元素仅供内部使用。 此元素不由客户端使用。
ms.openlocfilehash: 72ccc93f21596a866346b0fb7e959dfaa2199ddd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546425"
---
# <a name="freebusyaccesslevel-soap"></a>FreeBusyAccessLevel (SOAP)

**FreeBusyAccessLevel** 元素表示 **FreeBusyAccessLevel** 属性。 **FreeBusyAccessLevel** 元素仅供内部使用。 此元素不由客户端使用。 
  
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
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |表示单个组织的组织关系列表。  <br/> |
   
## <a name="remarks"></a>注解

此元素指定响应中将返回的忙/闲数据的最大数量，并指示外部共享的忙/闲数据的级别。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

