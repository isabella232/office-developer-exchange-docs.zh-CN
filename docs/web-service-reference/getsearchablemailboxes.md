---
title: GetSearchableMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 949871f7-0d10-498e-84aa-f0652f1193be
description: GetSearchableMailboxes 元素包含一个请求，用于获取客户端有权执行电子数据展示搜索的邮箱列表。
ms.openlocfilehash: a327f8766e53e9f1fae6928179d5a4b8e3d044a8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530188"
---
# <a name="getsearchablemailboxes"></a><span data-ttu-id="5541d-103">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="5541d-103">GetSearchableMailboxes</span></span>

<span data-ttu-id="5541d-104">**GetSearchableMailboxes**元素包含一个请求，用于获取客户端有权执行电子数据展示搜索的邮箱列表。</span><span class="sxs-lookup"><span data-stu-id="5541d-104">The **GetSearchableMailboxes** element contains a request to get a list of mailboxes that the client has permission to perform an eDiscovery search.</span></span> 
  
```XML
<GetSearchableMailboxes>
   <SearchFilter/>
   <ExpandGroupMembership/>
</GetSearchableMailboxes>
```

 <span data-ttu-id="5541d-105">**GetSearchableMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="5541d-105">**GetSearchableMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5541d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5541d-106">Attributes and elements</span></span>

<span data-ttu-id="5541d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5541d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5541d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="5541d-108">Attributes</span></span>

<span data-ttu-id="5541d-109">无。</span><span class="sxs-lookup"><span data-stu-id="5541d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5541d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5541d-110">Child elements</span></span>

<span data-ttu-id="5541d-111">[过滤](searchfilter.md)  | [ExpandGroupMembership](expandgroupmembership.md)</span><span class="sxs-lookup"><span data-stu-id="5541d-111">[SearchFilter](searchfilter.md) | [ExpandGroupMembership](expandgroupmembership.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5541d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="5541d-112">Parent elements</span></span>

<span data-ttu-id="5541d-113">无。</span><span class="sxs-lookup"><span data-stu-id="5541d-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5541d-114">说明</span><span class="sxs-lookup"><span data-stu-id="5541d-114">Remarks</span></span>

<span data-ttu-id="5541d-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5541d-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5541d-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5541d-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5541d-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="5541d-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5541d-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="5541d-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5541d-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="5541d-119">Schema name</span></span>  <br/> |<span data-ttu-id="5541d-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="5541d-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5541d-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="5541d-121">Validation file</span></span>  <br/> |<span data-ttu-id="5541d-122">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="5541d-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5541d-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="5541d-123">Can be empty</span></span>  <br/> ||
   

