---
title: 在 Exchange 中处理 EWS 中的与删除相关的错误
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1bbe8507-7730-45e5-9232-c4f6fc39c2d9
description: 了解如何处理通过在 Exchange 中使用 EWS 托管 API 或 EWS 开发的应用程序中与删除相关的错误。
ms.openlocfilehash: 41c217c1c3815606d898b8237ea327f34869174b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455945"
---
# <a name="handling-deletion-related-errors-in-ews-in-exchange"></a><span data-ttu-id="3a45f-103">在 Exchange 中处理 EWS 中的与删除相关的错误</span><span class="sxs-lookup"><span data-stu-id="3a45f-103">Handling deletion-related errors in EWS in Exchange</span></span>

<span data-ttu-id="3a45f-104">了解如何处理通过在 Exchange 中使用 EWS 托管 API 或 EWS 开发的应用程序中与删除相关的错误。</span><span class="sxs-lookup"><span data-stu-id="3a45f-104">Find out how to handle deletion-related errors in applications that you develop by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="3a45f-105">如果您的应用程序[删除项目和文件夹](deleting-items-by-using-ews-in-exchange.md)，则可能需要处理与删除相关的错误。</span><span class="sxs-lookup"><span data-stu-id="3a45f-105">If your application [deletes items and folders](deleting-items-by-using-ews-in-exchange.md), you might have to handle deletion-related errors.</span></span> <span data-ttu-id="3a45f-106">您可以处理这些错误在运行时，或者开发 EWS 应用程序时。</span><span class="sxs-lookup"><span data-stu-id="3a45f-106">You can handle these errors at runtime, or while you are developing your EWS application.</span></span>
  
<span data-ttu-id="3a45f-107">**表1：与删除相关的错误及其处理方法**</span><span class="sxs-lookup"><span data-stu-id="3a45f-107">**Table 1: Deletion-related errors and how to handle them**</span></span>

|<span data-ttu-id="3a45f-108">**Error**</span><span class="sxs-lookup"><span data-stu-id="3a45f-108">**Error**</span></span>|<span data-ttu-id="3a45f-109">**当您尝试 .。。**</span><span class="sxs-lookup"><span data-stu-id="3a45f-109">**Occurs when you try to…**</span></span>|<span data-ttu-id="3a45f-110">**处理它的...**</span><span class="sxs-lookup"><span data-stu-id="3a45f-110">**Handle it by…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3a45f-111">ErrorAffectedTaskOccurrencesRequired</span><span class="sxs-lookup"><span data-stu-id="3a45f-111">ErrorAffectedTaskOccurrencesRequired</span></span>  <br/> |<span data-ttu-id="3a45f-112">删除定期任务的实例，并且不设置**AffectedTaskOccurrence**属性。</span><span class="sxs-lookup"><span data-stu-id="3a45f-112">Delete an instance of a recurring task, and the **AffectedTaskOccurrence** property is not set.</span></span>  <br/> |<span data-ttu-id="3a45f-113">设置**AffectedTaskOccurrence**属性，然后重试删除。</span><span class="sxs-lookup"><span data-stu-id="3a45f-113">Setting the **AffectedTaskOccurrence** property, and retrying the deletion.</span></span>  <br/> |
|<span data-ttu-id="3a45f-114">ErrorCalendarCannotUpdateDeletedItem</span><span class="sxs-lookup"><span data-stu-id="3a45f-114">ErrorCalendarCannotUpdateDeletedItem</span></span>  <br/> |<span data-ttu-id="3a45f-115">更新将导致向与会者发送会议邀请时，更新 "已删除邮件" 文件夹中的 "日历" 项目。</span><span class="sxs-lookup"><span data-stu-id="3a45f-115">Update a calendar item located in the Deleted Items folder when the update would result in sending a meeting invite to attendees.</span></span>  <br/> |<span data-ttu-id="3a45f-116">取消更新或将日历项目移回默认的 "日历" 文件夹，并更新 "日历" 项目。</span><span class="sxs-lookup"><span data-stu-id="3a45f-116">Canceling the update or moving the calendar item back to the default Calendar folder and updating the calendar item.</span></span>  <br/> |
|<span data-ttu-id="3a45f-117">ErrorCalendarOccurrenceIsDeletedFromRecurrence</span><span class="sxs-lookup"><span data-stu-id="3a45f-117">ErrorCalendarOccurrenceIsDeletedFromRecurrence</span></span>  <br/> |<span data-ttu-id="3a45f-118">引用定期约会的已删除事件。</span><span class="sxs-lookup"><span data-stu-id="3a45f-118">Reference a deleted occurrence of a recurring appointment.</span></span>  <br/> |<span data-ttu-id="3a45f-119">删除对已删除事件的引用。</span><span class="sxs-lookup"><span data-stu-id="3a45f-119">Removing a reference to a deleted occurrence.</span></span>  <br/> |
|<span data-ttu-id="3a45f-120">ErrorCannotDeleteObject</span><span class="sxs-lookup"><span data-stu-id="3a45f-120">ErrorCannotDeleteObject</span></span>  <br/> |<span data-ttu-id="3a45f-121">删除无法删除的项目。</span><span class="sxs-lookup"><span data-stu-id="3a45f-121">Delete an item that cannot be deleted.</span></span>  <br/> |<span data-ttu-id="3a45f-122">退出删除项目的尝试。</span><span class="sxs-lookup"><span data-stu-id="3a45f-122">Quitting attempts to delete the item.</span></span>  <br/> |
|<span data-ttu-id="3a45f-123">ErrorCannotDeleteTaskOccurrence</span><span class="sxs-lookup"><span data-stu-id="3a45f-123">ErrorCannotDeleteTaskOccurrence</span></span>  <br/> |<span data-ttu-id="3a45f-124">删除非定期任务的事件或删除定期任务的最后一个事件。</span><span class="sxs-lookup"><span data-stu-id="3a45f-124">Delete an occurrence of a nonrecurring task or delete the last occurrence of a recurring task.</span></span>  <br/> |<span data-ttu-id="3a45f-125">删除非定期任务或退出删除定期任务的最后一个事件的尝试。</span><span class="sxs-lookup"><span data-stu-id="3a45f-125">Deleting a nonrecurring task or quitting attempts to delete the last occurrence of a recurring task.</span></span>  <br/> |
|<span data-ttu-id="3a45f-126">ErrorDeleteDistinguishedFolder</span><span class="sxs-lookup"><span data-stu-id="3a45f-126">ErrorDeleteDistinguishedFolder</span></span>  <br/> |<span data-ttu-id="3a45f-127">删除可分辨文件夹。</span><span class="sxs-lookup"><span data-stu-id="3a45f-127">Delete a distinguished folder.</span></span>  <br/> |<span data-ttu-id="3a45f-128">指示不能删除默认文件夹。</span><span class="sxs-lookup"><span data-stu-id="3a45f-128">Indicating that default folders cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="3a45f-129">ErrorItemNotFound</span><span class="sxs-lookup"><span data-stu-id="3a45f-129">ErrorItemNotFound</span></span>  <br/> |<span data-ttu-id="3a45f-130">访问永久删除的项目。</span><span class="sxs-lookup"><span data-stu-id="3a45f-130">Access a permanently deleted item.</span></span>  <br/> |<span data-ttu-id="3a45f-131">从存储区中删除对项的引用。</span><span class="sxs-lookup"><span data-stu-id="3a45f-131">Removing references to an item when it is deleted from the store.</span></span> <span data-ttu-id="3a45f-132">如果某项已恢复，请确保恢复对客户端所需的引用。</span><span class="sxs-lookup"><span data-stu-id="3a45f-132">If an item is recovered, make sure that you reinstate required references to the client.</span></span>  <br/> |
|<span data-ttu-id="3a45f-133">ErrorSendMeetingCancellationsRequired</span><span class="sxs-lookup"><span data-stu-id="3a45f-133">ErrorSendMeetingCancellationsRequired</span></span>  <br/> |<span data-ttu-id="3a45f-134">删除日历项目，而不指定是否应发送会议取消。</span><span class="sxs-lookup"><span data-stu-id="3a45f-134">Delete a calendar item without specifying whether meeting cancellations should be sent.</span></span>  <br/> |<span data-ttu-id="3a45f-135">指定应发送还是不应发送会议取消通知。</span><span class="sxs-lookup"><span data-stu-id="3a45f-135">Specifying that meeting cancellations should or should not be sent.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a45f-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3a45f-136">See also</span></span>


- [<span data-ttu-id="3a45f-137">使用 Exchange 中的 EWS 删除项目</span><span class="sxs-lookup"><span data-stu-id="3a45f-137">Deleting items by using EWS in Exchange</span></span>](deleting-items-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="3a45f-138">Exchange 中有关与 EWS 删除相关邮箱事件的拉取通知</span><span class="sxs-lookup"><span data-stu-id="3a45f-138">Pull notifications for EWS deletion-related mailbox events in Exchange</span></span>](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)
    
- [<span data-ttu-id="3a45f-139">使用 Exchange 中的 EWS 删除约会和取消会议</span><span class="sxs-lookup"><span data-stu-id="3a45f-139">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

