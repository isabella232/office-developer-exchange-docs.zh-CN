---
title: GetAppManifestsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 815908f1-4223-42d8-92dc-f8bdfc6b5df8
description: GetAppManifestsResponseMessage 元素指定 Getappmanifests 已请求的响应消息。
ms.openlocfilehash: 26a521d8647a010fe956596eaf63d4df4756edb2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459530"
---
# <a name="getappmanifestsresponsemessage"></a><span data-ttu-id="807e1-103">GetAppManifestsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="807e1-103">GetAppManifestsResponseMessage</span></span>

<span data-ttu-id="807e1-104">**GetAppManifestsResponseMessage**元素指定**getappmanifests 已**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="807e1-104">The **GetAppManifestsResponseMessage** element specifies the response message for a **GetAppManifests** request.</span></span> 
  
```XML
<GetAppManifestsResponseMessage ResponseClass=" Success | Warning | Error ">
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetAppManifestsResponseMessage>
```

 <span data-ttu-id="807e1-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="807e1-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="807e1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="807e1-106">Attributes and elements</span></span>

<span data-ttu-id="807e1-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="807e1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="807e1-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="807e1-108">Attributes</span></span>

|<span data-ttu-id="807e1-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="807e1-109">**Attribute**</span></span>|<span data-ttu-id="807e1-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="807e1-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="807e1-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="807e1-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="807e1-112">指示响应的类。</span><span class="sxs-lookup"><span data-stu-id="807e1-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="807e1-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="807e1-113">ResponseClass</span></span>

|<span data-ttu-id="807e1-114">**值**</span><span class="sxs-lookup"><span data-stu-id="807e1-114">**Value**</span></span>|<span data-ttu-id="807e1-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="807e1-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="807e1-116">成功</span><span class="sxs-lookup"><span data-stu-id="807e1-116">Success</span></span>  <br/> |<span data-ttu-id="807e1-117">指示成功。</span><span class="sxs-lookup"><span data-stu-id="807e1-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="807e1-118">警告</span><span class="sxs-lookup"><span data-stu-id="807e1-118">Warning</span></span>  <br/> |<span data-ttu-id="807e1-119">指示警告。</span><span class="sxs-lookup"><span data-stu-id="807e1-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="807e1-120">错误</span><span class="sxs-lookup"><span data-stu-id="807e1-120">Error</span></span>  <br/> |<span data-ttu-id="807e1-121">指示错误。</span><span class="sxs-lookup"><span data-stu-id="807e1-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="807e1-122">子元素</span><span class="sxs-lookup"><span data-stu-id="807e1-122">Child elements</span></span>

|<span data-ttu-id="807e1-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="807e1-123">**Element**</span></span>|<span data-ttu-id="807e1-124">**描述**</span><span class="sxs-lookup"><span data-stu-id="807e1-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="807e1-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="807e1-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="807e1-126">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="807e1-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="807e1-127">MessageText</span><span class="sxs-lookup"><span data-stu-id="807e1-127">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="807e1-128">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="807e1-128">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="807e1-129">MessageXml</span><span class="sxs-lookup"><span data-stu-id="807e1-129">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="807e1-130">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="807e1-130">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="807e1-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="807e1-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="807e1-132">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="807e1-132">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="807e1-133">父元素</span><span class="sxs-lookup"><span data-stu-id="807e1-133">Parent elements</span></span>

|<span data-ttu-id="807e1-134">**元素**</span><span class="sxs-lookup"><span data-stu-id="807e1-134">**Element**</span></span>|<span data-ttu-id="807e1-135">**描述**</span><span class="sxs-lookup"><span data-stu-id="807e1-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="807e1-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="807e1-136">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="807e1-137">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="807e1-137">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="807e1-138">备注</span><span class="sxs-lookup"><span data-stu-id="807e1-138">Remarks</span></span>

<span data-ttu-id="807e1-139">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="807e1-139">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="807e1-140">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="807e1-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="807e1-141">元素信息</span><span class="sxs-lookup"><span data-stu-id="807e1-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="807e1-142">命名空间</span><span class="sxs-lookup"><span data-stu-id="807e1-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="807e1-143">架构名称</span><span class="sxs-lookup"><span data-stu-id="807e1-143">Schema Name</span></span>  <br/> |<span data-ttu-id="807e1-144">消息架构</span><span class="sxs-lookup"><span data-stu-id="807e1-144">Message schema</span></span>  <br/> |
|<span data-ttu-id="807e1-145">验证文件</span><span class="sxs-lookup"><span data-stu-id="807e1-145">Validation File</span></span>  <br/> |<span data-ttu-id="807e1-146">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="807e1-146">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="807e1-147">可以为空</span><span class="sxs-lookup"><span data-stu-id="807e1-147">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="807e1-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="807e1-148">See also</span></span>



- [<span data-ttu-id="807e1-149">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="807e1-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

