---
title: AddDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AddDelegate
api_type:
- schema
ms.assetid: 646fb994-229e-4d90-8b95-6541191cb3ae
description: AddDelegate 元素定义将委派添加到邮箱的请求。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: a08b83ad6e114c194073716c82228ea20ae1d3b7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466498"
---
# <a name="adddelegate"></a><span data-ttu-id="372ad-104">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="372ad-104">AddDelegate</span></span>

<span data-ttu-id="372ad-105">**AddDelegate**元素定义将委派添加到邮箱的请求。</span><span class="sxs-lookup"><span data-stu-id="372ad-105">The **AddDelegate** element defines a request to add delegates to a mailbox.</span></span> <span data-ttu-id="372ad-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="372ad-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<AddDelegate>
   <DelegateUsers/>
   <DeliverMeetingRequests/>
   <Mailbox/>
</AddDelegate>
```

 <span data-ttu-id="372ad-107">**AddDelegateType**</span><span class="sxs-lookup"><span data-stu-id="372ad-107">**AddDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="372ad-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="372ad-108">Attributes and elements</span></span>

<span data-ttu-id="372ad-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="372ad-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="372ad-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="372ad-110">Attributes</span></span>

<span data-ttu-id="372ad-111">无。</span><span class="sxs-lookup"><span data-stu-id="372ad-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="372ad-112">子元素</span><span class="sxs-lookup"><span data-stu-id="372ad-112">Child elements</span></span>

|<span data-ttu-id="372ad-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="372ad-113">**Element**</span></span>|<span data-ttu-id="372ad-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="372ad-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="372ad-115">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="372ad-115">DelegateUsers</span></span>](delegateusers.md) <br/> |<span data-ttu-id="372ad-116">包含要添加到邮箱或在邮箱中更新的代理的标识。</span><span class="sxs-lookup"><span data-stu-id="372ad-116">Contains the identities of delegates to add to or update in a mailbox.</span></span> <span data-ttu-id="372ad-117">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="372ad-117">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="372ad-118">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="372ad-118">DeliverMeetingRequests</span></span>](delivermeetingrequests.md) <br/> |<span data-ttu-id="372ad-119">定义在委托和主体之间如何处理会议请求。</span><span class="sxs-lookup"><span data-stu-id="372ad-119">Defines how meeting requests are handled between the delegate and the principal.</span></span> <span data-ttu-id="372ad-120">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="372ad-120">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="372ad-121">Mailbox</span><span class="sxs-lookup"><span data-stu-id="372ad-121">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="372ad-122">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="372ad-122">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="372ad-123">父元素</span><span class="sxs-lookup"><span data-stu-id="372ad-123">Parent elements</span></span>

<span data-ttu-id="372ad-124">无。</span><span class="sxs-lookup"><span data-stu-id="372ad-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="372ad-125">说明</span><span class="sxs-lookup"><span data-stu-id="372ad-125">Remarks</span></span>

<span data-ttu-id="372ad-126">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="372ad-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="372ad-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="372ad-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="372ad-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="372ad-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="372ad-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="372ad-129">Schema Name</span></span>  <br/> |<span data-ttu-id="372ad-130">消息架构</span><span class="sxs-lookup"><span data-stu-id="372ad-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="372ad-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="372ad-131">Validation File</span></span>  <br/> |<span data-ttu-id="372ad-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="372ad-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="372ad-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="372ad-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="372ad-134">False</span><span class="sxs-lookup"><span data-stu-id="372ad-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="372ad-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="372ad-135">See also</span></span>

- [<span data-ttu-id="372ad-136">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="372ad-136">AddDelegate operation</span></span>](adddelegate-operation.md)
- [<span data-ttu-id="372ad-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="372ad-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="372ad-138">添加委派</span><span class="sxs-lookup"><span data-stu-id="372ad-138">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

