---
title: RoutingType (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RoutingType
api_type:
- schema
ms.assetid: 683216be-9972-4f48-a148-c34bfe7f53e5
description: RoutingType 元素定义邮箱的地址类型。
ms.openlocfilehash: fdbe40bd74debe517739e0fe0c47ed108bd614c6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509363"
---
# <a name="routingtype-emailaddresstype"></a>RoutingType (EmailAddressType)

**RoutingType** 元素定义邮箱的地址类型。 
  
```XML
<RoutingType/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ActingAs](actingas.md) <br/> |标识呼叫者发送身份。  <br/> |
|[邮箱](mailbox.md) <br/> |标识完全解析的电子邮件地址。  <br/> |
|[RoomList](roomlist.md) <br/> |标识会议室列表。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示传送类型。 SMTP 是此元素的典型文本值。
  
## <a name="remarks"></a>注解

此元素在 [Mailbox](mailbox.md) 元素中是可选的。 另 [一个 RoutingType (EmailAddress) ](routingtype-emailaddress.md) 元素用于 Availability 操作。 
  
描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

