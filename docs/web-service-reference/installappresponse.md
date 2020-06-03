---
title: InstallAppResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5e0582d-c1e1-453b-93ed-c31165c82697
description: InstallAppResponse 元素指定对 InstallApp 请求的响应。
ms.openlocfilehash: 0f7690e2df7e71c4e478dec191671af24f96294b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465665"
---
# <a name="installappresponse"></a><span data-ttu-id="beca5-103">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="beca5-103">InstallAppResponse</span></span>

<span data-ttu-id="beca5-104">**InstallAppResponse**元素指定对**InstallApp**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="beca5-104">The **InstallAppResponse** element specifies the response to an **InstallApp** request.</span></span> 
  
```xml
<InstallAppResponse ResponseClass="">
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</InstallAppResponse>
```

 <span data-ttu-id="beca5-105">**InstallAppResponseType**</span><span class="sxs-lookup"><span data-stu-id="beca5-105">**InstallAppResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="beca5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="beca5-106">Attributes and elements</span></span>

<span data-ttu-id="beca5-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="beca5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="beca5-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="beca5-108">Attributes</span></span>

|<span data-ttu-id="beca5-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="beca5-109">**Attribute**</span></span>|<span data-ttu-id="beca5-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="beca5-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="beca5-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="beca5-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="beca5-112">指示响应的类。</span><span class="sxs-lookup"><span data-stu-id="beca5-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="beca5-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="beca5-113">ResponseClass</span></span>

|<span data-ttu-id="beca5-114">**值**</span><span class="sxs-lookup"><span data-stu-id="beca5-114">**Value**</span></span>|<span data-ttu-id="beca5-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="beca5-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="beca5-116">成功</span><span class="sxs-lookup"><span data-stu-id="beca5-116">Success</span></span>  <br/> |<span data-ttu-id="beca5-117">指示成功。</span><span class="sxs-lookup"><span data-stu-id="beca5-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="beca5-118">警告</span><span class="sxs-lookup"><span data-stu-id="beca5-118">Warning</span></span>  <br/> |<span data-ttu-id="beca5-119">指示警告。</span><span class="sxs-lookup"><span data-stu-id="beca5-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="beca5-120">错误</span><span class="sxs-lookup"><span data-stu-id="beca5-120">Error</span></span>  <br/> |<span data-ttu-id="beca5-121">指示错误。</span><span class="sxs-lookup"><span data-stu-id="beca5-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="beca5-122">子元素</span><span class="sxs-lookup"><span data-stu-id="beca5-122">Child elements</span></span>

|<span data-ttu-id="beca5-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="beca5-123">**Element**</span></span>|<span data-ttu-id="beca5-124">**描述**</span><span class="sxs-lookup"><span data-stu-id="beca5-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="beca5-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="beca5-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="beca5-126">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="beca5-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="beca5-127">MessageText</span><span class="sxs-lookup"><span data-stu-id="beca5-127">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="beca5-128">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="beca5-128">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="beca5-129">MessageXml</span><span class="sxs-lookup"><span data-stu-id="beca5-129">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="beca5-130">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="beca5-130">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="beca5-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="beca5-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="beca5-132">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="beca5-132">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="beca5-133">父元素</span><span class="sxs-lookup"><span data-stu-id="beca5-133">Parent elements</span></span>

|<span data-ttu-id="beca5-134">**元素**</span><span class="sxs-lookup"><span data-stu-id="beca5-134">**Element**</span></span>|<span data-ttu-id="beca5-135">**描述**</span><span class="sxs-lookup"><span data-stu-id="beca5-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="beca5-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="beca5-136">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="beca5-137">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="beca5-137">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="beca5-138">文本值</span><span class="sxs-lookup"><span data-stu-id="beca5-138">Text value</span></span>

<span data-ttu-id="beca5-139">无。</span><span class="sxs-lookup"><span data-stu-id="beca5-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="beca5-140">说明</span><span class="sxs-lookup"><span data-stu-id="beca5-140">Remarks</span></span>

<span data-ttu-id="beca5-141">**GetAppManifestsResponseMessage**元素适用于面向 exchange Online 的客户端和从 exchange 2013 开始的 Microsoft Exchange Server 版本。</span><span class="sxs-lookup"><span data-stu-id="beca5-141">The **GetAppManifestsResponseMessage** element is applicable for clients that target Exchange Online and versions of Microsoft Exchange Server starting with Exchange 2013.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="beca5-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="beca5-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="beca5-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="beca5-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="beca5-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="beca5-144">Schema Name</span></span>  <br/> |<span data-ttu-id="beca5-145">消息架构</span><span class="sxs-lookup"><span data-stu-id="beca5-145">Message schema</span></span>  <br/> |
|<span data-ttu-id="beca5-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="beca5-146">Validation File</span></span>  <br/> |<span data-ttu-id="beca5-147">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="beca5-147">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="beca5-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="beca5-148">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="beca5-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="beca5-149">See also</span></span>



- [<span data-ttu-id="beca5-150">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="beca5-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

