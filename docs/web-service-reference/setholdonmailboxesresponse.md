---
title: SetHoldOnMailboxesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 909194d6-e2b1-4774-bf29-04ed4318df1d
description: SetHoldOnMailboxesResponse 元素均表示 SetHoldOnMailboxes 请求的响应。
ms.openlocfilehash: bb1d64b98f5e1ab4cdbe4a297ded46d00b27b364
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827418"
---
# <a name="setholdonmailboxesresponse"></a><span data-ttu-id="2fb5c-103">SetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="2fb5c-103">SetHoldOnMailboxesResponse</span></span>

<span data-ttu-id="2fb5c-104">**SetHoldOnMailboxesResponse**元素均表示**SetHoldOnMailboxes**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="2fb5c-104">The **SetHoldOnMailboxesResponse** element represents a response to a **SetHoldOnMailboxes** request.</span></span> 
  
```XML
<SetHoldOnMailboxesResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MailboxHoldResult/>
</SetHoldOnMailboxesResponse>
```

 <span data-ttu-id="2fb5c-105">**SetHoldOnMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2fb5c-105">**SetHoldOnMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2fb5c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2fb5c-106">Attributes and elements</span></span>

<span data-ttu-id="2fb5c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2fb5c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2fb5c-108">属性</span><span class="sxs-lookup"><span data-stu-id="2fb5c-108">Attributes</span></span>

<span data-ttu-id="2fb5c-109">无。</span><span class="sxs-lookup"><span data-stu-id="2fb5c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2fb5c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2fb5c-110">Child elements</span></span>

<span data-ttu-id="2fb5c-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [MailboxHoldResult](mailboxholdresult.md)</span><span class="sxs-lookup"><span data-stu-id="2fb5c-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [MailboxHoldResult](mailboxholdresult.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2fb5c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2fb5c-112">Parent elements</span></span>

<span data-ttu-id="2fb5c-113">无。</span><span class="sxs-lookup"><span data-stu-id="2fb5c-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2fb5c-114">备注</span><span class="sxs-lookup"><span data-stu-id="2fb5c-114">Remarks</span></span>

<span data-ttu-id="2fb5c-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2fb5c-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2fb5c-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2fb5c-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2fb5c-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="2fb5c-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2fb5c-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="2fb5c-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2fb5c-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="2fb5c-119">Schema name</span></span>  <br/> |<span data-ttu-id="2fb5c-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="2fb5c-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2fb5c-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="2fb5c-121">Validation file</span></span>  <br/> |<span data-ttu-id="2fb5c-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2fb5c-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2fb5c-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="2fb5c-123">Can be empty</span></span>  <br/> |<span data-ttu-id="2fb5c-124">false</span><span class="sxs-lookup"><span data-stu-id="2fb5c-124">false</span></span>  <br/> |
   

