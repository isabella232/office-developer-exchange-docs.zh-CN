---
title: CalendarItemType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarItemType
api_type:
- schema
ms.assetid: 1feb0788-adf7-4a7c-830c-005214ad930f
description: CalendarItemType 元素表示的日历项目的类型。
ms.openlocfilehash: 3fe95c86ea24e6dfeb4740ead5e787bd63b5190d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753415"
---
# <a name="calendaritemtype"></a><span data-ttu-id="18ed6-103">CalendarItemType</span><span class="sxs-lookup"><span data-stu-id="18ed6-103">CalendarItemType</span></span>

<span data-ttu-id="18ed6-104">**CalendarItemType**元素表示的日历项目的类型。</span><span class="sxs-lookup"><span data-stu-id="18ed6-104">The **CalendarItemType** element represents the type of a calendar item.</span></span> 
  
```xml
<CalendarItemType/>
```

 <span data-ttu-id="18ed6-105">**CalendarItemTypeType**</span><span class="sxs-lookup"><span data-stu-id="18ed6-105">**CalendarItemTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="18ed6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="18ed6-106">Attributes and elements</span></span>

<span data-ttu-id="18ed6-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="18ed6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18ed6-108">属性</span><span class="sxs-lookup"><span data-stu-id="18ed6-108">Attributes</span></span>

<span data-ttu-id="18ed6-109">无。</span><span class="sxs-lookup"><span data-stu-id="18ed6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="18ed6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="18ed6-110">Child elements</span></span>

<span data-ttu-id="18ed6-111">无。</span><span class="sxs-lookup"><span data-stu-id="18ed6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="18ed6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="18ed6-112">Parent elements</span></span>

|<span data-ttu-id="18ed6-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="18ed6-113">**Element**</span></span>|<span data-ttu-id="18ed6-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="18ed6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18ed6-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="18ed6-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="18ed6-116">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="18ed6-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="18ed6-117">日历项目</span><span class="sxs-lookup"><span data-stu-id="18ed6-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="18ed6-118">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="18ed6-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="18ed6-119">文本值</span><span class="sxs-lookup"><span data-stu-id="18ed6-119">Text value</span></span>

<span data-ttu-id="18ed6-120">如果使用此元素，则需要的文本值。</span><span class="sxs-lookup"><span data-stu-id="18ed6-120">A text value is required if this element is used.</span></span> <span data-ttu-id="18ed6-121">此元素的可能值如下：</span><span class="sxs-lookup"><span data-stu-id="18ed6-121">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="18ed6-122">**单个**项目不与定期日历项目相关联。</span><span class="sxs-lookup"><span data-stu-id="18ed6-122">**Single** The item is not associated with a recurring calendar item.</span></span> 
    
- <span data-ttu-id="18ed6-123">**匹配项**该项目是定期日历项目的匹配项。</span><span class="sxs-lookup"><span data-stu-id="18ed6-123">**Occurrence** The item is an occurrence of a recurring calendar item.</span></span> 
    
- <span data-ttu-id="18ed6-124">**异常**该项目是定期日历项目的例外。</span><span class="sxs-lookup"><span data-stu-id="18ed6-124">**Exception** The item is an exception to a recurring calendar item.</span></span> 
    
- <span data-ttu-id="18ed6-125">**RecurringMaster**该项目是一组定期日历项目的主控形状。</span><span class="sxs-lookup"><span data-stu-id="18ed6-125">**RecurringMaster** The item is master for a set of recurring calendar items.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="18ed6-126">备注</span><span class="sxs-lookup"><span data-stu-id="18ed6-126">Remarks</span></span>

<span data-ttu-id="18ed6-127">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="18ed6-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18ed6-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="18ed6-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18ed6-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="18ed6-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="18ed6-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="18ed6-130">Schema name</span></span>  <br/> |<span data-ttu-id="18ed6-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="18ed6-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="18ed6-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="18ed6-132">Validation file</span></span>  <br/> |<span data-ttu-id="18ed6-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="18ed6-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="18ed6-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="18ed6-134">Can be empty</span></span>  <br/> |<span data-ttu-id="18ed6-135">False</span><span class="sxs-lookup"><span data-stu-id="18ed6-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18ed6-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="18ed6-136">See also</span></span>



- [<span data-ttu-id="18ed6-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="18ed6-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

