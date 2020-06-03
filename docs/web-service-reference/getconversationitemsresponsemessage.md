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
ms.openlocfilehash: b38bca60bb51c24a7635391c4e23e5426366cd72
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461070"
---
# <a name="getconversationitemsresponsemessage"></a><span data-ttu-id="4885e-103">GetConversationItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4885e-103">GetConversationItemsResponseMessage</span></span>

<span data-ttu-id="4885e-104">**GetConversationItemsResponseMessage**元素指定**GetConversationItems**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="4885e-104">The **GetConversationItemsResponseMessage** element specifies the response message for a **GetConversationItems** request.</span></span> 
  
```XML
<GetConversationItemsResponseMessage ResponseClass="Success | Warning | Error">
    <Conversation/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetConversationItemsResponseMessage>
```

 <span data-ttu-id="4885e-105">**GetConversationItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="4885e-105">**GetConversationItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4885e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4885e-106">Attributes and elements</span></span>

<span data-ttu-id="4885e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4885e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4885e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4885e-108">Attributes</span></span>

|<span data-ttu-id="4885e-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="4885e-109">**Attribute**</span></span>|<span data-ttu-id="4885e-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="4885e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4885e-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="4885e-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="4885e-112">指示响应的类。</span><span class="sxs-lookup"><span data-stu-id="4885e-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="4885e-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="4885e-113">ResponseClass</span></span>

|<span data-ttu-id="4885e-114">**值**</span><span class="sxs-lookup"><span data-stu-id="4885e-114">**Value**</span></span>|<span data-ttu-id="4885e-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="4885e-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4885e-116">成功</span><span class="sxs-lookup"><span data-stu-id="4885e-116">Success</span></span>  <br/> |<span data-ttu-id="4885e-117">指示成功。</span><span class="sxs-lookup"><span data-stu-id="4885e-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="4885e-118">警告</span><span class="sxs-lookup"><span data-stu-id="4885e-118">Warning</span></span>  <br/> |<span data-ttu-id="4885e-119">指示警告。</span><span class="sxs-lookup"><span data-stu-id="4885e-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="4885e-120">错误</span><span class="sxs-lookup"><span data-stu-id="4885e-120">Error</span></span>  <br/> |<span data-ttu-id="4885e-121">指示错误。</span><span class="sxs-lookup"><span data-stu-id="4885e-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4885e-122">子元素</span><span class="sxs-lookup"><span data-stu-id="4885e-122">Child elements</span></span>

|<span data-ttu-id="4885e-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="4885e-123">**Element**</span></span>|<span data-ttu-id="4885e-124">**描述**</span><span class="sxs-lookup"><span data-stu-id="4885e-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4885e-125">对话（ConversationResponseType）</span><span class="sxs-lookup"><span data-stu-id="4885e-125">Conversation (ConversationResponseType)</span></span>](conversation-conversationresponsetype.md) <br/> |<span data-ttu-id="4885e-126">代表**GetConversationItems**响应中返回的单个对话。</span><span class="sxs-lookup"><span data-stu-id="4885e-126">Represents a single conversation returned in a **GetConversationItems** response.</span></span>  <br/> |
|[<span data-ttu-id="4885e-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="4885e-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="4885e-128">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="4885e-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="4885e-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="4885e-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="4885e-130">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="4885e-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="4885e-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="4885e-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="4885e-132">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="4885e-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="4885e-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4885e-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="4885e-134">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="4885e-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4885e-135">父元素</span><span class="sxs-lookup"><span data-stu-id="4885e-135">Parent elements</span></span>

|<span data-ttu-id="4885e-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="4885e-136">**Element**</span></span>|<span data-ttu-id="4885e-137">**描述**</span><span class="sxs-lookup"><span data-stu-id="4885e-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4885e-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4885e-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="4885e-139">包含 Exchange Web 服务（EWS）请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="4885e-139">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4885e-140">备注</span><span class="sxs-lookup"><span data-stu-id="4885e-140">Remarks</span></span>

<span data-ttu-id="4885e-141">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4885e-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4885e-142">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4885e-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4885e-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="4885e-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4885e-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="4885e-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4885e-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="4885e-145">Schema Name</span></span>  <br/> |<span data-ttu-id="4885e-146">消息架构</span><span class="sxs-lookup"><span data-stu-id="4885e-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="4885e-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="4885e-147">Validation File</span></span>  <br/> |<span data-ttu-id="4885e-148">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="4885e-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4885e-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="4885e-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="4885e-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4885e-150">See also</span></span>



- [<span data-ttu-id="4885e-151">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4885e-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

