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
description: AdditionalProperties 元素标识在 GetItem、UpdateItem、CreateItem、FindItem 或 FindFolder 请求中使用的其他属性。
ms.openlocfilehash: 90a307ba4d5ece10e15d2cec56cf5042c3d38685
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455812"
---
# <a name="additionalproperties"></a>AdditionalProperties

**AdditionalProperties**元素标识在[GetItem](getitem.md)、 [UpdateItem](updateitem.md)、 [CreateItem](createitem.md)、 [FindItem](finditem.md)或[FindFolder](findfolder.md)请求中使用的其他属性。 
  
```xml
<AdditionalProperties>
   <ExtendedFieldURI/>
   <FieldURI/>
   <IndexedFieldURI/>
</AdditionalProperties>
```

 **NonEmptyArrayOfPathsToElementType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ExtendedFieldURI](extendedfielduri.md) <br/> |标识要获取、设置或创建的扩展 MAPI 属性。  <br/> |
|[FieldURI](fielduri.md) <br/> |标识由 URI 频繁引用的属性。  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |按 URI 标识经常引用的字典属性。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> | 标识要包括在[GetFolder](getfolder.md)、 [FindFolder](findfolder.md)或[SyncFolderHierarchy](syncfolderhierarchy.md)响应中的文件夹属性。<br/><br/>  下面是此元素的 XPath 表达式：<br/><br/>  `/FindFolder/FolderShape` <br/>  `/GetFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[ItemShape](itemshape.md) <br/> | 标识要包括在[GetItem](getitem.md)、 [FindItem](finditem.md)或[SyncFolderItems](syncfolderitems.md)响应中的项目属性和内容。<br/><br/>  下面是此元素的 XPath 表达式：<br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
|[AttachmentShape](attachmentshape.md) <br/> |标识要在对[GetItem](getitem.md)请求的响应中返回的其他扩展项属性。<br/><br/> 下面是此元素的 XPath 表达式： <br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="remarks"></a>备注

并非所有子元素都可与[GetItem](getitem.md)、 [UpdateItem](updateitem.md)、 [CreateItem](createitem.md)、 [FindItem](finditem.md)或[FindFolder](findfolder.md)请求一起使用。 该属性必须适用于访问的文件夹或项目。 使用扩展属性访问其他属性。 如果给定项的属性不存在，则将不会在生成的 XML 中发出相应的元素。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。 
  
此元素为可选。
  
## <a name="example"></a>示例

以下请求示例演示如何使用**AdditionalProperties**元素获取项目主题。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   

