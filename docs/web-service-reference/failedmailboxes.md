---
title: FailedMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f34fb6f6-057e-4ae3-8e10-bc92112eafba
description: FailedMailboxes 元素指定的数组失败的邮箱搜索。
ms.openlocfilehash: f68cc29dc9da3b1b74369aa21cde65866e42f3b8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754289"
---
# <a name="failedmailboxes"></a><span data-ttu-id="4fb2e-103">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="4fb2e-103">FailedMailboxes</span></span>

<span data-ttu-id="4fb2e-104">**FailedMailboxes**元素指定的数组失败的邮箱搜索。</span><span class="sxs-lookup"><span data-stu-id="4fb2e-104">The **FailedMailboxes** element specifies an array of mailboxes that failed on search.</span></span> 
  
```XML
<FailedMailboxes>
    <FailedMailbox/>
<FailedMailboxes>
```

 <span data-ttu-id="4fb2e-105">**ArrayOfFailedSearchMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="4fb2e-105">**ArrayOfFailedSearchMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4fb2e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4fb2e-106">Attributes and elements</span></span>

<span data-ttu-id="4fb2e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4fb2e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4fb2e-108">属性</span><span class="sxs-lookup"><span data-stu-id="4fb2e-108">Attributes</span></span>

<span data-ttu-id="4fb2e-109">无。</span><span class="sxs-lookup"><span data-stu-id="4fb2e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4fb2e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4fb2e-110">Child elements</span></span>

|<span data-ttu-id="4fb2e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="4fb2e-111">**Element**</span></span>|<span data-ttu-id="4fb2e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="4fb2e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4fb2e-113">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="4fb2e-113">FailedMailbox</span></span>](failedmailbox.md) <br/> |<span data-ttu-id="4fb2e-114">在搜索指定邮箱的失败的错误消息。</span><span class="sxs-lookup"><span data-stu-id="4fb2e-114">Specifies the error message for a mailbox that failed on search.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4fb2e-115">父元素</span><span class="sxs-lookup"><span data-stu-id="4fb2e-115">Parent elements</span></span>

|<span data-ttu-id="4fb2e-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="4fb2e-116">**Element**</span></span>|<span data-ttu-id="4fb2e-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="4fb2e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4fb2e-118">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="4fb2e-118">SearchMailboxesResult</span></span>](searchmailboxesresult.md) <br/> |<span data-ttu-id="4fb2e-119">包含**SearchMailboxes**请求的结果。</span><span class="sxs-lookup"><span data-stu-id="4fb2e-119">Contains the result of the **SearchMailboxes** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4fb2e-120">备注</span><span class="sxs-lookup"><span data-stu-id="4fb2e-120">Remarks</span></span>

<span data-ttu-id="4fb2e-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4fb2e-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4fb2e-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4fb2e-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4fb2e-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="4fb2e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4fb2e-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="4fb2e-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4fb2e-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="4fb2e-125">Schema Name</span></span>  <br/> |<span data-ttu-id="4fb2e-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="4fb2e-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="4fb2e-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="4fb2e-127">Validation File</span></span>  <br/> |<span data-ttu-id="4fb2e-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="4fb2e-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="4fb2e-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="4fb2e-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="4fb2e-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4fb2e-130">See also</span></span>



- [<span data-ttu-id="4fb2e-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4fb2e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

