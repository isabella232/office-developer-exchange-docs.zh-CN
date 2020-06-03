---
title: IncludeUnsearchableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9a9bd2dc-f5b9-4b82-a6a0-f643d2951080
description: IncludeUnsearchableItems 元素指定是否包括无法搜索的项目。
ms.openlocfilehash: 19fe450f5b1647be2df75138dbe67dd9e1c05c21
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465700"
---
# <a name="includeunsearchableitems"></a><span data-ttu-id="f845c-103">IncludeUnsearchableItems</span><span class="sxs-lookup"><span data-stu-id="f845c-103">IncludeUnsearchableItems</span></span>

<span data-ttu-id="f845c-104">**IncludeUnsearchableItems**元素指定是否包括无法搜索的项目。</span><span class="sxs-lookup"><span data-stu-id="f845c-104">The **IncludeUnsearchableItems** element specifies whether to include items that cannot be searched.</span></span> 
  
```XML
<IncludeUnsearchableItems>true | false</IncludeUnsearchableItems>
```

 <span data-ttu-id="f845c-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f845c-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f845c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f845c-106">Attributes and elements</span></span>

<span data-ttu-id="f845c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f845c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f845c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f845c-108">Attributes</span></span>

<span data-ttu-id="f845c-109">无。</span><span class="sxs-lookup"><span data-stu-id="f845c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f845c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f845c-110">Child elements</span></span>

<span data-ttu-id="f845c-111">无。</span><span class="sxs-lookup"><span data-stu-id="f845c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f845c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f845c-112">Parent elements</span></span>

|<span data-ttu-id="f845c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f845c-113">**Element**</span></span>|<span data-ttu-id="f845c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="f845c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f845c-115">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="f845c-115">FindMailboxStatisticsByKeywords</span></span>](findmailboxstatisticsbykeywords.md) <br/> |<span data-ttu-id="f845c-116">指定按关键字搜索邮箱统计信息的请求。</span><span class="sxs-lookup"><span data-stu-id="f845c-116">Specifies a request to search for mailbox statistics by keyword.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f845c-117">文本值</span><span class="sxs-lookup"><span data-stu-id="f845c-117">Text value</span></span>

<span data-ttu-id="f845c-118">如果**IncludeUnsearchableItems**元素的文本值为**true** ，则表示不包含可搜索的项目的统计信息。</span><span class="sxs-lookup"><span data-stu-id="f845c-118">A text value of **true** for the **IncludeUnsearchableItems** element indicates that statistics are not included for items that are not searchable.</span></span> <span data-ttu-id="f845c-119">值为**false**表示对不可搜索的项目包含统计信息。</span><span class="sxs-lookup"><span data-stu-id="f845c-119">A value of **false** indicates that statistics are included for items that are not searchable.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f845c-120">备注</span><span class="sxs-lookup"><span data-stu-id="f845c-120">Remarks</span></span>

<span data-ttu-id="f845c-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f845c-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f845c-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f845c-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f845c-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="f845c-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f845c-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="f845c-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f845c-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="f845c-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f845c-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="f845c-126">Message schema</span></span>  <br/> |
|<span data-ttu-id="f845c-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="f845c-127">Validation File</span></span>  <br/> |<span data-ttu-id="f845c-128">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="f845c-128">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f845c-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="f845c-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f845c-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f845c-130">See also</span></span>



- [<span data-ttu-id="f845c-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f845c-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

