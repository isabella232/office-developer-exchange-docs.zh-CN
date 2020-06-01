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
ms.openlocfilehash: 3895c1351587db45881c661809a19dad1929b4a9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466393"
---
# <a name="mailboxholdresult"></a><span data-ttu-id="00886-103">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="00886-103">MailboxHoldResult</span></span>

<span data-ttu-id="00886-104">**MailboxHoldResult**元素包含**GetHoldOnMailboxes**请求的结果。</span><span class="sxs-lookup"><span data-stu-id="00886-104">The **MailboxHoldResult** element contains the result of the **GetHoldOnMailboxes** request.</span></span> 
  
```XML
<MailboxHoldResult>
   <HoldId/>
   <Query/>
   <MailboxHoldStatuses/>
</MailboxHoldResult>
```

<span data-ttu-id="00886-105">**MailboxHoldResultType**</span><span class="sxs-lookup"><span data-stu-id="00886-105">**MailboxHoldResultType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="00886-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="00886-106">Attributes and elements</span></span>

<span data-ttu-id="00886-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="00886-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="00886-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="00886-108">Attributes</span></span>

<span data-ttu-id="00886-109">无。</span><span class="sxs-lookup"><span data-stu-id="00886-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="00886-110">子元素</span><span class="sxs-lookup"><span data-stu-id="00886-110">Child elements</span></span>

<span data-ttu-id="00886-111">[HoldId](holdid.md)  | [查询](query.md)  | [MailboxHoldStatuses](mailboxholdstatuses.md)</span><span class="sxs-lookup"><span data-stu-id="00886-111">[HoldId](holdid.md) | [Query](query.md) | [MailboxHoldStatuses](mailboxholdstatuses.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="00886-112">父元素</span><span class="sxs-lookup"><span data-stu-id="00886-112">Parent elements</span></span>

<span data-ttu-id="00886-113">无。</span><span class="sxs-lookup"><span data-stu-id="00886-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00886-114">说明</span><span class="sxs-lookup"><span data-stu-id="00886-114">Remarks</span></span>

<span data-ttu-id="00886-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="00886-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="00886-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="00886-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="00886-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="00886-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00886-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="00886-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="00886-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="00886-119">Schema name</span></span>  <br/> |<span data-ttu-id="00886-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="00886-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="00886-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="00886-121">Validation file</span></span>  <br/> |<span data-ttu-id="00886-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="00886-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="00886-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="00886-123">Can be empty</span></span>  <br/> ||
   

