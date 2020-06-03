---
title: PolicyTipsEnabled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16409652-21e4-4bd3-9373-67e1882236b4
description: PolicyTipsEnabled 元素指示是否启用策略提示。
ms.openlocfilehash: 26a527022d60dd4b98f70c2b3bf020b649066057
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468514"
---
# <a name="policytipsenabled"></a><span data-ttu-id="1593a-103">PolicyTipsEnabled</span><span class="sxs-lookup"><span data-stu-id="1593a-103">PolicyTipsEnabled</span></span>

<span data-ttu-id="1593a-104">**PolicyTipsEnabled**元素指示是否启用策略提示。</span><span class="sxs-lookup"><span data-stu-id="1593a-104">The **PolicyTipsEnabled** element indicates whether policy tips are enabled.</span></span> 
  
```XML
<PolicyTipsEnabled> true | false </PolicyTipsEnabled>
```

 <span data-ttu-id="1593a-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1593a-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1593a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1593a-106">Attributes and elements</span></span>

<span data-ttu-id="1593a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1593a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1593a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1593a-108">Attributes</span></span>

<span data-ttu-id="1593a-109">无。</span><span class="sxs-lookup"><span data-stu-id="1593a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1593a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1593a-110">Child elements</span></span>

<span data-ttu-id="1593a-111">无。</span><span class="sxs-lookup"><span data-stu-id="1593a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1593a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1593a-112">Parent elements</span></span>

[<span data-ttu-id="1593a-113">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="1593a-113">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md)
  
## <a name="text-value"></a><span data-ttu-id="1593a-114">文本值</span><span class="sxs-lookup"><span data-stu-id="1593a-114">Text value</span></span>

<span data-ttu-id="1593a-115">如果**PolicyTipsEnabled**元素的文本值为**true，则**表示为邮箱启用了策略提示。</span><span class="sxs-lookup"><span data-stu-id="1593a-115">A text value of **true** for the **PolicyTipsEnabled** element indicates that policy tips are enabled for a mailbox.</span></span> <span data-ttu-id="1593a-116">**如果值为 false** ，则表示没有为邮箱启用策略提示。</span><span class="sxs-lookup"><span data-stu-id="1593a-116">A value of **false** indicates that policy tips are not enabled for a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1593a-117">备注</span><span class="sxs-lookup"><span data-stu-id="1593a-117">Remarks</span></span>

<span data-ttu-id="1593a-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1593a-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1593a-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1593a-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1593a-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="1593a-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1593a-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="1593a-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1593a-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="1593a-122">Schema name</span></span>  <br/> |<span data-ttu-id="1593a-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="1593a-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="1593a-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="1593a-124">Validation file</span></span>  <br/> |<span data-ttu-id="1593a-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1593a-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1593a-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="1593a-126">Can be empty</span></span>  <br/> ||
   

