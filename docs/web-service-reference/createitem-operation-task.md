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
# <a name="createitem-operation-task"></a><span data-ttu-id="1d642-103">CreateItem operation，（任务）</span><span class="sxs-lookup"><span data-stu-id="1d642-103">CreateItem operation (task)</span></span>

<span data-ttu-id="1d642-104">CreateItem operation，在 Exchange 存储中创建任务项目。</span><span class="sxs-lookup"><span data-stu-id="1d642-104">The CreateItem operation creates task items in the Exchange store.</span></span>
  
## <a name="task-createitem-request"></a><span data-ttu-id="1d642-105">任务 CreateItem 请求</span><span class="sxs-lookup"><span data-stu-id="1d642-105">Task CreateItem Request</span></span>

### <a name="description"></a><span data-ttu-id="1d642-106">说明</span><span class="sxs-lookup"><span data-stu-id="1d642-106">Description</span></span>

<span data-ttu-id="1d642-107">CreateItem 请求的下面的示例演示如何在邮箱中创建任务项目。</span><span class="sxs-lookup"><span data-stu-id="1d642-107">The following example of a CreateItem request shows how to create a task item in a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="1d642-108">代码</span><span class="sxs-lookup"><span data-stu-id="1d642-108">Code</span></span>

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

### <a name="comments"></a><span data-ttu-id="1d642-109">注释</span><span class="sxs-lookup"><span data-stu-id="1d642-109">Comments</span></span>

<span data-ttu-id="1d642-110">当他们都会收到的正在运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器角色的计算机，则会改动定期任务的请求。</span><span class="sxs-lookup"><span data-stu-id="1d642-110">Requests for recurring tasks are altered when they are received by the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span> <span data-ttu-id="1d642-111">发生了以下更改：</span><span class="sxs-lookup"><span data-stu-id="1d642-111">The following changes occur:</span></span>
  
- <span data-ttu-id="1d642-112">该日期仅保存定期任务的范围的[起始日期 （重复）](startdate-recurrence.md)属性。</span><span class="sxs-lookup"><span data-stu-id="1d642-112">Only the date is saved for the [StartDate (Recurrence)](startdate-recurrence.md) property of the recurrence range of the task.</span></span> <span data-ttu-id="1d642-113">时间部分将被截断。</span><span class="sxs-lookup"><span data-stu-id="1d642-113">The time part is truncated.</span></span> 
    
- <span data-ttu-id="1d642-114">[StartDate （重复）](startdate-recurrence.md)属性可能会调整，具体取决于定期模式。</span><span class="sxs-lookup"><span data-stu-id="1d642-114">The [StartDate (Recurrence)](startdate-recurrence.md) property may be adjusted, depending on the recurrence pattern.</span></span> <span data-ttu-id="1d642-115">例如，如果定期模式指定为每个星期一和起始日期设置为 2006 年 10 月 26 日，即星期四调整 StartDate 为 2006 年 10 月 30 日，这是下星期一。</span><span class="sxs-lookup"><span data-stu-id="1d642-115">For example, if the recurrence pattern is specified as every Monday and the StartDate is set to October 26, 2006, which is a Thursday, StartDate is adjusted to October 30, 2006, which is the next Monday.</span></span> 
    
- <span data-ttu-id="1d642-116">如果设置任务的[StartDate](startdate.md)属性，它将更新以匹配定期范围的[起始日期 （重复）](startdate-recurrence.md) 。</span><span class="sxs-lookup"><span data-stu-id="1d642-116">If the [StartDate](startdate.md) property of the task is set, it is updated to match the [StartDate (Recurrence)](startdate-recurrence.md) of the recurrence range.</span></span> <span data-ttu-id="1d642-117">任务的[DueDate](duedate.md)属性也会更新基于新[StartDate](startdate.md)。</span><span class="sxs-lookup"><span data-stu-id="1d642-117">The [DueDate](duedate.md) property of the task is also updated based on the new [StartDate](startdate.md).</span></span>
    
- <span data-ttu-id="1d642-118">如果未设置[StartDate](startdate.md) ，仅将[DueDate](duedate.md)属性将更新以匹配定期范围的[起始日期 （重复）](startdate-recurrence.md) 。</span><span class="sxs-lookup"><span data-stu-id="1d642-118">If the [StartDate](startdate.md) is not set, only the [DueDate](duedate.md) property is updated to match the [StartDate (Recurrence)](startdate-recurrence.md) of the recurrence range.</span></span> 
    
<span data-ttu-id="1d642-119">下表显示了客户端访问服务器向每个星期一 Task.Recurrence.Pattern 定期任务的更改。</span><span class="sxs-lookup"><span data-stu-id="1d642-119">The following table shows the changes that the Client Access server makes to a recurring task that has a Task.Recurrence.Pattern of every Monday.</span></span>
  
<span data-ttu-id="1d642-120">**对定期任务更改**</span><span class="sxs-lookup"><span data-stu-id="1d642-120">**Changes to a recurring task**</span></span>

|<span data-ttu-id="1d642-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="1d642-121">**Property**</span></span>|<span data-ttu-id="1d642-122">**原始值**</span><span class="sxs-lookup"><span data-stu-id="1d642-122">**Original Value**</span></span>|<span data-ttu-id="1d642-123">**更新后的值**</span><span class="sxs-lookup"><span data-stu-id="1d642-123">**Updated Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1d642-124">Task.StartDate</span><span class="sxs-lookup"><span data-stu-id="1d642-124">Task.StartDate</span></span>  <br/> |<span data-ttu-id="1d642-125">2006 年 1 月 1日日</span><span class="sxs-lookup"><span data-stu-id="1d642-125">January 1, 2006</span></span>  <br/> |<span data-ttu-id="1d642-126">2006 年 10 月 30日日</span><span class="sxs-lookup"><span data-stu-id="1d642-126">October 30, 2006</span></span>  <br/> |
|<span data-ttu-id="1d642-127">Task.DueDate</span><span class="sxs-lookup"><span data-stu-id="1d642-127">Task.DueDate</span></span>  <br/> |<span data-ttu-id="1d642-128">2006 年 1 月 3日日</span><span class="sxs-lookup"><span data-stu-id="1d642-128">January 3, 2006</span></span>  <br/> |<span data-ttu-id="1d642-129">2006 年 11 月 1日日</span><span class="sxs-lookup"><span data-stu-id="1d642-129">November 1, 2006</span></span>  <br/> |
|<span data-ttu-id="1d642-130">Task.Recurrence.Range.StartDate</span><span class="sxs-lookup"><span data-stu-id="1d642-130">Task.Recurrence.Range.StartDate</span></span>  <br/> |<span data-ttu-id="1d642-131">2006 年 10 月 26日日</span><span class="sxs-lookup"><span data-stu-id="1d642-131">October 26, 2006</span></span>  <br/> |<span data-ttu-id="1d642-132">2006 年 10 月 30日日</span><span class="sxs-lookup"><span data-stu-id="1d642-132">October 30, 2006</span></span>  <br/> |
   
<span data-ttu-id="1d642-133">默认情况下，如果未指定的目标文件夹，任务项目中创建任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="1d642-133">By default, if a destination folder is not specified, task items are created in the Tasks folder.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="1d642-134">请求元素</span><span class="sxs-lookup"><span data-stu-id="1d642-134">Request elements</span></span>

<span data-ttu-id="1d642-135">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="1d642-135">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="1d642-136">CreateItem</span><span class="sxs-lookup"><span data-stu-id="1d642-136">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="1d642-137">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="1d642-137">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="1d642-138">任务</span><span class="sxs-lookup"><span data-stu-id="1d642-138">Task</span></span>](task.md)
    
- [<span data-ttu-id="1d642-139">Subject</span><span class="sxs-lookup"><span data-stu-id="1d642-139">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="1d642-140">DueDate</span><span class="sxs-lookup"><span data-stu-id="1d642-140">DueDate</span></span>](duedate.md)
    
- [<span data-ttu-id="1d642-141">Status</span><span class="sxs-lookup"><span data-stu-id="1d642-141">Status</span></span>](status.md)
    
## <a name="successful-task-createitem-response"></a><span data-ttu-id="1d642-142">成功的任务 CreateItem 响应</span><span class="sxs-lookup"><span data-stu-id="1d642-142">Successful Task CreateItem Response</span></span>

### <a name="description"></a><span data-ttu-id="1d642-143">说明</span><span class="sxs-lookup"><span data-stu-id="1d642-143">Description</span></span>

<span data-ttu-id="1d642-144">下面的示例演示对 CreateItem 请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="1d642-144">The following example shows a successful response to the CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="1d642-145">代码</span><span class="sxs-lookup"><span data-stu-id="1d642-145">Code</span></span>

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

### <a name="successful-response-elements"></a><span data-ttu-id="1d642-146">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="1d642-146">Successful response elements</span></span>

<span data-ttu-id="1d642-147">在响应中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="1d642-147">The following elements are included in the response:</span></span>
  
- [<span data-ttu-id="1d642-148">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="1d642-148">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="1d642-149">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="1d642-149">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="1d642-150">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1d642-150">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="1d642-151">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1d642-151">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="1d642-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1d642-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="1d642-153">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="1d642-153">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="1d642-154">任务</span><span class="sxs-lookup"><span data-stu-id="1d642-154">Task</span></span>](task.md)
    
- [<span data-ttu-id="1d642-155">ItemId</span><span class="sxs-lookup"><span data-stu-id="1d642-155">ItemId</span></span>](itemid.md)
    
## <a name="see-also"></a><span data-ttu-id="1d642-156">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1d642-156">See also</span></span>



[<span data-ttu-id="1d642-157">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="1d642-157">CreateItem operation</span></span>](createitem-operation.md)


[<span data-ttu-id="1d642-158">创建任务</span><span class="sxs-lookup"><span data-stu-id="1d642-158">Creating Tasks</span></span>](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="1d642-159">更新任务</span><span class="sxs-lookup"><span data-stu-id="1d642-159">Updating Tasks</span></span>](http://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)
  
[<span data-ttu-id="1d642-160">删除任务</span><span class="sxs-lookup"><span data-stu-id="1d642-160">Deleting Tasks</span></span>](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

