---
title: IsDelegated
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsDelegated
api_type:
- schema
ms.assetid: c12907db-be80-4924-9469-8e58612cf42c
description: IsDelegated 元素指示会议已由具有代理访问的帐户。
ms.openlocfilehash: a6f42a57b2d0fdb760e4c36d3211ba57289a3c7c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826005"
---
# <a name="isdelegated"></a><span data-ttu-id="e357c-103">IsDelegated</span><span class="sxs-lookup"><span data-stu-id="e357c-103">IsDelegated</span></span>

<span data-ttu-id="e357c-104">**IsDelegated**元素指示会议已由具有代理访问的帐户。</span><span class="sxs-lookup"><span data-stu-id="e357c-104">The **IsDelegated** element indicates whether a meeting was handled by an account that has delegate access.</span></span> 
  
```xml
<IsDelegated/>
```

 <span data-ttu-id="e357c-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e357c-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e357c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e357c-106">Attributes and elements</span></span>

<span data-ttu-id="e357c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e357c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e357c-108">属性</span><span class="sxs-lookup"><span data-stu-id="e357c-108">Attributes</span></span>

<span data-ttu-id="e357c-109">无。</span><span class="sxs-lookup"><span data-stu-id="e357c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e357c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e357c-110">Child elements</span></span>

<span data-ttu-id="e357c-111">无。</span><span class="sxs-lookup"><span data-stu-id="e357c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e357c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e357c-112">Parent elements</span></span>

|<span data-ttu-id="e357c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e357c-113">**Element**</span></span>|<span data-ttu-id="e357c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e357c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e357c-115">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="e357c-115">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="e357c-116">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="e357c-116">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e357c-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="e357c-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="e357c-118">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="e357c-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e357c-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="e357c-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="e357c-120">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="e357c-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e357c-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="e357c-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="e357c-122">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="e357c-122">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e357c-123">文本值</span><span class="sxs-lookup"><span data-stu-id="e357c-123">Text value</span></span>

<span data-ttu-id="e357c-124">文本值为**true**指示会议已处理的具有代理访问的帐户。</span><span class="sxs-lookup"><span data-stu-id="e357c-124">A text value of **true** indicates that the meeting was handled by an account that has delegate access.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e357c-125">备注</span><span class="sxs-lookup"><span data-stu-id="e357c-125">Remarks</span></span>

<span data-ttu-id="e357c-126">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e357c-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e357c-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="e357c-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e357c-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="e357c-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e357c-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="e357c-129">Schema Name</span></span>  <br/> |<span data-ttu-id="e357c-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="e357c-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="e357c-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="e357c-131">Validation File</span></span>  <br/> |<span data-ttu-id="e357c-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e357c-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e357c-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="e357c-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="e357c-134">False</span><span class="sxs-lookup"><span data-stu-id="e357c-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e357c-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e357c-135">See also</span></span>



- [<span data-ttu-id="e357c-136">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e357c-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

