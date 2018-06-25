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
description: MailboxType 元素表示由的电子邮件地址的邮箱的类型。
ms.openlocfilehash: d7232377951e8d9c8f191ac856058bc28467cadd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826305"
---
# <a name="mailboxtype"></a>MailboxType

**MailboxType**元素表示由的电子邮件地址的邮箱的类型。 
  
```XML
<MailboxType>Mailbox | PublicDL | PrivateDL | Contact | PublicFolder | Unknown | OneOff | GroupMailbox</MailboxType>
```

**MailboxTypeType**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |标识完全解析电子邮件地址。  <br/> |
|[RoomList](roomlist.md) <br/> |标识会议室的列表。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**MailboxType**元素的可能值。 
  
|**值**|**说明**|
|:-----|:-----|
|Mailbox  <br/> |代表已启用邮件的 Active Directory 对象。  <br/> |
|PublicDL  <br/> |代表一个公用通讯组列表。  <br/> |
|PrivateDL  <br/> |表示用户的邮箱中的私人通讯组列表。  <br/> |
|联系人  <br/> |代表用户的邮箱中的联系人。  <br/> |
|PublicFolder  <br/> |代表公用文件夹。  <br/> |
|Unknown  <br/> |代表未知的类型的邮箱。  <br/> |
|OneOff  <br/> |代表个人通讯组列表的一次性成员。  <br/> |
|GroupMailbox  <br/> |代表组邮箱。  <br/> |
   
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

