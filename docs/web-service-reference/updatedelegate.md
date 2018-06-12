---
title: UpdateDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateDelegate
api_type:
- schema
ms.assetid: c6ae99c4-18b0-4136-90ab-12cf15e15f91
description: UpdateDelegate 元素定义一个请求来更新邮箱中的代理人。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 32322e48acfa5f1058786162565a185a3e565d6e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838366"
---
# <a name="updatedelegate"></a>UpdateDelegate

**UpdateDelegate**元素定义一个请求来更新邮箱中的代理人。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。 
  
```xml
<UpdateDelegate>
      <DelegateUsers/>
   <DeliverMeetingRequests/>
      <Mailbox/>
</UpdateDelegate>
```

 **UpdateDelegateType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[DelegateUsers](delegateusers.md) <br/> |包含标识代理人和更新将应用于代理人的[DelegateUser](delegateuser.md)元素的数组。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[DeliverMeetingRequests](delivermeetingrequests.md) <br/> |定义委托和主体之间确定如何处理会议请求。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[Mailbox](mailbox.md) <br/> |标识已启用邮件的Active Directory目录服务对象。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[UpdateDelegate 操作](updatedelegate-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

