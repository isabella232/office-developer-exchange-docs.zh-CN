---
title: SyncFolderItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderItemsResponseMessage
api_type:
- schema
ms.assetid: f58e773f-94a7-4729-90f0-ac4c71b4ba59
description: SyncFolderItemsResponseMessage 元素包含状态和单个 SyncFolderItems 操作请求的结果。
ms.openlocfilehash: 9bb32232143df56ad9de93480e10a5941e68025a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838180"
---
# <a name="syncfolderitemsresponsemessage"></a>SyncFolderItemsResponseMessage

**SyncFolderItemsResponseMessage**元素包含状态和的单个结果[SyncFolderItems 操作](syncfolderitems-operation.md)请求。 
  
- [SyncFolderItemsResponse](syncfolderitemsresponse.md) 
- [ResponseMessages](responsemessages.md)
- [SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)
  
```xml
<SyncFolderItemsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <SyncState/>
   <IncludesLastItemInRange/>
   <Changes/>
</SyncFolderItemsResponseMessage>
```

 **SyncFolderItemsResponseMessageType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**ResponseClass** <br/> | 描述[SyncFolderItems 操作](syncfolderitems-operation.md)的响应的状态。 <br/><br/>下面是此属性有效值： <br/> <br/>-成功  <br/>-警告  <br/>-错误  <br/> |
   
#### <a name="responseclass-attribute"></a>ResponseClass 属性

|**值**|**说明**|
|:-----|:-----|
|**成功** <br/> |介绍的已完成的请求。  <br/> |
|**Warning** <br/> | 介绍了未处理的请求。 如果处理请求中的项目时出错，因此无法处理后续项目，可能会返回一条警告。 <br/><br/>以下是源的警告的示例：  <br/><br/>-在 Exchange 存储过程批次中处于脱机状态。  <br/>-Active Directory 域服务 (AD DS) 处于脱机状态。  <br/>的已移动邮箱。  <br/>(MDB)-邮件数据库处于脱机状态。  <br/>的已过期密码。  <br/>已超出-配额。  <br/> |
|**Error** <br/> | 描述无法满足请求。 <br/><br/>错误的来源的示例如下：  <br/><br/>-无效属性或元素  <br/>-属性或超出范围的元素  <br/>-未知的标记  <br/>-属性或上下文中无效的元素  <br/>-任何未经授权的访问尝试的任何客户端  <br/>的有效的客户端的呼叫的响应中任何服务器端故障  <br/>  <br/>[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |提供的响应状态的文本说明。  <br/> |
|[ResponseCode](responsecode.md) <br/> |提供标识的特定错误的请求时遇到的错误代码。  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |当前未使用，供将来使用。 它包含 0 的值。  <br/> |
|[MessageXml](messagexml.md) <br/> |提供了其他错误响应信息。  <br/> |
|[SyncState](syncstate-ex15websvcsotherref.md) <br/> |包含 base64 编码的同步数据的每个请求成功后都会更新窗体。 这用于标识的同步状态。  <br/> |
|[IncludesLastItemInRange](includeslastiteminrange.md) <br/> |指示是否在响应中包含的最后一项进行同步。  <br/> |
|[更改 （项）](changes-items.md) <br/> |包含表示客户端上的项目和 Exchange 服务器上的项目之间的差异的类型的更改类型序列数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |包含为 Exchange Web 服务请求的响应消息。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [SyncFolderItems 操作](syncfolderitems-operation.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

