---
title: CreateAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CreateAttachment
api_type:
- schema
ms.assetid: e33b403a-b7d3-48ee-8d24-6b7abf0d70bc
description: CreateAttachment 元素定义创建项目附件的请求，该请求Exchange存储区。
ms.openlocfilehash: 6716a83b0d1ba9d7f39351da60f7009df04a3fa0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515871"
---
# <a name="createattachment"></a>CreateAttachment

**CreateAttachment** 元素定义创建项目附件的请求，该请求Exchange存储区。 
  
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
|[ParentItemId](parentitemid.md) <br/> |标识包含Exchange附件的父存储项目。 [ParentItemId](parentitemid.md)元素必须提供实际存储Exchange ID。 可以使用 [GetItem](getitem-operation.md)操作检索实际存储项目;使用 [GetAttachment](getattachment-operation.md)操作检索附件。 如果将 [ParentItemId](parentitemid.md) 传递给文件附件的 ID，将发生错误。 如果 [ParentItemId](parentitemid.md) 表示现有项目附件的 [ID，CreateAttachment 操作](createattachment-operation.md) 会将新附件添加到现有附件。  <br/> [CreateAttachment](createattachment-operation.md)操作需要此元素。  <br/> |
|[附件](attachments-ex15websvcsotherref.md) <br/> |包含要附加到项目存储中的项目或Exchange文件。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

项目附件不存在为存储项目。 它仅作为项目或其他附件的附件存在。 项目附件只能使用 [GetAttachment](getattachment.md) 请求进行检索。 
  
可创建以下项目附件：
  
- Item
    
- 邮件
    
- CalendarItem
    
- 联系人
    
- 任务
    
- MeetingMessage
    
- MeetingRequest
    
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="example"></a>示例

以下示例演示如何创建项目并将其附加到应用商店中的另一Exchange项。
  
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

