---
title: ItemShape
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemShape
api_type:
- schema
ms.assetid: c5604161-bbc0-40bc-ad75-ff7e837d745f
description: ItemShape 元素标识一要 GetItem 操作、 FindItem 操作或 SyncFolderItems 操作响应中返回的属性。
ms.openlocfilehash: 95174a85a8fa05cb2612e1289d46c8db32b6e052
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826191"
---
# <a name="itemshape"></a>ItemShape

**ItemShape**元素标识一要[GetItem 操作](getitem-operation.md)、 [FindItem 操作](finditem-operation.md)或[SyncFolderItems 操作](syncfolderitems-operation.md)的响应中返回的属性。 
  
```XML
<ItemShape>
   <BaseShape/>
   <IncludeMimeContent/>
   <BodyType/>
   <FilterHtmlContent/>
   <ConvertHtmlCodePageToUTF8/>
   <AdditionalProperties/>
</ItemShape>
```

 **ItemResponseShapeType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[BaseShape](baseshape.md) <br/> |标识要项目或文件夹响应中返回的属性的基本配置。  <br/> |
|[IncludeMimeContent](includemimecontent.md) <br/> |指定是否在响应中返回的项的多用途 Internet 邮件扩展 (MIME) 内容。  <br/> |
|[BodyType](bodytype.md) <br/> |介绍如何在响应中设置的正文文本的格式。  <br/> |
|[ConvertHtmlCodePageToUTF8](converthtmlcodepagetoutf8.md) <br/> |指示是否将项目 HTML 正文转换为 UTF8。  <br/> |
|[FilterHtmlContent](filterhtmlcontent.md) <br/> |指定是否启用 HTML 内容筛选。  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |标识要返回的响应中的其他属性。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetItem](getitem.md) <br/> |定义请求从 Exchange 存储中的邮箱检索项目。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/GetItem` <br/> |
|[FindItem](finditem.md) <br/> |定义查找文件夹中包含的所有项的请求。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/FindItem` <br/> |
|[SyncFolderItems](syncfolderitems.md) <br/> |定义同步 Exchange 存储区文件夹中的项目的请求。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/SyncFolderItems` <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetItem 操作](getitem-operation.md)
  
[FindItem 操作](finditem-operation.md)
  
[SyncFolderItems 操作](syncfolderitems-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

