---
title: GetServerTimeZones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServerTimeZones
api_type:
- schema
ms.assetid: 2a89098b-d89b-4d01-827b-50be00f7cbe9
description: GetServerTimeZones 元素是请求中的根元素，用于检索来自 Exchange 服务器的时区定义。
ms.openlocfilehash: 797e4543c94b0628242bcf544fe9a735ebaa5a63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460937"
---
# <a name="getservertimezones"></a><span data-ttu-id="8fc61-103">GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="8fc61-103">GetServerTimeZones</span></span>

<span data-ttu-id="8fc61-104">**GetServerTimeZones**元素是请求中的根元素，用于检索来自 Exchange 服务器的时区定义。</span><span class="sxs-lookup"><span data-stu-id="8fc61-104">The **GetServerTimeZones** element is the root element in a request to retrieve time zone definitions from the Exchange server.</span></span> 
  
```xml
<GetServerTimeZones ReturnFullTimeZoneData="">   <Ids/></GetServerTimeZones>
```

 <span data-ttu-id="8fc61-105">**GetServerTimeZonesType**</span><span class="sxs-lookup"><span data-stu-id="8fc61-105">**GetServerTimeZonesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8fc61-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8fc61-106">Attributes and elements</span></span>

<span data-ttu-id="8fc61-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8fc61-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8fc61-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="8fc61-108">Attributes</span></span>

|<span data-ttu-id="8fc61-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="8fc61-109">**Attribute**</span></span>|<span data-ttu-id="8fc61-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="8fc61-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8fc61-111">**ReturnFullTimeZoneData**</span><span class="sxs-lookup"><span data-stu-id="8fc61-111">**ReturnFullTimeZoneData**</span></span> <br/> |<span data-ttu-id="8fc61-112">指定[GetServerTimeZones 操作](getservertimezones-operation.md)是返回完整定义还是仅返回每个时区的名称和标识符。</span><span class="sxs-lookup"><span data-stu-id="8fc61-112">Specifies whether the [GetServerTimeZones operation](getservertimezones-operation.md) returns the complete definition or only the name and identifier for each time zone.</span></span> <span data-ttu-id="8fc61-113">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="8fc61-113">This attribute is optional.</span></span> <span data-ttu-id="8fc61-114">默认值为 **true** 。</span><span class="sxs-lookup"><span data-stu-id="8fc61-114">The default value is **true**.</span></span>  <br/> |
   
#### <a name="returnfulltimezonedata-attribute"></a><span data-ttu-id="8fc61-115">ReturnFullTimeZoneData 属性</span><span class="sxs-lookup"><span data-stu-id="8fc61-115">ReturnFullTimeZoneData Attribute</span></span>

|<span data-ttu-id="8fc61-116">**值**</span><span class="sxs-lookup"><span data-stu-id="8fc61-116">**Value**</span></span>|<span data-ttu-id="8fc61-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="8fc61-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8fc61-118">**true**</span><span class="sxs-lookup"><span data-stu-id="8fc61-118">**true**</span></span> <br/> |<span data-ttu-id="8fc61-119">返回每个时区的完整定义。</span><span class="sxs-lookup"><span data-stu-id="8fc61-119">Return the complete definitions for each time zone.</span></span>  <br/> |
|<span data-ttu-id="8fc61-120">**该值**</span><span class="sxs-lookup"><span data-stu-id="8fc61-120">**false**</span></span> <br/> |<span data-ttu-id="8fc61-121">仅返回每个时区的名称和标识符。</span><span class="sxs-lookup"><span data-stu-id="8fc61-121">Return only the name and identifier for each time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8fc61-122">子元素</span><span class="sxs-lookup"><span data-stu-id="8fc61-122">Child elements</span></span>

|<span data-ttu-id="8fc61-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="8fc61-123">**Element**</span></span>|<span data-ttu-id="8fc61-124">**描述**</span><span class="sxs-lookup"><span data-stu-id="8fc61-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8fc61-125">Id</span><span class="sxs-lookup"><span data-stu-id="8fc61-125">Ids</span></span>](ids.md) <br/> |<span data-ttu-id="8fc61-126">包含时区定义标识符的数组，该数组指定请求的时区定义。</span><span class="sxs-lookup"><span data-stu-id="8fc61-126">Contains an array of time zone definition identifiers that specifies the requested time zone definitions.</span></span> <span data-ttu-id="8fc61-127">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="8fc61-127">This element is optional.</span></span> <span data-ttu-id="8fc61-128">如果此元素未包含在[GetServerTimeZones 操作](getservertimezones-operation.md)请求中，则会在响应中返回服务器上可用的所有时区定义。</span><span class="sxs-lookup"><span data-stu-id="8fc61-128">If this element is not included in the [GetServerTimeZones operation](getservertimezones-operation.md) request, all time zone definitions that are available on the server are returned in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8fc61-129">父元素</span><span class="sxs-lookup"><span data-stu-id="8fc61-129">Parent elements</span></span>

<span data-ttu-id="8fc61-130">无。</span><span class="sxs-lookup"><span data-stu-id="8fc61-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8fc61-131">说明</span><span class="sxs-lookup"><span data-stu-id="8fc61-131">Remarks</span></span>

<span data-ttu-id="8fc61-132">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8fc61-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8fc61-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="8fc61-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8fc61-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="8fc61-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8fc61-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="8fc61-135">Schema Name</span></span>  <br/> |<span data-ttu-id="8fc61-136">消息架构</span><span class="sxs-lookup"><span data-stu-id="8fc61-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8fc61-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="8fc61-137">Validation File</span></span>  <br/> |<span data-ttu-id="8fc61-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8fc61-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8fc61-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="8fc61-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="8fc61-140">False</span><span class="sxs-lookup"><span data-stu-id="8fc61-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8fc61-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8fc61-141">See also</span></span>



[<span data-ttu-id="8fc61-142">GetServerTimeZones 操作</span><span class="sxs-lookup"><span data-stu-id="8fc61-142">GetServerTimeZones operation</span></span>](getservertimezones-operation.md)
  
[<span data-ttu-id="8fc61-143">GetServerTimeZonesResponse</span><span class="sxs-lookup"><span data-stu-id="8fc61-143">GetServerTimeZonesResponse</span></span>](getservertimezonesresponse.md)


- [<span data-ttu-id="8fc61-144">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8fc61-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

