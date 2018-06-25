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
description: DeletedOccurrence 元素均表示定期日历项目的已删除的匹配项。
ms.openlocfilehash: f12a2ba20f87f7803e492d8422b68c8ecdf9d797
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753794"
---
# <a name="deletedoccurrence"></a><span data-ttu-id="fb273-103">DeletedOccurrence</span><span class="sxs-lookup"><span data-stu-id="fb273-103">DeletedOccurrence</span></span>

<span data-ttu-id="fb273-104">**DeletedOccurrence**元素均表示定期日历项目的已删除的匹配项。</span><span class="sxs-lookup"><span data-stu-id="fb273-104">The **DeletedOccurrence** element represents a deleted occurrence of a recurring calendar item.</span></span> 
  
```xml
<DeletedOccurrence>
   <Start/>
</DeletedOccurrence>
```

 <span data-ttu-id="fb273-105">**DeletedOccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="fb273-105">**DeletedOccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fb273-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fb273-106">Attributes and elements</span></span>

<span data-ttu-id="fb273-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fb273-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fb273-108">属性</span><span class="sxs-lookup"><span data-stu-id="fb273-108">Attributes</span></span>

<span data-ttu-id="fb273-109">无。</span><span class="sxs-lookup"><span data-stu-id="fb273-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fb273-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fb273-110">Child elements</span></span>

|<span data-ttu-id="fb273-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="fb273-111">**Element**</span></span>|<span data-ttu-id="fb273-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="fb273-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fb273-113">Start</span><span class="sxs-lookup"><span data-stu-id="fb273-113">Start</span></span>](start.md) <br/> |<span data-ttu-id="fb273-114">代表已删除的匹配项的定期日历项目的开始时间。</span><span class="sxs-lookup"><span data-stu-id="fb273-114">Represents the start time of a deleted occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fb273-115">父元素</span><span class="sxs-lookup"><span data-stu-id="fb273-115">Parent elements</span></span>

|<span data-ttu-id="fb273-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="fb273-116">**Element**</span></span>|<span data-ttu-id="fb273-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="fb273-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fb273-118">DeletedOccurrences</span><span class="sxs-lookup"><span data-stu-id="fb273-118">DeletedOccurrences</span></span>](deletedoccurrences.md) <br/> |<span data-ttu-id="fb273-119">包含数组的定期日历项目的已删除匹配项。</span><span class="sxs-lookup"><span data-stu-id="fb273-119">Contains an array of deleted occurrences of a recurring calendar item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb273-120">备注</span><span class="sxs-lookup"><span data-stu-id="fb273-120">Remarks</span></span>

<span data-ttu-id="fb273-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fb273-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fb273-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="fb273-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb273-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="fb273-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fb273-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="fb273-124">Schema name</span></span>  <br/> |<span data-ttu-id="fb273-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="fb273-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="fb273-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="fb273-126">Validation file</span></span>  <br/> |<span data-ttu-id="fb273-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fb273-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fb273-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="fb273-128">Can be empty</span></span>  <br/> |<span data-ttu-id="fb273-129">False</span><span class="sxs-lookup"><span data-stu-id="fb273-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fb273-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fb273-130">See also</span></span>

- [<span data-ttu-id="fb273-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fb273-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)  
- [<span data-ttu-id="fb273-132">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="fb273-132">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

