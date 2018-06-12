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
description: ExecutedSearchScope 元素包含执行从中获取搜索结果的搜索范围。
ms.openlocfilehash: ece9fdfc156cedad2a9fa181897145ae4eea20a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754193"
---
# <a name="executedsearchscope"></a><span data-ttu-id="a3a60-103">ExecutedSearchScope</span><span class="sxs-lookup"><span data-stu-id="a3a60-103">ExecutedSearchScope</span></span>

<span data-ttu-id="a3a60-104">**ExecutedSearchScope**元素包含执行从中获取搜索结果的搜索范围。</span><span class="sxs-lookup"><span data-stu-id="a3a60-104">The **ExecutedSearchScope** element contains the scope of the search that was performed to get the search results.</span></span> 
  
```xml
<ExecutedSearchScope/>
```

 <span data-ttu-id="a3a60-105">**字符串**</span><span class="sxs-lookup"><span data-stu-id="a3a60-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a3a60-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a3a60-106">Attributes and elements</span></span>

<span data-ttu-id="a3a60-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a3a60-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3a60-108">属性</span><span class="sxs-lookup"><span data-stu-id="a3a60-108">Attributes</span></span>

<span data-ttu-id="a3a60-109">无。</span><span class="sxs-lookup"><span data-stu-id="a3a60-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a3a60-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a3a60-110">Child elements</span></span>

<span data-ttu-id="a3a60-111">无。</span><span class="sxs-lookup"><span data-stu-id="a3a60-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a3a60-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a3a60-112">Parent elements</span></span>

|<span data-ttu-id="a3a60-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a3a60-113">**Element**</span></span>|<span data-ttu-id="a3a60-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a3a60-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3a60-115">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="a3a60-115">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="a3a60-116">包含状态和的单个结果[FindMessageTrackingReport 操作](findmessagetrackingreport-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="a3a60-116">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a3a60-117">文本值</span><span class="sxs-lookup"><span data-stu-id="a3a60-117">Text value</span></span>

<span data-ttu-id="a3a60-118">文本值是可选的。</span><span class="sxs-lookup"><span data-stu-id="a3a60-118">The text value is optional.</span></span> <span data-ttu-id="a3a60-119">客户端应用程序使用此信息来更有效地缓存结果。</span><span class="sxs-lookup"><span data-stu-id="a3a60-119">This information is used by the client application to cache the results more effectively.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a3a60-120">备注</span><span class="sxs-lookup"><span data-stu-id="a3a60-120">Remarks</span></span>

<span data-ttu-id="a3a60-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a3a60-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a3a60-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="a3a60-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3a60-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="a3a60-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a3a60-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="a3a60-124">Schema Name</span></span>  <br/> |<span data-ttu-id="a3a60-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="a3a60-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="a3a60-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="a3a60-126">Validation File</span></span>  <br/> |<span data-ttu-id="a3a60-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a3a60-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a3a60-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="a3a60-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="a3a60-129">False</span><span class="sxs-lookup"><span data-stu-id="a3a60-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a3a60-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a3a60-130">See also</span></span>



[<span data-ttu-id="a3a60-131">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="a3a60-131">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="a3a60-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a3a60-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

