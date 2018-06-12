---
title: GetNonIndexableItemStatistics
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dd16d1fb-d82d-42e5-b64a-bc6c19c48fa8
description: GetNonIndexableItemStatistics 元素指定要检索 nonindexable 项目统计信息的请求。
ms.openlocfilehash: 4e6f9a0ba94e9946a3910661810bc2c9e748ba9f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754624"
---
# <a name="getnonindexableitemstatistics"></a><span data-ttu-id="a5660-103">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="a5660-103">GetNonIndexableItemStatistics</span></span>

<span data-ttu-id="a5660-104">**GetNonIndexableItemStatistics**元素指定要检索 nonindexable 项目统计信息的请求。</span><span class="sxs-lookup"><span data-stu-id="a5660-104">The **GetNonIndexableItemStatistics** element specifies a request to retrieve nonindexable item statistics.</span></span> 
  
```XML
<GetNonIndexableItemStatistics>
    <Mailboxes/>
</GetNonIndexableItemStatistics>
```

 <span data-ttu-id="a5660-105">**GetNonIndexableItemStatisticsType**</span><span class="sxs-lookup"><span data-stu-id="a5660-105">**GetNonIndexableItemStatisticsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a5660-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a5660-106">Attributes and elements</span></span>

<span data-ttu-id="a5660-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a5660-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a5660-108">属性</span><span class="sxs-lookup"><span data-stu-id="a5660-108">Attributes</span></span>

<span data-ttu-id="a5660-109">无。</span><span class="sxs-lookup"><span data-stu-id="a5660-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a5660-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a5660-110">Child elements</span></span>

|<span data-ttu-id="a5660-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a5660-111">**Element**</span></span>|<span data-ttu-id="a5660-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a5660-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a5660-113">邮箱 (NonEmptyArrayOfLegacyDNsType)</span><span class="sxs-lookup"><span data-stu-id="a5660-113">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md) <br/> |<span data-ttu-id="a5660-114">指定**邮箱**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="a5660-114">Specifies an array of **Mailbox** elements.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a5660-115">父元素</span><span class="sxs-lookup"><span data-stu-id="a5660-115">Parent elements</span></span>

<span data-ttu-id="a5660-116">无。</span><span class="sxs-lookup"><span data-stu-id="a5660-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a5660-117">备注</span><span class="sxs-lookup"><span data-stu-id="a5660-117">Remarks</span></span>

<span data-ttu-id="a5660-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a5660-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a5660-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a5660-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a5660-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="a5660-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a5660-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="a5660-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a5660-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="a5660-122">Schema Name</span></span>  <br/> |<span data-ttu-id="a5660-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="a5660-123">Message schema</span></span>  <br/> |
|<span data-ttu-id="a5660-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="a5660-124">Validation File</span></span>  <br/> |<span data-ttu-id="a5660-125">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a5660-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a5660-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="a5660-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="a5660-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a5660-127">See also</span></span>



- [<span data-ttu-id="a5660-128">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a5660-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

