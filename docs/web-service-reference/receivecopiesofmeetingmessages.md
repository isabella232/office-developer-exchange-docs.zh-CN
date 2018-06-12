---
title: ReceiveCopiesOfMeetingMessages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReceiveCopiesOfMeetingMessages
api_type:
- schema
ms.assetid: 65217ca8-6aea-47eb-a989-e6cce25f5f09
description: ReceiveCopiesOfMeetingMessages 元素指示代理是否接收发往主体的会议相关邮件的副本。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: e39a5d3255268b418fa956959da5ae0ea062d831
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826967"
---
# <a name="receivecopiesofmeetingmessages"></a><span data-ttu-id="6f31a-104">ReceiveCopiesOfMeetingMessages</span><span class="sxs-lookup"><span data-stu-id="6f31a-104">ReceiveCopiesOfMeetingMessages</span></span>

<span data-ttu-id="6f31a-105">**ReceiveCopiesOfMeetingMessages**元素指示代理是否接收发往主体的会议相关邮件的副本。</span><span class="sxs-lookup"><span data-stu-id="6f31a-105">The **ReceiveCopiesOfMeetingMessages** element indicates whether a delegate receives copies of meeting-related messages that are addressed to the principal.</span></span> <span data-ttu-id="6f31a-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6f31a-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ReceiveCopiesOfMeetingMessages>true or false</ReceiveCopiesOfMeetingMessages>
```

 <span data-ttu-id="6f31a-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6f31a-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f31a-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6f31a-108">Attributes and elements</span></span>

<span data-ttu-id="6f31a-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6f31a-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f31a-110">属性</span><span class="sxs-lookup"><span data-stu-id="6f31a-110">Attributes</span></span>

<span data-ttu-id="6f31a-111">无。</span><span class="sxs-lookup"><span data-stu-id="6f31a-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f31a-112">子元素</span><span class="sxs-lookup"><span data-stu-id="6f31a-112">Child elements</span></span>

<span data-ttu-id="6f31a-113">无。</span><span class="sxs-lookup"><span data-stu-id="6f31a-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6f31a-114">父元素</span><span class="sxs-lookup"><span data-stu-id="6f31a-114">Parent elements</span></span>

|<span data-ttu-id="6f31a-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="6f31a-115">**Element**</span></span>|<span data-ttu-id="6f31a-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="6f31a-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f31a-117">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="6f31a-117">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="6f31a-118">标识要添加或更新的邮箱中的单个委托。</span><span class="sxs-lookup"><span data-stu-id="6f31a-118">Identifies a single delegate to add or update in a mailbox.</span></span> <span data-ttu-id="6f31a-119">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6f31a-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6f31a-120">文本值</span><span class="sxs-lookup"><span data-stu-id="6f31a-120">Text value</span></span>

<span data-ttu-id="6f31a-121">文本值为**true**指示代理接收会议邮件的副本。</span><span class="sxs-lookup"><span data-stu-id="6f31a-121">A text value of **true** indicates that a delegate receives a copy of meeting messages.</span></span> <span data-ttu-id="6f31a-122">文本值为**false**指示委托不会收到会议邮件的副本。</span><span class="sxs-lookup"><span data-stu-id="6f31a-122">A text value of **false** indicates that a delegate does not receive a copy of meeting messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6f31a-123">备注</span><span class="sxs-lookup"><span data-stu-id="6f31a-123">Remarks</span></span>

<span data-ttu-id="6f31a-124">当**ReceiveCopiesOfMeetingMessages**设置为**false**时，委托仍可以发送消息代表主体，但不是会收到任何与会议相关的消息。</span><span class="sxs-lookup"><span data-stu-id="6f31a-124">When **ReceiveCopiesOfMeetingMessages** is set to **false**, the delegate can still send message on behalf of the principal, but will not receive any meeting-related messages.</span></span>
  
<span data-ttu-id="6f31a-125">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6f31a-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f31a-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="6f31a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f31a-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="6f31a-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6f31a-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="6f31a-128">Schema Name</span></span>  <br/> |<span data-ttu-id="6f31a-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="6f31a-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="6f31a-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="6f31a-130">Validation File</span></span>  <br/> |<span data-ttu-id="6f31a-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6f31a-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6f31a-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="6f31a-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="6f31a-133">False</span><span class="sxs-lookup"><span data-stu-id="6f31a-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f31a-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6f31a-134">See also</span></span>



[<span data-ttu-id="6f31a-135">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="6f31a-135">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="6f31a-136">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="6f31a-136">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="6f31a-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6f31a-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="6f31a-138">添加代理人</span><span class="sxs-lookup"><span data-stu-id="6f31a-138">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

