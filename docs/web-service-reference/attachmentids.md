---
title: AttachmentIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AttachmentIds
api_type:
- schema
ms.assetid: 46ce3ad7-4b20-43ae-8c63-39f1e3c2666b
description: AttachmentIds 元素包含一组附件标识符。
ms.openlocfilehash: a631edbd1b82f3bbf7b99014d623fbb0072bb0c8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525132"
---
# <a name="attachmentids"></a>AttachmentIds

**AttachmentIds** 元素包含一组附件标识符。 
  
```xml
<AttachmentIds>
   <AttachmentId Id=""/>
</AttachmentIds>
```

 **NonEmptyArrayOfRequestAttachmentIdsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[AttachmentId (GetAttachment and DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md) <br/> |标识单个附件的元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DeleteAttachment](deleteattachment.md) <br/> |定义从附件存储中删除附件Exchange元素。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/DeleteAttachment` <br/> |
|[GetAttachment](getattachment.md) <br/> |定义从附件存储获取附件Exchange元素。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/GetAttachment` <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [DeleteAttachment 操作](deleteattachment-operation.md)
- [GetAttachment 操作](getattachment-operation.md)

