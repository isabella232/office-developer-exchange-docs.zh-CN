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
description: CreateItem 元素定义一个请求，以在 Exchange 存储中创建项目。
ms.openlocfilehash: 235664b7baeceeccb14135fd346123f0f7d99346
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527059"
---
# <a name="createitem"></a><span data-ttu-id="109b6-103">CreateItem</span><span class="sxs-lookup"><span data-stu-id="109b6-103">CreateItem</span></span>

<span data-ttu-id="109b6-104">**CreateItem**元素定义一个请求，以在 Exchange 存储中创建项目。</span><span class="sxs-lookup"><span data-stu-id="109b6-104">The **CreateItem** element defines a request to create an item in the Exchange store.</span></span> 
  
```xml
<CreateItem MessageDisposition="" SendMeetingInvitations="">
   <SavedItemFolderId/>
   <Items/>
</CreateItem>
```

<span data-ttu-id="109b6-105">**CreateItemType**</span><span class="sxs-lookup"><span data-stu-id="109b6-105">**CreateItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="109b6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="109b6-106">Attributes and elements</span></span>

<span data-ttu-id="109b6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="109b6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="109b6-108">属性</span><span class="sxs-lookup"><span data-stu-id="109b6-108">Attributes</span></span>

|<span data-ttu-id="109b6-109">属性</span><span class="sxs-lookup"><span data-stu-id="109b6-109">Attribute</span></span>|<span data-ttu-id="109b6-110">说明</span><span class="sxs-lookup"><span data-stu-id="109b6-110">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="109b6-111">**MessageDisposition**</span><span class="sxs-lookup"><span data-stu-id="109b6-111">**MessageDisposition**</span></span> <br/> |<span data-ttu-id="109b6-112">介绍如何在创建项目后对其进行处理。</span><span class="sxs-lookup"><span data-stu-id="109b6-112">Describes how the item will be handled after it is created.</span></span> <span data-ttu-id="109b6-113">电子邮件的属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="109b6-113">The attribute is required for e-mail messages.</span></span> <span data-ttu-id="109b6-114">此属性仅适用于电子邮件。</span><span class="sxs-lookup"><span data-stu-id="109b6-114">This attribute is only applicable to e-mail messages.</span></span>  <br/> |
|<span data-ttu-id="109b6-115">**SendMeetingInvitations**</span><span class="sxs-lookup"><span data-stu-id="109b6-115">**SendMeetingInvitations**</span></span> <br/> |<span data-ttu-id="109b6-116">介绍如何在创建会议请求后对其进行处理。</span><span class="sxs-lookup"><span data-stu-id="109b6-116">Describes how meeting requests are handled after they are created.</span></span> <span data-ttu-id="109b6-117">此属性是日历项目所必需的。</span><span class="sxs-lookup"><span data-stu-id="109b6-117">This attribute is required for calendar items.</span></span>  <br/> |
   
#### <a name="messagedisposition-attribute"></a><span data-ttu-id="109b6-118">MessageDisposition 属性</span><span class="sxs-lookup"><span data-stu-id="109b6-118">MessageDisposition Attribute</span></span>

|<span data-ttu-id="109b6-119">值</span><span class="sxs-lookup"><span data-stu-id="109b6-119">Value</span></span>|<span data-ttu-id="109b6-120">Description</span><span class="sxs-lookup"><span data-stu-id="109b6-120">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="109b6-121">SaveOnly</span><span class="sxs-lookup"><span data-stu-id="109b6-121">SaveOnly</span></span>  <br/> |<span data-ttu-id="109b6-122">邮件项目保存在由[SavedItemFolderId](saveditemfolderid.md)元素指定的文件夹中。</span><span class="sxs-lookup"><span data-stu-id="109b6-122">The message item is saved in the folder that is specified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span> <span data-ttu-id="109b6-123">稍后可以使用[SendItem 操作](senditem-operation.md)发送邮件。</span><span class="sxs-lookup"><span data-stu-id="109b6-123">Messages can be sent later by using the [SendItem operation](senditem-operation.md).</span></span> <span data-ttu-id="109b6-124">响应中返回项目标识符。</span><span class="sxs-lookup"><span data-stu-id="109b6-124">An item identifier is returned in the response.</span></span> <span data-ttu-id="109b6-125">不会为除邮件项目之外的任何项目类型返回项目标识符。</span><span class="sxs-lookup"><span data-stu-id="109b6-125">Item identifiers are not returned for any item types except for message items.</span></span> <span data-ttu-id="109b6-126">其中包括 response 对象。</span><span class="sxs-lookup"><span data-stu-id="109b6-126">This includes response objects.</span></span>  <br/> |
|<span data-ttu-id="109b6-127">SendOnly</span><span class="sxs-lookup"><span data-stu-id="109b6-127">SendOnly</span></span>  <br/> |<span data-ttu-id="109b6-128">项目已发送，但未在 "已发送邮件" 文件夹中保存副本。</span><span class="sxs-lookup"><span data-stu-id="109b6-128">The item is sent but no copy is saved in the Sent Items folder.</span></span> <span data-ttu-id="109b6-129">响应中不返回项目标识符。</span><span class="sxs-lookup"><span data-stu-id="109b6-129">An item identifier is not returned in the response.</span></span><br/><br/><span data-ttu-id="109b6-130">**注意**： **CreateItem**不支持在使用 SendOnly 选项时进行代理访问，因为无法使用此选项指定目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="109b6-130">**NOTE**: **CreateItem** does not support delegate access when the SendOnly option is used because a destination folder cannot be specified with this option.</span></span> <span data-ttu-id="109b6-131">解决方法是创建项目，获取项目标识符，然后使用 SendItem 操作发送项目。</span><span class="sxs-lookup"><span data-stu-id="109b6-131">The workaround is to create the item, get the item identifier, and then use the SendItem operation to send the item.</span></span>           |
|<span data-ttu-id="109b6-132">SendAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="109b6-132">SendAndSaveCopy</span></span>  <br/> |<span data-ttu-id="109b6-133">将发送项目，并将副本保存在由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹中。</span><span class="sxs-lookup"><span data-stu-id="109b6-133">The item is sent and a copy is saved in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span> <span data-ttu-id="109b6-134">响应中不返回项目标识符。</span><span class="sxs-lookup"><span data-stu-id="109b6-134">An item identifier is not returned in the response.</span></span><br/><br/><span data-ttu-id="109b6-135">**注意**：会议请求不会保存到由[SavedItemFolderId](saveditemfolderid.md)属性标识的文件夹中。</span><span class="sxs-lookup"><span data-stu-id="109b6-135">**NOTE**: Meeting requests are not saved to the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) property.</span></span> <span data-ttu-id="109b6-136">对于日历，仅可通过**SavedItemFolderId**属性指定日历项目的保存位置。</span><span class="sxs-lookup"><span data-stu-id="109b6-136">For calendaring, only the save location for calendar items can be specified by the **SavedItemFolderId** property.</span></span> <span data-ttu-id="109b6-137">您不能控制会议请求项目的保存位置。</span><span class="sxs-lookup"><span data-stu-id="109b6-137">You cannot control where a meeting request item is saved.</span></span> <span data-ttu-id="109b6-138">只会复制关联的日历项目并将其保存到由**SavedItemFolderId**属性标识的文件夹中。</span><span class="sxs-lookup"><span data-stu-id="109b6-138">Only the associated calendar items are copied and saved into the folder that is identified by the **SavedItemFolderId** property.</span></span>           |
   
#### <a name="sendmeetinginvitations-attribute"></a><span data-ttu-id="109b6-139">SendMeetingInvitations 属性</span><span class="sxs-lookup"><span data-stu-id="109b6-139">SendMeetingInvitations Attribute</span></span>

|<span data-ttu-id="109b6-140">值</span><span class="sxs-lookup"><span data-stu-id="109b6-140">Value</span></span>|<span data-ttu-id="109b6-141">Description</span><span class="sxs-lookup"><span data-stu-id="109b6-141">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="109b6-142">SendToNone</span><span class="sxs-lookup"><span data-stu-id="109b6-142">SendToNone</span></span>  <br/> |<span data-ttu-id="109b6-143">如果该项目是会议请求，则会将其保存为日历项目，但不会发送。</span><span class="sxs-lookup"><span data-stu-id="109b6-143">If the item is a meeting request, it is saved as a calendar item but not sent.</span></span>  <br/> |
|<span data-ttu-id="109b6-144">SendOnlyToAll</span><span class="sxs-lookup"><span data-stu-id="109b6-144">SendOnlyToAll</span></span>  <br/> |<span data-ttu-id="109b6-145">会议请求将发送给所有与会者，但不会保存在 "已发送邮件" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="109b6-145">The meeting request is sent to all attendees but is not saved in the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="109b6-146">SendToAllAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="109b6-146">SendToAllAndSaveCopy</span></span>  <br/> |<span data-ttu-id="109b6-147">将会议请求发送给所有与会者，并将副本保存在由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹中。</span><span class="sxs-lookup"><span data-stu-id="109b6-147">The meeting request is sent to all attendees and a copy is saved in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="109b6-148">子元素</span><span class="sxs-lookup"><span data-stu-id="109b6-148">Child elements</span></span>

|<span data-ttu-id="109b6-149">元素</span><span class="sxs-lookup"><span data-stu-id="109b6-149">Element</span></span>|<span data-ttu-id="109b6-150">说明</span><span class="sxs-lookup"><span data-stu-id="109b6-150">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="109b6-151">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="109b6-151">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> |<span data-ttu-id="109b6-152">标识可在其中创建新项目的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="109b6-152">Identifies the target folder where a new item can be created.</span></span> <span data-ttu-id="109b6-153">如果将**MessageDisposition**属性设置为 SendOnly，则仅发送已创建的邮件。</span><span class="sxs-lookup"><span data-stu-id="109b6-153">If the **MessageDisposition** attribute is set to SendOnly, a created message will only be sent.</span></span> <span data-ttu-id="109b6-154">该邮件不会被放在由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹中。</span><span class="sxs-lookup"><span data-stu-id="109b6-154">The message will not be put in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="109b6-155">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="109b6-155">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="109b6-156">包含要在由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="109b6-156">Contains an array of items to create in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="109b6-157">父元素</span><span class="sxs-lookup"><span data-stu-id="109b6-157">Parent elements</span></span>

<span data-ttu-id="109b6-158">无。</span><span class="sxs-lookup"><span data-stu-id="109b6-158">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="109b6-159">说明</span><span class="sxs-lookup"><span data-stu-id="109b6-159">Remarks</span></span>

<span data-ttu-id="109b6-160">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="109b6-160">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="109b6-161">元素信息</span><span class="sxs-lookup"><span data-stu-id="109b6-161">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="109b6-162">命名空间</span><span class="sxs-lookup"><span data-stu-id="109b6-162">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="109b6-163">架构名称</span><span class="sxs-lookup"><span data-stu-id="109b6-163">Schema Name</span></span>  <br/> |<span data-ttu-id="109b6-164">消息架构</span><span class="sxs-lookup"><span data-stu-id="109b6-164">Messages schema</span></span>  <br/> |
|<span data-ttu-id="109b6-165">验证文件</span><span class="sxs-lookup"><span data-stu-id="109b6-165">Validation File</span></span>  <br/> |<span data-ttu-id="109b6-166">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="109b6-166">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="109b6-167">可以为空</span><span class="sxs-lookup"><span data-stu-id="109b6-167">Can be Empty</span></span>  <br/> |<span data-ttu-id="109b6-168">False</span><span class="sxs-lookup"><span data-stu-id="109b6-168">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="109b6-169">另请参阅</span><span class="sxs-lookup"><span data-stu-id="109b6-169">See also</span></span>

- [<span data-ttu-id="109b6-170">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="109b6-170">CreateItemResponse</span></span>](createitemresponse.md)  
- [<span data-ttu-id="109b6-171">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="109b6-171">CreateItem operation</span></span>](createitem-operation.md)
- [<span data-ttu-id="109b6-172">创建电子邮件</span><span class="sxs-lookup"><span data-stu-id="109b6-172">Creating E-mail Messages</span></span>](https://msdn.microsoft.com/library/05bfb83c-2866-427d-a9fe-14ba3cb02793%28Office.15%29.aspx) 
- [<span data-ttu-id="109b6-173">创建联系人（Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="109b6-173">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [<span data-ttu-id="109b6-174">创建任务</span><span class="sxs-lookup"><span data-stu-id="109b6-174">Creating Tasks</span></span>](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx) 
- [<span data-ttu-id="109b6-175">创建约会</span><span class="sxs-lookup"><span data-stu-id="109b6-175">Creating Appointments</span></span>](https://msdn.microsoft.com/library/2385391e-c9e7-4d45-b803-c4ff94d5c94e%28Office.15%29.aspx)

