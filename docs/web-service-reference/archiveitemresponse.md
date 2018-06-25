---
title: ArchiveItemResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 68109a92-c49e-4c0e-b6ec-e90d38d4be4d
description: ArchiveItemResponse 元素指定 ArchiveItem 请求的响应。
ms.openlocfilehash: bfd1b9d76c2b49e00a82bd8f6f57742007d0adf7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753257"
---
# <a name="archiveitemresponse"></a><span data-ttu-id="c5eb8-103">ArchiveItemResponse</span><span class="sxs-lookup"><span data-stu-id="c5eb8-103">ArchiveItemResponse</span></span>

<span data-ttu-id="c5eb8-104">**ArchiveItemResponse**元素指定**ArchiveItem**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="c5eb8-104">The **ArchiveItemResponse** element specifies the response to an **ArchiveItem** request.</span></span> 
  
```XML
<ArchiveItemResponse>
    <ResponseMessages></ResponseMessages>
</ArchiveItemResponse>
```

 <span data-ttu-id="c5eb8-105">**ArchiveItemResponseType**</span><span class="sxs-lookup"><span data-stu-id="c5eb8-105">**ArchiveItemResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c5eb8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c5eb8-106">Attributes and elements</span></span>

<span data-ttu-id="c5eb8-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c5eb8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5eb8-108">属性</span><span class="sxs-lookup"><span data-stu-id="c5eb8-108">Attributes</span></span>

<span data-ttu-id="c5eb8-109">无。</span><span class="sxs-lookup"><span data-stu-id="c5eb8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c5eb8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c5eb8-110">Child elements</span></span>

|<span data-ttu-id="c5eb8-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c5eb8-111">**Element**</span></span>|<span data-ttu-id="c5eb8-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c5eb8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5eb8-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c5eb8-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="c5eb8-114">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="c5eb8-114">Contains the response messages to an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c5eb8-115">父元素</span><span class="sxs-lookup"><span data-stu-id="c5eb8-115">Parent elements</span></span>

<span data-ttu-id="c5eb8-116">无。</span><span class="sxs-lookup"><span data-stu-id="c5eb8-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5eb8-117">备注</span><span class="sxs-lookup"><span data-stu-id="c5eb8-117">Remarks</span></span>

<span data-ttu-id="c5eb8-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c5eb8-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c5eb8-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c5eb8-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5eb8-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="c5eb8-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5eb8-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="c5eb8-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c5eb8-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="c5eb8-122">Schema Name</span></span>  <br/> |<span data-ttu-id="c5eb8-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="c5eb8-123">Message schema</span></span>  <br/> |
|<span data-ttu-id="c5eb8-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="c5eb8-124">Validation File</span></span>  <br/> |<span data-ttu-id="c5eb8-125">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c5eb8-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c5eb8-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="c5eb8-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c5eb8-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c5eb8-127">See also</span></span>

- [<span data-ttu-id="c5eb8-128">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c5eb8-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

