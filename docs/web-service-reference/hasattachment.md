---
title: HasAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de152be6-fc2f-48bc-a05d-1211935da20a
description: HasAttachment 元素指定布尔值，该值指示项目是否有附件。
ms.openlocfilehash: dfe163e0850e835784a43984a34c89f14bfbc59b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825798"
---
# <a name="hasattachment"></a><span data-ttu-id="0f18b-103">HasAttachment</span><span class="sxs-lookup"><span data-stu-id="0f18b-103">HasAttachment</span></span>

<span data-ttu-id="0f18b-104">**HasAttachment**元素指定布尔值，该值指示项目是否有附件。</span><span class="sxs-lookup"><span data-stu-id="0f18b-104">The **HasAttachment** element specifies a Boolean value to indicate whether the item has attachments.</span></span> 
  
```XML
<HasAttachment> true | false </HasAttachment
```

 <span data-ttu-id="0f18b-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0f18b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0f18b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0f18b-106">Attributes and elements</span></span>

<span data-ttu-id="0f18b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0f18b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0f18b-108">属性</span><span class="sxs-lookup"><span data-stu-id="0f18b-108">Attributes</span></span>

<span data-ttu-id="0f18b-109">无。</span><span class="sxs-lookup"><span data-stu-id="0f18b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0f18b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0f18b-110">Child elements</span></span>

<span data-ttu-id="0f18b-111">无。</span><span class="sxs-lookup"><span data-stu-id="0f18b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0f18b-112">父元素</span><span class="sxs-lookup"><span data-stu-id="0f18b-112">Parent elements</span></span>

|<span data-ttu-id="0f18b-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="0f18b-113">**Element**</span></span>|<span data-ttu-id="0f18b-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="0f18b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0f18b-115">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="0f18b-115">SearchPreviewItem</span></span>](searchpreviewitem.md) <br/> |<span data-ttu-id="0f18b-116">指定预览邮箱项目的前 256 个字符，而无需打开项目。</span><span class="sxs-lookup"><span data-stu-id="0f18b-116">Specifies the first 256 characters of a mailbox item for preview without opening the item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0f18b-117">文本值</span><span class="sxs-lookup"><span data-stu-id="0f18b-117">Text value</span></span>

<span data-ttu-id="0f18b-118">文本值为**true**的**HasAttachment**元素指示项目包含附件。</span><span class="sxs-lookup"><span data-stu-id="0f18b-118">A text value of **true** for the **HasAttachment** element indicates that the item has an attachment.</span></span> <span data-ttu-id="0f18b-119">如果值为**false**指示项目没有附件。</span><span class="sxs-lookup"><span data-stu-id="0f18b-119">A value of **false** indicates that the item does not have an attachment.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0f18b-120">备注</span><span class="sxs-lookup"><span data-stu-id="0f18b-120">Remarks</span></span>

<span data-ttu-id="0f18b-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0f18b-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0f18b-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0f18b-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0f18b-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="0f18b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0f18b-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="0f18b-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0f18b-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="0f18b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="0f18b-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="0f18b-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="0f18b-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="0f18b-127">Validation File</span></span>  <br/> |<span data-ttu-id="0f18b-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="0f18b-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="0f18b-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="0f18b-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0f18b-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0f18b-130">See also</span></span>



- [<span data-ttu-id="0f18b-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0f18b-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

