---
title: GetConversationItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e930650-7848-4bf2-a975-026309b3ea02
description: GetConversationItemsResponseMessage 元素指定 GetConversationItems 请求的响应消息。
ms.openlocfilehash: 997319193311ef9267d8f6ff14c70bfe40e2634b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754501"
---
# <a name="getconversationitemsresponsemessage"></a><span data-ttu-id="c4261-103">GetConversationItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c4261-103">GetConversationItemsResponseMessage</span></span>

<span data-ttu-id="c4261-104">**GetConversationItemsResponseMessage**元素指定**GetConversationItems**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="c4261-104">The **GetConversationItemsResponseMessage** element specifies the response message for a **GetConversationItems** request.</span></span> 
  
```XML
<GetConversationItemsResponseMessage ResponseClass="Success | Warning | Error">
    <Conversation/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetConversationItemsResponseMessage>
```

 <span data-ttu-id="c4261-105">**GetConversationItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="c4261-105">**GetConversationItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c4261-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c4261-106">Attributes and elements</span></span>

<span data-ttu-id="c4261-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c4261-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4261-108">属性</span><span class="sxs-lookup"><span data-stu-id="c4261-108">Attributes</span></span>

|<span data-ttu-id="c4261-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="c4261-109">**Attribute**</span></span>|<span data-ttu-id="c4261-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="c4261-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c4261-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="c4261-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="c4261-112">指示响应的类。</span><span class="sxs-lookup"><span data-stu-id="c4261-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="c4261-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="c4261-113">ResponseClass</span></span>

|<span data-ttu-id="c4261-114">**值**</span><span class="sxs-lookup"><span data-stu-id="c4261-114">**Value**</span></span>|<span data-ttu-id="c4261-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="c4261-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c4261-116">成功</span><span class="sxs-lookup"><span data-stu-id="c4261-116">Success</span></span>  <br/> |<span data-ttu-id="c4261-117">指示成功。</span><span class="sxs-lookup"><span data-stu-id="c4261-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="c4261-118">警告</span><span class="sxs-lookup"><span data-stu-id="c4261-118">Warning</span></span>  <br/> |<span data-ttu-id="c4261-119">指示警告。</span><span class="sxs-lookup"><span data-stu-id="c4261-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="c4261-120">Error</span><span class="sxs-lookup"><span data-stu-id="c4261-120">Error</span></span>  <br/> |<span data-ttu-id="c4261-121">指示错误。</span><span class="sxs-lookup"><span data-stu-id="c4261-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c4261-122">子元素</span><span class="sxs-lookup"><span data-stu-id="c4261-122">Child elements</span></span>

|<span data-ttu-id="c4261-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="c4261-123">**Element**</span></span>|<span data-ttu-id="c4261-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="c4261-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4261-125">对话 (ConversationResponseType)</span><span class="sxs-lookup"><span data-stu-id="c4261-125">Conversation (ConversationResponseType)</span></span>](conversation-conversationresponsetype.md) <br/> |<span data-ttu-id="c4261-126">表示**GetConversationItems**响应中返回单个对话。</span><span class="sxs-lookup"><span data-stu-id="c4261-126">Represents a single conversation returned in a **GetConversationItems** response.</span></span>  <br/> |
|[<span data-ttu-id="c4261-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c4261-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="c4261-128">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="c4261-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="c4261-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="c4261-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="c4261-130">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="c4261-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="c4261-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="c4261-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="c4261-132">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="c4261-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="c4261-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c4261-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="c4261-134">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="c4261-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c4261-135">父元素</span><span class="sxs-lookup"><span data-stu-id="c4261-135">Parent elements</span></span>

|<span data-ttu-id="c4261-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="c4261-136">**Element**</span></span>|<span data-ttu-id="c4261-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="c4261-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4261-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c4261-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="c4261-139">包含为 Exchange Web Services (EWS) 请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="c4261-139">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4261-140">备注</span><span class="sxs-lookup"><span data-stu-id="c4261-140">Remarks</span></span>

<span data-ttu-id="c4261-141">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c4261-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c4261-142">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c4261-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c4261-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="c4261-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4261-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="c4261-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c4261-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="c4261-145">Schema Name</span></span>  <br/> |<span data-ttu-id="c4261-146">消息架构</span><span class="sxs-lookup"><span data-stu-id="c4261-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="c4261-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="c4261-147">Validation File</span></span>  <br/> |<span data-ttu-id="c4261-148">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c4261-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c4261-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="c4261-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c4261-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c4261-150">See also</span></span>



- [<span data-ttu-id="c4261-151">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c4261-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

