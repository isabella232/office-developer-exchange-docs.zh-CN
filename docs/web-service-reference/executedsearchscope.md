---
title: ExecutedSearchScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExecutedSearchScope
api_type:
- schema
ms.assetid: 2de5f0ad-43f2-4d38-b520-06540066564e
description: ExecutedSearchScope 元素包含为获取搜索结果而执行的搜索的范围。
ms.openlocfilehash: 828fe3800b8c13a0e18c0daba6cdeab140a1c394
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456967"
---
# <a name="executedsearchscope"></a><span data-ttu-id="06d36-103">ExecutedSearchScope</span><span class="sxs-lookup"><span data-stu-id="06d36-103">ExecutedSearchScope</span></span>

<span data-ttu-id="06d36-104">**ExecutedSearchScope**元素包含为获取搜索结果而执行的搜索的范围。</span><span class="sxs-lookup"><span data-stu-id="06d36-104">The **ExecutedSearchScope** element contains the scope of the search that was performed to get the search results.</span></span> 
  
```xml
<ExecutedSearchScope/>
```

 <span data-ttu-id="06d36-105">**String**</span><span class="sxs-lookup"><span data-stu-id="06d36-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="06d36-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="06d36-106">Attributes and elements</span></span>

<span data-ttu-id="06d36-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="06d36-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06d36-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="06d36-108">Attributes</span></span>

<span data-ttu-id="06d36-109">无。</span><span class="sxs-lookup"><span data-stu-id="06d36-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="06d36-110">子元素</span><span class="sxs-lookup"><span data-stu-id="06d36-110">Child elements</span></span>

<span data-ttu-id="06d36-111">无。</span><span class="sxs-lookup"><span data-stu-id="06d36-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="06d36-112">父元素</span><span class="sxs-lookup"><span data-stu-id="06d36-112">Parent elements</span></span>

|<span data-ttu-id="06d36-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="06d36-113">**Element**</span></span>|<span data-ttu-id="06d36-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="06d36-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06d36-115">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="06d36-115">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="06d36-116">包含单个[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="06d36-116">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="06d36-117">文本值</span><span class="sxs-lookup"><span data-stu-id="06d36-117">Text value</span></span>

<span data-ttu-id="06d36-118">文本值是可选的。</span><span class="sxs-lookup"><span data-stu-id="06d36-118">The text value is optional.</span></span> <span data-ttu-id="06d36-119">客户端应用程序使用此信息来更有效地缓存结果。</span><span class="sxs-lookup"><span data-stu-id="06d36-119">This information is used by the client application to cache the results more effectively.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="06d36-120">备注</span><span class="sxs-lookup"><span data-stu-id="06d36-120">Remarks</span></span>

<span data-ttu-id="06d36-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="06d36-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="06d36-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="06d36-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06d36-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="06d36-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="06d36-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="06d36-124">Schema Name</span></span>  <br/> |<span data-ttu-id="06d36-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="06d36-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="06d36-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="06d36-126">Validation File</span></span>  <br/> |<span data-ttu-id="06d36-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="06d36-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="06d36-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="06d36-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="06d36-129">False</span><span class="sxs-lookup"><span data-stu-id="06d36-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="06d36-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="06d36-130">See also</span></span>



[<span data-ttu-id="06d36-131">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="06d36-131">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="06d36-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="06d36-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

