---
title: MailboxSearchScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ef4a4203-61e5-46b8-9fa4-d1a10e785aa2
description: MailboxSearchScope 元素指定用于发现搜索的邮箱和搜索范围。
ms.openlocfilehash: 20f528ddfb4812de8468af33bcb0b47d7d851f1d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457184"
---
# <a name="mailboxsearchscope"></a><span data-ttu-id="25459-103">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="25459-103">MailboxSearchScope</span></span>

<span data-ttu-id="25459-104">**MailboxSearchScope**元素指定用于发现搜索的邮箱和搜索范围。</span><span class="sxs-lookup"><span data-stu-id="25459-104">The **MailboxSearchScope** element specifies a mailbox and a search scope for a discovery search.</span></span> 
  
```XML
<MailboxSearchScope>
   <Mailbox/>
   <SearchScope/>
<MailboxSearchScope>
```

<span data-ttu-id="25459-105">**MailboxSearchScopeType**</span><span class="sxs-lookup"><span data-stu-id="25459-105">**MailboxSearchScopeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="25459-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="25459-106">Attributes and elements</span></span>

<span data-ttu-id="25459-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="25459-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25459-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="25459-108">Attributes</span></span>

<span data-ttu-id="25459-109">无。</span><span class="sxs-lookup"><span data-stu-id="25459-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="25459-110">子元素</span><span class="sxs-lookup"><span data-stu-id="25459-110">Child elements</span></span>

<span data-ttu-id="25459-111">[邮箱（字符串）](mailbox-string.md)  | [SearchScope](searchscope.md)</span><span class="sxs-lookup"><span data-stu-id="25459-111">[Mailbox (string)](mailbox-string.md) | [SearchScope](searchscope.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="25459-112">父元素</span><span class="sxs-lookup"><span data-stu-id="25459-112">Parent elements</span></span>

[<span data-ttu-id="25459-113">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="25459-113">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
  
## <a name="remarks"></a><span data-ttu-id="25459-114">备注</span><span class="sxs-lookup"><span data-stu-id="25459-114">Remarks</span></span>

<span data-ttu-id="25459-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="25459-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="25459-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="25459-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="25459-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="25459-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25459-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="25459-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="25459-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="25459-119">Schema name</span></span>  <br/> |<span data-ttu-id="25459-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="25459-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="25459-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="25459-121">Validation file</span></span>  <br/> |<span data-ttu-id="25459-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="25459-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="25459-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="25459-123">Can be empty</span></span>  <br/> ||
   

