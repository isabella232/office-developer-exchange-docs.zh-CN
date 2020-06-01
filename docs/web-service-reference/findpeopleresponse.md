---
title: FindPeopleResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 95f016a9-002f-4be3-abd6-f5e3528afd44
description: FindPeopleResponse 元素指定对 FindPeople 请求的响应。
ms.openlocfilehash: b969ac3f7bc2bbd3fc77bf753a15696c3b6d8216
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466400"
---
# <a name="findpeopleresponse"></a><span data-ttu-id="e35d2-103">FindPeopleResponse</span><span class="sxs-lookup"><span data-stu-id="e35d2-103">FindPeopleResponse</span></span>

<span data-ttu-id="e35d2-104">**FindPeopleResponse**元素指定对**FindPeople**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="e35d2-104">The **FindPeopleResponse** element specifies the response to a **FindPeople** request.</span></span> 
  
```XML
<FindPeopleResponse ResponseClass=" Success | Warning | Error ">
    <People/>
    <TotalNumberOfPeopleInView/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</FindPeopleResponse>
```

 <span data-ttu-id="e35d2-105">**FindPeopleResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e35d2-105">**FindPeopleResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e35d2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e35d2-106">Attributes and elements</span></span>

<span data-ttu-id="e35d2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e35d2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e35d2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e35d2-108">Attributes</span></span>

|<span data-ttu-id="e35d2-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="e35d2-109">**Attribute**</span></span>|<span data-ttu-id="e35d2-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="e35d2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e35d2-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="e35d2-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="e35d2-112">指定响应类。</span><span class="sxs-lookup"><span data-stu-id="e35d2-112">Specifies the response class.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="e35d2-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="e35d2-113">ResponseClass</span></span>

|<span data-ttu-id="e35d2-114">**值**</span><span class="sxs-lookup"><span data-stu-id="e35d2-114">**Value**</span></span>|<span data-ttu-id="e35d2-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="e35d2-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e35d2-116">成功</span><span class="sxs-lookup"><span data-stu-id="e35d2-116">Success</span></span>  <br/> |<span data-ttu-id="e35d2-117">指示成功。</span><span class="sxs-lookup"><span data-stu-id="e35d2-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="e35d2-118">警告</span><span class="sxs-lookup"><span data-stu-id="e35d2-118">Warning</span></span>  <br/> |<span data-ttu-id="e35d2-119">指示警告。</span><span class="sxs-lookup"><span data-stu-id="e35d2-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="e35d2-120">错误</span><span class="sxs-lookup"><span data-stu-id="e35d2-120">Error</span></span>  <br/> |<span data-ttu-id="e35d2-121">指示错误。</span><span class="sxs-lookup"><span data-stu-id="e35d2-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e35d2-122">子元素</span><span class="sxs-lookup"><span data-stu-id="e35d2-122">Child elements</span></span>

|<span data-ttu-id="e35d2-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="e35d2-123">**Element**</span></span>|<span data-ttu-id="e35d2-124">**描述**</span><span class="sxs-lookup"><span data-stu-id="e35d2-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e35d2-125">人员</span><span class="sxs-lookup"><span data-stu-id="e35d2-125">People</span></span>](people.md) <br/> |<span data-ttu-id="e35d2-126">指定作为**FindPeople**请求的结果返回的角色数据数组。</span><span class="sxs-lookup"><span data-stu-id="e35d2-126">Specifies an array of persona data returned as the result of a **FindPeople** request.</span></span>  <br/> |
|[<span data-ttu-id="e35d2-127">TotalNumberOfPeopleInView</span><span class="sxs-lookup"><span data-stu-id="e35d2-127">TotalNumberOfPeopleInView</span></span>](totalnumberofpeopleinview.md) <br/> |<span data-ttu-id="e35d2-128">指定由**FindPeople**请求返回的服务器上存储的角色的总数。</span><span class="sxs-lookup"><span data-stu-id="e35d2-128">Specifies the total number of personas stored on a server that are returned by a **FindPeople** request.</span></span>  <br/> |
|[<span data-ttu-id="e35d2-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="e35d2-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="e35d2-130">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="e35d2-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="e35d2-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e35d2-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="e35d2-132">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="e35d2-132">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="e35d2-133">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e35d2-133">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="e35d2-134">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="e35d2-134">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="e35d2-135">MessageXml</span><span class="sxs-lookup"><span data-stu-id="e35d2-135">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="e35d2-136">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="e35d2-136">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e35d2-137">父元素</span><span class="sxs-lookup"><span data-stu-id="e35d2-137">Parent elements</span></span>

|<span data-ttu-id="e35d2-138">**元素**</span><span class="sxs-lookup"><span data-stu-id="e35d2-138">**Element**</span></span>|<span data-ttu-id="e35d2-139">**描述**</span><span class="sxs-lookup"><span data-stu-id="e35d2-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e35d2-140">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e35d2-140">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="e35d2-141">指定响应消息的数组。</span><span class="sxs-lookup"><span data-stu-id="e35d2-141">Specifies an array of response messages.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e35d2-142">备注</span><span class="sxs-lookup"><span data-stu-id="e35d2-142">Remarks</span></span>

<span data-ttu-id="e35d2-143">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e35d2-143">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e35d2-144">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e35d2-144">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e35d2-145">元素信息</span><span class="sxs-lookup"><span data-stu-id="e35d2-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e35d2-146">命名空间</span><span class="sxs-lookup"><span data-stu-id="e35d2-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e35d2-147">架构名称</span><span class="sxs-lookup"><span data-stu-id="e35d2-147">Schema Name</span></span>  <br/> |<span data-ttu-id="e35d2-148">消息架构</span><span class="sxs-lookup"><span data-stu-id="e35d2-148">Message schema</span></span>  <br/> |
|<span data-ttu-id="e35d2-149">验证文件</span><span class="sxs-lookup"><span data-stu-id="e35d2-149">Validation File</span></span>  <br/> |<span data-ttu-id="e35d2-150">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="e35d2-150">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e35d2-151">可以为空</span><span class="sxs-lookup"><span data-stu-id="e35d2-151">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e35d2-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e35d2-152">See also</span></span>



- [<span data-ttu-id="e35d2-153">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e35d2-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

