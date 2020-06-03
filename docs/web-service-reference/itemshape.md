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
description: ItemShape 元素标识要在 GetItem 操作、FindItem 操作或 SyncFolderItems 操作响应中返回的一组属性。
ms.openlocfilehash: ffb666ee331b55a4f04cad076c705e4bec980e03
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458122"
---
# <a name="itemshape"></a>ItemShape

**ItemShape**元素标识要在[GetItem 操作](getitem-operation.md)、 [FindItem 操作](finditem-operation.md)或[SyncFolderItems 操作](syncfolderitems-operation.md)响应中返回的一组属性。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[BaseShape](baseshape.md) <br/> |标识要在项目或文件夹响应中返回的属性的基本配置。  <br/> |
|[IncludeMimeContent](includemimecontent.md) <br/> |指定是否在响应中返回项目的多用途 Internet 邮件扩展（MIME）内容。  <br/> |
|[BodyType](bodytype.md) <br/> |标识正文文本在响应中的格式。  <br/> |
|[ConvertHtmlCodePageToUTF8](converthtmlcodepagetoutf8.md) <br/> |指示是否将项目 HTML 正文转换为 UTF8。  <br/> |
|[FilterHtmlContent](filterhtmlcontent.md) <br/> |指定是否启用 HTML 内容筛选。  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |标识要在响应中返回的其他属性。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetItem](getitem.md) <br/> |定义从 Exchange 存储中的邮箱检索项目的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/GetItem` <br/> |
|[FindItem](finditem.md) <br/> |定义一个请求，以查找文件夹中包含的所有项目。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/FindItem` <br/> |
|[SyncFolderItems](syncfolderitems.md) <br/> |定义对 Exchange 存储文件夹中的项目进行同步的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/SyncFolderItems` <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetItem 操作](getitem-operation.md)
  
[FindItem 操作](finditem-operation.md)
  
[SyncFolderItems 操作](syncfolderitems-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

