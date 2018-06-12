---
title: ItemHoldPeriod
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 30369db5-4d45-40e8-bc83-3236667fc404
description: ItemHoldPeriod 元素指定的时间来保存与邮箱查询匹配的内容量。
ms.openlocfilehash: 212d765aa3f0493dd4f3051de483fa08a6fa8ac7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826144"
---
# <a name="itemholdperiod"></a><span data-ttu-id="9fd51-103">ItemHoldPeriod</span><span class="sxs-lookup"><span data-stu-id="9fd51-103">ItemHoldPeriod</span></span>

<span data-ttu-id="9fd51-104">**ItemHoldPeriod**元素指定的时间来保存与邮箱查询匹配的内容量。</span><span class="sxs-lookup"><span data-stu-id="9fd51-104">The **ItemHoldPeriod** element specifies the amount of time to hold content that matches the mailbox query.</span></span> 
  
```XML
<ItemHoldPeriod/>
```

 <span data-ttu-id="9fd51-105">**string**</span><span class="sxs-lookup"><span data-stu-id="9fd51-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9fd51-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9fd51-106">Attributes and elements</span></span>

<span data-ttu-id="9fd51-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9fd51-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9fd51-108">属性</span><span class="sxs-lookup"><span data-stu-id="9fd51-108">Attributes</span></span>

<span data-ttu-id="9fd51-109">无。</span><span class="sxs-lookup"><span data-stu-id="9fd51-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9fd51-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9fd51-110">Child elements</span></span>

<span data-ttu-id="9fd51-111">无。</span><span class="sxs-lookup"><span data-stu-id="9fd51-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9fd51-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9fd51-112">Parent elements</span></span>

[<span data-ttu-id="9fd51-113">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="9fd51-113">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="9fd51-114">文本值</span><span class="sxs-lookup"><span data-stu-id="9fd51-114">Text value</span></span>

<span data-ttu-id="9fd51-115">文本值可以是"Unlimited"或任何[Timespan](http://msdn.microsoft.com/en-us/library/1ecy8h51%28v=vs.110%29.aspx)值的字符串值。</span><span class="sxs-lookup"><span data-stu-id="9fd51-115">The text value can be "Unlimited" or the string value of any [Timespan](http://msdn.microsoft.com/en-us/library/1ecy8h51%28v=vs.110%29.aspx) value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9fd51-116">备注</span><span class="sxs-lookup"><span data-stu-id="9fd51-116">Remarks</span></span>

<span data-ttu-id="9fd51-117">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9fd51-117">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="9fd51-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9fd51-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9fd51-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="9fd51-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fd51-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="9fd51-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9fd51-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="9fd51-121">Schema Name</span></span>  <br/> |<span data-ttu-id="9fd51-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="9fd51-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9fd51-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="9fd51-123">Validation File</span></span>  <br/> |<span data-ttu-id="9fd51-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9fd51-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9fd51-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="9fd51-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="9fd51-126">True</span><span class="sxs-lookup"><span data-stu-id="9fd51-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9fd51-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9fd51-127">See also</span></span>



[<span data-ttu-id="9fd51-128">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="9fd51-128">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)


- [<span data-ttu-id="9fd51-129">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9fd51-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

