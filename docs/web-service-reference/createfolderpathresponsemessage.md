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
ms.openlocfilehash: 3c0c4e98b568a6398dcd0e71a6e6931a3f47e3da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458885"
---
# <a name="createfolderpathresponsemessage"></a><span data-ttu-id="99cec-103">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="99cec-103">CreateFolderPathResponseMessage</span></span>

<span data-ttu-id="99cec-104">**CreateFolderPathResponseMessage**元素指定**CreateFolderPath**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="99cec-104">The **CreateFolderPathResponseMessage** element specifies the response message for a **CreateFolderPath** request.</span></span> 
  
```XML
<CreateFolderPathResponseMessage ResponseClass="">
    <Folders></Folders>
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</CreateFolderPathResponseMessage>
```

 <span data-ttu-id="99cec-105">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="99cec-105">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="99cec-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="99cec-106">Attributes and elements</span></span>

<span data-ttu-id="99cec-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="99cec-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="99cec-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="99cec-108">Attributes</span></span>

|<span data-ttu-id="99cec-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="99cec-109">**Attribute**</span></span>|<span data-ttu-id="99cec-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="99cec-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="99cec-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="99cec-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="99cec-112">指示响应的类。</span><span class="sxs-lookup"><span data-stu-id="99cec-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="99cec-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="99cec-113">ResponseClass</span></span>

|<span data-ttu-id="99cec-114">**值**</span><span class="sxs-lookup"><span data-stu-id="99cec-114">**Value**</span></span>|<span data-ttu-id="99cec-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="99cec-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="99cec-116">成功</span><span class="sxs-lookup"><span data-stu-id="99cec-116">Success</span></span>  <br/> |<span data-ttu-id="99cec-117">指示成功。</span><span class="sxs-lookup"><span data-stu-id="99cec-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="99cec-118">警告</span><span class="sxs-lookup"><span data-stu-id="99cec-118">Warning</span></span>  <br/> |<span data-ttu-id="99cec-119">指示警告。</span><span class="sxs-lookup"><span data-stu-id="99cec-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="99cec-120">错误</span><span class="sxs-lookup"><span data-stu-id="99cec-120">Error</span></span>  <br/> |<span data-ttu-id="99cec-121">指示错误。</span><span class="sxs-lookup"><span data-stu-id="99cec-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="99cec-122">子元素</span><span class="sxs-lookup"><span data-stu-id="99cec-122">Child elements</span></span>

|<span data-ttu-id="99cec-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="99cec-123">**Element**</span></span>|<span data-ttu-id="99cec-124">**描述**</span><span class="sxs-lookup"><span data-stu-id="99cec-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99cec-125">Folders</span><span class="sxs-lookup"><span data-stu-id="99cec-125">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="99cec-126">包含一数组的文件夹操作中使用的文件夹。</span><span class="sxs-lookup"><span data-stu-id="99cec-126">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
|[<span data-ttu-id="99cec-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="99cec-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="99cec-128">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="99cec-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="99cec-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="99cec-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="99cec-130">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="99cec-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="99cec-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="99cec-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="99cec-132">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="99cec-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="99cec-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="99cec-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="99cec-134">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="99cec-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="99cec-135">父元素</span><span class="sxs-lookup"><span data-stu-id="99cec-135">Parent elements</span></span>

|<span data-ttu-id="99cec-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="99cec-136">**Element**</span></span>|<span data-ttu-id="99cec-137">**描述**</span><span class="sxs-lookup"><span data-stu-id="99cec-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99cec-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="99cec-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="99cec-139">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="99cec-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99cec-140">备注</span><span class="sxs-lookup"><span data-stu-id="99cec-140">Remarks</span></span>

<span data-ttu-id="99cec-141">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="99cec-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="99cec-142">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="99cec-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="99cec-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="99cec-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99cec-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="99cec-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="99cec-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="99cec-145">Schema Name</span></span>  <br/> |<span data-ttu-id="99cec-146">消息架构</span><span class="sxs-lookup"><span data-stu-id="99cec-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="99cec-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="99cec-147">Validation File</span></span>  <br/> |<span data-ttu-id="99cec-148">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="99cec-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="99cec-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="99cec-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="99cec-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="99cec-150">See also</span></span>

- [<span data-ttu-id="99cec-151">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="99cec-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

