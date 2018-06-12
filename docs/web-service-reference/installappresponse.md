---
title: InstallAppResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5e0582d-c1e1-453b-93ed-c31165c82697
description: InstallAppResponse 元素指定 InstallApp 请求的响应。
ms.openlocfilehash: 8e8da720b3a38e979b3d83810bb798350822146c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825942"
---
# <a name="installappresponse"></a><span data-ttu-id="36b91-103">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="36b91-103">InstallAppResponse</span></span>

<span data-ttu-id="36b91-104">**InstallAppResponse**元素指定**InstallApp**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="36b91-104">The **InstallAppResponse** element specifies the response to an **InstallApp** request.</span></span> 
  
```xml
<InstallAppResponse ResponseClass="">
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</InstallAppResponse>
```

 <span data-ttu-id="36b91-105">**InstallAppResponseType**</span><span class="sxs-lookup"><span data-stu-id="36b91-105">**InstallAppResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="36b91-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="36b91-106">Attributes and elements</span></span>

<span data-ttu-id="36b91-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="36b91-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="36b91-108">属性</span><span class="sxs-lookup"><span data-stu-id="36b91-108">Attributes</span></span>

|<span data-ttu-id="36b91-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="36b91-109">**Attribute**</span></span>|<span data-ttu-id="36b91-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="36b91-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="36b91-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="36b91-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="36b91-112">指示响应的类。</span><span class="sxs-lookup"><span data-stu-id="36b91-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="36b91-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="36b91-113">ResponseClass</span></span>

|<span data-ttu-id="36b91-114">**值**</span><span class="sxs-lookup"><span data-stu-id="36b91-114">**Value**</span></span>|<span data-ttu-id="36b91-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="36b91-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="36b91-116">成功</span><span class="sxs-lookup"><span data-stu-id="36b91-116">Success</span></span>  <br/> |<span data-ttu-id="36b91-117">指示成功。</span><span class="sxs-lookup"><span data-stu-id="36b91-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="36b91-118">警告</span><span class="sxs-lookup"><span data-stu-id="36b91-118">Warning</span></span>  <br/> |<span data-ttu-id="36b91-119">指示警告。</span><span class="sxs-lookup"><span data-stu-id="36b91-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="36b91-120">Error</span><span class="sxs-lookup"><span data-stu-id="36b91-120">Error</span></span>  <br/> |<span data-ttu-id="36b91-121">指示错误。</span><span class="sxs-lookup"><span data-stu-id="36b91-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="36b91-122">子元素</span><span class="sxs-lookup"><span data-stu-id="36b91-122">Child elements</span></span>

|<span data-ttu-id="36b91-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="36b91-123">**Element**</span></span>|<span data-ttu-id="36b91-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="36b91-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36b91-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="36b91-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="36b91-126">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="36b91-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="36b91-127">MessageText</span><span class="sxs-lookup"><span data-stu-id="36b91-127">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="36b91-128">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="36b91-128">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="36b91-129">MessageXml</span><span class="sxs-lookup"><span data-stu-id="36b91-129">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="36b91-130">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="36b91-130">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="36b91-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="36b91-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="36b91-132">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="36b91-132">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="36b91-133">父元素</span><span class="sxs-lookup"><span data-stu-id="36b91-133">Parent elements</span></span>

|<span data-ttu-id="36b91-134">**元素**</span><span class="sxs-lookup"><span data-stu-id="36b91-134">**Element**</span></span>|<span data-ttu-id="36b91-135">**说明**</span><span class="sxs-lookup"><span data-stu-id="36b91-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36b91-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="36b91-136">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="36b91-137">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="36b91-137">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="36b91-138">文本值</span><span class="sxs-lookup"><span data-stu-id="36b91-138">Text value</span></span>

<span data-ttu-id="36b91-139">无。</span><span class="sxs-lookup"><span data-stu-id="36b91-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="36b91-140">备注</span><span class="sxs-lookup"><span data-stu-id="36b91-140">Remarks</span></span>

<span data-ttu-id="36b91-141">适用于 Exchange Online 和版本的开头 Exchange 2013 的 Microsoft Exchange Server 的目标设定的客户端**GetAppManifestsResponseMessage**元素。</span><span class="sxs-lookup"><span data-stu-id="36b91-141">The **GetAppManifestsResponseMessage** element is applicable for clients that target Exchange Online and versions of Microsoft Exchange Server starting with Exchange 2013.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="36b91-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="36b91-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36b91-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="36b91-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="36b91-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="36b91-144">Schema Name</span></span>  <br/> |<span data-ttu-id="36b91-145">消息架构</span><span class="sxs-lookup"><span data-stu-id="36b91-145">Message schema</span></span>  <br/> |
|<span data-ttu-id="36b91-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="36b91-146">Validation File</span></span>  <br/> |<span data-ttu-id="36b91-147">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="36b91-147">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="36b91-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="36b91-148">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="36b91-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="36b91-149">See also</span></span>



- [<span data-ttu-id="36b91-150">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="36b91-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

