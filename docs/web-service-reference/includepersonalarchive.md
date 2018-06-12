---
title: IncludePersonalArchive
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b373bb1a-6b1d-4959-98a1-4c4ea62973bc
description: IncludePersonalArchive 元素指定是否在搜索中包括个人存档。
ms.openlocfilehash: ba2dcaae3befd3595815c7281858e4fa8a738e0a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825905"
---
# <a name="includepersonalarchive"></a><span data-ttu-id="8dee4-103">IncludePersonalArchive</span><span class="sxs-lookup"><span data-stu-id="8dee4-103">IncludePersonalArchive</span></span>

<span data-ttu-id="8dee4-104">**IncludePersonalArchive**元素指定是否在搜索中包括个人存档。</span><span class="sxs-lookup"><span data-stu-id="8dee4-104">The **IncludePersonalArchive** element specifies whether to include the personal archive in the search.</span></span> 
  
```XML
<IncludePersonalArchive>true | false</IncludePersonalArchive>
```

 <span data-ttu-id="8dee4-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="8dee4-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8dee4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8dee4-106">Attributes and elements</span></span>

<span data-ttu-id="8dee4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8dee4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8dee4-108">属性</span><span class="sxs-lookup"><span data-stu-id="8dee4-108">Attributes</span></span>

<span data-ttu-id="8dee4-109">无。</span><span class="sxs-lookup"><span data-stu-id="8dee4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8dee4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8dee4-110">Child elements</span></span>

<span data-ttu-id="8dee4-111">无。</span><span class="sxs-lookup"><span data-stu-id="8dee4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8dee4-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8dee4-112">Parent elements</span></span>

|<span data-ttu-id="8dee4-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="8dee4-113">**Element**</span></span>|<span data-ttu-id="8dee4-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="8dee4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8dee4-115">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="8dee4-115">FindMailboxStatisticsByKeywords</span></span>](findmailboxstatisticsbykeywords.md) <br/> |<span data-ttu-id="8dee4-116">指定按关键字搜索的邮箱统计信息的请求。</span><span class="sxs-lookup"><span data-stu-id="8dee4-116">Specifies a request to search for mailbox statistics by keyword.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8dee4-117">文本值</span><span class="sxs-lookup"><span data-stu-id="8dee4-117">Text value</span></span>

<span data-ttu-id="8dee4-118">文本值为**true**的**IncludePersonalArchive**元素表示包含在搜索中，必须个人存档。</span><span class="sxs-lookup"><span data-stu-id="8dee4-118">A text value of **true** for the **IncludePersonalArchive** element indicates that the personal archive is included in the search.</span></span> <span data-ttu-id="8dee4-119">如果值为**false**指示个人存档不包括在搜索。</span><span class="sxs-lookup"><span data-stu-id="8dee4-119">A value of **false** indicates that the personal archive is not included in the search.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8dee4-120">备注</span><span class="sxs-lookup"><span data-stu-id="8dee4-120">Remarks</span></span>

<span data-ttu-id="8dee4-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8dee4-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8dee4-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="8dee4-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8dee4-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="8dee4-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8dee4-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="8dee4-124">Schema Name</span></span>  <br/> |<span data-ttu-id="8dee4-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="8dee4-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="8dee4-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="8dee4-126">Validation File</span></span>  <br/> |<span data-ttu-id="8dee4-127">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8dee4-127">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8dee4-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="8dee4-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="8dee4-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8dee4-129">See also</span></span>



- [<span data-ttu-id="8dee4-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8dee4-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

