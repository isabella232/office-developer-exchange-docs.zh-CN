---
title: ConflictingMeetings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConflictingMeetings
api_type:
- schema
ms.assetid: cfff7a11-7b3a-4995-9815-afedd45ebb0f
description: ConflictingMeetings 元素标识与会议时间冲突的所有日历项目。
ms.openlocfilehash: 1d2558dba41ec3e7ae2711bb2dc26f54cada827a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753480"
---
# <a name="conflictingmeetings"></a><span data-ttu-id="2a6a3-103">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="2a6a3-103">ConflictingMeetings</span></span>

<span data-ttu-id="2a6a3-104">**ConflictingMeetings**元素标识与会议时间冲突的所有日历项目。</span><span class="sxs-lookup"><span data-stu-id="2a6a3-104">The **ConflictingMeetings** element identifies all calendar items that conflict with a meeting time.</span></span> 
  
```xml
<ConflictingMeetings>
   <CalendarItem/>
</ConflictingMeetings>
```

 <span data-ttu-id="2a6a3-105">**NonEmptyArrayOfAllItemsType**</span><span class="sxs-lookup"><span data-stu-id="2a6a3-105">**NonEmptyArrayOfAllItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2a6a3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2a6a3-106">Attributes and elements</span></span>

<span data-ttu-id="2a6a3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2a6a3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a6a3-108">属性</span><span class="sxs-lookup"><span data-stu-id="2a6a3-108">Attributes</span></span>

<span data-ttu-id="2a6a3-109">无。</span><span class="sxs-lookup"><span data-stu-id="2a6a3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2a6a3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2a6a3-110">Child elements</span></span>

|<span data-ttu-id="2a6a3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2a6a3-111">**Element**</span></span>|<span data-ttu-id="2a6a3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2a6a3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a6a3-113">日历项目</span><span class="sxs-lookup"><span data-stu-id="2a6a3-113">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="2a6a3-114">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="2a6a3-114">Represents an Exchange calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2a6a3-115">父元素</span><span class="sxs-lookup"><span data-stu-id="2a6a3-115">Parent elements</span></span>

|<span data-ttu-id="2a6a3-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="2a6a3-116">**Element**</span></span>|<span data-ttu-id="2a6a3-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="2a6a3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a6a3-118">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="2a6a3-118">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="2a6a3-119">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="2a6a3-119">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2a6a3-120">日历项目</span><span class="sxs-lookup"><span data-stu-id="2a6a3-120">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="2a6a3-121">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="2a6a3-121">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a6a3-122">备注</span><span class="sxs-lookup"><span data-stu-id="2a6a3-122">Remarks</span></span>

<span data-ttu-id="2a6a3-123">如果使用此元素，则它必须包含一个或多个子元素。</span><span class="sxs-lookup"><span data-stu-id="2a6a3-123">If this element is used, it must contain one or more child elements.</span></span>
  
<span data-ttu-id="2a6a3-124">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2a6a3-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2a6a3-125">尽管其他子元素都有效每个架构，但的[日历项目](calendaritem.md)元素是 Exchange Web Services (EWS) 将返回**ConflictingMeetings**元素中的唯一子元素。</span><span class="sxs-lookup"><span data-stu-id="2a6a3-125">Although additional child elements are valid per the schema, the [CalendarItem](calendaritem.md) element is the only child element that Exchange Web Services (EWS) will return within the **ConflictingMeetings** element.</span></span> <span data-ttu-id="2a6a3-126">本主题不会列出的每个架构有效，但不是会通过 EWS 返回子元素。</span><span class="sxs-lookup"><span data-stu-id="2a6a3-126">This topic does not list child elements that are valid per the schema but will not be returned by EWS.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="2a6a3-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="2a6a3-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a6a3-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="2a6a3-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2a6a3-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="2a6a3-129">Schema Name</span></span>  <br/> |<span data-ttu-id="2a6a3-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="2a6a3-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="2a6a3-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="2a6a3-131">Validation File</span></span>  <br/> |<span data-ttu-id="2a6a3-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2a6a3-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2a6a3-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="2a6a3-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="2a6a3-134">False</span><span class="sxs-lookup"><span data-stu-id="2a6a3-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2a6a3-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2a6a3-135">See also</span></span>



- [<span data-ttu-id="2a6a3-136">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2a6a3-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

