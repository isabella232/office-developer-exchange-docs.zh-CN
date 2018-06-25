---
title: GetDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetDelegate
api_type:
- schema
ms.assetid: 6d5efe59-596f-46f8-bdc6-ca9cded9bb8e
description: GetDelegate 元素定义一个请求以获取有关委派给邮箱的信息。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: e31d6bd4f4387094beb467fcc4dff31ca7ec5d62
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754513"
---
# <a name="getdelegate"></a>GetDelegate

**GetDelegate**元素定义一个请求以获取有关委派给邮箱的信息。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。 
  
```xml
<GetDelegate IncludePermissions="">
      <Mailbox/>
   <UserIds/>
</GetDelegate>
```

 **GetDelegateType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**IncludePermissions** <br/> |指示响应是否包含为每个委派用户的权限设置。  <br/> |
   
#### <a name="includepermissions-attribute-values"></a>IncludePermissions 属性值

|**值**|**说明**|
|:-----|:-----|
|**True** <br/> |授予的用户权限返回除了[UserId](userid.md)元素中返回的委托用户信息。  <br/> |
|**False** <br/> |将返回[用户 Id](userid.md)信息。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |标识的主体的邮箱。  <br/> |
|[UserIds](userids.md) <br/> |包含委派用户获取主体的邮箱的数组。 Exchange 2007 SP1 中引入了此元素。  <br/> |
   
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



[GetDelegate 操作](getdelegate-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

