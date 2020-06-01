---
title: AttendeeType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttendeeType
api_type:
- schema
ms.assetid: 048043a8-dbad-45a0-97c8-4cad63d8898b
description: AttendeeType 元素表示在 Email （EmailAddressType）元素中标识的与会者的类型。 此元素用于会议建议的请求中。
ms.openlocfilehash: 104b9f38cc891310ecb47c0b47837a912ced6ab7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462295"
---
# <a name="attendeetype"></a>AttendeeType

**AttendeeType**元素表示在[Email （EmailAddressType）](email-emailaddresstype.md)元素中标识的与会者的类型。 此元素用于会议建议的请求中。 
  
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
- [MailboxDataArray](mailboxdataarray.md)
  
- [MailboxData](mailboxdata.md)
  
- [AttendeeType](attendeetype.md)
  
```xml
<AttendeeType>Organizer or Required or Optional or Room or Resource</AttendeeType>
```

 **MeetingAttendeeType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[MailboxData](mailboxdata.md) <br/> |代表单个邮箱用户以及有关邮箱用户要返回的数据类型的选项。  <br/> 以下是此元素的 XPath：  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="text-value"></a>文本值

此元素需要一个文本值。 下表列出了此元素的可能值。
  
|**值**|**说明**|
|:-----|:-----|
|Organizer  <br/> |创建日历项目的邮箱用户和与会者。  <br/> |
|必需  <br/> |会议所必需的与会者的邮箱用户。  <br/> |
|可选  <br/> |作为会议的可选与会者的邮箱用户。  <br/> |
|房间  <br/> |表示用于会议的会议室资源的邮箱实体。  <br/> |
|Resource  <br/> |安排在会议中使用的一种资源，如电视或投影仪。  <br/> |
   
## <a name="remarks"></a>备注

此元素是[MailboxData](mailboxdata.md)元素的必需子元素。 此元素只能在[MailboxData](mailboxdata.md)元素中出现一次。 描述此元素的架构位于运行 MicrosoftExchange Server 2007 且安装了客户端访问服务器角色的计算机的/EWS/目录中。 
  
> [!NOTE]
> AttendeeType 架构类型用于表示与会者的日历项目。 请勿将此元素与 AttendeeType 架构类型的元素混淆。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetUserAvailability 操作](getuseravailability-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

