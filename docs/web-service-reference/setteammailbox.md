---
title: SetTeamMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d6ee7cc-8f88-4de2-ae5c-cabf2f2193d0
description: SetTeamMailbox元素中包含的请求设置网站邮箱。
ms.openlocfilehash: 708863168f4e89775deee8c5d66427df41515089
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827455"
---
# <a name="setteammailbox"></a><span data-ttu-id="f50ec-103">SetTeamMailbox</span><span class="sxs-lookup"><span data-stu-id="f50ec-103">SetTeamMailbox</span></span>

<span data-ttu-id="f50ec-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **SetTeamMailbox**元素中包含的请求设置网站邮箱。</span><span class="sxs-lookup"><span data-stu-id="f50ec-104">The **SetTeamMailbox** element contains a request to set a site mailbox.</span></span> 
  
```XML
<SetTeamMailbox>
   <EmailAddress/>
   <SharePointSiteUrl/>
   <State/>
</SetTeamMailbox>
```

 <span data-ttu-id="f50ec-105">**SetTeamMailboxRequestType**</span><span class="sxs-lookup"><span data-stu-id="f50ec-105">**SetTeamMailboxRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f50ec-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f50ec-106">Attributes and elements</span></span>

<span data-ttu-id="f50ec-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f50ec-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f50ec-108">属性</span><span class="sxs-lookup"><span data-stu-id="f50ec-108">Attributes</span></span>

<span data-ttu-id="f50ec-109">无。</span><span class="sxs-lookup"><span data-stu-id="f50ec-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f50ec-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f50ec-110">Child elements</span></span>

<span data-ttu-id="f50ec-111">[EmailAddress (EmailAddressType)](emailaddress-emailaddresstype.md) | [SharePointSiteUrl](sharepointsiteurl.md) | [状态 (TeamMailboxLifecycleStateType)](state-teammailboxlifecyclestatetype.md)</span><span class="sxs-lookup"><span data-stu-id="f50ec-111">[EmailAddress (EmailAddressType)](emailaddress-emailaddresstype.md) | [SharePointSiteUrl](sharepointsiteurl.md) | [State (TeamMailboxLifecycleStateType)](state-teammailboxlifecyclestatetype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f50ec-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f50ec-112">Parent elements</span></span>

<span data-ttu-id="f50ec-113">无。</span><span class="sxs-lookup"><span data-stu-id="f50ec-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f50ec-114">备注</span><span class="sxs-lookup"><span data-stu-id="f50ec-114">Remarks</span></span>

<span data-ttu-id="f50ec-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f50ec-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f50ec-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f50ec-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f50ec-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="f50ec-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f50ec-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="f50ec-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f50ec-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="f50ec-119">Schema name</span></span>  <br/> |<span data-ttu-id="f50ec-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="f50ec-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f50ec-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="f50ec-121">Validation file</span></span>  <br/> |<span data-ttu-id="f50ec-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f50ec-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f50ec-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="f50ec-123">Can be empty</span></span>  <br/> ||
   

