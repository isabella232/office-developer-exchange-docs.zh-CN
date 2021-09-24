---
title: InternetMessageHeader
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- InternetMessageHeader
api_type:
- schema
ms.assetid: c70675f8-6feb-4c89-ba48-bce0479b308b
description: InternetMessageHeader 元素代表 headers 集合中给定邮件头的 Internet 邮件头。 若要获取整个 Internet 邮件头集合，请使用 PR_TRANSPORT_MESSAGE_HEADERS 属性。 有关 EWS 和 Internet 邮件头的信息，请参阅在 EWS、MIME 中获取 Internet 邮件头和缺少的 Internet 邮件头。
ms.openlocfilehash: 4b3072611e8a3debf87ce2a023f4f68ee4487185
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541079"
---
# <a name="internetmessageheader"></a>InternetMessageHeader

**InternetMessageHeader** 元素代表 headers 集合中给定邮件头的 Internet 邮件头。 若要获取整个 Internet 邮件头集合，请使用 **PR_TRANSPORT_MESSAGE_HEADERS** 属性。 有关 EWS 和 Internet 邮件头的信息，请参阅"在 [EWS、MIME](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)中获取 Internet 邮件头和缺少的 Internet 邮件头。"
  
```XML
<InternetMessageHeader HeaderName=""/>
```

 **InternetHeaderType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**HeaderName** <br/> |标识标头名称。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |表示包含在邮箱中的项目的所有 Internet 邮件头的集合。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示标头的值。
  
## <a name="remarks"></a>注解

下面是 EWS 托管 API 扩展属性定义的 PR_TRANSPORT_MESSAGE_HEADERS **属性。** 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

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


[EWS、MIME 和缺少的 Internet 邮件头](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)

