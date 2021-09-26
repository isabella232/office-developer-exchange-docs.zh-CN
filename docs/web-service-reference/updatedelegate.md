---
title: UpdateDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UpdateDelegate
api_type:
- schema
ms.assetid: c6ae99c4-18b0-4136-90ab-12cf15e15f91
description: UpdateDelegate 元素定义更新邮箱中的代理的请求。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: e4e5f79a54e6555a8758612fa02d897df5c3f0af
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541803"
---
# <a name="updatedelegate"></a>UpdateDelegate

**UpdateDelegate** 元素定义更新邮箱中的代理的请求。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
```xml
<UpdateDelegate>
      <DelegateUsers/>
   <DeliverMeetingRequests/>
      <Mailbox/>
</UpdateDelegate>
```

 **UpdateDelegateType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[DelegateUsers](delegateusers.md) <br/> |包含一个 [DelegateUser](delegateuser.md) 元素数组，这些元素标识要应用于委托的委托和更新。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[DeliverMeetingRequests](delivermeetingrequests.md) <br/> |定义如何在代理人和主体之间处理会议请求。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[Mailbox](mailbox.md) <br/> |标识已启用邮件的Active Directory目录服务对象。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[UpdateDelegate 操作](updatedelegate-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

