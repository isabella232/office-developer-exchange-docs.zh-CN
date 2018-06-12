---
title: RoutingType （电子邮件地址）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RoutingType
api_type:
- schema
ms.assetid: 74d83198-0d9d-4c78-a2bc-9a671859ff37
description: RoutingType 元素表示收件人的路由协议。
ms.openlocfilehash: a0a6cf312bcb1d4b4818a82bc8d8d3e3f33ad6f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827255"
---
# <a name="routingtype-emailaddress"></a>RoutingType （电子邮件地址）

**RoutingType**元素表示收件人的路由协议。 
  
```XML
<RoutingType/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[电子邮件 (EmailAddressType)](email-emailaddresstype.md) <br/> |指定 MailboxData 对象的电子邮件地址。 此元素使用[GetUserAvailability 操作](getuseravailability-operation.md)。  <br/><br/> 以下是此元素的 XPath:  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[邮箱 （可用性）](mailbox-availability.md) <br/> | 表示 SetUserOofSettings 或 GetUserOofSettings 请求的邮箱用户。  <br/><br/>  下面是此元素的 XPath 表达式： <br/> <br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a>文本值

文本值是可选的。 唯一有效的值是 SMTP。 如果未提供值，使用 SMTP 的默认值。
  
## <a name="remarks"></a>备注

此元素可以发生最一次中的[电子邮件 (EmailAddressType)](email-emailaddresstype.md)元素。 此元素不是必需的。 此元素存在包含将来的协议。 另一个**RoutingType**元素用于访问用户的邮箱中的项。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetUserAvailability 操作](getuseravailability-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [Getting User Availability](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

