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
description: DeletedOccurrences 元素包含数组的定期日历项目的已删除匹配项。
ms.openlocfilehash: 269c1176913cd642f93987462286dd1fee3a7339
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753798"
---
# <a name="deletedoccurrences"></a><span data-ttu-id="fe3a5-103">DeletedOccurrences</span><span class="sxs-lookup"><span data-stu-id="fe3a5-103">DeletedOccurrences</span></span>

<span data-ttu-id="fe3a5-104">**DeletedOccurrences**元素包含数组的定期日历项目的已删除匹配项。</span><span class="sxs-lookup"><span data-stu-id="fe3a5-104">The **DeletedOccurrences** element contains an array of deleted occurrences of a recurring calendar item.</span></span> 
  
```xml
<DeletedOccurrences>
   <DeletedOccurrence/>
</DeletedOccurrences>
```

 <span data-ttu-id="fe3a5-105">**NonEmptyArrayOfDeletedOccurrencesType**</span><span class="sxs-lookup"><span data-stu-id="fe3a5-105">**NonEmptyArrayOfDeletedOccurrencesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fe3a5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fe3a5-106">Attributes and elements</span></span>

<span data-ttu-id="fe3a5-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fe3a5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fe3a5-108">属性</span><span class="sxs-lookup"><span data-stu-id="fe3a5-108">Attributes</span></span>

<span data-ttu-id="fe3a5-109">无。</span><span class="sxs-lookup"><span data-stu-id="fe3a5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fe3a5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fe3a5-110">Child elements</span></span>

|<span data-ttu-id="fe3a5-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="fe3a5-111">**Element**</span></span>|<span data-ttu-id="fe3a5-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="fe3a5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe3a5-113">DeletedOccurrence</span><span class="sxs-lookup"><span data-stu-id="fe3a5-113">DeletedOccurrence</span></span>](deletedoccurrence.md) <br/> |<span data-ttu-id="fe3a5-114">代表定期日历项目的已删除的匹配项。</span><span class="sxs-lookup"><span data-stu-id="fe3a5-114">Represents a deleted occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fe3a5-115">父元素</span><span class="sxs-lookup"><span data-stu-id="fe3a5-115">Parent elements</span></span>

|<span data-ttu-id="fe3a5-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="fe3a5-116">**Element**</span></span>|<span data-ttu-id="fe3a5-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="fe3a5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe3a5-118">日历项目</span><span class="sxs-lookup"><span data-stu-id="fe3a5-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="fe3a5-119">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="fe3a5-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="fe3a5-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="fe3a5-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="fe3a5-121">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="fe3a5-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe3a5-122">注解</span><span class="sxs-lookup"><span data-stu-id="fe3a5-122">Remarks</span></span>

<span data-ttu-id="fe3a5-123">此元素是 RecurringMaster 文本值使用[CalendarItemType](calendaritemtype.md)元素时有效。</span><span class="sxs-lookup"><span data-stu-id="fe3a5-123">This element is valid if the RecurringMaster text value is used for the [CalendarItemType](calendaritemtype.md) element.</span></span> 
  
<span data-ttu-id="fe3a5-124">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fe3a5-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fe3a5-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="fe3a5-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe3a5-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="fe3a5-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fe3a5-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="fe3a5-127">Schema name</span></span>  <br/> |<span data-ttu-id="fe3a5-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="fe3a5-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="fe3a5-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="fe3a5-129">Validation file</span></span>  <br/> |<span data-ttu-id="fe3a5-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fe3a5-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fe3a5-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="fe3a5-131">Can be empty</span></span>  <br/> |<span data-ttu-id="fe3a5-132">False</span><span class="sxs-lookup"><span data-stu-id="fe3a5-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fe3a5-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fe3a5-133">See also</span></span>

- [<span data-ttu-id="fe3a5-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fe3a5-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)  
- [<span data-ttu-id="fe3a5-135">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="fe3a5-135">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

