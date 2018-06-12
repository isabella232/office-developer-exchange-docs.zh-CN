---
title: GetAppManifestsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 815908f1-4223-42d8-92dc-f8bdfc6b5df8
description: GetAppManifestsResponseMessage 元素指定 GetAppManifests 请求的响应消息。
ms.openlocfilehash: 05eeef7f7194c1dc05be93ed13ebff93d5013e94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754458"
---
# <a name="getappmanifestsresponsemessage"></a><span data-ttu-id="9992a-103">GetAppManifestsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9992a-103">GetAppManifestsResponseMessage</span></span>

<span data-ttu-id="9992a-104">**GetAppManifestsResponseMessage**元素指定**GetAppManifests**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="9992a-104">The **GetAppManifestsResponseMessage** element specifies the response message for a **GetAppManifests** request.</span></span> 
  
```XML
<GetAppManifestsResponseMessage ResponseClass=" Success | Warning | Error ">
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetAppManifestsResponseMessage>
```

 <span data-ttu-id="9992a-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="9992a-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9992a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9992a-106">Attributes and elements</span></span>

<span data-ttu-id="9992a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9992a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9992a-108">属性</span><span class="sxs-lookup"><span data-stu-id="9992a-108">Attributes</span></span>

|<span data-ttu-id="9992a-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="9992a-109">**Attribute**</span></span>|<span data-ttu-id="9992a-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="9992a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9992a-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="9992a-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="9992a-112">指示响应的类。</span><span class="sxs-lookup"><span data-stu-id="9992a-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="9992a-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="9992a-113">ResponseClass</span></span>

|<span data-ttu-id="9992a-114">**值**</span><span class="sxs-lookup"><span data-stu-id="9992a-114">**Value**</span></span>|<span data-ttu-id="9992a-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="9992a-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9992a-116">成功</span><span class="sxs-lookup"><span data-stu-id="9992a-116">Success</span></span>  <br/> |<span data-ttu-id="9992a-117">指示成功。</span><span class="sxs-lookup"><span data-stu-id="9992a-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="9992a-118">警告</span><span class="sxs-lookup"><span data-stu-id="9992a-118">Warning</span></span>  <br/> |<span data-ttu-id="9992a-119">指示警告。</span><span class="sxs-lookup"><span data-stu-id="9992a-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="9992a-120">Error</span><span class="sxs-lookup"><span data-stu-id="9992a-120">Error</span></span>  <br/> |<span data-ttu-id="9992a-121">指示错误。</span><span class="sxs-lookup"><span data-stu-id="9992a-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9992a-122">子元素</span><span class="sxs-lookup"><span data-stu-id="9992a-122">Child elements</span></span>

|<span data-ttu-id="9992a-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="9992a-123">**Element**</span></span>|<span data-ttu-id="9992a-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="9992a-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9992a-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9992a-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="9992a-126">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="9992a-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="9992a-127">MessageText</span><span class="sxs-lookup"><span data-stu-id="9992a-127">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="9992a-128">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="9992a-128">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="9992a-129">MessageXml</span><span class="sxs-lookup"><span data-stu-id="9992a-129">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="9992a-130">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="9992a-130">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="9992a-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9992a-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="9992a-132">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="9992a-132">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9992a-133">父元素</span><span class="sxs-lookup"><span data-stu-id="9992a-133">Parent elements</span></span>

|<span data-ttu-id="9992a-134">**元素**</span><span class="sxs-lookup"><span data-stu-id="9992a-134">**Element**</span></span>|<span data-ttu-id="9992a-135">**说明**</span><span class="sxs-lookup"><span data-stu-id="9992a-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9992a-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9992a-136">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="9992a-137">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="9992a-137">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9992a-138">备注</span><span class="sxs-lookup"><span data-stu-id="9992a-138">Remarks</span></span>

<span data-ttu-id="9992a-139">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9992a-139">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9992a-140">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9992a-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9992a-141">元素信息</span><span class="sxs-lookup"><span data-stu-id="9992a-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9992a-142">命名空间</span><span class="sxs-lookup"><span data-stu-id="9992a-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9992a-143">架构名称</span><span class="sxs-lookup"><span data-stu-id="9992a-143">Schema Name</span></span>  <br/> |<span data-ttu-id="9992a-144">消息架构</span><span class="sxs-lookup"><span data-stu-id="9992a-144">Message schema</span></span>  <br/> |
|<span data-ttu-id="9992a-145">验证文件</span><span class="sxs-lookup"><span data-stu-id="9992a-145">Validation File</span></span>  <br/> |<span data-ttu-id="9992a-146">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9992a-146">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9992a-147">可以为空</span><span class="sxs-lookup"><span data-stu-id="9992a-147">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="9992a-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9992a-148">See also</span></span>



- [<span data-ttu-id="9992a-149">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9992a-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

