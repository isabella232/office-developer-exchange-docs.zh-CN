---
title: MailboxData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MailboxData
api_type:
- schema
ms.assetid: e9e3f50c-5a7b-49c7-a9ea-117959c08352
description: MailboxData 元素表示单个邮箱用户和要返回的邮箱用户数据类型的选项。
ms.openlocfilehash: 62c8c816fc0b0e0c6831d468d90e7303fb72d9be
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546131"
---
# <a name="mailboxdata"></a>MailboxData

**MailboxData** 元素表示单个邮箱用户和要返回的邮箱用户数据类型的选项。 
  
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
|[Email (EmailAddressType)](email-emailaddresstype.md) <br/> |表示 GetUserAvailability 查询的邮箱用户。  <br/> |
|[AttendeeType](attendeetype.md) <br/> |表示 [EmailAddressType ](email-emailaddresstype.md) (元素中标识) 的类型。 在会议建议请求中会使用此功能。  <br/> |
|[ExcludeConflicts](excludeconflicts.md) <br/> |指定是否返回与会者之间发生冲突的日历时间的建议时间。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MailboxDataArray](mailboxdataarray.md) <br/> |包含要查询可用性信息的邮箱列表。  <br/> 下面是此元素的 XPath：  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]` <br/> |
   
## <a name="remarks"></a>注解

客户端应用程序可以定义一到多个 **MailboxData** 元素。 
  
> [!NOTE]
> 描述此元素的架构位于运行 Exchange Server 2007（已安装客户端访问服务器角色）的计算机的 EWS 虚拟目录中。 
  
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

