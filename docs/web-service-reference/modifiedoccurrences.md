---
title: ModifiedOccurrences
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ModifiedOccurrences
api_type:
- schema
ms.assetid: 552932fc-b3b4-486e-8d73-32c0bb10bd68
description: ModifiedOccurrences 元素包含已修改的定期日历项目匹配项的数组，以便它们不同于定期主项目。
ms.openlocfilehash: d599e3d232bfffc5bedd37f3dae4d8b10a82ffde
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530420"
---
# <a name="modifiedoccurrences"></a><span data-ttu-id="f2198-103">ModifiedOccurrences</span><span class="sxs-lookup"><span data-stu-id="f2198-103">ModifiedOccurrences</span></span>

<span data-ttu-id="f2198-104">**ModifiedOccurrences**元素包含已修改的定期日历项目匹配项的数组，以便它们不同于定期主项目。</span><span class="sxs-lookup"><span data-stu-id="f2198-104">The **ModifiedOccurrences** element contains an array of recurring calendar item occurrences that have been modified so that they are different than the recurrence master item.</span></span> 
  
```xml
<ModifiedOccurrences>
   <Occurrence/>
</ModifiedOccurrences>
```

 <span data-ttu-id="f2198-105">**NonEmptyArrayOfOccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="f2198-105">**NonEmptyArrayOfOccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f2198-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f2198-106">Attributes and elements</span></span>

<span data-ttu-id="f2198-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f2198-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2198-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f2198-108">Attributes</span></span>

<span data-ttu-id="f2198-109">无。</span><span class="sxs-lookup"><span data-stu-id="f2198-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f2198-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f2198-110">Child elements</span></span>

|<span data-ttu-id="f2198-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f2198-111">**Element**</span></span>|<span data-ttu-id="f2198-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f2198-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2198-113">重复</span><span class="sxs-lookup"><span data-stu-id="f2198-113">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="f2198-114">代表定期日历项目的单个修改事件。</span><span class="sxs-lookup"><span data-stu-id="f2198-114">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f2198-115">父元素</span><span class="sxs-lookup"><span data-stu-id="f2198-115">Parent elements</span></span>

|<span data-ttu-id="f2198-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="f2198-116">**Element**</span></span>|<span data-ttu-id="f2198-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f2198-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2198-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="f2198-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="f2198-119">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="f2198-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f2198-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="f2198-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="f2198-121">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="f2198-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2198-122">备注</span><span class="sxs-lookup"><span data-stu-id="f2198-122">Remarks</span></span>

<span data-ttu-id="f2198-123">如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。</span><span class="sxs-lookup"><span data-stu-id="f2198-123">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="f2198-124">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f2198-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f2198-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="f2198-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2198-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="f2198-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f2198-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="f2198-127">Schema name</span></span>  <br/> |<span data-ttu-id="f2198-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="f2198-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="f2198-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="f2198-129">Validation file</span></span>  <br/> |<span data-ttu-id="f2198-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f2198-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f2198-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="f2198-131">Can be empty</span></span>  <br/> |<span data-ttu-id="f2198-132">False</span><span class="sxs-lookup"><span data-stu-id="f2198-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2198-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f2198-133">See also</span></span>



- [<span data-ttu-id="f2198-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f2198-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

