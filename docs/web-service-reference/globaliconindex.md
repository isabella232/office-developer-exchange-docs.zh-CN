---
title: GlobalIconIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3d28ed70-4cfe-46e4-8d15-593c6e355bcf
description: GlobalIconIndex 元素标识会话中所有项目的全局图标索引。
ms.openlocfilehash: 9900a80136a1a7eaae4634afd31568679f6dba1b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459459"
---
# <a name="globaliconindex"></a>GlobalIconIndex

**GlobalIconIndex**元素标识会话中所有项目的全局图标索引。 
  
```XML
<IconIndex>Default | PostItem | MailRead | MailUnread | MailReplied | MailForwarded | MailEncrypted | MailSmimeSigned | MailEncrytedReplied | MailSmimeSignedReplied | MailEncryptedForwarded | MailSmimeSignedForwarded | MailEncryptedRead | MailSmimeSignedRead | MailIrm | MaillrmForwarded | MaillrmReplied | SmsSubmitted | SmsRoutedToDeliveryPoint | SmsRoutedToExternalMessagingSystem | SmsDelivered | OutlookDefaultForContacts | AppointmentItem | AppointmentRecur | AppointmentMeet | AppointmentMeetRecur | AppointmentMeetNY | AppointmentMeetYes | AppointmentMeetNo | AppointmentMeetMaybe | AppointmentMeetCancel | AppointmentMeetInfo | TaskItem | TaskRecur | TaskOwned | TaskDelegated</IconIndex>
```

 **IconIndexType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[对话（ConversationType）](conversation-conversationtype.md)  | [项](item.md)  | [联系人](contact.md)  | [DistributionList](distributionlist.md)  | [邮件](message-ex15websvcsotherref.md)  | [CalendarItem](calendaritem.md)  | [PostItem](postitem.md)  | [任务](task.md)
  
## <a name="text-value"></a>文本值

下表包含**GlobalIconIndex**元素的可能的文本值。 
  
|**值**|**说明**|
|:-----|:-----|
|||
|默认  <br/> |指定默认图标。  <br/> |
|PostItem  <br/> |指定公告项的图标。  <br/> |
|MailRead  <br/> |指定邮件读取图标。  <br/> |
|MailUnread  <br/> |指定 "未读邮件" 图标。  <br/> |
|MailReplied  <br/> |指定 "答复邮件" 图标。  <br/> |
|MailForwarded  <br/> |指定转发的邮件图标。  <br/> |
|MailEncrypted  <br/> |指定加密的邮件图标。  <br/> |
|MailSmimeSigned  <br/> |指定 "安全/多用途 Internet 邮件扩展（S/MIME）" "签名邮件" 图标。  <br/> |
|MailEncryptedReplied  <br/> |指定已加密答复邮件图标。  <br/> |
|MailSmimeSignedReplied  <br/> |指定 S/MIME 签名答复邮件图标。  <br/> |
|MailEncryptedForwarded  <br/> |指定加密的转发邮件图标。  <br/> |
|MailSmimeSignedForwarded  <br/> |指定 S/MIME 签名的已转发邮件图标。  <br/> |
|MailEncryptedRead  <br/> |指定加密的 "已读邮件" 图标。  <br/> |
|MailSmimeSignedRead  <br/> |指定 S/MIME 签名的阅读邮件图标。  <br/> |
|MailIrm  <br/> |指定信息权限管理（IRM）保护的邮件图标。  <br/> |
|MailIrmForwarded  <br/> |指定受 IRM 保护的转发邮件图标。  <br/> |
|MailIrmReplied  <br/> |指定受 IRM 保护的 "已答复邮件" 图标。  <br/> |
|SmsSubmitted  <br/> |指定用于短信服务（SMS）路由的邮件提交的图标。  <br/> |
|SmsRoutedToDeliveryPoint  <br/> |指定用于将 SMS 路由到外部传递点的图标。  <br/> |
|SmsRoutedToExternalMessagingSystem  <br/> |指定用于将 SMS 路由到外部邮件系统的图标。  <br/> |
|SmsDelivered  <br/> |指定 "发送短信邮件" 图标。  <br/> |
|OutlookDefaultForContacts  <br/> |指定联系人的默认图标。  <br/> |
|AppointmentItem  <br/> |指定约会项图标。  <br/> |
|AppointmentRecur  <br/> |指定定期约会图标。  <br/> |
|AppointmentMeet  <br/> |指定会议图标。  <br/> |
|AppointmentMeetRecur  <br/> |指定定期会议图标。  <br/> |
|AppointmentMeetNY  <br/> |指定对会议的暂定响应的图标。  <br/> |
|AppointmentMeetYes  <br/> |指定 "接受会议" 图标。  <br/> |
|AppointmentMeetNo  <br/> |指定 "已拒绝会议" 图标。  <br/> |
|AppointmentMeetMaybe  <br/> |指定可能响应会议的图标。  <br/> |
|AppointmentMeetCancel  <br/> |指定会议取消图标。  <br/> |
|AppointmentMeetInfo  <br/> |指定 "会议信息" 图标。  <br/> |
|TaskItem  <br/> |指定任务项图标。  <br/> |
|TaskRecur  <br/> |指定定期任务图标。  <br/> |
|TaskOwned  <br/> |指定任务拥有的图标。  <br/> |
|TaskDelegated  <br/> |指定 "任务委派" 图标。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

