---
title: 重复
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
description: 具体值元素表示定期日历项目的单个修改事件。
ms.openlocfilehash: c3a6bcce23f0bb1125dbd2a5bb86e9b20039a4e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466316"
---
# <a name="occurrence"></a><span data-ttu-id="64056-103">重复</span><span class="sxs-lookup"><span data-stu-id="64056-103">Occurrence</span></span>

<span data-ttu-id="64056-104">**具体**值元素表示定期日历项目的单个修改事件。</span><span class="sxs-lookup"><span data-stu-id="64056-104">The **Occurrence** element represents a single modified occurrence of a recurring calendar item.</span></span> 
  
```xml
<Occurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</Occurrence>
```

<span data-ttu-id="64056-105">**OccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="64056-105">**OccurrenceInfoType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="64056-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="64056-106">Attributes and elements</span></span>

<span data-ttu-id="64056-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="64056-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="64056-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="64056-108">Attributes</span></span>

<span data-ttu-id="64056-109">无。</span><span class="sxs-lookup"><span data-stu-id="64056-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="64056-110">子元素</span><span class="sxs-lookup"><span data-stu-id="64056-110">Child elements</span></span>

|<span data-ttu-id="64056-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="64056-111">**Element**</span></span>|<span data-ttu-id="64056-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="64056-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="64056-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="64056-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="64056-114">包含定期日历项目的已修改事件的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="64056-114">Contains the unique identifier and change key of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="64056-115">开始</span><span class="sxs-lookup"><span data-stu-id="64056-115">Start</span></span>](start.md) <br/> |<span data-ttu-id="64056-116">表示定期日历项目的已修改事件的开始时间。</span><span class="sxs-lookup"><span data-stu-id="64056-116">Represents the start time of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="64056-117">停止</span><span class="sxs-lookup"><span data-stu-id="64056-117">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="64056-118">表示定期日历项目的已修改事件的结束时间。</span><span class="sxs-lookup"><span data-stu-id="64056-118">Represents the end time of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="64056-119">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="64056-119">OriginalStart</span></span>](originalstart.md) <br/> |<span data-ttu-id="64056-120">表示定期日历项目的已修改事件的原始开始时间。</span><span class="sxs-lookup"><span data-stu-id="64056-120">Represents the original start time of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="64056-121">父元素</span><span class="sxs-lookup"><span data-stu-id="64056-121">Parent elements</span></span>

|<span data-ttu-id="64056-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="64056-122">**Element**</span></span>|<span data-ttu-id="64056-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="64056-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="64056-124">ModifiedOccurrences</span><span class="sxs-lookup"><span data-stu-id="64056-124">ModifiedOccurrences</span></span>](modifiedoccurrences.md) <br/> |<span data-ttu-id="64056-125">包含已修改的定期日历项目匹配项的集合，以便它们不同于定期主项目。</span><span class="sxs-lookup"><span data-stu-id="64056-125">Contains a collection of recurring calendar item occurrences that have been modified so that they are different than the recurrence master item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64056-126">说明</span><span class="sxs-lookup"><span data-stu-id="64056-126">Remarks</span></span>

<span data-ttu-id="64056-127">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="64056-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="64056-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="64056-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64056-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="64056-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="64056-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="64056-130">Schema name</span></span>  <br/> |<span data-ttu-id="64056-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="64056-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="64056-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="64056-132">Validation file</span></span>  <br/> |<span data-ttu-id="64056-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="64056-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="64056-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="64056-134">Can be empty</span></span>  <br/> |<span data-ttu-id="64056-135">False</span><span class="sxs-lookup"><span data-stu-id="64056-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="64056-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="64056-136">See also</span></span>

- [<span data-ttu-id="64056-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="64056-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

