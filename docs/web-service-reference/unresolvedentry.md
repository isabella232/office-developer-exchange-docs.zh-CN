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
ms.openlocfilehash: 98b447cd49685b49f73f75f12d921a65749be245
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838348"
---
# <a name="unresolvedentry"></a><span data-ttu-id="4713e-103">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="4713e-103">UnresolvedEntry</span></span>

<span data-ttu-id="4713e-104">**UnresolvedEntry**元素包含要解析的联系人或通讯组列表的名称。</span><span class="sxs-lookup"><span data-stu-id="4713e-104">The **UnresolvedEntry** element contains the name of a contact or distribution list to resolve.</span></span> 
  
[<span data-ttu-id="4713e-105">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="4713e-105">ResolveNames</span></span>](resolvenames.md)
  
[<span data-ttu-id="4713e-106">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="4713e-106">UnresolvedEntry</span></span>](unresolvedentry.md)
  
```xml
<UnresolvedEntry/>
```

 <span data-ttu-id="4713e-107">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="4713e-107">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4713e-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4713e-108">Attributes and elements</span></span>

<span data-ttu-id="4713e-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4713e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4713e-110">属性</span><span class="sxs-lookup"><span data-stu-id="4713e-110">Attributes</span></span>

<span data-ttu-id="4713e-111">无。</span><span class="sxs-lookup"><span data-stu-id="4713e-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4713e-112">子元素</span><span class="sxs-lookup"><span data-stu-id="4713e-112">Child elements</span></span>

<span data-ttu-id="4713e-113">无。</span><span class="sxs-lookup"><span data-stu-id="4713e-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4713e-114">父元素</span><span class="sxs-lookup"><span data-stu-id="4713e-114">Parent elements</span></span>

|<span data-ttu-id="4713e-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="4713e-115">**Element**</span></span>|<span data-ttu-id="4713e-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="4713e-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4713e-117">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="4713e-117">ResolveNames</span></span>](resolvenames.md) <br/> |<span data-ttu-id="4713e-118">定义请求解析模糊名称。</span><span class="sxs-lookup"><span data-stu-id="4713e-118">Defines a request to resolve ambiguous names.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4713e-119">文本值</span><span class="sxs-lookup"><span data-stu-id="4713e-119">Text value</span></span>

<span data-ttu-id="4713e-120">文本值表示公共联系人或通讯组列表的名称。</span><span class="sxs-lookup"><span data-stu-id="4713e-120">The text value represents the name of a public contact or distribution list.</span></span> <span data-ttu-id="4713e-121">字符串的最小长度是一个字符。</span><span class="sxs-lookup"><span data-stu-id="4713e-121">The minimum length of the string is one character.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4713e-122">注解</span><span class="sxs-lookup"><span data-stu-id="4713e-122">Remarks</span></span>

<span data-ttu-id="4713e-123">此元素的文本值用于解析名称针对以下字段：</span><span class="sxs-lookup"><span data-stu-id="4713e-123">The text value of this element is used to resolve names against the following fields:</span></span>
  
- <span data-ttu-id="4713e-124">名</span><span class="sxs-lookup"><span data-stu-id="4713e-124">First name</span></span>
    
- <span data-ttu-id="4713e-125">姓</span><span class="sxs-lookup"><span data-stu-id="4713e-125">Last name</span></span>
    
- <span data-ttu-id="4713e-126">显示名称</span><span class="sxs-lookup"><span data-stu-id="4713e-126">Display name</span></span>
    
- <span data-ttu-id="4713e-127">全名</span><span class="sxs-lookup"><span data-stu-id="4713e-127">Full name</span></span>
    
- <span data-ttu-id="4713e-128">Office</span><span class="sxs-lookup"><span data-stu-id="4713e-128">Office</span></span>
    
- <span data-ttu-id="4713e-129">Alias</span><span class="sxs-lookup"><span data-stu-id="4713e-129">Alias</span></span>
    
- <span data-ttu-id="4713e-130">SMTP 地址</span><span class="sxs-lookup"><span data-stu-id="4713e-130">SMTP address</span></span>
    
<span data-ttu-id="4713e-131">多值数组中保存前缀的路由类型，如 smtp 或 sip，与电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="4713e-131">Email addresses with prefixed routing types, such as smtp or sip, are saved in a multivalue array.</span></span> <span data-ttu-id="4713e-132">无法解析的名称，例如"sip:User1@Contoso.com"的开头添加路由类型时， [ResolveNames 操作](resolvenames-operation.md)执行针对该数组的每个值的部分匹配。</span><span class="sxs-lookup"><span data-stu-id="4713e-132">The [ResolveNames operation](resolvenames-operation.md) performs a partial match against each value of that array when you add the routing type at the beginning of the unresolved name, such as "sip:User1@Contoso.com".</span></span> <span data-ttu-id="4713e-133">如果不指定传送类型， **ResolveNames**操作将默认为 smtp 的路由类型、 匹配到主 SMTP 地址属性，和搜索多值数组。</span><span class="sxs-lookup"><span data-stu-id="4713e-133">If you don't specify a routing type, the **ResolveNames** operation will default to the routing type of smtp, match it to a primary SMTP address property, and not search the multivalue array.</span></span> 
  
<span data-ttu-id="4713e-134">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4713e-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4713e-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="4713e-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4713e-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="4713e-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4713e-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="4713e-137">Schema Name</span></span>  <br/> |<span data-ttu-id="4713e-138">消息架构</span><span class="sxs-lookup"><span data-stu-id="4713e-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4713e-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="4713e-139">Validation File</span></span>  <br/> |<span data-ttu-id="4713e-140">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4713e-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4713e-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="4713e-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="4713e-142">False</span><span class="sxs-lookup"><span data-stu-id="4713e-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4713e-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4713e-143">See also</span></span>



[<span data-ttu-id="4713e-144">ResolveNames 操作</span><span class="sxs-lookup"><span data-stu-id="4713e-144">ResolveNames operation</span></span>](resolvenames-operation.md)


- [<span data-ttu-id="4713e-145">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4713e-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

