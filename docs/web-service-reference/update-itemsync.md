---
title: Update （ItemSync）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Update
api_type:
- schema
ms.assetid: 4e204446-1c80-44f9-b93b-77ce630a01a5
description: Update 元素标识要在本地客户端存储中更新的单个项。
ms.openlocfilehash: 12248cbbd5d47a19e36d49fcebe6d4753a2e162f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468885"
---
# <a name="update-itemsync"></a><span data-ttu-id="716a6-103">Update （ItemSync）</span><span class="sxs-lookup"><span data-stu-id="716a6-103">Update (ItemSync)</span></span>

<span data-ttu-id="716a6-104">**Update**元素标识要在本地客户端存储中更新的单个项。</span><span class="sxs-lookup"><span data-stu-id="716a6-104">The **Update** element identifies a single item to update in the local client store.</span></span> 
  
- [<span data-ttu-id="716a6-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="716a6-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md) 
- [<span data-ttu-id="716a6-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="716a6-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="716a6-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="716a6-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)  
- [<span data-ttu-id="716a6-108">更改（项目）</span><span class="sxs-lookup"><span data-stu-id="716a6-108">Changes (Items)</span></span>](changes-items.md)  
- [<span data-ttu-id="716a6-109">Update （ItemSync）</span><span class="sxs-lookup"><span data-stu-id="716a6-109">Update (ItemSync)</span></span>](update-itemsync.md)
  
```xml
<Update>
   <Item/>
</Update>
```

```xml
<Update>
   <MeetingRequest/>
</Update>
```

```xml
<Update>
   <MeetingCancellation/>
</Update>
```

```xml
<Update>
   <Task/>
</Update>
```

```xml
<Update>
   <CalendarItem/>
</Update>
```

```xml
<Update>
   <MeetingResponse/>
</Update>
```

```xml
<Update>
   <Message/>
</Update>
```

```xml
<Update>
   <DistributionList/>
</Update>
```

```xml
<Update>
   <MeetingMessage/>
</Update>
```

```xml
<Update>
   <Contact/> 
</Update>
```

<span data-ttu-id="716a6-110">**SyncFolderItemsCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="716a6-110">**SyncFolderItemsCreateOrUpdateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="716a6-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="716a6-111">Attributes and elements</span></span>

<span data-ttu-id="716a6-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="716a6-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="716a6-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="716a6-113">Attributes</span></span>

<span data-ttu-id="716a6-114">无。</span><span class="sxs-lookup"><span data-stu-id="716a6-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="716a6-115">子元素</span><span class="sxs-lookup"><span data-stu-id="716a6-115">Child elements</span></span>

|<span data-ttu-id="716a6-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="716a6-116">**Element**</span></span>|<span data-ttu-id="716a6-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="716a6-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="716a6-118">Item</span><span class="sxs-lookup"><span data-stu-id="716a6-118">Item</span></span>](item.md) <br/> |<span data-ttu-id="716a6-119">表示要更新的通用 Exchange 项。</span><span class="sxs-lookup"><span data-stu-id="716a6-119">Represents a generic Exchange item to update.</span></span>  <br/> |
|[<span data-ttu-id="716a6-120">邮件</span><span class="sxs-lookup"><span data-stu-id="716a6-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="716a6-121">表示要更新的 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="716a6-121">Represents an Exchange e-mail message to update.</span></span>  <br/> |
|[<span data-ttu-id="716a6-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="716a6-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="716a6-123">表示要更新的 Exchange 日历项目。</span><span class="sxs-lookup"><span data-stu-id="716a6-123">Represents an Exchange calendar item to update.</span></span>  <br/> |
|[<span data-ttu-id="716a6-124">联系人</span><span class="sxs-lookup"><span data-stu-id="716a6-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="716a6-125">表示要更新的 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="716a6-125">Represents an Exchange contact item to update.</span></span>  <br/> |
|[<span data-ttu-id="716a6-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="716a6-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="716a6-127">表示要更新的通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="716a6-127">Represents a distribution list to update.</span></span>  <br/> |
|[<span data-ttu-id="716a6-128">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="716a6-128">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="716a6-129">表示要更新的会议邮件。</span><span class="sxs-lookup"><span data-stu-id="716a6-129">Represents a meeting message to update.</span></span>  <br/> |
|[<span data-ttu-id="716a6-130">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="716a6-130">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="716a6-131">表示要更新的会议请求。</span><span class="sxs-lookup"><span data-stu-id="716a6-131">Represents a meeting request to update.</span></span>  <br/> |
|[<span data-ttu-id="716a6-132">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="716a6-132">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="716a6-133">表示要更新的会议响应。</span><span class="sxs-lookup"><span data-stu-id="716a6-133">Represents a meeting response to update.</span></span>  <br/> |
|[<span data-ttu-id="716a6-134">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="716a6-134">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="716a6-135">表示要更新的会议取消。</span><span class="sxs-lookup"><span data-stu-id="716a6-135">Represents a meeting cancellation to update.</span></span>  <br/> |
|[<span data-ttu-id="716a6-136">Task</span><span class="sxs-lookup"><span data-stu-id="716a6-136">Task</span></span>](task.md) <br/> |<span data-ttu-id="716a6-137">表示要更新的任务。</span><span class="sxs-lookup"><span data-stu-id="716a6-137">Represents a task to update.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="716a6-138">父元素</span><span class="sxs-lookup"><span data-stu-id="716a6-138">Parent elements</span></span>

|<span data-ttu-id="716a6-139">**元素**</span><span class="sxs-lookup"><span data-stu-id="716a6-139">**Element**</span></span>|<span data-ttu-id="716a6-140">**说明**</span><span class="sxs-lookup"><span data-stu-id="716a6-140">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="716a6-141">更改（项目）</span><span class="sxs-lookup"><span data-stu-id="716a6-141">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="716a6-142">包含更改类型的序列数组，这些类型表示客户端上的项与 Exchange 服务器上的项之间的差异类型。</span><span class="sxs-lookup"><span data-stu-id="716a6-142">Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="716a6-143">说明</span><span class="sxs-lookup"><span data-stu-id="716a6-143">Remarks</span></span>

<span data-ttu-id="716a6-144">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="716a6-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="716a6-145">元素信息</span><span class="sxs-lookup"><span data-stu-id="716a6-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="716a6-146">命名空间</span><span class="sxs-lookup"><span data-stu-id="716a6-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="716a6-147">架构名称</span><span class="sxs-lookup"><span data-stu-id="716a6-147">Schema name</span></span>  <br/> |<span data-ttu-id="716a6-148">类型架构</span><span class="sxs-lookup"><span data-stu-id="716a6-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="716a6-149">验证文件</span><span class="sxs-lookup"><span data-stu-id="716a6-149">Validation file</span></span>  <br/> |<span data-ttu-id="716a6-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="716a6-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="716a6-151">可以为空</span><span class="sxs-lookup"><span data-stu-id="716a6-151">Can be empty</span></span>  <br/> |<span data-ttu-id="716a6-152">False</span><span class="sxs-lookup"><span data-stu-id="716a6-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="716a6-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="716a6-153">See also</span></span>

- [<span data-ttu-id="716a6-154">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="716a6-154">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="716a6-155">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="716a6-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

