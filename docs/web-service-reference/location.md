---
title: Location
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Location
api_type:
- schema
ms.assetid: 3fcf7133-ae1c-47b4-a187-660045f71df0
description: Location 元素表示会议、 约会或个人的位置。
ms.openlocfilehash: 0d2bc131763c4ffa399fe9397d247d89a84e0d1b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826241"
---
# <a name="location"></a><span data-ttu-id="a40d9-103">位置</span><span class="sxs-lookup"><span data-stu-id="a40d9-103">Location</span></span>

<span data-ttu-id="a40d9-104">**Location**元素表示会议、 约会或个人的位置。</span><span class="sxs-lookup"><span data-stu-id="a40d9-104">The **Location** element represents the location of a meeting, appointment, or persona.</span></span> 
  
```xml
<Location/>
```

 <span data-ttu-id="a40d9-105">**string**</span><span class="sxs-lookup"><span data-stu-id="a40d9-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a40d9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a40d9-106">Attributes and elements</span></span>

<span data-ttu-id="a40d9-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a40d9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a40d9-108">属性</span><span class="sxs-lookup"><span data-stu-id="a40d9-108">Attributes</span></span>

<span data-ttu-id="a40d9-109">无。</span><span class="sxs-lookup"><span data-stu-id="a40d9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a40d9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a40d9-110">Child elements</span></span>

<span data-ttu-id="a40d9-111">无。</span><span class="sxs-lookup"><span data-stu-id="a40d9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a40d9-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a40d9-112">Parent elements</span></span>

|<span data-ttu-id="a40d9-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a40d9-113">**Element**</span></span>|<span data-ttu-id="a40d9-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a40d9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a40d9-115">日历项目</span><span class="sxs-lookup"><span data-stu-id="a40d9-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="a40d9-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="a40d9-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="a40d9-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="a40d9-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="a40d9-118">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="a40d9-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a40d9-119">文本值</span><span class="sxs-lookup"><span data-stu-id="a40d9-119">Text value</span></span>

<span data-ttu-id="a40d9-120">需要安装一个表示会议或约会的位置的文本值。</span><span class="sxs-lookup"><span data-stu-id="a40d9-120">A text value that represents the location of a meeting or appointment is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a40d9-121">备注</span><span class="sxs-lookup"><span data-stu-id="a40d9-121">Remarks</span></span>

<span data-ttu-id="a40d9-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a40d9-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a40d9-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="a40d9-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a40d9-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="a40d9-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a40d9-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="a40d9-125">Schema name</span></span>  <br/> |<span data-ttu-id="a40d9-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="a40d9-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="a40d9-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="a40d9-127">Validation file</span></span>  <br/> |<span data-ttu-id="a40d9-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a40d9-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a40d9-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="a40d9-129">Can be empty</span></span>  <br/> |<span data-ttu-id="a40d9-130">False</span><span class="sxs-lookup"><span data-stu-id="a40d9-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a40d9-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a40d9-131">See also</span></span>



- [<span data-ttu-id="a40d9-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a40d9-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

