---
title: MailboxHoldResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da03b877-37c6-4ecb-8549-c639f140302e
description: MailboxHoldResult 元素包含 GetHoldOnMailboxes 请求的结果。
ms.openlocfilehash: 333a2d2d4a30a63a78660d167cefe75653f8ea82
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826289"
---
# <a name="mailboxholdresult"></a><span data-ttu-id="c6730-103">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="c6730-103">MailboxHoldResult</span></span>

<span data-ttu-id="c6730-104">**MailboxHoldResult**元素包含**GetHoldOnMailboxes**请求的结果。</span><span class="sxs-lookup"><span data-stu-id="c6730-104">The **MailboxHoldResult** element contains the result of the **GetHoldOnMailboxes** request.</span></span> 
  
```XML
<MailboxHoldResult>
   <HoldId/>
   <Query/>
   <MailboxHoldStatuses/>
</MailboxHoldResult>
```

<span data-ttu-id="c6730-105">**MailboxHoldResultType**</span><span class="sxs-lookup"><span data-stu-id="c6730-105">**MailboxHoldResultType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c6730-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c6730-106">Attributes and elements</span></span>

<span data-ttu-id="c6730-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c6730-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6730-108">属性</span><span class="sxs-lookup"><span data-stu-id="c6730-108">Attributes</span></span>

<span data-ttu-id="c6730-109">无。</span><span class="sxs-lookup"><span data-stu-id="c6730-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c6730-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c6730-110">Child elements</span></span>

<span data-ttu-id="c6730-111">[HoldId](holdid.md) | [查询](query.md) | [MailboxHoldStatuses](mailboxholdstatuses.md)</span><span class="sxs-lookup"><span data-stu-id="c6730-111">[HoldId](holdid.md) | [Query](query.md) | [MailboxHoldStatuses](mailboxholdstatuses.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c6730-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c6730-112">Parent elements</span></span>

<span data-ttu-id="c6730-113">无。</span><span class="sxs-lookup"><span data-stu-id="c6730-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c6730-114">备注</span><span class="sxs-lookup"><span data-stu-id="c6730-114">Remarks</span></span>

<span data-ttu-id="c6730-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c6730-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c6730-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c6730-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c6730-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="c6730-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6730-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="c6730-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c6730-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="c6730-119">Schema name</span></span>  <br/> |<span data-ttu-id="c6730-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="c6730-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c6730-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="c6730-121">Validation file</span></span>  <br/> |<span data-ttu-id="c6730-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c6730-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c6730-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="c6730-123">Can be empty</span></span>  <br/> ||
   
