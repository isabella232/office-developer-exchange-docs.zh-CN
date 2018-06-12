---
title: UpdateItem 操作 （任务）
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
ms.openlocfilehash: d6f966fa663300b476383a136d30cf611d6bfb9b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838400"
---
# <a name="updateitem-operation-task"></a><span data-ttu-id="43460-103">UpdateItem 操作 （任务）</span><span class="sxs-lookup"><span data-stu-id="43460-103">UpdateItem operation (task)</span></span>

<span data-ttu-id="43460-104">UpdateItem 操作用于更新 Exchange 存储中的任务项属性。</span><span class="sxs-lookup"><span data-stu-id="43460-104">The UpdateItem operation is used to update task item properties in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="43460-105">备注</span><span class="sxs-lookup"><span data-stu-id="43460-105">Remarks</span></span>

<span data-ttu-id="43460-106">您无法使用 Exchange Web 服务发送任务请求。</span><span class="sxs-lookup"><span data-stu-id="43460-106">You cannot use Exchange Web Services to send task requests.</span></span> <span data-ttu-id="43460-107">Exchange Web 服务可以返回由 MicrosoftOfficeOutlook 创建的任务请求。</span><span class="sxs-lookup"><span data-stu-id="43460-107">Exchange Web Services can return task requests that are created by MicrosoftOfficeOutlook.</span></span> <span data-ttu-id="43460-108">如果已发送的任务请求，请求更新任务将返回错误。</span><span class="sxs-lookup"><span data-stu-id="43460-108">If a task request has already been sent, a request to update the task will return an error.</span></span>
  
## <a name="updating-the-current-occurrence-of-a-recurring-task"></a><span data-ttu-id="43460-109">更新定期任务的当前匹配项</span><span class="sxs-lookup"><span data-stu-id="43460-109">Updating the Current Occurrence of a Recurring Task</span></span>

<span data-ttu-id="43460-110">定期任务 UpdateItem 操作的结果与单个、 非定期任务 UpdateItem 操作的结果。</span><span class="sxs-lookup"><span data-stu-id="43460-110">The result of an UpdateItem operation on recurring tasks differs from the result of the UpdateItem operation on a single, nonrecurring task.</span></span> <span data-ttu-id="43460-111">定期任务出现更改导致一次性任务要生成时进行以下更新：</span><span class="sxs-lookup"><span data-stu-id="43460-111">Changes to an occurrence of a recurring task cause one-off tasks to be generated when the following updates are made:</span></span>
  
1. <span data-ttu-id="43460-112">重新生成或 nonregenerating 重复性任务的 status 属性设置为**已完成**。</span><span class="sxs-lookup"><span data-stu-id="43460-112">The status property of a regenerating or nonregenerating recurrent task is set to **Completed**.</span></span>
    
2. <span data-ttu-id="43460-113">更改的开始日期或结束日期 nonregenerating 重复性任务。</span><span class="sxs-lookup"><span data-stu-id="43460-113">The start date or end date of a nonregenerating recurrent task is changed.</span></span>
    
<span data-ttu-id="43460-114">例如，如果**UpdateItem**请求将定期任务的完成值设置为**true**， **UpdateItemResponse**将包含新 Id 和更改密钥表示新创建的一次性任务。</span><span class="sxs-lookup"><span data-stu-id="43460-114">For example, if an **UpdateItem** request sets the Completed value of a recurring task to **true**, the **UpdateItemResponse** will include a new Id and ChangeKey that represent a newly created one-off task.</span></span> <span data-ttu-id="43460-115">仍然有效请求中包含的 Id，并由该 Id 定期任务已更新，以表示的下一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="43460-115">The Id that was included in the request is still valid and the recurring task that is represented by that Id has been updated to represent the next occurrence.</span></span> <span data-ttu-id="43460-116">包含在请求中更改密钥不再有效，因为已更新周期性任务。</span><span class="sxs-lookup"><span data-stu-id="43460-116">The ChangeKey that was included in the request is no longer valid because the recurring task has been updated.</span></span> 
  
<span data-ttu-id="43460-117">可以使用[GetItem 操作](getitem-operation.md)获取最新**更改密钥**周期性任务。</span><span class="sxs-lookup"><span data-stu-id="43460-117">You can use the [GetItem operation](getitem-operation.md) to get the latest **ChangeKey** for the recurring task.</span></span> 
  
<span data-ttu-id="43460-118">对于非定期任务或定期任务的最后一个实例，UpdateItem 响应将返回相同的**Id**的已传递给它，并返回关联的更新**更改密钥**。</span><span class="sxs-lookup"><span data-stu-id="43460-118">For nonrecurring tasks or for the last occurrence of a recurring task, the UpdateItem response returns the same **Id** that was passed to it and returns the associated updated **ChangeKey**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="43460-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="43460-119">See also</span></span>



[<span data-ttu-id="43460-120">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="43460-120">UpdateItem operation</span></span>](updateitem-operation.md)

