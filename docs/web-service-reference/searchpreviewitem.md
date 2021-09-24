---
title: SearchPreviewItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 59b0b2db-a0ae-4162-a2cb-5f37f42fe872
description: SearchPreviewItem 元素指定发现搜索的项目预览。
ms.openlocfilehash: 7ecc034de3386ed35f0071403c013e91b79d13c5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59534299"
---
# <a name="searchpreviewitem"></a>SearchPreviewItem

**SearchPreviewItem** 元素指定发现搜索的项目预览。 
  
```XML
<SearchPreviewItem>
   <Id/>
   <Mailbox/>
   <ParentId/>
   <ItemClass/>
   <UniqueHash/>
   <SortValue/>
   <OwaLink/>
   <Sender/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <CreatedTime/>
   <ReceivedTime/>
   <SentTime/>
   <Subject/>
   <Size/>
   <Preview/>
   <Importance/>
   <Read/>
   <HasAttachment/>
   <ExtendedProperties/>
</SearchPreviewItem>
```

 **SearchPreviewItemType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[Id (ItemIdType) ](id-itemidtype.md)  | [Mailbox (PreviewItemMailboxType) ](mailbox-previewitemmailboxtype.md)  | [ParentId](parentid.md)  | [ItemClass](itemclass.md)  | [UniqueHash](uniquehash.md)  | [SortValue](sortvalue.md)  | [OwaLink](owalink.md)  | [发件人 (字符串) ](sender-string.md)  | [ToRecipients (ArrayOfSmtpAddressType) ](torecipients-arrayofsmtpaddresstype.md)  | [CcRecipients](ccrecipients.md)  | [BccRecipients](bccrecipients.md)  | [CreatedTime](createdtime.md)  | [ReceivedTime](receivedtime.md)  | [SentTime](senttime.md)  | [主题](subject.md)  | [长 (大小) ](size-long.md)  | [预览](preview-ex15websvcsotherref.md)  | [重要性](importance.md)  | [读取](read.md)  | [HasAttachment](hasattachment.md)  | [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType) ](extendedproperties-nonemptyarrayofextendedpropertytype.md)
  
### <a name="parent-elements"></a>父元素

[Items (ArrayOfSearchPreviewItemsType)](items-arrayofsearchpreviewitemstype.md)
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

