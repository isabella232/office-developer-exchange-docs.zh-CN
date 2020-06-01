---
title: ArchiveItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2ac58d6f-e019-4352-b82f-8ac67a171e63
description: ArchiveItemResponseMessage 元素指定对 ArchiveItem 请求的响应消息。
ms.openlocfilehash: 24d09d63cab6805194e35031d8590290573de0a9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463389"
---
# <a name="archiveitemresponsemessage"></a><span data-ttu-id="e8404-103">ArchiveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e8404-103">ArchiveItemResponseMessage</span></span>

<span data-ttu-id="e8404-104">**ArchiveItemResponseMessage**元素指定对**ArchiveItem**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="e8404-104">The **ArchiveItemResponseMessage** element specifies the response message to an **ArchiveItem** request.</span></span> 
  
```XML
<ArchiveItemResponseMessage ResponseClass="">
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
    <Items></Items>
</ArchiveItemResponseMessage>
```

 <span data-ttu-id="e8404-105">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e8404-105">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e8404-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e8404-106">Attributes and elements</span></span>

<span data-ttu-id="e8404-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e8404-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8404-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e8404-108">Attributes</span></span>

|<span data-ttu-id="e8404-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="e8404-109">**Attribute**</span></span>|<span data-ttu-id="e8404-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="e8404-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8404-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="e8404-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="e8404-112">指示响应的类。</span><span class="sxs-lookup"><span data-stu-id="e8404-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="e8404-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="e8404-113">ResponseClass</span></span>

|<span data-ttu-id="e8404-114">**值**</span><span class="sxs-lookup"><span data-stu-id="e8404-114">**Value**</span></span>|<span data-ttu-id="e8404-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="e8404-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8404-116">成功</span><span class="sxs-lookup"><span data-stu-id="e8404-116">Success</span></span>  <br/> |<span data-ttu-id="e8404-117">指示成功。</span><span class="sxs-lookup"><span data-stu-id="e8404-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="e8404-118">警告</span><span class="sxs-lookup"><span data-stu-id="e8404-118">Warning</span></span>  <br/> |<span data-ttu-id="e8404-119">指示警告。</span><span class="sxs-lookup"><span data-stu-id="e8404-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="e8404-120">错误</span><span class="sxs-lookup"><span data-stu-id="e8404-120">Error</span></span>  <br/> |<span data-ttu-id="e8404-121">指示错误。</span><span class="sxs-lookup"><span data-stu-id="e8404-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e8404-122">子元素</span><span class="sxs-lookup"><span data-stu-id="e8404-122">Child elements</span></span>

|<span data-ttu-id="e8404-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="e8404-123">**Element**</span></span>|<span data-ttu-id="e8404-124">**描述**</span><span class="sxs-lookup"><span data-stu-id="e8404-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8404-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e8404-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="e8404-126">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="e8404-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="e8404-127">Items</span><span class="sxs-lookup"><span data-stu-id="e8404-127">Items</span></span>](items.md) <br/> |<span data-ttu-id="e8404-128">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="e8404-128">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="e8404-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="e8404-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="e8404-130">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="e8404-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="e8404-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="e8404-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="e8404-132">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="e8404-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="e8404-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e8404-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="e8404-134">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="e8404-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e8404-135">父元素</span><span class="sxs-lookup"><span data-stu-id="e8404-135">Parent elements</span></span>

|<span data-ttu-id="e8404-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="e8404-136">**Element**</span></span>|<span data-ttu-id="e8404-137">**描述**</span><span class="sxs-lookup"><span data-stu-id="e8404-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8404-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e8404-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="e8404-139">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="e8404-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8404-140">备注</span><span class="sxs-lookup"><span data-stu-id="e8404-140">Remarks</span></span>

<span data-ttu-id="e8404-141">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e8404-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e8404-142">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e8404-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e8404-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="e8404-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8404-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="e8404-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e8404-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="e8404-145">Schema Name</span></span>  <br/> |<span data-ttu-id="e8404-146">消息架构</span><span class="sxs-lookup"><span data-stu-id="e8404-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="e8404-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="e8404-147">Validation File</span></span>  <br/> |<span data-ttu-id="e8404-148">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="e8404-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e8404-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="e8404-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e8404-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e8404-150">See also</span></span>

- [<span data-ttu-id="e8404-151">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e8404-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

