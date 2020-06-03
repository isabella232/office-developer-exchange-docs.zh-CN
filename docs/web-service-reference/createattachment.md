---
title: CreateAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAttachment
api_type:
- schema
ms.assetid: e33b403a-b7d3-48ee-8d24-6b7abf0d70bc
description: CreateAttachment 元素定义一个请求，用于创建到 Exchange 存储中的项目的附件。
ms.openlocfilehash: 4cba1b8865dae5da58b9617b249a29314c67331a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466435"
---
# <a name="createattachment"></a>CreateAttachment

**CreateAttachment**元素定义一个请求，用于创建到 Exchange 存储中的项目的附件。 
  
```xml
<CreateAttachment>
   <ParentItemId/>
   <Attachments/>
</CreateAttachment>
```

 **CreateAttachmentType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ParentItemId](parentitemid.md) <br/> |标识包含创建的附件的父 Exchange 存储项。 [ParentItemId](parentitemid.md)元素必须提供实际 Exchange 存储项的 ID。 可以使用[GetItem 操作](getitem-operation.md)检索真实的存储项;附件是通过使用[GetAttachment 操作](getattachment-operation.md)检索的。 如果[ParentItemId](parentitemid.md)传递的是文件附件的 ID，则会发生错误。 如果[ParentItemId](parentitemid.md)代表现有项目附件的 ID，则[CreateAttachment 操作](createattachment-operation.md)会将新附件添加到现有附件中。  <br/> 此元素是[CreateAttachment 操作](createattachment-operation.md)所必需的。  <br/> |
|[附件](attachments-ex15websvcsotherref.md) <br/> |包含要附加到 Exchange 存储中的项目的项目或文件。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

项目附件不作为存储项存在。 它仅作为项目附件或其他附件存在。 仅可使用[GetAttachment](getattachment.md)请求检索项目附件。 
  
可以创建以下项附件：
  
- 项目
    
- 消息
    
- CalendarItem
    
- Contact
    
- 任务
    
- MeetingMessage
    
- MeetingRequest
    
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="example"></a>示例

下面的示例演示如何创建项目并将其附加到 Exchange 存储中的其他项目。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <ParentItemId Id="ASkAS"/>
      <Attachments>
        <t:ItemAttachment>
          <t:Name>MyAttachment</t:Name>
          <t:Message>
            <t:ItemClass>IPM>Note</t:ItemClass>
            <t:Subject>My attachment subject</t:Subject>
            <t:Body BodyType="Text">My attachment body</t:Body>
          </t:Message>
        </t:ItemAttachment>
      </Attachments>
    </CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[CreateAttachment 操作](createattachment-operation.md)
  
[DeleteAttachment 操作](deleteattachment-operation.md)
  
[GetAttachment 操作](getattachment-operation.md)

