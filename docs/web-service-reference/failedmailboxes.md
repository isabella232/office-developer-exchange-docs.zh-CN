---
title: FailedMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f34fb6f6-057e-4ae3-8e10-bc92112eafba
description: FailedMailboxes 元素指定搜索失败的邮箱数组。
ms.openlocfilehash: 10f10d3f2ac4379d7ddcb3a13019d17a17bb676a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461952"
---
# <a name="failedmailboxes"></a><span data-ttu-id="5d2e6-103">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="5d2e6-103">FailedMailboxes</span></span>

<span data-ttu-id="5d2e6-104">**FailedMailboxes**元素指定搜索失败的邮箱数组。</span><span class="sxs-lookup"><span data-stu-id="5d2e6-104">The **FailedMailboxes** element specifies an array of mailboxes that failed on search.</span></span> 
  
```XML
<FailedMailboxes>
    <FailedMailbox/>
<FailedMailboxes>
```

 <span data-ttu-id="5d2e6-105">**ArrayOfFailedSearchMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="5d2e6-105">**ArrayOfFailedSearchMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5d2e6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5d2e6-106">Attributes and elements</span></span>

<span data-ttu-id="5d2e6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5d2e6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5d2e6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="5d2e6-108">Attributes</span></span>

<span data-ttu-id="5d2e6-109">无。</span><span class="sxs-lookup"><span data-stu-id="5d2e6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5d2e6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5d2e6-110">Child elements</span></span>

|<span data-ttu-id="5d2e6-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="5d2e6-111">**Element**</span></span>|<span data-ttu-id="5d2e6-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="5d2e6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d2e6-113">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="5d2e6-113">FailedMailbox</span></span>](failedmailbox.md) <br/> |<span data-ttu-id="5d2e6-114">为搜索失败的邮箱指定错误消息。</span><span class="sxs-lookup"><span data-stu-id="5d2e6-114">Specifies the error message for a mailbox that failed on search.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5d2e6-115">父元素</span><span class="sxs-lookup"><span data-stu-id="5d2e6-115">Parent elements</span></span>

|<span data-ttu-id="5d2e6-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="5d2e6-116">**Element**</span></span>|<span data-ttu-id="5d2e6-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="5d2e6-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d2e6-118">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="5d2e6-118">SearchMailboxesResult</span></span>](searchmailboxesresult.md) <br/> |<span data-ttu-id="5d2e6-119">包含**SearchMailboxes**请求的结果。</span><span class="sxs-lookup"><span data-stu-id="5d2e6-119">Contains the result of the **SearchMailboxes** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d2e6-120">备注</span><span class="sxs-lookup"><span data-stu-id="5d2e6-120">Remarks</span></span>

<span data-ttu-id="5d2e6-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5d2e6-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5d2e6-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5d2e6-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5d2e6-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="5d2e6-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d2e6-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="5d2e6-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5d2e6-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="5d2e6-125">Schema Name</span></span>  <br/> |<span data-ttu-id="5d2e6-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="5d2e6-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="5d2e6-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="5d2e6-127">Validation File</span></span>  <br/> |<span data-ttu-id="5d2e6-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="5d2e6-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="5d2e6-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="5d2e6-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="5d2e6-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5d2e6-130">See also</span></span>



- [<span data-ttu-id="5d2e6-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5d2e6-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

