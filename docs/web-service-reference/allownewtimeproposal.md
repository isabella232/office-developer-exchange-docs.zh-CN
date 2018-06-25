---
title: AllowNewTimeProposal
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AllowNewTimeProposal
api_type:
- schema
ms.assetid: afdb4ec9-2daf-48a1-a0bb-a7f647f212f2
description: AllowNewTimeProposal 元素指示是否可以建议会议与会者的新的会议时间。
ms.openlocfilehash: d5deed5044769c477ffe54cc533d5261ba2e1932
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753137"
---
# <a name="allownewtimeproposal"></a><span data-ttu-id="2d478-103">AllowNewTimeProposal</span><span class="sxs-lookup"><span data-stu-id="2d478-103">AllowNewTimeProposal</span></span>

<span data-ttu-id="2d478-104">**AllowNewTimeProposal**元素指示是否可以建议会议与会者的新的会议时间。</span><span class="sxs-lookup"><span data-stu-id="2d478-104">The **AllowNewTimeProposal** element indicates whether a new meeting time can be proposed for a meeting by an attendee.</span></span> 
  
```xml
<AllowNewTimeProposal/>
```

 <span data-ttu-id="2d478-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2d478-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2d478-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2d478-106">Attributes and elements</span></span>

<span data-ttu-id="2d478-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2d478-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d478-108">属性</span><span class="sxs-lookup"><span data-stu-id="2d478-108">Attributes</span></span>

<span data-ttu-id="2d478-109">无</span><span class="sxs-lookup"><span data-stu-id="2d478-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2d478-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2d478-110">Child elements</span></span>

<span data-ttu-id="2d478-111">无。</span><span class="sxs-lookup"><span data-stu-id="2d478-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2d478-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2d478-112">Parent elements</span></span>

|<span data-ttu-id="2d478-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="2d478-113">**Element**</span></span>|<span data-ttu-id="2d478-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="2d478-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d478-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="2d478-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="2d478-116">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="2d478-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2d478-117">日历项目</span><span class="sxs-lookup"><span data-stu-id="2d478-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="2d478-118">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="2d478-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2d478-119">文本值</span><span class="sxs-lookup"><span data-stu-id="2d478-119">Text value</span></span>

<span data-ttu-id="2d478-120">表示一个布尔值的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="2d478-120">A text value that represents a Boolean value is required.</span></span> <span data-ttu-id="2d478-121">值为**true**指示可以创建新的会议时间的建议;如果值为**false**指示不允许建议新的时间。</span><span class="sxs-lookup"><span data-stu-id="2d478-121">A value of **true** indicates that a new proposal for the meeting time can be created; a value of **false** indicates that new time proposals are not allowed.</span></span> <span data-ttu-id="2d478-122">组织者在会议请求中设置此值。</span><span class="sxs-lookup"><span data-stu-id="2d478-122">The organizer sets this value in the meeting request.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2d478-123">注解</span><span class="sxs-lookup"><span data-stu-id="2d478-123">Remarks</span></span>

<span data-ttu-id="2d478-124">读写的组织者的日历项目的 AllowNewTimeProposal 属性。</span><span class="sxs-lookup"><span data-stu-id="2d478-124">The AllowNewTimeProposal property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="2d478-125">它是只读的会议请求和与会者的日历项目。</span><span class="sxs-lookup"><span data-stu-id="2d478-125">It is read-only for meeting requests and for attendees' calendar items.</span></span>
  
<span data-ttu-id="2d478-126">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2d478-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2d478-127">Exchange Web 服务不支持新邮件时建议。</span><span class="sxs-lookup"><span data-stu-id="2d478-127">Exchange Web Services does not support new time proposal messages.</span></span> <span data-ttu-id="2d478-128">若要获取新的时间建议邮件相关的属性，请使用扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="2d478-128">To get properties that are related to new time proposal messages, use extended properties.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="2d478-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="2d478-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d478-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="2d478-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2d478-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="2d478-131">Schema name</span></span>  <br/> |<span data-ttu-id="2d478-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="2d478-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="2d478-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="2d478-133">Validation file</span></span>  <br/> |<span data-ttu-id="2d478-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2d478-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2d478-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="2d478-135">Can be empty</span></span>  <br/> |<span data-ttu-id="2d478-136">False</span><span class="sxs-lookup"><span data-stu-id="2d478-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d478-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2d478-137">See also</span></span>

- [<span data-ttu-id="2d478-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2d478-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

