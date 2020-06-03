---
title: HasAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de152be6-fc2f-48bc-a05d-1211935da20a
description: HasAttachment 元素指定一个布尔值，以指示该项目是否具有附件。
ms.openlocfilehash: c6bc0932a08a1bbec215bb8a974ed746d2961123
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530259"
---
# <a name="hasattachment"></a><span data-ttu-id="13ce1-103">HasAttachment</span><span class="sxs-lookup"><span data-stu-id="13ce1-103">HasAttachment</span></span>

<span data-ttu-id="13ce1-104">**HasAttachment**元素指定一个布尔值，以指示该项目是否具有附件。</span><span class="sxs-lookup"><span data-stu-id="13ce1-104">The **HasAttachment** element specifies a Boolean value to indicate whether the item has attachments.</span></span> 
  
```XML
<HasAttachment> true | false </HasAttachment
```

 <span data-ttu-id="13ce1-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="13ce1-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="13ce1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="13ce1-106">Attributes and elements</span></span>

<span data-ttu-id="13ce1-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="13ce1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13ce1-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="13ce1-108">Attributes</span></span>

<span data-ttu-id="13ce1-109">无。</span><span class="sxs-lookup"><span data-stu-id="13ce1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="13ce1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="13ce1-110">Child elements</span></span>

<span data-ttu-id="13ce1-111">无。</span><span class="sxs-lookup"><span data-stu-id="13ce1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="13ce1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="13ce1-112">Parent elements</span></span>

|<span data-ttu-id="13ce1-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="13ce1-113">**Element**</span></span>|<span data-ttu-id="13ce1-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="13ce1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13ce1-115">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="13ce1-115">SearchPreviewItem</span></span>](searchpreviewitem.md) <br/> |<span data-ttu-id="13ce1-116">指定在不打开项目的情况下预览邮箱项目的前256个字符。</span><span class="sxs-lookup"><span data-stu-id="13ce1-116">Specifies the first 256 characters of a mailbox item for preview without opening the item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="13ce1-117">文本值</span><span class="sxs-lookup"><span data-stu-id="13ce1-117">Text value</span></span>

<span data-ttu-id="13ce1-118">如果**HasAttachment**元素的文本值为**true** ，则表示该项目具有附件。</span><span class="sxs-lookup"><span data-stu-id="13ce1-118">A text value of **true** for the **HasAttachment** element indicates that the item has an attachment.</span></span> <span data-ttu-id="13ce1-119">**如果值为 false** ，则表示该项目没有附件。</span><span class="sxs-lookup"><span data-stu-id="13ce1-119">A value of **false** indicates that the item does not have an attachment.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="13ce1-120">备注</span><span class="sxs-lookup"><span data-stu-id="13ce1-120">Remarks</span></span>

<span data-ttu-id="13ce1-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="13ce1-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="13ce1-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="13ce1-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="13ce1-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="13ce1-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13ce1-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="13ce1-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="13ce1-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="13ce1-125">Schema Name</span></span>  <br/> |<span data-ttu-id="13ce1-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="13ce1-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="13ce1-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="13ce1-127">Validation File</span></span>  <br/> |<span data-ttu-id="13ce1-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="13ce1-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="13ce1-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="13ce1-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="13ce1-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="13ce1-130">See also</span></span>



- [<span data-ttu-id="13ce1-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="13ce1-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

