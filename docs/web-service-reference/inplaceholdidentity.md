---
title: InPlaceHoldIdentity
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54f45774-00a0-4392-af1b-8c5f2208a53f
description: InPlaceHoldIdentity 元素指定保留邮箱项目的保留的标识。
ms.openlocfilehash: a06f72e478e7dc5bd1a499dceefeb352b14d7362
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466092"
---
# <a name="inplaceholdidentity"></a><span data-ttu-id="b1cf0-103">InPlaceHoldIdentity</span><span class="sxs-lookup"><span data-stu-id="b1cf0-103">InPlaceHoldIdentity</span></span>

<span data-ttu-id="b1cf0-104">**InPlaceHoldIdentity**元素指定保留邮箱项目的保留的标识。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-104">The **InPlaceHoldIdentity** element specifies the identity of a hold that preserves the mailbox items.</span></span> 
  
```XML
<InPlaceHoldIdentity></InPlaceHoldIdentity>
```

 <span data-ttu-id="b1cf0-105">**string**</span><span class="sxs-lookup"><span data-stu-id="b1cf0-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b1cf0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b1cf0-106">Attributes and elements</span></span>

<span data-ttu-id="b1cf0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1cf0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b1cf0-108">Attributes</span></span>

<span data-ttu-id="b1cf0-109">无。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b1cf0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b1cf0-110">Child elements</span></span>

<span data-ttu-id="b1cf0-111">无。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b1cf0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b1cf0-112">Parent elements</span></span>

<span data-ttu-id="b1cf0-113">[SetHoldOnMailboxes](setholdonmailboxes.md)  | [DiscoverySearchConfiguration](discoverysearchconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b1cf0-113">[SetHoldOnMailboxes](setholdonmailboxes.md) | [DiscoverySearchConfiguration](discoverysearchconfiguration.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="b1cf0-114">文本值</span><span class="sxs-lookup"><span data-stu-id="b1cf0-114">Text value</span></span>

<span data-ttu-id="b1cf0-115">**InPlaceHoldIdentity**元素的文本值是邮箱保留标识符。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-115">The text value of the **InPlaceHoldIdentity** element is the mailbox hold identifier.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b1cf0-116">备注</span><span class="sxs-lookup"><span data-stu-id="b1cf0-116">Remarks</span></span>

<span data-ttu-id="b1cf0-117">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b1cf0-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b1cf0-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="b1cf0-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1cf0-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="b1cf0-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b1cf0-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="b1cf0-121">Schema name</span></span>  <br/> |<span data-ttu-id="b1cf0-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="b1cf0-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b1cf0-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="b1cf0-123">Validation file</span></span>  <br/> |<span data-ttu-id="b1cf0-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b1cf0-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b1cf0-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="b1cf0-125">Can be empty</span></span>  <br/> |<span data-ttu-id="b1cf0-126">False</span><span class="sxs-lookup"><span data-stu-id="b1cf0-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b1cf0-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b1cf0-127">See also</span></span>



[<span data-ttu-id="b1cf0-128">SetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="b1cf0-128">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)


- [<span data-ttu-id="b1cf0-129">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b1cf0-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

