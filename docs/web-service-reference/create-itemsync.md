---
title: 创建 (ItemSync)
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
ms.openlocfilehash: 39056bcaab3577b1b729421118a45571910922fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753621"
---
# <a name="create-itemsync"></a><span data-ttu-id="f08be-103">创建 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="f08be-103">Create (ItemSync)</span></span>

<span data-ttu-id="f08be-104">**创建**元素标识在本地客户端库中创建的单个项。</span><span class="sxs-lookup"><span data-stu-id="f08be-104">The **Create** element identifies a single item to create in the local client store.</span></span> 
  
[<span data-ttu-id="f08be-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="f08be-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
  
[<span data-ttu-id="f08be-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f08be-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="f08be-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f08be-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
  
[<span data-ttu-id="f08be-108">更改 （项）</span><span class="sxs-lookup"><span data-stu-id="f08be-108">Changes (Items)</span></span>](changes-items.md)
  
[<span data-ttu-id="f08be-109">创建 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="f08be-109">Create (ItemSync)</span></span>](create-itemsync.md)
  
```xml
<Create>
   <Item/>
</Create>
```

 <span data-ttu-id="f08be-110">**SyncFolderItemsCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="f08be-110">**SyncFolderItemsCreateOrUpdateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f08be-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f08be-111">Attributes and elements</span></span>

<span data-ttu-id="f08be-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f08be-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f08be-113">属性</span><span class="sxs-lookup"><span data-stu-id="f08be-113">Attributes</span></span>

<span data-ttu-id="f08be-114">无。</span><span class="sxs-lookup"><span data-stu-id="f08be-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f08be-115">子元素</span><span class="sxs-lookup"><span data-stu-id="f08be-115">Child elements</span></span>

|<span data-ttu-id="f08be-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="f08be-116">**Element**</span></span>|<span data-ttu-id="f08be-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f08be-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f08be-118">Item</span><span class="sxs-lookup"><span data-stu-id="f08be-118">Item</span></span>](item.md) <br/> |<span data-ttu-id="f08be-119">表示要创建的泛型 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="f08be-119">Represents a generic Exchange item to create.</span></span>  <br/> |
|[<span data-ttu-id="f08be-120">Message</span><span class="sxs-lookup"><span data-stu-id="f08be-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f08be-121">代表要创建 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="f08be-121">Represents an Exchange e-mail message to create.</span></span>  <br/> |
|[<span data-ttu-id="f08be-122">日历项目</span><span class="sxs-lookup"><span data-stu-id="f08be-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="f08be-123">表示要创建 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="f08be-123">Represents an Exchange calendar item to create.</span></span>  <br/> |
|[<span data-ttu-id="f08be-124">Contact</span><span class="sxs-lookup"><span data-stu-id="f08be-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="f08be-125">表示要创建 Exchange 联系人项。</span><span class="sxs-lookup"><span data-stu-id="f08be-125">Represents an Exchange contact item to create.</span></span>  <br/> |
|[<span data-ttu-id="f08be-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="f08be-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="f08be-127">代表创建的通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="f08be-127">Represents a distribution list to create.</span></span>  <br/> |
|[<span data-ttu-id="f08be-128">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="f08be-128">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="f08be-129">代表要创建的会议消息。</span><span class="sxs-lookup"><span data-stu-id="f08be-129">Represents a meeting message to create.</span></span>  <br/> |
|[<span data-ttu-id="f08be-130">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="f08be-130">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="f08be-131">表示要创建的会议请求。</span><span class="sxs-lookup"><span data-stu-id="f08be-131">Represents a meeting request to create.</span></span>  <br/> |
|[<span data-ttu-id="f08be-132">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="f08be-132">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="f08be-133">代表要创建的会议响应。</span><span class="sxs-lookup"><span data-stu-id="f08be-133">Represents a meeting response to create.</span></span>  <br/> |
|[<span data-ttu-id="f08be-134">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="f08be-134">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="f08be-135">代表取消会议创建。</span><span class="sxs-lookup"><span data-stu-id="f08be-135">Represents a meeting cancellation to create.</span></span>  <br/> |
|[<span data-ttu-id="f08be-136">任务</span><span class="sxs-lookup"><span data-stu-id="f08be-136">Task</span></span>](task.md) <br/> |<span data-ttu-id="f08be-137">代表要创建的任务。</span><span class="sxs-lookup"><span data-stu-id="f08be-137">Represents a task to create.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f08be-138">父元素</span><span class="sxs-lookup"><span data-stu-id="f08be-138">Parent elements</span></span>

|<span data-ttu-id="f08be-139">**元素**</span><span class="sxs-lookup"><span data-stu-id="f08be-139">**Element**</span></span>|<span data-ttu-id="f08be-140">**说明**</span><span class="sxs-lookup"><span data-stu-id="f08be-140">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f08be-141">更改 （项）</span><span class="sxs-lookup"><span data-stu-id="f08be-141">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="f08be-142">包含表示客户端上的项目和 Exchange 服务器上的项目之间的差异的类型的更改类型序列数组。</span><span class="sxs-lookup"><span data-stu-id="f08be-142">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f08be-143">备注</span><span class="sxs-lookup"><span data-stu-id="f08be-143">Remarks</span></span>

<span data-ttu-id="f08be-144">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f08be-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f08be-145">元素信息</span><span class="sxs-lookup"><span data-stu-id="f08be-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f08be-146">命名空间</span><span class="sxs-lookup"><span data-stu-id="f08be-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f08be-147">架构名称</span><span class="sxs-lookup"><span data-stu-id="f08be-147">Schema name</span></span>  <br/> |<span data-ttu-id="f08be-148">类型架构</span><span class="sxs-lookup"><span data-stu-id="f08be-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="f08be-149">验证文件</span><span class="sxs-lookup"><span data-stu-id="f08be-149">Validation file</span></span>  <br/> |<span data-ttu-id="f08be-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f08be-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f08be-151">可以为空</span><span class="sxs-lookup"><span data-stu-id="f08be-151">Can be empty</span></span>  <br/> |<span data-ttu-id="f08be-152">False</span><span class="sxs-lookup"><span data-stu-id="f08be-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f08be-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f08be-153">See also</span></span>



[<span data-ttu-id="f08be-154">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="f08be-154">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="f08be-155">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f08be-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

