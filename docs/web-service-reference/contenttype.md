---
title: ContentType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContentType
api_type:
- schema
ms.assetid: f91ff0df-0d8a-43ea-a188-d80f0e885f19
description: ContentType 元素描述附件内容的多用途 Internet 邮件扩展（MIME）类型。
ms.openlocfilehash: cb326bb761ea28e0e9f77501bf754c7c1f0318fb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455224"
---
# <a name="contenttype"></a><span data-ttu-id="35510-103">ContentType</span><span class="sxs-lookup"><span data-stu-id="35510-103">ContentType</span></span>

<span data-ttu-id="35510-104">**ContentType**元素描述附件内容的多用途 Internet 邮件扩展（MIME）类型。</span><span class="sxs-lookup"><span data-stu-id="35510-104">The **ContentType** element describes the Multipurpose Internet Mail Extensions (MIME) type of the attachment content.</span></span> 
  
```xml
<ContentType/>
```

 <span data-ttu-id="35510-105">**String**</span><span class="sxs-lookup"><span data-stu-id="35510-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="35510-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="35510-106">Attributes and elements</span></span>

<span data-ttu-id="35510-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="35510-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="35510-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="35510-108">Attributes</span></span>

<span data-ttu-id="35510-109">无。</span><span class="sxs-lookup"><span data-stu-id="35510-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="35510-110">子元素</span><span class="sxs-lookup"><span data-stu-id="35510-110">Child elements</span></span>

<span data-ttu-id="35510-111">无。</span><span class="sxs-lookup"><span data-stu-id="35510-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="35510-112">父元素</span><span class="sxs-lookup"><span data-stu-id="35510-112">Parent elements</span></span>

|<span data-ttu-id="35510-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="35510-113">**Element**</span></span>|<span data-ttu-id="35510-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="35510-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="35510-115">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="35510-115">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="35510-116">表示附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="35510-116">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="35510-117">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="35510-117">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="35510-118">代表附加到 Exchange 存储中的项目的文件。</span><span class="sxs-lookup"><span data-stu-id="35510-118">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="35510-119">文本值</span><span class="sxs-lookup"><span data-stu-id="35510-119">Text value</span></span>

<span data-ttu-id="35510-120">Text 值是一个 string 值，表示附件的内容类型。</span><span class="sxs-lookup"><span data-stu-id="35510-120">The text value is a string value that represents the content type of the attachment.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="35510-121">说明</span><span class="sxs-lookup"><span data-stu-id="35510-121">Remarks</span></span>

<span data-ttu-id="35510-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="35510-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="35510-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="35510-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35510-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="35510-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="35510-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="35510-125">Schema name</span></span>  <br/> |<span data-ttu-id="35510-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="35510-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="35510-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="35510-127">Validation file</span></span>  <br/> |<span data-ttu-id="35510-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="35510-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="35510-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="35510-129">Can be empty</span></span>  <br/> |<span data-ttu-id="35510-130">False</span><span class="sxs-lookup"><span data-stu-id="35510-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="35510-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="35510-131">See also</span></span>



- [<span data-ttu-id="35510-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="35510-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

