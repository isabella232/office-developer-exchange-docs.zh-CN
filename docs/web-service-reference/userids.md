---
title: UserIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserIds
api_type:
- schema
ms.assetid: 78a09c3a-1646-4c55-95a2-1109fb11e1c6
description: Userid 元素包含一个数组委派用户获取或删除主体的邮箱。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 277ae96fdbc30f1b39ef20553e10ff1de3ff7a8b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838472"
---
# <a name="userids"></a>UserIds

**Userid**元素包含一个数组委派用户获取或删除主体的邮箱。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。 
  
```xml
<UserIds>
   <UserId/>
</UserIds>
```

 **ArrayOfUserIdType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[用户 Id](userid.md) <br/> |标识用于获取或删除主体的邮箱的代理人。 Exchange 2007 SP1 中引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetDelegate](getdelegate.md) <br/> |定义请求以获取有关委派给邮箱的信息。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[RemoveDelegate](removedelegate.md) <br/> |定义请求以从邮箱删除代理人。 Exchange 2007 SP1 中引入了此元素。  <br/> |
   
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



[GetDelegate 操作](getdelegate-operation.md)
  
[RemoveDelegate 操作](removedelegate-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

