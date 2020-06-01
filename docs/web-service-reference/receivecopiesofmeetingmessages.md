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
description: ReceiveCopiesOfMeetingMessages 元素指示代理是否接收发往主体的与会议相关的邮件的副本。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: af6e220304f88c4db00ab675077dcd9bf581ea9e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468262"
---
# <a name="receivecopiesofmeetingmessages"></a><span data-ttu-id="b7cbc-104">ReceiveCopiesOfMeetingMessages</span><span class="sxs-lookup"><span data-stu-id="b7cbc-104">ReceiveCopiesOfMeetingMessages</span></span>

<span data-ttu-id="b7cbc-105">**ReceiveCopiesOfMeetingMessages**元素指示代理是否接收发往主体的与会议相关的邮件的副本。</span><span class="sxs-lookup"><span data-stu-id="b7cbc-105">The **ReceiveCopiesOfMeetingMessages** element indicates whether a delegate receives copies of meeting-related messages that are addressed to the principal.</span></span> <span data-ttu-id="b7cbc-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b7cbc-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ReceiveCopiesOfMeetingMessages>true or false</ReceiveCopiesOfMeetingMessages>
```

 <span data-ttu-id="b7cbc-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b7cbc-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b7cbc-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b7cbc-108">Attributes and elements</span></span>

<span data-ttu-id="b7cbc-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b7cbc-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7cbc-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="b7cbc-110">Attributes</span></span>

<span data-ttu-id="b7cbc-111">无。</span><span class="sxs-lookup"><span data-stu-id="b7cbc-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b7cbc-112">子元素</span><span class="sxs-lookup"><span data-stu-id="b7cbc-112">Child elements</span></span>

<span data-ttu-id="b7cbc-113">无。</span><span class="sxs-lookup"><span data-stu-id="b7cbc-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b7cbc-114">父元素</span><span class="sxs-lookup"><span data-stu-id="b7cbc-114">Parent elements</span></span>

|<span data-ttu-id="b7cbc-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="b7cbc-115">**Element**</span></span>|<span data-ttu-id="b7cbc-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="b7cbc-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7cbc-117">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="b7cbc-117">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="b7cbc-118">标识要在邮箱中添加或更新的单个代理。</span><span class="sxs-lookup"><span data-stu-id="b7cbc-118">Identifies a single delegate to add or update in a mailbox.</span></span> <span data-ttu-id="b7cbc-119">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b7cbc-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b7cbc-120">文本值</span><span class="sxs-lookup"><span data-stu-id="b7cbc-120">Text value</span></span>

<span data-ttu-id="b7cbc-121">如果文本值为**true，则**表示代理将接收会议邮件的副本。</span><span class="sxs-lookup"><span data-stu-id="b7cbc-121">A text value of **true** indicates that a delegate receives a copy of meeting messages.</span></span> <span data-ttu-id="b7cbc-122">如果文本值为**false** ，则表示代理不会收到会议邮件的副本。</span><span class="sxs-lookup"><span data-stu-id="b7cbc-122">A text value of **false** indicates that a delegate does not receive a copy of meeting messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b7cbc-123">备注</span><span class="sxs-lookup"><span data-stu-id="b7cbc-123">Remarks</span></span>

<span data-ttu-id="b7cbc-124">当**ReceiveCopiesOfMeetingMessages**设置为**false**时，代理仍可以代表主体发送邮件，但不会收到任何与会议相关的邮件。</span><span class="sxs-lookup"><span data-stu-id="b7cbc-124">When **ReceiveCopiesOfMeetingMessages** is set to **false**, the delegate can still send message on behalf of the principal, but will not receive any meeting-related messages.</span></span>
  
<span data-ttu-id="b7cbc-125">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b7cbc-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7cbc-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="b7cbc-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7cbc-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="b7cbc-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b7cbc-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="b7cbc-128">Schema Name</span></span>  <br/> |<span data-ttu-id="b7cbc-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="b7cbc-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="b7cbc-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="b7cbc-130">Validation File</span></span>  <br/> |<span data-ttu-id="b7cbc-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b7cbc-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b7cbc-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="b7cbc-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="b7cbc-133">False</span><span class="sxs-lookup"><span data-stu-id="b7cbc-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7cbc-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b7cbc-134">See also</span></span>



[<span data-ttu-id="b7cbc-135">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="b7cbc-135">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="b7cbc-136">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="b7cbc-136">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="b7cbc-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b7cbc-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="b7cbc-138">添加委派</span><span class="sxs-lookup"><span data-stu-id="b7cbc-138">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

