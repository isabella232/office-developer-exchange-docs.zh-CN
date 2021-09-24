---
title: AttendeeType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AttendeeType
api_type:
- schema
ms.assetid: 048043a8-dbad-45a0-97c8-4cad63d8898b
description: AttendeeType 元素表示 EmailAddressType (元素中标识的与会者) 类型。 此元素用于请求会议建议。
ms.openlocfilehash: 5bcec50fe6cccc3df48ca9615dbd0d9418211b4b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533932"
---
# <a name="attendeetype"></a>AttendeeType

**AttendeeType** 元素表示 [EmailAddressType](email-emailaddresstype.md) (元素中标识) 的类型。 此元素用于请求会议建议。 
  
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

|**元素**|**说明**|
|:-----|:-----|
|[MailboxData](mailboxdata.md) <br/> |表示单个邮箱用户和要返回的邮箱用户数据类型的选项。  <br/> 下面是此元素的 XPath：  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="text-value"></a>文本值

此元素需要文本值。 下表列出了此元素的可能值。
  
|**值**|**说明**|
|:-----|:-----|
|组织者  <br/> |创建日历项目的邮箱用户和与会者。  <br/> |
|必需  <br/> |作为会议必做与会者的邮箱用户。  <br/> |
|可选  <br/> |作为会议可选与会者的邮箱用户。  <br/> |
|Room  <br/> |一个邮箱实体，表示用于会议的会议室资源。  <br/> |
|资源  <br/> |计划用于会议的资源，如电视或投影仪。  <br/> |
   
## <a name="remarks"></a>注解

此元素是 [MailboxData](mailboxdata.md) 元素的必需子元素。 此元素只能在 [MailboxData](mailboxdata.md) 元素中出现一次。 描述此元素的架构位于运行已安装客户端访问服务器角色的 MicrosoftExchange Server 2007 的计算机的 /EWS/ 目录中。 
  
> [!NOTE]
> AttendeeType 架构类型用于表示日历项目的与会者。 不要将此元素与 AttendeeType 架构类型的元素相混淆。 
  
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

