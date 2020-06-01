---
title: DeletedOccurrences
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeletedOccurrences
api_type:
- schema
ms.assetid: 736fb305-9528-4be8-ad37-65d7556edbf2
description: DeletedOccurrences 元素包含定期日历项目的已删除事件数组。
ms.openlocfilehash: be39ff95b5529481a36b7549e638818a20e01283
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463704"
---
# <a name="deletedoccurrences"></a><span data-ttu-id="605cc-103">DeletedOccurrences</span><span class="sxs-lookup"><span data-stu-id="605cc-103">DeletedOccurrences</span></span>

<span data-ttu-id="605cc-104">**DeletedOccurrences**元素包含定期日历项目的已删除事件数组。</span><span class="sxs-lookup"><span data-stu-id="605cc-104">The **DeletedOccurrences** element contains an array of deleted occurrences of a recurring calendar item.</span></span> 
  
```xml
<DeletedOccurrences>
   <DeletedOccurrence/>
</DeletedOccurrences>
```

 <span data-ttu-id="605cc-105">**NonEmptyArrayOfDeletedOccurrencesType**</span><span class="sxs-lookup"><span data-stu-id="605cc-105">**NonEmptyArrayOfDeletedOccurrencesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="605cc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="605cc-106">Attributes and elements</span></span>

<span data-ttu-id="605cc-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="605cc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="605cc-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="605cc-108">Attributes</span></span>

<span data-ttu-id="605cc-109">无。</span><span class="sxs-lookup"><span data-stu-id="605cc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="605cc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="605cc-110">Child elements</span></span>

|<span data-ttu-id="605cc-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="605cc-111">**Element**</span></span>|<span data-ttu-id="605cc-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="605cc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="605cc-113">DeletedOccurrence</span><span class="sxs-lookup"><span data-stu-id="605cc-113">DeletedOccurrence</span></span>](deletedoccurrence.md) <br/> |<span data-ttu-id="605cc-114">表示定期日历项目的已删除事件。</span><span class="sxs-lookup"><span data-stu-id="605cc-114">Represents a deleted occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="605cc-115">父元素</span><span class="sxs-lookup"><span data-stu-id="605cc-115">Parent elements</span></span>

|<span data-ttu-id="605cc-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="605cc-116">**Element**</span></span>|<span data-ttu-id="605cc-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="605cc-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="605cc-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="605cc-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="605cc-119">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="605cc-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="605cc-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="605cc-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="605cc-121">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="605cc-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="605cc-122">备注</span><span class="sxs-lookup"><span data-stu-id="605cc-122">Remarks</span></span>

<span data-ttu-id="605cc-123">如果将 RecurringMaster 文本值用于[CalendarItemType](calendaritemtype.md)元素，则此元素有效。</span><span class="sxs-lookup"><span data-stu-id="605cc-123">This element is valid if the RecurringMaster text value is used for the [CalendarItemType](calendaritemtype.md) element.</span></span> 
  
<span data-ttu-id="605cc-124">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="605cc-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="605cc-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="605cc-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="605cc-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="605cc-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="605cc-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="605cc-127">Schema name</span></span>  <br/> |<span data-ttu-id="605cc-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="605cc-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="605cc-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="605cc-129">Validation file</span></span>  <br/> |<span data-ttu-id="605cc-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="605cc-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="605cc-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="605cc-131">Can be empty</span></span>  <br/> |<span data-ttu-id="605cc-132">False</span><span class="sxs-lookup"><span data-stu-id="605cc-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="605cc-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="605cc-133">See also</span></span>

- [<span data-ttu-id="605cc-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="605cc-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)  
- [<span data-ttu-id="605cc-135">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="605cc-135">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

