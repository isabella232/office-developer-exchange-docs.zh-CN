---
title: UpdateItem 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4
description: UpdateItem 操作用于修改项目存储中现有Exchange属性。
ms.openlocfilehash: 6ac09c24c13efff8053fc605ec2c0e6cf2957429
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514058"
---
# <a name="updateitem-operation"></a>UpdateItem 操作

**UpdateItem** 操作用于修改项目存储中现有Exchange的属性。 
  
## <a name="remarks"></a>注解

您可以对项目执行三个基本更新操作。 下表列出了可以执行的操作。
  
|**操作**|**说明**|
|:-----|:-----|
|Append  <br/> |向现有属性添加数据。 此操作将保留当前数据。 Append 并不适用于所有属性。  <br/> |
|Set  <br/> |如果属性包含数据，则替换该属性的数据，或者创建该属性并设置其值（如果该属性不存在）。 set 操作仅适用于可写属性。  <br/> |
|删除  <br/> |从项目中删除属性。 这与将属性设置为空值不同。 完成此操作后，该项目不存在该属性。 Delete 仅适用于可写属性。  <br/> |
   
**UpdateItem** 调用可用于修改一个或多个项目，以及每个项目的一个或多个属性。 [ItemChanges](itemchanges.md)元素包含要作为此调用的一部分执行的所有修改。 [ItemChange](itemchange.md)元素是[ItemChanges](itemchanges.md)元素的子元素，表示对单个项目执行的修改。 [ItemChange](itemchange.md)元素包含一组可在单个项目上执行的更新操作。 这些更改包含在 Updates ([Item) ](updates-item.md) 元素中。 [ItemId](itemid.md)元素标识要更新的项。 若要更新项目上的多个属性，必须为需要更新的每个属性提供[SetItemField、AppendToItemField](setitemfield.md)或[DeleteItemField。](deleteitemfield.md) [](appendtoitemfield.md) 
  
> [!NOTE]
> 更新操作将按指定的顺序应用。 
  
对于每个更改，必须指定要更改的属性的路径以及具有新值的项的表示形式。 删除操作略有不同，因为只需要应删除的属性的路径。 对于 set 和 append 操作，指定的路径必须引用在项目表示形式中设置的同一属性。 如果这些不同，将返回错误。
  
**UpdateItem** 操作 [可以设置存储](start.md)[项目的Exchange](end-ex15websvcsotherref.md)结束时间。 在 **UpdateItem** 请求中， [可以](start.md) 设置开始时间，而无需同时设置 [结束](end-ex15websvcsotherref.md) 时间。 如果开始时间晚于结束 [时间](start.md) ， [这可能会导致错误 ](end-ex15websvcsotherref.md) 。 请注意，客户端应用程序必须在更改"开始时间[](end-ex15websvcsotherref.md)"时调整"[](start.md)结束时间"以保留持续时间。 
  
当单个日历项目更新为定期主日历项目时 [，MeetingTimeZone](meetingtimezone.md) 属性必须由 **UpdateItem** 操作设置才能保留日历项目的原始时区。 
  
## <a name="setitemfield-request-example"></a>SetItemField 请求示例

### <a name="description"></a>Description

下面的 **UpdateItem** 请求示例演示如何设置项目的敏感度属性。 
  
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

已缩短项目标识符和更改键以保持可读性。
  
### <a name="setitemfield-request-elements"></a>SetItemField 请求元素

请求中会使用下列元素：
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [Updates (Item)](updates-item.md)
    
- [SetItemField](setitemfield.md)
    
- [FieldURI](fielduri.md)
    
- [消息](message-ex15websvcsotherref.md)
    
- [Sensitivity](sensitivity.md)
    
## <a name="appendtoitemfield-request-example"></a>AppendToItemField 请求示例

### <a name="description"></a>Description

下面的 **UpdateItem** 请求示例演示如何将文本追加到项目的 body 属性。 
  
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
  
- **message：ReplyTo**
    
- **item：Body**
    
- 所有收件人和与会者集合属性
    
已缩短项目标识符和更改键以保持可读性。
  
### <a name="appendtoitemfield-request-elements"></a>AppendToItemField 请求元素

请求中会使用下列元素：
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [Updates (Item)](updates-item.md)
    
- [AppendToItemField](appendtoitemfield.md)
    
- [FieldURI](fielduri.md)
    
- [消息](message-ex15websvcsotherref.md)
    
- [正文](body.md)
    
## <a name="deleteitemfield-request-example"></a>DeleteItemField 请求示例

### <a name="description"></a>Description

下面的 **UpdateItem** 请求示例演示如何删除项目上的属性。 
  
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

已缩短项目标识符和更改键以保持可读性。
  
### <a name="deleteitemfield-request-elements"></a>DeleteItemField 请求元素

请求中会使用下列元素：
  
- [UpdateItem](updateitem.md)
    
- [ItemChanges](itemchanges.md)
    
- [ItemChange](itemchange.md)
    
- [ItemId](itemid.md)
    
- [Updates (Item)](updates-item.md)
    
- [DeleteItemField](deleteitemfield.md)
    
- [FieldURI](fielduri.md)
    
## <a name="successful-response-example"></a>成功的响应示例

### <a name="description"></a>Description

以下示例显示了对 **UpdateItem** 请求的成功响应。 
  
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

已缩短项目标识符和更改键以保持可读性。
  
### <a name="successful-response-elements"></a>成功的响应元素

响应中会使用下列元素：
  
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

