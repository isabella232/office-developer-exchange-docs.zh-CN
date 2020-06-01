---
title: DeliverMeetingRequests
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeliverMeetingRequests
api_type:
- schema
ms.assetid: 04b999af-0b27-4e6d-a8b1-400955a1afaa
description: DeliverMeetingRequests 元素定义如何在代理和主体之间处理会议请求。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 3998443613437bca2267678f7bc2c5584b779135
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463676"
---
# <a name="delivermeetingrequests"></a>DeliverMeetingRequests

**DeliverMeetingRequests**元素定义如何在代理和主体之间处理会议请求。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
```XML
<DeliverMeetingRequests>DelegatesOnly or DelegatesAndMe or DelegatesAndSendInformationToMe or NoForward</DeliverMeetingRequests>
```

 **DeliverMeetingRequestsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[AddDelegate](adddelegate.md) <br/> |定义请求以将代理人添加到邮箱。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[UpdateDelegate](updatedelegate.md) <br/> |定义请求以更新邮箱中的代理人。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |包含 GetDelegate 请求的状态和结果。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**DeliverMeetingRequests**元素的可能值。 
  
**DeliverMeetingRequests 元素值**

|**值**|**说明**|
|:-----|:-----|
|DelegatesOnly  <br/> |将会议请求转发到代理并移动到主体邮箱中的 "已删除邮件" 文件夹。  <br/> |
|DelegatesAndMe  <br/> |会议请求将转发给代理，并保留在主体邮箱的 "收件箱" 文件夹中。  <br/> |
|DelegatesAndSendInformationToMe  <br/> |会议请求将转发给代理，并保留在主体邮箱的 "收件箱" 文件夹中，但 "接受"、"暂定" 和 "拒绝" 按钮不会显示在 Microsoft Office Outlook 阅读窗格中。  <br/> |
|NoForward  <br/> |不会将会议请求转发给代理。  <br/> |
   
## <a name="remarks"></a>备注

**DeliverMeetingRequests**设置影响主体邮箱中的所有委派。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [AddDelegate 操作](adddelegate-operation.md)  
- [UpdateDelegate 操作](updatedelegate-operation.md)  
- [GetDelegate 操作](getdelegate-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [添加委派](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

