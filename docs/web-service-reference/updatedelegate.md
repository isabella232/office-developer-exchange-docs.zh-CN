---
title: UpdateDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateDelegate
api_type:
- schema
ms.assetid: c6ae99c4-18b0-4136-90ab-12cf15e15f91
description: UpdateDelegate 元素定义一个请求来更新邮箱中的代理人。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 32322e48acfa5f1058786162565a185a3e565d6e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838366"
---
# <a name="updatedelegate"></a><span data-ttu-id="b660f-104">UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="b660f-104">UpdateDelegate</span></span>

<span data-ttu-id="b660f-105">**UpdateDelegate**元素定义一个请求来更新邮箱中的代理人。</span><span class="sxs-lookup"><span data-stu-id="b660f-105">The **UpdateDelegate** element defines a request to update delegates in a mailbox.</span></span> <span data-ttu-id="b660f-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b660f-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UpdateDelegate>
      <DelegateUsers/>
   <DeliverMeetingRequests/>
      <Mailbox/>
</UpdateDelegate>
```

 <span data-ttu-id="b660f-107">**UpdateDelegateType**</span><span class="sxs-lookup"><span data-stu-id="b660f-107">**UpdateDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b660f-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b660f-108">Attributes and elements</span></span>

<span data-ttu-id="b660f-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b660f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b660f-110">属性</span><span class="sxs-lookup"><span data-stu-id="b660f-110">Attributes</span></span>

<span data-ttu-id="b660f-111">无。</span><span class="sxs-lookup"><span data-stu-id="b660f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b660f-112">子元素</span><span class="sxs-lookup"><span data-stu-id="b660f-112">Child elements</span></span>

|<span data-ttu-id="b660f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="b660f-113">**Element**</span></span>|<span data-ttu-id="b660f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="b660f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b660f-115">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="b660f-115">DelegateUsers</span></span>](delegateusers.md) <br/> |<span data-ttu-id="b660f-116">包含标识代理人和更新将应用于代理人的[DelegateUser](delegateuser.md)元素的数组。</span><span class="sxs-lookup"><span data-stu-id="b660f-116">Contains an array of [DelegateUser](delegateuser.md) elements that identify the delegates and the updates to apply to the delegates.</span></span> <span data-ttu-id="b660f-117">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b660f-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="b660f-118">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="b660f-118">DeliverMeetingRequests</span></span>](delivermeetingrequests.md) <br/> |<span data-ttu-id="b660f-119">定义委托和主体之间确定如何处理会议请求。</span><span class="sxs-lookup"><span data-stu-id="b660f-119">Defines how meeting requests are handled between the delegate and the principal.</span></span> <span data-ttu-id="b660f-120">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b660f-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="b660f-121">Mailbox</span><span class="sxs-lookup"><span data-stu-id="b660f-121">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="b660f-122">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="b660f-122">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b660f-123">父元素</span><span class="sxs-lookup"><span data-stu-id="b660f-123">Parent elements</span></span>

<span data-ttu-id="b660f-124">无。</span><span class="sxs-lookup"><span data-stu-id="b660f-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b660f-125">备注</span><span class="sxs-lookup"><span data-stu-id="b660f-125">Remarks</span></span>

<span data-ttu-id="b660f-126">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b660f-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b660f-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="b660f-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b660f-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="b660f-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b660f-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="b660f-129">Schema Name</span></span>  <br/> |<span data-ttu-id="b660f-130">消息架构</span><span class="sxs-lookup"><span data-stu-id="b660f-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b660f-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="b660f-131">Validation File</span></span>  <br/> |<span data-ttu-id="b660f-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b660f-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b660f-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="b660f-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="b660f-134">False</span><span class="sxs-lookup"><span data-stu-id="b660f-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b660f-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b660f-135">See also</span></span>



[<span data-ttu-id="b660f-136">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="b660f-136">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="b660f-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b660f-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

