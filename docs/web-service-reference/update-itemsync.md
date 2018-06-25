---
title: 更新 (ItemSync)
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
description: 更新元素标识更新本地客户端存储中的单个项。
ms.openlocfilehash: ef1bd46906152affbe54372472766afc2a6ae8c1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838363"
---
# <a name="update-itemsync"></a><span data-ttu-id="c7458-103">更新 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="c7458-103">Update (ItemSync)</span></span>

<span data-ttu-id="c7458-104">**更新**元素标识更新本地客户端存储中的单个项。</span><span class="sxs-lookup"><span data-stu-id="c7458-104">The **Update** element identifies a single item to update in the local client store.</span></span> 
  
[<span data-ttu-id="c7458-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="c7458-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
  
[<span data-ttu-id="c7458-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c7458-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="c7458-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c7458-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
  
[<span data-ttu-id="c7458-108">更改 （项）</span><span class="sxs-lookup"><span data-stu-id="c7458-108">Changes (Items)</span></span>](changes-items.md)
  
[<span data-ttu-id="c7458-109">更新 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="c7458-109">Update (ItemSync)</span></span>](update-itemsync.md)
  
```xml
<Update>
   <Item/>
</Update>
```

 <span data-ttu-id="c7458-110">**SyncFolderItemsCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="c7458-110">**SyncFolderItemsCreateOrUpdateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c7458-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c7458-111">Attributes and elements</span></span>

<span data-ttu-id="c7458-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c7458-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7458-113">属性</span><span class="sxs-lookup"><span data-stu-id="c7458-113">Attributes</span></span>

<span data-ttu-id="c7458-114">无。</span><span class="sxs-lookup"><span data-stu-id="c7458-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c7458-115">子元素</span><span class="sxs-lookup"><span data-stu-id="c7458-115">Child elements</span></span>

|<span data-ttu-id="c7458-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="c7458-116">**Element**</span></span>|<span data-ttu-id="c7458-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="c7458-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7458-118">Item</span><span class="sxs-lookup"><span data-stu-id="c7458-118">Item</span></span>](item.md) <br/> |<span data-ttu-id="c7458-119">代表要更新的泛型 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="c7458-119">Represents a generic Exchange item to update.</span></span>  <br/> |
|[<span data-ttu-id="c7458-120">Message</span><span class="sxs-lookup"><span data-stu-id="c7458-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c7458-121">代表要更新 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="c7458-121">Represents an Exchange e-mail message to update.</span></span>  <br/> |
|[<span data-ttu-id="c7458-122">日历项目</span><span class="sxs-lookup"><span data-stu-id="c7458-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="c7458-123">代表要更新 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="c7458-123">Represents an Exchange calendar item to update.</span></span>  <br/> |
|[<span data-ttu-id="c7458-124">Contact</span><span class="sxs-lookup"><span data-stu-id="c7458-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="c7458-125">代表要更新 Exchange 联系人项。</span><span class="sxs-lookup"><span data-stu-id="c7458-125">Represents an Exchange contact item to update.</span></span>  <br/> |
|[<span data-ttu-id="c7458-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="c7458-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="c7458-127">代表要更新的通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="c7458-127">Represents a distribution list to update.</span></span>  <br/> |
|[<span data-ttu-id="c7458-128">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="c7458-128">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="c7458-129">代表要更新的会议消息。</span><span class="sxs-lookup"><span data-stu-id="c7458-129">Represents a meeting message to update.</span></span>  <br/> |
|[<span data-ttu-id="c7458-130">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="c7458-130">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="c7458-131">表示要更新的会议请求。</span><span class="sxs-lookup"><span data-stu-id="c7458-131">Represents a meeting request to update.</span></span>  <br/> |
|[<span data-ttu-id="c7458-132">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="c7458-132">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="c7458-133">代表要更新的会议响应。</span><span class="sxs-lookup"><span data-stu-id="c7458-133">Represents a meeting response to update.</span></span>  <br/> |
|[<span data-ttu-id="c7458-134">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="c7458-134">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="c7458-135">代表要更新会议取消。</span><span class="sxs-lookup"><span data-stu-id="c7458-135">Represents a meeting cancellation to update.</span></span>  <br/> |
|[<span data-ttu-id="c7458-136">任务</span><span class="sxs-lookup"><span data-stu-id="c7458-136">Task</span></span>](task.md) <br/> |<span data-ttu-id="c7458-137">代表要更新的任务。</span><span class="sxs-lookup"><span data-stu-id="c7458-137">Represents a task to update.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c7458-138">父元素</span><span class="sxs-lookup"><span data-stu-id="c7458-138">Parent elements</span></span>

|<span data-ttu-id="c7458-139">**元素**</span><span class="sxs-lookup"><span data-stu-id="c7458-139">**Element**</span></span>|<span data-ttu-id="c7458-140">**说明**</span><span class="sxs-lookup"><span data-stu-id="c7458-140">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7458-141">更改 （项）</span><span class="sxs-lookup"><span data-stu-id="c7458-141">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="c7458-142">包含表示的客户端上的项目和 Exchange 服务器上的项目之间的差异的类型的更改类型序列数组。</span><span class="sxs-lookup"><span data-stu-id="c7458-142">Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7458-143">备注</span><span class="sxs-lookup"><span data-stu-id="c7458-143">Remarks</span></span>

<span data-ttu-id="c7458-144">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c7458-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c7458-145">元素信息</span><span class="sxs-lookup"><span data-stu-id="c7458-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7458-146">命名空间</span><span class="sxs-lookup"><span data-stu-id="c7458-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c7458-147">架构名称</span><span class="sxs-lookup"><span data-stu-id="c7458-147">Schema name</span></span>  <br/> |<span data-ttu-id="c7458-148">类型架构</span><span class="sxs-lookup"><span data-stu-id="c7458-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="c7458-149">验证文件</span><span class="sxs-lookup"><span data-stu-id="c7458-149">Validation file</span></span>  <br/> |<span data-ttu-id="c7458-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c7458-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c7458-151">可以为空</span><span class="sxs-lookup"><span data-stu-id="c7458-151">Can be empty</span></span>  <br/> |<span data-ttu-id="c7458-152">False</span><span class="sxs-lookup"><span data-stu-id="c7458-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7458-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c7458-153">See also</span></span>



[<span data-ttu-id="c7458-154">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="c7458-154">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="c7458-155">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c7458-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

