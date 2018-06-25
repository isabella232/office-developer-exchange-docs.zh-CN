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
description: DeliverMeetingRequests 元素定义委托和主体之间确定如何处理会议请求。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 803bd2da72bdb21b507a59cc11635a40d4431acf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753831"
---
# <a name="delivermeetingrequests"></a>DeliverMeetingRequests

**DeliverMeetingRequests**元素定义委托和主体之间确定如何处理会议请求。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。 
  
```XML
<DeliverMeetingRequests>DelegatesOnly or DelegatesAndMe or DelegatesAndSendInformationToMe or NoForward</DeliverMeetingRequests>
```

 **DeliverMeetingRequestsType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AddDelegate](adddelegate.md) <br/> |定义请求以将代理人添加到邮箱。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[UpdateDelegate](updatedelegate.md) <br/> |定义请求以更新邮箱中的代理人。 Exchange 2007 SP1 中引入了此元素。  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |包含状态和 GetDelegate 请求的结果。 在 Exchange 2007 SP1 引入了此元素。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**DeliverMeetingRequests**元素的可能值。 
  
**DeliverMeetingRequests 元素的值**

|**值**|**说明**|
|:-----|:-----|
|DelegatesOnly  <br/> |会议请求的转发到委派和移动到的主体的邮箱中的已删除邮件文件夹。  <br/> |
|DelegatesAndMe  <br/> |会议请求转发到委派和保留在的主体的邮箱中收件箱文件夹中。  <br/> |
|DelegatesAndSendInformationToMe  <br/> |会议请求转发到委派和保留的收件箱文件夹中的主体的邮箱，但不是在 Microsoft Office Outlook 阅读窗格中显示接受、 暂定和拒绝按钮。  <br/> |
|NoForward  <br/> |会议请求不转发到委派。  <br/> |
   
## <a name="remarks"></a>注解

**DeliverMeetingRequests**设置会影响的主体的邮箱中的所有代理人。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [AddDelegate 操作](adddelegate-operation.md)  
- [UpdateDelegate 操作](updatedelegate-operation.md)  
- [GetDelegate 操作](getdelegate-operation.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [添加代理人](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

