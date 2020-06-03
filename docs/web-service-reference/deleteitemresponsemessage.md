---
title: DeleteItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItemResponseMessage
api_type:
- schema
ms.assetid: c3d34c4d-8d83-4612-aa9e-66f9cc7314df
description: DeleteItemResponseMessage 元素包含单个 DeleteItem 操作请求的状态和结果。
ms.openlocfilehash: 78e3efc6a9e9e6629d7efe7f2dc294e0a731005a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526926"
---
# <a name="deleteitemresponsemessage"></a>DeleteItemResponseMessage

**DeleteItemResponseMessage**元素包含单个[DeleteItem 操作](deleteitem-operation.md)请求的状态和结果。 
  
- [DeleteItemResponse](deleteitemresponse.md) 
- [ResponseMessages](responsemessages.md)  
- [DeleteItemResponseMessage](deleteitemresponsemessage.md)
  
```xml
<DeleteItemResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DeleteItemResponseMessage>
```

 **DeleteItemResponseMessageType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**ResponseClass** <br/> | 描述[DeleteItem 操作](deleteitem-operation.md)响应的状态。<br/><br/>以下值对此属性有效：<br/><br/>-成功  <br/>-警告  <br/>-错误  <br/> |
   
#### <a name="responseclass-attribute"></a>ResponseClass 属性

|**值**|**说明**|
|:-----|:-----|
|**Success** <br/> |描述已完成的请求。  <br/> |
|**警告** <br/> | 介绍未处理的请求。 如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。<br/><br/>以下是警告源的示例：<br/><br/>-Exchange 存储在批处理过程中脱机。  <br/>-Active Directory 域服务（AD DS）脱机。  <br/>-移动邮箱。  <br/>-邮件数据库（MDB）脱机。  <br/>-密码已过期。  <br/>-超出配额。  <br/> |
|**Error** <br/> | 介绍无法满足的请求。<br/><br/>以下是错误源的示例：<br/><br/>-属性或元素无效  <br/>-属性或元素越界  <br/>-未知标记  <br/>-Context 中的属性或元素无效  <br/>-客户端尝试将错误日志记录级别设置为管理员允许的最高级别以上  <br/>-客户端尝试将严重级别故障级别设置为低于管理员指定的默认级别  <br/>-任何客户端的未经授权访问尝试  <br/>-响应有效客户端调用的服务器端故障<br/><br/>  有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**描述**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |提供响应状态的文本说明。  <br/> |
|[ResponseCode](responsecode.md) <br/> |提供用于标识请求遇到的特定错误的错误代码。  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |当前未使用，并保留以供将来使用。 它包含值0。  <br/> |
|[MessageXml](messagexml.md) <br/> |提供其他错误响应信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |包含 Exchange Web 服务请求的响应消息。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
### <a name="version-differences"></a>版本差异

在从 build 15.00.0986.00 开始的 Exchange 版本中， **DeleteItemResponseMessage**元素的类型为**DeleteItemResponseMessageType**。 在以前的版本中，元素的类型为**ResponseMessageType**。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [DeleteItem 操作](deleteitem-operation.md)
- [Exchange 的 EWS 引用](ews-reference-for-exchange.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [删除项目（Exchange Web 服务）](https://msdn.microsoft.com/library/9bfc39e6-d944-4eb6-8aee-cbaf1e37c67d%28Office.15%29.aspx)

