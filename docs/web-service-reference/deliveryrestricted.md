---
title: DeliveryRestricted
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeliveryRestricted
api_type:
- schema
ms.assetid: 05989915-121c-4f26-93cc-af8d454ab442
description: DeliveryRestricted 元素指示传递限制是否会阻止发件人的邮件到达收件人。
ms.openlocfilehash: 1df5254a284989a8ffc02a8c650eaf69b2214583
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545361"
---
# <a name="deliveryrestricted"></a>DeliveryRestricted

**DeliveryRestricted** 元素指示传递限制是否会阻止发件人的邮件到达收件人。 
  
```XML
<DeliveryRestricted>true | false</DeliveryRestricted>
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
|[邮件提示](mailtips.md) <br/> |表示各种类型的邮件提示的值。  <br/> |
   
## <a name="text-value"></a>文本值

如果传递限制将阻止发件人的邮件到达 **收件人** ，则此元素的文本值为 true。 如果传递限制不会阻止发件人的邮件到达收件人，则值为 **false。** 
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

