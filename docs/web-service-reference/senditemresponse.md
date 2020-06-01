---
title: SendItemResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendItemResponse
api_type:
- schema
ms.assetid: 26ac41c7-57d9-473e-ab7a-bae93e1d2aba
description: SendItemResponse 元素定义对 SendItem 请求的响应。
ms.openlocfilehash: dd90510547c3db8c3531663c23d05055bd774fab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462127"
---
# <a name="senditemresponse"></a><span data-ttu-id="d43f9-103">SendItemResponse</span><span class="sxs-lookup"><span data-stu-id="d43f9-103">SendItemResponse</span></span>

<span data-ttu-id="d43f9-104">**SendItemResponse**元素定义对 SendItem 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="d43f9-104">The **SendItemResponse** element defines a response to a SendItem request.</span></span> 
  
```xml
<SendItemResponse>
   <ResponseMessages/>
</SendItemResponse>
```

 <span data-ttu-id="d43f9-105">**SendItemResponseType**</span><span class="sxs-lookup"><span data-stu-id="d43f9-105">**SendItemResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d43f9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d43f9-106">Attributes and elements</span></span>

<span data-ttu-id="d43f9-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d43f9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d43f9-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d43f9-108">Attributes</span></span>

<span data-ttu-id="d43f9-109">无。</span><span class="sxs-lookup"><span data-stu-id="d43f9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d43f9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d43f9-110">Child elements</span></span>

|<span data-ttu-id="d43f9-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d43f9-111">**Element**</span></span>|<span data-ttu-id="d43f9-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d43f9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d43f9-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d43f9-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="d43f9-114">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="d43f9-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d43f9-115">父元素</span><span class="sxs-lookup"><span data-stu-id="d43f9-115">Parent elements</span></span>

<span data-ttu-id="d43f9-116">无。</span><span class="sxs-lookup"><span data-stu-id="d43f9-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d43f9-117">说明</span><span class="sxs-lookup"><span data-stu-id="d43f9-117">Remarks</span></span>

<span data-ttu-id="d43f9-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d43f9-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d43f9-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="d43f9-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d43f9-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="d43f9-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d43f9-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="d43f9-121">Schema name</span></span>  <br/> |<span data-ttu-id="d43f9-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="d43f9-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d43f9-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="d43f9-123">Validation file</span></span>  <br/> |<span data-ttu-id="d43f9-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d43f9-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d43f9-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="d43f9-125">Can be empty</span></span>  <br/> |<span data-ttu-id="d43f9-126">False</span><span class="sxs-lookup"><span data-stu-id="d43f9-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d43f9-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d43f9-127">See also</span></span>



[<span data-ttu-id="d43f9-128">SendItem 操作</span><span class="sxs-lookup"><span data-stu-id="d43f9-128">SendItem operation</span></span>](senditem-operation.md)
  
[<span data-ttu-id="d43f9-129">SendItem</span><span class="sxs-lookup"><span data-stu-id="d43f9-129">SendItem</span></span>](senditem.md)


- [<span data-ttu-id="d43f9-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d43f9-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

