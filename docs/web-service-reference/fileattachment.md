---
title: FileAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FileAttachment
api_type:
- schema
ms.assetid: 3ecea174-73d1-47fd-8917-6065cef1d565
description: FileAttachment 元素表示附加到 Exchange 存储中的项的文件。
ms.openlocfilehash: 5ce7aef753313aa9430f640bb3c26f652b8c1c43
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754310"
---
# <a name="fileattachment"></a>FileAttachment

**FileAttachment**元素表示附加到 Exchange 存储中的项的文件。 
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[AttachmentId](attachmentid.md) <br/> |标识的文件附件。  <br/> |
|[名称 (AttachmentType)](name-attachmenttype.md) <br/> |表示附件的名称。  <br/> |
|[ContentType](contenttype.md) <br/> |描述附件内容多用途 Internet 邮件扩展 (MIME) 类型。  <br/> |
|[ContentId](contentid.md) <br/> |表示内容的附件的标识符。 [ContentId](contentid.md)可以设置为任何字符串值。 应用程序可以使用[ContentId](contentid.md)来实现自己标识机制。  <br/> |
|[ContentLocation](contentlocation.md) <br/> |包含附件的内容的位置所对应的统一资源标识符 (URI)。  <br/> |
|[Size](size.md) <br/> |表示以字节为单位的附件文件的大小。  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |表示上次修改文件附件。  <br/> |
|[IsInline](isinline.md) <br/> |表示是否附件显示为内嵌项目中。  <br/> |
|[IsContactPhoto](iscontactphoto.md) <br/> |指示附件是否是联系人的图片。  <br/> |
|[内容](content.md) <br/> |包含 Base64 编码的文件附件的内容。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[附件](attachments-ex15websvcsotherref.md) <br/> |包含的项或附加到 Exchange 存储中的项目文件。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

