---
title: Id
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Ids
api_type:
- schema
ms.assetid: c54cdeaf-6761-4d1a-a329-fb279f0e2a64
description: Ids 元素包含时区定义标识符的数组。
ms.openlocfilehash: 1c5a6974c8d3abc318ff122f3db09d8c3472dc65
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457618"
---
# <a name="ids"></a><span data-ttu-id="9ccbd-103">Id</span><span class="sxs-lookup"><span data-stu-id="9ccbd-103">Ids</span></span>

<span data-ttu-id="9ccbd-104">**Ids**元素包含时区定义标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="9ccbd-104">The **Ids** element contains an array of time zone definition identifiers.</span></span> 
  
```XML
<Ids>
   <Id/>
</Ids>
```

 <span data-ttu-id="9ccbd-105">**NonEmptyArrayOfTimeZoneIdType**</span><span class="sxs-lookup"><span data-stu-id="9ccbd-105">**NonEmptyArrayOfTimeZoneIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9ccbd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9ccbd-106">Attributes and elements</span></span>

<span data-ttu-id="9ccbd-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9ccbd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9ccbd-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9ccbd-108">Attributes</span></span>

<span data-ttu-id="9ccbd-109">无。</span><span class="sxs-lookup"><span data-stu-id="9ccbd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9ccbd-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9ccbd-110">Child elements</span></span>

|<span data-ttu-id="9ccbd-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="9ccbd-111">**Element**</span></span>|<span data-ttu-id="9ccbd-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="9ccbd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9ccbd-113">Id （时区）</span><span class="sxs-lookup"><span data-stu-id="9ccbd-113">Id (TimeZone)</span></span>](id-timezone.md) <br/> |<span data-ttu-id="9ccbd-114">标识单个时区定义的元素。</span><span class="sxs-lookup"><span data-stu-id="9ccbd-114">The element that identifies a single time zone definition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9ccbd-115">父元素</span><span class="sxs-lookup"><span data-stu-id="9ccbd-115">Parent elements</span></span>

|<span data-ttu-id="9ccbd-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="9ccbd-116">**Element**</span></span>|<span data-ttu-id="9ccbd-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="9ccbd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9ccbd-118">GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="9ccbd-118">GetServerTimeZones</span></span>](getservertimezones.md) <br/> |<span data-ttu-id="9ccbd-119">定义从 Exchange 服务器检索时区定义的请求。</span><span class="sxs-lookup"><span data-stu-id="9ccbd-119">Defines a request to retrieve time zone definitions from the Exchange server.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="9ccbd-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="9ccbd-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ccbd-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="9ccbd-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9ccbd-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="9ccbd-122">Schema Name</span></span>  <br/> |<span data-ttu-id="9ccbd-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="9ccbd-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9ccbd-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="9ccbd-124">Validation File</span></span>  <br/> |<span data-ttu-id="9ccbd-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9ccbd-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9ccbd-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="9ccbd-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="9ccbd-127">False</span><span class="sxs-lookup"><span data-stu-id="9ccbd-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9ccbd-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9ccbd-128">See also</span></span>



- [<span data-ttu-id="9ccbd-129">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9ccbd-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

