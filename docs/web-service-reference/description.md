---
title: 说明
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6e4cd194-0696-4fec-8ab0-e1d349ed0be0
description: Description 元素指定保留策略的描述性文本。
ms.openlocfilehash: e001733e7011610dc09c2cce389104d74894772d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753846"
---
# <a name="description"></a><span data-ttu-id="0c347-103">说明</span><span class="sxs-lookup"><span data-stu-id="0c347-103">Description</span></span>

<span data-ttu-id="0c347-104">**Description**元素指定保留策略的描述性文本。</span><span class="sxs-lookup"><span data-stu-id="0c347-104">The **Description** element specifies the descriptive text for the retention policy.</span></span> 
  
```XML
<Description></Description>
```

 <span data-ttu-id="0c347-105">**string**</span><span class="sxs-lookup"><span data-stu-id="0c347-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0c347-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0c347-106">Attributes and elements</span></span>

<span data-ttu-id="0c347-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0c347-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c347-108">属性</span><span class="sxs-lookup"><span data-stu-id="0c347-108">Attributes</span></span>

<span data-ttu-id="0c347-109">无。</span><span class="sxs-lookup"><span data-stu-id="0c347-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0c347-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0c347-110">Child elements</span></span>

<span data-ttu-id="0c347-111">无。</span><span class="sxs-lookup"><span data-stu-id="0c347-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0c347-112">父元素</span><span class="sxs-lookup"><span data-stu-id="0c347-112">Parent elements</span></span>

|<span data-ttu-id="0c347-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="0c347-113">**Element**</span></span>|<span data-ttu-id="0c347-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="0c347-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0c347-115">RetentionPolicyTag</span><span class="sxs-lookup"><span data-stu-id="0c347-115">RetentionPolicyTag</span></span>](retentionpolicytag.md) <br/> |<span data-ttu-id="0c347-116">指定的邮箱项目的保留策略。</span><span class="sxs-lookup"><span data-stu-id="0c347-116">Specifies the retention policy for a mailbox item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0c347-117">文本值</span><span class="sxs-lookup"><span data-stu-id="0c347-117">Text value</span></span>

<span data-ttu-id="0c347-118">**Description**元素的文本值是一个 string 值，介绍了保留策略。</span><span class="sxs-lookup"><span data-stu-id="0c347-118">The text value of the **Description** element is a string value that describes the retention policy.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0c347-119">备注</span><span class="sxs-lookup"><span data-stu-id="0c347-119">Remarks</span></span>

<span data-ttu-id="0c347-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0c347-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0c347-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0c347-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0c347-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="0c347-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c347-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="0c347-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0c347-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="0c347-124">Schema Name</span></span>  <br/> |<span data-ttu-id="0c347-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="0c347-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="0c347-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="0c347-126">Validation File</span></span>  <br/> |<span data-ttu-id="0c347-127">types.xsd</span><span class="sxs-lookup"><span data-stu-id="0c347-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="0c347-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="0c347-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0c347-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0c347-129">See also</span></span>

- [<span data-ttu-id="0c347-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0c347-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

