---
title: InternetMessageHeader
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InternetMessageHeader
api_type:
- schema
ms.assetid: c70675f8-6feb-4c89-ba48-bce0479b308b
description: InternetMessageHeader 元素均表示给定标题的标头集合中的 Internet 邮件标题。 若要获取的 Internet 邮件头的整个集合，请使用 PR_TRANSPORT_MESSAGE_HEADERS 属性。 有关 EWS 和 Internet 邮件头、 seeGetting EWS、 MIME 和缺少的 Internet 邮件头中的 Internet 邮件头的详细信息。
ms.openlocfilehash: 9457cdabe99c0adcb8183cbc039cc86db881fec7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825952"
---
# <a name="internetmessageheader"></a><span data-ttu-id="58415-105">InternetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="58415-105">InternetMessageHeader</span></span>

<span data-ttu-id="58415-106">**InternetMessageHeader**元素均表示给定标题的标头集合中的 Internet 邮件标题。</span><span class="sxs-lookup"><span data-stu-id="58415-106">The **InternetMessageHeader** element represents the Internet message header for a given header within the headers collection.</span></span> <span data-ttu-id="58415-107">若要获取的 Internet 邮件头的整个集合，请使用**PR_TRANSPORT_MESSAGE_HEADERS**属性。</span><span class="sxs-lookup"><span data-stu-id="58415-107">To get the entire collection of Internet message headers, use the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> <span data-ttu-id="58415-108">有关 EWS 和 Internet 邮件头的详细信息，请参阅["EWS、 MIME 和缺少的 Internet 邮件头](http://msdn.microsoft.com/zh-cn/library/exchange/hh545614%28v=exchg.140%29.aspx)中获取 Internet 邮件头。</span><span class="sxs-lookup"><span data-stu-id="58415-108">For more information about EWS and Internet message headers, see "Getting Internet message headers in [EWS, MIME, and the missing Internet message headers](http://msdn.microsoft.com/zh-cn/library/exchange/hh545614%28v=exchg.140%29.aspx).</span></span>
  
```XML
<InternetMessageHeader HeaderName=""/>
```

 <span data-ttu-id="58415-109">**InternetHeaderType**</span><span class="sxs-lookup"><span data-stu-id="58415-109">**InternetHeaderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="58415-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="58415-110">Attributes and elements</span></span>

<span data-ttu-id="58415-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="58415-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58415-112">属性</span><span class="sxs-lookup"><span data-stu-id="58415-112">Attributes</span></span>

|<span data-ttu-id="58415-113">**属性**</span><span class="sxs-lookup"><span data-stu-id="58415-113">**Attribute**</span></span>|<span data-ttu-id="58415-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="58415-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="58415-115">**HeaderName**</span><span class="sxs-lookup"><span data-stu-id="58415-115">**HeaderName**</span></span> <br/> |<span data-ttu-id="58415-116">标识的标头名称。</span><span class="sxs-lookup"><span data-stu-id="58415-116">Identifies the header name.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="58415-117">子元素</span><span class="sxs-lookup"><span data-stu-id="58415-117">Child elements</span></span>

<span data-ttu-id="58415-118">无。</span><span class="sxs-lookup"><span data-stu-id="58415-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="58415-119">父元素</span><span class="sxs-lookup"><span data-stu-id="58415-119">Parent elements</span></span>

|<span data-ttu-id="58415-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="58415-120">**Element**</span></span>|<span data-ttu-id="58415-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="58415-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58415-122">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="58415-122">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="58415-123">代表在邮箱中某个项目中包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="58415-123">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="58415-124">文本值</span><span class="sxs-lookup"><span data-stu-id="58415-124">Text value</span></span>

<span data-ttu-id="58415-125">文本值表示标头的值。</span><span class="sxs-lookup"><span data-stu-id="58415-125">The text value represents the value for the header.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="58415-126">注解</span><span class="sxs-lookup"><span data-stu-id="58415-126">Remarks</span></span>

<span data-ttu-id="58415-127">下面是 EWS 托管 API 扩展属性**PR_TRANSPORT_MESSAGE_HEADERS**属性的定义。</span><span class="sxs-lookup"><span data-stu-id="58415-127">The following is the EWS Managed API extended property definition for the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

<span data-ttu-id="58415-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="58415-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="58415-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="58415-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58415-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="58415-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="58415-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="58415-131">Schema Name</span></span>  <br/> |<span data-ttu-id="58415-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="58415-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="58415-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="58415-133">Validation File</span></span>  <br/> |<span data-ttu-id="58415-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="58415-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="58415-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="58415-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="58415-136">False</span><span class="sxs-lookup"><span data-stu-id="58415-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58415-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="58415-137">See also</span></span>



- [<span data-ttu-id="58415-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="58415-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="58415-139">EWS、 MIME 和缺少的 Internet 邮件头</span><span class="sxs-lookup"><span data-stu-id="58415-139">EWS, MIME, and the missing Internet message headers</span></span>](http://msdn.microsoft.com/zh-cn/library/exchange/hh545614%28v=exchg.140%29.aspx)

