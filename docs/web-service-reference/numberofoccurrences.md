---
title: NumberOfOccurrences
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NumberOfOccurrences
api_type:
- schema
ms.assetid: 9ec86ceb-b271-4718-97ca-b6a532ea7223
description: NumberOfOccurrences 元素包含定期项目的次数。
ms.openlocfilehash: f9b72611e87c5f2b98deb14c25988e574a324491
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462540"
---
# <a name="numberofoccurrences"></a><span data-ttu-id="ae80f-103">NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="ae80f-103">NumberOfOccurrences</span></span>

<span data-ttu-id="ae80f-104">**NumberOfOccurrences**元素包含定期项目的次数。</span><span class="sxs-lookup"><span data-stu-id="ae80f-104">The **NumberOfOccurrences** element contains the number of occurrences of a recurring item.</span></span> 
  
```xml
<NumberOfOccurrences/>
```

 <span data-ttu-id="ae80f-105">**int**</span><span class="sxs-lookup"><span data-stu-id="ae80f-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ae80f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ae80f-106">Attributes and elements</span></span>

<span data-ttu-id="ae80f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ae80f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae80f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ae80f-108">Attributes</span></span>

<span data-ttu-id="ae80f-109">无。</span><span class="sxs-lookup"><span data-stu-id="ae80f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae80f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ae80f-110">Child elements</span></span>

<span data-ttu-id="ae80f-111">无。</span><span class="sxs-lookup"><span data-stu-id="ae80f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ae80f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ae80f-112">Parent elements</span></span>

|<span data-ttu-id="ae80f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="ae80f-113">**Element**</span></span>|<span data-ttu-id="ae80f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="ae80f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae80f-115">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="ae80f-115">NumberedRecurrence</span></span>](numberedrecurrence.md) <br/> |<span data-ttu-id="ae80f-116">描述定期项目的开始日期和发生次数。</span><span class="sxs-lookup"><span data-stu-id="ae80f-116">Describes the start date and the number of occurrences of a recurring item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ae80f-117">文本值</span><span class="sxs-lookup"><span data-stu-id="ae80f-117">Text value</span></span>

<span data-ttu-id="ae80f-118">Text 值是一个整数，表示定期项目的次数。</span><span class="sxs-lookup"><span data-stu-id="ae80f-118">The text value is an integer that represents the number of occurrences of a recurring item.</span></span> <span data-ttu-id="ae80f-119">该值必须是介于1到999之间的整数。</span><span class="sxs-lookup"><span data-stu-id="ae80f-119">The value must be an integer in the range of 1 to 999.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ae80f-120">说明</span><span class="sxs-lookup"><span data-stu-id="ae80f-120">Remarks</span></span>

<span data-ttu-id="ae80f-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ae80f-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae80f-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="ae80f-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae80f-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="ae80f-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ae80f-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="ae80f-124">Schema name</span></span>  <br/> |<span data-ttu-id="ae80f-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="ae80f-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="ae80f-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="ae80f-126">Validation file</span></span>  <br/> |<span data-ttu-id="ae80f-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ae80f-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ae80f-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="ae80f-128">Can be empty</span></span>  <br/> |<span data-ttu-id="ae80f-129">False</span><span class="sxs-lookup"><span data-stu-id="ae80f-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae80f-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ae80f-130">See also</span></span>



- [<span data-ttu-id="ae80f-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ae80f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

