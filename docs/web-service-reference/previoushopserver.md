---
title: PreviousHopServer
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PreviousHopServer
api_type:
- schema
ms.assetid: 74456709-1250-4943-bae0-11a3db44a684
description: PreviousHopServer 元素表示接受邮件的以前的服务器名称。
ms.openlocfilehash: f85896107c720179d76e0cbeb31588e17c1f3d95
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528877"
---
# <a name="previoushopserver"></a><span data-ttu-id="c6e66-103">PreviousHopServer</span><span class="sxs-lookup"><span data-stu-id="c6e66-103">PreviousHopServer</span></span>

<span data-ttu-id="c6e66-104">**PreviousHopServer**元素表示接受邮件的以前的服务器名称。</span><span class="sxs-lookup"><span data-stu-id="c6e66-104">The **PreviousHopServer** element represents the previous server name that accepted the message.</span></span> 
  
```XML
<PreviousHopServer/>
```

 <span data-ttu-id="c6e66-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="c6e66-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c6e66-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c6e66-106">Attributes and elements</span></span>

<span data-ttu-id="c6e66-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c6e66-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6e66-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c6e66-108">Attributes</span></span>

<span data-ttu-id="c6e66-109">无。</span><span class="sxs-lookup"><span data-stu-id="c6e66-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c6e66-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c6e66-110">Child elements</span></span>

<span data-ttu-id="c6e66-111">无。</span><span class="sxs-lookup"><span data-stu-id="c6e66-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c6e66-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c6e66-112">Parent elements</span></span>

|<span data-ttu-id="c6e66-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c6e66-113">**Element**</span></span>|<span data-ttu-id="c6e66-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c6e66-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6e66-115">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="c6e66-115">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="c6e66-116">包含[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素的单个邮件结果。</span><span class="sxs-lookup"><span data-stu-id="c6e66-116">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c6e66-117">文本值</span><span class="sxs-lookup"><span data-stu-id="c6e66-117">Text value</span></span>

<span data-ttu-id="c6e66-118">如果使用此元素，则需要一个表示字符串的文本值。</span><span class="sxs-lookup"><span data-stu-id="c6e66-118">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c6e66-119">说明</span><span class="sxs-lookup"><span data-stu-id="c6e66-119">Remarks</span></span>

<span data-ttu-id="c6e66-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c6e66-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c6e66-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="c6e66-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6e66-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="c6e66-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c6e66-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="c6e66-123">Schema Name</span></span>  <br/> |<span data-ttu-id="c6e66-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="c6e66-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="c6e66-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="c6e66-125">Validation File</span></span>  <br/> |<span data-ttu-id="c6e66-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c6e66-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c6e66-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="c6e66-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="c6e66-128">False</span><span class="sxs-lookup"><span data-stu-id="c6e66-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c6e66-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c6e66-129">See also</span></span>



- [<span data-ttu-id="c6e66-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c6e66-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

