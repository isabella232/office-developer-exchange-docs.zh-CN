---
title: MailboxType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MailboxType
api_type:
- schema
ms.assetid: 696e5fdb-d8c5-40f0-9e79-885eae65dfa4
description: MailboxType 元素表示由电子邮件地址表示的邮箱的类型。
ms.openlocfilehash: f7605bf0e90851352efaaabed09e878be0925581
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524047"
---
# <a name="mailboxtype"></a>MailboxType

**MailboxType** 元素表示由电子邮件地址表示的邮箱的类型。 
  
```XML
<MailboxType>Mailbox | PublicDL | PrivateDL | Contact | PublicFolder | Unknown | OneOff | GroupMailbox</MailboxType>
```

**MailboxTypeType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |标识完全解析的电子邮件地址。  <br/> |
|[RoomList](roomlist.md) <br/> |标识会议室列表。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了 **MailboxType** 元素的可能值。 
  
|**值**|**说明**|
|:-----|:-----|
|邮箱  <br/> |表示启用邮件的 Active Directory 对象。  <br/> |
|PublicDL  <br/> |代表一个公共通讯组列表。  <br/> |
|PrivateDL  <br/> |表示用户邮箱中的专用通讯组列表。  <br/> |
|联系人  <br/> |表示用户邮箱中的联系人。  <br/> |
|PublicFolder  <br/> |表示公用文件夹。  <br/> |
|未知  <br/> |表示未知类型的邮箱。  <br/> |
|OneOff  <br/> |代表个人通讯组列表的一次成员。  <br/> |
|GroupMailbox  <br/> |表示组邮箱。  <br/> |
   
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

