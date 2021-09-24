---
title: UserIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UserIds
api_type:
- schema
ms.assetid: 78a09c3a-1646-4c55-95a2-1109fb11e1c6
description: UserIds 元素包含要从主体邮箱获取或删除的委派用户数组。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: c99c39a75060780974cb26546e3a9d2947a9dfb8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517356"
---
# <a name="userids"></a>UserIds

**UserIds** 元素包含要从主体邮箱获取或删除的委派用户数组。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
```xml
<UserIds>
   <UserId/>
</UserIds>
```

 **ArrayOfUserIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[UserId](userid.md) <br/> |标识要从主体邮箱获取或删除的代理。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetDelegate](getdelegate.md) <br/> |定义请求以获取有关委派给邮箱的信息。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[RemoveDelegate](removedelegate.md) <br/> |定义请求以从邮箱删除代理人。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetDelegate 操作](getdelegate-operation.md)
  
[RemoveDelegate 操作](removedelegate-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

