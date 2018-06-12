---
title: IsCancelled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsCancelled
api_type:
- schema
ms.assetid: 50c1e97f-2913-47a1-8457-60428a3c5b92
description: IsCancelled 元素指示是否已取消约会或会议。
ms.openlocfilehash: 594b8a9ccb535f074a8cf1da060373f640231a29
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825993"
---
# <a name="iscancelled"></a><span data-ttu-id="78527-103">IsCancelled</span><span class="sxs-lookup"><span data-stu-id="78527-103">IsCancelled</span></span>

<span data-ttu-id="78527-104">**IsCancelled**元素指示是否已取消约会或会议。</span><span class="sxs-lookup"><span data-stu-id="78527-104">The **IsCancelled** element indicates whether an appointment or meeting has been canceled.</span></span> 
  
```xml
<IsCancelled/>
```

 <span data-ttu-id="78527-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="78527-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="78527-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="78527-106">Attributes and elements</span></span>

<span data-ttu-id="78527-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="78527-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="78527-108">属性</span><span class="sxs-lookup"><span data-stu-id="78527-108">Attributes</span></span>

<span data-ttu-id="78527-109">无。</span><span class="sxs-lookup"><span data-stu-id="78527-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="78527-110">子元素</span><span class="sxs-lookup"><span data-stu-id="78527-110">Child elements</span></span>

<span data-ttu-id="78527-111">无。</span><span class="sxs-lookup"><span data-stu-id="78527-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="78527-112">父元素</span><span class="sxs-lookup"><span data-stu-id="78527-112">Parent elements</span></span>

|<span data-ttu-id="78527-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="78527-113">**Element**</span></span>|<span data-ttu-id="78527-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="78527-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78527-115">日历项目</span><span class="sxs-lookup"><span data-stu-id="78527-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="78527-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="78527-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="78527-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="78527-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="78527-118">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="78527-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="78527-119">文本值</span><span class="sxs-lookup"><span data-stu-id="78527-119">Text value</span></span>

<span data-ttu-id="78527-120">如果此元素是包含，则需要一个文本值，它代表一个布尔值。</span><span class="sxs-lookup"><span data-stu-id="78527-120">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="78527-121">值为**true**指示日历项目已被取消。</span><span class="sxs-lookup"><span data-stu-id="78527-121">A value of **true** indicates that the calendar item has been canceled.</span></span> <span data-ttu-id="78527-122">如果值为**false**指示日历项目不被取消。</span><span class="sxs-lookup"><span data-stu-id="78527-122">A value of **false** indicates that a calendar item has not been canceled.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="78527-123">备注</span><span class="sxs-lookup"><span data-stu-id="78527-123">Remarks</span></span>

<span data-ttu-id="78527-124">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="78527-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="78527-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="78527-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78527-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="78527-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="78527-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="78527-127">Schema name</span></span>  <br/> |<span data-ttu-id="78527-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="78527-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="78527-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="78527-129">Validation file</span></span>  <br/> |<span data-ttu-id="78527-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="78527-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="78527-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="78527-131">Can be empty</span></span>  <br/> |<span data-ttu-id="78527-132">False</span><span class="sxs-lookup"><span data-stu-id="78527-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78527-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="78527-133">See also</span></span>



- [<span data-ttu-id="78527-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="78527-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

