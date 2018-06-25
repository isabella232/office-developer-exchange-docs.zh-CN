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
description: ContentId 元素表示内容的附件的标识符。 ContentId 可以设置为任何字符串值。 应用程序可以使用 ContentId 来实现自己标识机制。
ms.openlocfilehash: dc46ae4b33d435f5d47eb7deb39e92fd0170194b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753563"
---
# <a name="contentid"></a><span data-ttu-id="6980b-105">ContentId</span><span class="sxs-lookup"><span data-stu-id="6980b-105">ContentId</span></span>

<span data-ttu-id="6980b-106">**ContentId**元素表示内容的附件的标识符。</span><span class="sxs-lookup"><span data-stu-id="6980b-106">The **ContentId** element represents an identifier for the contents of an attachment.</span></span> <span data-ttu-id="6980b-107">**ContentId**可以设置为任何字符串值。</span><span class="sxs-lookup"><span data-stu-id="6980b-107">**ContentId** can be set to any string value.</span></span> <span data-ttu-id="6980b-108">应用程序可以使用**ContentId**来实现自己标识机制。</span><span class="sxs-lookup"><span data-stu-id="6980b-108">Applications can use **ContentId** to implement their own identification mechanisms.</span></span> 
  
```xml
<ContentId/>
```

 <span data-ttu-id="6980b-109">**字符串**</span><span class="sxs-lookup"><span data-stu-id="6980b-109">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6980b-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6980b-110">Attributes and elements</span></span>

<span data-ttu-id="6980b-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6980b-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6980b-112">属性</span><span class="sxs-lookup"><span data-stu-id="6980b-112">Attributes</span></span>

<span data-ttu-id="6980b-113">无。</span><span class="sxs-lookup"><span data-stu-id="6980b-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6980b-114">子元素</span><span class="sxs-lookup"><span data-stu-id="6980b-114">Child elements</span></span>

<span data-ttu-id="6980b-115">无。</span><span class="sxs-lookup"><span data-stu-id="6980b-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6980b-116">父元素</span><span class="sxs-lookup"><span data-stu-id="6980b-116">Parent elements</span></span>

|<span data-ttu-id="6980b-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="6980b-117">**Element**</span></span>|<span data-ttu-id="6980b-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="6980b-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6980b-119">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="6980b-119">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="6980b-120">代表附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="6980b-120">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="6980b-121">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="6980b-121">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="6980b-122">代表附加到 Exchange 存储中的项的文件。</span><span class="sxs-lookup"><span data-stu-id="6980b-122">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6980b-123">文本值</span><span class="sxs-lookup"><span data-stu-id="6980b-123">Text value</span></span>

<span data-ttu-id="6980b-124">字符串值表示附件的内容的标识符。</span><span class="sxs-lookup"><span data-stu-id="6980b-124">The string value represents the identifier to the contents of an attachment.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6980b-125">备注</span><span class="sxs-lookup"><span data-stu-id="6980b-125">Remarks</span></span>

<span data-ttu-id="6980b-126">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6980b-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6980b-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="6980b-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6980b-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="6980b-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6980b-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="6980b-129">Schema name</span></span>  <br/> |<span data-ttu-id="6980b-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="6980b-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="6980b-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="6980b-131">Validation file</span></span>  <br/> |<span data-ttu-id="6980b-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6980b-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6980b-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="6980b-133">Can be empty</span></span>  <br/> |<span data-ttu-id="6980b-134">False</span><span class="sxs-lookup"><span data-stu-id="6980b-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6980b-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6980b-135">See also</span></span>



- [<span data-ttu-id="6980b-136">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6980b-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

