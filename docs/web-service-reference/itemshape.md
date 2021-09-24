---
title: ItemShape
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ItemShape
api_type:
- schema
ms.assetid: c5604161-bbc0-40bc-ad75-ff7e837d745f
description: ItemShape 元素标识在 GetItem 操作、FindItem 操作或 SyncFolderItems 操作响应中返回的一组属性。
ms.openlocfilehash: d6cc1efc85a8a22e12f2a3616fe949b72b3bba33
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519392"
---
# <a name="itemshape"></a>ItemShape

**ItemShape** 元素标识在 [GetItem](getitem-operation.md)操作 [、FindItem](finditem-operation.md)操作或 [SyncFolderItems](syncfolderitems-operation.md)操作响应中返回的一组属性。 
  
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
|[BaseShape](baseshape.md) <br/> |标识项目或文件夹响应中要返回的属性的基本配置。  <br/> |
|[IncludeMimeContent](includemimecontent.md) <br/> |指定是否在响应中返回项目 (MIME) 多用途 Internet 邮件扩展和 MIME 内容。  <br/> |
|[BodyType](bodytype.md) <br/> |标识如何在响应中设置正文文本的格式。  <br/> |
|[ConvertHtmlCodePageToUTF8](converthtmlcodepagetoutf8.md) <br/> |指示项目 HTML 正文是否转换为 UTF8。  <br/> |
|[FilterHtmlContent](filterhtmlcontent.md) <br/> |指定是否启用 HTML 内容筛选。  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |标识响应中要返回的其他属性。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetItem](getitem.md) <br/> |定义从邮件存储中的邮箱检索Exchange请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/GetItem` <br/> |
|[FindItem](finditem.md) <br/> |定义查找文件夹中包含的所有项目的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/FindItem` <br/> |
|[SyncFolderItems](syncfolderitems.md) <br/> |定义同步邮件存储文件夹中Exchange的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/SyncFolderItems` <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

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

