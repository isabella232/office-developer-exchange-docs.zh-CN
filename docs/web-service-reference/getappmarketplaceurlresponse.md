---
title: GetAppMarketplaceUrlResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc3368ec-78c2-4f8d-8394-4891e90dafd2
description: GetAppMarketplaceUrlResponse 元素指定 GetAppMarketplaceUrl 请求的响应。
ms.openlocfilehash: 553ebfc4615280c77d4a1ef9e5db3e5d10a0f2a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754460"
---
# <a name="getappmarketplaceurlresponse"></a><span data-ttu-id="3955d-103">GetAppMarketplaceUrlResponse</span><span class="sxs-lookup"><span data-stu-id="3955d-103">GetAppMarketplaceUrlResponse</span></span>

<span data-ttu-id="3955d-104">**GetAppMarketplaceUrlResponse**元素指定**GetAppMarketplaceUrl**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="3955d-104">The **GetAppMarketplaceUrlResponse** element specifies the response to a **GetAppMarketplaceUrl** request.</span></span> 
  
```XML
<GetAppMarketplaceUrlResponse ResponseClass=" Success | Warning | Error ">
    <AppMarketplaceUrl/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetAppMarketplaceUrlResponse>
```

 <span data-ttu-id="3955d-105">**GetAppMarketplaceUrlResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="3955d-105">**GetAppMarketplaceUrlResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3955d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3955d-106">Attributes and elements</span></span>

<span data-ttu-id="3955d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3955d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3955d-108">属性</span><span class="sxs-lookup"><span data-stu-id="3955d-108">Attributes</span></span>

|<span data-ttu-id="3955d-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="3955d-109">**Attribute**</span></span>|<span data-ttu-id="3955d-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="3955d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3955d-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="3955d-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="3955d-112">指示响应的类。</span><span class="sxs-lookup"><span data-stu-id="3955d-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="3955d-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="3955d-113">ResponseClass</span></span>

|<span data-ttu-id="3955d-114">**值**</span><span class="sxs-lookup"><span data-stu-id="3955d-114">**Value**</span></span>|<span data-ttu-id="3955d-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="3955d-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3955d-116">成功</span><span class="sxs-lookup"><span data-stu-id="3955d-116">Success</span></span>  <br/> |<span data-ttu-id="3955d-117">指示成功。</span><span class="sxs-lookup"><span data-stu-id="3955d-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="3955d-118">警告</span><span class="sxs-lookup"><span data-stu-id="3955d-118">Warning</span></span>  <br/> |<span data-ttu-id="3955d-119">指示警告。</span><span class="sxs-lookup"><span data-stu-id="3955d-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="3955d-120">错误</span><span class="sxs-lookup"><span data-stu-id="3955d-120">Error</span></span>  <br/> |<span data-ttu-id="3955d-121">指示错误。</span><span class="sxs-lookup"><span data-stu-id="3955d-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3955d-122">子元素</span><span class="sxs-lookup"><span data-stu-id="3955d-122">Child elements</span></span>

|<span data-ttu-id="3955d-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="3955d-123">**Element**</span></span>|<span data-ttu-id="3955d-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="3955d-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3955d-125">AppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="3955d-125">AppMarketplaceUrl</span></span>](appmarketplaceurl.md) <br/> |<span data-ttu-id="3955d-126">指定应用程序的 URL。</span><span class="sxs-lookup"><span data-stu-id="3955d-126">Specifies the URL for the app.</span></span>  <br/> |
|[<span data-ttu-id="3955d-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="3955d-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="3955d-128">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="3955d-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="3955d-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="3955d-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="3955d-130">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="3955d-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="3955d-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="3955d-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="3955d-132">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="3955d-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="3955d-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3955d-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="3955d-134">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="3955d-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3955d-135">父元素</span><span class="sxs-lookup"><span data-stu-id="3955d-135">Parent elements</span></span>

|<span data-ttu-id="3955d-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="3955d-136">**Element**</span></span>|<span data-ttu-id="3955d-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="3955d-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3955d-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3955d-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="3955d-139">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="3955d-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3955d-140">备注</span><span class="sxs-lookup"><span data-stu-id="3955d-140">Remarks</span></span>

<span data-ttu-id="3955d-141">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3955d-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3955d-142">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3955d-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3955d-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="3955d-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3955d-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="3955d-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3955d-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="3955d-145">Schema Name</span></span>  <br/> |<span data-ttu-id="3955d-146">消息架构</span><span class="sxs-lookup"><span data-stu-id="3955d-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="3955d-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="3955d-147">Validation File</span></span>  <br/> |<span data-ttu-id="3955d-148">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3955d-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3955d-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="3955d-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3955d-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3955d-150">See also</span></span>



- [<span data-ttu-id="3955d-151">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3955d-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

