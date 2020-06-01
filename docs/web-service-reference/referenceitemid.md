---
title: ReferenceItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReferenceItemId
api_type:
- schema
ms.assetid: 8fd4bb12-a94b-43f5-be3b-f435684e311d
description: ReferenceItemId 元素标识 response 对象引用的项。
ms.openlocfilehash: 3b77d75de91af8ec8fb7ae2d507377d1d976febf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457226"
---
# <a name="referenceitemid"></a><span data-ttu-id="89d12-103">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="89d12-103">ReferenceItemId</span></span>

<span data-ttu-id="89d12-104">**ReferenceItemId**元素标识 response 对象引用的项。</span><span class="sxs-lookup"><span data-stu-id="89d12-104">The **ReferenceItemId** element identifies the item to which the response object refers.</span></span> 
  
```xml
<ReferenceItemId Id="" ChangeKey="" />
```

 <span data-ttu-id="89d12-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="89d12-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="89d12-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="89d12-106">Attributes and elements</span></span>

<span data-ttu-id="89d12-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="89d12-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="89d12-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="89d12-108">Attributes</span></span>

|<span data-ttu-id="89d12-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="89d12-109">**Attribute**</span></span>|<span data-ttu-id="89d12-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="89d12-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="89d12-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="89d12-111">**Id**</span></span> <br/> |<span data-ttu-id="89d12-112">标识 Exchange 存储中的特定项目。</span><span class="sxs-lookup"><span data-stu-id="89d12-112">Identifies a specific item in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="89d12-113">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="89d12-113">**ChangeKey**</span></span> <br/> |<span data-ttu-id="89d12-114">标识项目的特定版本。</span><span class="sxs-lookup"><span data-stu-id="89d12-114">Identifies a specific version of an item.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="89d12-115">子元素</span><span class="sxs-lookup"><span data-stu-id="89d12-115">Child elements</span></span>

<span data-ttu-id="89d12-116">无。</span><span class="sxs-lookup"><span data-stu-id="89d12-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="89d12-117">父元素</span><span class="sxs-lookup"><span data-stu-id="89d12-117">Parent elements</span></span>

|<span data-ttu-id="89d12-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="89d12-118">**Element**</span></span>|<span data-ttu-id="89d12-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="89d12-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89d12-120">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="89d12-120">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="89d12-121">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="89d12-121">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="89d12-122">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="89d12-122">AcceptSharingInvitation</span></span>](acceptsharinginvitation.md) <br/> |<span data-ttu-id="89d12-123">表示对共享邀请的接受答复。</span><span class="sxs-lookup"><span data-stu-id="89d12-123">Represents an Accept reply to a sharing invitation.</span></span>  <br/> |
|[<span data-ttu-id="89d12-124">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="89d12-124">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="89d12-125">表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="89d12-125">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="89d12-126">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="89d12-126">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="89d12-127">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="89d12-127">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="89d12-128">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="89d12-128">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="89d12-129">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="89d12-129">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="89d12-130">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="89d12-130">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="89d12-131">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="89d12-131">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="89d12-132">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="89d12-132">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="89d12-133">包含对所有确定收件人的 Exchange 存储中的项的答复。</span><span class="sxs-lookup"><span data-stu-id="89d12-133">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="89d12-134">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="89d12-134">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="89d12-135">包含对 Exchange 存储中的项的创建者的答复。</span><span class="sxs-lookup"><span data-stu-id="89d12-135">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="89d12-136">SuppressReadReceipt</span><span class="sxs-lookup"><span data-stu-id="89d12-136">SuppressReadReceipt</span></span>](suppressreadreceipt.md) <br/> |<span data-ttu-id="89d12-137">用于响应已读回执请求。</span><span class="sxs-lookup"><span data-stu-id="89d12-137">Used to respond to read receipt requests.</span></span>  <br/> |
|[<span data-ttu-id="89d12-138">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="89d12-138">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="89d12-139">表示一个暂定答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="89d12-139">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89d12-140">说明</span><span class="sxs-lookup"><span data-stu-id="89d12-140">Remarks</span></span>

<span data-ttu-id="89d12-141">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="89d12-141">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="89d12-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="89d12-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89d12-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="89d12-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="89d12-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="89d12-144">Schema Name</span></span>  <br/> |<span data-ttu-id="89d12-145">类型架构</span><span class="sxs-lookup"><span data-stu-id="89d12-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="89d12-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="89d12-146">Validation File</span></span>  <br/> |<span data-ttu-id="89d12-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="89d12-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="89d12-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="89d12-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="89d12-149">False</span><span class="sxs-lookup"><span data-stu-id="89d12-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89d12-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="89d12-150">See also</span></span>



- [<span data-ttu-id="89d12-151">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="89d12-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

