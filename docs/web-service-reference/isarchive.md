---
title: IsArchive
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b89d8a78-5c18-4547-aaf4-4b16a93190a7
description: IsArchive 元素指定一个布尔值，该值指示邮箱是否存档邮箱。
ms.openlocfilehash: 417afd1afc25e5872d1f511feff34494fe6b7b62
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825990"
---
# <a name="isarchive"></a><span data-ttu-id="35a2d-103">IsArchive</span><span class="sxs-lookup"><span data-stu-id="35a2d-103">IsArchive</span></span>

<span data-ttu-id="35a2d-104">**IsArchive**元素指定一个布尔值，该值指示邮箱是否存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="35a2d-104">The **IsArchive** element specifies a Boolean value that indicates whether the mailbox is an archive mailbox.</span></span> 
  
```XML
<IsArchive>true | false</IsArchive>
```

 <span data-ttu-id="35a2d-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="35a2d-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="35a2d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="35a2d-106">Attributes and elements</span></span>

<span data-ttu-id="35a2d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="35a2d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="35a2d-108">属性</span><span class="sxs-lookup"><span data-stu-id="35a2d-108">Attributes</span></span>

<span data-ttu-id="35a2d-109">无。</span><span class="sxs-lookup"><span data-stu-id="35a2d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="35a2d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="35a2d-110">Child elements</span></span>

<span data-ttu-id="35a2d-111">无。</span><span class="sxs-lookup"><span data-stu-id="35a2d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="35a2d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="35a2d-112">Parent elements</span></span>

<span data-ttu-id="35a2d-113">[FailedMailbox](failedmailbox.md) | [RetentionPolicyTag](retentionpolicytag.md)</span><span class="sxs-lookup"><span data-stu-id="35a2d-113">[FailedMailbox](failedmailbox.md) | [RetentionPolicyTag](retentionpolicytag.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="35a2d-114">文本值</span><span class="sxs-lookup"><span data-stu-id="35a2d-114">Text value</span></span>

<span data-ttu-id="35a2d-115">文本值为**true**的**IsArchive**元素指示目标邮箱的存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="35a2d-115">A text value of **true** for the **IsArchive** element indicates that the target mailbox is an archive mailbox.</span></span> <span data-ttu-id="35a2d-116">如果值为**false**指示目标邮箱不是存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="35a2d-116">A value of **false** indicates that the target mailbox is not an archive mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="35a2d-117">备注</span><span class="sxs-lookup"><span data-stu-id="35a2d-117">Remarks</span></span>

<span data-ttu-id="35a2d-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="35a2d-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="35a2d-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="35a2d-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="35a2d-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="35a2d-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35a2d-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="35a2d-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="35a2d-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="35a2d-122">Schema Name</span></span>  <br/> |<span data-ttu-id="35a2d-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="35a2d-123">Type schema</span></span>  <br/> |
|<span data-ttu-id="35a2d-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="35a2d-124">Validation File</span></span>  <br/> |<span data-ttu-id="35a2d-125">types.xsd</span><span class="sxs-lookup"><span data-stu-id="35a2d-125">types.xsd</span></span>  <br/> |
|<span data-ttu-id="35a2d-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="35a2d-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="35a2d-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="35a2d-127">See also</span></span>



- [<span data-ttu-id="35a2d-128">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="35a2d-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

