---
title: NetShowUrl
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NetShowUrl
api_type:
- schema
ms.assetid: a5d48fc1-b141-422c-bcb0-05d0f9ba90dd
description: NetShowUrl 元素指定 Microsoft NetShow online 会议的 URL。
ms.openlocfilehash: 66e288a5e66eecf404698135cc3257085b852034
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466330"
---
# <a name="netshowurl"></a><span data-ttu-id="0b7e4-103">NetShowUrl</span><span class="sxs-lookup"><span data-stu-id="0b7e4-103">NetShowUrl</span></span>

<span data-ttu-id="0b7e4-104">**NetShowUrl**元素指定 Microsoft NetShow online 会议的 URL。</span><span class="sxs-lookup"><span data-stu-id="0b7e4-104">The **NetShowUrl** element specifies the URL for a Microsoft NetShow online meeting.</span></span> 
  
```xml
<NetShowUrl/>
```

 <span data-ttu-id="0b7e4-105">**string**</span><span class="sxs-lookup"><span data-stu-id="0b7e4-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0b7e4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0b7e4-106">Attributes and elements</span></span>

<span data-ttu-id="0b7e4-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0b7e4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0b7e4-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="0b7e4-108">Attributes</span></span>

<span data-ttu-id="0b7e4-109">无。</span><span class="sxs-lookup"><span data-stu-id="0b7e4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0b7e4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0b7e4-110">Child elements</span></span>

<span data-ttu-id="0b7e4-111">无。</span><span class="sxs-lookup"><span data-stu-id="0b7e4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0b7e4-112">父元素</span><span class="sxs-lookup"><span data-stu-id="0b7e4-112">Parent elements</span></span>

|<span data-ttu-id="0b7e4-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="0b7e4-113">**Element**</span></span>|<span data-ttu-id="0b7e4-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="0b7e4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0b7e4-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="0b7e4-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="0b7e4-116">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="0b7e4-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0b7e4-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="0b7e4-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="0b7e4-118">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="0b7e4-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0b7e4-119">文本值</span><span class="sxs-lookup"><span data-stu-id="0b7e4-119">Text value</span></span>

<span data-ttu-id="0b7e4-120">如果使用此元素，则需要一个表示 URL 的文本值。</span><span class="sxs-lookup"><span data-stu-id="0b7e4-120">A text value that represents a URL is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0b7e4-121">备注</span><span class="sxs-lookup"><span data-stu-id="0b7e4-121">Remarks</span></span>

<span data-ttu-id="0b7e4-122">此 NetShowUrl 属性可读写组织者的日历项目。</span><span class="sxs-lookup"><span data-stu-id="0b7e4-122">This NetShowUrl property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="0b7e4-123">对于会议请求和与会者，它是只读的。</span><span class="sxs-lookup"><span data-stu-id="0b7e4-123">It is read-only for meeting requests and for attendees.</span></span>
  
<span data-ttu-id="0b7e4-124">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0b7e4-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0b7e4-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="0b7e4-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b7e4-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="0b7e4-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0b7e4-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="0b7e4-127">Schema name</span></span>  <br/> |<span data-ttu-id="0b7e4-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="0b7e4-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="0b7e4-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="0b7e4-129">Validation file</span></span>  <br/> |<span data-ttu-id="0b7e4-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0b7e4-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0b7e4-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="0b7e4-131">Can be empty</span></span>  <br/> |<span data-ttu-id="0b7e4-132">False</span><span class="sxs-lookup"><span data-stu-id="0b7e4-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0b7e4-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0b7e4-133">See also</span></span>



- [<span data-ttu-id="0b7e4-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0b7e4-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

