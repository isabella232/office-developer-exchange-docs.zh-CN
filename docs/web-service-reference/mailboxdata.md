---
title: MailboxData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxData
api_type:
- schema
ms.assetid: e9e3f50c-5a7b-49c7-a9ea-117959c08352
description: MailboxData 元素表示单个邮箱用户，以及有关邮箱用户要返回的数据类型的选项。
ms.openlocfilehash: bfcb8c01d40af81097c7d9868006fe9b7b5519d4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467247"
---
# <a name="mailboxdata"></a>MailboxData

**MailboxData**元素表示单个邮箱用户，以及有关邮箱用户要返回的数据类型的选项。 
  
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
- [MailboxDataArray](mailboxdataarray.md)
  
- [MailboxData](mailboxdata.md)
  
```xml
<MailboxData>
   <Email>...</Email>
   <AttendeeType>...</AttendeeType>
   <ExcludeConflicts>...</ExcludeConflicts>
<MailboxData>
```

**MailboxData**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[电子邮件（EmailAddressType）](email-emailaddresstype.md) <br/> |表示 GetUserAvailability 查询的邮箱用户。  <br/> |
|[AttendeeType](attendeetype.md) <br/> |表示在[Email （EmailAddressType）](email-emailaddresstype.md)元素中标识的与会者的类型。 这用于会议建议的请求。  <br/> |
|[ExcludeConflicts](excludeconflicts.md) <br/> |指定是否为日历时间返回在与会者之间发生冲突的建议时间。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MailboxDataArray](mailboxdataarray.md) <br/> |包含要查询可用性信息的邮箱的列表。  <br/> 以下是此元素的 XPath：  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]` <br/> |
   
## <a name="remarks"></a>备注

客户端应用程序可以定义一个到多个**MailboxData**元素。 
  
> [!NOTE]
> 描述此元素的架构位于运行 Exchange Server 2007 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。 
  
## <a name="example"></a>示例

```xml
<MailboxDataArray>
  <MailboxData xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
    <Email>
      <Name></Name>
      <Address>someone@ExServer.example.com</Address>
      <RoutingType>SMTP</RoutingType>
    </Email>
    <AttendeeType>Organizer</AttendeeType>
    <ExcludeConflicts>false</ExcludeConflicts>
  </MailboxData>
</MailboxDataArray>
```

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

