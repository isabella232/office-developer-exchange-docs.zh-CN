---
title: CreateItem 操作（任务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: 12c5da4d-290c-4a8a-a965-0bf5d55c7978
description: CreateItem 操作在 Exchange 存储中创建任务项。
ms.openlocfilehash: 502108843193e7ed8377b0fade9e106ef3d1976c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457100"
---
# <a name="createitem-operation-task"></a>CreateItem 操作（任务）

CreateItem 操作在 Exchange 存储中创建任务项。
  
## <a name="task-createitem-request"></a>任务 CreateItem 请求

### <a name="description"></a>说明

下面的 CreateItem 请求示例演示如何在邮箱中创建任务项。
  
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

如果运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色的计算机收到定期任务的请求，则会更改这些请求。 将发生以下更改：
  
- 仅为任务的定期日期范围的开始日期[（定期）](startdate-recurrence.md)属性保存日期。 时间部分将被截断。 
    
- "开始[日期" （定期）](startdate-recurrence.md)属性可能会根据定期模式进行调整。 例如，如果定期模式被指定为每周一次，并且起始日期设置为10月26日2006，即星期四，则开始日期将调整为10月 30 2006 日，即下个星期一。 
    
- 如果设置了任务的 "开始[日期](startdate.md)" 属性，则会进行更新，以匹配定期范围的开始[日期（定期）](startdate-recurrence.md) 。 此外，还将根据新的[起始日期](startdate.md)更新任务的[DueDate](duedate.md)属性。
    
- 如果未设置[起始日期](startdate.md)，则仅更新[DueDate](duedate.md)属性以匹配定期范围的开始[日期（定期）](startdate-recurrence.md) 。 
    
下表显示了客户端访问服务器对具有任务的定期任务进行的更改。每个星期一的模式。
  
**对定期任务的更改**

|**Property**|**原始值**|**更新值**|
|:-----|:-----|:-----|
|任务. 起始日期  <br/> |2006年1月1日  <br/> |2006年10月30日  <br/> |
|DueDate  <br/> |2006年1月3日  <br/> |2006年11月1日  <br/> |
|定期开始日期范围. 开始日期  <br/> |2006年10月26日  <br/> |2006年10月30日  <br/> |
   
默认情况下，如果未指定目标文件夹，则会在 "任务" 文件夹中创建任务项目。
  
### <a name="request-elements"></a>Request 元素

请求中使用以下元素：
  
- [CreateItem](createitem.md)
    
- [项目（NonEmptyArrayOfAllItemsType）](items-nonemptyarrayofallitemstype.md)
    
- [Task](task.md)
    
- [主题](subject.md)
    
- [DueDate](duedate.md)
    
- [Status](status.md)
    
## <a name="successful-task-createitem-response"></a>成功的任务 CreateItem 响应

### <a name="description"></a>说明

下面的示例演示对 CreateItem 请求的成功响应。
  
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
    
- [项目（NonEmptyArrayOfAllItemsType）](items-nonemptyarrayofallitemstype.md)
    
- [Task](task.md)
    
- [ItemId](itemid.md)
    
## <a name="see-also"></a>另请参阅



[CreateItem 操作](createitem-operation.md)


[创建任务](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[更新任务](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)
  
[删除任务](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

