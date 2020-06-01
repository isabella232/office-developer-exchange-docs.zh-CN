---
title: DeliverMeetingRequests
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeliverMeetingRequests
api_type:
- schema
ms.assetid: 04b999af-0b27-4e6d-a8b1-400955a1afaa
description: DeliverMeetingRequests 元素定义如何在代理和主体之间处理会议请求。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 3998443613437bca2267678f7bc2c5584b779135
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463676"
---
# <a name="delivermeetingrequests"></a><span data-ttu-id="e3d55-104">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="e3d55-104">DeliverMeetingRequests</span></span>

<span data-ttu-id="e3d55-105">**DeliverMeetingRequests**元素定义如何在代理和主体之间处理会议请求。</span><span class="sxs-lookup"><span data-stu-id="e3d55-105">The **DeliverMeetingRequests** element defines how meeting requests are handled between the delegate and the principal.</span></span> <span data-ttu-id="e3d55-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e3d55-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```XML
<DeliverMeetingRequests>DelegatesOnly or DelegatesAndMe or DelegatesAndSendInformationToMe or NoForward</DeliverMeetingRequests>
```

 <span data-ttu-id="e3d55-107">**DeliverMeetingRequestsType**</span><span class="sxs-lookup"><span data-stu-id="e3d55-107">**DeliverMeetingRequestsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e3d55-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e3d55-108">Attributes and elements</span></span>

<span data-ttu-id="e3d55-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e3d55-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3d55-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="e3d55-110">Attributes</span></span>

<span data-ttu-id="e3d55-111">无。</span><span class="sxs-lookup"><span data-stu-id="e3d55-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e3d55-112">子元素</span><span class="sxs-lookup"><span data-stu-id="e3d55-112">Child elements</span></span>

<span data-ttu-id="e3d55-113">无。</span><span class="sxs-lookup"><span data-stu-id="e3d55-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e3d55-114">父元素</span><span class="sxs-lookup"><span data-stu-id="e3d55-114">Parent elements</span></span>

|<span data-ttu-id="e3d55-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="e3d55-115">**Element**</span></span>|<span data-ttu-id="e3d55-116">**描述**</span><span class="sxs-lookup"><span data-stu-id="e3d55-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3d55-117">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="e3d55-117">AddDelegate</span></span>](adddelegate.md) <br/> |<span data-ttu-id="e3d55-118">定义请求以将代理人添加到邮箱。</span><span class="sxs-lookup"><span data-stu-id="e3d55-118">Defines a request to add delegates to a mailbox.</span></span> <span data-ttu-id="e3d55-119">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e3d55-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e3d55-120">UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="e3d55-120">UpdateDelegate</span></span>](updatedelegate.md) <br/> |<span data-ttu-id="e3d55-121">定义请求以更新邮箱中的代理人。</span><span class="sxs-lookup"><span data-stu-id="e3d55-121">Defines a request to update delegates in a mailbox.</span></span> <span data-ttu-id="e3d55-122">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e3d55-122">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="e3d55-123">GetDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="e3d55-123">GetDelegateResponse</span></span>](getdelegateresponse.md) <br/> |<span data-ttu-id="e3d55-124">包含 GetDelegate 请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="e3d55-124">Contains the status and result of a GetDelegate request.</span></span> <span data-ttu-id="e3d55-125">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e3d55-125">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e3d55-126">文本值</span><span class="sxs-lookup"><span data-stu-id="e3d55-126">Text value</span></span>

<span data-ttu-id="e3d55-127">下表列出了**DeliverMeetingRequests**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="e3d55-127">The following table lists the possible values for the **DeliverMeetingRequests** element.</span></span> 
  
<span data-ttu-id="e3d55-128">**DeliverMeetingRequests 元素值**</span><span class="sxs-lookup"><span data-stu-id="e3d55-128">**DeliverMeetingRequests element values**</span></span>

|<span data-ttu-id="e3d55-129">**值**</span><span class="sxs-lookup"><span data-stu-id="e3d55-129">**Value**</span></span>|<span data-ttu-id="e3d55-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="e3d55-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e3d55-131">DelegatesOnly</span><span class="sxs-lookup"><span data-stu-id="e3d55-131">DelegatesOnly</span></span>  <br/> |<span data-ttu-id="e3d55-132">将会议请求转发到代理并移动到主体邮箱中的 "已删除邮件" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="e3d55-132">Meeting requests are forwarded to the delegate and moved to the Deleted Items folder in the principal's mailbox.</span></span>  <br/> |
|<span data-ttu-id="e3d55-133">DelegatesAndMe</span><span class="sxs-lookup"><span data-stu-id="e3d55-133">DelegatesAndMe</span></span>  <br/> |<span data-ttu-id="e3d55-134">会议请求将转发给代理，并保留在主体邮箱的 "收件箱" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="e3d55-134">Meeting requests are forwarded to the delegate and remain in the Inbox folder in the principal's mailbox.</span></span>  <br/> |
|<span data-ttu-id="e3d55-135">DelegatesAndSendInformationToMe</span><span class="sxs-lookup"><span data-stu-id="e3d55-135">DelegatesAndSendInformationToMe</span></span>  <br/> |<span data-ttu-id="e3d55-136">会议请求将转发给代理，并保留在主体邮箱的 "收件箱" 文件夹中，但 "接受"、"暂定" 和 "拒绝" 按钮不会显示在 Microsoft Office Outlook 阅读窗格中。</span><span class="sxs-lookup"><span data-stu-id="e3d55-136">Meeting requests are forwarded to the delegate and remain in the Inbox folder in the principal's mailbox, but the Accept, Tentative, and Decline buttons do not appear in the Microsoft Office Outlook reading pane.</span></span>  <br/> |
|<span data-ttu-id="e3d55-137">NoForward</span><span class="sxs-lookup"><span data-stu-id="e3d55-137">NoForward</span></span>  <br/> |<span data-ttu-id="e3d55-138">不会将会议请求转发给代理。</span><span class="sxs-lookup"><span data-stu-id="e3d55-138">Meeting requests are not forwarded to the delegate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3d55-139">备注</span><span class="sxs-lookup"><span data-stu-id="e3d55-139">Remarks</span></span>

<span data-ttu-id="e3d55-140">**DeliverMeetingRequests**设置影响主体邮箱中的所有委派。</span><span class="sxs-lookup"><span data-stu-id="e3d55-140">The **DeliverMeetingRequests** setting affects all delegates in a principal's mailbox.</span></span> 
  
<span data-ttu-id="e3d55-141">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e3d55-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e3d55-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="e3d55-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3d55-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="e3d55-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e3d55-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="e3d55-144">Schema Name</span></span>  <br/> |<span data-ttu-id="e3d55-145">消息架构</span><span class="sxs-lookup"><span data-stu-id="e3d55-145">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e3d55-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="e3d55-146">Validation File</span></span>  <br/> |<span data-ttu-id="e3d55-147">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e3d55-147">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e3d55-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="e3d55-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="e3d55-149">False</span><span class="sxs-lookup"><span data-stu-id="e3d55-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3d55-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e3d55-150">See also</span></span>

- [<span data-ttu-id="e3d55-151">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="e3d55-151">AddDelegate operation</span></span>](adddelegate-operation.md)  
- [<span data-ttu-id="e3d55-152">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="e3d55-152">UpdateDelegate operation</span></span>](updatedelegate-operation.md)  
- [<span data-ttu-id="e3d55-153">GetDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="e3d55-153">GetDelegate operation</span></span>](getdelegate-operation.md)
- [<span data-ttu-id="e3d55-154">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e3d55-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="e3d55-155">添加委派</span><span class="sxs-lookup"><span data-stu-id="e3d55-155">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

