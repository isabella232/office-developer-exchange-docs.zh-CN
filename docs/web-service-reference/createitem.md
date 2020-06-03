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
description: CreateItem 元素定义一个请求，以在 Exchange 存储中创建项目。
ms.openlocfilehash: 235664b7baeceeccb14135fd346123f0f7d99346
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527059"
---
# <a name="createitem"></a>CreateItem

**CreateItem**元素定义一个请求，以在 Exchange 存储中创建项目。 
  
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
|**MessageDisposition** <br/> |介绍如何在创建项目后对其进行处理。 电子邮件的属性是必需的。 此属性仅适用于电子邮件。  <br/> |
|**SendMeetingInvitations** <br/> |介绍如何在创建会议请求后对其进行处理。 此属性是日历项目所必需的。  <br/> |
   
#### <a name="messagedisposition-attribute"></a>MessageDisposition 属性

|值|Description|
|:-----|:-----|
|SaveOnly  <br/> |邮件项目保存在由[SavedItemFolderId](saveditemfolderid.md)元素指定的文件夹中。 稍后可以使用[SendItem 操作](senditem-operation.md)发送邮件。 响应中返回项目标识符。 不会为除邮件项目之外的任何项目类型返回项目标识符。 其中包括 response 对象。  <br/> |
|SendOnly  <br/> |项目已发送，但未在 "已发送邮件" 文件夹中保存副本。 响应中不返回项目标识符。<br/><br/>**注意**： **CreateItem**不支持在使用 SendOnly 选项时进行代理访问，因为无法使用此选项指定目标文件夹。 解决方法是创建项目，获取项目标识符，然后使用 SendItem 操作发送项目。           |
|SendAndSaveCopy  <br/> |将发送项目，并将副本保存在由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹中。 响应中不返回项目标识符。<br/><br/>**注意**：会议请求不会保存到由[SavedItemFolderId](saveditemfolderid.md)属性标识的文件夹中。 对于日历，仅可通过**SavedItemFolderId**属性指定日历项目的保存位置。 您不能控制会议请求项目的保存位置。 只会复制关联的日历项目并将其保存到由**SavedItemFolderId**属性标识的文件夹中。           |
   
#### <a name="sendmeetinginvitations-attribute"></a>SendMeetingInvitations 属性

|值|Description|
|:-----|:-----|
|SendToNone  <br/> |如果该项目是会议请求，则会将其保存为日历项目，但不会发送。  <br/> |
|SendOnlyToAll  <br/> |会议请求将发送给所有与会者，但不会保存在 "已发送邮件" 文件夹中。  <br/> |
|SendToAllAndSaveCopy  <br/> |将会议请求发送给所有与会者，并将副本保存在由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹中。  <br/> |
   
### <a name="child-elements"></a>子元素

|元素|说明|
|:-----|:-----|
|[SavedItemFolderId](saveditemfolderid.md) <br/> |标识可在其中创建新项目的目标文件夹。 如果将**MessageDisposition**属性设置为 SendOnly，则仅发送已创建的邮件。 该邮件不会被放在由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹中。  <br/> |
|[项目（NonEmptyArrayOfAllItemsType）](items-nonemptyarrayofallitemstype.md) <br/> |包含要在由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹中创建的项的数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

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

