---
title: DisableAppResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11ebe618-d759-4f16-be99-eaaa817ba782
description: DisableAppResponse 元素指定对 DisableApp 请求的响应。
ms.openlocfilehash: cc28abf644247339e1226cd0e13824cc5f5669be
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455644"
---
# <a name="disableappresponse"></a><span data-ttu-id="aa890-103">DisableAppResponse</span><span class="sxs-lookup"><span data-stu-id="aa890-103">DisableAppResponse</span></span>

<span data-ttu-id="aa890-104">**DisableAppResponse**元素指定对**DisableApp**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="aa890-104">The **DisableAppResponse** element specifies the response to a **DisableApp** request.</span></span> 
  
```XML
<DisableAppResponse>
    <MessageText></MessageText>
    <ResponseCode></ResponeCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</DisableAppResponse>
```

 <span data-ttu-id="aa890-105">**DisableAppResponseType**</span><span class="sxs-lookup"><span data-stu-id="aa890-105">**DisableAppResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aa890-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="aa890-106">Attributes and elements</span></span>

<span data-ttu-id="aa890-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="aa890-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aa890-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="aa890-108">Attributes</span></span>

<span data-ttu-id="aa890-109">无。</span><span class="sxs-lookup"><span data-stu-id="aa890-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aa890-110">子元素</span><span class="sxs-lookup"><span data-stu-id="aa890-110">Child elements</span></span>

|<span data-ttu-id="aa890-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="aa890-111">**Element**</span></span>|<span data-ttu-id="aa890-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="aa890-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa890-113">MessageText</span><span class="sxs-lookup"><span data-stu-id="aa890-113">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="aa890-114">提供响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="aa890-114">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="aa890-115">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="aa890-115">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="aa890-116">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="aa890-116">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="aa890-117">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="aa890-117">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="aa890-118">当前未使用，并已保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="aa890-118">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="aa890-119">MessageXml</span><span class="sxs-lookup"><span data-stu-id="aa890-119">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="aa890-120">提供其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="aa890-120">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aa890-121">父元素</span><span class="sxs-lookup"><span data-stu-id="aa890-121">Parent elements</span></span>

<span data-ttu-id="aa890-122">无。</span><span class="sxs-lookup"><span data-stu-id="aa890-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aa890-123">说明</span><span class="sxs-lookup"><span data-stu-id="aa890-123">Remarks</span></span>

<span data-ttu-id="aa890-124">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="aa890-124">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="aa890-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="aa890-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aa890-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="aa890-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa890-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="aa890-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="aa890-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="aa890-128">Schema Name</span></span>  <br/> |<span data-ttu-id="aa890-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="aa890-129">Message schema</span></span>  <br/> |
|<span data-ttu-id="aa890-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="aa890-130">Validation File</span></span>  <br/> |<span data-ttu-id="aa890-131">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="aa890-131">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="aa890-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="aa890-132">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="aa890-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="aa890-133">See also</span></span>

- [<span data-ttu-id="aa890-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="aa890-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

