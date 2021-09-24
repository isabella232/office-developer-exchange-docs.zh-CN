---
title: CreateItem 操作（任务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CreateItem
api_type:
- schema
ms.assetid: 12c5da4d-290c-4a8a-a965-0bf5d55c7978
description: CreateItem 操作在任务存储区中Exchange项。
ms.openlocfilehash: 814a32e82cd5c1c95be252d1b53387741898dd40
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510253"
---
# <a name="createitem-operation-task"></a>CreateItem 操作（任务）

CreateItem 操作在任务存储区中Exchange项。
  
## <a name="task-createitem-request"></a>任务 CreateItem 请求

### <a name="description"></a>Description

下面的 CreateItem 请求示例演示如何在邮箱中创建任务项目。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                MessageDisposition="SaveOnly">
      <Items>
        <t:Task>
          <t:Subject>My task</t:Subject>
          <t:DueDate>2006-10-26T21:32:52</t:DueDate>
          <t:Status>NotStarted</t:Status>
        </t:Task>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

当运行 2007 年 Microsoft Exchange Server服务器角色的计算机收到定期任务请求时，会更改这些请求。 将发生以下更改：
  
- 仅保存任务的定期范围的 [StartDate (Recurrence) ](startdate-recurrence.md) 属性的日期。 将截断时间部分。 
    
- [StartDate (Recurrence) ](startdate-recurrence.md)属性可能会进行调整，具体取决于定期模式。 例如，如果将 定期模式 指定为每周一，并且 StartDate 设置为 2006 年 10 月 26 日（星期四）则 StartDate 将调整为 2006 年 10 月 30 日（即下一个星期一）。 
    
- 如果 [设置任务的 StartDate](startdate.md) 属性，则更新该属性以匹配定期 ([定期) 的 StartDate ](startdate-recurrence.md) 属性。 任务的 [DueDate](duedate.md) 属性也会基于新的 [StartDate 进行更新](startdate.md)。
    
- 如果未 [设置 StartDate，](startdate.md) 则仅更新 [DueDate](duedate.md) 属性以匹配定期范围的 [StartDate ](startdate-recurrence.md) (Recurrence) 。 
    
下表显示客户端访问服务器对每周一具有 Task.Recurrence.Pattern 的定期任务所做的更改。
  
**对定期任务所做的更改**

|**Property**|**原始值**|**更新的值**|
|:-----|:-----|:-----|
|Task.StartDate  <br/> |2006 年 1 月 1 日  <br/> |2006 年 10 月 30 日  <br/> |
|Task.DueDate  <br/> |2006 年 1 月 3 日  <br/> |2006 年 11 月 1 日  <br/> |
|Task.Recurrence.Range.StartDate  <br/> |2006 年 10 月 26 日  <br/> |2006 年 10 月 30 日  <br/> |
   
默认情况下，如果未指定目标文件夹，任务项目是在任务文件夹中创建的。
  
### <a name="request-elements"></a>请求元素

请求中会使用下列元素：
  
- [CreateItem](createitem.md)
    
- [Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)
    
- [任务](task.md)
    
- [主题](subject.md)
    
- [DueDate](duedate.md)
    
- [状态](status.md)
    
## <a name="successful-task-createitem-response"></a>成功任务 CreateItem 响应

### <a name="description"></a>Description

以下示例显示了对 CreateItem 请求的成功响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Task>
              <t:ItemId Id="AAAtAE=" ChangeKey="EwAAABYA"/>
            </t:Task>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>成功的响应元素

响应中包含以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateItemResponse](createitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateItemResponseMessage](createitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)
    
- [任务](task.md)
    
- [ItemId](itemid.md)
    
## <a name="see-also"></a>另请参阅



[CreateItem 操作](createitem-operation.md)


[创建任务](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[更新任务](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)
  
[删除任务](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

