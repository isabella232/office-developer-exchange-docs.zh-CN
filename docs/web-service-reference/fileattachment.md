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
description: FileAttachment 元素表示附加到 Exchange 存储中的项目的文件。
ms.openlocfilehash: db9b541fb2527ae3c09cbdb33bedea7fb215bd30
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461014"
---
# <a name="fileattachment"></a>FileAttachment

**FileAttachment**元素表示附加到 Exchange 存储中的项目的文件。 
  
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
|[名称（AttachmentType）](name-attachmenttype.md) <br/> |代表附件的名称。  <br/> |
|[ContentType](contenttype.md) <br/> |描述附件内容的多用途 Internet 邮件扩展（MIME）类型。  <br/> |
|[ContentId](contentid.md) <br/> |表示附件内容的标识符。 [ContentId](contentid.md)可以设置为任何字符串值。 应用程序可以使用[ContentId](contentid.md)来实现自己的标识机制。  <br/> |
|[ContentLocation](contentlocation.md) <br/> |包含与附件内容的位置相对应的统一资源标识符（URI）。  <br/> |
|[大小](size.md) <br/> |表示文件附件的大小（以字节为单位）。  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |表示上次修改文件附件的时间。  <br/> |
|[IsInline](isinline.md) <br/> |表示附件是否内联显示在项目中。  <br/> |
|[IsContactPhoto](iscontactphoto.md) <br/> |指示文件附件是否为联系人图片。  <br/> |
|[Content](content.md) <br/> |包含文件附件的 Base64 编码的内容。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[附件](attachments-ex15websvcsotherref.md) <br/> |包含附加到 Exchange 存储中的项目的项目或文件。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

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

