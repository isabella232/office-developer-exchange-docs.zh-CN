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
description: IntendedFreeBusyStatus 元素均表示与会议请求相关联的日历项目的预期的状态。
ms.openlocfilehash: 3254becf8c6885f7d6dc401ecf31da149e7de2d4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825945"
---
# <a name="intendedfreebusystatus"></a><span data-ttu-id="66118-103">IntendedFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="66118-103">IntendedFreeBusyStatus</span></span>

<span data-ttu-id="66118-104">**IntendedFreeBusyStatus**元素均表示与会议请求相关联的日历项目的预期的状态。</span><span class="sxs-lookup"><span data-stu-id="66118-104">The **IntendedFreeBusyStatus** element represents the intended status for the calendar item that is associated with the meeting request.</span></span> 
  
```xml
<IntendedFreeBusyStatus/>
```

 <span data-ttu-id="66118-105">**LegacyFreeBusyType**</span><span class="sxs-lookup"><span data-stu-id="66118-105">**LegacyFreeBusyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="66118-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="66118-106">Attributes and elements</span></span>

<span data-ttu-id="66118-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="66118-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66118-108">属性</span><span class="sxs-lookup"><span data-stu-id="66118-108">Attributes</span></span>

<span data-ttu-id="66118-109">无。</span><span class="sxs-lookup"><span data-stu-id="66118-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="66118-110">子元素</span><span class="sxs-lookup"><span data-stu-id="66118-110">Child elements</span></span>

<span data-ttu-id="66118-111">无。</span><span class="sxs-lookup"><span data-stu-id="66118-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="66118-112">父元素</span><span class="sxs-lookup"><span data-stu-id="66118-112">Parent elements</span></span>

|<span data-ttu-id="66118-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="66118-113">**Element**</span></span>|<span data-ttu-id="66118-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="66118-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66118-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="66118-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="66118-116">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="66118-116">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="66118-117">文本值</span><span class="sxs-lookup"><span data-stu-id="66118-117">Text value</span></span>

<span data-ttu-id="66118-118">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="66118-118">A text value is required.</span></span> <span data-ttu-id="66118-119">此元素的可能值如下：</span><span class="sxs-lookup"><span data-stu-id="66118-119">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="66118-120">免费</span><span class="sxs-lookup"><span data-stu-id="66118-120">Free</span></span>
    
- <span data-ttu-id="66118-121">暂定</span><span class="sxs-lookup"><span data-stu-id="66118-121">Tentative</span></span>
    
- <span data-ttu-id="66118-122">忙碌</span><span class="sxs-lookup"><span data-stu-id="66118-122">Busy</span></span>
    
- <span data-ttu-id="66118-123">OOF</span><span class="sxs-lookup"><span data-stu-id="66118-123">OOF</span></span>
    
- <span data-ttu-id="66118-124">NoData</span><span class="sxs-lookup"><span data-stu-id="66118-124">NoData</span></span>
    
## <a name="remarks"></a><span data-ttu-id="66118-125">备注</span><span class="sxs-lookup"><span data-stu-id="66118-125">Remarks</span></span>

<span data-ttu-id="66118-126">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="66118-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66118-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="66118-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66118-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="66118-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="66118-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="66118-129">Schema Name</span></span>  <br/> |<span data-ttu-id="66118-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="66118-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="66118-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="66118-131">Validation File</span></span>  <br/> |<span data-ttu-id="66118-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="66118-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="66118-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="66118-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="66118-134">False</span><span class="sxs-lookup"><span data-stu-id="66118-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="66118-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="66118-135">See also</span></span>



- [<span data-ttu-id="66118-136">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="66118-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

