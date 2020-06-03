---
title: IntendedFreeBusyStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IntendedFreeBusyStatus
api_type:
- schema
ms.assetid: 0e0fa898-69a4-4c57-8bb2-52f716b5b478
description: IntendedFreeBusyStatus 元素表示与会议请求相关联的日历项目的预期状态。
ms.openlocfilehash: c5502bcfb308aa2f02a9575ab43f80261b5fa4ed
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465616"
---
# <a name="intendedfreebusystatus"></a><span data-ttu-id="58f03-103">IntendedFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="58f03-103">IntendedFreeBusyStatus</span></span>

<span data-ttu-id="58f03-104">**IntendedFreeBusyStatus**元素表示与会议请求相关联的日历项目的预期状态。</span><span class="sxs-lookup"><span data-stu-id="58f03-104">The **IntendedFreeBusyStatus** element represents the intended status for the calendar item that is associated with the meeting request.</span></span> 
  
```xml
<IntendedFreeBusyStatus/>
```

 <span data-ttu-id="58f03-105">**LegacyFreeBusyType**</span><span class="sxs-lookup"><span data-stu-id="58f03-105">**LegacyFreeBusyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="58f03-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="58f03-106">Attributes and elements</span></span>

<span data-ttu-id="58f03-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="58f03-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58f03-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="58f03-108">Attributes</span></span>

<span data-ttu-id="58f03-109">无。</span><span class="sxs-lookup"><span data-stu-id="58f03-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="58f03-110">子元素</span><span class="sxs-lookup"><span data-stu-id="58f03-110">Child elements</span></span>

<span data-ttu-id="58f03-111">无。</span><span class="sxs-lookup"><span data-stu-id="58f03-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="58f03-112">父元素</span><span class="sxs-lookup"><span data-stu-id="58f03-112">Parent elements</span></span>

|<span data-ttu-id="58f03-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="58f03-113">**Element**</span></span>|<span data-ttu-id="58f03-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="58f03-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58f03-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="58f03-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="58f03-116">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="58f03-116">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="58f03-117">文本值</span><span class="sxs-lookup"><span data-stu-id="58f03-117">Text value</span></span>

<span data-ttu-id="58f03-118">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="58f03-118">A text value is required.</span></span> <span data-ttu-id="58f03-119">以下是此元素的可能值：</span><span class="sxs-lookup"><span data-stu-id="58f03-119">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="58f03-120">空闲</span><span class="sxs-lookup"><span data-stu-id="58f03-120">Free</span></span>
    
- <span data-ttu-id="58f03-121">暂</span><span class="sxs-lookup"><span data-stu-id="58f03-121">Tentative</span></span>
    
- <span data-ttu-id="58f03-122">忙碌</span><span class="sxs-lookup"><span data-stu-id="58f03-122">Busy</span></span>
    
- <span data-ttu-id="58f03-123">OOF</span><span class="sxs-lookup"><span data-stu-id="58f03-123">OOF</span></span>
    
- <span data-ttu-id="58f03-124">NoData</span><span class="sxs-lookup"><span data-stu-id="58f03-124">NoData</span></span>
    
## <a name="remarks"></a><span data-ttu-id="58f03-125">说明</span><span class="sxs-lookup"><span data-stu-id="58f03-125">Remarks</span></span>

<span data-ttu-id="58f03-126">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="58f03-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="58f03-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="58f03-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58f03-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="58f03-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="58f03-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="58f03-129">Schema Name</span></span>  <br/> |<span data-ttu-id="58f03-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="58f03-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="58f03-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="58f03-131">Validation File</span></span>  <br/> |<span data-ttu-id="58f03-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="58f03-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="58f03-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="58f03-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="58f03-134">False</span><span class="sxs-lookup"><span data-stu-id="58f03-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58f03-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="58f03-135">See also</span></span>



- [<span data-ttu-id="58f03-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="58f03-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

