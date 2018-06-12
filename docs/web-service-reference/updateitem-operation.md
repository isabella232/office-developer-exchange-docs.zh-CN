---
title: UpdateItem Operation
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
description: UpdateItem 操作用于修改 Exchange 存储中现有项目的属性。
ms.openlocfilehash: 009ba16315017c4418fbd71d49744015c4d6d1b1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838401"
---
# <a name="updateitem-operation"></a>UpdateItem Operation

**UpdateItem**操作用于修改 Exchange 存储中现有项目的属性。 
  
## <a name="remarks"></a>备注

您可以在项目上执行三个基本 update 操作。 下表列出了您可以执行的操作。
  
|**操作**|**说明**|
|:-----|:-----|
|追加  <br/> |将数据添加到现有属性。 此操作可保留当前的数据。 追加不适用于所有属性。  <br/> |
|设置  <br/> |如果属性包含数据，或创建属性并设置其值，如果属性不存在，将替换为属性的数据。 设置操作仅适用于可写属性。  <br/> |
|Delete  <br/> |从项目中删除属性。 这与属性设置为空值。 完成此操作后，该属性不存在的项目。 删除才适用于可写属性。  <br/> |
   
**UpdateItem**呼叫可修改一个或多个项目和对每个项目的一个或多个属性。 [ItemChanges](itemchanges.md)元素包含要执行此呼叫的一部分的所有的修改。 [ItemChange](itemchange.md)元素， [ItemChanges](itemchanges.md)元素的子元素均表示单个项目上执行的修改。 [ItemChange](itemchange.md)元素包含一组可对单个项目执行的 update 操作。 [更新 （项）](updates-item.md)元素中包含这些更改。 [ItemId](itemid.md)元素标识要更新的项。 若要更新的项的多个属性， [SetItemField](setitemfield.md)、 [AppendToItemField](appendtoitemfield.md)或[DeleteItemField](deleteitemfield.md)必须提供需要更新的每个属性。 
  
> [!NOTE]
> 指定它们的顺序应用更新操作。 
  
对于每个更改，您必须使用其新的值指定要更改的属性的路径和该项目的表示形式。 删除操作是略有不同的这是的只有属性应删除的路径，则需要。 组和追加操作，指定的路径必须指向同一属性中的项目表示要设置的。 如果这些不同，则将返回错误。
  
**UpdateItem**操作可以设置 Exchange 存储项目的[开始](start.md)和[结束](end-ex15websvcsotherref.md)时间。 在**UpdateItem**请求中，可以没有还设置的[结束](end-ex15websvcsotherref.md)时间设置[开始](start.md)时间。 如果[开始](start.md)时间晚于的[结束](end-ex15websvcsotherref.md)时间，这会导致错误。 注意客户端应用程序必须调整[开始](start.md)时间才能保留持续时间的更改时的[结束](end-ex15websvcsotherref.md)时间。 
  
更新单个日历项目时成为定期主日历项，您必须[MeetingTimeZone](meetingtimezone.md)属性的设置**UpdateItem**操作才能保留的日历项目的原始时区。 
  
## <a name="setitemfield-request-example"></a>SetItemField 请求示例

### <a name="description"></a>说明

**UpdateItem**请求的下面的示例演示如何设置对项目的 sensitivity 属性。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>注释

已缩短的项标识符和更改密钥，以保留可读性。
  
### <a name="setitemfield-request-elements"></a>SetItemField 请求元素

请求中使用以下元素：
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [更新 （项）](updates-item.md)
    
- [SetItemField](setitemfield.md)
    
- [FieldURI](fielduri.md)
    
- [Message](message-ex15websvcsotherref.md)
    
- [Sensitivity](sensitivity.md)
    
## <a name="appendtoitemfield-request-example"></a>AppendToItemField 请求示例

### <a name="description"></a>说明

**UpdateItem**请求的下面的示例演示如何将文本追加到的项的 body 属性。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>注释

以下属性支持 append 操作：
  
- **消息： 回复**
    
- **项目： 正文**
    
- 所有收件人和与会者集合属性
    
已缩短的项标识符和更改密钥，以保留可读性。
  
### <a name="appendtoitemfield-request-elements"></a>AppendToItemField 请求元素

请求中使用以下元素：
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [更新 （项）](updates-item.md)
    
- [AppendToItemField](appendtoitemfield.md)
    
- [FieldURI](fielduri.md)
    
- [Message](message-ex15websvcsotherref.md)
    
- [Body](body.md)
    
## <a name="deleteitemfield-request-example"></a>DeleteItemField 请求示例

### <a name="description"></a>说明

**UpdateItem**请求的下面的示例演示如何删除上一个项目的属性。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>注释

已缩短的项标识符和更改密钥，以保留可读性。
  
### <a name="deleteitemfield-request-elements"></a>DeleteItemField 请求元素

请求中使用以下元素：
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [更新 （项）](updates-item.md)
    
- [DeleteItemField](deleteitemfield.md)
    
- [FieldURI](fielduri.md)
    
## <a name="successful-response-example"></a>成功的响应示例

### <a name="description"></a>说明

下面的示例演示对**UpdateItem**请求成功响应。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
  xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="664" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <UpdateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>注释

已缩短的项标识符和更改密钥，以保留可读性。
  
### <a name="successful-response-elements"></a>成功响应元素

在响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateItemResponse](updateitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UpdateItemResponseMessage](updateitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Items](items.md)
    
- [Message](message-ex15websvcsotherref.md)
    
- [ItemId](itemid.md)
    
## <a name="see-also"></a>另请参阅



[UpdateItem 操作 （任务）](updateitem-operation-task.md)
  
[UpdateItem 操作 （联系人）](updateitem-operation-contact.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)


[更新联系人](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[更新任务](http://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

