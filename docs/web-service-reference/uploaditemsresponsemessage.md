---
title: UploadItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UploadItemsResponseMessage
api_type:
- schema
ms.assetid: 03febd08-c015-4009-b291-1b4296182ffe
description: UploadItemsResponseMessage 元素包含上载单个邮箱项目的请求的状态和结果。
ms.openlocfilehash: 8044950be1a891e20d97d988d8fca405f93d107e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517397"
---
# <a name="uploaditemsresponsemessage"></a>UploadItemsResponseMessage

**UploadItemsResponseMessage 元素** 包含上载单个邮箱项目的请求的状态和结果。 
  
- [UploadItemsResponse](uploaditemsresponse.md) 
- [ResponseMessages](responsemessages.md)
- [UploadItemsResponseMessage](uploaditemsresponsemessage.md)
  
```XML
<UploadItemsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ItemId/>
</UploadItemsResponseMessage>
```

 **UploadItemsResponseMessageType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**ResponseClass** <br/> | 描述响应的状态。 <br/><br/>以下值对此属性有效：  <br/><br/>- 成功  <br/>- 警告  <br/>- 错误  <br/> |
   
#### <a name="responseclass-attribute-values"></a>ResponseClass 属性值

|**值**|**说明**|
|:-----|:-----|
|**Success** <br/> |描述已实现的请求。  <br/> |
|**警告** <br/> | 描述未处理的请求。 如果在请求中的项目正在处理并且后续项目无法处理时发生错误，则可能会返回警告。 <br/><br/>以下是警告来源的示例：  <br/><br/>- Exchange存储在批处理期间处于脱机状态。  <br/>- Active Directory 域服务 (AD DS) 处于脱机状态。  <br/>- 邮箱已移动。  <br/>- 邮件数据库 (MDB) 处于脱机状态。  <br/>- 密码已过期。  <br/>- 已超出配额。  <br/> |
|**错误** <br/> | 描述无法实现的请求。 <br/><br/>以下是错误源的示例：  <br/><br/>- 无效的属性或元素  <br/>- 区域外的属性或元素  <br/>- 未知标记  <br/>- 在上下文中无效属性或元素  <br/>- 任何客户端的未授权访问尝试  <br/>- 响应有效的客户端调用的服务器端故障  <br/> <br/> 有关错误的信息可在 [ResponseCode](responsecode.md) 和 [MessageText](messagetext.md) 元素中找到。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |提供响应状态的文本说明。  <br/> |
|[ResponseCode](responsecode.md) <br/> |提供一个错误代码，用于标识请求遇到的特定错误。  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |当前未使用，保留以供将来使用。 此元素包含值 0。  <br/> |
|[MessageXml](messagexml.md) <br/> |提供其他错误响应信息。  <br/> |
|[ItemId](itemid.md) <br/> |包含已上载项的项目标识符。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |包含 Web 服务请求Exchange消息。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ExportItems 操作](exportitems-operation.md)
- [UploadItems 操作](uploaditems-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

