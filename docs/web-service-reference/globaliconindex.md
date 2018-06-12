---
title: GlobalIconIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3d28ed70-4cfe-46e4-8d15-593c6e355bcf
description: GlobalIconIndex 元素标识会话中的所有项目的全局图标索引。
ms.openlocfilehash: e8d78bfcfc0e57df9230db86e080d1ee29878094
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825727"
---
# <a name="globaliconindex"></a>GlobalIconIndex

**GlobalIconIndex**元素标识会话中的所有项目的全局图标索引。 
  
```XML
<IconIndex>Default | PostItem | MailRead | MailUnread | MailReplied | MailForwarded | MailEncrypted | MailSmimeSigned | MailEncrytedReplied | MailSmimeSignedReplied | MailEncryptedForwarded | MailSmimeSignedForwarded | MailEncryptedRead | MailSmimeSignedRead | MailIrm | MaillrmForwarded | MaillrmReplied | SmsSubmitted | SmsRoutedToDeliveryPoint | SmsRoutedToExternalMessagingSystem | SmsDelivered | OutlookDefaultForContacts | AppointmentItem | AppointmentRecur | AppointmentMeet | AppointmentMeetRecur | AppointmentMeetNY | AppointmentMeetYes | AppointmentMeetNo | AppointmentMeetMaybe | AppointmentMeetCancel | AppointmentMeetInfo | TaskItem | TaskRecur | TaskOwned | TaskDelegated</IconIndex>
```

 **IconIndexType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[对话 (ConversationType)](conversation-conversationtype.md) | [项](item.md) | [联系人](contact.md) | [DistributionList](distributionlist.md) | [消息](message-ex15websvcsotherref.md) | [日历项目](calendaritem.md) | [PostItem](postitem.md) | [任务](task.md)
  
## <a name="text-value"></a>文本值

下表包含**GlobalIconIndex**元素的可能的文本值。 
  
|**值**|**说明**|
|:-----|:-----|
|||
|默认  <br/> |指定的默认图标。  <br/> |
|PostItem  <br/> |指定一个公告项目的图标。  <br/> |
|MailRead  <br/> |指定邮件读取图标。  <br/> |
|MailUnread  <br/> |指定未读的邮件图标。  <br/> |
|MailReplied  <br/> |指定答复邮件图标。  <br/> |
|MailForwarded  <br/> |指定的转发的邮件图标。  <br/> |
|MailEncrypted  <br/> |指定加密的邮件图标。  <br/> |
|MailSmimeSigned  <br/> |指定安全/多用途 Internet 邮件扩展 (S/MIME) 签名的邮件图标。  <br/> |
|MailEncryptedReplied  <br/> |指定加密答复邮件图标。  <br/> |
|MailSmimeSignedReplied  <br/> |指定 S/MIME 签名答复邮件图标。  <br/> |
|MailEncryptedForwarded  <br/> |指定的转发的邮件加密的图标。  <br/> |
|MailSmimeSignedForwarded  <br/> |指定签名的 S/MIME 转发邮件图标。  <br/> |
|MailEncryptedRead  <br/> |指定读取的加密的邮件图标。  <br/> |
|MailSmimeSignedRead  <br/> |指定签名的 S/MIME 读取邮件图标。  <br/> |
|MailIrm  <br/> |指定受信息权限管理 IRM 保护的邮件图标。  <br/> |
|MailIrmForwarded  <br/> |指定受 IRM 保护转发邮件图标。  <br/> |
|MailIrmReplied  <br/> |指定受 IRM 保护答复邮件图标。  <br/> |
|SmsSubmitted  <br/> |指定短信服务 (SMS) 传送所提交的邮件的图标。  <br/> |
|SmsRoutedToDeliveryPoint  <br/> |指定 SMS 传送到一个外部传递点的图标。  <br/> |
|SmsRoutedToExternalMessagingSystem  <br/> |指定 SMS 路由到外部邮件系统的图标。  <br/> |
|SmsDelivered  <br/> |指定 SMS 发送的邮件图标。  <br/> |
|OutlookDefaultForContacts  <br/> |指定联系人的默认图标。  <br/> |
|AppointmentItem  <br/> |指定约会项目图标。  <br/> |
|AppointmentRecur  <br/> |指定的定期约会图标。  <br/> |
|AppointmentMeet  <br/> |指定会议图标。  <br/> |
|AppointmentMeetRecur  <br/> |指定定期会议图标。  <br/> |
|AppointmentMeetNY  <br/> |指定对会议的暂定响应的图标。  <br/> |
|AppointmentMeetYes  <br/> |指定会议验收图标。  <br/> |
|AppointmentMeetNo  <br/> |指定会议拒绝的图标。  <br/> |
|AppointmentMeetMaybe  <br/> |指定对会议的也许响应的图标。  <br/> |
|AppointmentMeetCancel  <br/> |指定会议取消图标。  <br/> |
|AppointmentMeetInfo  <br/> |指定会议信息图标。  <br/> |
|TaskItem  <br/> |指定任务项目图标。  <br/> |
|TaskRecur  <br/> |指定定期任务图标。  <br/> |
|TaskOwned  <br/> |指定拥有图标的任务。  <br/> |
|TaskDelegated  <br/> |指定的任务委派的图标。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

