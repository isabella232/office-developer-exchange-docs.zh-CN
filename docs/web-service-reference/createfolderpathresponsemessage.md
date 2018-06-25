---
title: CreateFolderPathResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f7b3507-713d-4ccf-8518-75fa6f967d6d
description: CreateFolderPathResponseMessage 元素指定 CreateFolderPath 请求的响应消息。
ms.openlocfilehash: f8f85cc246bb5d5ecd5cb745267d9d373286cf7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753646"
---
# <a name="createfolderpathresponsemessage"></a><span data-ttu-id="e53f0-103">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e53f0-103">CreateFolderPathResponseMessage</span></span>

<span data-ttu-id="e53f0-104">**CreateFolderPathResponseMessage**元素指定**CreateFolderPath**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="e53f0-104">The **CreateFolderPathResponseMessage** element specifies the response message for a **CreateFolderPath** request.</span></span> 
  
```XML
<CreateFolderPathResponseMessage ResponseClass="">
    <Folders></Folders>
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</CreateFolderPathResponseMessage>
```

 <span data-ttu-id="e53f0-105">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e53f0-105">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e53f0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e53f0-106">Attributes and elements</span></span>

<span data-ttu-id="e53f0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e53f0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e53f0-108">属性</span><span class="sxs-lookup"><span data-stu-id="e53f0-108">Attributes</span></span>

|<span data-ttu-id="e53f0-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="e53f0-109">**Attribute**</span></span>|<span data-ttu-id="e53f0-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="e53f0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e53f0-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="e53f0-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="e53f0-112">指示响应的类。</span><span class="sxs-lookup"><span data-stu-id="e53f0-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="e53f0-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="e53f0-113">ResponseClass</span></span>

|<span data-ttu-id="e53f0-114">**值**</span><span class="sxs-lookup"><span data-stu-id="e53f0-114">**Value**</span></span>|<span data-ttu-id="e53f0-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="e53f0-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e53f0-116">成功</span><span class="sxs-lookup"><span data-stu-id="e53f0-116">Success</span></span>  <br/> |<span data-ttu-id="e53f0-117">指示成功。</span><span class="sxs-lookup"><span data-stu-id="e53f0-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="e53f0-118">警告</span><span class="sxs-lookup"><span data-stu-id="e53f0-118">Warning</span></span>  <br/> |<span data-ttu-id="e53f0-119">指示警告。</span><span class="sxs-lookup"><span data-stu-id="e53f0-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="e53f0-120">错误</span><span class="sxs-lookup"><span data-stu-id="e53f0-120">Error</span></span>  <br/> |<span data-ttu-id="e53f0-121">指示错误。</span><span class="sxs-lookup"><span data-stu-id="e53f0-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e53f0-122">子元素</span><span class="sxs-lookup"><span data-stu-id="e53f0-122">Child elements</span></span>

|<span data-ttu-id="e53f0-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="e53f0-123">**Element**</span></span>|<span data-ttu-id="e53f0-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="e53f0-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e53f0-125">Folders</span><span class="sxs-lookup"><span data-stu-id="e53f0-125">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e53f0-126">包含一数组的文件夹操作中使用的文件夹。</span><span class="sxs-lookup"><span data-stu-id="e53f0-126">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
|[<span data-ttu-id="e53f0-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e53f0-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="e53f0-128">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="e53f0-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="e53f0-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="e53f0-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="e53f0-130">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="e53f0-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="e53f0-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="e53f0-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="e53f0-132">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="e53f0-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="e53f0-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e53f0-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="e53f0-134">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="e53f0-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e53f0-135">父元素</span><span class="sxs-lookup"><span data-stu-id="e53f0-135">Parent elements</span></span>

|<span data-ttu-id="e53f0-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="e53f0-136">**Element**</span></span>|<span data-ttu-id="e53f0-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="e53f0-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e53f0-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e53f0-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="e53f0-139">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="e53f0-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e53f0-140">备注</span><span class="sxs-lookup"><span data-stu-id="e53f0-140">Remarks</span></span>

<span data-ttu-id="e53f0-141">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e53f0-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e53f0-142">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e53f0-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e53f0-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="e53f0-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e53f0-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="e53f0-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e53f0-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="e53f0-145">Schema Name</span></span>  <br/> |<span data-ttu-id="e53f0-146">消息架构</span><span class="sxs-lookup"><span data-stu-id="e53f0-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="e53f0-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="e53f0-147">Validation File</span></span>  <br/> |<span data-ttu-id="e53f0-148">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e53f0-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e53f0-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="e53f0-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e53f0-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e53f0-150">See also</span></span>

- [<span data-ttu-id="e53f0-151">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e53f0-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

