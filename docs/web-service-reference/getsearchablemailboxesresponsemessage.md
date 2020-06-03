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
ms.openlocfilehash: 69f45d87cfbd398013d021cdd39b55497d78ae04
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458255"
---
# <a name="getsearchablemailboxesresponsemessage"></a><span data-ttu-id="3be16-103">GetSearchableMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3be16-103">GetSearchableMailboxesResponseMessage</span></span>

<span data-ttu-id="3be16-104">**GetSearchableMailboxesResponseMessage**元素指定**GetSearchableMailboxes**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="3be16-104">The **GetSearchableMailboxesResponseMessage** element specifies the response message for a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<GetSearchableMailboxesResponseMessage ResponseClass=" Success | Warning | Error ">
    <SearchableMailboxes/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetSearchablemailboxesResponseMessage>
```

 <span data-ttu-id="3be16-105">**GetSearchableMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="3be16-105">**GetSearchableMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3be16-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3be16-106">Attributes and elements</span></span>

<span data-ttu-id="3be16-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3be16-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3be16-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="3be16-108">Attributes</span></span>

|<span data-ttu-id="3be16-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="3be16-109">**Attribute**</span></span>|<span data-ttu-id="3be16-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="3be16-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3be16-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="3be16-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="3be16-112">指示响应的类。</span><span class="sxs-lookup"><span data-stu-id="3be16-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="3be16-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="3be16-113">ResponseClass</span></span>

|<span data-ttu-id="3be16-114">**值**</span><span class="sxs-lookup"><span data-stu-id="3be16-114">**Value**</span></span>|<span data-ttu-id="3be16-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="3be16-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3be16-116">成功</span><span class="sxs-lookup"><span data-stu-id="3be16-116">Success</span></span>  <br/> |<span data-ttu-id="3be16-117">指示成功。</span><span class="sxs-lookup"><span data-stu-id="3be16-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="3be16-118">警告</span><span class="sxs-lookup"><span data-stu-id="3be16-118">Warning</span></span>  <br/> |<span data-ttu-id="3be16-119">指示警告。</span><span class="sxs-lookup"><span data-stu-id="3be16-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="3be16-120">错误</span><span class="sxs-lookup"><span data-stu-id="3be16-120">Error</span></span>  <br/> |<span data-ttu-id="3be16-121">指示错误。</span><span class="sxs-lookup"><span data-stu-id="3be16-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3be16-122">子元素</span><span class="sxs-lookup"><span data-stu-id="3be16-122">Child elements</span></span>

|<span data-ttu-id="3be16-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="3be16-123">**Element**</span></span>|<span data-ttu-id="3be16-124">**描述**</span><span class="sxs-lookup"><span data-stu-id="3be16-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3be16-125">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="3be16-125">SearchableMailboxes</span></span>](searchablemailboxes.md) <br/> |<span data-ttu-id="3be16-126">包含从**GetSearchableMailboxes**请求返回的邮箱的数组。</span><span class="sxs-lookup"><span data-stu-id="3be16-126">Contains an array of the mailboxes returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
|[<span data-ttu-id="3be16-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="3be16-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="3be16-128">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="3be16-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="3be16-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="3be16-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="3be16-130">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="3be16-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="3be16-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="3be16-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="3be16-132">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="3be16-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="3be16-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3be16-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="3be16-134">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="3be16-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3be16-135">父元素</span><span class="sxs-lookup"><span data-stu-id="3be16-135">Parent elements</span></span>

|<span data-ttu-id="3be16-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="3be16-136">**Element**</span></span>|<span data-ttu-id="3be16-137">**描述**</span><span class="sxs-lookup"><span data-stu-id="3be16-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3be16-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3be16-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="3be16-139">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="3be16-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3be16-140">备注</span><span class="sxs-lookup"><span data-stu-id="3be16-140">Remarks</span></span>

<span data-ttu-id="3be16-141">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3be16-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3be16-142">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3be16-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3be16-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="3be16-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3be16-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="3be16-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3be16-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="3be16-145">Schema Name</span></span>  <br/> |<span data-ttu-id="3be16-146">消息架构</span><span class="sxs-lookup"><span data-stu-id="3be16-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="3be16-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="3be16-147">Validation File</span></span>  <br/> |<span data-ttu-id="3be16-148">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="3be16-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3be16-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="3be16-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3be16-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3be16-150">See also</span></span>



- [<span data-ttu-id="3be16-151">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3be16-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

