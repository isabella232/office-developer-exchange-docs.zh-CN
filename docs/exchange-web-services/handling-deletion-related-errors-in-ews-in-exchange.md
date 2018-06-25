---
title: 在 Exchange 处理删除相关 EWS 中的错误
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1bbe8507-7730-45e5-9232-c4f6fc39c2d9
description: 了解如何处理您通过使用 EWS 的 EWS 托管 API 在 Exchange 开发的应用程序中删除相关的错误。
ms.openlocfilehash: 0dc16c3350bb75fb1e91650f0a0f0b7423727eeb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752713"
---
# <a name="handling-deletion-related-errors-in-ews-in-exchange"></a><span data-ttu-id="1230a-103">在 Exchange 处理删除相关 EWS 中的错误</span><span class="sxs-lookup"><span data-stu-id="1230a-103">Handling deletion-related errors in EWS in Exchange</span></span>

<span data-ttu-id="1230a-104">了解如何处理您通过使用 EWS 的 EWS 托管 API 在 Exchange 开发的应用程序中删除相关的错误。</span><span class="sxs-lookup"><span data-stu-id="1230a-104">Find out how to handle deletion-related errors in applications that you develop by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="1230a-105">如果[项目和文件夹中删除](deleting-items-by-using-ews-in-exchange.md)您在应用程序，您可能需要处理删除相关的错误。</span><span class="sxs-lookup"><span data-stu-id="1230a-105">If your application [deletes items and folders](deleting-items-by-using-ews-in-exchange.md), you might have to handle deletion-related errors.</span></span> <span data-ttu-id="1230a-106">您可以处理这些错误在运行时，或者开发 EWS 应用程序时。</span><span class="sxs-lookup"><span data-stu-id="1230a-106">You can handle these errors at runtime, or while you are developing your EWS application.</span></span>
  
<span data-ttu-id="1230a-107">**表 1： 删除相关错误和如何处理它们**</span><span class="sxs-lookup"><span data-stu-id="1230a-107">**Table 1: Deletion-related errors and how to handle them**</span></span>

|<span data-ttu-id="1230a-108">**Error**</span><span class="sxs-lookup"><span data-stu-id="1230a-108">**Error**</span></span>|<span data-ttu-id="1230a-109">**您尝试对时发生...**</span><span class="sxs-lookup"><span data-stu-id="1230a-109">**Occurs when you try to…**</span></span>|<span data-ttu-id="1230a-110">**处理它的...**</span><span class="sxs-lookup"><span data-stu-id="1230a-110">**Handle it by…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1230a-111">ErrorAffectedTaskOccurrencesRequired</span><span class="sxs-lookup"><span data-stu-id="1230a-111">ErrorAffectedTaskOccurrencesRequired</span></span>  <br/> |<span data-ttu-id="1230a-112">删除实例定期任务，并**AffectedTaskOccurrence**属性未设置。</span><span class="sxs-lookup"><span data-stu-id="1230a-112">Delete an instance of a recurring task, and the **AffectedTaskOccurrence** property is not set.</span></span>  <br/> |<span data-ttu-id="1230a-113">设置**AffectedTaskOccurrence**属性，并删除重试。</span><span class="sxs-lookup"><span data-stu-id="1230a-113">Setting the **AffectedTaskOccurrence** property, and retrying the deletion.</span></span>  <br/> |
|<span data-ttu-id="1230a-114">ErrorCalendarCannotUpdateDeletedItem</span><span class="sxs-lookup"><span data-stu-id="1230a-114">ErrorCalendarCannotUpdateDeletedItem</span></span>  <br/> |<span data-ttu-id="1230a-115">更新日历项目位于已删除邮件文件夹中时更新将导致向与会者发送会议邀请。</span><span class="sxs-lookup"><span data-stu-id="1230a-115">Update a calendar item located in the Deleted Items folder when the update would result in sending a meeting invite to attendees.</span></span>  <br/> |<span data-ttu-id="1230a-116">取消更新或将日历项目移回默认日历文件夹和更新的日历项目。</span><span class="sxs-lookup"><span data-stu-id="1230a-116">Canceling the update or moving the calendar item back to the default Calendar folder and updating the calendar item.</span></span>  <br/> |
|<span data-ttu-id="1230a-117">ErrorCalendarOccurrenceIsDeletedFromRecurrence</span><span class="sxs-lookup"><span data-stu-id="1230a-117">ErrorCalendarOccurrenceIsDeletedFromRecurrence</span></span>  <br/> |<span data-ttu-id="1230a-118">引用已删除的匹配项的定期约会。</span><span class="sxs-lookup"><span data-stu-id="1230a-118">Reference a deleted occurrence of a recurring appointment.</span></span>  <br/> |<span data-ttu-id="1230a-119">删除已删除的匹配项的引用。</span><span class="sxs-lookup"><span data-stu-id="1230a-119">Removing a reference to a deleted occurrence.</span></span>  <br/> |
|<span data-ttu-id="1230a-120">ErrorCannotDeleteObject</span><span class="sxs-lookup"><span data-stu-id="1230a-120">ErrorCannotDeleteObject</span></span>  <br/> |<span data-ttu-id="1230a-121">删除无法删除项目。</span><span class="sxs-lookup"><span data-stu-id="1230a-121">Delete an item that cannot be deleted.</span></span>  <br/> |<span data-ttu-id="1230a-122">退出尝试删除项。</span><span class="sxs-lookup"><span data-stu-id="1230a-122">Quitting attempts to delete the item.</span></span>  <br/> |
|<span data-ttu-id="1230a-123">ErrorCannotDeleteTaskOccurrence</span><span class="sxs-lookup"><span data-stu-id="1230a-123">ErrorCannotDeleteTaskOccurrence</span></span>  <br/> |<span data-ttu-id="1230a-124">删除非定期任务的匹配项，或删除一个周期性任务的最后一个实例。</span><span class="sxs-lookup"><span data-stu-id="1230a-124">Delete an occurrence of a nonrecurring task or delete the last occurrence of a recurring task.</span></span>  <br/> |<span data-ttu-id="1230a-125">删除非定期任务或退出尝试删除一个周期性任务的最后一个实例。</span><span class="sxs-lookup"><span data-stu-id="1230a-125">Deleting a nonrecurring task or quitting attempts to delete the last occurrence of a recurring task.</span></span>  <br/> |
|<span data-ttu-id="1230a-126">ErrorDeleteDistinguishedFolder</span><span class="sxs-lookup"><span data-stu-id="1230a-126">ErrorDeleteDistinguishedFolder</span></span>  <br/> |<span data-ttu-id="1230a-127">删除可分辨的文件夹。</span><span class="sxs-lookup"><span data-stu-id="1230a-127">Delete a distinguished folder.</span></span>  <br/> |<span data-ttu-id="1230a-128">指示不能删除默认文件夹。</span><span class="sxs-lookup"><span data-stu-id="1230a-128">Indicating that default folders cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="1230a-129">ErrorItemNotFound</span><span class="sxs-lookup"><span data-stu-id="1230a-129">ErrorItemNotFound</span></span>  <br/> |<span data-ttu-id="1230a-130">永久删除项目的访问。</span><span class="sxs-lookup"><span data-stu-id="1230a-130">Access a permanently deleted item.</span></span>  <br/> |<span data-ttu-id="1230a-131">从存储区删除时，请删除项目的引用。</span><span class="sxs-lookup"><span data-stu-id="1230a-131">Removing references to an item when it is deleted from the store.</span></span> <span data-ttu-id="1230a-132">如果项目恢复，请确保您复原对客户端所需的引用。</span><span class="sxs-lookup"><span data-stu-id="1230a-132">If an item is recovered, make sure that you reinstate required references to the client.</span></span>  <br/> |
|<span data-ttu-id="1230a-133">ErrorSendMeetingCancellationsRequired</span><span class="sxs-lookup"><span data-stu-id="1230a-133">ErrorSendMeetingCancellationsRequired</span></span>  <br/> |<span data-ttu-id="1230a-134">删除日历项目时未指定是否应发送会议取消。</span><span class="sxs-lookup"><span data-stu-id="1230a-134">Delete a calendar item without specifying whether meeting cancellations should be sent.</span></span>  <br/> |<span data-ttu-id="1230a-135">指定会议取消应或不应发送。</span><span class="sxs-lookup"><span data-stu-id="1230a-135">Specifying that meeting cancellations should or should not be sent.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1230a-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1230a-136">See also</span></span>


- [<span data-ttu-id="1230a-137">通过在 Exchange 使用 EWS 中删除项目</span><span class="sxs-lookup"><span data-stu-id="1230a-137">Deleting items by using EWS in Exchange</span></span>](deleting-items-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="1230a-138">在 Exchange 拉 EWS 删除相关邮箱事件通知</span><span class="sxs-lookup"><span data-stu-id="1230a-138">Pull notifications for EWS deletion-related mailbox events in Exchange</span></span>](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)
    
- [<span data-ttu-id="1230a-139">删除约会，并在 Exchange 使用 EWS 取消会议</span><span class="sxs-lookup"><span data-stu-id="1230a-139">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

