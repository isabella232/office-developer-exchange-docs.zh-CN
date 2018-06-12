---
title: InternetMessageHeader
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InternetMessageHeader
api_type:
- schema
ms.assetid: c70675f8-6feb-4c89-ba48-bce0479b308b
description: InternetMessageHeader 元素均表示给定标题的标头集合中的 Internet 邮件标题。 若要获取的 Internet 邮件头的整个集合，请使用 PR_TRANSPORT_MESSAGE_HEADERS 属性。 有关 EWS 和 Internet 邮件头、 seeGetting EWS、 MIME 和缺少的 Internet 邮件头中的 Internet 邮件头的详细信息。
ms.openlocfilehash: 9457cdabe99c0adcb8183cbc039cc86db881fec7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825952"
---
# <a name="internetmessageheader"></a>InternetMessageHeader

**InternetMessageHeader**元素均表示给定标题的标头集合中的 Internet 邮件标题。 若要获取的 Internet 邮件头的整个集合，请使用**PR_TRANSPORT_MESSAGE_HEADERS**属性。 有关 EWS 和 Internet 邮件头的详细信息，请参阅["EWS、 MIME 和缺少的 Internet 邮件头](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx)中获取 Internet 邮件头。
  
```XML
<InternetMessageHeader HeaderName=""/>
```

 **InternetHeaderType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**HeaderName** <br/> |标识的标头名称。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |代表在邮箱中某个项目中包含的所有 Internet 邮件头的集合。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示标头的值。
  
## <a name="remarks"></a>备注

下面是 EWS 托管 API 扩展属性**PR_TRANSPORT_MESSAGE_HEADERS**属性的定义。 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)


[EWS、 MIME 和缺少的 Internet 邮件头](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx)

