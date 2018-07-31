---
title: CreateItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: c3707feb-3fd4-4b8a-a68f-2abadd455163
description: CreateItem 元素定义一个请求在 Exchange 存储中创建项目。
ms.openlocfilehash: 9453323bff07749f5852dae75284c61c0895adb6
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353124"
---
# <a name="createitem"></a>CreateItem

**CreateItem**元素定义一个请求在 Exchange 存储中创建项目。 
  
```xml
<CreateItem MessageDisposition="" SendMeetingInvitations="">
   <SavedItemFolderId/>
   <Items/>
</CreateItem>
```

**CreateItemType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|属性|说明|
|:-----|:-----|
|**MessageDisposition** <br/> |介绍在创建之后将如何处理项目。 属性是必需的电子邮件。 此属性才适用的电子邮件。  <br/> |
|**SendMeetingInvitations** <br/> |介绍在创建后如何处理会议请求。 此属性是必需的日历项目。  <br/> |
   
#### <a name="messagedisposition-attribute"></a>MessageDisposition 属性

|值|说明|
|:-----|:-----|
|SaveOnly  <br/> |由[SavedItemFolderId](saveditemfolderid.md)元素指定的文件夹中保存邮件项目。 使用[SendItem 操作](senditem-operation.md)，可以稍后发送消息。 在响应中返回的项标识符。 项标识符不返回任何除外邮件项目的项目类型。 这包括响应对象。  <br/> |
|SendOnly  <br/> |发送项目，但没有副本保存在已发送邮件文件夹中。 项标识符未响应中返回。<br/><br/>**注意**： **CreateItem**不支持代理访问使用 SendOnly 选项时，因为无法使用此选项指定的目标文件夹。 解决方法是创建该项目，获取的项标识符，，然后使用 SendItem 操作发送项目。           |
|SendAndSaveCopy  <br/> |发送项目，复制并保存在由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹。 项标识符未响应中返回。<br/><br/>**注意**： 会议请求不会保存到由[SavedItemFolderId](saveditemfolderid.md)属性标识的文件夹。 为日历，只保存**SavedItemFolderId**属性可指定的日历项目的位置。 您无法控制会议请求项目的保存位置。 仅的关联的日历项目进行复制和保存到由**SavedItemFolderId**属性标识的文件夹。           |
   
#### <a name="sendmeetinginvitations-attribute"></a>SendMeetingInvitations 属性

|值|说明|
|:-----|:-----|
|SendToNone  <br/> |如果项目位于会议请求，它是另存为日历项目，但不是发送。  <br/> |
|SendOnlyToAll  <br/> |会议请求发送给所有与会者，但不是保存在已发送邮件文件夹中。  <br/> |
|SendToAllAndSaveCopy  <br/> |会议请求发送给所有与会者和副本保存由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹中。  <br/> |
   
### <a name="child-elements"></a>子元素

|元素|说明|
|:-----|:-----|
|[SavedItemFolderId](saveditemfolderid.md) <br/> |标识在其中创建新项的目标文件夹。 如果**MessageDisposition**属性设置为 SendOnly，将只发送创建的消息。 由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹中将不进行邮件。  <br/> |
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |包含由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹中创建的项的数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [CreateItemResponse](createitemresponse.md)  
- [CreateItem 操作](createitem-operation.md)
- [创建电子邮件](http://msdn.microsoft.com/library/05bfb83c-2866-427d-a9fe-14ba3cb02793%28Office.15%29.aspx) 
- [Creating Contacts (Exchange Web Services)](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [创建任务](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx) 
- [创建约会](http://msdn.microsoft.com/library/2385391e-c9e7-4d45-b803-c4ff94d5c94e%28Office.15%29.aspx)

