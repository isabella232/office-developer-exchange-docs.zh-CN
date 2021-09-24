---
title: CreateItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CreateItem
api_type:
- schema
ms.assetid: c3707feb-3fd4-4b8a-a68f-2abadd455163
description: CreateItem 元素定义在项目存储中创建Exchange请求。
ms.openlocfilehash: 7276b88bd3b90edc68d7ac8fd4a7646324eadb61
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526496"
---
# <a name="createitem"></a>CreateItem

**CreateItem** 元素定义在项目存储中创建Exchange请求。 
  
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
|**MessageDisposition** <br/> |描述创建项目后如何处理该项目。 属性是电子邮件的必需属性。 此属性仅适用于电子邮件。  <br/> |
|**SendMeetingInvitations** <br/> |介绍创建会议请求后如何处理它们。 此属性是日历项目必需的。  <br/> |
   
#### <a name="messagedisposition-attribute"></a>MessageDisposition 属性

|值|Description|
|:-----|:-----|
|SaveOnly  <br/> |邮件项目保存在 [SavedItemFolderId](saveditemfolderid.md) 元素指定的文件夹中。 以后可以使用 [SendItem](senditem-operation.md)操作发送邮件。 响应中返回项目标识符。 对于除邮件项之外的任何项目类型，不会返回项目标识符。 这包括 response 对象。  <br/> |
|SendOnly  <br/> |该项目已发送，但"已发送项目"文件夹中未保存任何副本。 响应中不返回项目标识符。<br/><br/>**注意****：使用 SendOnly** 选项时，CreateItem 不支持委派访问，因为无法使用此选项指定目标文件夹。 解决方法是创建项目、获取项目标识符，然后使用 SendItem 操作发送该项目。           |
|SendAndSaveCopy  <br/> |该项目将发送，副本保存在 [SavedItemFolderId](saveditemfolderid.md) 元素标识的文件夹中。 响应中不返回项目标识符。<br/><br/>**注意**：会议请求不会保存到 [SavedItemFolderId](saveditemfolderid.md) 属性标识的文件夹。 对于日历 **，SavedItemFolderId** 属性只能指定日历项目的保存位置。 您无法控制保存会议请求项目的位置。 仅将关联的日历项目复制并保存到 **SavedItemFolderId** 属性标识的文件夹中。           |
   
#### <a name="sendmeetinginvitations-attribute"></a>SendMeetingInvitations 属性

|值|Description|
|:-----|:-----|
|SendToNone  <br/> |如果此项是会议请求，则另存为日历项目，但不发送。  <br/> |
|SendOnlyToAll  <br/> |会议请求将发送给所有与会者，但不保存在"已发送的项目"文件夹中。  <br/> |
|SendToAllAndSaveCopy  <br/> |会议请求将发送给所有与会者，副本保存在 [SavedItemFolderId](saveditemfolderid.md) 元素标识的文件夹中。  <br/> |
   
### <a name="child-elements"></a>子元素

|元素|说明|
|:-----|:-----|
|[SavedItemFolderId](saveditemfolderid.md) <br/> |标识可在其中新建项目的目标文件夹。 如果将 **MessageDisposition** 属性设置为 SendOnly，则只会发送已创建的邮件。 邮件不会放入 [SavedItemFolderId](saveditemfolderid.md) 元素标识的文件夹中。  <br/> |
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |包含在 [SavedItemFolderId](saveditemfolderid.md) 元素标识的文件夹中要创建的项数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [CreateItemResponse](createitemresponse.md)  
- [CreateItem 操作](createitem-operation.md)
- [创建电子邮件](https://msdn.microsoft.com/library/05bfb83c-2866-427d-a9fe-14ba3cb02793%28Office.15%29.aspx) 
- [创建联系人（Exchange Web 服务）](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [创建任务](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx) 
- [创建约会](https://msdn.microsoft.com/library/2385391e-c9e7-4d45-b803-c4ff94d5c94e%28Office.15%29.aspx)

