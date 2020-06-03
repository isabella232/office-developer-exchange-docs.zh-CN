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
description: GetServerTimeZonesResponse 元素定义对 GetServerTimeZones 操作请求的响应。
ms.openlocfilehash: 5a8dbe19055e3b697149c10df610d081cb65430b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460923"
---
# <a name="getservertimezonesresponse"></a><span data-ttu-id="13df7-103">GetServerTimeZonesResponse</span><span class="sxs-lookup"><span data-stu-id="13df7-103">GetServerTimeZonesResponse</span></span>

<span data-ttu-id="13df7-104">**GetServerTimeZonesResponse**元素定义对[GetServerTimeZones 操作](getservertimezones-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="13df7-104">The **GetServerTimeZonesResponse** element defines a response to a [GetServerTimeZones operation](getservertimezones-operation.md) request.</span></span> 
  
```XML
<GetServerTimeZonesResponse>
   <ResponseMessages/>
</GetServerTimeZonesResponse>
```

 <span data-ttu-id="13df7-105">**GetServerTimeZonesResponseType**</span><span class="sxs-lookup"><span data-stu-id="13df7-105">**GetServerTimeZonesResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="13df7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="13df7-106">Attributes and elements</span></span>

<span data-ttu-id="13df7-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="13df7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13df7-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="13df7-108">Attributes</span></span>

<span data-ttu-id="13df7-109">无。</span><span class="sxs-lookup"><span data-stu-id="13df7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="13df7-110">子元素</span><span class="sxs-lookup"><span data-stu-id="13df7-110">Child elements</span></span>

|<span data-ttu-id="13df7-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="13df7-111">**Element**</span></span>|<span data-ttu-id="13df7-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="13df7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13df7-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="13df7-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="13df7-114">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="13df7-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="13df7-115">父元素</span><span class="sxs-lookup"><span data-stu-id="13df7-115">Parent elements</span></span>

<span data-ttu-id="13df7-116">无。</span><span class="sxs-lookup"><span data-stu-id="13df7-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="13df7-117">说明</span><span class="sxs-lookup"><span data-stu-id="13df7-117">Remarks</span></span>

<span data-ttu-id="13df7-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="13df7-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="13df7-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="13df7-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13df7-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="13df7-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="13df7-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="13df7-121">Schema Name</span></span>  <br/> |<span data-ttu-id="13df7-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="13df7-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="13df7-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="13df7-123">Validation File</span></span>  <br/> |<span data-ttu-id="13df7-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="13df7-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="13df7-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="13df7-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="13df7-126">False</span><span class="sxs-lookup"><span data-stu-id="13df7-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13df7-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="13df7-127">See also</span></span>



- [<span data-ttu-id="13df7-128">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="13df7-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

