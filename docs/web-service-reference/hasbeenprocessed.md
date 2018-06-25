---
title: HasBeenProcessed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HasBeenProcessed
api_type:
- schema
ms.assetid: 46d4af8e-0f11-4a74-9365-1d983731fed8
description: HasBeenProcessed 元素指示是否会议邮件项已处理。
ms.openlocfilehash: cccd3b2258490fcbe902bcd391f25b0be2fe7c26
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825796"
---
# <a name="hasbeenprocessed"></a><span data-ttu-id="da909-103">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="da909-103">HasBeenProcessed</span></span>

<span data-ttu-id="da909-104">**HasBeenProcessed**元素指示是否会议邮件项已处理。</span><span class="sxs-lookup"><span data-stu-id="da909-104">The **HasBeenProcessed** element indicates whether a meeting message item has been processed.</span></span> 
  
```xml
<HasBeenProcessed/>
```

 <span data-ttu-id="da909-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="da909-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="da909-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="da909-106">Attributes and elements</span></span>

<span data-ttu-id="da909-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="da909-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da909-108">属性</span><span class="sxs-lookup"><span data-stu-id="da909-108">Attributes</span></span>

<span data-ttu-id="da909-109">无。</span><span class="sxs-lookup"><span data-stu-id="da909-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="da909-110">子元素</span><span class="sxs-lookup"><span data-stu-id="da909-110">Child elements</span></span>

<span data-ttu-id="da909-111">无。</span><span class="sxs-lookup"><span data-stu-id="da909-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="da909-112">父元素</span><span class="sxs-lookup"><span data-stu-id="da909-112">Parent elements</span></span>

|<span data-ttu-id="da909-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="da909-113">**Element**</span></span>|<span data-ttu-id="da909-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="da909-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da909-115">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="da909-115">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="da909-116">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="da909-116">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="da909-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="da909-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="da909-118">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="da909-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="da909-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="da909-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="da909-120">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="da909-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="da909-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="da909-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="da909-122">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="da909-122">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="da909-123">文本值</span><span class="sxs-lookup"><span data-stu-id="da909-123">Text value</span></span>

<span data-ttu-id="da909-124">文本值为**true**指示已处理的会议消息。</span><span class="sxs-lookup"><span data-stu-id="da909-124">A text value of **true** indicates that the meeting message has been processed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="da909-125">备注</span><span class="sxs-lookup"><span data-stu-id="da909-125">Remarks</span></span>

<span data-ttu-id="da909-126">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="da909-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="da909-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="da909-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da909-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="da909-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="da909-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="da909-129">Schema Name</span></span>  <br/> |<span data-ttu-id="da909-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="da909-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="da909-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="da909-131">Validation File</span></span>  <br/> |<span data-ttu-id="da909-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="da909-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="da909-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="da909-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="da909-134">False</span><span class="sxs-lookup"><span data-stu-id="da909-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da909-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="da909-135">See also</span></span>



- [<span data-ttu-id="da909-136">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="da909-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

