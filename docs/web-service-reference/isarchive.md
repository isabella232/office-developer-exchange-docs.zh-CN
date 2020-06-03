---
title: IsArchive
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b89d8a78-5c18-4547-aaf4-4b16a93190a7
description: IsArchive 元素指定一个布尔值，该值指示邮箱是否为存档邮箱。
ms.openlocfilehash: 6d0be0eb283de3f4d8f786ff96f4a0d4f49e2009
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526513"
---
# <a name="isarchive"></a><span data-ttu-id="ba717-103">IsArchive</span><span class="sxs-lookup"><span data-stu-id="ba717-103">IsArchive</span></span>

<span data-ttu-id="ba717-104">**IsArchive**元素指定一个布尔值，该值指示邮箱是否为存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="ba717-104">The **IsArchive** element specifies a Boolean value that indicates whether the mailbox is an archive mailbox.</span></span> 
  
```XML
<IsArchive>true | false</IsArchive>
```

 <span data-ttu-id="ba717-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ba717-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba717-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ba717-106">Attributes and elements</span></span>

<span data-ttu-id="ba717-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ba717-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba717-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ba717-108">Attributes</span></span>

<span data-ttu-id="ba717-109">无。</span><span class="sxs-lookup"><span data-stu-id="ba717-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba717-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ba717-110">Child elements</span></span>

<span data-ttu-id="ba717-111">无。</span><span class="sxs-lookup"><span data-stu-id="ba717-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ba717-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ba717-112">Parent elements</span></span>

<span data-ttu-id="ba717-113">[FailedMailbox](failedmailbox.md)  | [Get-retentionpolicytag](retentionpolicytag.md)</span><span class="sxs-lookup"><span data-stu-id="ba717-113">[FailedMailbox](failedmailbox.md) | [RetentionPolicyTag](retentionpolicytag.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="ba717-114">文本值</span><span class="sxs-lookup"><span data-stu-id="ba717-114">Text value</span></span>

<span data-ttu-id="ba717-115">如果**IsArchive**元素的文本值为**true** ，则表示目标邮箱是存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="ba717-115">A text value of **true** for the **IsArchive** element indicates that the target mailbox is an archive mailbox.</span></span> <span data-ttu-id="ba717-116">**如果值为 false** ，则表示目标邮箱不是存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="ba717-116">A value of **false** indicates that the target mailbox is not an archive mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ba717-117">备注</span><span class="sxs-lookup"><span data-stu-id="ba717-117">Remarks</span></span>

<span data-ttu-id="ba717-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ba717-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ba717-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ba717-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba717-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="ba717-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba717-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="ba717-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ba717-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="ba717-122">Schema Name</span></span>  <br/> |<span data-ttu-id="ba717-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="ba717-123">Type schema</span></span>  <br/> |
|<span data-ttu-id="ba717-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="ba717-124">Validation File</span></span>  <br/> |<span data-ttu-id="ba717-125">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="ba717-125">types.xsd</span></span>  <br/> |
|<span data-ttu-id="ba717-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="ba717-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ba717-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ba717-127">See also</span></span>



- [<span data-ttu-id="ba717-128">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ba717-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

