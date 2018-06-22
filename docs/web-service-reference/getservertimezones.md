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
description: GetServerTimeZones 元素是从 Exchange 服务器中检索时区定义的请求中的根元素。
ms.openlocfilehash: 1ad503ff312497189f57bce9a3670571aedad5ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754688"
---
# <a name="getservertimezones"></a><span data-ttu-id="264e4-103">GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="264e4-103">GetServerTimeZones</span></span>

<span data-ttu-id="264e4-104">**GetServerTimeZones**元素是从 Exchange 服务器中检索时区定义的请求中的根元素。</span><span class="sxs-lookup"><span data-stu-id="264e4-104">The **GetServerTimeZones** element is the root element in a request to retrieve time zone definitions from the Exchange server.</span></span> 
  
```xml
<GetServerTimeZones ReturnFullTimeZoneData="">   <Ids/></GetServerTimeZones>
```

 <span data-ttu-id="264e4-105">**GetServerTimeZonesType**</span><span class="sxs-lookup"><span data-stu-id="264e4-105">**GetServerTimeZonesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="264e4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="264e4-106">Attributes and elements</span></span>

<span data-ttu-id="264e4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="264e4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="264e4-108">属性</span><span class="sxs-lookup"><span data-stu-id="264e4-108">Attributes</span></span>

|<span data-ttu-id="264e4-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="264e4-109">**Attribute**</span></span>|<span data-ttu-id="264e4-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="264e4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="264e4-111">**ReturnFullTimeZoneData**</span><span class="sxs-lookup"><span data-stu-id="264e4-111">**ReturnFullTimeZoneData**</span></span> <br/> |<span data-ttu-id="264e4-112">指定是否[GetServerTimeZones 操作](getservertimezones-operation.md)的完整定义或只返回名称和每个时区的标识符。</span><span class="sxs-lookup"><span data-stu-id="264e4-112">Specifies whether the [GetServerTimeZones operation](getservertimezones-operation.md) returns the complete definition or only the name and identifier for each time zone.</span></span> <span data-ttu-id="264e4-113">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="264e4-113">This attribute is optional.</span></span> <span data-ttu-id="264e4-114">默认值为 **true** 。</span><span class="sxs-lookup"><span data-stu-id="264e4-114">The default value is **true**.</span></span>  <br/> |
   
#### <a name="returnfulltimezonedata-attribute"></a><span data-ttu-id="264e4-115">ReturnFullTimeZoneData 属性</span><span class="sxs-lookup"><span data-stu-id="264e4-115">ReturnFullTimeZoneData Attribute</span></span>

|<span data-ttu-id="264e4-116">**值**</span><span class="sxs-lookup"><span data-stu-id="264e4-116">**Value**</span></span>|<span data-ttu-id="264e4-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="264e4-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="264e4-118">**true**</span><span class="sxs-lookup"><span data-stu-id="264e4-118">**true**</span></span> <br/> |<span data-ttu-id="264e4-119">返回每个时区的完整定义。</span><span class="sxs-lookup"><span data-stu-id="264e4-119">Return the complete definitions for each time zone.</span></span>  <br/> |
|<span data-ttu-id="264e4-120">**false**</span><span class="sxs-lookup"><span data-stu-id="264e4-120">**false**</span></span> <br/> |<span data-ttu-id="264e4-121">返回仅的名称和为每个时区的标识符。</span><span class="sxs-lookup"><span data-stu-id="264e4-121">Return only the name and identifier for each time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="264e4-122">子元素</span><span class="sxs-lookup"><span data-stu-id="264e4-122">Child elements</span></span>

|<span data-ttu-id="264e4-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="264e4-123">**Element**</span></span>|<span data-ttu-id="264e4-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="264e4-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="264e4-125">Id</span><span class="sxs-lookup"><span data-stu-id="264e4-125">Ids</span></span>](ids.md) <br/> |<span data-ttu-id="264e4-126">包含指定的请求的所在的时区定义的时区定义标识符数组。</span><span class="sxs-lookup"><span data-stu-id="264e4-126">Contains an array of time zone definition identifiers that specifies the requested time zone definitions.</span></span> <span data-ttu-id="264e4-127">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="264e4-127">This element is optional.</span></span> <span data-ttu-id="264e4-128">如果此元素不包括[GetServerTimeZones 操作](getservertimezones-operation.md)请求中，可在服务器上的所有所在的时区定义的响应中都返回。</span><span class="sxs-lookup"><span data-stu-id="264e4-128">If this element is not included in the [GetServerTimeZones operation](getservertimezones-operation.md) request, all time zone definitions that are available on the server are returned in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="264e4-129">父元素</span><span class="sxs-lookup"><span data-stu-id="264e4-129">Parent elements</span></span>

<span data-ttu-id="264e4-130">无。</span><span class="sxs-lookup"><span data-stu-id="264e4-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="264e4-131">备注</span><span class="sxs-lookup"><span data-stu-id="264e4-131">Remarks</span></span>

<span data-ttu-id="264e4-132">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="264e4-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="264e4-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="264e4-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="264e4-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="264e4-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="264e4-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="264e4-135">Schema Name</span></span>  <br/> |<span data-ttu-id="264e4-136">消息架构</span><span class="sxs-lookup"><span data-stu-id="264e4-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="264e4-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="264e4-137">Validation File</span></span>  <br/> |<span data-ttu-id="264e4-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="264e4-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="264e4-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="264e4-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="264e4-140">False</span><span class="sxs-lookup"><span data-stu-id="264e4-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="264e4-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="264e4-141">See also</span></span>



[<span data-ttu-id="264e4-142">GetServerTimeZones 操作</span><span class="sxs-lookup"><span data-stu-id="264e4-142">GetServerTimeZones operation</span></span>](getservertimezones-operation.md)
  
[<span data-ttu-id="264e4-143">GetServerTimeZonesResponse</span><span class="sxs-lookup"><span data-stu-id="264e4-143">GetServerTimeZonesResponse</span></span>](getservertimezonesresponse.md)


- [<span data-ttu-id="264e4-144">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="264e4-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

