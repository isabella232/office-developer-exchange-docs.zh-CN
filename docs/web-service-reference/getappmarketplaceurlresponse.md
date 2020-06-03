---
title: GetAppMarketplaceUrlResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc3368ec-78c2-4f8d-8394-4891e90dafd2
description: GetAppMarketplaceUrlResponse 元素指定对 GetAppMarketplaceUrl 请求的响应。
ms.openlocfilehash: 7ff000908a2f73f41575cae8a7795644dd60565d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530851"
---
# <a name="getappmarketplaceurlresponse"></a><span data-ttu-id="85aba-103">GetAppMarketplaceUrlResponse</span><span class="sxs-lookup"><span data-stu-id="85aba-103">GetAppMarketplaceUrlResponse</span></span>

<span data-ttu-id="85aba-104">**GetAppMarketplaceUrlResponse**元素指定对**GetAppMarketplaceUrl**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="85aba-104">The **GetAppMarketplaceUrlResponse** element specifies the response to a **GetAppMarketplaceUrl** request.</span></span> 
  
```XML
<GetAppMarketplaceUrlResponse ResponseClass=" Success | Warning | Error ">
    <AppMarketplaceUrl/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetAppMarketplaceUrlResponse>
```

 <span data-ttu-id="85aba-105">**GetAppMarketplaceUrlResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="85aba-105">**GetAppMarketplaceUrlResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85aba-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="85aba-106">Attributes and elements</span></span>

<span data-ttu-id="85aba-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="85aba-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85aba-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="85aba-108">Attributes</span></span>

|<span data-ttu-id="85aba-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="85aba-109">**Attribute**</span></span>|<span data-ttu-id="85aba-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="85aba-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85aba-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="85aba-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="85aba-112">指示响应的类。</span><span class="sxs-lookup"><span data-stu-id="85aba-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="85aba-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="85aba-113">ResponseClass</span></span>

|<span data-ttu-id="85aba-114">**值**</span><span class="sxs-lookup"><span data-stu-id="85aba-114">**Value**</span></span>|<span data-ttu-id="85aba-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="85aba-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85aba-116">成功</span><span class="sxs-lookup"><span data-stu-id="85aba-116">Success</span></span>  <br/> |<span data-ttu-id="85aba-117">指示成功。</span><span class="sxs-lookup"><span data-stu-id="85aba-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="85aba-118">警告</span><span class="sxs-lookup"><span data-stu-id="85aba-118">Warning</span></span>  <br/> |<span data-ttu-id="85aba-119">指示警告。</span><span class="sxs-lookup"><span data-stu-id="85aba-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="85aba-120">错误</span><span class="sxs-lookup"><span data-stu-id="85aba-120">Error</span></span>  <br/> |<span data-ttu-id="85aba-121">指示错误。</span><span class="sxs-lookup"><span data-stu-id="85aba-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="85aba-122">子元素</span><span class="sxs-lookup"><span data-stu-id="85aba-122">Child elements</span></span>

|<span data-ttu-id="85aba-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="85aba-123">**Element**</span></span>|<span data-ttu-id="85aba-124">**描述**</span><span class="sxs-lookup"><span data-stu-id="85aba-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85aba-125">AppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="85aba-125">AppMarketplaceUrl</span></span>](appmarketplaceurl.md) <br/> |<span data-ttu-id="85aba-126">指定应用程序的 URL。</span><span class="sxs-lookup"><span data-stu-id="85aba-126">Specifies the URL for the app.</span></span>  <br/> |
|[<span data-ttu-id="85aba-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="85aba-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="85aba-128">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="85aba-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="85aba-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="85aba-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="85aba-130">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="85aba-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="85aba-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="85aba-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="85aba-132">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="85aba-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="85aba-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="85aba-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="85aba-134">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="85aba-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="85aba-135">父元素</span><span class="sxs-lookup"><span data-stu-id="85aba-135">Parent elements</span></span>

|<span data-ttu-id="85aba-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="85aba-136">**Element**</span></span>|<span data-ttu-id="85aba-137">**描述**</span><span class="sxs-lookup"><span data-stu-id="85aba-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85aba-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="85aba-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="85aba-139">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="85aba-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85aba-140">备注</span><span class="sxs-lookup"><span data-stu-id="85aba-140">Remarks</span></span>

<span data-ttu-id="85aba-141">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="85aba-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="85aba-142">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="85aba-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85aba-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="85aba-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85aba-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="85aba-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="85aba-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="85aba-145">Schema Name</span></span>  <br/> |<span data-ttu-id="85aba-146">消息架构</span><span class="sxs-lookup"><span data-stu-id="85aba-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="85aba-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="85aba-147">Validation File</span></span>  <br/> |<span data-ttu-id="85aba-148">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="85aba-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="85aba-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="85aba-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="85aba-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="85aba-150">See also</span></span>



- [<span data-ttu-id="85aba-151">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="85aba-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

