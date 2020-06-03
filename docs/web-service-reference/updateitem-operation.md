---
title: UpdateItem 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4
description: UpdateItem 操作用于修改 Exchange 存储中现有项的属性。
ms.openlocfilehash: c001b7656862144023e9704cb04e6b4c0030f9df
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459389"
---
# <a name="updateitem-operation"></a>UpdateItem 操作

**UpdateItem**操作用于修改 Exchange 存储中现有项的属性。 
  
## <a name="remarks"></a>备注

您可以对项目执行三个基本的更新操作。 下表列出了您可以执行的操作。
  
|**操作**|**说明**|
|:-----|:-----|
|Append  <br/> |将数据添加到现有属性。 此操作将保留当前数据。 Append 不应用于所有属性。  <br/> |
|Set  <br/> |如果属性包含数据，则替换属性的数据; 或者，如果属性不存在，则创建属性并设置其值。 Set 操作仅适用于可写属性。  <br/> |
|Delete  <br/> |从项目中删除属性。 这与将属性设置为空值不同。 完成此操作后，该项目的属性不存在。 删除仅适用于可写属性。  <br/> |
   
**UpdateItem**调用可用于修改一个或多个项目，以及每个项目上的一个或多个属性。 [ItemChanges](itemchanges.md)元素包含要作为此调用的一部分执行的所有修改。 [ItemChange](itemchange.md)元素（ [ItemChanges](itemchanges.md)元素的子元素）表示要对单个项目执行的修改。 [ItemChange](itemchange.md)元素包含一组可对单个项目执行的更新操作。 这些更改包含在[Updates （Item）](updates-item.md)元素中。 [ItemId](itemid.md)元素标识要更新的项。 若要更新一个项的多个属性，必须为需要更新的每个属性提供[SetItemField](setitemfield.md)、 [AppendToItemField](appendtoitemfield.md)或[DeleteItemField](deleteitemfield.md) 。 
  
> [!NOTE]
> 将按指定的顺序应用更新操作。 
  
对于每个更改，您必须指定要更改的属性的路径以及该项目的表示形式的新值。 删除操作略有不同，只有应删除的属性的路径是必需的。 对于 set 和 append 操作，指定的路径必须引用在项目表示形式中设置的同一属性。 如果这些不同，将返回错误。
  
**UpdateItem**操作可以设置 Exchange 存储项的[开始](start.md)和[结束](end-ex15websvcsotherref.md)时间。 在**UpdateItem**请求中，可以设置[开始](start.md)时间，而不同时设置[结束](end-ex15websvcsotherref.md)时间。 如果[开始](start.md)时间晚于[结束](end-ex15websvcsotherref.md)时间，这可能会导致错误。 请注意，客户端应用程序必须调整[开始](start.md)时间更改的[结束](end-ex15websvcsotherref.md)时间，以便保留持续时间。 
  
如果将单个日历项目更新为定期主日历项目，则必须通过**UpdateItem**操作设置[MeetingTimeZone](meetingtimezone.md)属性，以便保留日历项目的原始时区。 
  
## <a name="setitemfield-request-example"></a>SetItemField 请求示例

### <a name="description"></a>Description

以下示例的**UpdateItem**请求显示如何设置项目的敏感度属性。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkb..." ChangeKey="CQAAABYAAAB..."/>
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Sensitivity"/>
              <t:Message>
                <t:Sensitivity>Normal</t:Sensitivity>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

项目标识符和更改密钥已缩短，以保持可读性。
  
### <a name="setitemfield-request-elements"></a>SetItemField 请求元素

请求中使用以下元素：
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [更新（项目）](updates-item.md)
    
- [SetItemField](setitemfield.md)
    
- [FieldURI](fielduri.md)
    
- [消息](message-ex15websvcsotherref.md)
    
- [Sensitivity](sensitivity.md)
    
## <a name="appendtoitemfield-request-example"></a>AppendToItemField 请求示例

### <a name="description"></a>Description

以下示例的**UpdateItem**请求显示如何将文本追加到项的 body 属性。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkbW..." ChangeKey="CQAAABYA..."/>
          <t:Updates>
            <t:AppendToItemField>
              <t:FieldURI FieldURI="item:Body"/>
              <t:Message>
                <t:Body BodyType="Text">Some additional text to append</t:Body>
              </t:Message>
            </t:AppendToItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

以下属性支持 append 操作：
  
- **邮件： ReplyTo**
    
- **项目：正文**
    
- 所有收件人和与会者集合属性
    
项目标识符和更改密钥已缩短，以保持可读性。
  
### <a name="appendtoitemfield-request-elements"></a>AppendToItemField 请求元素

请求中使用以下元素：
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [更新（项目）](updates-item.md)
    
- [AppendToItemField](appendtoitemfield.md)
    
- [FieldURI](fielduri.md)
    
- [消息](message-ex15websvcsotherref.md)
    
- [Body](body.md)
    
## <a name="deleteitemfield-request-example"></a>DeleteItemField 请求示例

### <a name="description"></a>Description

下面的**UpdateItem**请求示例演示如何删除项的属性。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkbWluaXN0cm..." ChangeKey="CQAAABYAA..."/>
          <t:Updates>
            <t:DeleteItemField>
              <t:FieldURI FieldURI="item:Body"/>
            </t:DeleteItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

项目标识符和更改密钥已缩短，以保持可读性。
  
### <a name="deleteitemfield-request-elements"></a>DeleteItemField 请求元素

请求中使用以下元素：
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [更新（项目）](updates-item.md)
    
- [DeleteItemField](deleteitemfield.md)
    
- [FieldURI](fielduri.md)
    
## <a name="successful-response-example"></a>成功的响应示例

### <a name="description"></a>Description

下面的示例演示对**UpdateItem**请求的成功响应。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
  xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="664" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <UpdateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="AAAtAEFkbW..." ChangeKey="CQAAABYAAA..."/>
            </t:Message>
          </m:Items>
        </m:UpdateItemResponseMessage>
      </m:ResponseMessages>
    </UpdateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

项目标识符和更改密钥已缩短，以保持可读性。
  
### <a name="successful-response-elements"></a>成功的响应元素

响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateItemResponse](updateitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UpdateItemResponseMessage](updateitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Items](items.md)
    
- [消息](message-ex15websvcsotherref.md)
    
- [ItemId](itemid.md)
    
## <a name="see-also"></a>另请参阅



[UpdateItem 操作（任务）](updateitem-operation-task.md)
  
[UpdateItem 操作（联系人）](updateitem-operation-contact.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)


[更新联系人](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[更新任务](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

