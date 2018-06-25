---
title: IncludeUnsearchableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9a9bd2dc-f5b9-4b82-a6a0-f643d2951080
description: IncludeUnsearchableItems 元素指定是否包含无法搜索的项目。
ms.openlocfilehash: 4c6b9b3752330bf914c9901d2e8f69e93546fec6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825907"
---
# <a name="includeunsearchableitems"></a><span data-ttu-id="1a65b-103">IncludeUnsearchableItems</span><span class="sxs-lookup"><span data-stu-id="1a65b-103">IncludeUnsearchableItems</span></span>

<span data-ttu-id="1a65b-104">**IncludeUnsearchableItems**元素指定是否包含无法搜索的项目。</span><span class="sxs-lookup"><span data-stu-id="1a65b-104">The **IncludeUnsearchableItems** element specifies whether to include items that cannot be searched.</span></span> 
  
```XML
<IncludeUnsearchableItems>true | false</IncludeUnsearchableItems>
```

 <span data-ttu-id="1a65b-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1a65b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1a65b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1a65b-106">Attributes and elements</span></span>

<span data-ttu-id="1a65b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1a65b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1a65b-108">属性</span><span class="sxs-lookup"><span data-stu-id="1a65b-108">Attributes</span></span>

<span data-ttu-id="1a65b-109">无。</span><span class="sxs-lookup"><span data-stu-id="1a65b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1a65b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1a65b-110">Child elements</span></span>

<span data-ttu-id="1a65b-111">无。</span><span class="sxs-lookup"><span data-stu-id="1a65b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1a65b-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1a65b-112">Parent elements</span></span>

|<span data-ttu-id="1a65b-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="1a65b-113">**Element**</span></span>|<span data-ttu-id="1a65b-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="1a65b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1a65b-115">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="1a65b-115">FindMailboxStatisticsByKeywords</span></span>](findmailboxstatisticsbykeywords.md) <br/> |<span data-ttu-id="1a65b-116">指定按关键字搜索的邮箱统计信息的请求。</span><span class="sxs-lookup"><span data-stu-id="1a65b-116">Specifies a request to search for mailbox statistics by keyword.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1a65b-117">文本值</span><span class="sxs-lookup"><span data-stu-id="1a65b-117">Text value</span></span>

<span data-ttu-id="1a65b-118">文本值为**true**的**IncludeUnsearchableItems**元素指示统计信息不包括不可搜索的项目。</span><span class="sxs-lookup"><span data-stu-id="1a65b-118">A text value of **true** for the **IncludeUnsearchableItems** element indicates that statistics are not included for items that are not searchable.</span></span> <span data-ttu-id="1a65b-119">如果值为**false**指示统计信息已包含的是不可搜索的项目。</span><span class="sxs-lookup"><span data-stu-id="1a65b-119">A value of **false** indicates that statistics are included for items that are not searchable.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1a65b-120">备注</span><span class="sxs-lookup"><span data-stu-id="1a65b-120">Remarks</span></span>

<span data-ttu-id="1a65b-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1a65b-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1a65b-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1a65b-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1a65b-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="1a65b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a65b-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="1a65b-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1a65b-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="1a65b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="1a65b-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="1a65b-126">Message schema</span></span>  <br/> |
|<span data-ttu-id="1a65b-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="1a65b-127">Validation File</span></span>  <br/> |<span data-ttu-id="1a65b-128">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1a65b-128">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1a65b-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="1a65b-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="1a65b-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1a65b-130">See also</span></span>



- [<span data-ttu-id="1a65b-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1a65b-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

