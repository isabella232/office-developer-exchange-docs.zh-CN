---
title: GetSearchableMailboxesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f45865fd-4626-4d80-84f6-7989339fdd85
description: GetSearchableMailboxesResponseMessage 元素指定 GetSearchableMailboxes 请求的响应消息。
ms.openlocfilehash: 2a4d1fe357656fe29d8572e7f32a4bc2e4a6131e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754684"
---
# <a name="getsearchablemailboxesresponsemessage"></a><span data-ttu-id="b7621-103">GetSearchableMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b7621-103">GetSearchableMailboxesResponseMessage</span></span>

<span data-ttu-id="b7621-104">**GetSearchableMailboxesResponseMessage**元素指定**GetSearchableMailboxes**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="b7621-104">The **GetSearchableMailboxesResponseMessage** element specifies the response message for a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<GetSearchableMailboxesResponseMessage ResponseClass=" Success | Warning | Error ">
    <SearchableMailboxes/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetSearchablemailboxesResponseMessage>
```

 <span data-ttu-id="b7621-105">**GetSearchableMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="b7621-105">**GetSearchableMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b7621-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b7621-106">Attributes and elements</span></span>

<span data-ttu-id="b7621-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b7621-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7621-108">属性</span><span class="sxs-lookup"><span data-stu-id="b7621-108">Attributes</span></span>

|<span data-ttu-id="b7621-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="b7621-109">**Attribute**</span></span>|<span data-ttu-id="b7621-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="b7621-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b7621-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="b7621-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="b7621-112">指示响应的类。</span><span class="sxs-lookup"><span data-stu-id="b7621-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="b7621-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="b7621-113">ResponseClass</span></span>

|<span data-ttu-id="b7621-114">**值**</span><span class="sxs-lookup"><span data-stu-id="b7621-114">**Value**</span></span>|<span data-ttu-id="b7621-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="b7621-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b7621-116">成功</span><span class="sxs-lookup"><span data-stu-id="b7621-116">Success</span></span>  <br/> |<span data-ttu-id="b7621-117">指示成功。</span><span class="sxs-lookup"><span data-stu-id="b7621-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="b7621-118">警告</span><span class="sxs-lookup"><span data-stu-id="b7621-118">Warning</span></span>  <br/> |<span data-ttu-id="b7621-119">指示警告。</span><span class="sxs-lookup"><span data-stu-id="b7621-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="b7621-120">错误</span><span class="sxs-lookup"><span data-stu-id="b7621-120">Error</span></span>  <br/> |<span data-ttu-id="b7621-121">指示错误。</span><span class="sxs-lookup"><span data-stu-id="b7621-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b7621-122">子元素</span><span class="sxs-lookup"><span data-stu-id="b7621-122">Child elements</span></span>

|<span data-ttu-id="b7621-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="b7621-123">**Element**</span></span>|<span data-ttu-id="b7621-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="b7621-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7621-125">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="b7621-125">SearchableMailboxes</span></span>](searchablemailboxes.md) <br/> |<span data-ttu-id="b7621-126">包含邮箱从**GetSearchableMailboxes**请求返回的数组。</span><span class="sxs-lookup"><span data-stu-id="b7621-126">Contains an array of the mailboxes returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
|[<span data-ttu-id="b7621-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b7621-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="b7621-128">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="b7621-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="b7621-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="b7621-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="b7621-130">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="b7621-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="b7621-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="b7621-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="b7621-132">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="b7621-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="b7621-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b7621-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="b7621-134">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="b7621-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b7621-135">父元素</span><span class="sxs-lookup"><span data-stu-id="b7621-135">Parent elements</span></span>

|<span data-ttu-id="b7621-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="b7621-136">**Element**</span></span>|<span data-ttu-id="b7621-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="b7621-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7621-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b7621-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="b7621-139">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="b7621-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7621-140">备注</span><span class="sxs-lookup"><span data-stu-id="b7621-140">Remarks</span></span>

<span data-ttu-id="b7621-141">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b7621-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b7621-142">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b7621-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7621-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="b7621-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7621-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="b7621-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b7621-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="b7621-145">Schema Name</span></span>  <br/> |<span data-ttu-id="b7621-146">消息架构</span><span class="sxs-lookup"><span data-stu-id="b7621-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="b7621-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="b7621-147">Validation File</span></span>  <br/> |<span data-ttu-id="b7621-148">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b7621-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b7621-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="b7621-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="b7621-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b7621-150">See also</span></span>



- [<span data-ttu-id="b7621-151">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b7621-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

