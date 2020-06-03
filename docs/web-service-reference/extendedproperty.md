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
description: ExtendedProperty 元素标识文件夹和项目的扩展 MAPI 属性。
ms.openlocfilehash: 99ede097d803d6fbf534cde0e77c08cec054bfa3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530605"
---
# <a name="extendedproperty"></a><span data-ttu-id="ba4da-103">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="ba4da-103">ExtendedProperty</span></span>

<span data-ttu-id="ba4da-104">**ExtendedProperty**元素标识文件夹和项目的扩展 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="ba4da-104">The **ExtendedProperty** element identifies extended MAPI properties on folders and items.</span></span> 
  
```xml
<ExtendedProperty>
   <ExtendedFieldURI/>
   <Values/>
</ExtendedProperty>
```

```xml
<ExtendedProperty>
   <ExtendedFieldURI/>
   <Value/>
</ExtendedProperty>
```

<span data-ttu-id="ba4da-105">**ExtendedPropertyType**</span><span class="sxs-lookup"><span data-stu-id="ba4da-105">**ExtendedPropertyType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ba4da-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ba4da-106">Attributes and elements</span></span>

<span data-ttu-id="ba4da-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ba4da-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba4da-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ba4da-108">Attributes</span></span>

<span data-ttu-id="ba4da-109">无。</span><span class="sxs-lookup"><span data-stu-id="ba4da-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba4da-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ba4da-110">Child elements</span></span>

|<span data-ttu-id="ba4da-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ba4da-111">**Element**</span></span>|<span data-ttu-id="ba4da-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ba4da-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba4da-113">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="ba4da-113">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="ba4da-114">标识要获取、设置或创建的扩展 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="ba4da-114">Identifies an extended MAPI property to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="ba4da-115">值</span><span class="sxs-lookup"><span data-stu-id="ba4da-115">Values</span></span>](values.md) <br/> |<span data-ttu-id="ba4da-116">包含多值扩展 MAPI 属性的值的集合。</span><span class="sxs-lookup"><span data-stu-id="ba4da-116">Contains a collection of values for a multivalued extended MAPI property.</span></span>  <br/> |
|[<span data-ttu-id="ba4da-117">值</span><span class="sxs-lookup"><span data-stu-id="ba4da-117">Value</span></span>](value.md) <br/> |<span data-ttu-id="ba4da-118">包含单值 MAPI 扩展属性的值。</span><span class="sxs-lookup"><span data-stu-id="ba4da-118">Contains the value of single-valued MAPI extended property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ba4da-119">父元素</span><span class="sxs-lookup"><span data-stu-id="ba4da-119">Parent elements</span></span>

|<span data-ttu-id="ba4da-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="ba4da-120">**Element**</span></span>|<span data-ttu-id="ba4da-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="ba4da-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba4da-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="ba4da-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="ba4da-123">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="ba4da-123">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="ba4da-124">Contact</span><span class="sxs-lookup"><span data-stu-id="ba4da-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="ba4da-125">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="ba4da-125">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="ba4da-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="ba4da-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="ba4da-127">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="ba4da-127">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="ba4da-128">项目</span><span class="sxs-lookup"><span data-stu-id="ba4da-128">Item</span></span>](item.md) <br/> |<span data-ttu-id="ba4da-129">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="ba4da-129">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ba4da-130">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="ba4da-130">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="ba4da-131">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="ba4da-131">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ba4da-132">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="ba4da-132">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="ba4da-133">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="ba4da-133">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ba4da-134">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="ba4da-134">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="ba4da-135">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="ba4da-135">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ba4da-136">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="ba4da-136">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="ba4da-137">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="ba4da-137">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ba4da-138">Message</span><span class="sxs-lookup"><span data-stu-id="ba4da-138">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ba4da-139">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="ba4da-139">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="ba4da-140">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="ba4da-140">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="ba4da-141">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="ba4da-141">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ba4da-142">任务</span><span class="sxs-lookup"><span data-stu-id="ba4da-142">Task</span></span>](task.md) <br/> |<span data-ttu-id="ba4da-143">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="ba4da-143">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ba4da-144">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="ba4da-144">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="ba4da-145">代表主要包含日历项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="ba4da-145">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="ba4da-146">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="ba4da-146">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="ba4da-147">表示邮箱中的 "联系人" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="ba4da-147">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="ba4da-148">Folder</span><span class="sxs-lookup"><span data-stu-id="ba4da-148">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="ba4da-149">表示要创建、获取、查找、同步或更新的文件夹。</span><span class="sxs-lookup"><span data-stu-id="ba4da-149">Represents a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="ba4da-150">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="ba4da-150">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="ba4da-151">表示邮箱中包含的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="ba4da-151">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="ba4da-152">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="ba4da-152">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="ba4da-153">表示邮箱中包含的 "任务" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="ba4da-153">Represents a tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba4da-154">说明</span><span class="sxs-lookup"><span data-stu-id="ba4da-154">Remarks</span></span>

<span data-ttu-id="ba4da-155">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ba4da-155">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba4da-156">元素信息</span><span class="sxs-lookup"><span data-stu-id="ba4da-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba4da-157">命名空间</span><span class="sxs-lookup"><span data-stu-id="ba4da-157">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ba4da-158">架构名称</span><span class="sxs-lookup"><span data-stu-id="ba4da-158">Schema Name</span></span>  <br/> |<span data-ttu-id="ba4da-159">类型架构</span><span class="sxs-lookup"><span data-stu-id="ba4da-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="ba4da-160">验证文件</span><span class="sxs-lookup"><span data-stu-id="ba4da-160">Validation File</span></span>  <br/> |<span data-ttu-id="ba4da-161">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ba4da-161">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ba4da-162">可以为空</span><span class="sxs-lookup"><span data-stu-id="ba4da-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="ba4da-163">False</span><span class="sxs-lookup"><span data-stu-id="ba4da-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba4da-164">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ba4da-164">See also</span></span>

- [<span data-ttu-id="ba4da-165">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ba4da-165">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

