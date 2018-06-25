---
title: DeliveryReportEnabled (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ab522bc-40ea-4e43-aa57-6d2562db35e9
description: DeliveryReportEnabled 元素均表示 DeliveryReportEnabled() 标志。 DeliveryReportEnabled 元素是仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 089256a5f75ad92a4f11c5aaf3d175382eeee456
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753833"
---
# <a name="deliveryreportenabled-soap"></a>DeliveryReportEnabled (SOAP)

**DeliveryReportEnabled**元素均表示**DeliveryReportEnabled()** 标志。 **DeliveryReportEnabled**元素是仅供内部使用。 客户端不使用此元素。 
  
```XML
<DeliveryReportEnabled>true | false</DeliveryReportEnabled>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |代表单个组织的组织关系的列表。  <br/> |
   
## <a name="text-value"></a>文本值

True DeliveryReportEnabled 元素的文本值指示可从组织中的用户的送达报告。 值为 false 指示应取消送达报告。
  
## <a name="remarks"></a>注解

使用此元素以允许或禁止从服务器的送达报告。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

