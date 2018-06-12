---
title: UnpinTeamMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1034b013-ef34-4e72-99b3-38bff475b3e8
description: UnpinTeamMailbox元素包含从Autodiscover响应删除脱离网站邮箱从客户端的请求。
ms.openlocfilehash: d303b47f0796f9bec7e9f198afa81d2ecd9fd5cd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838343"
---
# <a name="unpinteammailbox"></a><span data-ttu-id="0e732-103">UnpinTeamMailbox</span><span class="sxs-lookup"><span data-stu-id="0e732-103">UnpinTeamMailbox</span></span>

<span data-ttu-id="0e732-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **UnpinTeamMailbox**元素包含从 **Autodiscover**响应删除脱离网站邮箱从客户端的请求。</span><span class="sxs-lookup"><span data-stu-id="0e732-104">The **UnpinTeamMailbox** element contains the request to unpin a site mailbox from the client by removing it from the **Autodiscover** response.</span></span> 
  
```XML
<UnpinTeamMailbox>
   <EmailAddress/>
</UnpinTeamMailbox>
```

 <span data-ttu-id="0e732-105">**UnpinTeamMailboxRequestType**</span><span class="sxs-lookup"><span data-stu-id="0e732-105">**UnpinTeamMailboxRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0e732-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0e732-106">Attributes and elements</span></span>

<span data-ttu-id="0e732-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0e732-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0e732-108">属性</span><span class="sxs-lookup"><span data-stu-id="0e732-108">Attributes</span></span>

<span data-ttu-id="0e732-109">无。</span><span class="sxs-lookup"><span data-stu-id="0e732-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0e732-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0e732-110">Child elements</span></span>

[<span data-ttu-id="0e732-111">EmailAddress (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="0e732-111">EmailAddress (EmailAddressType)</span></span>](emailaddress-emailaddresstype.md)
  
### <a name="parent-elements"></a><span data-ttu-id="0e732-112">父元素</span><span class="sxs-lookup"><span data-stu-id="0e732-112">Parent elements</span></span>

<span data-ttu-id="0e732-113">无。</span><span class="sxs-lookup"><span data-stu-id="0e732-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0e732-114">备注</span><span class="sxs-lookup"><span data-stu-id="0e732-114">Remarks</span></span>

<span data-ttu-id="0e732-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0e732-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0e732-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0e732-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0e732-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="0e732-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e732-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="0e732-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0e732-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="0e732-119">Schema name</span></span>  <br/> |<span data-ttu-id="0e732-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="0e732-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0e732-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="0e732-121">Validation file</span></span>  <br/> |<span data-ttu-id="0e732-122">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0e732-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0e732-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="0e732-123">Can be empty</span></span>  <br/> ||
   

