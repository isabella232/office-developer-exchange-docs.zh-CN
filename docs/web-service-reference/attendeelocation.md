---
title: AttendeeLocation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1344a087-88ea-472a-bebf-9b45245592fb
description: AttendeeLocation 元素指定日历项目的与会者的位置。
ms.openlocfilehash: 34a4ee8ea5f4c59cce6eebd8977bd4733f7c7134
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460342"
---
# <a name="attendeelocation"></a><span data-ttu-id="2f141-103">AttendeeLocation</span><span class="sxs-lookup"><span data-stu-id="2f141-103">AttendeeLocation</span></span>

<span data-ttu-id="2f141-104">**AttendeeLocation**元素指定日历项目的与会者的位置。</span><span class="sxs-lookup"><span data-stu-id="2f141-104">The **AttendeeLocation** element specifies the location of an attendee for a calendar item.</span></span> 
  
```XML
<AttendeeLocation></AttendeeLocation>
```

 <span data-ttu-id="2f141-105">**xs： string**</span><span class="sxs-lookup"><span data-stu-id="2f141-105">**xs:string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2f141-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2f141-106">Attributes and elements</span></span>

<span data-ttu-id="2f141-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2f141-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f141-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2f141-108">Attributes</span></span>

<span data-ttu-id="2f141-109">无。</span><span class="sxs-lookup"><span data-stu-id="2f141-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2f141-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2f141-110">Child elements</span></span>

<span data-ttu-id="2f141-111">无。</span><span class="sxs-lookup"><span data-stu-id="2f141-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2f141-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2f141-112">Parent elements</span></span>

|<span data-ttu-id="2f141-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="2f141-113">**Element**</span></span>|<span data-ttu-id="2f141-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="2f141-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f141-115">LocationBasedStateDefinition</span><span class="sxs-lookup"><span data-stu-id="2f141-115">LocationBasedStateDefinition</span></span>](locationbasedstatedefinition.md) <br/> |<span data-ttu-id="2f141-116">指定当它基于位置时的状态。</span><span class="sxs-lookup"><span data-stu-id="2f141-116">Specifies the state when it is based on location.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2f141-117">文本值</span><span class="sxs-lookup"><span data-stu-id="2f141-117">Text value</span></span>

<span data-ttu-id="2f141-118">AttendeeLocation 元素的文本值是 attendess 位置。</span><span class="sxs-lookup"><span data-stu-id="2f141-118">The text value of the AttendeeLocation element is the attendess location.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2f141-119">备注</span><span class="sxs-lookup"><span data-stu-id="2f141-119">Remarks</span></span>

<span data-ttu-id="2f141-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2f141-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2f141-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2f141-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f141-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="2f141-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f141-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="2f141-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2f141-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="2f141-124">Schema Name</span></span>  <br/> |<span data-ttu-id="2f141-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="2f141-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="2f141-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="2f141-126">Validation File</span></span>  <br/> |<span data-ttu-id="2f141-127">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="2f141-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2f141-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="2f141-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2f141-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2f141-129">See also</span></span>

- [<span data-ttu-id="2f141-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2f141-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

