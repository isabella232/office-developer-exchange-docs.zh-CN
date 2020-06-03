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
description: Office.mailboxenums.bodytype 元素标识如何在响应中设置正文文本的格式。
ms.openlocfilehash: 448d20ac54b09a2f4f6a273a1099519371ac7f5b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465945"
---
# <a name="bodytype"></a>BodyType

**Office.mailboxenums.bodytype**元素标识如何在响应中设置正文文本的格式。 
  
```xml
<BodyType>Best or HTML or Text</BodyType>
```

**BodyTypeResponseType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> | 标识要包括在 GetItem、FindItem 或 SyncFolderItems 响应中的项目属性和内容。  <br/><br/>下面是此元素的 XPath 表达式：<br/><br/>  `/GetItem/ItemShape`<br/><br/>`/FindItem/ItemShape`<br/><br/>`/SyncFolderItems/ItemShape` <br/> |
|[AttachmentShape](attachmentshape.md) <br/> |标识要在对[GetAttachment](getattachment.md)请求的响应中返回的其他扩展项属性。  <br/><br/>下面是此元素的 XPath 表达式： <br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**office.mailboxenums.bodytype**元素的可能值。 
  
|**值**|**说明**|
|:-----|:-----|
|最好  <br/> |响应将返回正文文本的最丰富的可用内容。 如果不知道内容是文本还是 HTML，这将非常有用。<br/><br/> 如果存储的正文为纯文本，则返回的正文将为文本。 否则，如果存储的正文是 HTML 格式或 RTF 格式，则响应将返回 HTML。<br/><br/> 此值为默认值。  <br/> |
|HTML  <br/> |响应将以 HTML 形式返回项目正文。  <br/> |
|文本  <br/> |响应将以纯文本形式返回项目正文。  <br/> |
   
## <a name="remarks"></a>备注

您可以通过检查[body](body.md)元素的**office.mailboxenums.bodytype**属性来标识响应中返回的正文的类型。 **Office.mailboxenums.bodytype**属性将正文标识为 HTML 或文本。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="example"></a>示例

下面的请求示例显示了**office.mailboxenums.bodytype**元素的使用位置。 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

已缩短 Id 属性以保留可读性。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   

