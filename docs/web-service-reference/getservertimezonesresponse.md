---
title: GetServerTimeZonesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServerTimeZonesResponse
api_type:
- schema
ms.assetid: 97c94d32-10f1-4c3e-ab20-9fd7e8257e50
description: GetServerTimeZonesResponse 元素定义 GetServerTimeZones 操作请求的响应。
ms.openlocfilehash: 119809076c82ff75a6dd061fc976f861e13f4e57
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825664"
---
# <a name="getservertimezonesresponse"></a><span data-ttu-id="2e8f8-103">GetServerTimeZonesResponse</span><span class="sxs-lookup"><span data-stu-id="2e8f8-103">GetServerTimeZonesResponse</span></span>

<span data-ttu-id="2e8f8-104">**GetServerTimeZonesResponse**元素定义[GetServerTimeZones 操作](getservertimezones-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="2e8f8-104">The **GetServerTimeZonesResponse** element defines a response to a [GetServerTimeZones operation](getservertimezones-operation.md) request.</span></span> 
  
```XML
<GetServerTimeZonesResponse>
   <ResponseMessages/>
</GetServerTimeZonesResponse>
```

 <span data-ttu-id="2e8f8-105">**GetServerTimeZonesResponseType**</span><span class="sxs-lookup"><span data-stu-id="2e8f8-105">**GetServerTimeZonesResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2e8f8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2e8f8-106">Attributes and elements</span></span>

<span data-ttu-id="2e8f8-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2e8f8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e8f8-108">属性</span><span class="sxs-lookup"><span data-stu-id="2e8f8-108">Attributes</span></span>

<span data-ttu-id="2e8f8-109">无。</span><span class="sxs-lookup"><span data-stu-id="2e8f8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2e8f8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2e8f8-110">Child elements</span></span>

|<span data-ttu-id="2e8f8-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2e8f8-111">**Element**</span></span>|<span data-ttu-id="2e8f8-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2e8f8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e8f8-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2e8f8-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="2e8f8-114">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="2e8f8-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2e8f8-115">父元素</span><span class="sxs-lookup"><span data-stu-id="2e8f8-115">Parent elements</span></span>

<span data-ttu-id="2e8f8-116">无。</span><span class="sxs-lookup"><span data-stu-id="2e8f8-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e8f8-117">备注</span><span class="sxs-lookup"><span data-stu-id="2e8f8-117">Remarks</span></span>

<span data-ttu-id="2e8f8-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2e8f8-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2e8f8-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="2e8f8-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e8f8-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="2e8f8-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2e8f8-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="2e8f8-121">Schema Name</span></span>  <br/> |<span data-ttu-id="2e8f8-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="2e8f8-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2e8f8-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="2e8f8-123">Validation File</span></span>  <br/> |<span data-ttu-id="2e8f8-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2e8f8-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2e8f8-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="2e8f8-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="2e8f8-126">False</span><span class="sxs-lookup"><span data-stu-id="2e8f8-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e8f8-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2e8f8-127">See also</span></span>



- [<span data-ttu-id="2e8f8-128">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2e8f8-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

