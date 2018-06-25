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
description: DeliverMeetingRequests 元素定义委托和主体之间确定如何处理会议请求。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 803bd2da72bdb21b507a59cc11635a40d4431acf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753831"
---
# <a name="delivermeetingrequests"></a><span data-ttu-id="bc20e-104">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="bc20e-104">DeliverMeetingRequests</span></span>

<span data-ttu-id="bc20e-105">**DeliverMeetingRequests**元素定义委托和主体之间确定如何处理会议请求。</span><span class="sxs-lookup"><span data-stu-id="bc20e-105">The **DeliverMeetingRequests** element defines how meeting requests are handled between the delegate and the principal.</span></span> <span data-ttu-id="bc20e-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="bc20e-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```XML
<DeliverMeetingRequests>DelegatesOnly or DelegatesAndMe or DelegatesAndSendInformationToMe or NoForward</DeliverMeetingRequests>
```

 <span data-ttu-id="bc20e-107">**DeliverMeetingRequestsType**</span><span class="sxs-lookup"><span data-stu-id="bc20e-107">**DeliverMeetingRequestsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bc20e-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bc20e-108">Attributes and elements</span></span>

<span data-ttu-id="bc20e-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bc20e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bc20e-110">属性</span><span class="sxs-lookup"><span data-stu-id="bc20e-110">Attributes</span></span>

<span data-ttu-id="bc20e-111">无。</span><span class="sxs-lookup"><span data-stu-id="bc20e-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bc20e-112">子元素</span><span class="sxs-lookup"><span data-stu-id="bc20e-112">Child elements</span></span>

<span data-ttu-id="bc20e-113">无。</span><span class="sxs-lookup"><span data-stu-id="bc20e-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bc20e-114">父元素</span><span class="sxs-lookup"><span data-stu-id="bc20e-114">Parent elements</span></span>

|<span data-ttu-id="bc20e-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="bc20e-115">**Element**</span></span>|<span data-ttu-id="bc20e-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="bc20e-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bc20e-117">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="bc20e-117">AddDelegate</span></span>](adddelegate.md) <br/> |<span data-ttu-id="bc20e-118">定义请求以将代理人添加到邮箱。</span><span class="sxs-lookup"><span data-stu-id="bc20e-118">Defines a request to add delegates to a mailbox.</span></span> <span data-ttu-id="bc20e-119">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="bc20e-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="bc20e-120">UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="bc20e-120">UpdateDelegate</span></span>](updatedelegate.md) <br/> |<span data-ttu-id="bc20e-121">定义请求以更新邮箱中的代理人。</span><span class="sxs-lookup"><span data-stu-id="bc20e-121">Defines a request to update delegates in a mailbox.</span></span> <span data-ttu-id="bc20e-122">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="bc20e-122">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="bc20e-123">GetDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="bc20e-123">GetDelegateResponse</span></span>](getdelegateresponse.md) <br/> |<span data-ttu-id="bc20e-124">包含状态和 GetDelegate 请求的结果。</span><span class="sxs-lookup"><span data-stu-id="bc20e-124">Contains the status and result of a GetDelegate request.</span></span> <span data-ttu-id="bc20e-125">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="bc20e-125">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bc20e-126">文本值</span><span class="sxs-lookup"><span data-stu-id="bc20e-126">Text value</span></span>

<span data-ttu-id="bc20e-127">下表列出了**DeliverMeetingRequests**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="bc20e-127">The following table lists the possible values for the **DeliverMeetingRequests** element.</span></span> 
  
<span data-ttu-id="bc20e-128">**DeliverMeetingRequests 元素的值**</span><span class="sxs-lookup"><span data-stu-id="bc20e-128">**DeliverMeetingRequests element values**</span></span>

|<span data-ttu-id="bc20e-129">**值**</span><span class="sxs-lookup"><span data-stu-id="bc20e-129">**Value**</span></span>|<span data-ttu-id="bc20e-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="bc20e-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bc20e-131">DelegatesOnly</span><span class="sxs-lookup"><span data-stu-id="bc20e-131">DelegatesOnly</span></span>  <br/> |<span data-ttu-id="bc20e-132">会议请求的转发到委派和移动到的主体的邮箱中的已删除邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="bc20e-132">Meeting requests are forwarded to the delegate and moved to the Deleted Items folder in the principal's mailbox.</span></span>  <br/> |
|<span data-ttu-id="bc20e-133">DelegatesAndMe</span><span class="sxs-lookup"><span data-stu-id="bc20e-133">DelegatesAndMe</span></span>  <br/> |<span data-ttu-id="bc20e-134">会议请求转发到委派和保留在的主体的邮箱中收件箱文件夹中。</span><span class="sxs-lookup"><span data-stu-id="bc20e-134">Meeting requests are forwarded to the delegate and remain in the Inbox folder in the principal's mailbox.</span></span>  <br/> |
|<span data-ttu-id="bc20e-135">DelegatesAndSendInformationToMe</span><span class="sxs-lookup"><span data-stu-id="bc20e-135">DelegatesAndSendInformationToMe</span></span>  <br/> |<span data-ttu-id="bc20e-136">会议请求转发到委派和保留的收件箱文件夹中的主体的邮箱，但不是在 Microsoft Office Outlook 阅读窗格中显示接受、 暂定和拒绝按钮。</span><span class="sxs-lookup"><span data-stu-id="bc20e-136">Meeting requests are forwarded to the delegate and remain in the Inbox folder in the principal's mailbox, but the Accept, Tentative, and Decline buttons do not appear in the Microsoft Office Outlook reading pane.</span></span>  <br/> |
|<span data-ttu-id="bc20e-137">NoForward</span><span class="sxs-lookup"><span data-stu-id="bc20e-137">NoForward</span></span>  <br/> |<span data-ttu-id="bc20e-138">会议请求不转发到委派。</span><span class="sxs-lookup"><span data-stu-id="bc20e-138">Meeting requests are not forwarded to the delegate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc20e-139">注解</span><span class="sxs-lookup"><span data-stu-id="bc20e-139">Remarks</span></span>

<span data-ttu-id="bc20e-140">**DeliverMeetingRequests**设置会影响的主体的邮箱中的所有代理人。</span><span class="sxs-lookup"><span data-stu-id="bc20e-140">The **DeliverMeetingRequests** setting affects all delegates in a principal's mailbox.</span></span> 
  
<span data-ttu-id="bc20e-141">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bc20e-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bc20e-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="bc20e-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bc20e-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="bc20e-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bc20e-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="bc20e-144">Schema Name</span></span>  <br/> |<span data-ttu-id="bc20e-145">消息架构</span><span class="sxs-lookup"><span data-stu-id="bc20e-145">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bc20e-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="bc20e-146">Validation File</span></span>  <br/> |<span data-ttu-id="bc20e-147">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bc20e-147">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bc20e-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="bc20e-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="bc20e-149">False</span><span class="sxs-lookup"><span data-stu-id="bc20e-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bc20e-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bc20e-150">See also</span></span>

- [<span data-ttu-id="bc20e-151">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="bc20e-151">AddDelegate operation</span></span>](adddelegate-operation.md)  
- [<span data-ttu-id="bc20e-152">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="bc20e-152">UpdateDelegate operation</span></span>](updatedelegate-operation.md)  
- [<span data-ttu-id="bc20e-153">GetDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="bc20e-153">GetDelegate operation</span></span>](getdelegate-operation.md)
- [<span data-ttu-id="bc20e-154">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bc20e-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="bc20e-155">添加代理人</span><span class="sxs-lookup"><span data-stu-id="bc20e-155">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

