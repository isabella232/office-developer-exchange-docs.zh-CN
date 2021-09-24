---
title: GetAttachmentResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetAttachmentResponseMessage
api_type:
- schema
ms.assetid: f0a841af-422d-4c82-b710-41e2038dbee4
description: GetAttachmentResponseMessage 元素包含单个 GetAttachment 操作请求的状态和结果。
ms.openlocfilehash: 943474827ebc96894fbde973fde0872deadc9ecc
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511591"
---
# <a name="getattachmentresponsemessage"></a>GetAttachmentResponseMessage

**GetAttachmentResponseMessage 元素** 包含单个 [GetAttachment](getattachment-operation.md)操作请求的状态和结果。 
  
- [GetAttachmentResponse](getattachmentresponse.md) 
- [ResponseMessages](responsemessages.md) 
- [GetAttachmentResponseMessage](getattachmentresponsemessage.md)
  
```xml
<GetAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Attachments/>
</GetAttachmentResponseMessage>
```

 **AttachmentInfoResponseMessageType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**ResponseClass** <br/> | 描述 [GetAttachment 操作响应](getattachment-operation.md) 的状态。<br/><br/> 以下值对此属性有效： <br/> <br/>- 成功  <br/>- 警告  <br/>- 错误  <br/> |
   
#### <a name="responseclass-attribute"></a>ResponseClass 属性

|**值**|**说明**|
|:-----|:-----|
|成功  <br/> |描述已实现的请求。  <br/> |
|警告  <br/> | 描述未处理的请求。 如果在请求中的项目正在处理并且后续项目无法处理时发生错误，则可能会返回警告。 <br/><br/>以下是警告来源的示例： <br/> <br/>- Exchange存储在批处理期间处于脱机状态。  <br/>- Active Directory 域服务 (AD DS) 处于脱机状态。  <br/>- 移动邮箱。  <br/>- 邮件数据库 (MDB) 处于脱机状态。  <br/>- 密码已过期。  <br/>- 超出配额。  <br/> |
|错误  <br/> | 描述无法实现的请求。 <br/><br/>以下是错误源的示例：  <br/><br/>- 无效的属性或元素  <br/>- 属性或元素范围外  <br/>- 未知标记  <br/>- 上下文中无效属性或元素  <br/>- 任何客户端的未授权访问尝试  <br/>- 响应有效的客户端调用的服务器端故障  <br/><br/>  有关错误的信息可在 [ResponseCode](responsecode.md) 和 [MessageText](messagetext.md) 元素中找到。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |提供响应状态的文本说明。  <br/> |
|[ResponseCode](responsecode.md) <br/> |提供一个错误代码，用于标识请求遇到的特定错误。  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |当前未使用且保留以供将来使用。 它包含值 0。  <br/> |
|[MessageXml](messagexml.md) <br/> |提供其他错误响应信息。  <br/> |
|[附件](attachments-ex15websvcsotherref.md) <br/> |包含未到达项目存储中的项或Exchange文件。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |包含 Web 服务请求Exchange消息。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于运行安装了客户端访问服务器角色的 Microsoft Exchange Server 2010 的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetAttachment](getattachment.md) 
- [GetAttachment 操作](getattachment-operation.md)

