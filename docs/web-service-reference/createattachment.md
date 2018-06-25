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
description: CreateAttachment 元素定义一个请求在 Exchange 存储中创建项目的附件。
ms.openlocfilehash: d403eb5ca15623d3a973f7b224dbcde5529cf1bc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753625"
---
# <a name="createattachment"></a>CreateAttachment

**CreateAttachment**元素定义一个请求在 Exchange 存储中创建项目的附件。 
  
```xml
<CreateAttachment>
   <ParentItemId/>
   <Attachments/>
</CreateAttachment>
```

 **CreateAttachmentType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ParentItemId](parentitemid.md) <br/> |标识父 Exchange 存储项包含创建的附件。 [ParentItemId](parentitemid.md)元素必须提供的实际 Exchange ID 存储项。 可以通过使用[GetItem 操作](getitem-operation.md); 来检索实际存储项目通过使用[GetAttachment 操作](getattachment-operation.md)检索附件。 如果[ParentItemId](parentitemid.md)传递的文件附件 ID，将发生错误。 如果[ParentItemId](parentitemid.md)表示现有项目附件的 ID， [CreateAttachment 操作](createattachment-operation.md)添加到现有的附件的新附件。  <br/> 此元素是[CreateAttachment 操作](createattachment-operation.md)所必需的。  <br/> |
|[附件](attachments-ex15websvcsotherref.md) <br/> |包含的项目或文件附加到 Exchange 存储中的项。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

为存储项不存在项目附件。 仅存在为项目附件或另一个附件。 只能通过使用[GetAttachment](getattachment.md)请求检索项附件。 
  
可以创建以下项附件：
  
- 项目
    
- 邮件
    
- 日历项目
    
- 联系人
    
- 任务
    
- MeetingMessage
    
- MeetingRequest
    
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="example"></a>示例

下面的示例演示如何创建并附加到 Exchange 存储中的另一个项目的项目。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[CreateAttachment 操作](createattachment-operation.md)
  
[DeleteAttachment 操作](deleteattachment-operation.md)
  
[GetAttachment 操作](getattachment-operation.md)

