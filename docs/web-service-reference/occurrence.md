---
title: 匹配项
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Occurrence
api_type:
- schema
ms.assetid: d292b99c-b896-40b7-be5d-2cb314c9481f
description: 出现元素均表示定期日历项目的一个已修改匹配项。
ms.openlocfilehash: 5a40faa9b885a235d30e7f41830d1eefe2ed23c3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826653"
---
# <a name="occurrence"></a><span data-ttu-id="59878-103">匹配项</span><span class="sxs-lookup"><span data-stu-id="59878-103">Occurrence</span></span>

<span data-ttu-id="59878-104">**出现**元素均表示定期日历项目的一个已修改匹配项。</span><span class="sxs-lookup"><span data-stu-id="59878-104">The **Occurrence** element represents a single modified occurrence of a recurring calendar item.</span></span> 
  
```xml
<Occurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</Occurrence>
```

<span data-ttu-id="59878-105">**OccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="59878-105">**OccurrenceInfoType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="59878-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="59878-106">Attributes and elements</span></span>

<span data-ttu-id="59878-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="59878-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="59878-108">属性</span><span class="sxs-lookup"><span data-stu-id="59878-108">Attributes</span></span>

<span data-ttu-id="59878-109">无。</span><span class="sxs-lookup"><span data-stu-id="59878-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="59878-110">子元素</span><span class="sxs-lookup"><span data-stu-id="59878-110">Child elements</span></span>

|<span data-ttu-id="59878-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="59878-111">**Element**</span></span>|<span data-ttu-id="59878-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="59878-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59878-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="59878-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="59878-114">包含定期日历项目的已修改事件的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="59878-114">Contains the unique identifier and change key of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="59878-115">Start</span><span class="sxs-lookup"><span data-stu-id="59878-115">Start</span></span>](start.md) <br/> |<span data-ttu-id="59878-116">代表已修改事件的定期日历项目的开始时间。</span><span class="sxs-lookup"><span data-stu-id="59878-116">Represents the start time of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="59878-117">结束</span><span class="sxs-lookup"><span data-stu-id="59878-117">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="59878-118">代表定期日历项目的已修改事件的结束时间。</span><span class="sxs-lookup"><span data-stu-id="59878-118">Represents the end time of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="59878-119">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="59878-119">OriginalStart</span></span>](originalstart.md) <br/> |<span data-ttu-id="59878-120">代表定期日历项目的已修改事件的原始开始时间。</span><span class="sxs-lookup"><span data-stu-id="59878-120">Represents the original start time of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="59878-121">父元素</span><span class="sxs-lookup"><span data-stu-id="59878-121">Parent elements</span></span>

|<span data-ttu-id="59878-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="59878-122">**Element**</span></span>|<span data-ttu-id="59878-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="59878-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59878-124">ModifiedOccurrences</span><span class="sxs-lookup"><span data-stu-id="59878-124">ModifiedOccurrences</span></span>](modifiedoccurrences.md) <br/> |<span data-ttu-id="59878-125">包含的定期日历项目匹配项，以便它们是不同的定期主项目已修改的集合。</span><span class="sxs-lookup"><span data-stu-id="59878-125">Contains a collection of recurring calendar item occurrences that have been modified so that they are different than the recurrence master item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59878-126">备注</span><span class="sxs-lookup"><span data-stu-id="59878-126">Remarks</span></span>

<span data-ttu-id="59878-127">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="59878-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="59878-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="59878-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59878-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="59878-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="59878-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="59878-130">Schema name</span></span>  <br/> |<span data-ttu-id="59878-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="59878-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="59878-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="59878-132">Validation file</span></span>  <br/> |<span data-ttu-id="59878-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="59878-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="59878-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="59878-134">Can be empty</span></span>  <br/> |<span data-ttu-id="59878-135">False</span><span class="sxs-lookup"><span data-stu-id="59878-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="59878-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="59878-136">See also</span></span>

- [<span data-ttu-id="59878-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="59878-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

