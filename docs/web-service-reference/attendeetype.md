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
description: AttendeeType 元素表示与会者的电子邮件 (EmailAddressType) 元素中标识的类型。 此元素是请求中使用的会议建议。
ms.openlocfilehash: a08532ed78296102ee252c1e0c40beee7ca8ea5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753288"
---
# <a name="attendeetype"></a>AttendeeType

**AttendeeType**元素表示与会者的[电子邮件 (EmailAddressType)](email-emailaddresstype.md)元素中标识的类型。 此元素是请求中使用的会议建议。 
  
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
- [MailboxDataArray](mailboxdataarray.md)
  
- [MailboxData](mailboxdata.md)
  
- [AttendeeType](attendeetype.md)
  
```xml
<AttendeeType>Organizer or Required or Optional or Room or Resource</AttendeeType>
```

 **MeetingAttendeeType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MailboxData](mailboxdata.md) <br/> |代表单个邮箱用户和类型的数据的选项，将返回有关邮箱用户。  <br/> 以下是此元素的 XPath:  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="text-value"></a>文本值

需要为此元素的文本值。 下表列出了此元素的可能值。
  
|**值**|**说明**|
|:-----|:-----|
|组织者  <br/> |邮箱用户和创建的日历项目的与会者。  <br/> |
|必需  <br/> |作为会议必需的与会者的邮箱用户。  <br/> |
|可选  <br/> |作为会议可选与会者的邮箱用户。  <br/> |
|聊天室  <br/> |表示用于会议的会议室资源邮箱实体。  <br/> |
|资源  <br/> |如 TV 或计划在会议中使用的投影仪资源。  <br/> |
   
## <a name="remarks"></a>备注

此元素是[MailboxData](mailboxdata.md)元素的必需的子元素。 此元素[MailboxData](mailboxdata.md)元素中只能出现一次。 描述此元素的架构位于运行 MicrosoftExchange Server 2007 的安装了客户端访问服务器角色的计算机的 /EWS/ 目录中。 
  
> [!NOTE]
> AttendeeType 架构类型用于表示与会者的日历项目。 请勿将此元素包含 AttendeeType 架构类型元素的混淆。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetUserAvailability 操作](getuseravailability-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [Getting User Availability](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

