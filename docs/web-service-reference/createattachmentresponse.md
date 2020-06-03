---
title: CreateAttachmentResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAttachmentResponse
api_type:
- schema
ms.assetid: cf6bd8bb-5317-4a03-bd75-297dd359b5da
description: CreateAttachmentResponse 元素定义对 CreateAttachment 请求的响应。
ms.openlocfilehash: df2b0e37adaeaef32f845e5a28615ce874cb3447
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466414"
---
# <a name="createattachmentresponse"></a><span data-ttu-id="9b989-103">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="9b989-103">CreateAttachmentResponse</span></span>

<span data-ttu-id="9b989-104">**CreateAttachmentResponse**元素定义对 CreateAttachment 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="9b989-104">The **CreateAttachmentResponse** element defines a response to a CreateAttachment request.</span></span> 
  
```xml
<CreateAttachmentResponse>
   <ResponseMessages/>
</CreateAttachmentResponse>
```

 <span data-ttu-id="9b989-105">**CreateAttachmentResponseType**</span><span class="sxs-lookup"><span data-stu-id="9b989-105">**CreateAttachmentResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9b989-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9b989-106">Attributes and elements</span></span>

<span data-ttu-id="9b989-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9b989-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9b989-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9b989-108">Attributes</span></span>

<span data-ttu-id="9b989-109">无。</span><span class="sxs-lookup"><span data-stu-id="9b989-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9b989-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9b989-110">Child elements</span></span>

|<span data-ttu-id="9b989-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="9b989-111">**Element**</span></span>|<span data-ttu-id="9b989-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="9b989-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b989-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9b989-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="9b989-114">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="9b989-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9b989-115">父元素</span><span class="sxs-lookup"><span data-stu-id="9b989-115">Parent elements</span></span>

<span data-ttu-id="9b989-116">无。</span><span class="sxs-lookup"><span data-stu-id="9b989-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9b989-117">说明</span><span class="sxs-lookup"><span data-stu-id="9b989-117">Remarks</span></span>

<span data-ttu-id="9b989-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9b989-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9b989-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="9b989-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b989-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="9b989-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9b989-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="9b989-121">Schema name</span></span>  <br/> |<span data-ttu-id="9b989-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="9b989-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9b989-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="9b989-123">Validation file</span></span>  <br/> |<span data-ttu-id="9b989-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9b989-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9b989-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="9b989-125">Can be empty</span></span>  <br/> |<span data-ttu-id="9b989-126">False</span><span class="sxs-lookup"><span data-stu-id="9b989-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b989-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9b989-127">See also</span></span>



[<span data-ttu-id="9b989-128">CreateAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="9b989-128">CreateAttachment operation</span></span>](createattachment-operation.md)
  
[<span data-ttu-id="9b989-129">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="9b989-129">CreateAttachment</span></span>](createattachment.md)


- [<span data-ttu-id="9b989-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9b989-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

