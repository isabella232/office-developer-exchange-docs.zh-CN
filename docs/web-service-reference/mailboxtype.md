---
title: MailboxType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxType
api_type:
- schema
ms.assetid: 696e5fdb-d8c5-40f0-9e79-885eae65dfa4
description: MailboxType 元素表示电子邮件地址所代表的邮箱的类型。
ms.openlocfilehash: 8c322ab8a87730832f5d199698a369656b058a9a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459796"
---
# <a name="mailboxtype"></a>MailboxType

**MailboxType**元素表示电子邮件地址所代表的邮箱的类型。 
  
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

|**元素**|**描述**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |标识完全解析的电子邮件地址。  <br/> |
|[RoomList](roomlist.md) <br/> |标识会议室列表。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**MailboxType**元素的可能值。 
  
|**值**|**说明**|
|:-----|:-----|
|邮箱  <br/> |表示启用邮件的 Active Directory 对象。  <br/> |
|PublicDL  <br/> |代表公共通讯组列表。  <br/> |
|PrivateDL  <br/> |代表用户邮箱中的专用通讯组列表。  <br/> |
|Contact  <br/> |表示用户邮箱中的联系人。  <br/> |
|Set-publicfolder  <br/> |表示公用文件夹。  <br/> |
|未知  <br/> |代表未知类型的邮箱。  <br/> |
|OneOff  <br/> |表示个人通讯组列表的一次性成员。  <br/> |
|GroupMailbox  <br/> |代表组邮箱。  <br/> |
   
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

