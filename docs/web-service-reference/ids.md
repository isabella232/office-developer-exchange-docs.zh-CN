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
description: Id 元素中包含时区定义标识符的数组。
ms.openlocfilehash: e4f8afb1292b3cb9f3990d4613b7461050976a59
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825856"
---
# <a name="ids"></a><span data-ttu-id="d3b9b-103">Id</span><span class="sxs-lookup"><span data-stu-id="d3b9b-103">Ids</span></span>

<span data-ttu-id="d3b9b-104">**Id**元素中包含时区定义标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="d3b9b-104">The **Ids** element contains an array of time zone definition identifiers.</span></span> 
  
```XML
<Ids>
   <Id/>
</Ids>
```

 <span data-ttu-id="d3b9b-105">**NonEmptyArrayOfTimeZoneIdType**</span><span class="sxs-lookup"><span data-stu-id="d3b9b-105">**NonEmptyArrayOfTimeZoneIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d3b9b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d3b9b-106">Attributes and elements</span></span>

<span data-ttu-id="d3b9b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d3b9b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d3b9b-108">属性</span><span class="sxs-lookup"><span data-stu-id="d3b9b-108">Attributes</span></span>

<span data-ttu-id="d3b9b-109">无。</span><span class="sxs-lookup"><span data-stu-id="d3b9b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d3b9b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d3b9b-110">Child elements</span></span>

|<span data-ttu-id="d3b9b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d3b9b-111">**Element**</span></span>|<span data-ttu-id="d3b9b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d3b9b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3b9b-113">Id (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="d3b9b-113">Id (TimeZone)</span></span>](id-timezone.md) <br/> |<span data-ttu-id="d3b9b-114">标识一个时区定义的元素。</span><span class="sxs-lookup"><span data-stu-id="d3b9b-114">The element that identifies a single time zone definition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d3b9b-115">父元素</span><span class="sxs-lookup"><span data-stu-id="d3b9b-115">Parent elements</span></span>

|<span data-ttu-id="d3b9b-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="d3b9b-116">**Element**</span></span>|<span data-ttu-id="d3b9b-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="d3b9b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3b9b-118">GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="d3b9b-118">GetServerTimeZones</span></span>](getservertimezones.md) <br/> |<span data-ttu-id="d3b9b-119">定义从 Exchange 服务器中检索时区定义的请求。</span><span class="sxs-lookup"><span data-stu-id="d3b9b-119">Defines a request to retrieve time zone definitions from the Exchange server.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="d3b9b-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="d3b9b-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3b9b-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="d3b9b-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d3b9b-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="d3b9b-122">Schema Name</span></span>  <br/> |<span data-ttu-id="d3b9b-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="d3b9b-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d3b9b-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="d3b9b-124">Validation File</span></span>  <br/> |<span data-ttu-id="d3b9b-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d3b9b-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d3b9b-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="d3b9b-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="d3b9b-127">False</span><span class="sxs-lookup"><span data-stu-id="d3b9b-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d3b9b-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d3b9b-128">See also</span></span>



- [<span data-ttu-id="d3b9b-129">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d3b9b-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

