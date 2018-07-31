---
title: CreateItem
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
ms.assetid: c3707feb-3fd4-4b8a-a68f-2abadd455163
description: CreateItem 元素定义一个请求在 Exchange 存储中创建项目。
ms.openlocfilehash: 9453323bff07749f5852dae75284c61c0895adb6
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353124"
---
# <a name="createitem"></a><span data-ttu-id="e6511-103">CreateItem</span><span class="sxs-lookup"><span data-stu-id="e6511-103">CreateItem</span></span>

<span data-ttu-id="e6511-104">**CreateItem**元素定义一个请求在 Exchange 存储中创建项目。</span><span class="sxs-lookup"><span data-stu-id="e6511-104">The **CreateItem** element defines a request to create an item in the Exchange store.</span></span> 
  
```xml
<CreateItem MessageDisposition="" SendMeetingInvitations="">
   <SavedItemFolderId/>
   <Items/>
</CreateItem>
```

<span data-ttu-id="e6511-105">**CreateItemType**</span><span class="sxs-lookup"><span data-stu-id="e6511-105">**CreateItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e6511-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e6511-106">Attributes and elements</span></span>

<span data-ttu-id="e6511-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e6511-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6511-108">属性</span><span class="sxs-lookup"><span data-stu-id="e6511-108">Attributes</span></span>

|<span data-ttu-id="e6511-109">属性</span><span class="sxs-lookup"><span data-stu-id="e6511-109">Attribute</span></span>|<span data-ttu-id="e6511-110">说明</span><span class="sxs-lookup"><span data-stu-id="e6511-110">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e6511-111">**MessageDisposition**</span><span class="sxs-lookup"><span data-stu-id="e6511-111">**MessageDisposition**</span></span> <br/> |<span data-ttu-id="e6511-112">介绍在创建之后将如何处理项目。</span><span class="sxs-lookup"><span data-stu-id="e6511-112">Describes how the item will be handled after it is created.</span></span> <span data-ttu-id="e6511-113">属性是必需的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="e6511-113">The attribute is required for e-mail messages.</span></span> <span data-ttu-id="e6511-114">此属性才适用的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="e6511-114">This attribute is only applicable to e-mail messages.</span></span>  <br/> |
|<span data-ttu-id="e6511-115">**SendMeetingInvitations**</span><span class="sxs-lookup"><span data-stu-id="e6511-115">**SendMeetingInvitations**</span></span> <br/> |<span data-ttu-id="e6511-116">介绍在创建后如何处理会议请求。</span><span class="sxs-lookup"><span data-stu-id="e6511-116">Describes how meeting requests are handled after they are created.</span></span> <span data-ttu-id="e6511-117">此属性是必需的日历项目。</span><span class="sxs-lookup"><span data-stu-id="e6511-117">This attribute is required for calendar items.</span></span>  <br/> |
   
#### <a name="messagedisposition-attribute"></a><span data-ttu-id="e6511-118">MessageDisposition 属性</span><span class="sxs-lookup"><span data-stu-id="e6511-118">MessageDisposition Attribute</span></span>

|<span data-ttu-id="e6511-119">值</span><span class="sxs-lookup"><span data-stu-id="e6511-119">Value</span></span>|<span data-ttu-id="e6511-120">说明</span><span class="sxs-lookup"><span data-stu-id="e6511-120">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e6511-121">SaveOnly</span><span class="sxs-lookup"><span data-stu-id="e6511-121">SaveOnly</span></span>  <br/> |<span data-ttu-id="e6511-122">由[SavedItemFolderId](saveditemfolderid.md)元素指定的文件夹中保存邮件项目。</span><span class="sxs-lookup"><span data-stu-id="e6511-122">The message item is saved in the folder that is specified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span> <span data-ttu-id="e6511-123">使用[SendItem 操作](senditem-operation.md)，可以稍后发送消息。</span><span class="sxs-lookup"><span data-stu-id="e6511-123">Messages can be sent later by using the [SendItem operation](senditem-operation.md).</span></span> <span data-ttu-id="e6511-124">在响应中返回的项标识符。</span><span class="sxs-lookup"><span data-stu-id="e6511-124">An item identifier is returned in the response.</span></span> <span data-ttu-id="e6511-125">项标识符不返回任何除外邮件项目的项目类型。</span><span class="sxs-lookup"><span data-stu-id="e6511-125">Item identifiers are not returned for any item types except for message items.</span></span> <span data-ttu-id="e6511-126">这包括响应对象。</span><span class="sxs-lookup"><span data-stu-id="e6511-126">This includes response objects.</span></span>  <br/> |
|<span data-ttu-id="e6511-127">SendOnly</span><span class="sxs-lookup"><span data-stu-id="e6511-127">SendOnly</span></span>  <br/> |<span data-ttu-id="e6511-128">发送项目，但没有副本保存在已发送邮件文件夹中。</span><span class="sxs-lookup"><span data-stu-id="e6511-128">The item is sent but no copy is saved in the Sent Items folder.</span></span> <span data-ttu-id="e6511-129">项标识符未响应中返回。</span><span class="sxs-lookup"><span data-stu-id="e6511-129">An item identifier is not returned in the response.</span></span><br/><br/><span data-ttu-id="e6511-130">**注意**： **CreateItem**不支持代理访问使用 SendOnly 选项时，因为无法使用此选项指定的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="e6511-130">**NOTE**: **CreateItem** does not support delegate access when the SendOnly option is used because a destination folder cannot be specified with this option.</span></span> <span data-ttu-id="e6511-131">解决方法是创建该项目，获取的项标识符，，然后使用 SendItem 操作发送项目。</span><span class="sxs-lookup"><span data-stu-id="e6511-131">The workaround is to create the item, get the item identifier, and then use the SendItem operation to send the item.</span></span>           |
|<span data-ttu-id="e6511-132">SendAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="e6511-132">SendAndSaveCopy</span></span>  <br/> |<span data-ttu-id="e6511-133">发送项目，复制并保存在由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹。</span><span class="sxs-lookup"><span data-stu-id="e6511-133">The item is sent and a copy is saved in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span> <span data-ttu-id="e6511-134">项标识符未响应中返回。</span><span class="sxs-lookup"><span data-stu-id="e6511-134">An item identifier is not returned in the response.</span></span><br/><br/><span data-ttu-id="e6511-135">**注意**： 会议请求不会保存到由[SavedItemFolderId](saveditemfolderid.md)属性标识的文件夹。</span><span class="sxs-lookup"><span data-stu-id="e6511-135">**NOTE**: Meeting requests are not saved to the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) property.</span></span> <span data-ttu-id="e6511-136">为日历，只保存**SavedItemFolderId**属性可指定的日历项目的位置。</span><span class="sxs-lookup"><span data-stu-id="e6511-136">For calendaring, only the save location for calendar items can be specified by the **SavedItemFolderId** property.</span></span> <span data-ttu-id="e6511-137">您无法控制会议请求项目的保存位置。</span><span class="sxs-lookup"><span data-stu-id="e6511-137">You cannot control where a meeting request item is saved.</span></span> <span data-ttu-id="e6511-138">仅的关联的日历项目进行复制和保存到由**SavedItemFolderId**属性标识的文件夹。</span><span class="sxs-lookup"><span data-stu-id="e6511-138">Only the associated calendar items are copied and saved into the folder that is identified by the **SavedItemFolderId** property.</span></span>           |
   
#### <a name="sendmeetinginvitations-attribute"></a><span data-ttu-id="e6511-139">SendMeetingInvitations 属性</span><span class="sxs-lookup"><span data-stu-id="e6511-139">SendMeetingInvitations Attribute</span></span>

|<span data-ttu-id="e6511-140">值</span><span class="sxs-lookup"><span data-stu-id="e6511-140">Value</span></span>|<span data-ttu-id="e6511-141">说明</span><span class="sxs-lookup"><span data-stu-id="e6511-141">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e6511-142">SendToNone</span><span class="sxs-lookup"><span data-stu-id="e6511-142">SendToNone</span></span>  <br/> |<span data-ttu-id="e6511-143">如果项目位于会议请求，它是另存为日历项目，但不是发送。</span><span class="sxs-lookup"><span data-stu-id="e6511-143">If the item is a meeting request, it is saved as a calendar item but not sent.</span></span>  <br/> |
|<span data-ttu-id="e6511-144">SendOnlyToAll</span><span class="sxs-lookup"><span data-stu-id="e6511-144">SendOnlyToAll</span></span>  <br/> |<span data-ttu-id="e6511-145">会议请求发送给所有与会者，但不是保存在已发送邮件文件夹中。</span><span class="sxs-lookup"><span data-stu-id="e6511-145">The meeting request is sent to all attendees but is not saved in the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="e6511-146">SendToAllAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="e6511-146">SendToAllAndSaveCopy</span></span>  <br/> |<span data-ttu-id="e6511-147">会议请求发送给所有与会者和副本保存由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹中。</span><span class="sxs-lookup"><span data-stu-id="e6511-147">The meeting request is sent to all attendees and a copy is saved in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e6511-148">子元素</span><span class="sxs-lookup"><span data-stu-id="e6511-148">Child elements</span></span>

|<span data-ttu-id="e6511-149">元素</span><span class="sxs-lookup"><span data-stu-id="e6511-149">Element</span></span>|<span data-ttu-id="e6511-150">说明</span><span class="sxs-lookup"><span data-stu-id="e6511-150">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6511-151">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="e6511-151">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> |<span data-ttu-id="e6511-152">标识在其中创建新项的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="e6511-152">Identifies the target folder where a new item can be created.</span></span> <span data-ttu-id="e6511-153">如果**MessageDisposition**属性设置为 SendOnly，将只发送创建的消息。</span><span class="sxs-lookup"><span data-stu-id="e6511-153">If the **MessageDisposition** attribute is set to SendOnly, a created message will only be sent.</span></span> <span data-ttu-id="e6511-154">由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹中将不进行邮件。</span><span class="sxs-lookup"><span data-stu-id="e6511-154">The message will not be put in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="e6511-155">Items (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="e6511-155">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="e6511-156">包含由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="e6511-156">Contains an array of items to create in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e6511-157">父元素</span><span class="sxs-lookup"><span data-stu-id="e6511-157">Parent elements</span></span>

<span data-ttu-id="e6511-158">无。</span><span class="sxs-lookup"><span data-stu-id="e6511-158">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e6511-159">说明</span><span class="sxs-lookup"><span data-stu-id="e6511-159">Remarks</span></span>

<span data-ttu-id="e6511-160">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e6511-160">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e6511-161">元素信息</span><span class="sxs-lookup"><span data-stu-id="e6511-161">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6511-162">命名空间</span><span class="sxs-lookup"><span data-stu-id="e6511-162">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e6511-163">架构名称</span><span class="sxs-lookup"><span data-stu-id="e6511-163">Schema Name</span></span>  <br/> |<span data-ttu-id="e6511-164">消息架构</span><span class="sxs-lookup"><span data-stu-id="e6511-164">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e6511-165">验证文件</span><span class="sxs-lookup"><span data-stu-id="e6511-165">Validation File</span></span>  <br/> |<span data-ttu-id="e6511-166">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e6511-166">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e6511-167">可以为空</span><span class="sxs-lookup"><span data-stu-id="e6511-167">Can be Empty</span></span>  <br/> |<span data-ttu-id="e6511-168">False</span><span class="sxs-lookup"><span data-stu-id="e6511-168">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6511-169">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e6511-169">See also</span></span>

- [<span data-ttu-id="e6511-170">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="e6511-170">CreateItemResponse</span></span>](createitemresponse.md)  
- [<span data-ttu-id="e6511-171">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="e6511-171">CreateItem operation</span></span>](createitem-operation.md)
- [<span data-ttu-id="e6511-172">创建电子邮件</span><span class="sxs-lookup"><span data-stu-id="e6511-172">Creating E-mail Messages</span></span>](http://msdn.microsoft.com/library/05bfb83c-2866-427d-a9fe-14ba3cb02793%28Office.15%29.aspx) 
- [<span data-ttu-id="e6511-173">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="e6511-173">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [<span data-ttu-id="e6511-174">创建任务</span><span class="sxs-lookup"><span data-stu-id="e6511-174">Creating Tasks</span></span>](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx) 
- [<span data-ttu-id="e6511-175">创建约会</span><span class="sxs-lookup"><span data-stu-id="e6511-175">Creating Appointments</span></span>](http://msdn.microsoft.com/library/2385391e-c9e7-4d45-b803-c4ff94d5c94e%28Office.15%29.aspx)

