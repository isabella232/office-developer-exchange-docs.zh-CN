---
title: DeleteFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolderResponseMessage
api_type:
- schema
ms.assetid: de4c63ff-80b2-40c2-bc06-ef0c23beacd4
description: DeleteFolderResponseMessage 元素包含状态和单个 DeleteFolder 操作请求的结果。
ms.openlocfilehash: 5601fe2e48ad002e0fab60d812e7d70c7398f3ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753806"
---
# <a name="deletefolderresponsemessage"></a>DeleteFolderResponseMessage

**DeleteFolderResponseMessage**元素包含状态和的单个结果[DeleteFolder 操作](deletefolder-operation.md)请求。 
  
- [DeleteFolderResponse](deletefolderresponse.md)  
- [ResponseMessages](responsemessages.md)  
- [DeleteFolderResponseMessage](deletefolderresponsemessage.md)
  
```xml
<DeleteFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DeleteFolderResponseMessage>
```

 **ResponseMessageType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**ResponseClass** <br/> | 描述[DeleteFolder 操作](deletefolder-operation.md)的响应的状态。<br/><br/>下面是此属性有效值：<br/><br/>-成功  <br/>-警告  <br/>-错误  <br/> |
   
#### <a name="responseclass-attribute-values"></a>ResponseClass 属性值

|**值**|**说明**|
|:-----|:-----|
|**成功** <br/> |介绍的已完成的请求。  <br/> |
|**Warning** <br/> | 介绍了未处理的请求。 如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。<br/><br/>以下是源的警告的示例：<br/><br/>在批处理期间脱机-Exchange 存储。<br/>-Active Directory 域服务 (AD DS) 将脱机。<br/>的移动邮箱。<br/>(MDB)-邮件数据库脱机。<br/>的已过期密码。<br/>超出了-配额。  <br/> |
|**Error** <br/> | 描述无法满足请求。<br/><br/>错误的来源的示例如下：<br/><br/>-无效属性或元素<br/>-属性或超出范围的元素<br/>-未知标记<br/>-属性或元素在上下文中无效<br/>-未授权访问尝试的任何客户端<br/>的有效的客户端的呼叫的响应中服务器端失败  <br/><br/>  [ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |响应状态的文本说明。  <br/> |
|[ResponseCode](responsecode.md) <br/> |提供标识的特定错误的请求时遇到的错误代码。  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |当前未使用，供将来使用。 它包含 0 的值。  <br/> |
|[MessageXml](messagexml.md) <br/> |提供了其他错误响应信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |包含为 Exchange Web 服务请求的响应消息。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [DeleteFolder 操作](deletefolder-operation.md)
- [Exchange 的 EWS 引用](ews-reference-for-exchange.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [删除文件夹](http://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

