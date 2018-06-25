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
description: AddDelegate 元素定义添加到邮箱代理人的请求。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: d1cb0ff3ea68904bf88e346f68afe7c349ae4394
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753110"
---
# <a name="adddelegate"></a><span data-ttu-id="5d956-104">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="5d956-104">AddDelegate</span></span>

<span data-ttu-id="5d956-105">**AddDelegate**元素定义添加到邮箱代理人的请求。</span><span class="sxs-lookup"><span data-stu-id="5d956-105">The **AddDelegate** element defines a request to add delegates to a mailbox.</span></span> <span data-ttu-id="5d956-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5d956-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<AddDelegate>
   <DelegateUsers/>
   <DeliverMeetingRequests/>
   <Mailbox/>
</AddDelegate>
```

 <span data-ttu-id="5d956-107">**AddDelegateType**</span><span class="sxs-lookup"><span data-stu-id="5d956-107">**AddDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5d956-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5d956-108">Attributes and elements</span></span>

<span data-ttu-id="5d956-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5d956-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5d956-110">属性</span><span class="sxs-lookup"><span data-stu-id="5d956-110">Attributes</span></span>

<span data-ttu-id="5d956-111">无。</span><span class="sxs-lookup"><span data-stu-id="5d956-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5d956-112">子元素</span><span class="sxs-lookup"><span data-stu-id="5d956-112">Child elements</span></span>

|<span data-ttu-id="5d956-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="5d956-113">**Element**</span></span>|<span data-ttu-id="5d956-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="5d956-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d956-115">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="5d956-115">DelegateUsers</span></span>](delegateusers.md) <br/> |<span data-ttu-id="5d956-116">包含代理人来添加或更新的邮箱中的标识。</span><span class="sxs-lookup"><span data-stu-id="5d956-116">Contains the identities of delegates to add to or update in a mailbox.</span></span> <span data-ttu-id="5d956-117">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5d956-117">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="5d956-118">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="5d956-118">DeliverMeetingRequests</span></span>](delivermeetingrequests.md) <br/> |<span data-ttu-id="5d956-119">定义委托和主体之间确定如何处理会议请求。</span><span class="sxs-lookup"><span data-stu-id="5d956-119">Defines how meeting requests are handled between the delegate and the principal.</span></span> <span data-ttu-id="5d956-120">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5d956-120">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="5d956-121">Mailbox</span><span class="sxs-lookup"><span data-stu-id="5d956-121">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="5d956-122">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="5d956-122">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5d956-123">父元素</span><span class="sxs-lookup"><span data-stu-id="5d956-123">Parent elements</span></span>

<span data-ttu-id="5d956-124">无。</span><span class="sxs-lookup"><span data-stu-id="5d956-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5d956-125">备注</span><span class="sxs-lookup"><span data-stu-id="5d956-125">Remarks</span></span>

<span data-ttu-id="5d956-126">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5d956-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5d956-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="5d956-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d956-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="5d956-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5d956-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="5d956-129">Schema Name</span></span>  <br/> |<span data-ttu-id="5d956-130">消息架构</span><span class="sxs-lookup"><span data-stu-id="5d956-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5d956-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="5d956-131">Validation File</span></span>  <br/> |<span data-ttu-id="5d956-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5d956-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5d956-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="5d956-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="5d956-134">False</span><span class="sxs-lookup"><span data-stu-id="5d956-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5d956-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5d956-135">See also</span></span>

- [<span data-ttu-id="5d956-136">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="5d956-136">AddDelegate operation</span></span>](adddelegate-operation.md)
- [<span data-ttu-id="5d956-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5d956-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="5d956-138">添加代理人</span><span class="sxs-lookup"><span data-stu-id="5d956-138">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

