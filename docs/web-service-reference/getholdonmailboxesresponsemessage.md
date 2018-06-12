---
title: GetHoldOnMailboxesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f7d0d90-d418-4ce9-8cea-afe8f14728c3
description: GetHoldOnMailboxesResponseMessage 元素指定 GetHoldOnMailboxes 请求的响应消息。
ms.openlocfilehash: e1c43f75bfa62b20de9248546e71c92ae5998ed9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754576"
---
# <a name="getholdonmailboxesresponsemessage"></a><span data-ttu-id="0b21b-103">GetHoldOnMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0b21b-103">GetHoldOnMailboxesResponseMessage</span></span>

<span data-ttu-id="0b21b-104">**GetHoldOnMailboxesResponseMessage**元素指定**GetHoldOnMailboxes**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="0b21b-104">The **GetHoldOnMailboxesResponseMessage** element specifies the response message for a **GetHoldOnMailboxes** request.</span></span> 
  
```XML
<GetHoldOnMailboxesResponseMessage ResponseClass=" Success | Warning | Error ">
    <MailboxHoldResult/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetHoldOnMailboxesResponseMessage>
```

 <span data-ttu-id="0b21b-105">**GetHoldOnMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="0b21b-105">**GetHoldOnMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0b21b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0b21b-106">Attributes and elements</span></span>

<span data-ttu-id="0b21b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0b21b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0b21b-108">属性</span><span class="sxs-lookup"><span data-stu-id="0b21b-108">Attributes</span></span>

|<span data-ttu-id="0b21b-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="0b21b-109">**Attribute**</span></span>|<span data-ttu-id="0b21b-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="0b21b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0b21b-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="0b21b-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="0b21b-112">指示响应的类。</span><span class="sxs-lookup"><span data-stu-id="0b21b-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="0b21b-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="0b21b-113">ResponseClass</span></span>

|<span data-ttu-id="0b21b-114">**值**</span><span class="sxs-lookup"><span data-stu-id="0b21b-114">**Value**</span></span>|<span data-ttu-id="0b21b-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="0b21b-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0b21b-116">成功</span><span class="sxs-lookup"><span data-stu-id="0b21b-116">Success</span></span>  <br/> |<span data-ttu-id="0b21b-117">指示成功。</span><span class="sxs-lookup"><span data-stu-id="0b21b-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="0b21b-118">警告</span><span class="sxs-lookup"><span data-stu-id="0b21b-118">Warning</span></span>  <br/> |<span data-ttu-id="0b21b-119">指示警告。</span><span class="sxs-lookup"><span data-stu-id="0b21b-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="0b21b-120">Error</span><span class="sxs-lookup"><span data-stu-id="0b21b-120">Error</span></span>  <br/> |<span data-ttu-id="0b21b-121">指示错误。</span><span class="sxs-lookup"><span data-stu-id="0b21b-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0b21b-122">子元素</span><span class="sxs-lookup"><span data-stu-id="0b21b-122">Child elements</span></span>

|<span data-ttu-id="0b21b-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="0b21b-123">**Element**</span></span>|<span data-ttu-id="0b21b-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="0b21b-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0b21b-125">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="0b21b-125">MailboxHoldResult</span></span>](mailboxholdresult.md) <br/> |<span data-ttu-id="0b21b-126">包含**GetHoldOnMailboxes**请求的结果。</span><span class="sxs-lookup"><span data-stu-id="0b21b-126">Contains the result of the **GetHoldOnMailboxes** request.</span></span>  <br/> |
|[<span data-ttu-id="0b21b-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0b21b-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="0b21b-128">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="0b21b-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="0b21b-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="0b21b-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0b21b-130">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="0b21b-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="0b21b-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0b21b-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="0b21b-132">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="0b21b-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="0b21b-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0b21b-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="0b21b-134">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="0b21b-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0b21b-135">父元素</span><span class="sxs-lookup"><span data-stu-id="0b21b-135">Parent elements</span></span>

|<span data-ttu-id="0b21b-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="0b21b-136">**Element**</span></span>|<span data-ttu-id="0b21b-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="0b21b-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0b21b-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0b21b-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="0b21b-139">包含为 Exchange Web Services (EWS) 请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="0b21b-139">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b21b-140">备注</span><span class="sxs-lookup"><span data-stu-id="0b21b-140">Remarks</span></span>

<span data-ttu-id="0b21b-141">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0b21b-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0b21b-142">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0b21b-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0b21b-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="0b21b-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b21b-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="0b21b-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0b21b-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="0b21b-145">Schema Name</span></span>  <br/> |<span data-ttu-id="0b21b-146">消息架构</span><span class="sxs-lookup"><span data-stu-id="0b21b-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="0b21b-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="0b21b-147">Validation File</span></span>  <br/> |<span data-ttu-id="0b21b-148">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0b21b-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0b21b-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="0b21b-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0b21b-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0b21b-150">See also</span></span>



- [<span data-ttu-id="0b21b-151">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0b21b-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

