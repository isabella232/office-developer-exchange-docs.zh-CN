---
title: DeliveryReportEnabled (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2ab522bc-40ea-4e43-aa57-6d2562db35e9
description: DeliveryReportEnabled 元素表示 DeliveryReportEnabled () 标志。 DeliveryReportEnabled 元素仅供内部使用。 此元素不由客户端使用。
ms.openlocfilehash: 95fe62e25ca871171b398b17f3d03dff9235001b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510167"
---
# <a name="deliveryreportenabled-soap"></a>DeliveryReportEnabled (SOAP)

**DeliveryReportEnabled** 元素表示 **DeliveryReportEnabled** () 标志。 **DeliveryReportEnabled** 元素仅供内部使用。 此元素不由客户端使用。 
  
```XML
<DeliveryReportEnabled>true | false</DeliveryReportEnabled>
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
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |表示单个组织的组织关系列表。  <br/> |
   
## <a name="text-value"></a>文本值

DeliveryReportEnabled 元素的文本值 true 指示可以使用来自组织中用户的送达报告。 false 值指示应禁止送达报告。
  
## <a name="remarks"></a>注解

使用此元素可允许或禁止从服务器发送送达报告。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

