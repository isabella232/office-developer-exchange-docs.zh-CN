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
description: InternetMessageHeader 元素表示标头集合中的给定标头的 Internet 邮件头。 若要获取 Internet 邮件头的整个集合，请使用 PR_TRANSPORT_MESSAGE_HEADERS 属性。 有关 EWS 和 Internet 邮件头的详细信息，请 seeGetting Internet 邮件头在 EWS、MIME 和缺少的 Internet 邮件头中。
ms.openlocfilehash: 7b662617e0b1a1fcdcce3449b729485ba6e0956b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459305"
---
# <a name="internetmessageheader"></a><span data-ttu-id="5e0b8-105">InternetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="5e0b8-105">InternetMessageHeader</span></span>

<span data-ttu-id="5e0b8-106">**InternetMessageHeader**元素表示标头集合中的给定标头的 Internet 邮件头。</span><span class="sxs-lookup"><span data-stu-id="5e0b8-106">The **InternetMessageHeader** element represents the Internet message header for a given header within the headers collection.</span></span> <span data-ttu-id="5e0b8-107">若要获取 Internet 邮件头的整个集合，请使用**PR_TRANSPORT_MESSAGE_HEADERS**属性。</span><span class="sxs-lookup"><span data-stu-id="5e0b8-107">To get the entire collection of Internet message headers, use the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> <span data-ttu-id="5e0b8-108">有关 EWS 和 Internet 邮件头的详细信息，请参阅 "在 Ews 中获取 Internet 邮件头" [、"MIME" 和 "缺少 internet 邮件头](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)"。</span><span class="sxs-lookup"><span data-stu-id="5e0b8-108">For more information about EWS and Internet message headers, see "Getting Internet message headers in [EWS, MIME, and the missing Internet message headers](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx).</span></span>
  
```XML
<InternetMessageHeader HeaderName=""/>
```

 <span data-ttu-id="5e0b8-109">**InternetHeaderType**</span><span class="sxs-lookup"><span data-stu-id="5e0b8-109">**InternetHeaderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5e0b8-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5e0b8-110">Attributes and elements</span></span>

<span data-ttu-id="5e0b8-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5e0b8-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5e0b8-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="5e0b8-112">Attributes</span></span>

|<span data-ttu-id="5e0b8-113">**属性**</span><span class="sxs-lookup"><span data-stu-id="5e0b8-113">**Attribute**</span></span>|<span data-ttu-id="5e0b8-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="5e0b8-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5e0b8-115">**HeaderName**</span><span class="sxs-lookup"><span data-stu-id="5e0b8-115">**HeaderName**</span></span> <br/> |<span data-ttu-id="5e0b8-116">标识标头名称。</span><span class="sxs-lookup"><span data-stu-id="5e0b8-116">Identifies the header name.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5e0b8-117">子元素</span><span class="sxs-lookup"><span data-stu-id="5e0b8-117">Child elements</span></span>

<span data-ttu-id="5e0b8-118">无。</span><span class="sxs-lookup"><span data-stu-id="5e0b8-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5e0b8-119">父元素</span><span class="sxs-lookup"><span data-stu-id="5e0b8-119">Parent elements</span></span>

|<span data-ttu-id="5e0b8-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="5e0b8-120">**Element**</span></span>|<span data-ttu-id="5e0b8-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="5e0b8-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5e0b8-122">Message</span><span class="sxs-lookup"><span data-stu-id="5e0b8-122">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="5e0b8-123">表示邮箱中的项目所包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="5e0b8-123">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5e0b8-124">文本值</span><span class="sxs-lookup"><span data-stu-id="5e0b8-124">Text value</span></span>

<span data-ttu-id="5e0b8-125">文本值表示标头的值。</span><span class="sxs-lookup"><span data-stu-id="5e0b8-125">The text value represents the value for the header.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5e0b8-126">备注</span><span class="sxs-lookup"><span data-stu-id="5e0b8-126">Remarks</span></span>

<span data-ttu-id="5e0b8-127">下面是**PR_TRANSPORT_MESSAGE_HEADERS**属性的 EWS 托管 API 扩展属性定义。</span><span class="sxs-lookup"><span data-stu-id="5e0b8-127">The following is the EWS Managed API extended property definition for the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

<span data-ttu-id="5e0b8-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5e0b8-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5e0b8-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="5e0b8-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5e0b8-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="5e0b8-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5e0b8-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="5e0b8-131">Schema Name</span></span>  <br/> |<span data-ttu-id="5e0b8-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="5e0b8-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="5e0b8-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="5e0b8-133">Validation File</span></span>  <br/> |<span data-ttu-id="5e0b8-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5e0b8-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5e0b8-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="5e0b8-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="5e0b8-136">False</span><span class="sxs-lookup"><span data-stu-id="5e0b8-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5e0b8-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5e0b8-137">See also</span></span>



- [<span data-ttu-id="5e0b8-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5e0b8-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="5e0b8-139">EWS、MIME 和缺少的 Internet 邮件头</span><span class="sxs-lookup"><span data-stu-id="5e0b8-139">EWS, MIME, and the missing Internet message headers</span></span>](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)

