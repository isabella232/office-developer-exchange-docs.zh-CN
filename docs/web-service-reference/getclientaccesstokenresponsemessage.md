---
title: GetClientAccessTokenResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45ca2500-ceab-4c98-9576-cb9e158e5896
description: GetClientAccessTokenResponseMessage 元素指定 GetClientAccessToken 请求的响应消息。
ms.openlocfilehash: 16fe684dd48f77156ed88d02a6ae7b8f3312cd87
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754482"
---
# <a name="getclientaccesstokenresponsemessage"></a><span data-ttu-id="21898-103">GetClientAccessTokenResponseMessage</span><span class="sxs-lookup"><span data-stu-id="21898-103">GetClientAccessTokenResponseMessage</span></span>

<span data-ttu-id="21898-104">**GetClientAccessTokenResponseMessage**元素指定**GetClientAccessToken**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="21898-104">The **GetClientAccessTokenResponseMessage** element specifies the response message for a **GetClientAccessToken** request.</span></span> 
  
```XML
<GetClientAccessTokenResponseMessage ResponseClass=" Success | Warning | Error ">
    <Token/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetClientAccessTokenResponseMessage>
```

 <span data-ttu-id="21898-105">**GetClientAccessTokenResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="21898-105">**GetClientAccessTokenResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="21898-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="21898-106">Attributes and elements</span></span>

<span data-ttu-id="21898-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="21898-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21898-108">属性</span><span class="sxs-lookup"><span data-stu-id="21898-108">Attributes</span></span>

|<span data-ttu-id="21898-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="21898-109">**Attribute**</span></span>|<span data-ttu-id="21898-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="21898-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="21898-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="21898-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="21898-112">指示响应的类。</span><span class="sxs-lookup"><span data-stu-id="21898-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="21898-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="21898-113">ResponseClass</span></span>

|<span data-ttu-id="21898-114">**值**</span><span class="sxs-lookup"><span data-stu-id="21898-114">**Value**</span></span>|<span data-ttu-id="21898-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="21898-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="21898-116">成功</span><span class="sxs-lookup"><span data-stu-id="21898-116">Success</span></span>  <br/> |<span data-ttu-id="21898-117">指示成功。</span><span class="sxs-lookup"><span data-stu-id="21898-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="21898-118">警告</span><span class="sxs-lookup"><span data-stu-id="21898-118">Warning</span></span>  <br/> |<span data-ttu-id="21898-119">指示警告。</span><span class="sxs-lookup"><span data-stu-id="21898-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="21898-120">错误</span><span class="sxs-lookup"><span data-stu-id="21898-120">Error</span></span>  <br/> |<span data-ttu-id="21898-121">指示错误。</span><span class="sxs-lookup"><span data-stu-id="21898-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="21898-122">子元素</span><span class="sxs-lookup"><span data-stu-id="21898-122">Child elements</span></span>

|<span data-ttu-id="21898-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="21898-123">**Element**</span></span>|<span data-ttu-id="21898-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="21898-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21898-125">令牌 (ClientAccessTokenType)</span><span class="sxs-lookup"><span data-stu-id="21898-125">Token (ClientAccessTokenType)</span></span>](token-clientaccesstokentype.md) <br/> |<span data-ttu-id="21898-126">指定客户端访问令牌。</span><span class="sxs-lookup"><span data-stu-id="21898-126">Specifies a client access token.</span></span>  <br/> |
|[<span data-ttu-id="21898-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="21898-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="21898-128">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="21898-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="21898-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="21898-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="21898-130">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="21898-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="21898-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="21898-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="21898-132">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="21898-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="21898-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="21898-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="21898-134">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="21898-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="21898-135">父元素</span><span class="sxs-lookup"><span data-stu-id="21898-135">Parent elements</span></span>

|<span data-ttu-id="21898-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="21898-136">**Element**</span></span>|<span data-ttu-id="21898-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="21898-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21898-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="21898-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="21898-139">包含为 Exchange Web Services (EWS) 请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="21898-139">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21898-140">备注</span><span class="sxs-lookup"><span data-stu-id="21898-140">Remarks</span></span>

<span data-ttu-id="21898-141">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="21898-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="21898-142">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="21898-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21898-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="21898-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21898-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="21898-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="21898-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="21898-145">Schema Name</span></span>  <br/> |<span data-ttu-id="21898-146">消息架构</span><span class="sxs-lookup"><span data-stu-id="21898-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="21898-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="21898-147">Validation File</span></span>  <br/> |<span data-ttu-id="21898-148">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="21898-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="21898-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="21898-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="21898-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="21898-150">See also</span></span>



- [<span data-ttu-id="21898-151">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="21898-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

