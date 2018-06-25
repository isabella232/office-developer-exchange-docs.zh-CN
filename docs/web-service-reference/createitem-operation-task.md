---
title: CreateItem operation，（任务）
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
description: CreateItem operation，在 Exchange 存储中创建任务项目。
ms.openlocfilehash: 5a5203202071ae9391faa9348902424317ee96d1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753664"
---
# <a name="createitem-operation-task"></a>CreateItem operation，（任务）

CreateItem operation，在 Exchange 存储中创建任务项目。
  
## <a name="task-createitem-request"></a>任务 CreateItem 请求

### <a name="description"></a>说明

CreateItem 请求的下面的示例演示如何在邮箱中创建任务项目。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
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

### <a name="comments"></a>注释

当他们都会收到的正在运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器角色的计算机，则会改动定期任务的请求。 发生了以下更改：
  
- 该日期仅保存定期任务的范围的[起始日期 （重复）](startdate-recurrence.md)属性。 时间部分将被截断。 
    
- [StartDate （重复）](startdate-recurrence.md)属性可能会调整，具体取决于定期模式。 例如，如果定期模式指定为每个星期一和起始日期设置为 2006 年 10 月 26 日，即星期四调整 StartDate 为 2006 年 10 月 30 日，这是下星期一。 
    
- 如果设置任务的[StartDate](startdate.md)属性，它将更新以匹配定期范围的[起始日期 （重复）](startdate-recurrence.md) 。 任务的[DueDate](duedate.md)属性也会更新基于新[StartDate](startdate.md)。
    
- 如果未设置[StartDate](startdate.md) ，仅将[DueDate](duedate.md)属性将更新以匹配定期范围的[起始日期 （重复）](startdate-recurrence.md) 。 
    
下表显示了客户端访问服务器向每个星期一 Task.Recurrence.Pattern 定期任务的更改。
  
**对定期任务更改**

|**属性**|**原始值**|**更新后的值**|
|:-----|:-----|:-----|
|Task.StartDate  <br/> |2006 年 1 月 1日日  <br/> |2006 年 10 月 30日日  <br/> |
|Task.DueDate  <br/> |2006 年 1 月 3日日  <br/> |2006 年 11 月 1日日  <br/> |
|Task.Recurrence.Range.StartDate  <br/> |2006 年 10 月 26日日  <br/> |2006 年 10 月 30日日  <br/> |
   
默认情况下，如果未指定的目标文件夹，任务项目中创建任务文件夹。
  
### <a name="request-elements"></a>请求元素

请求中使用以下元素：
  
- [CreateItem](createitem.md)
    
- [项目 (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)
    
- [任务](task.md)
    
- [Subject](subject.md)
    
- [DueDate](duedate.md)
    
- [Status](status.md)
    
## <a name="successful-task-createitem-response"></a>成功的任务 CreateItem 响应

### <a name="description"></a>说明

下面的示例演示对 CreateItem 请求成功响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a>成功响应元素

在响应中包含以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateItemResponse](createitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateItemResponseMessage](createitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [项目 (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)
    
- [任务](task.md)
    
- [ItemId](itemid.md)
    
## <a name="see-also"></a>另请参阅



[CreateItem 操作](createitem-operation.md)


[创建任务](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[更新任务](http://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)
  
[删除任务](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

