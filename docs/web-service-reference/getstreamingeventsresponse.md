---
title: GetStreamingEventsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetStreamingEventsResponse
api_type:
- schema
ms.assetid: ea1e7e7e-1b19-4e07-ba42-5dbd888c6db2
description: GetStreamingEventsResponse 元素均表示 GetStreamingEvents 元素请求的响应。
ms.openlocfilehash: 46e606c6093c0e9853668bea10cbdb006191f762
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825681"
---
# <a name="getstreamingeventsresponse"></a><span data-ttu-id="9402a-103">GetStreamingEventsResponse</span><span class="sxs-lookup"><span data-stu-id="9402a-103">GetStreamingEventsResponse</span></span>

<span data-ttu-id="9402a-104">**GetStreamingEventsResponse**元素均表示[GetStreamingEvents](getstreamingevents.md)元素请求的响应。</span><span class="sxs-lookup"><span data-stu-id="9402a-104">The **GetStreamingEventsResponse** element represents a response to a [GetStreamingEvents](getstreamingevents.md) element request.</span></span> 
  
```xml
<GetStreamingEventsResponse>
   <ResponseMessages/>
</GetStreamingEventsResponse>
```

 <span data-ttu-id="9402a-105">**GetStreamingEventsResponseType**</span><span class="sxs-lookup"><span data-stu-id="9402a-105">**GetStreamingEventsResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9402a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9402a-106">Attributes and elements</span></span>

<span data-ttu-id="9402a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9402a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9402a-108">属性</span><span class="sxs-lookup"><span data-stu-id="9402a-108">Attributes</span></span>

<span data-ttu-id="9402a-109">无。</span><span class="sxs-lookup"><span data-stu-id="9402a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9402a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9402a-110">Child elements</span></span>

|<span data-ttu-id="9402a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="9402a-111">**Element**</span></span>|<span data-ttu-id="9402a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="9402a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9402a-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9402a-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="9402a-114">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="9402a-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9402a-115">父元素</span><span class="sxs-lookup"><span data-stu-id="9402a-115">Parent elements</span></span>

<span data-ttu-id="9402a-116">无。</span><span class="sxs-lookup"><span data-stu-id="9402a-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="9402a-117">文本值</span><span class="sxs-lookup"><span data-stu-id="9402a-117">Text value</span></span>

<span data-ttu-id="9402a-118">无。</span><span class="sxs-lookup"><span data-stu-id="9402a-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9402a-119">备注</span><span class="sxs-lookup"><span data-stu-id="9402a-119">Remarks</span></span>

<span data-ttu-id="9402a-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9402a-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9402a-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="9402a-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9402a-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="9402a-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9402a-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="9402a-123">Schema name</span></span>  <br/> |<span data-ttu-id="9402a-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="9402a-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9402a-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="9402a-125">Validation file</span></span>  <br/> |<span data-ttu-id="9402a-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9402a-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9402a-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="9402a-127">Can be empty</span></span>  <br/> |<span data-ttu-id="9402a-128">False</span><span class="sxs-lookup"><span data-stu-id="9402a-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9402a-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9402a-129">See also</span></span>



[<span data-ttu-id="9402a-130">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="9402a-130">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)


- [<span data-ttu-id="9402a-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9402a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

