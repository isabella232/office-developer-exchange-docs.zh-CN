---
title: RemoveDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RemoveDelegate
api_type:
- schema
ms.assetid: f21c5171-62e7-47c8-99b1-22e1ff5883bb
description: RemoveDelegate 元素定义从邮箱中删除代理的请求。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 8ef8e2f6fb296ea4d3a9b8739f856bfe9a50985a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523578"
---
# <a name="removedelegate"></a>RemoveDelegate

**RemoveDelegate** 元素定义从邮箱中删除代理的请求。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
```xml
<RemoveDelegate>
      <Mailbox/>
   <UserIds/>
</RemoveDelegate>
```

 **RemoveDelegateType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |标识主体的邮箱。  <br/> |
|[UserIds](userids.md) <br/> |包含要从主体邮箱中删除的委派用户数组。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
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



[RemoveDelegate 操作](removedelegate-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

