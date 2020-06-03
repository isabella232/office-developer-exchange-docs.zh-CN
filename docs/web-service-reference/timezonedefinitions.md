---
title: TimeZoneDefinitions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeZoneDefinitions
api_type:
- schema
ms.assetid: 9ca1584e-65b8-49ba-a408-e3e8597e6607
description: TimeZoneDefinitions 元素表示时区定义的数组。
ms.openlocfilehash: 16a25eb4fdcad2554ebd19626d0a0bc7f6391ac5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468759"
---
# <a name="timezonedefinitions"></a><span data-ttu-id="4ae91-103">TimeZoneDefinitions</span><span class="sxs-lookup"><span data-stu-id="4ae91-103">TimeZoneDefinitions</span></span>

<span data-ttu-id="4ae91-104">**TimeZoneDefinitions**元素表示时区定义的数组。</span><span class="sxs-lookup"><span data-stu-id="4ae91-104">The **TimeZoneDefinitions** element represents an array of time zone definitions.</span></span> 
  
```XML
<TimeZoneDefinitions>
   <TimeZoneDefinition/>
</TimeZoneDefinitions>
```

 <span data-ttu-id="4ae91-105">**ArrayOfTimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="4ae91-105">**ArrayOfTimeZoneDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4ae91-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4ae91-106">Attributes and elements</span></span>

<span data-ttu-id="4ae91-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4ae91-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ae91-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4ae91-108">Attributes</span></span>

<span data-ttu-id="4ae91-109">无。</span><span class="sxs-lookup"><span data-stu-id="4ae91-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4ae91-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4ae91-110">Child elements</span></span>

|<span data-ttu-id="4ae91-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="4ae91-111">**Element**</span></span>|<span data-ttu-id="4ae91-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="4ae91-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ae91-113">TimeZoneDefinition</span><span class="sxs-lookup"><span data-stu-id="4ae91-113">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="4ae91-114">指定用于定义时区的周期和转换。</span><span class="sxs-lookup"><span data-stu-id="4ae91-114">Specifies the periods and transitions that define a time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4ae91-115">父元素</span><span class="sxs-lookup"><span data-stu-id="4ae91-115">Parent elements</span></span>

|<span data-ttu-id="4ae91-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="4ae91-116">**Element**</span></span>|<span data-ttu-id="4ae91-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="4ae91-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ae91-118">GetServerTimeZonesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4ae91-118">GetServerTimeZonesResponseMessage</span></span>](getservertimezonesresponsemessage.md) <br/> |<span data-ttu-id="4ae91-119">包含[GetServerTimeZones 操作](getservertimezones-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="4ae91-119">Contains the status and result of a [GetServerTimeZones operation](getservertimezones-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ae91-120">说明</span><span class="sxs-lookup"><span data-stu-id="4ae91-120">Remarks</span></span>

<span data-ttu-id="4ae91-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4ae91-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4ae91-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="4ae91-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ae91-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="4ae91-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4ae91-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="4ae91-124">Schema Name</span></span>  <br/> |<span data-ttu-id="4ae91-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="4ae91-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4ae91-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="4ae91-126">Validation File</span></span>  <br/> |<span data-ttu-id="4ae91-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4ae91-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4ae91-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="4ae91-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="4ae91-129">False</span><span class="sxs-lookup"><span data-stu-id="4ae91-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4ae91-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4ae91-130">See also</span></span>



- [<span data-ttu-id="4ae91-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4ae91-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

