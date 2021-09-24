---
title: FileAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FileAttachment
api_type:
- schema
ms.assetid: 3ecea174-73d1-47fd-8917-6065cef1d565
description: FileAttachment 元素表示附加到项目存储中的Exchange文件。
ms.openlocfilehash: 66424fefafd2084bf0b6f45881089448593e621d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518496"
---
# <a name="fileattachment"></a>FileAttachment

**FileAttachment** 元素表示附加到项目存储中的Exchange文件。 
  
```XML
<FileAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <IsContactPhoto/>
   <Content/>
</FileAttachment>
```

 **FileAttachmentType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[AttachmentId](attachmentid.md) <br/> |标识文件附件。  <br/> |
|[Name (AttachmentType)](name-attachmenttype.md) <br/> |表示附件的名称。  <br/> |
|[ContentType](contenttype.md) <br/> |介绍附件内容的 MIME (类型) 多用途 Internet 邮件扩展。  <br/> |
|[ContentId](contentid.md) <br/> |表示附件内容的标识符。 [ContentId](contentid.md) 可以设置为任何字符串值。 应用程序可以使用 [ContentId](contentid.md) 实现自己的标识机制。  <br/> |
|[ContentLocation](contentlocation.md) <br/> |包含对应于 () 位置的统一资源标识符 URI。  <br/> |
|[尺寸](size.md) <br/> |表示文件附件的大小（以字节为单位）。  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |表示上次修改文件附件时。  <br/> |
|[IsInline](isinline.md) <br/> |表示附件是否内联显示在项目内。  <br/> |
|[IsContactPhoto](iscontactphoto.md) <br/> |指示文件附件是否是联系人图片。  <br/> |
|[Content](content.md) <br/> |包含文件附件的 Base64 编码内容。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[附件](attachments-ex15websvcsotherref.md) <br/> |包含附加到项目存储中的项目或Exchange文件。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

