---
title: ContentLocation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContentLocation
api_type:
- schema
ms.assetid: d91cf587-24e3-4c13-8784-5ca29787cca7
description: ContentLocation 元素包含与附件内容的位置相对应的统一资源标识符（URI）。
ms.openlocfilehash: 01bb95da5f620fddc8777f88b1d3eb1a7e6069b1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461483"
---
# <a name="contentlocation"></a><span data-ttu-id="881d1-103">ContentLocation</span><span class="sxs-lookup"><span data-stu-id="881d1-103">ContentLocation</span></span>

<span data-ttu-id="881d1-104">**ContentLocation**元素包含与附件内容的位置相对应的统一资源标识符（URI）。</span><span class="sxs-lookup"><span data-stu-id="881d1-104">The **ContentLocation** element contains the Uniform Resource Identifier (URI) that corresponds to the location of the content of an attachment.</span></span> 
  
```xml
<ContentLocation/>
```

 <span data-ttu-id="881d1-105">**String**</span><span class="sxs-lookup"><span data-stu-id="881d1-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="881d1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="881d1-106">Attributes and elements</span></span>

<span data-ttu-id="881d1-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="881d1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="881d1-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="881d1-108">Attributes</span></span>

<span data-ttu-id="881d1-109">无。</span><span class="sxs-lookup"><span data-stu-id="881d1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="881d1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="881d1-110">Child elements</span></span>

<span data-ttu-id="881d1-111">无。</span><span class="sxs-lookup"><span data-stu-id="881d1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="881d1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="881d1-112">Parent elements</span></span>

|<span data-ttu-id="881d1-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="881d1-113">**Element**</span></span>|<span data-ttu-id="881d1-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="881d1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="881d1-115">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="881d1-115">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="881d1-116">表示附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="881d1-116">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="881d1-117">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="881d1-117">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="881d1-118">代表附加到 Exchange 存储中的项目的文件。</span><span class="sxs-lookup"><span data-stu-id="881d1-118">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="881d1-119">文本值</span><span class="sxs-lookup"><span data-stu-id="881d1-119">Text value</span></span>

<span data-ttu-id="881d1-120">Text 值是一个代表 URI 的字符串值。</span><span class="sxs-lookup"><span data-stu-id="881d1-120">The text value is a string value that represents a URI.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="881d1-121">说明</span><span class="sxs-lookup"><span data-stu-id="881d1-121">Remarks</span></span>

<span data-ttu-id="881d1-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="881d1-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="881d1-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="881d1-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="881d1-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="881d1-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="881d1-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="881d1-125">Schema name</span></span>  <br/> |<span data-ttu-id="881d1-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="881d1-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="881d1-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="881d1-127">Validation file</span></span>  <br/> |<span data-ttu-id="881d1-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="881d1-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="881d1-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="881d1-129">Can be empty</span></span>  <br/> |<span data-ttu-id="881d1-130">False</span><span class="sxs-lookup"><span data-stu-id="881d1-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="881d1-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="881d1-131">See also</span></span>



- [<span data-ttu-id="881d1-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="881d1-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

