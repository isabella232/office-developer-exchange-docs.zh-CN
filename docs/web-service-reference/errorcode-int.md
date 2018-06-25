---
title: ErrorCode （整数）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 65537d96-edf9-41ee-9ad5-91ffe37e2269
description: ErrorCode 元素指定针对邮箱执行失败搜索的错误代码。
ms.openlocfilehash: ed8a7771376f921303ea093f4be727c4146faa76
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754145"
---
# <a name="errorcode-int"></a><span data-ttu-id="a5786-103">ErrorCode （整数）</span><span class="sxs-lookup"><span data-stu-id="a5786-103">ErrorCode (int)</span></span>

<span data-ttu-id="a5786-104">**ErrorCode**元素指定针对邮箱执行失败搜索的错误代码。</span><span class="sxs-lookup"><span data-stu-id="a5786-104">The **ErrorCode** element specifies the error code of a failed search performed against a mailbox.</span></span> 
  
```XML
<ErrorCode></ErrorCode>
```

 <span data-ttu-id="a5786-105">**int**</span><span class="sxs-lookup"><span data-stu-id="a5786-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a5786-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a5786-106">Attributes and elements</span></span>

<span data-ttu-id="a5786-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a5786-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a5786-108">属性</span><span class="sxs-lookup"><span data-stu-id="a5786-108">Attributes</span></span>

<span data-ttu-id="a5786-109">无。</span><span class="sxs-lookup"><span data-stu-id="a5786-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a5786-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a5786-110">Child elements</span></span>

<span data-ttu-id="a5786-111">无。</span><span class="sxs-lookup"><span data-stu-id="a5786-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a5786-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a5786-112">Parent elements</span></span>

|<span data-ttu-id="a5786-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a5786-113">**Element**</span></span>|<span data-ttu-id="a5786-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a5786-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a5786-115">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="a5786-115">FailedMailbox</span></span>](failedmailbox.md) <br/> |<span data-ttu-id="a5786-116">指定邮箱的保留状态。</span><span class="sxs-lookup"><span data-stu-id="a5786-116">Specifies the hold status of the mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a5786-117">文本值</span><span class="sxs-lookup"><span data-stu-id="a5786-117">Text value</span></span>

<span data-ttu-id="a5786-118">对于针对邮箱执行失败搜索返回的错误代码的**ErrorCode**元素的文本值。</span><span class="sxs-lookup"><span data-stu-id="a5786-118">The text value of the **ErrorCode** element is the error code returned for a failed search performed against a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a5786-119">备注</span><span class="sxs-lookup"><span data-stu-id="a5786-119">Remarks</span></span>

<span data-ttu-id="a5786-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a5786-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a5786-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a5786-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a5786-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="a5786-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a5786-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="a5786-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a5786-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="a5786-124">Schema Name</span></span>  <br/> |<span data-ttu-id="a5786-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="a5786-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="a5786-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="a5786-126">Validation File</span></span>  <br/> |<span data-ttu-id="a5786-127">types.xsd</span><span class="sxs-lookup"><span data-stu-id="a5786-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="a5786-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="a5786-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="a5786-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a5786-129">See also</span></span>



- [<span data-ttu-id="a5786-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a5786-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

