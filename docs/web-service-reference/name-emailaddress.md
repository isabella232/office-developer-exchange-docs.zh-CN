---
title: 名称（EmailAddress）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Name
api_type:
- schema
ms.assetid: c719c55f-d625-4e64-846f-50ac91881443
description: Name 元素表示邮箱用户的显示名称。
ms.openlocfilehash: 2c6b29f1b069f9cc72ac84e7aebfff99437e630a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44466953"
---
# <a name="name-emailaddress"></a>名称（EmailAddress）

**Name**元素表示邮箱用户的显示名称。 
  
```xml
<Name/>
```

**String**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[电子邮件（EmailAddressType）](email-emailaddresstype.md) <br/> |表示 GetUserAvailability 查询的邮箱用户。  <br/> <br/>以下是此元素的 XPath：  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[邮箱（可用性）](mailbox-availability.md) <br/> | 表示 SetUserOofSettings 或 GetUserOofSettings 请求的邮箱用户。  <br/><br/>  下面是此元素的 XPath 表达式：  <br/><br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则需要一个 text 值。
  
## <a name="remarks"></a>备注

此元素最多可在[电子邮件（EmailAddressType）](email-emailaddresstype.md)元素中出现一次。 此元素不是必需的。 
  
> [!NOTE]
> 描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。 
  
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

