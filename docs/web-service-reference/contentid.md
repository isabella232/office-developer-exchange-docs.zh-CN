---
title: ContentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContentId
api_type:
- schema
ms.assetid: bc59100d-6079-414b-a6e0-7c15feaa3184
description: ContentId 元素表示附件内容的标识符。 ContentId 可以设置为任何字符串值。 应用程序可以使用 ContentId 来实现自己的标识机制。
ms.openlocfilehash: ca89c8790e839326412003f26b738ad1ee956211
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529264"
---
# <a name="contentid"></a><span data-ttu-id="6e844-105">ContentId</span><span class="sxs-lookup"><span data-stu-id="6e844-105">ContentId</span></span>

<span data-ttu-id="6e844-106">**ContentId**元素表示附件内容的标识符。</span><span class="sxs-lookup"><span data-stu-id="6e844-106">The **ContentId** element represents an identifier for the contents of an attachment.</span></span> <span data-ttu-id="6e844-107">**ContentId**可以设置为任何字符串值。</span><span class="sxs-lookup"><span data-stu-id="6e844-107">**ContentId** can be set to any string value.</span></span> <span data-ttu-id="6e844-108">应用程序可以使用**ContentId**来实现自己的标识机制。</span><span class="sxs-lookup"><span data-stu-id="6e844-108">Applications can use **ContentId** to implement their own identification mechanisms.</span></span> 
  
```xml
<ContentId/>
```

 <span data-ttu-id="6e844-109">**String**</span><span class="sxs-lookup"><span data-stu-id="6e844-109">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6e844-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6e844-110">Attributes and elements</span></span>

<span data-ttu-id="6e844-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6e844-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6e844-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="6e844-112">Attributes</span></span>

<span data-ttu-id="6e844-113">无。</span><span class="sxs-lookup"><span data-stu-id="6e844-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6e844-114">子元素</span><span class="sxs-lookup"><span data-stu-id="6e844-114">Child elements</span></span>

<span data-ttu-id="6e844-115">无。</span><span class="sxs-lookup"><span data-stu-id="6e844-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6e844-116">父元素</span><span class="sxs-lookup"><span data-stu-id="6e844-116">Parent elements</span></span>

|<span data-ttu-id="6e844-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="6e844-117">**Element**</span></span>|<span data-ttu-id="6e844-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="6e844-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6e844-119">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="6e844-119">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="6e844-120">表示附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="6e844-120">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="6e844-121">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="6e844-121">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="6e844-122">代表附加到 Exchange 存储中的项目的文件。</span><span class="sxs-lookup"><span data-stu-id="6e844-122">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6e844-123">文本值</span><span class="sxs-lookup"><span data-stu-id="6e844-123">Text value</span></span>

<span data-ttu-id="6e844-124">字符串值表示附件内容的标识符。</span><span class="sxs-lookup"><span data-stu-id="6e844-124">The string value represents the identifier to the contents of an attachment.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6e844-125">说明</span><span class="sxs-lookup"><span data-stu-id="6e844-125">Remarks</span></span>

<span data-ttu-id="6e844-126">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6e844-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6e844-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="6e844-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e844-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="6e844-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6e844-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="6e844-129">Schema name</span></span>  <br/> |<span data-ttu-id="6e844-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="6e844-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="6e844-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="6e844-131">Validation file</span></span>  <br/> |<span data-ttu-id="6e844-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6e844-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6e844-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="6e844-133">Can be empty</span></span>  <br/> |<span data-ttu-id="6e844-134">False</span><span class="sxs-lookup"><span data-stu-id="6e844-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6e844-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6e844-135">See also</span></span>



- [<span data-ttu-id="6e844-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6e844-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

