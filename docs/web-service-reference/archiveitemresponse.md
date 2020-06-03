---
title: ArchiveItemResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 68109a92-c49e-4c0e-b6ec-e90d38d4be4d
description: ArchiveItemResponse 元素指定对 ArchiveItem 请求的响应。
ms.openlocfilehash: 86360846a9a12955e7fa651d5b5027d90b5e56c0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463396"
---
# <a name="archiveitemresponse"></a><span data-ttu-id="b7671-103">ArchiveItemResponse</span><span class="sxs-lookup"><span data-stu-id="b7671-103">ArchiveItemResponse</span></span>

<span data-ttu-id="b7671-104">**ArchiveItemResponse**元素指定对**ArchiveItem**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="b7671-104">The **ArchiveItemResponse** element specifies the response to an **ArchiveItem** request.</span></span> 
  
```XML
<ArchiveItemResponse>
    <ResponseMessages></ResponseMessages>
</ArchiveItemResponse>
```

 <span data-ttu-id="b7671-105">**ArchiveItemResponseType**</span><span class="sxs-lookup"><span data-stu-id="b7671-105">**ArchiveItemResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b7671-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b7671-106">Attributes and elements</span></span>

<span data-ttu-id="b7671-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b7671-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7671-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b7671-108">Attributes</span></span>

<span data-ttu-id="b7671-109">无。</span><span class="sxs-lookup"><span data-stu-id="b7671-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b7671-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b7671-110">Child elements</span></span>

|<span data-ttu-id="b7671-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b7671-111">**Element**</span></span>|<span data-ttu-id="b7671-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b7671-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7671-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b7671-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="b7671-114">包含对 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="b7671-114">Contains the response messages to an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b7671-115">父元素</span><span class="sxs-lookup"><span data-stu-id="b7671-115">Parent elements</span></span>

<span data-ttu-id="b7671-116">无。</span><span class="sxs-lookup"><span data-stu-id="b7671-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b7671-117">说明</span><span class="sxs-lookup"><span data-stu-id="b7671-117">Remarks</span></span>

<span data-ttu-id="b7671-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b7671-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b7671-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b7671-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7671-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="b7671-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7671-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="b7671-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b7671-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="b7671-122">Schema Name</span></span>  <br/> |<span data-ttu-id="b7671-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="b7671-123">Message schema</span></span>  <br/> |
|<span data-ttu-id="b7671-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="b7671-124">Validation File</span></span>  <br/> |<span data-ttu-id="b7671-125">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="b7671-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b7671-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="b7671-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="b7671-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b7671-127">See also</span></span>

- [<span data-ttu-id="b7671-128">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b7671-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

