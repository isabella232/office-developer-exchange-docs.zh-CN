---
title: IncludePersonalArchive
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b373bb1a-6b1d-4959-98a1-4c4ea62973bc
description: IncludePersonalArchive 元素指定是否在搜索中包含个人存档。
ms.openlocfilehash: a25dd45bc0717af8f949d14b88793af3821ca69f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458248"
---
# <a name="includepersonalarchive"></a><span data-ttu-id="b7f82-103">IncludePersonalArchive</span><span class="sxs-lookup"><span data-stu-id="b7f82-103">IncludePersonalArchive</span></span>

<span data-ttu-id="b7f82-104">**IncludePersonalArchive**元素指定是否在搜索中包含个人存档。</span><span class="sxs-lookup"><span data-stu-id="b7f82-104">The **IncludePersonalArchive** element specifies whether to include the personal archive in the search.</span></span> 
  
```XML
<IncludePersonalArchive>true | false</IncludePersonalArchive>
```

 <span data-ttu-id="b7f82-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b7f82-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b7f82-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b7f82-106">Attributes and elements</span></span>

<span data-ttu-id="b7f82-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b7f82-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7f82-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b7f82-108">Attributes</span></span>

<span data-ttu-id="b7f82-109">无。</span><span class="sxs-lookup"><span data-stu-id="b7f82-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b7f82-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b7f82-110">Child elements</span></span>

<span data-ttu-id="b7f82-111">无。</span><span class="sxs-lookup"><span data-stu-id="b7f82-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b7f82-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b7f82-112">Parent elements</span></span>

|<span data-ttu-id="b7f82-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="b7f82-113">**Element**</span></span>|<span data-ttu-id="b7f82-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="b7f82-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7f82-115">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="b7f82-115">FindMailboxStatisticsByKeywords</span></span>](findmailboxstatisticsbykeywords.md) <br/> |<span data-ttu-id="b7f82-116">指定按关键字搜索邮箱统计信息的请求。</span><span class="sxs-lookup"><span data-stu-id="b7f82-116">Specifies a request to search for mailbox statistics by keyword.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b7f82-117">文本值</span><span class="sxs-lookup"><span data-stu-id="b7f82-117">Text value</span></span>

<span data-ttu-id="b7f82-118">如果**IncludePersonalArchive**元素的文本值为**true** ，则表示该个人存档包含在搜索中。</span><span class="sxs-lookup"><span data-stu-id="b7f82-118">A text value of **true** for the **IncludePersonalArchive** element indicates that the personal archive is included in the search.</span></span> <span data-ttu-id="b7f82-119">**如果值为 false** ，则表示个人存档不包含在搜索中。</span><span class="sxs-lookup"><span data-stu-id="b7f82-119">A value of **false** indicates that the personal archive is not included in the search.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b7f82-120">说明</span><span class="sxs-lookup"><span data-stu-id="b7f82-120">Remarks</span></span>

<span data-ttu-id="b7f82-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b7f82-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7f82-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="b7f82-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7f82-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="b7f82-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b7f82-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="b7f82-124">Schema Name</span></span>  <br/> |<span data-ttu-id="b7f82-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="b7f82-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="b7f82-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="b7f82-126">Validation File</span></span>  <br/> |<span data-ttu-id="b7f82-127">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="b7f82-127">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b7f82-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="b7f82-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="b7f82-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b7f82-129">See also</span></span>



- [<span data-ttu-id="b7f82-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b7f82-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

