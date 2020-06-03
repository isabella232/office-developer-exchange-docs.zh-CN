---
title: 创建（ItemSync）
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
description: Create 元素标识要在本地客户端存储中创建的单个项目。
ms.openlocfilehash: b9c0f28333594a6c17ee9581a227fc4773874fd6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460797"
---
# <a name="create-itemsync"></a><span data-ttu-id="5232e-103">创建（ItemSync）</span><span class="sxs-lookup"><span data-stu-id="5232e-103">Create (ItemSync)</span></span>

<span data-ttu-id="5232e-104">**Create**元素标识要在本地客户端存储中创建的单个项目。</span><span class="sxs-lookup"><span data-stu-id="5232e-104">The **Create** element identifies a single item to create in the local client store.</span></span> 
  
- [<span data-ttu-id="5232e-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="5232e-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md) 
- [<span data-ttu-id="5232e-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5232e-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="5232e-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5232e-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md) 
- [<span data-ttu-id="5232e-108">更改（项目）</span><span class="sxs-lookup"><span data-stu-id="5232e-108">Changes (Items)</span></span>](changes-items.md) 
- [<span data-ttu-id="5232e-109">创建（ItemSync）</span><span class="sxs-lookup"><span data-stu-id="5232e-109">Create (ItemSync)</span></span>](create-itemsync.md)
  
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

<span data-ttu-id="5232e-110">**SyncFolderItemsCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="5232e-110">**SyncFolderItemsCreateOrUpdateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5232e-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5232e-111">Attributes and elements</span></span>

<span data-ttu-id="5232e-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5232e-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5232e-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="5232e-113">Attributes</span></span>

<span data-ttu-id="5232e-114">无。</span><span class="sxs-lookup"><span data-stu-id="5232e-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5232e-115">子元素</span><span class="sxs-lookup"><span data-stu-id="5232e-115">Child elements</span></span>

|<span data-ttu-id="5232e-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="5232e-116">**Element**</span></span>|<span data-ttu-id="5232e-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="5232e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5232e-118">Item</span><span class="sxs-lookup"><span data-stu-id="5232e-118">Item</span></span>](item.md) <br/> |<span data-ttu-id="5232e-119">表示要创建的通用 Exchange 项。</span><span class="sxs-lookup"><span data-stu-id="5232e-119">Represents a generic Exchange item to create.</span></span>  <br/> |
|[<span data-ttu-id="5232e-120">消息</span><span class="sxs-lookup"><span data-stu-id="5232e-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5232e-121">表示要创建的 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="5232e-121">Represents an Exchange e-mail message to create.</span></span>  <br/> |
|[<span data-ttu-id="5232e-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="5232e-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="5232e-123">代表要创建的 Exchange 日历项目。</span><span class="sxs-lookup"><span data-stu-id="5232e-123">Represents an Exchange calendar item to create.</span></span>  <br/> |
|[<span data-ttu-id="5232e-124">联系人</span><span class="sxs-lookup"><span data-stu-id="5232e-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="5232e-125">表示要创建的 Exchange 联系人项。</span><span class="sxs-lookup"><span data-stu-id="5232e-125">Represents an Exchange contact item to create.</span></span>  <br/> |
|[<span data-ttu-id="5232e-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="5232e-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="5232e-127">表示要创建的通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="5232e-127">Represents a distribution list to create.</span></span>  <br/> |
|[<span data-ttu-id="5232e-128">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="5232e-128">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="5232e-129">表示要创建的会议消息。</span><span class="sxs-lookup"><span data-stu-id="5232e-129">Represents a meeting message to create.</span></span>  <br/> |
|[<span data-ttu-id="5232e-130">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="5232e-130">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="5232e-131">表示要创建的会议请求。</span><span class="sxs-lookup"><span data-stu-id="5232e-131">Represents a meeting request to create.</span></span>  <br/> |
|[<span data-ttu-id="5232e-132">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="5232e-132">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="5232e-133">表示要创建的会议响应。</span><span class="sxs-lookup"><span data-stu-id="5232e-133">Represents a meeting response to create.</span></span>  <br/> |
|[<span data-ttu-id="5232e-134">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="5232e-134">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="5232e-135">表示要创建的会议取消。</span><span class="sxs-lookup"><span data-stu-id="5232e-135">Represents a meeting cancellation to create.</span></span>  <br/> |
|[<span data-ttu-id="5232e-136">任务</span><span class="sxs-lookup"><span data-stu-id="5232e-136">Task</span></span>](task.md) <br/> |<span data-ttu-id="5232e-137">表示要创建的任务。</span><span class="sxs-lookup"><span data-stu-id="5232e-137">Represents a task to create.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5232e-138">父元素</span><span class="sxs-lookup"><span data-stu-id="5232e-138">Parent elements</span></span>

|<span data-ttu-id="5232e-139">**元素**</span><span class="sxs-lookup"><span data-stu-id="5232e-139">**Element**</span></span>|<span data-ttu-id="5232e-140">**说明**</span><span class="sxs-lookup"><span data-stu-id="5232e-140">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5232e-141">更改（项目）</span><span class="sxs-lookup"><span data-stu-id="5232e-141">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="5232e-142">包含更改类型的序列数组，这些类型表示客户端上的项与 Exchange 服务器上的项之间的差异类型。</span><span class="sxs-lookup"><span data-stu-id="5232e-142">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5232e-143">说明</span><span class="sxs-lookup"><span data-stu-id="5232e-143">Remarks</span></span>

<span data-ttu-id="5232e-144">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5232e-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5232e-145">元素信息</span><span class="sxs-lookup"><span data-stu-id="5232e-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5232e-146">命名空间</span><span class="sxs-lookup"><span data-stu-id="5232e-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5232e-147">架构名称</span><span class="sxs-lookup"><span data-stu-id="5232e-147">Schema name</span></span>  <br/> |<span data-ttu-id="5232e-148">类型架构</span><span class="sxs-lookup"><span data-stu-id="5232e-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="5232e-149">验证文件</span><span class="sxs-lookup"><span data-stu-id="5232e-149">Validation file</span></span>  <br/> |<span data-ttu-id="5232e-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5232e-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5232e-151">可以为空</span><span class="sxs-lookup"><span data-stu-id="5232e-151">Can be empty</span></span>  <br/> |<span data-ttu-id="5232e-152">False</span><span class="sxs-lookup"><span data-stu-id="5232e-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5232e-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5232e-153">See also</span></span>

- [<span data-ttu-id="5232e-154">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="5232e-154">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="5232e-155">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5232e-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

