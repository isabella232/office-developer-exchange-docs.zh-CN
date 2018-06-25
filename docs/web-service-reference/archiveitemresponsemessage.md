---
title: ArchiveItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2ac58d6f-e019-4352-b82f-8ac67a171e63
description: ArchiveItemResponseMessage 元素指定 ArchiveItem 请求的响应消息。
ms.openlocfilehash: a7832e2cb4ec91a0871de5979fd1b418c0626aa6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753260"
---
# <a name="archiveitemresponsemessage"></a><span data-ttu-id="ed871-103">ArchiveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ed871-103">ArchiveItemResponseMessage</span></span>

<span data-ttu-id="ed871-104">**ArchiveItemResponseMessage**元素指定**ArchiveItem**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="ed871-104">The **ArchiveItemResponseMessage** element specifies the response message to an **ArchiveItem** request.</span></span> 
  
```XML
<ArchiveItemResponseMessage ResponseClass="">
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
    <Items></Items>
</ArchiveItemResponseMessage>
```

 <span data-ttu-id="ed871-105">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ed871-105">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ed871-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ed871-106">Attributes and elements</span></span>

<span data-ttu-id="ed871-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ed871-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ed871-108">属性</span><span class="sxs-lookup"><span data-stu-id="ed871-108">Attributes</span></span>

|<span data-ttu-id="ed871-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="ed871-109">**Attribute**</span></span>|<span data-ttu-id="ed871-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="ed871-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ed871-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="ed871-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="ed871-112">指示响应的类。</span><span class="sxs-lookup"><span data-stu-id="ed871-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="ed871-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="ed871-113">ResponseClass</span></span>

|<span data-ttu-id="ed871-114">**值**</span><span class="sxs-lookup"><span data-stu-id="ed871-114">**Value**</span></span>|<span data-ttu-id="ed871-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="ed871-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ed871-116">成功</span><span class="sxs-lookup"><span data-stu-id="ed871-116">Success</span></span>  <br/> |<span data-ttu-id="ed871-117">指示成功。</span><span class="sxs-lookup"><span data-stu-id="ed871-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="ed871-118">警告</span><span class="sxs-lookup"><span data-stu-id="ed871-118">Warning</span></span>  <br/> |<span data-ttu-id="ed871-119">指示警告。</span><span class="sxs-lookup"><span data-stu-id="ed871-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="ed871-120">错误</span><span class="sxs-lookup"><span data-stu-id="ed871-120">Error</span></span>  <br/> |<span data-ttu-id="ed871-121">指示错误。</span><span class="sxs-lookup"><span data-stu-id="ed871-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ed871-122">子元素</span><span class="sxs-lookup"><span data-stu-id="ed871-122">Child elements</span></span>

|<span data-ttu-id="ed871-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="ed871-123">**Element**</span></span>|<span data-ttu-id="ed871-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="ed871-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed871-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ed871-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ed871-126">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="ed871-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="ed871-127">Items</span><span class="sxs-lookup"><span data-stu-id="ed871-127">Items</span></span>](items.md) <br/> |<span data-ttu-id="ed871-128">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="ed871-128">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="ed871-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="ed871-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ed871-130">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="ed871-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ed871-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="ed871-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ed871-132">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="ed871-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="ed871-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ed871-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ed871-134">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="ed871-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ed871-135">父元素</span><span class="sxs-lookup"><span data-stu-id="ed871-135">Parent elements</span></span>

|<span data-ttu-id="ed871-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="ed871-136">**Element**</span></span>|<span data-ttu-id="ed871-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="ed871-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed871-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ed871-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="ed871-139">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="ed871-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed871-140">备注</span><span class="sxs-lookup"><span data-stu-id="ed871-140">Remarks</span></span>

<span data-ttu-id="ed871-141">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ed871-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ed871-142">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ed871-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ed871-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="ed871-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed871-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="ed871-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ed871-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="ed871-145">Schema Name</span></span>  <br/> |<span data-ttu-id="ed871-146">消息架构</span><span class="sxs-lookup"><span data-stu-id="ed871-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="ed871-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="ed871-147">Validation File</span></span>  <br/> |<span data-ttu-id="ed871-148">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ed871-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ed871-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="ed871-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ed871-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ed871-150">See also</span></span>

- [<span data-ttu-id="ed871-151">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ed871-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

