---
title: ConvertIdResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertIdResponse
api_type:
- schema
ms.assetid: ac1f044f-04a4-42ef-b762-cac5cd37894d
description: ConvertIdResponse 元素包含对 ConvertId 请求的响应。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 690f0f2109dfc36dd8f359b7cef1e65beb47fc6e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452522"
---
# <a name="convertidresponse"></a><span data-ttu-id="af1c3-104">ConvertIdResponse</span><span class="sxs-lookup"><span data-stu-id="af1c3-104">ConvertIdResponse</span></span>

<span data-ttu-id="af1c3-105">**ConvertIdResponse**元素包含对 ConvertId 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="af1c3-105">The **ConvertIdResponse** element contains a response to a ConvertId request.</span></span> <span data-ttu-id="af1c3-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="af1c3-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ConvertIdResponse>
   <ResponseMessages/>
</ConvertIdResponse>
```

 <span data-ttu-id="af1c3-107">**ConvertIdResponseType**</span><span class="sxs-lookup"><span data-stu-id="af1c3-107">**ConvertIdResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="af1c3-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="af1c3-108">Attributes and elements</span></span>

<span data-ttu-id="af1c3-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="af1c3-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af1c3-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="af1c3-110">Attributes</span></span>

<span data-ttu-id="af1c3-111">无。</span><span class="sxs-lookup"><span data-stu-id="af1c3-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="af1c3-112">子元素</span><span class="sxs-lookup"><span data-stu-id="af1c3-112">Child elements</span></span>

|<span data-ttu-id="af1c3-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="af1c3-113">**Element**</span></span>|<span data-ttu-id="af1c3-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="af1c3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af1c3-115">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="af1c3-115">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="af1c3-116">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="af1c3-116">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="af1c3-117">父元素</span><span class="sxs-lookup"><span data-stu-id="af1c3-117">Parent elements</span></span>

<span data-ttu-id="af1c3-118">无。</span><span class="sxs-lookup"><span data-stu-id="af1c3-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="af1c3-119">说明</span><span class="sxs-lookup"><span data-stu-id="af1c3-119">Remarks</span></span>

<span data-ttu-id="af1c3-120">[ResponseMessages](responsemessages.md)元素中包含的响应消息将是 ConvertIdResponseMessageType 的实例。</span><span class="sxs-lookup"><span data-stu-id="af1c3-120">The response messages that are contained within the [ResponseMessages](responsemessages.md) element will be instances of ConvertIdResponseMessageType.</span></span> 
  
<span data-ttu-id="af1c3-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="af1c3-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="af1c3-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="af1c3-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af1c3-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="af1c3-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="af1c3-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="af1c3-124">Schema Name</span></span>  <br/> |<span data-ttu-id="af1c3-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="af1c3-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="af1c3-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="af1c3-126">Validation File</span></span>  <br/> |<span data-ttu-id="af1c3-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="af1c3-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="af1c3-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="af1c3-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="af1c3-129">False</span><span class="sxs-lookup"><span data-stu-id="af1c3-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af1c3-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="af1c3-130">See also</span></span>



[<span data-ttu-id="af1c3-131">ConvertId 操作</span><span class="sxs-lookup"><span data-stu-id="af1c3-131">ConvertId operation</span></span>](convertid-operation.md)


- [<span data-ttu-id="af1c3-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="af1c3-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="af1c3-133">转换标识符</span><span class="sxs-lookup"><span data-stu-id="af1c3-133">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

