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
description: InvalidRecipient 元素包含无效收件人的 SMTP 地址，以及有关收件人无效的原因的信息。
ms.openlocfilehash: f301b31c1054625151ce90e41fca5e3efc21f473
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526548"
---
# <a name="invalidrecipient"></a><span data-ttu-id="0c1f0-103">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="0c1f0-103">InvalidRecipient</span></span>

<span data-ttu-id="0c1f0-104">**InvalidRecipient**元素包含无效收件人的 SMTP 地址，以及有关收件人无效的原因的信息。</span><span class="sxs-lookup"><span data-stu-id="0c1f0-104">The **InvalidRecipient** element contains the SMTP address of the invalid recipient and information about why the recipient is invalid.</span></span> 
  
```XML
<InvalidRecipient>
   <SmtpAddress/>
   <ResponseCode/>
   <MessageText/>
</InvalidRecipient>

```

 <span data-ttu-id="0c1f0-105">**InvalidRecipientType**</span><span class="sxs-lookup"><span data-stu-id="0c1f0-105">**InvalidRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0c1f0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0c1f0-106">Attributes and elements</span></span>

<span data-ttu-id="0c1f0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0c1f0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c1f0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="0c1f0-108">Attributes</span></span>

<span data-ttu-id="0c1f0-109">无。</span><span class="sxs-lookup"><span data-stu-id="0c1f0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0c1f0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0c1f0-110">Child elements</span></span>

|<span data-ttu-id="0c1f0-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="0c1f0-111">**Element**</span></span>|<span data-ttu-id="0c1f0-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="0c1f0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0c1f0-113">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="0c1f0-113">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="0c1f0-114">包含无效收件人的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="0c1f0-114">Contains the SMTP address of the invalid recipient.</span></span> <span data-ttu-id="0c1f0-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="0c1f0-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="0c1f0-116">ResponseCode （InvalidRecipientResponseCodeType）</span><span class="sxs-lookup"><span data-stu-id="0c1f0-116">ResponseCode (InvalidRecipientResponseCodeType)</span></span>](responsecode-invalidrecipientresponsecodetype.md) <br/> |<span data-ttu-id="0c1f0-117">提供用于标识请求遇到的特定错误的错误代码。</span><span class="sxs-lookup"><span data-stu-id="0c1f0-117">Provides an error code that identifies the specific error that the request encountered.</span></span> <span data-ttu-id="0c1f0-118">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="0c1f0-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="0c1f0-119">MessageText</span><span class="sxs-lookup"><span data-stu-id="0c1f0-119">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0c1f0-120">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="0c1f0-120">Provides a text description of the status of the response.</span></span> <span data-ttu-id="0c1f0-121">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="0c1f0-121">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0c1f0-122">父元素</span><span class="sxs-lookup"><span data-stu-id="0c1f0-122">Parent elements</span></span>

|<span data-ttu-id="0c1f0-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="0c1f0-123">**Element**</span></span>|<span data-ttu-id="0c1f0-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="0c1f0-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0c1f0-125">InvalidRecipients</span><span class="sxs-lookup"><span data-stu-id="0c1f0-125">InvalidRecipients</span></span>](invalidrecipients.md) <br/> |<span data-ttu-id="0c1f0-126">表示无效的文件夹共享请求的收件人。</span><span class="sxs-lookup"><span data-stu-id="0c1f0-126">Represents the recipients of a folder sharing request that are invalid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c1f0-127">说明</span><span class="sxs-lookup"><span data-stu-id="0c1f0-127">Remarks</span></span>

<span data-ttu-id="0c1f0-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0c1f0-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0c1f0-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="0c1f0-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c1f0-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="0c1f0-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0c1f0-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="0c1f0-131">Schema Name</span></span>  <br/> |<span data-ttu-id="0c1f0-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="0c1f0-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="0c1f0-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="0c1f0-133">Validation File</span></span>  <br/> |<span data-ttu-id="0c1f0-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0c1f0-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0c1f0-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="0c1f0-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="0c1f0-136">False</span><span class="sxs-lookup"><span data-stu-id="0c1f0-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c1f0-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0c1f0-137">See also</span></span>



[<span data-ttu-id="0c1f0-138">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="0c1f0-138">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="0c1f0-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0c1f0-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

