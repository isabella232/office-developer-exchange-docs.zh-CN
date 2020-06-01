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
# <a name="createitem-operation-task"></a><span data-ttu-id="d6c9d-103">CreateItem 操作（任务）</span><span class="sxs-lookup"><span data-stu-id="d6c9d-103">CreateItem operation (task)</span></span>

<span data-ttu-id="d6c9d-104">CreateItem 操作在 Exchange 存储中创建任务项。</span><span class="sxs-lookup"><span data-stu-id="d6c9d-104">The CreateItem operation creates task items in the Exchange store.</span></span>
  
## <a name="task-createitem-request"></a><span data-ttu-id="d6c9d-105">任务 CreateItem 请求</span><span class="sxs-lookup"><span data-stu-id="d6c9d-105">Task CreateItem Request</span></span>

### <a name="description"></a><span data-ttu-id="d6c9d-106">说明</span><span class="sxs-lookup"><span data-stu-id="d6c9d-106">Description</span></span>

<span data-ttu-id="d6c9d-107">下面的 CreateItem 请求示例演示如何在邮箱中创建任务项。</span><span class="sxs-lookup"><span data-stu-id="d6c9d-107">The following example of a CreateItem request shows how to create a task item in a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="d6c9d-108">代码</span><span class="sxs-lookup"><span data-stu-id="d6c9d-108">Code</span></span>

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

### <a name="comments"></a><span data-ttu-id="d6c9d-109">备注</span><span class="sxs-lookup"><span data-stu-id="d6c9d-109">Comments</span></span>

<span data-ttu-id="d6c9d-110">如果运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色的计算机收到定期任务的请求，则会更改这些请求。</span><span class="sxs-lookup"><span data-stu-id="d6c9d-110">Requests for recurring tasks are altered when they are received by the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span> <span data-ttu-id="d6c9d-111">将发生以下更改：</span><span class="sxs-lookup"><span data-stu-id="d6c9d-111">The following changes occur:</span></span>
  
- <span data-ttu-id="d6c9d-112">仅为任务的定期日期范围的开始日期[（定期）](startdate-recurrence.md)属性保存日期。</span><span class="sxs-lookup"><span data-stu-id="d6c9d-112">Only the date is saved for the [StartDate (Recurrence)](startdate-recurrence.md) property of the recurrence range of the task.</span></span> <span data-ttu-id="d6c9d-113">时间部分将被截断。</span><span class="sxs-lookup"><span data-stu-id="d6c9d-113">The time part is truncated.</span></span> 
    
- <span data-ttu-id="d6c9d-114">"开始[日期" （定期）](startdate-recurrence.md)属性可能会根据定期模式进行调整。</span><span class="sxs-lookup"><span data-stu-id="d6c9d-114">The [StartDate (Recurrence)](startdate-recurrence.md) property may be adjusted, depending on the recurrence pattern.</span></span> <span data-ttu-id="d6c9d-115">例如，如果定期模式被指定为每周一次，并且起始日期设置为10月26日2006，即星期四，则开始日期将调整为10月 30 2006 日，即下个星期一。</span><span class="sxs-lookup"><span data-stu-id="d6c9d-115">For example, if the recurrence pattern is specified as every Monday and the StartDate is set to October 26, 2006, which is a Thursday, StartDate is adjusted to October 30, 2006, which is the next Monday.</span></span> 
    
- <span data-ttu-id="d6c9d-116">如果设置了任务的 "开始[日期](startdate.md)" 属性，则会进行更新，以匹配定期范围的开始[日期（定期）](startdate-recurrence.md) 。</span><span class="sxs-lookup"><span data-stu-id="d6c9d-116">If the [StartDate](startdate.md) property of the task is set, it is updated to match the [StartDate (Recurrence)](startdate-recurrence.md) of the recurrence range.</span></span> <span data-ttu-id="d6c9d-117">此外，还将根据新的[起始日期](startdate.md)更新任务的[DueDate](duedate.md)属性。</span><span class="sxs-lookup"><span data-stu-id="d6c9d-117">The [DueDate](duedate.md) property of the task is also updated based on the new [StartDate](startdate.md).</span></span>
    
- <span data-ttu-id="d6c9d-118">如果未设置[起始日期](startdate.md)，则仅更新[DueDate](duedate.md)属性以匹配定期范围的开始[日期（定期）](startdate-recurrence.md) 。</span><span class="sxs-lookup"><span data-stu-id="d6c9d-118">If the [StartDate](startdate.md) is not set, only the [DueDate](duedate.md) property is updated to match the [StartDate (Recurrence)](startdate-recurrence.md) of the recurrence range.</span></span> 
    
<span data-ttu-id="d6c9d-119">下表显示了客户端访问服务器对具有任务的定期任务进行的更改。每个星期一的模式。</span><span class="sxs-lookup"><span data-stu-id="d6c9d-119">The following table shows the changes that the Client Access server makes to a recurring task that has a Task.Recurrence.Pattern of every Monday.</span></span>
  
<span data-ttu-id="d6c9d-120">**对定期任务的更改**</span><span class="sxs-lookup"><span data-stu-id="d6c9d-120">**Changes to a recurring task**</span></span>

|<span data-ttu-id="d6c9d-121">**Property**</span><span class="sxs-lookup"><span data-stu-id="d6c9d-121">**Property**</span></span>|<span data-ttu-id="d6c9d-122">**原始值**</span><span class="sxs-lookup"><span data-stu-id="d6c9d-122">**Original Value**</span></span>|<span data-ttu-id="d6c9d-123">**更新值**</span><span class="sxs-lookup"><span data-stu-id="d6c9d-123">**Updated Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d6c9d-124">任务. 起始日期</span><span class="sxs-lookup"><span data-stu-id="d6c9d-124">Task.StartDate</span></span>  <br/> |<span data-ttu-id="d6c9d-125">2006年1月1日</span><span class="sxs-lookup"><span data-stu-id="d6c9d-125">January 1, 2006</span></span>  <br/> |<span data-ttu-id="d6c9d-126">2006年10月30日</span><span class="sxs-lookup"><span data-stu-id="d6c9d-126">October 30, 2006</span></span>  <br/> |
|<span data-ttu-id="d6c9d-127">DueDate</span><span class="sxs-lookup"><span data-stu-id="d6c9d-127">Task.DueDate</span></span>  <br/> |<span data-ttu-id="d6c9d-128">2006年1月3日</span><span class="sxs-lookup"><span data-stu-id="d6c9d-128">January 3, 2006</span></span>  <br/> |<span data-ttu-id="d6c9d-129">2006年11月1日</span><span class="sxs-lookup"><span data-stu-id="d6c9d-129">November 1, 2006</span></span>  <br/> |
|<span data-ttu-id="d6c9d-130">定期开始日期范围. 开始日期</span><span class="sxs-lookup"><span data-stu-id="d6c9d-130">Task.Recurrence.Range.StartDate</span></span>  <br/> |<span data-ttu-id="d6c9d-131">2006年10月26日</span><span class="sxs-lookup"><span data-stu-id="d6c9d-131">October 26, 2006</span></span>  <br/> |<span data-ttu-id="d6c9d-132">2006年10月30日</span><span class="sxs-lookup"><span data-stu-id="d6c9d-132">October 30, 2006</span></span>  <br/> |
   
<span data-ttu-id="d6c9d-133">默认情况下，如果未指定目标文件夹，则会在 "任务" 文件夹中创建任务项目。</span><span class="sxs-lookup"><span data-stu-id="d6c9d-133">By default, if a destination folder is not specified, task items are created in the Tasks folder.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="d6c9d-134">Request 元素</span><span class="sxs-lookup"><span data-stu-id="d6c9d-134">Request elements</span></span>

<span data-ttu-id="d6c9d-135">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="d6c9d-135">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="d6c9d-136">CreateItem</span><span class="sxs-lookup"><span data-stu-id="d6c9d-136">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="d6c9d-137">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="d6c9d-137">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="d6c9d-138">Task</span><span class="sxs-lookup"><span data-stu-id="d6c9d-138">Task</span></span>](task.md)
    
- [<span data-ttu-id="d6c9d-139">主题</span><span class="sxs-lookup"><span data-stu-id="d6c9d-139">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="d6c9d-140">DueDate</span><span class="sxs-lookup"><span data-stu-id="d6c9d-140">DueDate</span></span>](duedate.md)
    
- [<span data-ttu-id="d6c9d-141">Status</span><span class="sxs-lookup"><span data-stu-id="d6c9d-141">Status</span></span>](status.md)
    
## <a name="successful-task-createitem-response"></a><span data-ttu-id="d6c9d-142">成功的任务 CreateItem 响应</span><span class="sxs-lookup"><span data-stu-id="d6c9d-142">Successful Task CreateItem Response</span></span>

### <a name="description"></a><span data-ttu-id="d6c9d-143">说明</span><span class="sxs-lookup"><span data-stu-id="d6c9d-143">Description</span></span>

<span data-ttu-id="d6c9d-144">下面的示例演示对 CreateItem 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="d6c9d-144">The following example shows a successful response to the CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="d6c9d-145">代码</span><span class="sxs-lookup"><span data-stu-id="d6c9d-145">Code</span></span>

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

### <a name="successful-response-elements"></a><span data-ttu-id="d6c9d-146">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="d6c9d-146">Successful response elements</span></span>

<span data-ttu-id="d6c9d-147">响应中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="d6c9d-147">The following elements are included in the response:</span></span>
  
- [<span data-ttu-id="d6c9d-148">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d6c9d-148">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="d6c9d-149">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="d6c9d-149">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="d6c9d-150">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d6c9d-150">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d6c9d-151">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d6c9d-151">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="d6c9d-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d6c9d-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d6c9d-153">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="d6c9d-153">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="d6c9d-154">Task</span><span class="sxs-lookup"><span data-stu-id="d6c9d-154">Task</span></span>](task.md)
    
- [<span data-ttu-id="d6c9d-155">ItemId</span><span class="sxs-lookup"><span data-stu-id="d6c9d-155">ItemId</span></span>](itemid.md)
    
## <a name="see-also"></a><span data-ttu-id="d6c9d-156">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d6c9d-156">See also</span></span>



[<span data-ttu-id="d6c9d-157">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="d6c9d-157">CreateItem operation</span></span>](createitem-operation.md)


[<span data-ttu-id="d6c9d-158">创建任务</span><span class="sxs-lookup"><span data-stu-id="d6c9d-158">Creating Tasks</span></span>](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="d6c9d-159">更新任务</span><span class="sxs-lookup"><span data-stu-id="d6c9d-159">Updating Tasks</span></span>](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)
  
[<span data-ttu-id="d6c9d-160">删除任务</span><span class="sxs-lookup"><span data-stu-id="d6c9d-160">Deleting Tasks</span></span>](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

