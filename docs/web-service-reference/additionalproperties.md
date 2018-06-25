---
title: AdditionalProperties
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AdditionalProperties
api_type:
- schema
ms.assetid: 7a269aed-dcfd-4c3e-9e14-094e53828101
description: AdditionalProperties 元素标识用于 GetItem UpdateItem、 CreateItem、 FindItem，其他属性或 FindFolder 请求。
ms.openlocfilehash: 64e4f1ee6b24cf8015b7893dc4a904ca8b32d58e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753114"
---
# <a name="additionalproperties"></a>AdditionalProperties

**AdditionalProperties**元素标识用于[GetItem](getitem.md) [UpdateItem](updateitem.md)、 [CreateItem](createitem.md)、 [FindItem](finditem.md)，其他属性或[FindFolder](findfolder.md)请求。 
  
```xml
<AdditionalProperties>
   <ExtendedFieldURI/>
   <FieldURI/>
   <IndexedFieldURI/>
</AdditionalProperties>
```

 **NonEmptyArrayOfPathsToElementType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ExtendedFieldURI](extendedfielduri.md) <br/> |标识扩展的 MAPI 属性以获取、 设置或创建。  <br/> |
|[FieldURI](fielduri.md) <br/> |标识由 URI 频繁引用的属性。  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |标识经常引用的词典属性的 URI。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> | 标识要在[GetFolder](getfolder.md)、 [FindFolder](findfolder.md)或[SyncFolderHierarchy](syncfolderhierarchy.md)响应中包含的文件夹属性。<br/><br/>  下面是此元素的 XPath 表达式：<br/><br/>  `/FindFolder/FolderShape` <br/>  `/GetFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[ItemShape](itemshape.md) <br/> | 标识项目属性和[GetItem](getitem.md)、 [FindItem](finditem.md)或[SyncFolderItems](syncfolderitems.md)响应中包括的内容。<br/><br/>  下面是此元素的 XPath 表达式：<br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
|[AttachmentShape](attachmentshape.md) <br/> |标识要[GetItem](getitem.md)请求的响应中返回的其他扩展的项属性。<br/><br/> 以下是此元素的 XPath 表达式：<br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="remarks"></a>注解

并非所有的子元素可用于[GetItem](getitem.md)、 [UpdateItem](updateitem.md)、 [CreateItem](createitem.md)、 [FindItem](finditem.md)或[FindFolder](findfolder.md)请求。 该属性必须是适用于文件夹或项目的访问。 使用扩展的属性访问其他属性。 如果属性不存在的给定项目，将到所产生的 XML 激发没有相应的元素。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。 
  
此元素是可选的。
  
## <a name="example"></a>示例

下面的请求示例演示如何通过使用**AdditionalProperties**元素中获取项目主题。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="ASkAS="/>
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   

