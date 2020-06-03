---
title: RoutingType （EmailAddressType）
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
ms.assetid: 683216be-9972-4f48-a148-c34bfe7f53e5
description: RoutingType 元素定义邮箱的地址类型。
ms.openlocfilehash: d4229f2857a5c99cc9bb7ff9b9b103de099a0055
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465084"
---
# <a name="routingtype-emailaddresstype"></a>RoutingType （EmailAddressType）

**RoutingType**元素定义邮箱的地址类型。 
  
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
|[ActingAs](actingas.md) <br/> |标识呼叫者发送的人。  <br/> |
|[邮箱](mailbox.md) <br/> |标识完全解析的电子邮件地址。  <br/> |
|[RoomList](roomlist.md) <br/> |标识会议室列表。  <br/> |
   
## <a name="text-value"></a>文本值

该文本值表示路由类型。 SMTP 是此元素的典型文本值。
  
## <a name="remarks"></a>备注

此元素在[邮箱](mailbox.md)元素中是可选的。 另一个[RoutingType （EmailAddress）](routingtype-emailaddress.md)元素用于可用性操作。 
  
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

