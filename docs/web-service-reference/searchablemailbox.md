---
title: SearchableMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 339005cd-a3b9-47dd-bc7b-a860b699625b
description: SearchableMailbox元素指定邮箱GetSearchableMailboxes请求中返回。
ms.openlocfilehash: 0d0981d050fa388e83eaa8408b60d305296c1f36
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827284"
---
# <a name="searchablemailbox"></a><span data-ttu-id="8ef44-103">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="8ef44-103">SearchableMailbox</span></span>

<span data-ttu-id="8ef44-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **SearchableMailbox**元素指定邮箱 **GetSearchableMailboxes**请求中返回。</span><span class="sxs-lookup"><span data-stu-id="8ef44-104">The **SearchableMailbox** element specifies a mailbox returned from a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<SearchableMailbox>
   <Guid/>
   <PrimarySmtpAddress/>
   <IsExternalMailbox/>
   <ExternalEmailAddress/>
   <DisplayName/>
   <IsMembershipGroup/>
   <ReferenceId/>
</SearchableMailbox>
```

 <span data-ttu-id="8ef44-105">**SearchableMailboxType**</span><span class="sxs-lookup"><span data-stu-id="8ef44-105">**SearchableMailboxType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8ef44-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8ef44-106">Attributes and elements</span></span>

<span data-ttu-id="8ef44-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8ef44-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8ef44-108">属性</span><span class="sxs-lookup"><span data-stu-id="8ef44-108">Attributes</span></span>

<span data-ttu-id="8ef44-109">无。</span><span class="sxs-lookup"><span data-stu-id="8ef44-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8ef44-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8ef44-110">Child elements</span></span>

<span data-ttu-id="8ef44-111">[Guid](guid-ex15websvcsotherref.md) | [PrimarySmtpAddress (字符串)](primarysmtpaddress-string.md) | [IsExternalMailbox](isexternalmailbox.md) | [ExternalEmailAddress](externalemailaddress.md) | [显示名称 (字符串)](displayname-string.md) | [IsMembershipGroup](ismembershipgroup.md) | [ReferenceId](referenceid.md)</span><span class="sxs-lookup"><span data-stu-id="8ef44-111">[Guid](guid-ex15websvcsotherref.md) | [PrimarySmtpAddress (string)](primarysmtpaddress-string.md) | [IsExternalMailbox](isexternalmailbox.md) | [ExternalEmailAddress](externalemailaddress.md) | [DisplayName (string)](displayname-string.md) | [IsMembershipGroup](ismembershipgroup.md) | [ReferenceId](referenceid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8ef44-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8ef44-112">Parent elements</span></span>

[<span data-ttu-id="8ef44-113">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="8ef44-113">SearchableMailboxes</span></span>](searchablemailboxes.md)
  
## <a name="remarks"></a><span data-ttu-id="8ef44-114">备注</span><span class="sxs-lookup"><span data-stu-id="8ef44-114">Remarks</span></span>

<span data-ttu-id="8ef44-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8ef44-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8ef44-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8ef44-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8ef44-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="8ef44-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ef44-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="8ef44-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8ef44-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="8ef44-119">Schema name</span></span>  <br/> |<span data-ttu-id="8ef44-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="8ef44-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="8ef44-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="8ef44-121">Validation file</span></span>  <br/> |<span data-ttu-id="8ef44-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8ef44-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8ef44-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="8ef44-123">Can be empty</span></span>  <br/> ||
   

