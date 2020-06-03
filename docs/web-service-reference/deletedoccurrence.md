---
title: DeletedOccurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeletedOccurrence
api_type:
- schema
ms.assetid: ff24ea15-0cd7-407d-a378-73ec16451870
description: DeletedOccurrence 元素表示定期日历项目的已删除事件。
ms.openlocfilehash: 814a81934786963ae5e7ea3a40406834c27b64ce
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457835"
---
# <a name="deletedoccurrence"></a><span data-ttu-id="a2fca-103">DeletedOccurrence</span><span class="sxs-lookup"><span data-stu-id="a2fca-103">DeletedOccurrence</span></span>

<span data-ttu-id="a2fca-104">**DeletedOccurrence**元素表示定期日历项目的已删除事件。</span><span class="sxs-lookup"><span data-stu-id="a2fca-104">The **DeletedOccurrence** element represents a deleted occurrence of a recurring calendar item.</span></span> 
  
```xml
<DeletedOccurrence>
   <Start/>
</DeletedOccurrence>
```

 <span data-ttu-id="a2fca-105">**DeletedOccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="a2fca-105">**DeletedOccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a2fca-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a2fca-106">Attributes and elements</span></span>

<span data-ttu-id="a2fca-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a2fca-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a2fca-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a2fca-108">Attributes</span></span>

<span data-ttu-id="a2fca-109">无。</span><span class="sxs-lookup"><span data-stu-id="a2fca-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a2fca-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a2fca-110">Child elements</span></span>

|<span data-ttu-id="a2fca-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a2fca-111">**Element**</span></span>|<span data-ttu-id="a2fca-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a2fca-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a2fca-113">Start</span><span class="sxs-lookup"><span data-stu-id="a2fca-113">Start</span></span>](start.md) <br/> |<span data-ttu-id="a2fca-114">表示定期日历项目的已删除事件的开始时间。</span><span class="sxs-lookup"><span data-stu-id="a2fca-114">Represents the start time of a deleted occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a2fca-115">父元素</span><span class="sxs-lookup"><span data-stu-id="a2fca-115">Parent elements</span></span>

|<span data-ttu-id="a2fca-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="a2fca-116">**Element**</span></span>|<span data-ttu-id="a2fca-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="a2fca-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a2fca-118">DeletedOccurrences</span><span class="sxs-lookup"><span data-stu-id="a2fca-118">DeletedOccurrences</span></span>](deletedoccurrences.md) <br/> |<span data-ttu-id="a2fca-119">包含定期日历项目的已删除事件数组。</span><span class="sxs-lookup"><span data-stu-id="a2fca-119">Contains an array of deleted occurrences of a recurring calendar item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2fca-120">说明</span><span class="sxs-lookup"><span data-stu-id="a2fca-120">Remarks</span></span>

<span data-ttu-id="a2fca-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a2fca-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a2fca-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="a2fca-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2fca-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="a2fca-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a2fca-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="a2fca-124">Schema name</span></span>  <br/> |<span data-ttu-id="a2fca-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="a2fca-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="a2fca-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="a2fca-126">Validation file</span></span>  <br/> |<span data-ttu-id="a2fca-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a2fca-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a2fca-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="a2fca-128">Can be empty</span></span>  <br/> |<span data-ttu-id="a2fca-129">False</span><span class="sxs-lookup"><span data-stu-id="a2fca-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a2fca-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a2fca-130">See also</span></span>

- [<span data-ttu-id="a2fca-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a2fca-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)  
- [<span data-ttu-id="a2fca-132">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="a2fca-132">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

