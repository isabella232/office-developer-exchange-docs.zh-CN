---
title: DeleteFromFolderStateDefinition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3aba59a0-f12a-48b5-842b-11cf4530dd51
description: DeleteFromFolderStateDefinition 元素指定从文件夹中删除项目时的状态。
ms.openlocfilehash: 0ea8c61a6839790869781d5d87ca81772b2e38d6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455721"
---
# <a name="deletefromfolderstatedefinition"></a><span data-ttu-id="f7d75-103">DeleteFromFolderStateDefinition</span><span class="sxs-lookup"><span data-stu-id="f7d75-103">DeleteFromFolderStateDefinition</span></span>

<span data-ttu-id="f7d75-104">**DeleteFromFolderStateDefinition**元素指定从文件夹中删除项目时的状态。</span><span class="sxs-lookup"><span data-stu-id="f7d75-104">The **DeleteFromFolderStateDefinition** element specifies the state when an item is deleted from a folder.</span></span> 
  
```XML
<DeleteFromFolderStateDefinition>
    <OccurrenceDate></OccurrenceDate>
    <IsOccurrencePresent></IsOccurrencePresent>
</DeleteFromFolderStateDefinition>
```

 <span data-ttu-id="f7d75-105">**DeleteFromFolderStateDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="f7d75-105">**DeleteFromFolderStateDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f7d75-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f7d75-106">Attributes and elements</span></span>

<span data-ttu-id="f7d75-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f7d75-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f7d75-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f7d75-108">Attributes</span></span>

<span data-ttu-id="f7d75-109">无。</span><span class="sxs-lookup"><span data-stu-id="f7d75-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f7d75-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f7d75-110">Child elements</span></span>

|<span data-ttu-id="f7d75-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f7d75-111">**Element**</span></span>|<span data-ttu-id="f7d75-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f7d75-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7d75-113">事件（时区转换）</span><span class="sxs-lookup"><span data-stu-id="f7d75-113">Occurrence (Time Zone Transition)</span></span>](occurrence-time-zone-transition.md) <br/> |<span data-ttu-id="f7d75-114">指定日历项的发生日期。</span><span class="sxs-lookup"><span data-stu-id="f7d75-114">Specifies the date of the occurrence of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f7d75-115">IsOccurrencePresent</span><span class="sxs-lookup"><span data-stu-id="f7d75-115">IsOccurrencePresent</span></span>](isoccurrencepresent.md) <br/> |<span data-ttu-id="f7d75-116">指定一个布尔值，该值指示是否存在日历项。</span><span class="sxs-lookup"><span data-stu-id="f7d75-116">Specifies a Boolean value that indicates whether an occurrence of the calendar item is present.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f7d75-117">父元素</span><span class="sxs-lookup"><span data-stu-id="f7d75-117">Parent elements</span></span>

|<span data-ttu-id="f7d75-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="f7d75-118">**Element**</span></span>|<span data-ttu-id="f7d75-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="f7d75-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7d75-120">StateDefinition</span><span class="sxs-lookup"><span data-stu-id="f7d75-120">StateDefinition</span></span>](statedefinition.md) <br/> |<span data-ttu-id="f7d75-121">指定状态定义。</span><span class="sxs-lookup"><span data-stu-id="f7d75-121">Specifies a state definition.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7d75-122">备注</span><span class="sxs-lookup"><span data-stu-id="f7d75-122">Remarks</span></span>

<span data-ttu-id="f7d75-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f7d75-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f7d75-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f7d75-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f7d75-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="f7d75-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7d75-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="f7d75-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f7d75-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="f7d75-127">Schema Name</span></span>  <br/> |<span data-ttu-id="f7d75-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="f7d75-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="f7d75-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="f7d75-129">Validation File</span></span>  <br/> |<span data-ttu-id="f7d75-130">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="f7d75-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f7d75-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="f7d75-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f7d75-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f7d75-132">See also</span></span>

- [<span data-ttu-id="f7d75-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f7d75-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

