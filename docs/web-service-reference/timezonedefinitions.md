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
description: TimeZoneDefinitions 元素均表示所在的时区定义的数组。
ms.openlocfilehash: 0bc1b69ef564bb4e239d9845a4b1a0133292ff12
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838238"
---
# <a name="timezonedefinitions"></a><span data-ttu-id="7a40a-103">TimeZoneDefinitions</span><span class="sxs-lookup"><span data-stu-id="7a40a-103">TimeZoneDefinitions</span></span>

<span data-ttu-id="7a40a-104">**TimeZoneDefinitions**元素均表示所在的时区定义的数组。</span><span class="sxs-lookup"><span data-stu-id="7a40a-104">The **TimeZoneDefinitions** element represents an array of time zone definitions.</span></span> 
  
```XML
<TimeZoneDefinitions>
   <TimeZoneDefinition/>
</TimeZoneDefinitions>
```

 <span data-ttu-id="7a40a-105">**ArrayOfTimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="7a40a-105">**ArrayOfTimeZoneDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7a40a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7a40a-106">Attributes and elements</span></span>

<span data-ttu-id="7a40a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7a40a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a40a-108">属性</span><span class="sxs-lookup"><span data-stu-id="7a40a-108">Attributes</span></span>

<span data-ttu-id="7a40a-109">无。</span><span class="sxs-lookup"><span data-stu-id="7a40a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a40a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7a40a-110">Child elements</span></span>

|<span data-ttu-id="7a40a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7a40a-111">**Element**</span></span>|<span data-ttu-id="7a40a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7a40a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a40a-113">时区定义</span><span class="sxs-lookup"><span data-stu-id="7a40a-113">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="7a40a-114">指定的时间段和定义时区的切换。</span><span class="sxs-lookup"><span data-stu-id="7a40a-114">Specifies the periods and transitions that define a time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7a40a-115">父元素</span><span class="sxs-lookup"><span data-stu-id="7a40a-115">Parent elements</span></span>

|<span data-ttu-id="7a40a-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="7a40a-116">**Element**</span></span>|<span data-ttu-id="7a40a-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="7a40a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a40a-118">GetServerTimeZonesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7a40a-118">GetServerTimeZonesResponseMessage</span></span>](getservertimezonesresponsemessage.md) <br/> |<span data-ttu-id="7a40a-119">包含状态和[GetServerTimeZones 操作](getservertimezones-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="7a40a-119">Contains the status and result of a [GetServerTimeZones operation](getservertimezones-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a40a-120">备注</span><span class="sxs-lookup"><span data-stu-id="7a40a-120">Remarks</span></span>

<span data-ttu-id="7a40a-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7a40a-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a40a-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="7a40a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a40a-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="7a40a-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7a40a-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="7a40a-124">Schema Name</span></span>  <br/> |<span data-ttu-id="7a40a-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="7a40a-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7a40a-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="7a40a-126">Validation File</span></span>  <br/> |<span data-ttu-id="7a40a-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7a40a-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7a40a-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="7a40a-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="7a40a-129">False</span><span class="sxs-lookup"><span data-stu-id="7a40a-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a40a-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7a40a-130">See also</span></span>



- [<span data-ttu-id="7a40a-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7a40a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

