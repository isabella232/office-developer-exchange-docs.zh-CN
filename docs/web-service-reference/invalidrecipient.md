---
title: InvalidRecipient
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InvalidRecipient
api_type:
- schema
ms.assetid: 9e2d3433-22d7-444b-9883-e5649297d8fe
description: InvalidRecipient 元素包含无效的收件人和信息收件人为什么是无效的 SMTP 地址。
ms.openlocfilehash: 800056666e486e9337dcd1c2786f7e6db1e060bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825961"
---
# <a name="invalidrecipient"></a><span data-ttu-id="e2db7-103">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="e2db7-103">InvalidRecipient</span></span>

<span data-ttu-id="e2db7-104">**InvalidRecipient**元素包含无效的收件人和信息收件人为什么是无效的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="e2db7-104">The **InvalidRecipient** element contains the SMTP address of the invalid recipient and information about why the recipient is invalid.</span></span> 
  
```XML
<InvalidRecipient>
   <SmtpAddress/>
   <ResponseCode/>
   <MessageText/>
</InvalidRecipient>

```

 <span data-ttu-id="e2db7-105">**InvalidRecipientType**</span><span class="sxs-lookup"><span data-stu-id="e2db7-105">**InvalidRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e2db7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e2db7-106">Attributes and elements</span></span>

<span data-ttu-id="e2db7-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e2db7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2db7-108">属性</span><span class="sxs-lookup"><span data-stu-id="e2db7-108">Attributes</span></span>

<span data-ttu-id="e2db7-109">无。</span><span class="sxs-lookup"><span data-stu-id="e2db7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e2db7-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e2db7-110">Child elements</span></span>

|<span data-ttu-id="e2db7-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e2db7-111">**Element**</span></span>|<span data-ttu-id="e2db7-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e2db7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2db7-113">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="e2db7-113">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="e2db7-114">包含无效的收件人的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="e2db7-114">Contains the SMTP address of the invalid recipient.</span></span> <span data-ttu-id="e2db7-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="e2db7-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="e2db7-116">ResponseCode (InvalidRecipientResponseCodeType)</span><span class="sxs-lookup"><span data-stu-id="e2db7-116">ResponseCode (InvalidRecipientResponseCodeType)</span></span>](responsecode-invalidrecipientresponsecodetype.md) <br/> |<span data-ttu-id="e2db7-117">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="e2db7-117">Provides an error code that identifies the specific error that the request encountered.</span></span> <span data-ttu-id="e2db7-118">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="e2db7-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="e2db7-119">MessageText</span><span class="sxs-lookup"><span data-stu-id="e2db7-119">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="e2db7-120">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="e2db7-120">Provides a text description of the status of the response.</span></span> <span data-ttu-id="e2db7-121">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="e2db7-121">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e2db7-122">父元素</span><span class="sxs-lookup"><span data-stu-id="e2db7-122">Parent elements</span></span>

|<span data-ttu-id="e2db7-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="e2db7-123">**Element**</span></span>|<span data-ttu-id="e2db7-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="e2db7-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2db7-125">InvalidRecipients</span><span class="sxs-lookup"><span data-stu-id="e2db7-125">InvalidRecipients</span></span>](invalidrecipients.md) <br/> |<span data-ttu-id="e2db7-126">代表共享请求的文件夹中的收件人，无效。</span><span class="sxs-lookup"><span data-stu-id="e2db7-126">Represents the recipients of a folder sharing request that are invalid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2db7-127">备注</span><span class="sxs-lookup"><span data-stu-id="e2db7-127">Remarks</span></span>

<span data-ttu-id="e2db7-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e2db7-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e2db7-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="e2db7-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2db7-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="e2db7-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e2db7-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="e2db7-131">Schema Name</span></span>  <br/> |<span data-ttu-id="e2db7-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="e2db7-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="e2db7-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="e2db7-133">Validation File</span></span>  <br/> |<span data-ttu-id="e2db7-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e2db7-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e2db7-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="e2db7-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="e2db7-136">False</span><span class="sxs-lookup"><span data-stu-id="e2db7-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2db7-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e2db7-137">See also</span></span>



[<span data-ttu-id="e2db7-138">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="e2db7-138">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="e2db7-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e2db7-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

