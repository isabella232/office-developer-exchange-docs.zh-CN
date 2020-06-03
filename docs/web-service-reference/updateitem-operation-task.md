---
title: UpdateItem 操作（任务）
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
ms.assetid: b0a7f114-d040-40eb-a8f3-05ea6489e472
description: UpdateItem 操作用于更新 Exchange 存储中的任务项属性。
ms.openlocfilehash: 0041af114d11fd9577037dd154e40b84e8483c35
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459803"
---
# <a name="updateitem-operation-task"></a><span data-ttu-id="240b2-103">UpdateItem 操作（任务）</span><span class="sxs-lookup"><span data-stu-id="240b2-103">UpdateItem operation (task)</span></span>

<span data-ttu-id="240b2-104">UpdateItem 操作用于更新 Exchange 存储中的任务项属性。</span><span class="sxs-lookup"><span data-stu-id="240b2-104">The UpdateItem operation is used to update task item properties in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="240b2-105">备注</span><span class="sxs-lookup"><span data-stu-id="240b2-105">Remarks</span></span>

<span data-ttu-id="240b2-106">不能使用 Exchange Web 服务发送任务请求。</span><span class="sxs-lookup"><span data-stu-id="240b2-106">You cannot use Exchange Web Services to send task requests.</span></span> <span data-ttu-id="240b2-107">Exchange Web 服务可以返回由 MicrosoftOfficeOutlook 创建的任务请求。</span><span class="sxs-lookup"><span data-stu-id="240b2-107">Exchange Web Services can return task requests that are created by MicrosoftOfficeOutlook.</span></span> <span data-ttu-id="240b2-108">如果已发送任务请求，则更新该任务的请求将返回错误。</span><span class="sxs-lookup"><span data-stu-id="240b2-108">If a task request has already been sent, a request to update the task will return an error.</span></span>
  
## <a name="updating-the-current-occurrence-of-a-recurring-task"></a><span data-ttu-id="240b2-109">更新定期任务的当前事件</span><span class="sxs-lookup"><span data-stu-id="240b2-109">Updating the Current Occurrence of a Recurring Task</span></span>

<span data-ttu-id="240b2-110">定期任务的 UpdateItem 操作的结果与单个非定期任务上的 UpdateItem 操作的结果不同。</span><span class="sxs-lookup"><span data-stu-id="240b2-110">The result of an UpdateItem operation on recurring tasks differs from the result of the UpdateItem operation on a single, nonrecurring task.</span></span> <span data-ttu-id="240b2-111">在进行以下更新时，对定期任务的发生所做的更改会导致生成一次性任务：</span><span class="sxs-lookup"><span data-stu-id="240b2-111">Changes to an occurrence of a recurring task cause one-off tasks to be generated when the following updates are made:</span></span>
  
1. <span data-ttu-id="240b2-112">将重新生成或 nonregenerating 重复性任务的 status 属性设置为 "**已完成**"。</span><span class="sxs-lookup"><span data-stu-id="240b2-112">The status property of a regenerating or nonregenerating recurrent task is set to **Completed**.</span></span>
    
2. <span data-ttu-id="240b2-113">Nonregenerating 重复性任务的开始日期或结束日期已更改。</span><span class="sxs-lookup"><span data-stu-id="240b2-113">The start date or end date of a nonregenerating recurrent task is changed.</span></span>
    
<span data-ttu-id="240b2-114">例如，如果**UpdateItem**请求将定期任务的已完成值设置为**True**，则**UpdateItemResponse**将包含一个新的 Id 和 ChangeKey，表示新创建的一次性任务。</span><span class="sxs-lookup"><span data-stu-id="240b2-114">For example, if an **UpdateItem** request sets the Completed value of a recurring task to **true**, the **UpdateItemResponse** will include a new Id and ChangeKey that represent a newly created one-off task.</span></span> <span data-ttu-id="240b2-115">请求中包含的 Id 仍有效，并且该 Id 表示的定期任务已更新，以表示下一个事件。</span><span class="sxs-lookup"><span data-stu-id="240b2-115">The Id that was included in the request is still valid and the recurring task that is represented by that Id has been updated to represent the next occurrence.</span></span> <span data-ttu-id="240b2-116">由于定期任务已更新，因此请求中包含的 ChangeKey 已不再有效。</span><span class="sxs-lookup"><span data-stu-id="240b2-116">The ChangeKey that was included in the request is no longer valid because the recurring task has been updated.</span></span> 
  
<span data-ttu-id="240b2-117">您可以使用[GetItem 操作](getitem-operation.md)获取定期任务的最新**ChangeKey** 。</span><span class="sxs-lookup"><span data-stu-id="240b2-117">You can use the [GetItem operation](getitem-operation.md) to get the latest **ChangeKey** for the recurring task.</span></span> 
  
<span data-ttu-id="240b2-118">对于非定期任务或定期任务的最后一次发生，UpdateItem 响应将返回传递给它的同一**Id** ，并返回关联的更新的**ChangeKey**。</span><span class="sxs-lookup"><span data-stu-id="240b2-118">For nonrecurring tasks or for the last occurrence of a recurring task, the UpdateItem response returns the same **Id** that was passed to it and returns the associated updated **ChangeKey**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="240b2-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="240b2-119">See also</span></span>



[<span data-ttu-id="240b2-120">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="240b2-120">UpdateItem operation</span></span>](updateitem-operation.md)

