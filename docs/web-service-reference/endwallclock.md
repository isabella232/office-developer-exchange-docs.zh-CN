---
title: EndWallClock
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bc04e44e-e6d1-4355-a2b1-feb6663dc647
description: EndWallClock 元素指定时区会议发生的位置中的会议的结束时间。
ms.openlocfilehash: 10e4a2bde50354b2f2752751c01a6a70aa084d05
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754124"
---
# <a name="endwallclock"></a><span data-ttu-id="bb491-103">EndWallClock</span><span class="sxs-lookup"><span data-stu-id="bb491-103">EndWallClock</span></span>

<span data-ttu-id="bb491-104">**EndWallClock**元素指定时区会议发生的位置中的会议的结束时间。</span><span class="sxs-lookup"><span data-stu-id="bb491-104">The **EndWallClock** element specifies the end time of a meeting in the time zone of the location in which the meeting takes place.</span></span> 
  
```XML
<EndWallClock></EndWallClock>
```

 <span data-ttu-id="bb491-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="bb491-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bb491-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bb491-106">Attributes and elements</span></span>

<span data-ttu-id="bb491-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bb491-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb491-108">属性</span><span class="sxs-lookup"><span data-stu-id="bb491-108">Attributes</span></span>

<span data-ttu-id="bb491-109">无。</span><span class="sxs-lookup"><span data-stu-id="bb491-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bb491-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bb491-110">Child elements</span></span>

<span data-ttu-id="bb491-111">无。</span><span class="sxs-lookup"><span data-stu-id="bb491-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bb491-112">父元素</span><span class="sxs-lookup"><span data-stu-id="bb491-112">Parent elements</span></span>

|<span data-ttu-id="bb491-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="bb491-113">**Element**</span></span>|<span data-ttu-id="bb491-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="bb491-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb491-115">角色</span><span class="sxs-lookup"><span data-stu-id="bb491-115">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="bb491-116">指定一组个人**GetPersona**请求返回的数据。</span><span class="sxs-lookup"><span data-stu-id="bb491-116">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bb491-117">文本值</span><span class="sxs-lookup"><span data-stu-id="bb491-117">Text value</span></span>

<span data-ttu-id="bb491-118">**EndWallClock**元素的文本值是一个 string 值，指定时区标识符。</span><span class="sxs-lookup"><span data-stu-id="bb491-118">The text value of the **EndWallClock** element is a string value that specifies the time zone identifier.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bb491-119">备注</span><span class="sxs-lookup"><span data-stu-id="bb491-119">Remarks</span></span>

<span data-ttu-id="bb491-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="bb491-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="bb491-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bb491-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bb491-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="bb491-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb491-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="bb491-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bb491-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="bb491-124">Schema Name</span></span>  <br/> |<span data-ttu-id="bb491-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="bb491-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="bb491-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="bb491-126">Validation File</span></span>  <br/> |<span data-ttu-id="bb491-127">types.xsd</span><span class="sxs-lookup"><span data-stu-id="bb491-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="bb491-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="bb491-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="bb491-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bb491-129">See also</span></span>



- [<span data-ttu-id="bb491-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bb491-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

