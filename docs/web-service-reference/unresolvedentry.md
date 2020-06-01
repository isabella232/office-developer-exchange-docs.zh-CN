---
title: UnresolvedEntry
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnresolvedEntry
api_type:
- schema
ms.assetid: 5ac6116a-3b24-40f8-a877-dbe9a6935919
description: UnresolvedEntry 元素包含要解析的联系人或通讯组列表的名称。
ms.openlocfilehash: 0f157c1be6c327187456a795c4c1000b8c35b620
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459838"
---
# <a name="unresolvedentry"></a><span data-ttu-id="203e7-103">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="203e7-103">UnresolvedEntry</span></span>

<span data-ttu-id="203e7-104">**UnresolvedEntry**元素包含要解析的联系人或通讯组列表的名称。</span><span class="sxs-lookup"><span data-stu-id="203e7-104">The **UnresolvedEntry** element contains the name of a contact or distribution list to resolve.</span></span> 
  
[<span data-ttu-id="203e7-105">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="203e7-105">ResolveNames</span></span>](resolvenames.md)
  
[<span data-ttu-id="203e7-106">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="203e7-106">UnresolvedEntry</span></span>](unresolvedentry.md)
  
```xml
<UnresolvedEntry/>
```

 <span data-ttu-id="203e7-107">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="203e7-107">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="203e7-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="203e7-108">Attributes and elements</span></span>

<span data-ttu-id="203e7-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="203e7-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="203e7-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="203e7-110">Attributes</span></span>

<span data-ttu-id="203e7-111">无。</span><span class="sxs-lookup"><span data-stu-id="203e7-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="203e7-112">子元素</span><span class="sxs-lookup"><span data-stu-id="203e7-112">Child elements</span></span>

<span data-ttu-id="203e7-113">无。</span><span class="sxs-lookup"><span data-stu-id="203e7-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="203e7-114">父元素</span><span class="sxs-lookup"><span data-stu-id="203e7-114">Parent elements</span></span>

|<span data-ttu-id="203e7-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="203e7-115">**Element**</span></span>|<span data-ttu-id="203e7-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="203e7-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="203e7-117">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="203e7-117">ResolveNames</span></span>](resolvenames.md) <br/> |<span data-ttu-id="203e7-118">定义用于解析不明确名称的请求。</span><span class="sxs-lookup"><span data-stu-id="203e7-118">Defines a request to resolve ambiguous names.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="203e7-119">文本值</span><span class="sxs-lookup"><span data-stu-id="203e7-119">Text value</span></span>

<span data-ttu-id="203e7-120">该文本值代表公共联系人或通讯组列表的名称。</span><span class="sxs-lookup"><span data-stu-id="203e7-120">The text value represents the name of a public contact or distribution list.</span></span> <span data-ttu-id="203e7-121">字符串的最小长度为一个字符。</span><span class="sxs-lookup"><span data-stu-id="203e7-121">The minimum length of the string is one character.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="203e7-122">备注</span><span class="sxs-lookup"><span data-stu-id="203e7-122">Remarks</span></span>

<span data-ttu-id="203e7-123">此元素的文本值用于针对以下字段解析名称：</span><span class="sxs-lookup"><span data-stu-id="203e7-123">The text value of this element is used to resolve names against the following fields:</span></span>
  
- <span data-ttu-id="203e7-124">名</span><span class="sxs-lookup"><span data-stu-id="203e7-124">First name</span></span>
    
- <span data-ttu-id="203e7-125">姓</span><span class="sxs-lookup"><span data-stu-id="203e7-125">Last name</span></span>
    
- <span data-ttu-id="203e7-126">可分辨名称 (DN)</span><span class="sxs-lookup"><span data-stu-id="203e7-126">Display name</span></span>
    
- <span data-ttu-id="203e7-127">全名</span><span class="sxs-lookup"><span data-stu-id="203e7-127">Full name</span></span>
    
- <span data-ttu-id="203e7-128">Office</span><span class="sxs-lookup"><span data-stu-id="203e7-128">Office</span></span>
    
- <span data-ttu-id="203e7-129">别名</span><span class="sxs-lookup"><span data-stu-id="203e7-129">Alias</span></span>
    
- <span data-ttu-id="203e7-130">SMTP 地址</span><span class="sxs-lookup"><span data-stu-id="203e7-130">SMTP address</span></span>
    
<span data-ttu-id="203e7-131">带有前缀路由类型（如 smtp 或 sip）的电子邮件地址保存在多值数组中。</span><span class="sxs-lookup"><span data-stu-id="203e7-131">Email addresses with prefixed routing types, such as smtp or sip, are saved in a multivalue array.</span></span> <span data-ttu-id="203e7-132">当您在未解析名称的开头添加路由类型（如 "sip:User1@Contoso.com"）时， [ResolveNames 操作](resolvenames-operation.md)将对该数组的每个值执行部分匹配。</span><span class="sxs-lookup"><span data-stu-id="203e7-132">The [ResolveNames operation](resolvenames-operation.md) performs a partial match against each value of that array when you add the routing type at the beginning of the unresolved name, such as "sip:User1@Contoso.com".</span></span> <span data-ttu-id="203e7-133">如果不指定路由类型， **ResolveNames**操作将默认为 smtp 的路由类型，将其与主 smtp 地址属性相匹配，而不会搜索多值数组。</span><span class="sxs-lookup"><span data-stu-id="203e7-133">If you don't specify a routing type, the **ResolveNames** operation will default to the routing type of smtp, match it to a primary SMTP address property, and not search the multivalue array.</span></span> 
  
<span data-ttu-id="203e7-134">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="203e7-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="203e7-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="203e7-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="203e7-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="203e7-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="203e7-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="203e7-137">Schema Name</span></span>  <br/> |<span data-ttu-id="203e7-138">消息架构</span><span class="sxs-lookup"><span data-stu-id="203e7-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="203e7-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="203e7-139">Validation File</span></span>  <br/> |<span data-ttu-id="203e7-140">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="203e7-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="203e7-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="203e7-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="203e7-142">False</span><span class="sxs-lookup"><span data-stu-id="203e7-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="203e7-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="203e7-143">See also</span></span>



[<span data-ttu-id="203e7-144">ResolveNames 操作</span><span class="sxs-lookup"><span data-stu-id="203e7-144">ResolveNames operation</span></span>](resolvenames-operation.md)


- [<span data-ttu-id="203e7-145">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="203e7-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

