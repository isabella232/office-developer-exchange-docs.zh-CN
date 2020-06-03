---
title: EndWallClock
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bc04e44e-e6d1-4355-a2b1-feb6663dc647
description: EndWallClock 元素指定会议在发生的位置所在的时区的结束时间。
ms.openlocfilehash: 48b762d0bfe367b966b6f1790230f6a2118c3fd6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462969"
---
# <a name="endwallclock"></a><span data-ttu-id="8705f-103">EndWallClock</span><span class="sxs-lookup"><span data-stu-id="8705f-103">EndWallClock</span></span>

<span data-ttu-id="8705f-104">**EndWallClock**元素指定会议在发生的位置所在的时区的结束时间。</span><span class="sxs-lookup"><span data-stu-id="8705f-104">The **EndWallClock** element specifies the end time of a meeting in the time zone of the location in which the meeting takes place.</span></span> 
  
```XML
<EndWallClock></EndWallClock>
```

 <span data-ttu-id="8705f-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="8705f-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8705f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8705f-106">Attributes and elements</span></span>

<span data-ttu-id="8705f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8705f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8705f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="8705f-108">Attributes</span></span>

<span data-ttu-id="8705f-109">无。</span><span class="sxs-lookup"><span data-stu-id="8705f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8705f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8705f-110">Child elements</span></span>

<span data-ttu-id="8705f-111">无。</span><span class="sxs-lookup"><span data-stu-id="8705f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8705f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8705f-112">Parent elements</span></span>

|<span data-ttu-id="8705f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="8705f-113">**Element**</span></span>|<span data-ttu-id="8705f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="8705f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8705f-115">角色</span><span class="sxs-lookup"><span data-stu-id="8705f-115">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="8705f-116">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="8705f-116">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8705f-117">文本值</span><span class="sxs-lookup"><span data-stu-id="8705f-117">Text value</span></span>

<span data-ttu-id="8705f-118">**EndWallClock**元素的文本值是指定时区标识符的字符串值。</span><span class="sxs-lookup"><span data-stu-id="8705f-118">The text value of the **EndWallClock** element is a string value that specifies the time zone identifier.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8705f-119">备注</span><span class="sxs-lookup"><span data-stu-id="8705f-119">Remarks</span></span>

<span data-ttu-id="8705f-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8705f-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8705f-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8705f-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8705f-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="8705f-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8705f-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="8705f-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8705f-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="8705f-124">Schema Name</span></span>  <br/> |<span data-ttu-id="8705f-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="8705f-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="8705f-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="8705f-126">Validation File</span></span>  <br/> |<span data-ttu-id="8705f-127">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="8705f-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="8705f-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="8705f-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="8705f-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8705f-129">See also</span></span>



- [<span data-ttu-id="8705f-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8705f-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

