---
title: BodyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BodyType
api_type:
- schema
ms.assetid: d42ec77b-fb9f-404a-9bf2-1801e8744676
description: BodyType 元素标识如何响应中设置的正文文本的格式。
ms.openlocfilehash: f8be2e96390b40faa367cf0d34c533accc3b8afb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753363"
---
# <a name="bodytype"></a>BodyType

**BodyType**元素标识如何响应中设置的正文文本的格式。 
  
```xml
<BodyType>Best or HTML or Text</BodyType>
```

**BodyTypeResponseType**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> | 标识项目属性和 GetItem、 FindItem 或 SyncFolderItems 响应中包括的内容。  <br/><br/>下面是此元素的 XPath 表达式：<br/><br/>  `/GetItem/ItemShape`<br/><br/>`/FindItem/ItemShape`<br/><br/>`/SyncFolderItems/ItemShape` <br/> |
|[AttachmentShape](attachmentshape.md) <br/> |标识要[GetAttachment](getattachment.md)请求的响应中返回的其他扩展的项属性。  <br/><br/>以下是此元素的 XPath 表达式：<br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**BodyType**元素的可能值。 
  
|**值**|**说明**|
|:-----|:-----|
|最佳  <br/> |响应将返回正文文本的丰富的可用内容。 这很有用，如果不知道的内容是否是文本或 HTML。<br/><br/> 返回的正文将文本，如果存储的正文采用纯文本。 否则，如果存储的正文采用 HTML 或 RTF 格式响应将返回 HTML。<br/><br/> 这是默认值。  <br/> |
|HTML  <br/> |响应将以 HTML 形式返回项目正文。  <br/> |
|Text  <br/> |响应将以纯文本形式返回项目正文。  <br/> |
   
## <a name="remarks"></a>注解

您可以标识正文响应中返回通过检查[Body](body.md)元素的**BodyType**属性的类型。 **BodyType**属性将标识以 HTML 或文本正文。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="example"></a>示例

请求的下面的示例演示使用**BodyType**元素的位置。 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape>
        <t:BodyType>Best</t:BodyType>
      </AttachmentShape>
      <AttachmentIds>
        <t:AttachmentId Id="ASkAS="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

已缩短的 Id 属性保留可读性。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   

