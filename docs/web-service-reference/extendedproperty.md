---
title: ExtendedProperty
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExtendedProperty
api_type:
- schema
ms.assetid: f9701409-b620-4afe-b9ee-4c1e95507af7
description: ExtendedProperty 元素标识文件夹和项扩展的 MAPI 属性。
ms.openlocfilehash: 6a0aecc732ef634c2258127fca89b19461e25762
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754235"
---
# <a name="extendedproperty"></a><span data-ttu-id="42d56-103">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="42d56-103">ExtendedProperty</span></span>

<span data-ttu-id="42d56-104">**ExtendedProperty**元素标识文件夹和项扩展的 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="42d56-104">The **ExtendedProperty** element identifies extended MAPI properties on folders and items.</span></span> 
  
```xml
<ExtendedProperty>
   <ExtendedFieldURI/>
   <Values/>
</ExtendedProperty>
```

 <span data-ttu-id="42d56-105">**ExtendedPropertyType**</span><span class="sxs-lookup"><span data-stu-id="42d56-105">**ExtendedPropertyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="42d56-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="42d56-106">Attributes and elements</span></span>

<span data-ttu-id="42d56-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="42d56-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="42d56-108">属性</span><span class="sxs-lookup"><span data-stu-id="42d56-108">Attributes</span></span>

<span data-ttu-id="42d56-109">无。</span><span class="sxs-lookup"><span data-stu-id="42d56-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="42d56-110">子元素</span><span class="sxs-lookup"><span data-stu-id="42d56-110">Child elements</span></span>

|<span data-ttu-id="42d56-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="42d56-111">**Element**</span></span>|<span data-ttu-id="42d56-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="42d56-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42d56-113">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="42d56-113">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="42d56-114">标识扩展的 MAPI 属性以获取、 设置或创建。</span><span class="sxs-lookup"><span data-stu-id="42d56-114">Identifies an extended MAPI property to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="42d56-115">Values</span><span class="sxs-lookup"><span data-stu-id="42d56-115">Values</span></span>](values.md) <br/> |<span data-ttu-id="42d56-116">包含多值的扩展 MAPI 属性的值的集合。</span><span class="sxs-lookup"><span data-stu-id="42d56-116">Contains a collection of values for a multivalued extended MAPI property.</span></span>  <br/> |
|[<span data-ttu-id="42d56-117">值</span><span class="sxs-lookup"><span data-stu-id="42d56-117">Value</span></span>](value.md) <br/> |<span data-ttu-id="42d56-118">包含的单值 MAPI 扩展属性的值。</span><span class="sxs-lookup"><span data-stu-id="42d56-118">Contains the value of single-valued MAPI extended property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="42d56-119">父元素</span><span class="sxs-lookup"><span data-stu-id="42d56-119">Parent elements</span></span>

|<span data-ttu-id="42d56-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="42d56-120">**Element**</span></span>|<span data-ttu-id="42d56-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="42d56-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42d56-122">日历项目</span><span class="sxs-lookup"><span data-stu-id="42d56-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="42d56-123">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="42d56-123">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="42d56-124">联系人</span><span class="sxs-lookup"><span data-stu-id="42d56-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="42d56-125">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="42d56-125">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="42d56-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="42d56-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="42d56-127">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="42d56-127">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="42d56-128">项目</span><span class="sxs-lookup"><span data-stu-id="42d56-128">Item</span></span>](item.md) <br/> |<span data-ttu-id="42d56-129">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="42d56-129">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="42d56-130">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="42d56-130">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="42d56-131">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="42d56-131">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="42d56-132">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="42d56-132">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="42d56-133">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="42d56-133">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="42d56-134">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="42d56-134">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="42d56-135">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="42d56-135">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="42d56-136">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="42d56-136">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="42d56-137">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="42d56-137">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="42d56-138">Message</span><span class="sxs-lookup"><span data-stu-id="42d56-138">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="42d56-139">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="42d56-139">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="42d56-140">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="42d56-140">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="42d56-141">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="42d56-141">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="42d56-142">任务</span><span class="sxs-lookup"><span data-stu-id="42d56-142">Task</span></span>](task.md) <br/> |<span data-ttu-id="42d56-143">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="42d56-143">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="42d56-144">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="42d56-144">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="42d56-145">表示主要包含日历项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="42d56-145">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="42d56-146">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="42d56-146">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="42d56-147">表示邮箱中的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="42d56-147">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="42d56-148">Folder</span><span class="sxs-lookup"><span data-stu-id="42d56-148">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="42d56-149">代表一个文件夹，用于创建、 获取、 查找、 同步，或更新。</span><span class="sxs-lookup"><span data-stu-id="42d56-149">Represents a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="42d56-150">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="42d56-150">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="42d56-151">表示包含在邮箱中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="42d56-151">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="42d56-152">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="42d56-152">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="42d56-153">表示包含在邮箱中的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="42d56-153">Represents a tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42d56-154">备注</span><span class="sxs-lookup"><span data-stu-id="42d56-154">Remarks</span></span>

<span data-ttu-id="42d56-155">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="42d56-155">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="42d56-156">元素信息</span><span class="sxs-lookup"><span data-stu-id="42d56-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="42d56-157">命名空间</span><span class="sxs-lookup"><span data-stu-id="42d56-157">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="42d56-158">架构名称</span><span class="sxs-lookup"><span data-stu-id="42d56-158">Schema Name</span></span>  <br/> |<span data-ttu-id="42d56-159">类型架构</span><span class="sxs-lookup"><span data-stu-id="42d56-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="42d56-160">验证文件</span><span class="sxs-lookup"><span data-stu-id="42d56-160">Validation File</span></span>  <br/> |<span data-ttu-id="42d56-161">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="42d56-161">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="42d56-162">可以为空</span><span class="sxs-lookup"><span data-stu-id="42d56-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="42d56-163">False</span><span class="sxs-lookup"><span data-stu-id="42d56-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42d56-164">另请参阅</span><span class="sxs-lookup"><span data-stu-id="42d56-164">See also</span></span>



- [<span data-ttu-id="42d56-165">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="42d56-165">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

