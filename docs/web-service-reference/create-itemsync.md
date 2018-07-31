---
title: Create (ItemSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Create
api_type:
- schema
ms.assetid: cb5e64a2-66a5-4447-921e-7c13efb8f6bf
description: 创建元素标识在本地客户端库中创建的单个项。
ms.openlocfilehash: d49e54c64f7bd53dcb296d998a856c20570d81be
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353943"
---
# <a name="create-itemsync"></a><span data-ttu-id="f3362-103">Create (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="f3362-103">Create (ItemSync)</span></span>

<span data-ttu-id="f3362-104">**创建**元素标识在本地客户端库中创建的单个项。</span><span class="sxs-lookup"><span data-stu-id="f3362-104">The **Create** element identifies a single item to create in the local client store.</span></span> 
  
- [<span data-ttu-id="f3362-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="f3362-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md) 
- [<span data-ttu-id="f3362-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f3362-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="f3362-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f3362-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md) 
- [<span data-ttu-id="f3362-108">Changes (Items)</span><span class="sxs-lookup"><span data-stu-id="f3362-108">Changes (Items)</span></span>](changes-items.md) 
- [<span data-ttu-id="f3362-109">Create (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="f3362-109">Create (ItemSync)</span></span>](create-itemsync.md)
  
```xml
<Create>
   <Item/>
</Create>
```

```xml
<Create>
   <Task/> 
</Create>
```

```xml
<Create>
   <MeetingResponse/>
</Create>
```

```xml
<Create>
   <CalendarItem/>
</Create>
```

```xml
<Create>
   <MeetingMessage/>
</Create>
```

```xml
<Create>
   <DistributionList/>
</Create>
```

```xml
<Create>
   <MeetingCancellation/>
</Create>
```

```xml
<Create>
   <MeetingRequest/> 
</Create>
```

```xml
<Create>
   <Message/> 
</Create>
```

```xml
<Create>
   <Contact/> 
</Create>
```

<span data-ttu-id="f3362-110">**SyncFolderItemsCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="f3362-110">**SyncFolderItemsCreateOrUpdateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f3362-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f3362-111">Attributes and elements</span></span>

<span data-ttu-id="f3362-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f3362-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f3362-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="f3362-113">Attributes</span></span>

<span data-ttu-id="f3362-114">无。</span><span class="sxs-lookup"><span data-stu-id="f3362-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f3362-115">子元素</span><span class="sxs-lookup"><span data-stu-id="f3362-115">Child elements</span></span>

|<span data-ttu-id="f3362-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="f3362-116">**Element**</span></span>|<span data-ttu-id="f3362-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f3362-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f3362-118">Item</span><span class="sxs-lookup"><span data-stu-id="f3362-118">Item</span></span>](item.md) <br/> |<span data-ttu-id="f3362-119">表示要创建的泛型 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="f3362-119">Represents a generic Exchange item to create.</span></span>  <br/> |
|[<span data-ttu-id="f3362-120">邮件</span><span class="sxs-lookup"><span data-stu-id="f3362-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f3362-121">代表要创建 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="f3362-121">Represents an Exchange e-mail message to create.</span></span>  <br/> |
|[<span data-ttu-id="f3362-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="f3362-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="f3362-123">表示要创建 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="f3362-123">Represents an Exchange calendar item to create.</span></span>  <br/> |
|[<span data-ttu-id="f3362-124">Contact</span><span class="sxs-lookup"><span data-stu-id="f3362-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="f3362-125">表示要创建 Exchange 联系人项。</span><span class="sxs-lookup"><span data-stu-id="f3362-125">Represents an Exchange contact item to create.</span></span>  <br/> |
|[<span data-ttu-id="f3362-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="f3362-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="f3362-127">代表创建的通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="f3362-127">Represents a distribution list to create.</span></span>  <br/> |
|[<span data-ttu-id="f3362-128">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="f3362-128">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="f3362-129">代表要创建的会议消息。</span><span class="sxs-lookup"><span data-stu-id="f3362-129">Represents a meeting message to create.</span></span>  <br/> |
|[<span data-ttu-id="f3362-130">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="f3362-130">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="f3362-131">表示要创建的会议请求。</span><span class="sxs-lookup"><span data-stu-id="f3362-131">Represents a meeting request to create.</span></span>  <br/> |
|[<span data-ttu-id="f3362-132">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="f3362-132">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="f3362-133">代表要创建的会议响应。</span><span class="sxs-lookup"><span data-stu-id="f3362-133">Represents a meeting response to create.</span></span>  <br/> |
|[<span data-ttu-id="f3362-134">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="f3362-134">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="f3362-135">代表取消会议创建。</span><span class="sxs-lookup"><span data-stu-id="f3362-135">Represents a meeting cancellation to create.</span></span>  <br/> |
|[<span data-ttu-id="f3362-136">任务</span><span class="sxs-lookup"><span data-stu-id="f3362-136">Task</span></span>](task.md) <br/> |<span data-ttu-id="f3362-137">代表要创建的任务。</span><span class="sxs-lookup"><span data-stu-id="f3362-137">Represents a task to create.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f3362-138">父元素</span><span class="sxs-lookup"><span data-stu-id="f3362-138">Parent elements</span></span>

|<span data-ttu-id="f3362-139">**元素**</span><span class="sxs-lookup"><span data-stu-id="f3362-139">**Element**</span></span>|<span data-ttu-id="f3362-140">**说明**</span><span class="sxs-lookup"><span data-stu-id="f3362-140">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f3362-141">Changes (Items)</span><span class="sxs-lookup"><span data-stu-id="f3362-141">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="f3362-142">包含表示客户端上的项目和 Exchange 服务器上的项目之间的差异的类型的更改类型序列数组。</span><span class="sxs-lookup"><span data-stu-id="f3362-142">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3362-143">说明</span><span class="sxs-lookup"><span data-stu-id="f3362-143">Remarks</span></span>

<span data-ttu-id="f3362-144">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f3362-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f3362-145">元素信息</span><span class="sxs-lookup"><span data-stu-id="f3362-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3362-146">命名空间</span><span class="sxs-lookup"><span data-stu-id="f3362-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f3362-147">架构名称</span><span class="sxs-lookup"><span data-stu-id="f3362-147">Schema name</span></span>  <br/> |<span data-ttu-id="f3362-148">类型架构</span><span class="sxs-lookup"><span data-stu-id="f3362-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="f3362-149">验证文件</span><span class="sxs-lookup"><span data-stu-id="f3362-149">Validation file</span></span>  <br/> |<span data-ttu-id="f3362-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f3362-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f3362-151">可以为空</span><span class="sxs-lookup"><span data-stu-id="f3362-151">Can be empty</span></span>  <br/> |<span data-ttu-id="f3362-152">False</span><span class="sxs-lookup"><span data-stu-id="f3362-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f3362-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f3362-153">See also</span></span>

- [<span data-ttu-id="f3362-154">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="f3362-154">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="f3362-155">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f3362-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

